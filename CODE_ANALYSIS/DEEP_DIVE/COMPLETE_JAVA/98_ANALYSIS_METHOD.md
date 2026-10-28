# Java 코드 분석 문서의 생성 방식

이 설명용 Markdown에는 **게임 실행 기능이 없는 코드 분석 절차 예시**를 기록한다. 프로그램 소스나 Gradle 파일을 변경하지 않으며, 아래 예시는 실제 Java 파일의 정적 선언·호출 표현을 문서화하는 데만 사용한다.

이 추출기는 AST/컴파일러가 아니다. 여러 줄 선언, 익명 클래스, 동적 디스패치, 긴 메서드, 중괄호가 등장하는 문자열을 완전하게 처리하지 못할 수 있다. 메서드의 기능 분류는 이름·코드 내 표면 패턴에 따른 **추론 후보**다. 분석을 검증한 것으로 잘못 주장하지 않는다.

~~~javascript
(data,paths,repo,ref,start)=>{
const bt=String.fromCharCode(96),link=(p,n)=>'https://github.com/'+repo+'/blob/'+ref+'/'+p+(n?'#L'+n:'');
const roles=[[/^(act|update|evolve|process)/,'시간·상태 갱신'],[/^(create|build|init|setup|reset)/,'생성·초기화'],[/^(save|store|load|restore)/,'저장·복원'],[/^(attack|damage|hit|defense)/,'전투 관련'],[/^(paint|draw|render|layout)/,'지형/화면 표현'],[/^(on|execute|use|zap|cast|activate|trigger)/,'이벤트·효과 실행'],[/^(can|is|has|check)/,'조건 판정'],[/^(get|find|search|select)/,'조회·탐색'],[/^(set|add|remove|clear)/,'상태 갱신']];
let md='# Java 파일별 소스 구현 해설 '+(start+1)+'–'+(start+data.length)+'\n\n실제 소스 기준 '+bt+ref+bt+'. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.\n\n';
let stats={files:data.length,failed:0,types:0,fields:0,methods:0};
for(let i=0;i<data.length;i++){
let f=data[i],p=f.path;md+='## '+(start+i+1)+'. ['+bt+p.split('/').pop()+bt+']('+link(p)+')\n\n';if(f.error){stats.failed++;md+='읽기 실패: '+f.error+'\n\n';continue;}
let lines=f.src.split('\n'),cls=[],fld=[],meth=[];
for(let k=0;k<lines.length;k++){
let t=lines[k].trim();if(t.startsWith('//')||t.startsWith('*')||t.startsWith('import '))continue;
let c=t.match(/(?:^|\s)(class|enum|interface)\s+(\w+)([^{]*)/);if(c)cls.push([k+1,(c[1]+' '+c[2]+' '+c[3]).trim().slice(0,130)]);
let v=t.match(/^(?:(?:public|private|protected|static|final|transient|volatile)\s+)+([\w.$<>?,\[\] ]+)\s+(\w+)\s*(?:=([^;]*))?;/);if(v&&!t.includes('('))fld.push([k+1,v[1].trim()+' '+v[2],(v[3]||'').trim().slice(0,90)]);
let sig=t;if(sig.includes('(')&&!/\)\s*(?:\{|;)/.test(sig)){for(let z=1;z<=4&&k+z<lines.length;z++){sig+=' '+lines[k+z].trim();if(/\)\s*(?:throws [\w,. ]+)?\s*(?:\{|;)/.test(sig))break;}}
let m=sig.match(/^(?:(?:public|private|protected|static|final|synchronized|abstract|native|default)\s+)+(.{0,130}?)\b(\w+)\s*\(([^{};]*)\)\s*(?:throws [\w,. ]+)?\s*(\{|;)/);
if(m){let body=lines.slice(k,k+80).join('\n'),op=body.indexOf('{'),dep=0,end=body.length;if(m[4]==='{'&&op>=0){for(let x=op;x<body.length;x++){if(body[x]==='{')dep++;if(body[x]==='}'&&--dep===0){end=x+1;break;}}body=body.slice(op,end)}else body='';body=body.replace(/\/\*[\s\S]*?\*\/|\/\/[^\n]*/g,' ');
let calls=[...new Set([...body.matchAll(/\b([\w$]+(?:\.[\w$]+){0,2})\s*\(/g)].map(x=>x[1]).filter(x=>!['if','while','for','switch','catch','return','new','super','this'].includes(x)))].slice(0,9);
let states=[/\bif\s*\(/.test(body)?'조건 분기':'',/\b(for|while)\s*\(/.test(body)?'반복':'',/\bswitch\s*\(/.test(body)?'상태 선택':'',/\btry\s*\{/.test(body)?'예외 처리':''].filter(Boolean);
let role=(roles.find(([re])=>re.test(m[2]))||[])[1]||'개별 처리';meth.push([k+1,m[2],m[3].trim().replace(/\|/g,'\\|').slice(0,120),role,states,calls]);}
}
stats.types+=cls.length;stats.fields+=fld.length;stats.methods+=meth.length;
let pkg=(f.src.match(/^\s*package\s+([\w.]+);/m)||[])[1]||'없음';md+='패키지: '+bt+pkg+bt+' / 본문 '+lines.length+'행 / 타입 '+cls.length+'개 / 필드 '+fld.length+'개 / 메서드 '+meth.length+'개.\n\n';
md+='### 타입·상속 선언\n\n'+(cls.map(x=>'- [L'+x[0]+']('+link(p,x[0])+') '+bt+x[1]+bt).join('\n')||'- 검출 없음')+'\n\n';
md+='### 변수·상수 (단일 행 선언)\n\n'+(fld.map(x=>'- [L'+x[0]+']('+link(p,x[0])+') '+bt+x[1]+bt+(x[2]?' 초기식: '+bt+x[2]+bt:'')).join('\n')||'- 검출 없음')+'\n\n';
md+='### 함수·메서드 역할과 내부 연결\n\n'+(meth.map(x=>'- [L'+x[0]+']('+link(p,x[0])+') **'+bt+x[1]+'('+x[2]+')'+bt+'**: '+x[3]+(x[4].length?' / '+x[4].join('·'):'')+(x[5].length?' / 참조 호출: '+x[5].join(', '):'')).join('\n')||'- 검출 없음')+'\n\n';
md+='**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.\n\n';
}
md+='## 정적 분석 수치\n\n'+JSON.stringify(stats)+'\n';return {markdown:md,summary:stats};
}
~~~

## 문서 사용 시 주의
실제 동작은 원본 코드와 수동 해설(10~23번 문서)을 우선한다. 메서드별 참조 호출은 발견한 구문이지 런타임 실행 순서를 입증한 것이 아니다.

# 모호한 이름·잠재적 오해 해설집

원칙: **이름만으로 추측하지 않는다.** 가능하면 해당 선언과 실행 경로를 함께 연결하며, 아직 보지 않은 하위 클래스의 동작을 일반화하지 않는다.

| 용어/식별자 | 잘못 해석하기 쉬운 뜻 | 이 코드에서 확인된 의미 및 추가 조건 |
|---|---|---|
| Dungeon | 현재 2차원 맵 자체 | 전역 플레이 상태, 영웅, 층, 소지 자원, 시드, 저장 로직을 묶는 클래스. 한 층의 타일은 Level |
| Level / Item.level() | 모두 현재 층 숫자 | Level은 월드 층 객체, Item.level()은 개별 아이템의 강화 수준 |
| Dungeon.depth / Dungeon.branch | 같은 단계 값 | depth는 층 깊이, branch는 분기 경로. 저장 파일명과 생성 여부 키에서 함께 사용 |
| Actor.time / Actor.now() | 실시간 벽시계 | 액터 행동 스케줄 시간; Game.realTime 등과 구분 |
| Actor.act() boolean | 공격 또는 행동 성공 | 처리 지속과 대기 흐름 관련. 하위 클래스에서 반환 경로를 확인 |
| actPriority / speed | 모두 움직이는 속도 | 동일 시점 처리 순위와 시간 소비/행동 속도는 별도 축 |
| Actor.next() | 다음 적의 턴 | 현재 액터 처리 상태를 갱신하는 메서드. 실제 선택은 Actor.process가 결정 |
| Hero.ready | 그래픽/데이터 로딩 완료 | 영웅이 다음 명령을 받을 수 있는 행동 준비 상태 맥락 |
| Hero.curAction | 사용자가 누른 키 그 자체 | Move/Attack 등 구체 행동 데이터를 담는 HeroAction 객체 |
| SPDAction | 영웅의 물리 행동 목록 | GameAction 기반 명령/키 바인딩 및 UI 입력 체계 |
| Char.HT | 체력 회복량 | HP와 별개인 체력 최대량 쪽 값. HP/HT 비율 보존 로직으로 확인 |
| Char.alignment | 화면 정렬 옵션 | 몬스터/영웅의 적대·우호 상태 관련 Alignment |
| Mob.state | int enum AI 상태 | AiState 구현 객체 참조. 서로 다른 객체가 act(...) 구현 |
| Mob.enemy / target | 완전한 동의어 | 적 참조와 위치/목표값의 저장·추적 목적이 다름 |
| Level.map / Level.passable | 동일 배열 | 지형 ID 배열과 통과 가능 플래그 배열 |
| Level.heroFOV / visited / mapped | '본 타일' 하나의 목록 | 현재 시야, 방문/지도 기록과 목적이 다른 배열 |
| Room.neigbours / connected | 같은 연결 목록 | 인접 관계와 실제 연결/문 정보를 구분 |
| Painter.paint | 픽셀 스프라이트 그림 | 절차적 맵 생성 시 타일 지형을 채우는 작업 |
| Blob | 컴퓨터 바이너리 블롭 | actors.blobs 패키지에서는 가스/불 등의 공간 영역 효과 |
| Trap.trigger / activate | 항상 같은 작업 | trigger에서 효과 발동 조건/가시성 등을 처리, 구체 효과는 activate에 위임 |
| Heap / Bag | 단순한 배열 | Heap은 바닥의 아이템 더미, Bag은 소지품 컨테이너 |
| Item.cursedKnown | 저주 여부 자체 | 저주 상태(cursed)와 플레이어의 저주 인지 여부를 별도 저장 |
| Weapon.ACC/DLY/RCH | 고정 공격력/공격속도/원거리 피해 | 각각 명중/지연/사거리 계수. 최종 전투 결과는 다수 보정 필요 |
| Item.image / icon | 둘 다 파일 경로 | 시각 표현 및 추가 이미지 구분 ID에 사용, 실제 Assets 경로와 별도 |
| Generator.random | 단순 균등 랜덤 | 분류별 확률, 덱, 소진, 별도 RNG seed 사용 |
| Random.pushGenerator | RNG 객체 1개 영구 교체 | 난수 생성기 스택에 일시적으로 push, 적절히 pop 필요 |
| seed / seedForDepth | 난수 시드 하나 | 게임 전체 시드와 층별 파생 시드. 사용자 지정 문자열/날짜 구분 |
| generatedLevels | 이미 생성된 Level 객체 목록 | depth + 1000*branch 정수 키로 생성 여부 추적 |
| limited drops | 아이템 스폰 완전 금지 목록 | LimitedDrops별 횟수·유일성 등을 관리하는 상태 |
| saveGame / saveLevel / saveAll | 모두 같은 파일에 저장 | 전체 플레이 상태 / 현재 층 상태 / 두 경로를 묶은 상위 호출 |
| version / versionCode | 같은 문자 버전 | 사용자 표시 버전명과 정수 코드/마이그레이션 기준을 구분 |
| GameScene / Dungeon.level | 둘 다 게임 실행 상태 | 화면 장면과 논리 층 상태. 화면을 닫아도 저장된 논리 상태와 역할이 다름 |
| News / Updates | 반드시 실시간 온라인 서버 | 추상 서비스 + 선택된 구현체. 지원 여부와 네트워크/오류 처리에 따라 달라짐 |
| local/global badge | 위치 기반 업적 | 게임 진행 안에서의 로컬 상태 및 전역 기록으로 분리되는 업적 저장 |

## 특히 위험한 추론 네 가지
1. **seed만 같으면 완전히 똑같다** → 같은 버전·설정·RNG 경로·생성 상태가 맞아야 재현성을 평가할 수 있음.
2. **동일 시각에 등록된 액터는 항상 등록 순서대로 움직인다** → Actor.process는 HashSet을 훑어 시간을 비교하고 동률의 높은 priority를 선택함. 동일 시간·동일 priority 시 등록 순서 보장은 코드에 없음.
3. **모든 몬스터는 항상 적이다** → Mob은 ENEMY로 시작하지만 하위 클래스/버프/아군화 등으로 역할이 달라질 수 있음.
4. **모든 파일을 분석했다** → Git 트리의 전체 경로 수집과 각 파일 구현의 내용 검증은 별개다. 실제로 내용 분석한 중심 클래스를 나눠 표기.

## 근거
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java:180-214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L180-L214), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java:37-59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L37-L59), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java:250-344](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L250-L344), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java:829-948](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L829-L948), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java:111-143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L111-L143), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java:153-198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java#L153-L198), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java:37-43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L37-L43), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java:73-103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L73-L103), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java:620-750](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L620-L750).

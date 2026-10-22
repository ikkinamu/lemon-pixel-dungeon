# 자산·텍스트·다국어·화면 표현

## 1. 실제 트리에서 확인한 자산 분포
기준 커밋 bd3a990254e4249458816f4879e93ab87275555b, core/src/main/assets 아래 **460개 파일**:
- messages 207개
- sprites 78개
- sounds 67개
- music 31개
- environment 28개
- interfaces 21개
- splashes 15개
- effects 6개
- gdx 5개
- fonts 2개

별도로 desktop/src/main/assets 아래 9개(icons 8, fonts 1), ios/assets 아래 57개(music 31, Assets.xcassets 24, storyboard, privacy metadata).

**파일 수는 자산의 실제 '종류 수'와 같지 않다.** spritesheet 한 장에 여러 게임 그래픽이 들어갈 수 있다.

## 2. Assets.java: 경로 레지스트리
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java)에는 Effects, Environment, Fonts, Interfaces, Messages, Music, Sounds, Splashes, Title, Sprites 등의 정적 중첩 클래스가 있다.
이 클래스는 리소스 파일 경로 상수를 선언한다. 렌더링 라이브러리 자체도 아니고 자산 데이터를 배열로 전부 포함한 것만은 아니다.

그림이 화면에 나오려면 보통:
~~~
Assets.* 경로 상수
 -> 리소스 로딩
 -> Sprite/ItemSprite/Tilemap/UI 컴포넌트가 사용
 -> GameScene/PixelScene에서 배치 및 렌더링
~~~
개별 사용처는 해당 스프라이트/맵/창 코드를 따라가야 정확해진다.

## 3. 다국어
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java:46-165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L46-L165): 언어별 번들을 연결하고 클래스/키 기반 텍스트를 조회. lang()/locale()/setup()/get()/format() 등의 API.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java): 언어 코드, 표시명, 번역 상태, 번역 담당자 정보를 가진 enum.
- core/src/main/assets/messages에 다수의 현지화 파일이 존재.

**중요:** Messages.get(this, "name")과 Messages.get(Class, "name")은 호출 맥락 및 키 탐색 방식이 다를 수 있다. UI 문구가 Java 문자열 리터럴에 없다고 번역이 없는 것은 아니다. 번역 파일 경로와 키 매핑을 함께 조사해야 한다.
Messages.NO_TEXT_FOUND = "!!!NO TEXT FOUND!!!"라는 누락 문자열 표식이 존재함.

## 4. 글꼴·플랫폼
AndroidPlatformSupport에 한글/중국어/일본어 범위의 매칭 및 개별 글꼴 생성기 로직이 확인됨. DesktopPlatformSupport 역시 서구 문자/아시아 문자용 글꼴 생성 경로를 다룸.
다국어 문제는 Messages 번역 키와 FreeType 글꼴 선택·렌더링을 분리해서 진단해야 한다.

## 5. Sprite와 게임 규칙의 관계
- sprites/는 캐릭터 및 아이템의 시각 표현을 담당하는 Java 코드군.
- tiles/는 지형 표현/안개/벽 가림 등의 레이어를 다룸.
- effects/particles/는 시각 효과 관련 파일.
- 논리 몬스터 클래스 actors/mobs/*와 몬스터 Sprite 클래스 sprites/*는 **항상 동일 이름의 일대일 파일이라고 가정하지 않는다**. 실제 spriteClass 등 참조를 확인해야 함.

## 변경 시 주의 (문서화 목적)
소스 코드·리소스는 이번 작업에서 수정하지 않았다. 향후 리소스 교체를 계획한다면 파일 경로 상수와 실제 경로, 레이어/타일 크기, 다국어 키 및 플랫폼 패키징을 함께 검증할 필요가 있다.

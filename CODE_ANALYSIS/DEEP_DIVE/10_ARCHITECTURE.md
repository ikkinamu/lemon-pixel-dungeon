# 전체 아키텍처 상세 분석

## 증거 수준
- **확인:** 파일의 실제 선언·구현 또는 Gradle 설정에서 확인한 내용.
- **해석:** 확인된 구현을 종합하여 설명한 설계적 의미.
- **미검증:** 다른 하위 클래스 또는 런타임 조건에 따라 달라질 수 있는 내용.
- 소스 분석 기준 커밋: bd3a990254e4249458816f4879e93ab87275555b. 프로그램 실행 테스트는 수행하지 않음.

## 계층
1. **플랫폼 진입:** AndroidLauncher / IOSLauncher / DesktopLauncher가 플랫폼별 앱을 시작.
2. **공통 게임 프레임워크:** SPD-classes의 com.watabou.noosa.Game, Scene, 그래픽·입력·파일·경로 탐색 유틸리티.
3. **공통 게임 상태:** core의 Dungeon, GamesInProgress, Statistics, Rankings, SPDSettings, SPDAction.
4. **세계 시뮬레이션:** Actor → Char → Hero 또는 Mob, Buff, Level, Room, Trap, Blob.
5. **아이템 및 전투:** Item → Weapon/Armor/Wand/Potion/Scroll 등, Generator.
6. **표시와 조작:** PixelScene/GameScene, UI·Window·Sprite·Tilemap.
7. **외부 서비스:** services/news 및 services/updates 모듈.

## 의존성의 방향
- [settings.gradle](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/settings.gradle): 선언된 모듈 SPD-classes, core, android, ios, desktop, services 및 뉴스/업데이트 하위 모듈.
- [core/build.gradle](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/build.gradle): core는 SPD-classes를 api, services를 implementation으로 참조.
- [android/build.gradle](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/build.gradle): Android는 core, libGDX Android 백엔드, 네이티브 라이브러리를 이용. debug/release에서 다른 서비스 구현을 선택함.
- [desktop/build.gradle](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/build.gradle): 데스크톱 진입 클래스를 DesktopLauncher로 지정하고 core의 assets를 processResources에 복사.
- [SPD-classes/build.gradle](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/build.gradle): libGDX, controllers, FreeType 및 JSON 의존성 선언.

## 프레임워크 vs 게임
**Game**은 ApplicationListener를 구현하고 create/render/resize/pause/resume/dispose의 애플리케이션 생명주기를 담당([SPD-classes/src/main/java/com/watabou/noosa/Game.java:45-79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L45-L79)).
**ShatteredPixelDungeon**은 Game을 상속하며 바인딩, 오디오, 종료 처리, 장면 전환을 게임에 맞게 연결([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java:37-120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java#L37-L120)).
**Dungeon**은 현재 플레이의 핵심 상태를 static 멤버로 보관함([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java:180-214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L180-L214)). 클래스 이름만으로 '던전 맵 하나'라고 오해하지 말 것.
**Level**은 지형 배열, 개체 집합 및 층 자체를 표현함([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java:145-198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java#L145-L198)).

## 주요 실행 화살표 (확인된 호출 경로와 설계적 연결)
~~~
DesktopLauncher.main
  -> 플랫폼 설정 및 libGDX 데스크톱 애플리케이션 생성
  -> Game.create() / ShatteredPixelDungeon.create()
  -> Scene 표시
  -> 게임 시작/층 전환 시 InterlevelScene
  -> Dungeon.init(), Dungeon.newLevel() 또는 Dungeon.loadLevel()
  -> Dungeon.switchLevel()
  -> GameScene.create() / update()
  -> Actor.process() (액터 처리 전용 스레드)
~~~
이 다이어그램은 여러 파일의 실행 경로를 합성한 **개략도**이며, 모든 경우에 똑같은 함수 순서를 보장한다는 의미는 아님. 구체적인 경로는 각 상세 문서를 참고.

## 우선 읽을 파일
1. [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
2. [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java)
3. [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
4. [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
5. [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
6. [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
7. [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
8. [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
9. [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
10. [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

## 중요한 설계상 특성
- Java 기반의 플랫폼 분리 구조; 주요 게임 로직은 core에 집중.
- 게임의 '턴'은 단순한 플레이어·적 교대 배열이 아니라 Actor.time 및 actPriority로 스케줄링됨.
- Dungeon의 static 데이터는 전역 게임 상태이므로 호출 순서/초기화 여부가 중요함.
- 맵 생성에는 던전 seed와 층별 seed가 쓰이며, 한정 드롭과 상태 복원도 함께 맞춰야 함.
- 렌더 스레드, 액터 스레드, 층 전환 로딩 스레드가 별도로 등장. 스레드 안전성은 코드 단위로 판단해야 함.

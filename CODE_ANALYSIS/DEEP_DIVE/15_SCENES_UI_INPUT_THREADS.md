# 장면·UI·입력·스레드의 경계

## 1. 장면 계층
- [SPD-classes/src/main/java/com/watabou/noosa/Game.java:45-85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L45-L85): 공통 Game은 ApplicationListener. scene/requestedScene/sceneClass를 다룸.
- [SPD-classes/src/main/java/com/watabou/noosa/Scene.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java): Scene은 Group을 상속하고 create/update/destroy/pause/resume, 입력 이벤트 처리.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java:64-96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java#L64-L96): 게임용 공통 장면. UI 카메라, 픽셀 확대, 창 상태 보존 및 화면 전환 효과.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java): 타이틀, 뉴스/변경 내역/설정 등의 진입 UI.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java): 영웅 클래스와 새 게임 설정, 도전, 시드/옵션 화면.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java:70-121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java#L70-L121): 층 이동, 이어하기, 부활, 초기화 등 상태 전환 작업.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java:161-225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java#L161-L225): 실제 지형/캐릭터/아이템/효과와 입력 UI를 배치하는 플레이 장면.

## 2. 게임 장면의 실제 구성
GameScene.create()는 유효한 Dungeon.hero/level 여부를 확인하고, 음악과 카메라, 지형·물·벽·조명/안개 등 시각 객체를 초기화한다([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java:225-270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java#L225-L270)).
- terrain / water / tiles / walls / fog: 화면에 그려지는 시각적 객체.
- Dungeon.level.map / passable / heroFOV: 게임 상태·충돌·시야 판정 데이터.
- UI 컴포넌트: Toolbar, InventoryPane, StatusPane, GameLog, TargetHealthIndicator 등.
**중요:** 화면에 보이는 Sprite와 논리 객체(Char/Item/Level)는 별도 계층이다. 시각 객체 하나를 바꿨다고 실제 게임 규칙이 자동으로 바뀌는 것은 아니다.

## 3. 입력과 액션
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java): 키 바인딩의 GameAction 정의 (8방향 이동, 가방, 퀵슬롯, 대기 등).
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java:46-152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L46-L152): 맵 클릭/드래그/줌/키보드 조작/대상 선택.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java:518-526](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L518-L526): onSelect(Integer cell), prompt() 등의 콜백을 가진 Listener.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java): 대기/수색/소지품/퀵슬롯 등의 버튼·키 액션 연결.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java): 큰 화면의 소지품 UI 표시/아이템 선택.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java): 가방 창과 아이템 선택 필터.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java): 게임 시뮬레이션으로 넘어가는 Move/Attack 등 **행동 객체**.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java:829-948](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L829-L948): Hero.act()가 실제 현재 행동 객체를 처리.

**해설:** SPDAction은 '사용자가 누를 수 있는 명령/바인딩', HeroAction은 '영웅이 수행하려는 게임 내 행동'으로 계층이 다르다. 두 이름이 유사하지만 일대일 대응은 아니다.

## 4. 스레드
### 렌더링과 액터
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java:817-928](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java#L817-L928):
- GameScene.update()는 필요 시 SHPD Actor Thread를 새로 생성하고 Actor.process()를 실행한다.
- 현재 액터 처리가 끝난 구간에는 notify()로 스레드를 깨워 처리를 재개한다.
- notifyDelay 기본값은 1/60f로, 소스 주석상 렌더 갱신 주기가 빠를 때 휴식 속도를 제한하려는 목적.
- GameScene.onPause()는 게임 저장을 호출하며 특정 상황에 액터 처리 완료를 기다릴 수 있다.
- endActorThread()는 종료 플래그 변경 및 interrupt를 사용한다.

### 층 이동 로딩
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java:410-463](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java#L410-L463):
- 새 Thread에서 Actor.fixTime() 후 Mode에 따라 descend/ascend/restore/resurrect/returnTo/fall/reset 등을 선택한다.
- 작업 완료 후 phase 상태를 조절하고, 화면의 전환 애니메이션 종료 시 GameScene으로 넘어간다.

### 해석 주의
- 스레드가 분리되어 있다는 사실은 모든 공유 상태 접근이 안전하다는 보증이 아니다.
- synchronized, volatile, wait/notify, runOnRenderThread의 실제 범위를 각각 보아야 한다.
- **분석만으로 '레이스 컨디션이 반드시 존재한다'고 확정하지 않는다.** 재현 가능한 테스트가 필요하다.
- Actor.process()의 boolean 반환과 장면 전환 중단 조건은 일반적인 UI 이벤트 루프와 다르다.

## 5. 장면 전환
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java:77-124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java#L77-L124):
- switchNoFade: 화면 전환에 페이드를 적용하지 않도록 지정.
- seamlessResetScene: 현재 창 상태를 저장하고 장면을 재설정.
- PixelScene.saveWindows()/restoreWindows()가 상태를 관리.
'seamless'는 장면 재생성 동안 창 상태 등을 보존한다는 목적이지, 모든 게임 객체가 재생성되지 않는다는 보장이 아니다.

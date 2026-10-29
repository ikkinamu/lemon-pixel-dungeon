# Java 소스 구현 분석 940–957

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 940. [`ShockingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ShockingTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 60행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ShockingTrap.java#L35) `public class ShockingTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ShockingTrap.java#L43) `public void activate() {` — 행동·상태 갱신, 인접 호출: INSTANCE.play, GameScene.add, Blob.seed, Actor.findChar, Buff.prolong

## 941. [`StormTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/StormTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 62행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/StormTrap.java#L36) `public class StormTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/StormTrap.java#L44) `public void activate() {` — 행동·상태 갱신, 인접 호출: INSTANCE.play, PathFinder.buildDistanceMap, BArray.not, GameScene.add, Blob.seed, Actor.findChar, Buff.prolong

## 942. [`SummoningTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/SummoningTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 108행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/SummoningTrap.java#L36) `public class SummoningTrap extends Trap {`

### 변수·상수 후보
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/SummoningTrap.java#L38) `private static final float DELAY = 2f;`

### 메서드 및 코드 의존 단서
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/SummoningTrap.java#L46) `public void activate() {` — 행동·상태 갱신, 인접 호출: Random.Int, Actor.findChar, Random.index, Char.hasProp, GameScene.add

## 943. [`TeleportationTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/TeleportationTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 78행.

### 클래스/타입
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/TeleportationTrap.java#L39) `public class TeleportationTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/TeleportationTrap.java#L47) `public void activate() {` — 행동·상태 갱신, 인접 호출: Actor.findChar, ScrollOfTeleportation.teleportChar, Buff.prolong, INSTANCE.play, CellEmitter.get, Speck.factory

## 944. [`TenguDartTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/TenguDartTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 50행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/TenguDartTrap.java#L29) `public class TenguDartTrap extends PoisonDartTrap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/TenguDartTrap.java#L37) `protected int poisonAmount() {` — 개별 처리, 인접 호출: Dungeon.isChallenged
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/TenguDartTrap.java#L46) `protected boolean canTarget(Char ch) {` — 조회·판정

## 945. [`ToxicTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ToxicTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 55행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ToxicTrap.java#L34) `public class ToxicTrap extends Trap{`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ToxicTrap.java#L42) `public void activate() {` — 행동·상태 갱신, 인접 호출: GameScene.add, Blob.seed, INSTANCE.play, Actor.findChar, Buff.prolong

## 946. [`Trap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 159행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L35) `public abstract class Trap implements Bundlable {`
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L155) `public static class HazardAssistTracker extends FlavourBuff{`

### 변수·상수 후보
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L38) `public static final int RED     = 0;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L39) `public static final int ORANGE  = 1;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L40) `public static final int YELLOW  = 2;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L41) `public static final int GREEN   = 3;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L42) `public static final int TEAL    = 4;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L43) `public static final int VIOLET  = 5;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L44) `public static final int WHITE   = 6;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L45) `public static final int GREY    = 7;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L46) `public static final int BLACK   = 8;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L49) `public static final int DOTS        = 0;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L50) `public static final int WAVES       = 1;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L51) `public static final int GRILL       = 2;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L52) `public static final int STARS       = 3;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L53) `public static final int DIAMOND     = 4;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L54) `public static final int CROSSHAIR   = 5;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L55) `public static final int LARGE_DOT   = 6;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L57) `public int color;`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L58) `public int shape;`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L60) `public int pos;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L63) `public boolean visible;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L64) `public boolean active = true;`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L65) `public boolean disarmedByActivation = true;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L67) `public boolean canBeHidden = true;`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L68) `public boolean canBeSearched = true;`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L71) `public boolean avoidsClosedSpaces = false;`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L134) `private static final String POS	= "pos";`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L135) `private static final String VISIBLE	= "visible";`
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L136) `private static final String ACTIVE = "active";`
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L156) `public static final float DURATION = 50f;`

### 메서드 및 코드 의존 단서
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L73) `public Trap set(int pos){` — 개별 처리, 인접 호출: GameScene.updateMap, INSTANCE.play, Bestiary.setSeen, Bestiary.countEncounter
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L78) `public Trap reveal() {` — 개별 처리, 인접 호출: GameScene.updateMap, INSTANCE.play, Bestiary.setSeen, Bestiary.countEncounter, Dungeon.scalingDepth, Messages.get
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L84) `public Trap hide() {` — 개별 처리, 인접 호출: GameScene.updateMap, INSTANCE.play, Bestiary.setSeen, Bestiary.countEncounter, Dungeon.scalingDepth, Messages.get
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L94) `public void trigger() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, Bestiary.setSeen, Bestiary.countEncounter, Dungeon.scalingDepth, Messages.get
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L107) `public abstract void activate();` — 행동·상태 갱신, 인접 호출: Dungeon.scalingDepth, Messages.get
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L109) `public void disarm(){` — 개별 처리, 인접 호출: Dungeon.scalingDepth, Messages.get
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L117) `protected int scalingDepth(){` — 개별 처리, 인접 호출: Dungeon.scalingDepth, Messages.get
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L121) `public String name(){` — 개별 처리, 인접 호출: Messages.get
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L125) `public String desc() {` — 개별 처리, 인접 호출: Messages.get
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L139) `public void restoreFromBundle( Bundle bundle ) {` — 저장·복원
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java#L148) `public void storeInBundle( Bundle bundle ) {` — 저장·복원

## 947. [`WarpingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WarpingTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 49행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WarpingTrap.java#L28) `public class WarpingTrap extends TeleportationTrap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WarpingTrap.java#L36) `public void activate() {` — 행동·상태 갱신, 인접 호출: BArray.setFalse, GameScene.updateFog, Dungeon.observe

## 948. [`WeakeningTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WeakeningTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 59행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WeakeningTrap.java#L33) `public class WeakeningTrap extends Trap{`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WeakeningTrap.java#L41) `public void activate() {` — 행동·상태 갱신, 인접 호출: CellEmitter.get, Actor.findChar, Buff.prolong

## 949. [`WornDartTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WornDartTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 126행.

### 클래스/타입
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WornDartTrap.java#L42) `public class WornDartTrap extends Trap {`

### 변수·상수 후보
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WornDartTrap.java#L94) `final Char finalTarget = target;`

### 메서드 및 코드 의존 단서
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WornDartTrap.java#L53) `public void activate() {` — 행동·상태 갱신, 인접 호출: Actor.add, Actor.remove, Actor.findChar, Math.max, Actor.chars, Buff.prolong, ShatteredPixelDungeon.scene
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WornDartTrap.java#L63) `protected boolean act() {` — 행동·상태 갱신, 인접 호출: Actor.remove, Actor.findChar, Math.max, Actor.chars, Buff.prolong, ShatteredPixelDungeon.scene, Random.NormalIntRange
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WornDartTrap.java#L99) `public void call() {` — 개별 처리, 인접 호출: Random.NormalIntRange, Dungeon.fail, GLog.n, Messages.get, Badges.validateDeathFromFriendlyMagic, INSTANCE.play, Random.Float

## 950. [`VaultLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels`, 706행.

### 클래스/타입
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L123) `public class VaultLevel extends CityLevel {`
- [L674](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L674) `public static class VaultFlameTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L126) `public void playLevelMusic() {` — 개별 처리, 인접 호출: INSTANCE.play, Generator.randomUsingDefaults, VaultRoom.setupChances, VaultRoom.createRoom, VaultTreasureRoom.generateRoomList, VaultTreasureRoom.nextRoom
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L131) `protected boolean build() {` — 생성·초기화, 인접 호출: Generator.randomUsingDefaults, VaultRoom.setupChances, VaultRoom.createRoom, VaultTreasureRoom.generateRoomList, VaultTreasureRoom.nextRoom
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L149) `protected ArrayList<Room> initRooms() {` — 생성·초기화, 인접 호출: VaultRoom.setupChances, VaultRoom.createRoom, VaultTreasureRoom.generateRoomList, VaultTreasureRoom.nextRoom, Math.min
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L174) `public float levelExplorePercent(int depth) {` — 개별 처리, 인접 호출: Math.min
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L185) `protected Builder builder() {` — 생성·초기화
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L190) `protected Painter painter() {` — 개별 처리
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L192) `public float hiddenDoorChance( Level l ){` — 개별 처리
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L201) `protected int nTraps() {` — 개별 처리
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L206) `public boolean activateTransition(Hero hero, LevelTransition transition) {` — 행동·상태 갱신
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L220) `public void setupEquipment(){` — 생성·초기화, 인접 호출: Generator.randomUsingDefaults
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L241) `public void setupEquipmentAtTier(int lootTier){` — 생성·초기화, 인접 호출: Generator.randomUsingDefaults, Random.Int
- [L381](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L381) `public Item createEquipment(int lootTier) {` — 생성·초기화, 인접 호출: Mob.destroy
- [L431](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L431) `private void setupConsumables(){` — 생성·초기화, 인접 호출: Arrays.asList, Reflection.newInstance, Random.oneOf, Collections.shuffle
- [L485](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L485) `public Item createConsumabe(int tier){` — 생성·초기화, 인접 호출: Random.shuffle
- [L498](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L498) `public Item findT3SolveItem(){` — 조회·판정, 인접 호출: Random.shuffle
- [L515](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L515) `public Item findT2SolveItem(){` — 조회·판정, 인접 호출: Random.shuffle, Collections.addAll, Random.oneOf
- [L548](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L548) `public Mob createMob() {` — 생성·초기화, 인접 호출: Collections.addAll, Random.oneOf, Random.shuffle, VaultElemental.random, Reflection.newInstance, Quest.isCompleted, Quest.isOld
- [L566](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L566) `public void returnMob( Class<?extends Mob> cls){` — 개별 처리, 인접 호출: Quest.isCompleted, Quest.isOld, Game.switchScene
- [L571](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L571) `protected void createMobs() {` — 생성·초기화, 인접 호출: Quest.isCompleted, Quest.isOld, Game.switchScene, Dungeon.isChallenged, Random.pushGenerator, Random.Long
- [L576](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L576) `public void occupyCell(Char ch) {` — 개별 처리, 인접 호출: Quest.isCompleted, Quest.isOld, Game.switchScene, Dungeon.isChallenged, Random.pushGenerator, Random.Long
- [L597](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L597) `public Actor addRespawner() {` — 개별 처리, 인접 호출: Dungeon.isChallenged, Random.pushGenerator, Random.Long, Random.popGenerator
- [L602](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L602) `protected void createItems() {` — 생성·초기화, 인접 호출: Dungeon.isChallenged, Random.pushGenerator, Random.Long, Random.popGenerator
- [L645](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L645) `public void seal() {` — 개별 처리, 인접 호출: Game.runOnRenderThread, INSTANCE.fadeOut, INSTANCE.end
- [L654](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L654) `public void unseal() {` — 개별 처리, 인접 호출: Game.runOnRenderThread, INSTANCE.fadeOut, INSTANCE.end, Messages.get, Blob.seed
- [L663](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L663) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.fadeOut, INSTANCE.end, Messages.get, Blob.seed, VaultLevel.VaultFlameTrap, Painter.set
- [L666](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L666) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.end, Messages.get, Blob.seed, VaultLevel.VaultFlameTrap, Painter.set
- [L685](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L685) `public void activate() {` — 행동·상태 갱신, 인접 호출: Messages.get, Blob.seed, VaultLevel.VaultFlameTrap, Painter.set
- [L690](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L690) `public String desc() {` — 개별 처리, 인접 호출: Messages.get, Blob.seed, VaultLevel.VaultFlameTrap, Painter.set
- [L694](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java#L694) `public static void setupTrap(Level level, int cell, int initialCD, int afterTriggerCD, int triggers){` — 생성·초기화, 인접 호출: Blob.seed, VaultLevel.VaultFlameTrap, Painter.set

## 951. [`Ballistica.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.mechanics`, 173행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L31) `public class Ballistica {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L36) `public Integer sourcePos = null;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L37) `public Integer collisionPos = null;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L38) `public Integer collisionProperties = null;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L39) `public Integer dist = 0;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L47) `public static final int PROJECTILE =  	STOP_TARGET	| STOP_CHARS	| STOP_SOLID;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L49) `public static final int MAGIC_BOLT =    STOP_CHARS  | STOP_SOLID;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L51) `public static final int WONT_STOP =     0;`

### 메서드 및 코드 의존 단서
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L54) `public Ballistica( int from, int to, int params ){` — 개별 처리, 인접 호출: Math.abs
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L74) `private void build( int from, int to, boolean stopTarget, boolean stopChars, boolean stopTerrain, boolean ignoreSoftSolid ) {` — 생성·초기화, 인접 호출: Math.abs
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L155) `private void collide(int cell){` — 개별 처리, 인접 호출: Math.min, ShatteredPixelDungeon.reportException
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L163) `public List<Integer> subPath(int start, int end){` — 개별 처리, 인접 호출: Math.min, ShatteredPixelDungeon.reportException

## 952. [`ConeAOE.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.mechanics`, 117행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java#L34) `public class ConeAOE {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java#L36) `public Ballistica coreRay;`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java#L42) `public ConeAOE( Ballistica core, float degrees ){` — 개별 처리, 인접 호출: PointF.distance, PointF.inter, PointF.angle, GameMath.gate, Math.floor
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java#L46) `public ConeAOE( Ballistica core, float maxDist, float degrees, int ballisticaParams ){` — 개별 처리, 인접 호출: PointF.distance, PointF.inter, PointF.angle, GameMath.gate, Math.floor

## 953. [`ShadowCaster.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ShadowCaster.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.mechanics`, 166행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ShadowCaster.java#L28) `public final class ShadowCaster {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ShadowCaster.java#L30) `public static final int MAX_DISTANCE = 20;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ShadowCaster.java#L34) `public static int[][] rounding;`

### 메서드 및 코드 의존 단서
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ShadowCaster.java#L48) `public static void castShadow( int x, int y, int w, boolean[] fieldOfView, boolean[] blocking, int distance ) {` — 개별 처리, 인접 호출: BArray.setFalse, ShatteredPixelDungeon.reportException

## 954. [`Languages.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.messages`, 115행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L26) `public enum Languages {`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L55) `public enum Status{`

### 변수·상수 후보
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L62) `private String name;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L63) `private String code;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L64) `private Status status;`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L65) `private String[] reviewers;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L66) `private String[] translators;`

### 메서드 및 코드 의존 단서
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L76) `public String nativeName(){` — 개별 처리, 인접 호출: Languages.values
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L80) `public String code(){` — 개별 처리, 인접 호출: Languages.values
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L84) `public Status status(){` — 개별 처리, 인접 호출: Languages.values
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L88) `public String[] reviewers() {` — 개별 처리, 인접 호출: Languages.values
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L93) `public String[] translators() {` — 개별 처리, 인접 호출: Languages.values
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L98) `public static Languages matchLocale(Locale locale){` — 개별 처리, 인접 호출: Languages.values
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java#L106) `public static Languages matchCode(String code){` — 개별 처리, 인접 호출: Languages.values

## 955. [`Messages.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.messages`, 223행.

### 클래스/타입
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L40) `Simple wrapper class for libGDX I18NBundles.`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L42) `The core idea here is that each string resource's key is a combination of the class definition and a local value.`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L43) `An object or static method would usually call this with an object/class reference (usually its own) and a local key.`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L46) `public class Messages {`

### 변수·상수 후보
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L48) `private static ArrayList<I18NBundle> bundles;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L49) `private static Languages lang;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L50) `private static Locale locale;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L52) `public static final String NO_TEXT_FOUND = "!!!NO TEXT FOUND!!!";`
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L176) `private static HashMap<String, DecimalFormat> formatters;`

### 메서드 및 코드 의존 단서
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L54) `public static Languages lang(){` — 개별 처리, 인접 호출: SPDSettings.language, I18NBundle.setExceptionOnMissingKey
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L58) `public static Locale locale(){` — 개별 처리, 인접 호출: SPDSettings.language, I18NBundle.setExceptionOnMissingKey
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L83) `public static void setup( Languages lang ){` — 생성·초기화, 인접 호출: I18NBundle.setExceptionOnMissingKey, I18NBundle.createBundle
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L117) `public static String get(String key, Object...args){` — 조회·판정
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L121) `public static String get(Object o, String k, Object...args){` — 조회·판정
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L125) `public static String get(Class c, String k, Object...args){` — 조회·판정, 인접 호출: String.format
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L149) `private static String getFromBundle(String key){` — 조회·판정, 인접 호출: String.format, ShatteredPixelDungeon.reportException, DecimalFormatSymbols.getInstance, Arrays.asList
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L167) `public static String format( String format, Object...args ) {` — 개별 처리, 인접 호출: String.format, ShatteredPixelDungeon.reportException, DecimalFormatSymbols.getInstance, Arrays.asList
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L178) `public static String decimalFormat( String format, double number ){` — 개별 처리, 인접 호출: DecimalFormatSymbols.getInstance, Arrays.asList
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L185) `public static String capitalize( String str ){` — 개별 처리, 인접 호출: Arrays.asList
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L196) `public static String titleCase( String str ){` — 개별 처리
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L216) `public static String upperCase( String str ){` — 개별 처리
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java#L220) `public static String lowerCase( String str ){` — 개별 처리

## 956. [`BlandfruitBush.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/BlandfruitBush.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 47행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/BlandfruitBush.java#L28) `public class BlandfruitBush extends Plant {`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/BlandfruitBush.java#L40) `public static class Seed extends Plant.Seed {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/BlandfruitBush.java#L35) `public void activate( Char ch ) {` — 행동·상태 갱신

## 957. [`Blindweed.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Blindweed.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 75행.

### 클래스/타입
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Blindweed.java#L38) `public class Blindweed extends Plant {`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Blindweed.java#L67) `public static class Seed extends Plant.Seed {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Blindweed.java#L46) `public void activate( Char ch ) {` — 행동·상태 갱신, 인접 호출: Buff.affect, Buff.prolong, CellEmitter.get, Speck.factory


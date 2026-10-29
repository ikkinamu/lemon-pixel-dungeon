# Java 소스 구현 분석 958–975

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 958. [`Earthroot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 159행.

### 클래스/타입
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L38) `public class Earthroot extends Plant {`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L62) `public static class Seed extends Plant.Seed {`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L72) `public static class Armor extends Buff {`

### 변수·상수 후보
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L74) `private static final float STEP = 1f;`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L76) `private int pos;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L77) `private int level;`
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L141) `private static final String POS		= "pos";`
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L142) `private static final String LEVEL	= "level";`

### 메서드 및 코드 의존 단서
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L46) `public void activate( Char ch ) {` — 행동·상태 갱신, 인접 호출: Barkskin.conditionallyAppend, Buff.affect, CellEmitter.bottom, PixelScene.shake
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L85) `public boolean act() {` — 행동·상태 갱신, 인접 호출: Dungeon.scalingDepth, Math.min, Math.max
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L93) `private static int blocking(){` — 개별 처리, 인접 호출: Dungeon.scalingDepth, Math.min, Math.max, Integer.toString
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L97) `public int absorb( int damage ) {` — 개별 처리, 인접 호출: Math.min, Math.max, Integer.toString, Messages.get
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L112) `public void level( int value ) {` — 개별 처리, 인접 호출: Math.max, Integer.toString, Messages.get
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L122) `public int icon() {` — 개별 처리, 인접 호출: Math.max, Integer.toString, Messages.get
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L127) `public float iconFadePercent() {` — 개별 처리, 인접 호출: Math.max, Integer.toString, Messages.get
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L132) `public String iconTextDisplay() {` — 개별 처리, 인접 호출: Integer.toString, Messages.get
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L137) `public String desc() {` — 개별 처리, 인접 호출: Messages.get
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L145) `public void storeInBundle( Bundle bundle ) {` — 저장·복원
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java#L152) `public void restoreFromBundle( Bundle bundle ) {` — 저장·복원

## 959. [`Fadeleaf.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Fadeleaf.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 86행.

### 클래스/타입
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Fadeleaf.java#L39) `public class Fadeleaf extends Plant {`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Fadeleaf.java#L78) `public static class Seed extends Plant.Seed {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Fadeleaf.java#L47) `public void activate( final Char ch ) {` — 행동·상태 갱신, 인접 호출: Dungeon.interfloorTeleportAllowed, Level.beforeTransition, Math.max, Game.switchScene, ScrollOfTeleportation.teleportChar, Buff.prolong, CellEmitter.get

## 960. [`Firebloom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Firebloom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 72행.

### 클래스/타입
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Firebloom.java#L39) `public class Firebloom extends Plant {`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Firebloom.java#L64) `public static class Seed extends Plant.Seed {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Firebloom.java#L47) `public void activate( Char ch ) {` — 행동·상태 갱신, 인접 호출: Buff.affect, Buff.prolong, GameScene.add, Blob.seed, CellEmitter.get

## 961. [`Icecap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Icecap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 69행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Icecap.java#L37) `public class Icecap extends Plant {`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Icecap.java#L61) `public static class Seed extends Plant.Seed {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Icecap.java#L45) `public void activate( Char ch ) {` — 행동·상태 갱신, 인접 호출: Buff.affect, Freezing.affect, Actor.findChar, Buff.prolong

## 962. [`Mageroyal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Mageroyal.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 64행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Mageroyal.java#L34) `public class Mageroyal extends Plant {`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Mageroyal.java#L57) `public static class Seed extends Plant.Seed {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Mageroyal.java#L42) `public void activate( Char ch ) {` — 행동·상태 갱신, 인접 호출: PotionOfHealing.cure, GLog.i, Messages.get, Buff.affect

## 963. [`Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 254행.

### 클래스/타입
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L53) `public abstract class Plant implements Bundlable {`
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L133) `public static class Seed extends Item {`
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L236) `public static class PlaceHolder extends Seed {`

### 변수·상수 후보
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L55) `public int image;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L56) `public int pos;`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L58) `protected Class<? extends Plant.Seed> seedClass;`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L109) `private static final String POS	= "pos";`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L135) `public static final String AC_PLANT	= "PLANT";`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L137) `private static final float TIME_TO_PLANT = 1f;`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L144) `protected Class<? extends Plant> plantClass;`

### 메서드 및 코드 의존 단서
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L60) `public void trigger(){` — 이벤트·효과 실행, 인접 호출: Actor.findChar, Barkskin.conditionallyAppend, Bestiary.setSeen, Bestiary.countEncounter, CellEmitter.get, Actor.chars, Math.max
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L82) `public abstract void activate( Char ch );` — 행동·상태 갱신, 인접 호출: CellEmitter.get, Actor.chars, Math.max, Random.Float, Reflection.newInstance, Messages.get
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L84) `public void wither() {` — 개별 처리, 인접 호출: CellEmitter.get, Actor.chars, Math.max, Random.Float, Reflection.newInstance, Messages.get
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L112) `public void restoreFromBundle( Bundle bundle ) {` — 저장·복원, 인접 호출: Messages.get
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L117) `public void storeInBundle( Bundle bundle ) {` — 저장·복원, 인접 호출: Messages.get, Dungeon.isChallenged, Catalog.countUse
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L121) `public String name(){` — 개별 처리, 인접 호출: Messages.get, Dungeon.isChallenged, Catalog.countUse
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L125) `public String desc() {` — 개별 처리, 인접 호출: Messages.get, Dungeon.isChallenged, Catalog.countUse, Level.set, GameScene.updateMap
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L147) `public ArrayList<String> actions( Hero hero ) {` — 행동·상태 갱신, 인접 호출: Dungeon.isChallenged, Catalog.countUse, Level.set, GameScene.updateMap, CellEmitter.get
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L154) `protected void onThrow( int cell ) {` — 이벤트·효과 실행, 인접 호출: Dungeon.isChallenged, Catalog.countUse, Level.set, GameScene.updateMap, CellEmitter.get, INSTANCE.play, Reflection.newInstance
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L178) `public void execute( Hero hero, String action ) {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, Reflection.newInstance
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L193) `public Plant couch( int pos, Level level ) {` — 개별 처리, 인접 호출: INSTANCE.play, Reflection.newInstance, Messages.get
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L203) `public boolean isUpgradable() {` — 조회·판정, 인접 호출: Messages.get
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L208) `public boolean isIdentified() {` — 조회·판정, 인접 호출: Messages.get
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L213) `public int value() {` — 개별 처리, 인접 호출: Messages.get
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L218) `public int energyVal() {` — 개별 처리, 인접 호출: Messages.get
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L223) `public String desc() {` — 개별 처리, 인접 호출: Messages.get
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L232) `public String info() {` — 개별 처리, 인접 호출: Messages.get
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L243) `public boolean isSimilar(Item item) {` — 조회·판정
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L248) `public String info() {` — 개별 처리

## 964. [`Rotberry.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Rotberry.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 85행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Rotberry.java#L37) `public class Rotberry extends Plant {`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Rotberry.java#L65) `public static class Seed extends Plant.Seed {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Rotberry.java#L45) `public void activate( Char ch ) {` — 행동·상태 갱신, 인접 호출: Buff.affect, GameScene.add, Blob.seed, CellEmitter.get
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Rotberry.java#L54) `public void wither() {` — 개별 처리, 인접 호출: CellEmitter.get
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Rotberry.java#L75) `public int value() {` — 개별 처리
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Rotberry.java#L80) `public int energyVal() {` — 개별 처리

## 965. [`Sorrowmoss.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sorrowmoss.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 70행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sorrowmoss.java#L37) `public class Sorrowmoss extends Plant {`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sorrowmoss.java#L62) `public static class Seed extends Plant.Seed {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sorrowmoss.java#L45) `public void activate( Char ch ) {` — 행동·상태 갱신, 인접 호출: Buff.affect, Buff.prolong, Math.round, Dungeon.scalingDepth, CellEmitter.center

## 966. [`Starflower.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Starflower.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 77행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Starflower.java#L35) `public class Starflower extends Plant {`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Starflower.java#L58) `public static class Seed extends Plant.Seed{`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Starflower.java#L43) `public void activate( Char ch ) {` — 행동·상태 갱신, 인접 호출: Buff.prolong, SpellSprite.show
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Starflower.java#L67) `public int value() {` — 개별 처리
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Starflower.java#L72) `public int energyVal() {` — 개별 처리

## 967. [`Stormvine.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Stormvine.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 64행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Stormvine.java#L34) `public class Stormvine extends Plant {`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Stormvine.java#L56) `public static class Seed extends Plant.Seed {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Stormvine.java#L42) `public void activate( Char ch ) {` — 행동·상태 갱신, 인접 호출: Buff.affect, Buff.prolong

## 968. [`Sungrass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 172행.

### 클래스/타입
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L39) `public class Sungrass extends Plant {`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L62) `public static class Seed extends Plant.Seed {`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L72) `public static class Health extends Buff {`

### 변수·상수 후보
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L74) `private static final float STEP = 1f;`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L76) `private int pos;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L77) `private float partialHeal;`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L78) `private int level;`
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L150) `private static final String POS	= "pos";`
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L151) `private static final String PARTIAL = "partial_heal";`
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L152) `private static final String LEVEL = "level";`

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L47) `public void activate( Char ch ) {` — 행동·상태 갱신, 인접 호출: Buff.affect, CellEmitter.get
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L86) `public boolean act() {` — 행동·상태 갱신, 인접 호출: Integer.toString
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L123) `public void boost( int amount ){` — 개별 처리, 인접 호출: Math.max, Integer.toString, Messages.get
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L131) `public int icon() {` — 개별 처리, 인접 호출: Math.max, Integer.toString, Messages.get
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L136) `public float iconFadePercent() {` — 개별 처리, 인접 호출: Math.max, Integer.toString, Messages.get
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L141) `public String iconTextDisplay() {` — 개별 처리, 인접 호출: Integer.toString, Messages.get
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L146) `public String desc() {` — 개별 처리, 인접 호출: Messages.get
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L155) `public void storeInBundle( Bundle bundle ) {` — 저장·복원
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L163) `public void restoreFromBundle( Bundle bundle ) {` — 저장·복원

## 969. [`Swiftthistle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.plants`, 220행.

### 클래스/타입
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L43) `public class Swiftthistle extends Plant {`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L60) `public static class Seed extends Plant.Seed {`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L70) `public static class TimeBubble extends Buff {`

### 변수·상수 후보
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L77) `private float left;`
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L192) `private static final String PRESSES = "presses";`
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L193) `private static final String LEFT = "left";`

### 메서드 및 코드 의존 단서
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L51) `public void activate( Char ch ) {` — 행동·상태 갱신, 인접 호출: Buff.affect, Math.max
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L81) `public int icon() {` — 개별 처리, 인접 호출: Math.max, Integer.toString, Messages.get
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L86) `public void tintIcon(Image icon) {` — 개별 처리, 인접 호출: Math.max, Integer.toString, Messages.get
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L91) `public float iconFadePercent() {` — 개별 처리, 인접 호출: Math.max, Integer.toString, Messages.get, Actor.add
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L96) `public String iconTextDisplay() {` — 개별 처리, 인접 호출: Integer.toString, Messages.get, Math.max, Actor.add
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L100) `public void reset(){` — 개별 처리, 인접 호출: Messages.get, Math.max, Actor.add
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L104) `public void reset(int turns){` — 개별 처리, 인접 호출: Messages.get, Math.max, Actor.add
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L109) `public String desc() {` — 개별 처리, 인접 호출: Messages.get, Math.max, Actor.add, Actor.remove
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L113) `public void processTime(float time){` — 행동·상태 갱신, 인접 호출: Actor.add, Actor.remove
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L123) `public void setDelayedPress(int cell){` — 개별 처리, 인접 호출: Actor.add, Actor.remove
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L129) `public void triggerPresses(){` — 이벤트·효과 실행, 인접 호출: Actor.add, Actor.remove
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L138) `protected boolean act() {` — 행동·상태 갱신, 인접 호출: Actor.remove
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L155) `public void disarmPresses(){` — 개별 처리
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L171) `public void detach(){` — 개별 처리
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L178) `public void fx(boolean on) {` — 개별 처리
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L196) `public void storeInBundle(Bundle bundle) {` — 저장·복원
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java#L208) `public void restoreFromBundle(Bundle bundle) {` — 저장·복원

## 970. [`QuickSlot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon`, 160행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L32) `public class QuickSlot {`

### 변수·상수 후보
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L40) `public static int SIZE = 6;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L41) `private Item[] slots = new Item[SIZE];`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L121) `private final String PLACEHOLDERS = "placeholders";`
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L122) `private final String PLACEMENTS = "placements";`

### 메서드 및 코드 의존 단서
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L45) `public void setSlot(int slot, Item item){` — 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L50) `public void clearSlot(int slot){` — 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L54) `public void reset(){` — 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L58) `public Item getItem(int slot){` — 조회·판정
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L63) `public int getSlot(Item item) {` — 조회·판정
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L72) `public Boolean isPlaceholder(int slot){` — 조회·판정
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L76) `public Boolean isNonePlaceholder(int slot){` — 조회·판정, 인접 호출: Random.element
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L80) `public void clearItem(Item item){` — 개별 처리, 인접 호출: Random.element
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L86) `public boolean contains(Item item){` — 개별 처리, 인접 호출: Random.element
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L90) `public void replacePlaceholder(Item item) {` — 개별 처리, 인접 호출: Random.element
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L98) `public void convertToPlaceholder(Item item){` — 개별 처리, 인접 호출: Random.element
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L110) `public Item randomNonePlaceholder(){` — 개별 처리, 인접 호출: Random.element
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L130) `public void storePlaceholders(Bundle bundle){` — 저장·복원
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java#L144) `public void restorePlaceholders(Bundle bundle){` — 저장·복원

## 971. [`Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon`, 613행.

### 클래스/타입
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L62) `public enum Rankings {`
- [L478](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L478) `public static class Record implements Bundlable {`

### 변수·상수 후보
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L66) `public static final int TABLE_SIZE	= 11;`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L68) `public static final String RANKINGS_FILE = "rankings.dat";`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L70) `public ArrayList<Record> records;`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L71) `public int lastRecord;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L72) `public int totalNumber;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L73) `public int wonNumber;`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L76) `public int localTotal;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L77) `public int localWon;`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L79) `public Record latestDaily;`
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L259) `public static final String HERO         = "hero";`
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L260) `public static final String STATS        = "stats";`
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L261) `public static final String BADGES       = "badges";`
- [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L262) `public static final String HANDLERS     = "handlers";`
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L263) `public static final String CHALLENGES   = "challenges";`
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L264) `public static final String GAME_VERSION = "game_version";`
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L265) `public static final String SEED         = "seed";`
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L266) `public static final String CUSTOM_SEED	= "custom_seed";`
- [L267](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L267) `public static final String DAILY	    = "daily";`
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L268) `public static final String DAILY_REPLAY	= "daily_replay";`
- [L390](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L390) `private static final String RECORDS	= "records";`
- [L391](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L391) `private static final String LATEST	= "latest";`
- [L392](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L392) `private static final String TOTAL	= "total";`
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L393) `private static final String WON     = "won";`
- [L395](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L395) `public static final String LATEST_DAILY	        = "latest_daily";`
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L396) `public static final String DAILY_HISTORY_DATES  = "daily_history_dates";`
- [L397](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L397) `public static final String DAILY_HISTORY_SCORES = "daily_history_scores";`
- [L480](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L480) `private static final String CAUSE   = "cause";`
- [L481](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L481) `private static final String WIN		= "win";`
- [L482](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L482) `private static final String SCORE	= "score";`
- [L483](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L483) `private static final String CLASS	= "class";`
- [L484](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L484) `private static final String TIER	= "tier";`
- [L485](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L485) `private static final String LEVEL	= "level";`
- [L486](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L486) `private static final String DEPTH	= "depth";`
- [L487](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L487) `private static final String ASCEND	= "ascending";`
- [L488](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L488) `private static final String DATA	= "gameData";`
- [L489](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L489) `private static final String ID      = "gameID";`
- [L490](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L490) `private static final String SEED    = "custom_seed";`
- [L491](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L491) `private static final String DAILY   = "daily";`
- [L493](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L493) `private static final String DATE    = "date";`
- [L494](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L494) `private static final String VERSION = "version";`
- [L496](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L496) `public Class cause;`
- [L497](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L497) `public boolean win;`
- [L499](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L499) `public HeroClass heroClass;`
- [L500](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L500) `public int armorTier;`
- [L501](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L501) `public int herolevel;`
- [L502](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L502) `public int depth;`
- [L503](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L503) `public boolean ascending;`
- [L505](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L505) `public Bundle gameData;`
- [L506](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L506) `public String gameID;`
- [L509](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L509) `public int score;`
- [L511](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L511) `public String customSeed;`
- [L512](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L512) `public boolean daily;`
- [L514](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L514) `public String date;`
- [L515](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L515) `public String version;`

### 메서드 및 코드 의존 단서
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L83) `public void submit( boolean win, Object cause ) {` — 개별 처리, 인접 호출: Pattern.compile, Badges.validateHighScore
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L182) `private int score( boolean win ) {` — 개별 처리, 인접 호출: Math.min, Math.round
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L187) `public int calculateScore(){` — 개별 처리, 인접 호출: Math.min, Math.round
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L270) `public void saveGameData(Record rec){` — 저장·복원, 인접 호출: Statistics.storeInBundle
- [L343](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L343) `public void loadGameData(Record rec){` — 저장·복원, 인접 호출: Actor.clear, Generator.fullReset, Notes.reset, QuickSlotButton.reset, Scroll.restore, Potion.restore, Ring.restore
- [L399](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L399) `public void save() {` — 저장·복원, 인접 호출: FileUtils.bundleToFile, ShatteredPixelDungeon.reportException, FileUtils.bundleFromFile
- [L427](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L427) `public void load() {` — 저장·복원, 인접 호출: FileUtils.bundleFromFile, SPDSettings.lastDaily
- [L517](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L517) `public String desc(){` — 개별 처리, 인접 호출: Messages.get
- [L537](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L537) `public void restoreFromBundle( Bundle bundle ) {` — 저장·복원, 인접 호출: UUID.randomUUID
- [L571](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L571) `public void storeInBundle( Bundle bundle ) {` — 저장·복원, 인접 호출: Math.signum
- [L596](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L596) `public int compare( Record lhs, Record rhs ) {` — 개별 처리, 인접 호출: Math.signum

## 972. [`AboutScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AboutScene.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.scenes`, 421행.

### 클래스/타입
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AboutScene.java#L41) `public class AboutScene extends PixelScene {`
- [L281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AboutScene.java#L281) `private static class CreditsBlock extends Component {`

### 변수·상수 후보
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AboutScene.java#L136) `final int WATA_COLOR = 0x55AAFF;`
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AboutScene.java#L168) `final int GDX_COLOR = 0xE44D3C;`

### 메서드 및 코드 의존 단서
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AboutScene.java#L44) `public void create() {` — 생성·초기화, 인접 호출: SHPX.get, ALEKS.get
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AboutScene.java#L48) `final float fullWidth = colWidth * (landscape() ? 2 : 1);` — 개별 처리, 인접 호출: SHPX.get, ALEKS.get
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AboutScene.java#L271) `protected void onBackPressed() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.switchScene, PixelScene.renderTextBlock
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AboutScene.java#L275) `private void addLine( float y, Group content ){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AboutScene.java#L294) `private CreditsBlock(boolean large, int highlight, String title, Image avatar, String body, String linkText, String linkUrl){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock
- [L333](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AboutScene.java#L333) `protected void onClick( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: PixelScene.align, Math.max
- [L343](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AboutScene.java#L343) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, Math.max

## 973. [`AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.scenes`, 1214행.

### 클래스/타입
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L87) `public class AlchemyScene extends PixelScene {`
- [L973](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L973) `private class InputButton extends Component {`
- [L1078](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1078) `private class CombineButton extends Component {`
- [L1163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1163) `private class OutputSlot extends Component {`

### 변수·상수 후보
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L90) `private static final InputButton[] inputs = new InputButton[3];`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L91) `private static final CombineButton[] combines = new CombineButton[3];`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L92) `private static final OutputSlot[] outputs = new OutputSlot[3];`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L94) `private IconButton cancel;`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L95) `private IconButton repeat;`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L97) `private static Recipe lastRecipe = null;`
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L99) `private Emitter smokeEmitter;`
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L100) `private Emitter bubbleEmitter;`
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L101) `private Emitter sparkEmitter;`
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L103) `private Emitter lowerBubbles;`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L104) `private SkinnedBlock water;`
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L106) `private Image energyIcon;`
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L107) `private RenderedTextBlock energyLeft;`
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L108) `private IconButton energyAdd;`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L109) `private boolean energyAddBlinking = false;`
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L111) `private static boolean splitAlchGuide = false;`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L112) `private WndJournal.AlchemyTab alchGuide = null;`
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L113) `private static int centerW;`
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L115) `private static final int BTN_SIZE	= 28;`
- [L450](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L450) `private float time = 0;`
- [L820](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L820) `private boolean saveNeeded = false;`
- [L975](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L975) `protected NinePatch bg;`
- [L976](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L976) `protected ItemSlot slot;`
- [L978](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L978) `private Item item = null;`
- [L1080](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1080) `protected int slot;`
- [L1082](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1082) `protected RedButton button;`
- [L1083](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1083) `protected RenderedTextBlock costText;`
- [L1165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1165) `protected NinePatch bg;`
- [L1166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1166) `protected ItemSlot slot;`
- [L1203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1203) `private static AlchemistsToolkit toolkit;`

### 메서드 및 코드 의존 단서
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L122) `public void create() {` — 생성·초기화, 인접 호출: NoosaScriptNoLighting.get, Blending.disable, Blending.enable, TextureCache.createGradient, Game.switchScene
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L134) `protected NoosaScript script() {` — 개별 처리, 인접 호출: NoosaScriptNoLighting.get, Blending.disable, Blending.enable, TextureCache.createGradient, Game.switchScene, ALCHEMY.get, Messages.get
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L139) `public void draw() {` — 개별 처리, 인접 호출: Blending.disable, Blending.enable, TextureCache.createGradient, Game.switchScene, ALCHEMY.get, Messages.get, Math.min
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L161) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Game.switchScene, ALCHEMY.get, Messages.get, Math.min, Chrome.get, Math.max, WndJournal.AlchemyTab
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L230) `synchronized (inputs) {` — 개별 처리, 인접 호출: Messages.titleCase, KeyBindings.getKeyName, KeyBindings.getFirstKeyForAction, Messages.get, LEFT_CLICK.name, Game.scene
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L250) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase, KeyBindings.getKeyName, KeyBindings.getFirstKeyForAction, Messages.get, LEFT_CLICK.name, Game.scene, Recipe.usableInRecipe
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L271) `public void onSelect(int idx, boolean alt) {` — 이벤트·효과 실행, 인접 호출: Recipe.usableInRecipe, ShatteredPixelDungeon.scene, Messages.get, Messages.titleCase, KeyBindings.getKeyName, KeyBindings.getFirstKeyForAction, LEFT_CLICK.name
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L304) `public void onSelect(int idx, boolean alt) {` — 이벤트·효과 실행, 인접 호출: CLOSE.get
- [L307](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L307) `synchronized (inputs) {` — 개별 처리, 인접 호출: CLOSE.get
- [L331](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L331) `public GameAction keyAction() {` — 개별 처리, 인접 호출: CLOSE.get, Messages.get, REPEAT.get
- [L339](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L339) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.get, REPEAT.get
- [L346](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L346) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.get, REPEAT.get
- [L351](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L351) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, REPEAT.get
- [L361](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L361) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.get
- [L369](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L369) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.get
- [L374](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L374) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get
- [L453](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L453) `public void update() {` — 행동·상태 갱신, 인접 호출: Math.abs, Math.cos, WndEnergizeItem.openItemSelector, Messages.get, ShatteredPixelDungeon.seamlessResetScene
- [L466](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L466) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: WndEnergizeItem.openItemSelector, Messages.get, ShatteredPixelDungeon.seamlessResetScene, WndJournal.AlchemyTab
- [L471](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L471) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.get, ShatteredPixelDungeon.seamlessResetScene, WndJournal.AlchemyTab
- [L476](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L476) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, ShatteredPixelDungeon.seamlessResetScene, WndJournal.AlchemyTab
- [L491](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L491) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.seamlessResetScene, WndJournal.AlchemyTab, Messages.titleCase, ALCHEMY_GUIDE.title
- [L521](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L521) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.titleCase, ALCHEMY_GUIDE.title, TrinketCatalyst.WndTrinket, Dungeon.saveAll, Badges.saveGlobal, Journal.saveGlobal, ShatteredPixelDungeon.reportException
- [L526](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L526) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, ALCHEMY_GUIDE.title, TrinketCatalyst.WndTrinket, Dungeon.saveAll, Badges.saveGlobal, Journal.saveGlobal, ShatteredPixelDungeon.reportException
- [L554](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L554) `public void update() {` — 행동·상태 갱신, 인접 호출: Game.switchScene, WndBag.ItemSelector, Messages.get, Recipe.usableInRecipe
- [L560](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L560) `protected void onBackPressed() {` — 이벤트·효과 실행, 인접 호출: Game.switchScene, WndBag.ItemSelector, Messages.get, Recipe.usableInRecipe
- [L564](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L564) `protected WndBag.ItemSelector itemSelector = new WndBag.ItemSelector() {` — 개별 처리, 인접 호출: Messages.get, Recipe.usableInRecipe
- [L567](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L567) `public String textPrompt() {` — 개별 처리, 인접 호출: Messages.get, Recipe.usableInRecipe
- [L572](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L572) `public boolean itemSelectable(Item item) {` — 개별 처리, 인접 호출: Recipe.usableInRecipe, Recipe.findRecipes
- [L577](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L577) `public void onSelect( Item item ) {` — 이벤트·효과 실행, 인접 호출: Recipe.findRecipes
- [L578](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L578) `synchronized (inputs) {` — 개별 처리, 인접 호출: Recipe.findRecipes
- [L607](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L607) `private void updateState(){` — 행동·상태 갱신, 인접 호출: Recipe.findRecipes
- [L677](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L677) `private void combine( int slot ){` — 개별 처리, 인접 호출: Recipe.findRecipes, Catalog.countUses, Messages.get
- [L740](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L740) `synchronized (inputs) {` — 개별 처리, 인접 호출: Speck.factory, INSTANCE.play, Badges.validateItemsCrafted, Dungeon.saveAll, Badges.saveGlobal, Journal.saveGlobal, ShatteredPixelDungeon.reportException
- [L754](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L754) `public void craftItem( ArrayList<Item> ingredients, Item result ){` — 개별 처리, 인접 호출: Speck.factory, INSTANCE.play, Badges.validateItemsCrafted, Dungeon.saveAll, Badges.saveGlobal, Journal.saveGlobal, ShatteredPixelDungeon.reportException
- [L776](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L776) `synchronized (inputs) {` — 개별 처리
- [L795](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L795) `public void populate(ArrayList<Item> toFind, Belongings inventory){` — 개별 처리, 인접 호출: Dungeon.saveAll, Badges.saveGlobal, Journal.saveGlobal, ShatteredPixelDungeon.reportException
- [L823](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L823) `public void onPause() {` — 이벤트·효과 실행, 인접 호출: Dungeon.saveAll, Badges.saveGlobal, Journal.saveGlobal, ShatteredPixelDungeon.reportException
- [L839](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L839) `public void destroy() {` — 개별 처리, 인접 호출: Dungeon.saveAll, Badges.saveGlobal, Journal.saveGlobal, ShatteredPixelDungeon.reportException, Messages.get
- [L840](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L840) `synchronized ( inputs ) {` — 개별 처리, 인접 호출: Dungeon.saveAll, Badges.saveGlobal, Journal.saveGlobal, ShatteredPixelDungeon.reportException, Messages.get
- [L858](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L858) `public void clearSlots(){` — 개별 처리, 인접 호출: Messages.get, Speck.factory, INSTANCE.play
- [L859](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L859) `synchronized ( inputs ) {` — 개별 처리, 인접 호출: Messages.get, Speck.factory, INSTANCE.play
- [L877](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L877) `public void createEnergy(){` — 생성·초기화, 인접 호출: Messages.get, Speck.factory, INSTANCE.play, Chrome.get
- [L904](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L904) `public void showIdentify(Item item){` — 개별 처리, 인접 호출: Chrome.get, BG.alpha, BG.killAndErase, Math.ceil, Math.max
- [L911](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L911) `public synchronized void update() {` — 행동·상태 갱신, 인접 호출: BG.alpha, BG.killAndErase, Math.ceil, Math.max
- [L925](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L925) `public synchronized void update() {` — 행동·상태 갱신, 인접 호출: BG.alpha, BG.killAndErase, Math.ceil, Math.max, BG.size
- [L981](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L981) `protected void createChildren() {` — 생성·초기화, 인접 호출: Chrome.get, INSTANCE.play, WndBag.getBag
- [L989](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L989) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, WndBag.getBag
- [L994](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L994) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: WndBag.getBag
- [L998](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L998) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: WndBag.getBag, Messages.get
- [L1012](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1012) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: Messages.get
- [L1023](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1023) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.get
- [L1037](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1037) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, WndBag.Placeholder
- [L1045](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1045) `public GameAction secondaryTooltipAction() {` — 개별 처리, 인접 호출: WndBag.Placeholder
- [L1054](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1054) `protected void layout() {` — 개별 처리, 인접 호출: WndBag.Placeholder
- [L1064](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1064) `public Item item(){` — 개별 처리, 인접 호출: WndBag.Placeholder, Messages.get
- [L1068](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1068) `public void item( Item item ) {` — 개별 처리, 인접 호출: WndBag.Placeholder, Messages.get
- [L1085](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1085) `private CombineButton(int slot){` — 개별 처리, 인접 호출: Messages.get, Icons.get, PixelScene.renderTextBlock
- [L1092](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1092) `protected void createChildren() {` — 생성·초기화, 인접 호출: Messages.get, Icons.get, PixelScene.renderTextBlock
- [L1097](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1097) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.get, Icons.get, PixelScene.renderTextBlock
- [L1103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1103) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, Icons.get, PixelScene.renderTextBlock
- [L1108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1108) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Icons.get, PixelScene.renderTextBlock
- [L1123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1123) `protected void layout() {` — 개별 처리, 인접 호출: Messages.get
- [L1134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1134) `public void enable( boolean enabled ){` — 개별 처리, 인접 호출: Messages.get, Chrome.get
- [L1138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1138) `public void enable( boolean enabled, int cost ){` — 개별 처리, 인접 호출: Messages.get, Chrome.get
- [L1169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1169) `protected void createChildren() {` — 생성·초기화, 인접 호출: Chrome.get
- [L1176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1176) `protected void onClick() {` — 이벤트·효과 실행
- [L1188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1188) `protected void layout() {` — 개별 처리
- [L1198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1198) `public void item( Item item ) {` — 개별 처리
- [L1205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1205) `public static void assignToolkit( AlchemistsToolkit toolkit ){` — 개별 처리
- [L1209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java#L1209) `public static void clearToolkit(){` — 개별 처리

## 974. [`AmuletScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.scenes`, 182행.

### 클래스/타입
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L47) `public class AmuletScene extends PixelScene {`

### 변수·상수 후보
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L49) `private static final int WIDTH			= 120;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L50) `private static final int BTN_HEIGHT		= 20;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L51) `private static final float SMALL_GAP	= 2;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L52) `private static final float LARGE_GAP	= 8;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L54) `public static boolean noText = false;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L56) `private Image amulet;`
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L167) `private float timer = 0;`

### 메서드 및 코드 의존 단서
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L66) `public void create() {` — 생성·초기화, 인접 호출: Messages.get, PixelScene.landscape, Dungeon.win, Dungeon.deleteGame, Badges.saveGlobal, BadgeBanner.isShowingBadges, Game.switchScene
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L80) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Dungeon.win, Dungeon.deleteGame, Badges.saveGlobal, BadgeBanner.isShowingBadges, Game.switchScene, INSTANCE.playTracks, Messages.get
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L89) `protected void onComplete() {` — 이벤트·효과 실행, 인접 호출: BadgeBanner.isShowingBadges, Game.switchScene, INSTANCE.playTracks, Messages.get, CLOSE.get
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L93) `protected void onComplete() {` — 이벤트·효과 실행, 인접 호출: Game.switchScene, INSTANCE.playTracks, Messages.get, CLOSE.get
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L114) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: CLOSE.get
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L160) `protected void onBackPressed() {` — 이벤트·효과 실행, 인접 호출: Game.switchScene, Random.Float
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AmuletScene.java#L170) `public void update() {` — 행동·상태 갱신, 인접 호출: Random.Float

## 975. [`CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.scenes`, 526행.

### 클래스/타입
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L46) `public class CellSelector extends ScrollArea {`
- [L518](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L518) `public static abstract class Listener {`

### 변수·상수 후보
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L48) `public Listener listener = null;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L50) `public boolean enabled;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L52) `private float dragThreshold;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L64) `private float mouseZoom;`
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L173) `private boolean pinching = false;`
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L174) `private PointerEvent another;`
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L175) `private float startZoom;`
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L176) `private float startSpan;`
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L219) `private boolean dragging = false;`
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L250) `private GameAction heldAction1 = SPDAction.NONE;`
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L251) `private GameAction heldAction2 = SPDAction.NONE;`
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L253) `private GameAction heldAction3 = SPDAction.NONE;`
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L255) `private float heldDelay = 0f;`
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L256) `private boolean delayingForRelease = false;`
- [L353](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L353) `private GameAction leftStickAction = SPDAction.NONE;`
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L393) `private int lastCellMoved = 0;`

### 메서드 및 코드 의존 단서
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L54) `public CellSelector( DungeonTilemap map ) {` — 개별 처리, 인접 호출: KeyEvent.addKeyListener, Math.min, GameMath.gate, Math.round, DungeonTilemap.tileCenterToWorld, Math.abs
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L67) `protected void onScroll( ScrollEvent event ) {` — 이벤트·효과 실행, 인접 호출: Math.min, GameMath.gate, Math.round, DungeonTilemap.tileCenterToWorld, Math.abs
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L79) `protected void onClick( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: DungeonTilemap.tileCenterToWorld, Math.abs
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L129) `private float zoom( float value ) {` — 개별 처리, 인접 호출: GameMath.gate, SPDSettings.zoom, Actor.chars, GameScene.interfaceBlockingHero, GameScene.ready, GameScene.cancel
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L152) `public void select( int cell, int button ) {` — 개별 처리, 인접 호출: GameScene.interfaceBlockingHero, GameScene.ready, GameScene.cancel, PointF.distance
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L179) `protected void onPointerDown( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: PointF.distance, Math.round
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L202) `protected void onPointerUp( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: Math.round, PointF.distance, GameMath.gate, PointF.diff
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L220) `private PointF lastPos = new PointF();` — 개별 처리, 인접 호출: PointF.distance, GameMath.gate, PointF.diff, SPDSettings.movementHoldSensitivity
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L223) `protected void onDrag( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: PointF.distance, GameMath.gate, PointF.diff, SPDSettings.movementHoldSensitivity
- [L258](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L258) `private static float initialDelay(){` — 생성·초기화, 인접 호출: SPDSettings.movementHoldSensitivity, KeyBindings.getActionForKey
- [L277](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L277) `public boolean onSignal(KeyEvent event) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getActionForKey
- [L356](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L356) `public void update() {` — 행동·상태 갱신, 인접 호출: GameScene.interfaceBlockingHero, GameScene.cancelCellSelector
- [L395](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L395) `private boolean moveFromActions(GameAction... actions){` — 개별 처리, 인접 호출: GameScene.cancelCellSelector, GameMath.gate
- [L426](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L426) `private Point directionFromAction(GameAction action){` — 개별 처리, 인접 호출: Dungeon.observe
- [L439](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L439) `private GameAction actionFromStick(float x, float y){` — 행동·상태 갱신, 인접 호출: Dungeon.observe
- [L464](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L464) `public void processKeyHold() {` — 행동·상태 갱신, 인접 호출: Dungeon.observe, GameScene.ready, Math.round
- [L482](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L482) `public void resetKeyHold(){` — 개별 처리, 인접 호출: GameScene.ready, Math.round, KeyEvent.removeKeyListener
- [L486](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L486) `public void cancel() {` — 조회·판정, 인접 호출: GameScene.ready, Math.round, KeyEvent.removeKeyListener
- [L496](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L496) `public void reset() {` — 개별 처리, 인접 호출: Math.round, KeyEvent.removeKeyListener
- [L506](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L506) `public void enable(boolean value){` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener
- [L513](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L513) `public void destroy() {` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener
- [L519](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L519) `public abstract void onSelect( Integer cell );` — 이벤트·효과 실행
- [L521](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L521) `public void onRightClick( Integer cell ){} //do nothing by default` — 이벤트·효과 실행
- [L523](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java#L523) `public abstract String prompt();` — 개별 처리


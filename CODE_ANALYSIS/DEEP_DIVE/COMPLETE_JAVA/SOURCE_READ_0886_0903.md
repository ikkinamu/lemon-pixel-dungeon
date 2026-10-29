# Java 소스 구현 분석 886–903

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 886. [`HallwayRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/HallwayRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 159행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/HallwayRoom.java#L35) `public class HallwayRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/HallwayRoom.java#L38) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set, Painter.fill
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/HallwayRoom.java#L43) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set, Painter.fill
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/HallwayRoom.java#L48) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {` — 조회·판정, 인접 호출: Painter.set, Painter.fill
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/HallwayRoom.java#L53) `public void merge(Level l, Room other, Rect merge, int mergeTerrain) {` — 개별 처리, 인접 호출: Painter.set, Painter.fill
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/HallwayRoom.java#L60) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.drawLine
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/HallwayRoom.java#L131) `protected Rect getConnectionSpace(){` — 조회·판정, 인접 호출: GameMath.gate, Random.Float
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/HallwayRoom.java#L141) `protected final Point getDoorCenter(){` — 조회·판정, 인접 호출: Random.Float, GameMath.gate

## 887. [`ImpShopRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 162행.

### 클래스/타입
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L42) `public class ImpShopRoom extends ShopRoom {`

### 변수·상수 후보
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L44) `private boolean impSpawned = false;`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L134) `private static final String IMP = "imp_spawned";`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L135) `private static final String ITEMS = "items";`

### 메서드 및 코드 의존 단서
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L48) `public int minWidth() {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, GameScene.add
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L51) `public int minHeight() {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, GameScene.add
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L54) `public int maxWidth() { return 9; }` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, GameScene.add
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L55) `public int maxHeight() { return 9; }` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, GameScene.add
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L58) `public int maxConnections(int direction) {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, GameScene.add
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L63) `public void paint(Level level) {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, GameScene.add
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L72) `protected void placeShopkeeper(Level level) {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, GameScene.add
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L95) `public Door entrance() {` — 개별 처리, 인접 호출: Random.Int
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L99) `public void spawnShop(Level level){` — 개별 처리, 인접 호출: Random.Int
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L106) `protected void placeItems(Level level) {` — 개별 처리, 인접 호출: Random.Int
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L130) `public boolean shopSpawned(){` — 개별 처리, 인접 호출: Quest.isCompleted, Quest.earnedShop
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L138) `public void storeInBundle(Bundle bundle) {` — 저장·복원, 인접 호출: Quest.isCompleted, Quest.earnedShop
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L145) `public void restoreFromBundle(Bundle bundle) {` — 저장·복원, 인접 호출: Quest.isCompleted, Quest.earnedShop
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ImpShopRoom.java#L154) `public void onLevelLoad(Level level) {` — 이벤트·효과 실행, 인접 호출: Quest.isCompleted, Quest.earnedShop

## 888. [`LibraryHallRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryHallRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 145행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryHallRoom.java#L30) `public class LibraryHallRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryHallRoom.java#L33) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryHallRoom.java#L38) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Random.Int
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryHallRoom.java#L43) `public float[] sizeCatProbs(){` — 개별 처리, 인접 호출: Painter.fill, Random.Int
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryHallRoom.java#L50) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Random.Int, Painter.drawLine

## 889. [`LibraryRingRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryRingRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 80행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryRingRoom.java#L31) `public class LibraryRingRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryRingRoom.java#L34) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.drawInside
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryRingRoom.java#L39) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.drawInside
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryRingRoom.java#L44) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Painter.drawInside
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryRingRoom.java#L50) `public Rect resize(int w, int h) {` — 개별 처리, 인접 호출: Painter.fill, Painter.drawInside
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/LibraryRingRoom.java#L60) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.drawInside

## 890. [`MinefieldRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/MinefieldRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 99행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/MinefieldRoom.java#L34) `public class MinefieldRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/MinefieldRoom.java#L37) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Math.round, Math.sqrt, TrapMechanism.revealHiddenTrapChance, Random.Int, Painter.set
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/MinefieldRoom.java#L42) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {` — 조회·판정, 인접 호출: Painter.fill, Math.round, Math.sqrt, TrapMechanism.revealHiddenTrapChance, Random.Int, Painter.set
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/MinefieldRoom.java#L48) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Math.round, Math.sqrt, TrapMechanism.revealHiddenTrapChance, Random.Int, Painter.set

## 891. [`PatchRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PatchRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 140행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PatchRoom.java#L31) `public abstract class PatchRoom extends StandardRoom {`

### 변수·상수 후보
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PatchRoom.java#L33) `protected boolean[] patch;`

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PatchRoom.java#L35) `protected abstract float fill();` — 개별 처리, 인접 호출: PathFinder.setMapSize, Patch.generate, PathFinder.buildDistanceMap, BArray.not
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PatchRoom.java#L36) `protected abstract int clustering();` — 개별 처리, 인접 호출: PathFinder.setMapSize, Patch.generate, PathFinder.buildDistanceMap, BArray.not
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PatchRoom.java#L37) `protected abstract boolean ensurePath();` — 개별 처리, 인접 호출: PathFinder.setMapSize, Patch.generate, PathFinder.buildDistanceMap, BArray.not
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PatchRoom.java#L38) `protected abstract boolean cleanEdges();` — 개별 처리, 인접 호출: PathFinder.setMapSize, Patch.generate, PathFinder.buildDistanceMap, BArray.not
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PatchRoom.java#L40) `protected void setupPatch(Level level){` — 생성·초기화, 인접 호출: PathFinder.setMapSize, Patch.generate, PathFinder.buildDistanceMap, BArray.not
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PatchRoom.java#L95) `protected void fillPatch(Level level, int terrain){` — 개별 처리
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PatchRoom.java#L108) `protected void cleanDiagonalEdges(){` — 개별 처리
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PatchRoom.java#L136) `protected int xyToPatchCoords(int x, int y){` — 개별 처리

## 892. [`PillarsRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PillarsRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 107행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PillarsRoom.java#L29) `public class PillarsRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PillarsRoom.java#L32) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Math.min, Random.Int, Random.IntRange
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PillarsRoom.java#L37) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Math.min, Random.Int, Random.IntRange
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PillarsRoom.java#L42) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Math.min, Random.Int, Random.IntRange
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PillarsRoom.java#L47) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Math.min, Random.Int, Random.IntRange, Math.round, Random.Float

## 893. [`PlantsRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlantsRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 129행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlantsRoom.java#L35) `public class PlantsRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlantsRoom.java#L38) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Math.min, Painter.drawLine
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlantsRoom.java#L43) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Math.min, Painter.drawLine
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlantsRoom.java#L48) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Math.min, Math.max, Painter.drawLine, Random.Int
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlantsRoom.java#L53) `public void merge(Level l, Room other, Rect merge, int mergeTerrain) {` — 개별 처리, 인접 호출: Painter.fill, Math.min, Math.max, Painter.drawLine, Random.Int
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlantsRoom.java#L63) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Math.min, Math.max, Painter.drawLine, Random.Int
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlantsRoom.java#L112) `public boolean canPlaceItem(Point p, Level l) {` — 조회·판정, 인접 호출: Generator.randomUsingDefaults
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlantsRoom.java#L117) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정, 인접 호출: Generator.randomUsingDefaults
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlantsRoom.java#L121) `private static Plant.Seed randomSeed(){` — 개별 처리, 인접 호출: Generator.randomUsingDefaults

## 894. [`PlatformRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlatformRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 117행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlatformRoom.java#L33) `public class PlatformRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlatformRoom.java#L36) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set, Painter.fill, Painter.drawInside
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlatformRoom.java#L41) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set, Painter.fill, Painter.drawInside
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlatformRoom.java#L46) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set, Painter.fill, Painter.drawInside, Random.Float, Random.Int
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlatformRoom.java#L51) `public void merge(Level l, Room other, Rect merge, int mergeTerrain) {` — 개별 처리, 인접 호출: Painter.set, Painter.fill, Painter.drawInside, Random.Float, Random.Int, Random.IntRange
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlatformRoom.java#L62) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.drawInside, Random.Float, Random.Int, Random.IntRange, Random.NormalIntRange
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/PlatformRoom.java#L82) `private void splitPlatforms( Rect curPlatform, ArrayList<Rect> allPlatforms ){` — 개별 처리, 인접 호출: Random.Float, Random.Int, Random.IntRange, Random.NormalIntRange

## 895. [`RegionDecoBridgeRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoBridgeRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 47행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoBridgeRoom.java#L27) `public class RegionDecoBridgeRoom extends StandardBridgeRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoBridgeRoom.java#L30) `public float[] sizeCatProbs(){` — 개별 처리
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoBridgeRoom.java#L34) `protected int maxBridgeWidth( int roomDimension ) {` — 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoBridgeRoom.java#L38) `protected int spaceTile(){` — 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoBridgeRoom.java#L43) `protected int bridgeTile() {` — 개별 처리

## 896. [`RegionDecoLineRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoLineRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 34행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoLineRoom.java#L26) `public class RegionDecoLineRoom extends StatueLineRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoLineRoom.java#L29) `protected int decoTerrain() {` — 개별 처리

## 897. [`RegionDecoPatchRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoPatchRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 76행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoPatchRoom.java#L29) `public class RegionDecoPatchRoom extends PatchRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoPatchRoom.java#L32) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Math.min, Painter.fill
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoPatchRoom.java#L37) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Math.min, Painter.fill
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoPatchRoom.java#L42) `protected float fill() {` — 개별 처리, 인접 호출: Math.min, Painter.fill
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoPatchRoom.java#L49) `protected int clustering() {` — 개별 처리, 인접 호출: Painter.fill
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoPatchRoom.java#L54) `protected boolean ensurePath() {` — 개별 처리, 인접 호출: Painter.fill
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoPatchRoom.java#L59) `protected boolean cleanEdges() {` — 개별 처리, 인접 호출: Painter.fill
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RegionDecoPatchRoom.java#L64) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill

## 898. [`RingRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RingRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 106행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RingRoom.java#L30) `public class RingRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RingRoom.java#L33) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Math.min, Math.floor, Random.Int
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RingRoom.java#L38) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Math.min, Math.floor, Random.Int, Painter.set
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RingRoom.java#L43) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Math.min, Math.floor, Random.Int, Painter.set
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RingRoom.java#L48) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Math.min, Math.floor, Random.Int, Painter.set
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RingRoom.java#L98) `protected int centerDecoTiles(){` — 개별 처리
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RingRoom.java#L102) `protected void placeCenterDetail(Level level, int pos){` — 개별 처리

## 899. [`RitualRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RitualRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 115행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RitualRoom.java#L32) `public class RitualRoom extends PatchRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RitualRoom.java#L35) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Math.min, Painter.fill
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RitualRoom.java#L40) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Math.min, Painter.fill
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RitualRoom.java#L45) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Math.min, Painter.fill, Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RitualRoom.java#L50) `protected float fill() {` — 개별 처리, 인접 호출: Math.min, Painter.fill, Painter.set
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RitualRoom.java#L61) `protected int clustering() {` — 개별 처리, 인접 호출: Painter.fill, Painter.set
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RitualRoom.java#L66) `protected boolean ensurePath() {` — 개별 처리, 인접 호출: Painter.fill, Painter.set, Random.Int, Generator.random, Random.oneOf
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RitualRoom.java#L71) `protected boolean cleanEdges() {` — 개별 처리, 인접 호출: Painter.fill, Painter.set, Random.Int, Generator.random, Random.oneOf
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RitualRoom.java#L76) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.set, Random.Int, Generator.random, Random.oneOf
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RitualRoom.java#L105) `protected void placeloot(Level level, Point p){` — 개별 처리, 인접 호출: Random.Int, Generator.random, Random.oneOf

## 900. [`RuinsRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RuinsRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 101행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RuinsRoom.java#L31) `public class RuinsRoom extends PatchRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RuinsRoom.java#L34) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Math.min, Painter.fill
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RuinsRoom.java#L39) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {` — 조회·판정, 인접 호출: Math.min, Painter.fill
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RuinsRoom.java#L44) `protected float fill() {` — 개별 처리, 인접 호출: Math.min, Painter.fill
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RuinsRoom.java#L54) `protected int clustering() {` — 개별 처리, 인접 호출: Painter.fill, Random.Int
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RuinsRoom.java#L59) `protected boolean ensurePath() {` — 개별 처리, 인접 호출: Painter.fill, Random.Int
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RuinsRoom.java#L64) `protected boolean cleanEdges() {` — 개별 처리, 인접 호출: Painter.fill, Random.Int
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/RuinsRoom.java#L69) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Random.Int

## 901. [`SegmentedLibraryRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SegmentedLibraryRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 138행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SegmentedLibraryRoom.java#L33) `public class SegmentedLibraryRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SegmentedLibraryRoom.java#L36) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Painter.drawInside, Math.max, Math.min
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SegmentedLibraryRoom.java#L41) `public void paint( Level level ) {` — 개별 처리, 인접 호출: Painter.fill, Painter.drawInside, Math.max, Math.min, Random.Int
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SegmentedLibraryRoom.java#L77) `private void createWalls( Level level, Rect area ){` — 생성·초기화, 인접 호출: Math.max, Math.min, Random.Int, Random.IntRange, Painter.drawLine, Painter.set

## 902. [`SegmentedRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SegmentedRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 117행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SegmentedRoom.java#L31) `public class SegmentedRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SegmentedRoom.java#L34) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set, Math.min, Random.Int, Random.IntRange
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SegmentedRoom.java#L39) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set, Math.min, Random.Int, Random.IntRange, Painter.drawLine
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SegmentedRoom.java#L44) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Painter.set, Math.max, Math.min, Random.Int, Random.IntRange, Painter.drawLine
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SegmentedRoom.java#L49) `public void paint( Level level ) {` — 개별 처리, 인접 호출: Painter.fill, Painter.set, Math.max, Math.min, Random.Int, Random.IntRange, Painter.drawLine
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SegmentedRoom.java#L62) `private void createWalls( Level level, Rect area ){` — 생성·초기화, 인접 호출: Math.max, Math.min, Random.Int, Random.IntRange, Painter.drawLine, Painter.set

## 903. [`SewerPipeRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 323행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L37) `public class SewerPipeRoom extends StandardRoom {`

### 변수·상수 후보
- [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L262) `private Point[] corners;`

### 메서드 및 코드 의존 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L40) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L45) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L50) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L55) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {` — 조회·판정, 인접 호출: Painter.fill
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L60) `public boolean canConnect(Point p) {` — 조회·판정, 인접 호출: Painter.fill
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L67) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.drawLine
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L209) `protected Rect getConnectionSpace(){` — 조회·판정, 인접 호출: Random.Float, GameMath.gate, Math.abs, Math.max, Math.min
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L216) `public boolean canPlaceWater(Point p) {` — 조회·판정, 인접 호출: Random.Float, GameMath.gate, Math.abs, Math.max, Math.min
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L221) `protected final Point getDoorCenter(){` — 조회·판정, 인접 호출: Random.Float, GameMath.gate, Math.abs, Math.max, Math.min
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L238) `private int spaceBetween(int a, int b){` — 개별 처리, 인접 호출: Math.abs, Math.max, Math.min, Painter.fill
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L243) `private int distanceBetweenPoints(Point a, Point b){` — 개별 처리, 인접 호출: Math.max, Math.min, Painter.fill
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SewerPipeRoom.java#L265) `private void fillBetweenPoints(Level level, Point from, Point to, int floor){` — 개별 처리, 인접 호출: Painter.fill, Math.min, Painter.drawLine


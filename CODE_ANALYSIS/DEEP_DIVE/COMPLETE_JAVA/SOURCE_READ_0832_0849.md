# 실제 Java 소스 정적 분석 832–849

기준 `bd3a990254e4249458816f4879e93ab87275555b`. 모든 항목의 원문을 불러와 타입·상태 변수·메서드와 호출 표현을 조사한다. 기능명은 **정적 의미 추론**이며 AST/런타임 검증이 아니다. 다중행·익명 구조 누락 가능.

## 832. [`BurnedRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/BurnedRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard` / 136행

### 타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/BurnedRoom.java#L33) `public class BurnedRoom extends PatchRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/BurnedRoom.java#L36) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.min, Painter.fill, TrapMechanism.revealHiddenTrapChance
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/BurnedRoom.java#L41) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {`: 조회·조건, 조건문, 반복문; 인접 호출 Math.min, Painter.fill, TrapMechanism.revealHiddenTrapChance, Random.Int
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/BurnedRoom.java#L47) `protected float fill() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.min, Painter.fill, TrapMechanism.revealHiddenTrapChance, Random.Int
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/BurnedRoom.java#L54) `protected int clustering() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, TrapMechanism.revealHiddenTrapChance, Random.Int
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/BurnedRoom.java#L59) `protected boolean ensurePath() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, TrapMechanism.revealHiddenTrapChance, Random.Int
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/BurnedRoom.java#L64) `protected boolean cleanEdges() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, TrapMechanism.revealHiddenTrapChance, Random.Int
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/BurnedRoom.java#L69) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, TrapMechanism.revealHiddenTrapChance, Random.Int
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/BurnedRoom.java#L121) `public boolean canPlaceWater(Point p) {`: 조회·조건
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/BurnedRoom.java#L126) `public boolean canPlaceGrass(Point p) {`: 조회·조건
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/BurnedRoom.java#L131) `public boolean canPlaceTrap(Point p) {`: 조회·조건

## 833. [`CaveRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CaveRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard` / 82행

### 타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CaveRoom.java#L28) `public class CaveRoom extends PatchRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CaveRoom.java#L31) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Math.max, Math.min, Painter.fill
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CaveRoom.java#L36) `public int minHeight() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Math.max, Math.min, Painter.fill
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CaveRoom.java#L41) `public int minWidth() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Math.max, Math.min, Painter.fill
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CaveRoom.java#L46) `protected float fill() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Math.min, Painter.fill
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CaveRoom.java#L56) `protected int clustering() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CaveRoom.java#L61) `protected boolean ensurePath() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CaveRoom.java#L66) `protected boolean cleanEdges() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CaveRoom.java#L71) `public void paint(Level level) {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill

## 834. [`CavesFissureRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard` / 325행

### 타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java#L35) `public class CavesFissureRoom extends StandardRoom {`

### 필드·상수
- [L310](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java#L310) `private static final double A = 180 / Math.PI;`

### 메서드와 연관 호출
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java#L38) `public int minWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, PathFinder.setMapSize, Painter.fill
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java#L43) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, PathFinder.setMapSize, Painter.fill
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java#L48) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 PathFinder.setMapSize, Painter.fill
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java#L53) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {`: 조회·조건, 조건문, 반복문; 인접 호출 PathFinder.setMapSize, Painter.fill
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java#L63) `public boolean canPlaceItem(Point p, Level l) {`: 조회·조건, 조건문, 반복문; 인접 호출 PathFinder.setMapSize, Painter.fill, Random.Float, Math.abs
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java#L68) `public boolean canPlaceCharacter(Point p, Level l) {`: 조회·조건, 조건문, 반복문; 인접 호출 PathFinder.setMapSize, Painter.fill, Random.Float, Math.abs
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java#L73) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 PathFinder.setMapSize, Painter.fill, Random.Float, Math.abs
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java#L243) `private void buildBridge( Level level, float fisssureAngle, PointF center, int centerMargin){`: 생성·초기화, 조건문, 반복문; 인접 호출 Math.cos, Math.sin, Math.abs, Random.IntRange, Painter.set
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java#L312) `protected static float angleBetweenPoints( PointF from, PointF to ){`: 개별 처리(본문 확인), 조건문; 인접 호출 Math.atan
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CavesFissureRoom.java#L320) `protected int xyToRoomCoords(int x, int y){`: 개별 처리(본문 확인)

## 835. [`CellBlockRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CellBlockRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard` / 124행

### 타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CellBlockRoom.java#L30) `public class CellBlockRoom extends StandardRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CellBlockRoom.java#L33) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CellBlockRoom.java#L38) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int

## 836. [`ChasmBridgeRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmBridgeRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard` / 37행

### 타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmBridgeRoom.java#L26) `public class ChasmBridgeRoom extends StandardBridgeRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmBridgeRoom.java#L28) `protected int maxBridgeWidth( int roomDimension ) {`: 개별 처리(본문 확인)
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmBridgeRoom.java#L32) `protected int spaceTile(){`: 개별 처리(본문 확인)

## 837. [`ChasmRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard` / 97행

### 타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmRoom.java#L30) `public class ChasmRoom extends PatchRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmRoom.java#L33) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문; 인접 호출 Math.max, Math.min, Painter.set
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmRoom.java#L38) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Math.min, Painter.set, Painter.fill
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmRoom.java#L43) `public int minWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Math.min, Painter.set, Painter.fill
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmRoom.java#L48) `protected float fill() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.min, Painter.set, Painter.fill
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmRoom.java#L58) `protected int clustering() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.set, Painter.fill
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmRoom.java#L63) `protected boolean ensurePath() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.set, Painter.fill
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmRoom.java#L68) `protected boolean cleanEdges() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.set, Painter.fill
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmRoom.java#L73) `public void merge(Level l, Room other, Rect merge, int mergeTerrain) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.set, Painter.fill
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/ChasmRoom.java#L84) `public void paint(Level level) {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill

## 838. [`CircleBasinRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleBasinRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard` / 119행

### 타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleBasinRoom.java#L30) `public class CircleBasinRoom extends PatchRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleBasinRoom.java#L33) `public int minWidth() { return sizeCat.minDim+1; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleBasinRoom.java#L34) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleBasinRoom.java#L39) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleBasinRoom.java#L45) `public Rect resize(int w, int h) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside, Painter.drawLine
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleBasinRoom.java#L53) `protected float fill() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside, Painter.drawLine, Painter.set
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleBasinRoom.java#L58) `protected int clustering() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside, Painter.drawLine, Painter.set
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleBasinRoom.java#L63) `protected boolean ensurePath() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside, Painter.drawLine, Painter.set
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleBasinRoom.java#L68) `protected boolean cleanEdges() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside, Painter.drawLine, Painter.set
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleBasinRoom.java#L73) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside, Painter.drawLine, Painter.set

## 839. [`CirclePitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CirclePitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard` / 107행

### 타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CirclePitRoom.java#L30) `public class CirclePitRoom extends StandardRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CirclePitRoom.java#L33) `public int minWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Painter.fill, Painter.fillEllipse, Painter.drawInside, Random.Int, Random.IntRange
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CirclePitRoom.java#L38) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Painter.fill, Painter.fillEllipse, Painter.drawInside, Random.Int, Random.IntRange
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CirclePitRoom.java#L43) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside, Random.Int, Random.IntRange
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CirclePitRoom.java#L48) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside, Random.Int, Random.IntRange, Painter.drawLine

## 840. [`CircleWallRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleWallRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard` / 52행

### 타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleWallRoom.java#L28) `public class CircleWallRoom extends StandardRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleWallRoom.java#L31) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/CircleWallRoom.java#L36) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside

## 841. [`EmptyRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/EmptyRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard` / 40행

### 타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/EmptyRoom.java#L28) `public class EmptyRoom extends StandardRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/EmptyRoom.java#L31) `public void paint(Level level) {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill

## 842. [`CaveEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CaveEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance` / 86행

### 타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CaveEntranceRoom.java#L31) `public class CaveEntranceRoom extends CaveRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CaveEntranceRoom.java#L34) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CaveEntranceRoom.java#L39) `public int minWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Painter.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CaveEntranceRoom.java#L44) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.set
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CaveEntranceRoom.java#L49) `public boolean isEntrance() {`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.set
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CaveEntranceRoom.java#L54) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.set

## 843. [`CavesFissureEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CavesFissureEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance` / 65행

### 타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CavesFissureEntranceRoom.java#L31) `public class CavesFissureEntranceRoom extends CavesFissureRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CavesFissureEntranceRoom.java#L34) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CavesFissureEntranceRoom.java#L39) `public boolean isEntrance() {`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CavesFissureEntranceRoom.java#L44) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.set

## 844. [`CellBlockEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CellBlockEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance` / 72행

### 타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CellBlockEntranceRoom.java#L32) `public class CellBlockEntranceRoom extends CellBlockRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CellBlockEntranceRoom.java#L35) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.set
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CellBlockEntranceRoom.java#L40) `public boolean isEntrance() {`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.set
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CellBlockEntranceRoom.java#L45) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.set

## 845. [`ChasmBridgeEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmBridgeEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance` / 67행

### 타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmBridgeEntranceRoom.java#L31) `public class ChasmBridgeEntranceRoom extends ChasmBridgeRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmBridgeEntranceRoom.java#L34) `public int minWidth() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Math.max, Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmBridgeEntranceRoom.java#L39) `public int minHeight() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Math.max, Painter.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmBridgeEntranceRoom.java#L44) `public boolean isEntrance() {`: 조회·조건, 반복문; 인접 호출 Painter.set
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmBridgeEntranceRoom.java#L49) `public void paint(Level level) {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.set

## 846. [`ChasmEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance` / 86행

### 타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmEntranceRoom.java#L31) `public class ChasmEntranceRoom extends ChasmRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmEntranceRoom.java#L34) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmEntranceRoom.java#L39) `public int minWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Painter.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmEntranceRoom.java#L44) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.set
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmEntranceRoom.java#L49) `public boolean isEntrance() {`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.set
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/ChasmEntranceRoom.java#L54) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.set

## 847. [`CircleBasinEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CircleBasinEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance` / 53행

### 타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CircleBasinEntranceRoom.java#L30) `public class CircleBasinEntranceRoom extends CircleBasinRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CircleBasinEntranceRoom.java#L33) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인); 인접 호출 Painter.set
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CircleBasinEntranceRoom.java#L38) `public boolean isEntrance() {`: 조회·조건; 인접 호출 Painter.set
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/CircleBasinEntranceRoom.java#L43) `public void paint(Level level) {`: 개별 처리(본문 확인); 인접 호출 Painter.set

## 848. [`EntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance` / 189행

### 타입
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java#L42) `public class EntranceRoom extends StandardRoom {`

### 필드·상수
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java#L163) `private static float[][] chances = new float[27][];`

### 메서드와 연관 호출
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java#L45) `public int minWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Painter.fill, Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java#L50) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Painter.fill, Painter.set
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java#L55) `public boolean isEntrance() {`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Random.pushGenerator
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java#L60) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Random.pushGenerator, ADVENTURERS_GUIDE.isPageRead, SPDSettings.intro
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java#L69) `public boolean canPlaceTrap(Point p) {`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Random.pushGenerator, ADVENTURERS_GUIDE.isPageRead, SPDSettings.intro, Random.IntRange, ADVENTURERS_GUIDE.deletePage
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java#L77) `public void paint(Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Random.pushGenerator, ADVENTURERS_GUIDE.isPageRead, SPDSettings.intro, Random.IntRange, ADVENTURERS_GUIDE.deletePage, ADVENTURERS_GUIDE.isPageFound
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java#L102) `public static void placeEarlyGuidePages(Level level, Room r){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.pushGenerator, ADVENTURERS_GUIDE.isPageRead, SPDSettings.intro, Random.IntRange, ADVENTURERS_GUIDE.deletePage, ADVENTURERS_GUIDE.isPageFound, Random.popGenerator
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java#L184) `public static StandardRoom createEntrance(){`: 생성·초기화; 인접 호출 Reflection.newInstance, Random.chances

## 849. [`HallwayEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/HallwayEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance` / 53행

### 타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/HallwayEntranceRoom.java#L31) `public class HallwayEntranceRoom extends HallwayRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/HallwayEntranceRoom.java#L34) `public boolean isEntrance() {`: 조회·조건, 조건문, 반복문
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/HallwayEntranceRoom.java#L39) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문


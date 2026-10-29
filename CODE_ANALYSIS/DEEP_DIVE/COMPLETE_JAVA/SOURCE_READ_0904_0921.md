# Java 소스 구현 분석 904–921

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 904. [`SkullsRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SkullsRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 66행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SkullsRoom.java#L28) `public class SkullsRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SkullsRoom.java#L31) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.fillEllipse, Painter.drawInside
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SkullsRoom.java#L36) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.fillEllipse, Painter.drawInside
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SkullsRoom.java#L41) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Painter.fillEllipse, Painter.drawInside
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SkullsRoom.java#L46) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.fillEllipse, Painter.drawInside

## 905. [`StandardBridgeRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 186행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L36) `public abstract class StandardBridgeRoom extends StandardRoom {`

### 변수·상수 후보
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L65) `protected Rect spaceRect;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L66) `protected Rect bridgeRect;`

### 메서드 및 코드 의존 단서
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L39) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L44) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Random.Int
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L49) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {` — 조회·판정, 인접 호출: Painter.fill, Random.Int
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L55) `public boolean canPlaceItem(Point p, Level l) {` — 조회·판정, 인접 호출: Painter.fill, Random.Int, Collections.sort
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L60) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정, 인접 호출: Painter.fill, Random.Int, Collections.sort
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L69) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Random.Int, Collections.sort
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L100) `public int compare(Point d1, Point d2) {` — 개별 처리, 인접 호출: Random.Int, Random.NormalIntRange, Collections.sort
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L142) `public int compare(Point d1, Point d2) {` — 개별 처리, 인접 호출: Random.Int, Random.NormalIntRange, Painter.fill
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L176) `protected abstract int maxBridgeWidth( int roomDimension );` — 개별 처리
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L178) `protected abstract int spaceTile();` — 개별 처리
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardBridgeRoom.java#L181) `protected int bridgeTile(){` — 개별 처리

## 906. [`StandardRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 195행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L34) `public abstract class StandardRoom extends Room {`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L36) `public enum SizeCategory {`

### 변수·상수 후보
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L42) `public final int minDim, maxDim;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L43) `public final int roomValue;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L53) `public SizeCategory sizeCat;`
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L169) `private static float[][] chances = new float[27][];`

### 메서드 및 코드 의존 단서
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L58) `public float[] sizeCatProbs(){` — 개별 처리, 인접 호출: SizeCategory.values, Random.chances
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L63) `public boolean setSizeCat(){` — 개별 처리, 인접 호출: SizeCategory.values, Random.chances
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L68) `public boolean setSizeCat( int maxRoomValue ){` — 개별 처리, 인접 호출: SizeCategory.values, Random.chances
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L73) `public boolean setSizeCat( int minOrdinal, int maxOrdinal ) {` — 개별 처리, 인접 호출: SizeCategory.values, Random.chances
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L93) `public int minWidth() { return sizeCat.minDim; }` — 개별 처리
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L94) `public int maxWidth() { return sizeCat.maxDim; }` — 개별 처리
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L97) `public int minHeight() { return sizeCat.minDim; }` — 개별 처리
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L98) `public int maxHeight() { return sizeCat.maxDim; }` — 개별 처리
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L102) `public int sizeFactor(){` — 개별 처리
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L106) `public int mobSpawnWeight(){` — 개별 처리
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L113) `public int connectionWeight(){` — 개별 처리
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L118) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {` — 조회·판정
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L190) `public static StandardRoom createRoom(){` — 생성·초기화, 인접 호출: Reflection.newInstance, Random.chances

## 907. [`StatueLineRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatueLineRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 110행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatueLineRoom.java#L31) `public class StatueLineRoom extends StandardRoom {`

### 변수·상수 후보
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatueLineRoom.java#L43) `private static final Integer N = 0;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatueLineRoom.java#L44) `private static final Integer E = 1;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatueLineRoom.java#L45) `private static final Integer S = 2;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatueLineRoom.java#L46) `private static final Integer W = 3;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatueLineRoom.java#L34) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Random.chances
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatueLineRoom.java#L39) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Random.chances
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatueLineRoom.java#L49) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Random.chances, Painter.drawInside
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatueLineRoom.java#L88) `protected int decoTerrain(){` — 개별 처리, 인접 호출: Painter.drawLine
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatueLineRoom.java#L92) `private void fillAlongSide(Integer side, Level level){` — 개별 처리, 인접 호출: Painter.drawLine

## 908. [`StatuesRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatuesRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 111행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatuesRoom.java#L30) `public class StatuesRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatuesRoom.java#L33) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatuesRoom.java#L38) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatuesRoom.java#L43) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Painter.set
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StatuesRoom.java#L48) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.set, Random.Int

## 909. [`StripedRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StripedRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 75행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StripedRoom.java#L31) `public class StripedRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StripedRoom.java#L34) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Random.Int, Math.min
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StripedRoom.java#L39) `public void merge(Level l, Room other, Rect merge, int mergeTerrain) {` — 개별 처리, 인접 호출: Painter.fill, Random.Int, Math.min
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StripedRoom.java#L49) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Random.Int, Math.min

## 910. [`StudyRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StudyRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 92행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StudyRoom.java#L32) `public class StudyRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StudyRoom.java#L35) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.drawInside, Painter.set
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StudyRoom.java#L40) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.drawInside, Painter.set, Random.Int
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StudyRoom.java#L45) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Painter.drawInside, Painter.set, Random.Int, Generator.random, Random.oneOf
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StudyRoom.java#L50) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.drawInside, Painter.set, Random.Int, Generator.random, Random.oneOf

## 911. [`SuspiciousChestRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SuspiciousChestRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 73행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SuspiciousChestRoom.java#L34) `public class SuspiciousChestRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SuspiciousChestRoom.java#L37) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set, MimicTooth.mimicChanceMultiplier, Random.Float, Mimic.spawnAt
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SuspiciousChestRoom.java#L42) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set, MimicTooth.mimicChanceMultiplier, Random.Float, Mimic.spawnAt
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/SuspiciousChestRoom.java#L47) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.set, MimicTooth.mimicChanceMultiplier, Random.Float, Mimic.spawnAt

## 912. [`WaterBridgeRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/WaterBridgeRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 43행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/WaterBridgeRoom.java#L27) `public class WaterBridgeRoom extends StandardBridgeRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/WaterBridgeRoom.java#L29) `protected int maxBridgeWidth( int roomDimension ) {` — 개별 처리
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/WaterBridgeRoom.java#L33) `protected int spaceTile(){` — 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/WaterBridgeRoom.java#L38) `public boolean canPlaceWater(Point p) {` — 조회·판정

## 913. [`SewerBossLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels`, 233행.

### 클래스/타입
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L54) `public class SewerBossLevel extends SewerLevel {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L62) `public void playLevelMusic() {` — 개별 처리, 인접 호출: INSTANCE.play, INSTANCE.end, INSTANCE.playTracks, StandardRoom.createRoom, GooBossRoom.randomGooRoom
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L85) `protected ArrayList<Room> initRooms() {` — 생성·초기화, 인접 호출: StandardRoom.createRoom, GooBossRoom.randomGooRoom, Random.chances, Random.Float
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L107) `protected int standardRooms(boolean forceMax) {` — 개별 처리, 인접 호출: Random.chances, Random.Float, Random.pushGenerator, Random.Long, Bones.get
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L113) `protected Builder builder(){` — 생성·초기화, 인접 호출: Random.Float, Random.pushGenerator, Random.Long, Bones.get, Random.popGenerator
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L121) `protected Painter painter() {` — 개별 처리, 인접 호출: Random.pushGenerator, Random.Long, Bones.get, Random.popGenerator, Actor.findChar, Char.hasProp
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L128) `protected int nTraps() {` — 개별 처리, 인접 호출: Random.pushGenerator, Random.Long, Bones.get, Random.popGenerator, Actor.findChar, Char.hasProp, Random.element
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L133) `protected void createMobs() {` — 생성·초기화, 인접 호출: Random.pushGenerator, Random.Long, Bones.get, Random.popGenerator, Actor.findChar, Char.hasProp, Random.element
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L136) `public Actor addRespawner() {` — 개별 처리, 인접 호출: Random.pushGenerator, Random.Long, Bones.get, Random.popGenerator, Actor.findChar, Char.hasProp, Random.element
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L141) `protected void createItems() {` — 생성·초기화, 인접 호출: Random.pushGenerator, Random.Long, Bones.get, Random.popGenerator, Actor.findChar, Char.hasProp, Random.element
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L157) `public int randomRespawnCell( Char ch ) {` — 개별 처리, 인접 호출: Actor.findChar, Char.hasProp, Random.element, GameScene.updateMap, GameScene.ripple, Game.runOnRenderThread, INSTANCE.play
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L177) `public void seal() {` — 개별 처리, 인접 호출: GameScene.updateMap, GameScene.ripple, Game.runOnRenderThread, INSTANCE.play, INSTANCE.fadeOut, INSTANCE.end
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L190) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play, GameScene.updateMap, Game.runOnRenderThread, INSTANCE.fadeOut, INSTANCE.end, PrisonLevel.Torch
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L197) `public void unseal() {` — 개별 처리, 인접 호출: GameScene.updateMap, Game.runOnRenderThread, INSTANCE.fadeOut, INSTANCE.end, PrisonLevel.Torch
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L207) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.fadeOut, INSTANCE.end, PrisonLevel.Torch
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L210) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.end, PrisonLevel.Torch
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L220) `public Group addVisuals() {` — 개별 처리, 인접 호출: PrisonLevel.Torch
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java#L228) `public void restoreFromBundle( Bundle bundle ) {` — 저장·복원

## 914. [`SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels`, 312행.

### 클래스/타입
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L63) `public class SewerLevel extends RegularLevel {`
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L246) `private static class Sink extends Emitter {`
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L288) `public static final class WaterParticle extends PixelParticle {`

### 변수·상수 후보
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L73) `public static final float[] SEWER_TRACK_CHANCES = new float[]{1f, 1f, 0.5f, 0.25f, 1f, 0.5f};`
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L248) `private int pos;`
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L249) `private float rippleDelay = 0;`

### 메서드 및 코드 의존 단서
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L75) `public void playLevelMusic(){` — 개별 처리, 인접 호출: Quest.active, INSTANCE.play, INSTANCE.playTracks, Random.chances
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L88) `protected int standardRooms(boolean forceMax) {` — 개별 처리, 인접 호출: Random.chances
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L95) `protected int specialRooms(boolean forceMax) {` — 개별 처리, 인접 호출: Random.chances
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L102) `protected Painter painter() {` — 개별 처리, 인접 호출: Quest.spawn
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L110) `public String tilesTex() {` — 개별 처리, 인접 호출: Quest.spawn, Game.runOnRenderThread, GameScene.show, Messages.get
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L115) `public String waterTex() {` — 개별 처리, 인접 호출: Quest.spawn, Game.runOnRenderThread, GameScene.show, Messages.get, Game.switchScene, Game.SceneChangeCallback
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L120) `protected Class<?>[] trapClasses() {` — 개별 처리, 인접 호출: Quest.spawn, Game.runOnRenderThread, GameScene.show, Messages.get, Game.switchScene, Game.SceneChangeCallback
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L130) `protected float[] trapChances() {` — 개별 처리, 인접 호출: Quest.spawn, Game.runOnRenderThread, GameScene.show, Messages.get, Game.switchScene, Game.SceneChangeCallback, Badges.validateHappyEnd
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L140) `protected void createMobs() {` — 생성·초기화, 인접 호출: Quest.spawn, Game.runOnRenderThread, GameScene.show, Messages.get, Game.switchScene, Game.SceneChangeCallback, Badges.validateHappyEnd
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L146) `public boolean activateTransition(Hero hero, LevelTransition transition) {` — 행동·상태 갱신, 인접 호출: Game.runOnRenderThread, GameScene.show, Messages.get, Game.switchScene, Game.SceneChangeCallback, Badges.validateHappyEnd, Dungeon.win
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L151) `public void call() {` — 개별 처리, 인접 호출: GameScene.show, Messages.get, Game.switchScene, Game.SceneChangeCallback, Badges.validateHappyEnd, Dungeon.win, Dungeon.deleteGame
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L160) `public void beforeCreate() {` — 개별 처리, 인접 호출: Badges.validateHappyEnd, Dungeon.win, Dungeon.deleteGame, Badges.saveGlobal, Splash.at
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L165) `public void afterCreate() {` — 개별 처리, 인접 호출: Badges.validateHappyEnd, Dungeon.win, Dungeon.deleteGame, Badges.saveGlobal, Splash.at
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L180) `public Group addVisuals() {` — 개별 처리, 인접 호출: Splash.at, Messages.get
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L187) `public void buildFlagMaps() {` — 생성·초기화, 인접 호출: Splash.at, Messages.get
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L197) `public void destroy(int pos) {` — 개별 처리, 인접 호출: Splash.at, Messages.get
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L210) `public static void addSewerVisuals(Level level, Group group ) {` — 개별 처리, 인접 호출: Messages.get
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L219) `public String tileName( int tile ) {` — 개별 처리, 인접 호출: Messages.get
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L232) `public String tileDesc(int tile) {` — 개별 처리, 인접 호출: Messages.get, DungeonTilemap.tileCenterToWorld
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L251) `private static final Emitter.Factory factory = new Factory() {` — 개별 처리, 인접 호출: DungeonTilemap.tileCenterToWorld, GameScene.ripple, Random.Float
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L254) `public void emit( Emitter emitter, int index, float x, float y ) {` — 개별 처리, 인접 호출: DungeonTilemap.tileCenterToWorld, GameScene.ripple, Random.Float, ColorMath.random
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L260) `public Sink( int pos ) {` — 개별 처리, 인접 호출: DungeonTilemap.tileCenterToWorld, GameScene.ripple, Random.Float, ColorMath.random
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L272) `public void update() {` — 행동·상태 갱신, 인접 호출: GameScene.ripple, Random.Float, ColorMath.random
- [L290](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L290) `public WaterParticle() {` — 개별 처리, 인접 호출: ColorMath.random, Random.Float
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L300) `public void reset( float x, float y ) {` — 개별 처리, 인접 호출: Random.Float

## 915. [`Terrain.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels`, 143행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L24) `public class Terrain {`

### 변수·상수 후보
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L26) `public static final int CHASM			= 0;`
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L27) `public static final int EMPTY			= 1;`
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L28) `public static final int GRASS			= 2;`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L29) `public static final int EMPTY_WELL		= 3;`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L30) `public static final int WALL			= 4;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L31) `public static final int DOOR			= 5;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L32) `public static final int OPEN_DOOR		= 6;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L33) `public static final int ENTRANCE		= 7;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L34) `public static final int ENTRANCE_SP		= 37;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L35) `public static final int EXIT			= 8;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L36) `public static final int EMBERS			= 9;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L37) `public static final int LOCKED_DOOR		= 10;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L39) `public static final int CRYSTAL_DOOR	= 31;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L40) `public static final int PEDESTAL		= 11;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L41) `public static final int WALL_DECO		= 12;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L42) `public static final int BARRICADE		= 13;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L43) `public static final int EMPTY_SP		= 14;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L44) `public static final int HIGH_GRASS		= 15;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L45) `public static final int FURROWED_GRASS	= 30;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L47) `public static final int SECRET_DOOR	    = 16;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L48) `public static final int SECRET_TRAP     = 17;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L49) `public static final int TRAP            = 18;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L50) `public static final int INACTIVE_TRAP   = 19;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L52) `public static final int EMPTY_DECO		= 20;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L53) `public static final int LOCKED_EXIT		= 21;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L54) `public static final int UNLOCKED_EXIT	= 22;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L55) `public static final int WELL			= 24;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L56) `public static final int BOOKSHELF		= 27;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L57) `public static final int ALCHEMY			= 28;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L63) `public static final int STATUE			= 25;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L64) `public static final int STATUE_SP		= 26;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L66) `public static final int REGION_DECO		= 33;`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L68) `public static final int MINE_CRYSTAL    = 35;`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L69) `public static final int MINE_BOULDER    = 36;`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L71) `public static final int WATER		    = 29;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L73) `public static final int PASSABLE		= 0x01;`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L74) `public static final int LOS_BLOCKING	= 0x02;`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L75) `public static final int FLAMABLE		= 0x04;`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L76) `public static final int SECRET			= 0x08;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L77) `public static final int SOLID			= 0x10;`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L78) `public static final int AVOID			= 0x20;`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L79) `public static final int LIQUID			= 0x40;`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L80) `public static final int PIT				= 0x80;`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L82) `public static final int[] flags = new int[256];`

### 메서드 및 코드 의존 단서
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L131) `public static int discover( int terr ) {` — 개별 처리

## 916. [`AlarmTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/AlarmTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 55행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/AlarmTrap.java#L33) `public class AlarmTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/AlarmTrap.java#L41) `public void activate() {` — 행동·상태 갱신, 인접 호출: GLog.w, Messages.get, CellEmitter.center, Speck.factory, INSTANCE.play

## 917. [`BlazingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/BlazingTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 65행.

### 클래스/타입
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/BlazingTrap.java#L38) `public class BlazingTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/BlazingTrap.java#L47) `public void activate() {` — 행동·상태 갱신, 인접 호출: PathFinder.buildDistanceMap, BArray.not, GameScene.add, Blob.seed, CellEmitter.get, Actor.findChar, Buff.prolong

## 918. [`BurningTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/BurningTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 59행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/BurningTrap.java#L37) `public class BurningTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/BurningTrap.java#L45) `public void activate() {` — 행동·상태 갱신, 인접 호출: GameScene.add, Blob.seed, CellEmitter.get, Actor.findChar, Buff.prolong, INSTANCE.play

## 919. [`ChillingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ChillingTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 60행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ChillingTrap.java#L36) `public class ChillingTrap extends Trap{`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ChillingTrap.java#L44) `public void activate() {` — 행동·상태 갱신, 인접 호출: Splash.at, INSTANCE.play, GameScene.add, Blob.seed, Actor.findChar, Buff.prolong

## 920. [`ConfusionTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ConfusionTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 55행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ConfusionTrap.java#L34) `public class ConfusionTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ConfusionTrap.java#L42) `public void activate() {` — 행동·상태 갱신, 인접 호출: GameScene.add, Blob.seed, INSTANCE.play, Actor.findChar, Buff.prolong

## 921. [`CorrosionTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/CorrosionTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 59행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/CorrosionTrap.java#L34) `public class CorrosionTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/CorrosionTrap.java#L42) `public void activate() {` — 행동·상태 갱신, 인접 호출: Blob.seed, INSTANCE.play, Actor.findChar, Buff.prolong, GameScene.add


# Java 구현 분석 742–759

소스 `bd3a990254e4249458816f4879e93ab87275555b` 직접 열람. 메서드 역할은 선언과 근처 본문에서 추론한 것으로 AST/런타임 검증은 아니다. 다중 행 선언과 익명 클래스는 누락·오분류될 수 있다.

## 742. [`ConnectionRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/ConnectionRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.connection` / 85행 / 타입 1 · 필드 후보 1 · 메서드 후보 6

### 선언 타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/ConnectionRoom.java#L31) `public abstract class ConnectionRoom extends Room {`

### 변수·상수 후보
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/ConnectionRoom.java#L60) `private static float[][] chances = new float[27][];`

### 메서드와 사용처 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/ConnectionRoom.java#L34) `public int minWidth() { return 3; }` — 구현 별도 확인 · 분기
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/ConnectionRoom.java#L35) `public int maxWidth() { return 10; }` — 구현 별도 확인 · 분기
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/ConnectionRoom.java#L38) `public int minHeight() { return 3; }` — 구현 별도 확인 · 분기 · 인접 호출 Reflection.newInstance, Random.chances
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/ConnectionRoom.java#L39) `public int maxHeight() { return 10; }` — 구현 별도 확인 · 분기 · 인접 호출 Reflection.newInstance, Random.chances
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/ConnectionRoom.java#L42) `public int minConnections(int direction) {` — 구현 별도 확인 · 분기 · 인접 호출 Reflection.newInstance, Random.chances
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/ConnectionRoom.java#L81) `public static ConnectionRoom createRoom(){` — 생성·초기화 · 인접 호출 Reflection.newInstance, Random.chances

## 743. [`MazeConnectionRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/MazeConnectionRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.connection` / 66행 / 타입 1 · 필드 후보 0 · 메서드 후보 2

### 선언 타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/MazeConnectionRoom.java#L29) `public class MazeConnectionRoom extends ConnectionRoom {`

### 변수·상수 후보
- 없음

### 메서드와 사용처 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/MazeConnectionRoom.java#L32) `public void paint(Level level) {` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Painter.fill, Maze.generate
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/MazeConnectionRoom.java#L62) `public int maxConnections(int direction) {` — 구현 별도 확인

## 744. [`PerimeterRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/PerimeterRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.connection` / 172행 / 타입 1 · 필드 후보 1 · 메서드 후보 5

### 선언 타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/PerimeterRoom.java#L32) `public class PerimeterRoom extends ConnectionRoom {`

### 변수·상수 후보
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/PerimeterRoom.java#L112) `private static Point[] corners;`

### 메서드와 사용처 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/PerimeterRoom.java#L34) `public void paint( Level level ) {` — 표시·지형 처리 · 분기 · 반복
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/PerimeterRoom.java#L45) `public static void fillPerimiterPaths( Level l, Room r, int floor ){` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Math.abs
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/PerimeterRoom.java#L88) `private static int spaceBetween(int a, int b){` — 구현 별도 확인 · 분기 · 인접 호출 Math.abs, Math.max, Math.min, Painter.fill
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/PerimeterRoom.java#L93) `private static int distanceBetweenPoints(Room r, Point a, Point b){` — 구현 별도 확인 · 분기 · 인접 호출 Math.max, Math.min, Painter.fill
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/PerimeterRoom.java#L115) `private static void fillBetweenPoints(Level level, Room r, Point from, Point to, int floor){` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Painter.fill, Math.min, Painter.drawLine

## 745. [`RingBridgeRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/RingBridgeRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.connection` / 59행 / 타입 1 · 필드 후보 0 · 메서드 후보 2

### 선언 타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/RingBridgeRoom.java#L31) `public class RingBridgeRoom extends RingTunnelRoom {`

### 변수·상수 후보
- 없음

### 메서드와 사용처 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/RingBridgeRoom.java#L34) `public void paint(Level level) {` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Painter.fill
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/RingBridgeRoom.java#L55) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {` — 조회·판정

## 746. [`RingTunnelRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/RingTunnelRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.connection` / 73행 / 타입 1 · 필드 후보 1 · 메서드 후보 4

### 선언 타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/RingTunnelRoom.java#L31) `public class RingTunnelRoom extends TunnelRoom {`

### 변수·상수 후보
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/RingTunnelRoom.java#L56) `private Rect connSpace;`

### 메서드와 사용처 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/RingTunnelRoom.java#L34) `public int minWidth() {` — 구현 별도 확인 · 분기 · 인접 호출 Math.max, Painter.fill, GameMath.gate
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/RingTunnelRoom.java#L39) `public int minHeight() {` — 구현 별도 확인 · 분기 · 인접 호출 Math.max, Painter.fill, GameMath.gate
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/RingTunnelRoom.java#L44) `public void paint(Level level) {` — 표시·지형 처리 · 분기 · 인접 호출 Painter.fill, GameMath.gate
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/RingTunnelRoom.java#L59) `protected Rect getConnectionSpace() {` — 조회·판정 · 분기 · 인접 호출 GameMath.gate

## 747. [`TunnelRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/TunnelRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.connection` / 124행 / 타입 1 · 필드 후보 0 · 메서드 후보 3

### 선언 타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/TunnelRoom.java#L34) `public class TunnelRoom extends ConnectionRoom {`

### 변수·상수 후보
- 없음

### 메서드와 사용처 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/TunnelRoom.java#L36) `public void paint(Level level) {` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Painter.drawLine
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/TunnelRoom.java#L100) `protected Rect getConnectionSpace(){` — 조회·판정 · 분기 · 반복 · 인접 호출 Random.Float, GameMath.gate
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/TunnelRoom.java#L107) `protected final Point getDoorCenter(){` — 조회·판정 · 분기 · 반복 · 인접 호출 Random.Float, GameMath.gate

## 748. [`WalkwayRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/WalkwayRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.connection` / 62행 / 타입 1 · 필드 후보 0 · 메서드 후보 2

### 선언 타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/WalkwayRoom.java#L31) `public class WalkwayRoom extends PerimeterRoom {`

### 변수·상수 후보
- 없음

### 메서드와 사용처 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/WalkwayRoom.java#L34) `public void paint(Level level) {` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Math.min, Painter.fill
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/WalkwayRoom.java#L58) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {` — 조회·판정

## 749. [`AmbitiousImpRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest` / 290행 / 타입 4 · 필드 후보 5 · 메서드 후보 22

### 선언 타입
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L43) `public class AmbitiousImpRoom extends SpecialRoom {`
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L145) `public static class QuestEntrance extends CustomTilemap {`
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L184) `public static class WallBanners extends CustomTilemap {`
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L247) `public static class EntranceBarrier extends CustomTilemap {`

### 변수·상수 후보
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L153) `final int TEX_WIDTH = 256;`
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L192) `private final int BANNER_1 = 80;`
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L193) `private final int BANNER_2 = 81;`
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L194) `private final int BANNER__BOTTOM = 82;`
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L254) `final int TEX_WIDTH = 256;`

### 메서드와 사용처 단서
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L46) `public int maxWidth() { return 9; }` — 구현 별도 확인 · 분기 · 인접 호출 Painter.fill, Painter.set, Random.IntRange, Painter.drawInside
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L47) `public int minWidth() { return 9; }` — 구현 별도 확인 · 분기 · 인접 호출 Painter.fill, Painter.set, Random.IntRange, Painter.drawInside
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L48) `public int maxHeight() { return 9; }` — 구현 별도 확인 · 분기 · 인접 호출 Painter.fill, Painter.set, Random.IntRange, Painter.drawInside
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L49) `public int minHeight() { return 9; }` — 구현 별도 확인 · 분기 · 인접 호출 Painter.fill, Painter.set, Random.IntRange, Painter.drawInside
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L52) `public void paint(Level level) {` — 표시·지형 처리 · 분기 · 인접 호출 Painter.fill, Painter.set, Random.IntRange, Painter.drawInside
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L121) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정 · 인접 호출 Point.distance, Messages.get
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L126) `public boolean canPlaceItem(Point p, Level l) {` — 조회·판정 · 인접 호출 Point.distance, Messages.get
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L131) `public boolean canPlaceTrap(Point p) {` — 조회·판정 · 분기 · 인접 호출 Point.distance, Messages.get
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L136) `public boolean canPlaceGrass(Point p) {` — 조회·판정 · 분기 · 인접 호출 Point.distance, Messages.get
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L141) `public boolean canPlaceWater(Point p) {` — 조회·판정 · 분기 · 인접 호출 Point.distance, Messages.get
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L156) `public Tilemap create() {` — 생성·초기화 · 분기 · 인접 호출 Messages.get
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L163) `public String name(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 Messages.get, Dungeon.level.width
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L168) `public String desc(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 Messages.get, Dungeon.level.width, Random.Int
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L173) `public Image image(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 Dungeon.level.width, Random.Int
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L197) `public void pos(int pos) {` — 구현 별도 확인 · 분기 · 인접 호출 Dungeon.level.width, Random.Int
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L202) `public Tilemap create() {` — 생성·초기화 · 분기 · 인접 호출 Dungeon.level.width, Random.Int
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L242) `public Image image(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 NoosaScript.get, Math.sin
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L257) `public Tilemap create() {` — 생성·초기화 · 분기 · 인접 호출 NoosaScript.get, Math.sin
- [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L262) `protected NoosaScript script() {` — 구현 별도 확인 · 인접 호출 NoosaScript.get, Math.sin
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L268) `public void update() {` — 상태·시간 갱신 · 인접 호출 Math.sin
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L274) `public synchronized void updateMapCell(int cell) {` — 상태·시간 갱신
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/AmbitiousImpRoom.java#L285) `public Image image(int tileX, int tileY) {` — 구현 별도 확인

## 750. [`BlacksmithRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest` / 291행 / 타입 4 · 필드 후보 0 · 메서드 후보 19

### 선언 타입
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L42) `public class BlacksmithRoom extends StandardRoom {`
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L185) `public static class QuestEntrance extends CustomTilemap {`
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L212) `public static class SmithyVisuals extends CustomTilemap {`
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L273) `public static class FurnaceOverhang extends CustomTilemap{`

### 변수·상수 후보
- 없음

### 메서드와 사용처 단서
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L45) `public int minWidth() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Math.max, Painter.fill, Painter.drawInside, Painter.set, Generator.random, Random.oneOf
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L50) `public int minHeight() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Math.max, Painter.fill, Painter.drawInside, Painter.set, Generator.random, Random.oneOf, Random.Int
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L54) `public void paint(Level level ) {` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Painter.fill, Painter.drawInside, Painter.set, Generator.random, Random.oneOf, Random.Int
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L127) `public boolean canConnect(Room r) {` — 조회·판정 · 분기
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L136) `public int maxConnections(int direction) {` — 구현 별도 확인 · 분기
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L146) `public boolean canConnect(Point p) {` — 조회·판정 · 분기
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L156) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L161) `public boolean canPlaceItem(Point p, Level l) {` — 조회·판정 · 인접 호출 Messages.get
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L166) `public boolean canPlaceGrass(Point p) {` — 조회·판정 · 인접 호출 Messages.get
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L171) `public boolean canPlaceTrap(Point p) {` — 조회·판정 · 인접 호출 Messages.get
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L176) `public boolean canPlaceWater(Point p) {` — 조회·판정 · 인접 호출 Messages.get
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L181) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {` — 조회·판정 · 분기 · 반복 · 인접 호출 Messages.get
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L194) `public Tilemap create() {` — 생성·초기화 · 분기 · 반복 · 인접 호출 Messages.get, Dungeon.level.width
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L201) `public String name(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Messages.get, Dungeon.level.width
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L206) `public String desc(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Messages.get, Dungeon.level.width
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L219) `public Tilemap create() {` — 생성·초기화 · 분기 · 반복 · 인접 호출 Dungeon.level.width, Messages.get
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L255) `public String name(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 Dungeon.level.width, Messages.get, Arrays.fill
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L264) `public String desc(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 Dungeon.level.width, Messages.get, Arrays.fill
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/BlacksmithRoom.java#L280) `public Tilemap create() {` — 생성·초기화 · 인접 호출 Arrays.fill

## 751. [`MassGraveRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest` / 269행 / 타입 4 · 필드 후보 2 · 메서드 후보 16

### 선언 타입
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L47) `public class MassGraveRoom extends SpecialRoom {`
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L163) `public static class Bones extends CustomTilemap {`
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L201) `public static class MassGraveDeco extends CustomTilemap {`
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L253) `public static class StatueRaised extends CustomTilemap {`

### 변수·상수 후보
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L165) `private static final int WALL_OVERLAP   = 3;`
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L166) `private static final int FLOOR          = 7;`

### 메서드와 사용처 단서
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L50) `public int minWidth() { return 11; }` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Painter.fill, Painter.set, Random.Int, Random.IntRange
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L51) `public int maxWidth() { return 11; }` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Painter.fill, Painter.set, Random.Int, Random.IntRange
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L52) `public int minHeight() { return 10; }` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Painter.fill, Painter.set, Random.Int, Random.IntRange
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L53) `public int maxHeight() { return 10; }` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Painter.fill, Painter.set, Random.Int, Random.IntRange
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L55) `public void paint(Level level){` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Painter.fill, Painter.set, Random.Int, Random.IntRange
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L127) `public boolean canConnect(int direction) {` — 조회·판정 · 분기 · 반복 · 인접 호출 Math.abs
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L132) `public boolean canConnect(Point p) {` — 조회·판정 · 분기 · 반복 · 인접 호출 Math.abs
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L137) `public boolean canConnect(Room r) {` — 조회·판정 · 분기 · 반복
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L173) `public Tilemap create() {` — 생성·초기화 · 분기 · 반복 · 인접 호출 Messages.get
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L185) `public Image image(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Messages.get
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L191) `public String name(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Messages.get
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L196) `public String desc(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Messages.get
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L223) `public Tilemap create() {` — 생성·초기화 · 분기 · 반복 · 인접 호출 Messages.get, Arrays.fill
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L234) `public String name(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 Messages.get, Arrays.fill
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L243) `public String desc(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 Messages.get, Arrays.fill
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MassGraveRoom.java#L260) `public Tilemap create() {` — 생성·초기화 · 인접 호출 Arrays.fill

## 752. [`MineEntrance.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest` / 194행 / 타입 2 · 필드 후보 1 · 메서드 후보 9

### 선언 타입
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java#L45) `public class MineEntrance extends CaveRoom {`
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java#L152) `public static class QuestExit extends CustomTilemap {`

### 변수·상수 후보
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java#L160) `final int TEX_WIDTH = 64;`

### 메서드와 사용처 단서
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java#L48) `public float[] sizeCatProbs() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Math.max, Painter.set
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java#L53) `public int minWidth() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Math.max, Painter.set
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java#L58) `public int minHeight() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Math.max, Painter.set
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java#L63) `public boolean isEntrance() {` — 조회·판정 · 분기 · 반복 · 인접 호출 Painter.set, Blacksmith.Quest.Type
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java#L68) `public void paint(Level level) {` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Painter.set, Blacksmith.Quest.Type
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java#L163) `public Tilemap create() {` — 생성·초기화 · 분기 · 인접 호출 Messages.get
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java#L170) `public String name(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 Messages.get
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java#L178) `public String desc(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 Messages.get
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineEntrance.java#L186) `public Image image(int tileX, int tileY) {` — 구현 별도 확인 · 분기

## 753. [`MineGiantRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineGiantRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest` / 150행 / 타입 1 · 필드 후보 0 · 메서드 후보 4

### 선언 타입
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineGiantRoom.java#L42) `public class MineGiantRoom extends CaveRoom {`

### 변수·상수 후보
- 없음

### 메서드와 사용처 단서
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineGiantRoom.java#L45) `public float[] sizeCatProbs() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.fillEllipse, Painter.set, Random.Int
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineGiantRoom.java#L50) `protected float fill() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.fillEllipse, Painter.set, Random.Int
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineGiantRoom.java#L55) `public int mobSpawnWeight() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.fillEllipse, Painter.set, Random.Int
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineGiantRoom.java#L62) `public void paint(Level level) {` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.fillEllipse, Painter.set, Random.Int

## 754. [`MineLargeRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineLargeRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest` / 227행 / 타입 1 · 필드 후보 0 · 메서드 후보 7

### 선언 타입
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineLargeRoom.java#L43) `public class MineLargeRoom extends CaveRoom {`

### 변수·상수 후보
- 없음

### 메서드와 사용처 단서
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineLargeRoom.java#L46) `public float[] sizeCatProbs() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.fillEllipse
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineLargeRoom.java#L51) `public int minHeight() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.fillEllipse
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineLargeRoom.java#L56) `public int minWidth() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.fillEllipse, Painter.set
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineLargeRoom.java#L61) `protected float fill() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.fillEllipse, Painter.set
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineLargeRoom.java#L66) `public int mobSpawnWeight() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.fillEllipse, Painter.set
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineLargeRoom.java#L73) `public void paint(Level level) {` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.fillEllipse, Painter.set, Random.Int
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineLargeRoom.java#L217) `private void findInternalCells(Level level, int cell, ArrayList<Integer> internalCells){` — 조회·판정 · 분기 · 반복

## 755. [`MineSecretRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineSecretRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest` / 74행 / 타입 1 · 필드 후보 0 · 메서드 후보 3

### 선언 타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineSecretRoom.java#L33) `public class MineSecretRoom extends SecretRoom {`

### 변수·상수 후보
- 없음

### 메서드와 사용처 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineSecretRoom.java#L36) `public int maxWidth() { return 7; }` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Painter.fill, Blacksmith.Quest.Type, Random.NormalIntRange, Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineSecretRoom.java#L39) `public int maxHeight() { return 7; }` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Painter.fill, Blacksmith.Quest.Type, Random.NormalIntRange, Painter.set
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineSecretRoom.java#L42) `public void paint(Level level) {` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Painter.fill, Blacksmith.Quest.Type, Random.NormalIntRange, Painter.set

## 756. [`MineSmallRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineSmallRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest` / 108행 / 타입 1 · 필드 후보 0 · 메서드 후보 5

### 선언 타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineSmallRoom.java#L37) `public class MineSmallRoom extends CaveRoom {`

### 변수·상수 후보
- 없음

### 메서드와 사용처 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineSmallRoom.java#L40) `public int minWidth() { return Math.max(6, super.minWidth()); }` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Math.max, Blacksmith.Quest.Type, Painter.set, Random.Int
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineSmallRoom.java#L43) `public int minHeight() { return Math.max(6, super.minHeight()); }` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.set, Random.Int
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineSmallRoom.java#L46) `public float[] sizeCatProbs() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.set, Random.Int
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineSmallRoom.java#L51) `protected float fill() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.set, Random.Int, Math.min, Point.distance, GameMath.gate, Random.Float
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/MineSmallRoom.java#L56) `public void paint(Level level) {` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Blacksmith.Quest.Type, Painter.set, Random.Int, Math.min, Point.distance, GameMath.gate, Random.Float

## 757. [`RitualSiteRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest` / 231행 / 타입 3 · 필드 후보 2 · 메서드 후보 14

### 선언 타입
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L40) `public class RitualSiteRoom extends StandardRoom {`
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L153) `public static class RitualMarker extends CustomTilemap {`
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L200) `public static class Table extends CustomTilemap {`

### 변수·상수 후보
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L161) `final int TEX_WIDTH = 256;`
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L209) `final int TEX_WIDTH = 256;`

### 메서드와 사용처 단서
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L43) `public int minWidth() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Math.max, Painter.fill, Arrays.fill, Random.Int, Painter.drawInside
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L48) `public int minHeight() {` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Math.max, Painter.fill, Arrays.fill, Random.Int, Painter.drawInside, Random.IntRange
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L52) `public void paint( Level level ) {` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Painter.fill, Arrays.fill, Random.Int, Painter.drawInside, Random.IntRange
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L135) `public boolean canPlaceItem(Point p, Level l) {` — 조회·판정 · 분기
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L140) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정 · 분기 · 인접 호출 Messages.get
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L145) `public boolean canConnect(Point p) {` — 조회·판정 · 분기 · 인접 호출 Messages.get
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L164) `public Tilemap create() {` — 생성·초기화 · 분기 · 인접 호출 Messages.get
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L171) `public Image image(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 Messages.get
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L179) `public String name(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 Messages.get
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L184) `public String desc(int tileX, int tileY) {` — 구현 별도 확인 · 분기 · 인접 호출 Messages.get
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L189) `public void restoreFromBundle(Bundle bundle) {` — 저장·복원 · 분기 · 인접 호출 Messages.get
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L212) `public Tilemap create() {` — 생성·초기화 · 인접 호출 Messages.get
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L219) `public String name(int tileX, int tileY) {` — 구현 별도 확인 · 인접 호출 Messages.get
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RitualSiteRoom.java#L224) `public String desc(int tileX, int tileY) {` — 구현 별도 확인 · 인접 호출 Messages.get

## 758. [`RotGardenRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RotGardenRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest` / 183행 / 타입 1 · 필드 후보 0 · 메서드 후보 5

### 선언 타입
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RotGardenRoom.java#L40) `public class RotGardenRoom extends SpecialRoom {`

### 변수·상수 후보
- 없음

### 메서드와 사용처 단서
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RotGardenRoom.java#L43) `public int minWidth() { return 10; }` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Painter.fill, Painter.set, Painter.drawInside, PathFinder.buildDistanceMap
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RotGardenRoom.java#L46) `public int minHeight() { return 10; }` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 Painter.fill, Painter.set, Painter.drawInside, PathFinder.buildDistanceMap
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RotGardenRoom.java#L48) `public void paint( Level level ) {` — 표시·지형 처리 · 분기 · 반복 · 인접 호출 Painter.fill, Painter.set, Painter.drawInside, PathFinder.buildDistanceMap
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RotGardenRoom.java#L139) `private static boolean validPlantPos(boolean[] passable, boolean[] newPassable, Level level, int pos, int heartPos, int entryPos){` — 구현 별도 확인 · 분기 · 반복 · 인접 호출 PathFinder.buildDistanceMap, System.arraycopy, Painter.set
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/RotGardenRoom.java#L176) `private static void placePlant(Level level, int pos, Mob plant){` — 구현 별도 확인 · 인접 호출 Painter.set

## 759. [`VaultBookcaseTreasureRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultBookcaseTreasureRoom.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault.treasure` / 101행 / 타입 1 · 필드 후보 0 · 메서드 후보 1

### 선언 타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultBookcaseTreasureRoom.java#L36) `public class VaultBookcaseTreasureRoom extends VaultTreasureRoom {`

### 변수·상수 후보
- 없음

### 메서드와 사용처 단서
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultBookcaseTreasureRoom.java#L39) `public void paint(Level level) {` — 표시·지형 처리 · 분기 · 인접 호출 Painter.fill, GameMath.gate, Painter.set


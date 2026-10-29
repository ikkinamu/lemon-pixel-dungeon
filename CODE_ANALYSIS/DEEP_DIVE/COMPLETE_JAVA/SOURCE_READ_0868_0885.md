# Java 소스 구현 분석 868–885

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 868. [`CircleWallEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 87행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallEntranceRoom.java#L33) `public class CircleWallEntranceRoom extends CircleWallRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallEntranceRoom.java#L36) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set, Random.Int
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallEntranceRoom.java#L41) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set, Random.Int
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallEntranceRoom.java#L46) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set, Random.Int
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallEntranceRoom.java#L51) `public boolean isEntrance() {` — 조회·판정, 인접 호출: Painter.set, Random.Int
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallEntranceRoom.java#L56) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set, Random.Int

## 869. [`CircleWallExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 93행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallExitRoom.java#L33) `public class CircleWallExitRoom extends CircleWallRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallExitRoom.java#L36) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set, Random.Int
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallExitRoom.java#L41) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set, Random.Int
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallExitRoom.java#L46) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set, Random.Int
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallExitRoom.java#L51) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set, Random.Int
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallExitRoom.java#L56) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set, Random.Int
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleWallExitRoom.java#L88) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 870. [`ExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 125행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ExitRoom.java#L37) `public class ExitRoom extends StandardRoom {`

### 변수·상수 후보
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ExitRoom.java#L101) `private static float[][] chances = new float[27][];`

### 메서드 및 코드 의존 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ExitRoom.java#L40) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ExitRoom.java#L45) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ExitRoom.java#L50) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.fill, Painter.set
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ExitRoom.java#L54) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.set
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ExitRoom.java#L69) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ExitRoom.java#L121) `public static StandardRoom createExit(){` — 생성·초기화, 인접 호출: Reflection.newInstance, Random.chances

## 871. [`HallwayExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/HallwayExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 59행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/HallwayExitRoom.java#L31) `public class HallwayExitRoom extends HallwayRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/HallwayExitRoom.java#L34) `public boolean isExit() {` — 조회·판정
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/HallwayExitRoom.java#L39) `public void paint(Level level) {` — 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/HallwayExitRoom.java#L54) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 872. [`LibraryHallExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryHallExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 62행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryHallExitRoom.java#L31) `public class LibraryHallExitRoom extends LibraryHallRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryHallExitRoom.java#L34) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryHallExitRoom.java#L39) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryHallExitRoom.java#L57) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 873. [`LibraryRingExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryRingExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 92행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryRingExitRoom.java#L33) `public class LibraryRingExitRoom extends LibraryRingRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryRingExitRoom.java#L36) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set, Random.Int
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryRingExitRoom.java#L41) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set, Random.Int
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryRingExitRoom.java#L46) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Painter.set, Random.Int
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryRingExitRoom.java#L51) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.fill, Painter.set, Random.Int
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryRingExitRoom.java#L56) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.set, Random.Int
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/LibraryRingExitRoom.java#L87) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 874. [`PillarsExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/PillarsExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 73행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/PillarsExitRoom.java#L32) `public class PillarsExitRoom extends PillarsRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/PillarsExitRoom.java#L35) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/PillarsExitRoom.java#L40) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/PillarsExitRoom.java#L45) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/PillarsExitRoom.java#L68) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 875. [`RegionDecoBridgeExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoBridgeExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 81행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoBridgeExitRoom.java#L32) `public class RegionDecoBridgeExitRoom extends RegionDecoBridgeRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoBridgeExitRoom.java#L35) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoBridgeExitRoom.java#L40) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoBridgeExitRoom.java#L45) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoBridgeExitRoom.java#L50) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoBridgeExitRoom.java#L76) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 876. [`RegionDecoLineExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoLineExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 34행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoLineExitRoom.java#L26) `public class RegionDecoLineExitRoom extends StatueLineExitRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoLineExitRoom.java#L29) `protected int decoTerrain() {` — 개별 처리

## 877. [`RegionDecoPatchExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoPatchExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 87행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoPatchExitRoom.java#L32) `public class RegionDecoPatchExitRoom extends RegionDecoPatchRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoPatchExitRoom.java#L35) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoPatchExitRoom.java#L40) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoPatchExitRoom.java#L45) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoPatchExitRoom.java#L50) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RegionDecoPatchExitRoom.java#L82) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 878. [`RingExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RingExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 59행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RingExitRoom.java#L31) `public class RingExitRoom extends RingRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RingExitRoom.java#L34) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RingExitRoom.java#L39) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RingExitRoom.java#L43) `protected int centerDecoTiles(){` — 개별 처리, 인접 호출: Painter.set
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RingExitRoom.java#L48) `protected void placeCenterDetail(Level level, int pos) {` — 개별 처리, 인접 호출: Painter.set
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RingExitRoom.java#L54) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 879. [`RitualExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RitualExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 54행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RitualExitRoom.java#L31) `public class RitualExitRoom extends RitualRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RitualExitRoom.java#L34) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RitualExitRoom.java#L39) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RitualExitRoom.java#L44) `protected void placeloot(Level level, Point p) {` — 개별 처리, 인접 호출: Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RitualExitRoom.java#L50) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 880. [`RuinsExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RuinsExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 92행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RuinsExitRoom.java#L32) `public class RuinsExitRoom extends RuinsRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RuinsExitRoom.java#L35) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RuinsExitRoom.java#L40) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RuinsExitRoom.java#L45) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RuinsExitRoom.java#L50) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RuinsExitRoom.java#L55) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/RuinsExitRoom.java#L87) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 881. [`StatueLineExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatueLineExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 68행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatueLineExitRoom.java#L31) `public class StatueLineExitRoom extends StatueLineRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatueLineExitRoom.java#L34) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatueLineExitRoom.java#L39) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatueLineExitRoom.java#L44) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatueLineExitRoom.java#L49) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatueLineExitRoom.java#L62) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 882. [`StatuesExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatuesExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 101행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatuesExitRoom.java#L33) `public class StatuesExitRoom extends StatuesRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatuesExitRoom.java#L36) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatuesExitRoom.java#L41) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatuesExitRoom.java#L46) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/StatuesExitRoom.java#L96) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 883. [`WaterBridgeExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/WaterBridgeExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 73행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/WaterBridgeExitRoom.java#L32) `public class WaterBridgeExitRoom extends WaterBridgeRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/WaterBridgeExitRoom.java#L35) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/WaterBridgeExitRoom.java#L40) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/WaterBridgeExitRoom.java#L45) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/WaterBridgeExitRoom.java#L50) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/WaterBridgeExitRoom.java#L68) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 884. [`FissureRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/FissureRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 83행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/FissureRoom.java#L30) `public class FissureRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/FissureRoom.java#L34) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set, Math.min, Math.sqrt, Random.Float
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/FissureRoom.java#L39) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set, Math.min, Math.sqrt, Random.Float
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/FissureRoom.java#L44) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set, Math.min, Math.sqrt, Random.Float
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/FissureRoom.java#L49) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.set, Math.min, Math.sqrt, Random.Float

## 885. [`GrassyGraveRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/GrassyGraveRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard`, 71행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/GrassyGraveRoom.java#L34) `public class GrassyGraveRoom extends StandardRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/GrassyGraveRoom.java#L37) `public void merge(Level l, Room other, Rect merge, int mergeTerrain) {` — 개별 처리, 인접 호출: Painter.fill, Math.max, Random.Int, Generator.random
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/GrassyGraveRoom.java#L47) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Math.max, Random.Int, Generator.random


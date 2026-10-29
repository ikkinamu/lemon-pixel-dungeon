# Java 소스 구현 분석 850–867

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 850. [`LibraryHallEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/LibraryHallEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance`, 57행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/LibraryHallEntranceRoom.java#L31) `public class LibraryHallEntranceRoom extends LibraryHallRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/LibraryHallEntranceRoom.java#L34) `public boolean isEntrance() {` — 조회·판정, 인접 호출: Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/LibraryHallEntranceRoom.java#L39) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set

## 851. [`LibraryRingEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/LibraryRingEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance`, 86행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/LibraryRingEntranceRoom.java#L33) `public class LibraryRingEntranceRoom extends LibraryRingRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/LibraryRingEntranceRoom.java#L36) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set, Random.Int
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/LibraryRingEntranceRoom.java#L41) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.fill, Painter.set, Random.Int
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/LibraryRingEntranceRoom.java#L46) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.fill, Painter.set, Random.Int
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/LibraryRingEntranceRoom.java#L51) `public boolean isEntrance() {` — 조회·판정, 인접 호출: Painter.fill, Painter.set, Random.Int
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/LibraryRingEntranceRoom.java#L56) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.fill, Painter.set, Random.Int

## 852. [`PillarsEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/PillarsEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance`, 66행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/PillarsEntranceRoom.java#L31) `public class PillarsEntranceRoom extends PillarsRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/PillarsEntranceRoom.java#L34) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/PillarsEntranceRoom.java#L39) `public boolean isEntrance() {` — 조회·판정, 인접 호출: Painter.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/PillarsEntranceRoom.java#L44) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set

## 853. [`RegionDecoBridgeEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoBridgeEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance`, 75행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoBridgeEntranceRoom.java#L31) `public class RegionDecoBridgeEntranceRoom extends RegionDecoBridgeRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoBridgeEntranceRoom.java#L34) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoBridgeEntranceRoom.java#L39) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoBridgeEntranceRoom.java#L44) `public boolean isEntrance() {` — 조회·판정, 인접 호출: Painter.set
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoBridgeEntranceRoom.java#L49) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set

## 854. [`RegionDecoLineEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoLineEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance`, 34행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoLineEntranceRoom.java#L26) `public class RegionDecoLineEntranceRoom extends StatueLineEntranceRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoLineEntranceRoom.java#L29) `protected int decoTerrain() {` — 개별 처리

## 855. [`RegionDecoPatchEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoPatchEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance`, 109행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoPatchEntranceRoom.java#L34) `public class RegionDecoPatchEntranceRoom extends RegionDecoPatchRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoPatchEntranceRoom.java#L37) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoPatchEntranceRoom.java#L42) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoPatchEntranceRoom.java#L47) `public boolean isEntrance() {` — 조회·판정
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoPatchEntranceRoom.java#L52) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {` — 조회·판정, 인접 호출: Painter.set
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoPatchEntranceRoom.java#L61) `public boolean canPlaceTrap(Point p) {` — 조회·판정, 인접 호출: Painter.set, EntranceRoom.placeEarlyGuidePages
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RegionDecoPatchEntranceRoom.java#L70) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set, EntranceRoom.placeEarlyGuidePages

## 856. [`RingEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RingEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance`, 53행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RingEntranceRoom.java#L30) `public class RingEntranceRoom extends RingRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RingEntranceRoom.java#L33) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RingEntranceRoom.java#L38) `public boolean isEntrance() {` — 조회·판정, 인접 호출: Painter.set
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RingEntranceRoom.java#L42) `protected int centerDecoTiles(){` — 개별 처리, 인접 호출: Painter.set
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RingEntranceRoom.java#L47) `protected void placeCenterDetail(Level level, int pos) {` — 개별 처리, 인접 호출: Painter.set

## 857. [`RitualEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RitualEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance`, 49행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RitualEntranceRoom.java#L31) `public class RitualEntranceRoom extends RitualRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RitualEntranceRoom.java#L34) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RitualEntranceRoom.java#L39) `public boolean isEntrance() {` — 조회·판정, 인접 호출: Painter.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RitualEntranceRoom.java#L44) `protected void placeloot(Level level, Point p) {` — 개별 처리, 인접 호출: Painter.set

## 858. [`RuinsEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RuinsEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance`, 85행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RuinsEntranceRoom.java#L31) `public class RuinsEntranceRoom extends RuinsRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RuinsEntranceRoom.java#L34) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RuinsEntranceRoom.java#L39) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RuinsEntranceRoom.java#L44) `public boolean isEntrance() {` — 조회·판정, 인접 호출: Painter.set
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RuinsEntranceRoom.java#L49) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/RuinsEntranceRoom.java#L54) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set

## 859. [`StatueLineEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/StatueLineEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance`, 61행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/StatueLineEntranceRoom.java#L30) `public class StatueLineEntranceRoom extends StatueLineRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/StatueLineEntranceRoom.java#L33) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/StatueLineEntranceRoom.java#L38) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/StatueLineEntranceRoom.java#L43) `public boolean isEntrance() {` — 조회·판정, 인접 호출: Painter.set
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/StatueLineEntranceRoom.java#L48) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set

## 860. [`StatuesEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/StatuesEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance`, 95행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/StatuesEntranceRoom.java#L33) `public class StatuesEntranceRoom extends StatuesRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/StatuesEntranceRoom.java#L36) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/StatuesEntranceRoom.java#L41) `public boolean isEntrance() {` — 조회·판정, 인접 호출: Painter.set
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/StatuesEntranceRoom.java#L46) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set

## 861. [`WaterBridgeEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/WaterBridgeEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.entrance`, 94행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/WaterBridgeEntranceRoom.java#L34) `public class WaterBridgeEntranceRoom extends WaterBridgeRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/WaterBridgeEntranceRoom.java#L37) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/WaterBridgeEntranceRoom.java#L42) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/WaterBridgeEntranceRoom.java#L47) `public boolean isEntrance() {` — 조회·판정, 인접 호출: Painter.set, EntranceRoom.placeEarlyGuidePages
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/WaterBridgeEntranceRoom.java#L52) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {` — 조회·판정, 인접 호출: Painter.set, EntranceRoom.placeEarlyGuidePages
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/WaterBridgeEntranceRoom.java#L61) `public boolean canPlaceTrap(Point p) {` — 조회·판정, 인접 호출: Painter.set, EntranceRoom.placeEarlyGuidePages
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/WaterBridgeEntranceRoom.java#L70) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set, EntranceRoom.placeEarlyGuidePages

## 862. [`CaveExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CaveExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 92행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CaveExitRoom.java#L32) `public class CaveExitRoom extends CaveRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CaveExitRoom.java#L35) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CaveExitRoom.java#L40) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CaveExitRoom.java#L45) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CaveExitRoom.java#L50) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CaveExitRoom.java#L55) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CaveExitRoom.java#L87) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 863. [`CavesFissureExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CavesFissureExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 74행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CavesFissureExitRoom.java#L32) `public class CavesFissureExitRoom extends CavesFissureRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CavesFissureExitRoom.java#L35) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CavesFissureExitRoom.java#L40) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CavesFissureExitRoom.java#L45) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CavesFissureExitRoom.java#L69) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 864. [`CellBlockExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CellBlockExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 77행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CellBlockExitRoom.java#L32) `public class CellBlockExitRoom extends CellBlockRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CellBlockExitRoom.java#L35) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CellBlockExitRoom.java#L40) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CellBlockExitRoom.java#L45) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CellBlockExitRoom.java#L72) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 865. [`ChasmBridgeExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmBridgeExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 73행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmBridgeExitRoom.java#L32) `public class ChasmBridgeExitRoom extends ChasmBridgeRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmBridgeExitRoom.java#L35) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmBridgeExitRoom.java#L40) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmBridgeExitRoom.java#L45) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmBridgeExitRoom.java#L50) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmBridgeExitRoom.java#L68) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 866. [`ChasmExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 92행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmExitRoom.java#L32) `public class ChasmExitRoom extends ChasmRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmExitRoom.java#L35) `public int minHeight() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmExitRoom.java#L40) `public int minWidth() {` — 개별 처리, 인접 호출: Math.max, Painter.set
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmExitRoom.java#L45) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmExitRoom.java#L50) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmExitRoom.java#L55) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ChasmExitRoom.java#L87) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정

## 867. [`CircleBasinExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleBasinExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard.exit`, 59행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleBasinExitRoom.java#L31) `public class CircleBasinExitRoom extends CircleBasinRoom {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleBasinExitRoom.java#L34) `public float[] sizeCatProbs() {` — 개별 처리, 인접 호출: Painter.set
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleBasinExitRoom.java#L39) `public boolean isExit() {` — 조회·판정, 인접 호출: Painter.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleBasinExitRoom.java#L44) `public void paint(Level level) {` — 개별 처리, 인접 호출: Painter.set
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/CircleBasinExitRoom.java#L54) `public boolean canPlaceCharacter(Point p, Level l) {` — 조회·판정


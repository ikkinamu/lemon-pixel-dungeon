# 실제 Java 소스 정적 분석 814–831

기준 `bd3a990254e4249458816f4879e93ab87275555b`. 모든 항목의 원문을 불러와 타입·상태 변수·메서드와 호출 표현을 조사한다. 기능명은 **정적 의미 추론**이며 AST/런타임 검증이 아니다. 다중행·익명 구조 누락 가능.

## 814. [`LaboratoryRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/LaboratoryRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 138행

### 타입
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/LaboratoryRoom.java#L44) `public class LaboratoryRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/LaboratoryRoom.java#L46) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Painter.set, Blob.seed, Random.NormalIntRange, ALCHEMY_GUIDE.pageNames, ALCHEMY_GUIDE.isPageFound
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/LaboratoryRoom.java#L125) `private static Item prize( Level level ) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Generator.random, Random.oneOf

## 815. [`LibraryRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/LibraryRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 81행

### 타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/LibraryRoom.java#L37) `public class LibraryRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/LibraryRoom.java#L39) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.drawInside, Random.NormalIntRange, Random.Int, Generator.random
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/LibraryRoom.java#L68) `private static Item prize( Level level ) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Generator.random

## 816. [`MagicalFireRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 290행

### 타입
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L50) `public class MagicalFireRoom extends SpecialRoom {`
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L156) `public static class EternalFire extends Blob {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L53) `public int minWidth() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Blob.seed, Painter.set, Random.Int, Random.IntRange
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L54) `public int minHeight() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Blob.seed, Painter.set, Random.Int, Random.IntRange
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L57) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Blob.seed, Painter.set, Random.Int, Random.IntRange
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L116) `private static Item prize( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.Int, Generator.random, Random.oneOf
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L133) `public boolean canPlaceGrass(Point p) {`: 조회·조건, 조건문, 반복문
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L138) `public boolean canPlaceCharacter(Point p, Level l) {`: 조회·조건, 조건문, 반복문
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L159) `protected void evolve() {`: 행동·상태 갱신, 조건문, 반복문
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L242) `public void seed(Level level, int cell, int amount) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Messages.get
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L248) `public void clear(int cell) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Messages.get
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L255) `public void fullyClear() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Messages.get
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L261) `public void use( BlobEmitter emitter ) {`: 이벤트·효과, 조건문, 반복문; 인접 호출 Messages.get
- [L267](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L267) `public String tileDesc() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Messages.get
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L272) `public void onBuildFlagMaps( Level l ) {`: 이벤트·효과, 조건문, 반복문
- [L281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java#L281) `public void onUpdateCellFlags(Level l, int cell) {`: 이벤트·효과, 조건문

## 817. [`MagicWellRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicWellRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 63행

### 타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicWellRoom.java#L35) `public class MagicWellRoom extends SpecialRoom {`

### 필드·상수
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicWellRoom.java#L40) `public Class<?extends WellWater> overrideWater = null;`

### 메서드와 연관 호출
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicWellRoom.java#L42) `public void paint( Level level ) {`: 개별 처리(본문 확인); 인접 호출 Painter.fill, Painter.set, Random.element, WellWater.seed

## 818. [`PitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 118행

### 타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PitRoom.java#L36) `public class PitRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PitRoom.java#L39) `public int minWidth() { return 6; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Painter.set, Generator.random, Random.oneOf, Challenges.isItemBlocked
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PitRoom.java#L40) `public int minHeight() { return 6; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Painter.set, Generator.random, Random.oneOf, Challenges.isItemBlocked, Random.IntRange
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PitRoom.java#L43) `public int maxWidth() { return 9; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Painter.set, Generator.random, Random.oneOf, Challenges.isItemBlocked, Random.IntRange
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PitRoom.java#L44) `public int maxHeight() { return 9; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Painter.set, Generator.random, Random.oneOf, Challenges.isItemBlocked, Random.IntRange
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PitRoom.java#L46) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Painter.set, Generator.random, Random.oneOf, Challenges.isItemBlocked, Random.IntRange
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PitRoom.java#L97) `private static Item prize( Level level ) {`: 개별 처리(본문 확인); 인접 호출 Generator.random, Random.oneOf
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PitRoom.java#L107) `public boolean canPlaceTrap(Point p) {`: 조회·조건
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PitRoom.java#L114) `public boolean canPlaceGrass(Point p) {`: 조회·조건

## 819. [`PoolRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PoolRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 145행

### 타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PoolRoom.java#L37) `public class PoolRoom extends SpecialRoom {`

### 필드·상수
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PoolRoom.java#L39) `private static final int NPIRANHAS	= 3;`

### 메서드와 연관 호출
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PoolRoom.java#L42) `public int minWidth() {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.set
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PoolRoom.java#L47) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Piranha.random
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PoolRoom.java#L51) `public void paint(Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Piranha.random
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PoolRoom.java#L102) `private static Item prize( Level level ) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Random.Int, Generator.randomWeapon, Generator.randomMissile, Generator.randomArmor

## 820. [`RunestoneRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/RunestoneRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 80행

### 타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/RunestoneRoom.java#L35) `public class RunestoneRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/RunestoneRoom.java#L38) `public int minWidth() { return 6; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.drawInside, Random.NormalIntRange, Generator.random
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/RunestoneRoom.java#L41) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.drawInside, Random.NormalIntRange, Generator.random
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/RunestoneRoom.java#L46) `public void paint( Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.drawInside, Random.NormalIntRange, Generator.random
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/RunestoneRoom.java#L67) `private static Item prize( Level level ) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Generator.random

## 821. [`SacrificeRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SacrificeRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 110행

### 타입
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SacrificeRoom.java#L38) `public class SacrificeRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SacrificeRoom.java#L41) `public int minWidth() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Painter.drawInside, Math.abs, Painter.set, Blob.seed, Generator.randomWeapon, Challenges.isItemBlocked
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SacrificeRoom.java#L42) `public int minHeight() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Painter.drawInside, Math.abs, Painter.set, Blob.seed, Generator.randomWeapon, Challenges.isItemBlocked
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SacrificeRoom.java#L45) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Painter.drawInside, Math.abs, Painter.set, Blob.seed, Generator.randomWeapon, Challenges.isItemBlocked
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SacrificeRoom.java#L84) `public static Item prize( Level level ) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Generator.randomWeapon, Challenges.isItemBlocked, Enchantment.randomCurse

## 822. [`SentryRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 364행

### 타입
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L50) `public class SentryRoom extends SpecialRoom {`
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L224) `public static class Sentry extends NPC {`

### 필드·상수
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L232) `private float initialChargeDelay;`
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L233) `private float curChargeDelay;`
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L235) `private EmptyRoom room;`
- [L342](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L342) `private static final String INITIAL_DELAY = "initial_delay";`
- [L343](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L343) `private static final String CUR_DELAY = "cur_delay";`
- [L344](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L344) `private static final String ROOM = "room";`

### 메서드와 연관 호출
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L53) `public int minWidth() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L54) `public int minHeight() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L57) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L166) `private static Item prize(Level level ) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Random.Int, Generator.randomWeapon, Generator.randomMissile, Generator.randomArmor
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L210) `public boolean canConnect(Point p) {`: 조회·조건, 조건문; 인접 호출 Bestiary.setSeen
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L238) `protected boolean act() {`: 행동·상태 갱신, 조건문; 인접 호출 Bestiary.setSeen
- [L290](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L290) `public void onZapComplete(){`: 이벤트·효과, 조건문; 인접 호출 Random.NormalIntRange, Eye.DeathGaze, Badges.validateDeathFromEnemyMagic, Dungeon.fail, GLog.n, Messages.capitalize, Messages.get
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L304) `public CharSprite sprite() {`: 개별 처리(본문 확인), 조건문
- [L313](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L313) `public int attackSkill(Char target) {`: 전투 관련
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L318) `public int defenseSkill( Char enemy ) {`: 전투 관련
- [L323](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L323) `public void damage( int dmg, Object src ) {`: 전투 관련
- [L328](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L328) `public boolean add( Buff buff ) {`: 개별 처리(본문 확인)
- [L333](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L333) `public boolean reset() {`: 개별 처리(본문 확인)
- [L338](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L338) `public boolean interact(Char c) {`: 개별 처리(본문 확인)
- [L347](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L347) `public void storeInBundle(Bundle bundle) {`: 저장·복원
- [L355](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SentryRoom.java#L355) `public void restoreFromBundle(Bundle bundle) {`: 저장·복원

## 823. [`ShopRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 406행

### 타입
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java#L67) `public class ShopRoom extends SpecialRoom {`

### 필드·상수
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java#L69) `protected ArrayList<Item> itemsToSpawn;`

### 메서드와 연관 호출
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java#L72) `public int minWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Math.sqrt, Painter.fill
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java#L77) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Math.sqrt, Painter.fill
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java#L81) `public int spacesNeeded(){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java#L100) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java#L115) `protected void placeShopkeeper( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java#L125) `protected void placeItems( Level level ){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.min
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java#L222) `protected static ArrayList<Item> generateItems() {`: 개별 처리(본문 확인); 인접 호출 Generator.random, TippedDart.randomTipped, Random.IntRange
- [L361](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java#L361) `protected static Bag ChooseBag(Belongings pack){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 VELVET_POUCH.dropped, SCROLL_HOLDER.dropped, POTION_BANDOLIER.dropped, MAGICAL_HOLSTER.dropped, VELVET_POUCH.drop, SCROLL_HOLDER.drop, POTION_BANDOLIER.drop, MAGICAL_HOLSTER.drop

## 824. [`SpecialRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 213행

### 타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L34) `public abstract class SpecialRoom extends Room {`

### 필드·상수
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L51) `private Door entrance;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L64) `private static final String ENTRANCE = "entrance";`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L109) `private static int pitNeededDepth = -1;`
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L192) `private static final String ROOMS	= "special_rooms";`
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L193) `private static final String PIT	    = "pit_needed";`

### 메서드와 연관 호출
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L37) `public int minWidth() { return 5; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Arrays.asList
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L38) `public int maxWidth() { return 10; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Arrays.asList
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L41) `public int minHeight() {`: 개별 처리(본문 확인), 조건문; 인접 호출 Arrays.asList
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L44) `public int maxHeight() { return 10; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Arrays.asList
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L47) `public int maxConnections(int direction) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Arrays.asList
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L53) `public Door entrance() {`: 개별 처리(본문 확인), 조건문; 인접 호출 Arrays.asList
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L67) `public void storeInBundle(Bundle bundle) {`: 저장·복원, 조건문; 인접 호출 Arrays.asList, EQUIP_SPECIALS.clone, CONSUMABLE_SPECIALS.clone
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L75) `public void restoreFromBundle(Bundle bundle) {`: 저장·복원, 조건문, 반복문; 인접 호출 Arrays.asList, EQUIP_SPECIALS.clone, CONSUMABLE_SPECIALS.clone, Random.shuffle
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L111) `public static void initForRun() {`: 생성·초기화, 조건문, 반복문; 인접 호출 EQUIP_SPECIALS.clone, CONSUMABLE_SPECIALS.clone, Random.shuffle, Dungeon.labRoomNeeded, CRYSTAL_KEY_SPECIALS.contains, POTION_SPAWN_ROOMS.contains
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L131) `public static void initForFloor(){`: 생성·초기화, 조건문, 반복문; 인접 호출 Dungeon.labRoomNeeded, CRYSTAL_KEY_SPECIALS.contains, POTION_SPAWN_ROOMS.contains, Dungeon.bossLevel, Random.chances, Reflection.newInstance
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L141) `private static void useType( Class<?extends Room> type ) {`: 이벤트·효과, 조건문, 반복문; 인접 호출 CRYSTAL_KEY_SPECIALS.contains, POTION_SPAWN_ROOMS.contains, Dungeon.bossLevel, Random.chances, Reflection.newInstance
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L154) `public static void resetPitRoom(int depth){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Dungeon.bossLevel, Random.chances, Reflection.newInstance, ShatteredPixelDungeon.reportException
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L158) `public static SpecialRoom createRoom(){`: 생성·초기화, 조건문, 반복문; 인접 호출 Dungeon.bossLevel, Random.chances, Reflection.newInstance, ShatteredPixelDungeon.reportException
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L195) `public static void restoreRoomsFromBundle( Bundle bundle ) {`: 저장·복원, 조건문, 반복문; 인접 호출 ShatteredPixelDungeon.reportException
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java#L208) `public static void storeRoomsInBundle( Bundle bundle ) {`: 저장·복원

## 825. [`StatueRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/StatueRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 75행

### 타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/StatueRoom.java#L32) `public class StatueRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/StatueRoom.java#L34) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Statue.random

## 826. [`StorageRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/StorageRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 76행

### 타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/StorageRoom.java#L33) `public class StorageRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/StorageRoom.java#L35) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Random.IntRange, Generator.random, Random.oneOf
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/StorageRoom.java#L60) `private static Item prize( Level level ) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Random.Int, Generator.random, Random.oneOf

## 827. [`ToxicGasRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ToxicGasRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 179행

### 타입
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ToxicGasRoom.java#L42) `public class ToxicGasRoom extends SpecialRoom {`
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ToxicGasRoom.java#L127) `public static class ToxicGasSeed extends Blob {`
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ToxicGasRoom.java#L157) `public static class ToxicVent extends Trap {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ToxicGasRoom.java#L45) `public int minWidth() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Blob.seed, Math.min
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ToxicGasRoom.java#L46) `public int minHeight() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Blob.seed, Math.min
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ToxicGasRoom.java#L49) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Blob.seed, Math.min
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ToxicGasRoom.java#L114) `public boolean canPlaceCharacter(Point p, Level l) {`: 조회·조건, 조건문, 반복문; 인접 호출 GameScene.add, Blob.seed
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ToxicGasRoom.java#L123) `public boolean canPlaceTrap(Point p) {`: 조회·조건, 조건문, 반복문; 인접 호출 GameScene.add, Blob.seed, Messages.get
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ToxicGasRoom.java#L130) `protected void evolve() {`: 행동·상태 갱신, 조건문, 반복문; 인접 호출 GameScene.add, Blob.seed, Messages.get
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ToxicGasRoom.java#L168) `public String desc() {`: 개별 처리(본문 확인); 인접 호출 Messages.get
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ToxicGasRoom.java#L173) `public void activate() {`: 행동·상태 갱신

## 828. [`TrapsRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/TrapsRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 173행

### 타입
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/TrapsRoom.java#L48) `public class TrapsRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/TrapsRoom.java#L52) `public int minWidth() { return 6; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Random.Int, Random.oneOf
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/TrapsRoom.java#L53) `public int maxWidth() { return 8; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Random.Int, Random.oneOf
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/TrapsRoom.java#L56) `public int minHeight() { return 6; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Random.oneOf
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/TrapsRoom.java#L57) `public int maxHeight() { return 8; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Random.oneOf
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/TrapsRoom.java#L59) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Random.oneOf, Reflection.newInstance
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/TrapsRoom.java#L125) `private static Item prize( Level level ) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Random.Int, Generator.randomWeapon, Generator.randomArmor

## 829. [`TreasuryRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/TreasuryRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 79행

### 타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/TreasuryRoom.java#L37) `public class TreasuryRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/TreasuryRoom.java#L39) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Random.Int, Random.IntRange, MimicTooth.mimicChanceMultiplier, Random.Float, Mimic.spawnAt

## 830. [`WeakFloorRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/WeakFloorRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 130행

### 타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/WeakFloorRoom.java#L37) `public class WeakFloorRoom extends SpecialRoom {`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/WeakFloorRoom.java#L79) `public static class HiddenWell extends CustomTilemap {`
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/WeakFloorRoom.java#L106) `public static class WellID extends Blob {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/WeakFloorRoom.java#L39) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.drawInside, Random.IntRange, Random.Int, Painter.set, Blob.seed
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/WeakFloorRoom.java#L87) `public Tilemap create() {`: 생성·초기화, 조건문, 반복문; 인접 호출 Messages.get
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/WeakFloorRoom.java#L94) `public String name(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Messages.get
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/WeakFloorRoom.java#L99) `public String desc(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Messages.get
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/WeakFloorRoom.java#L109) `public Notes.Landmark landmark() {`: 개별 처리(본문 확인), 조건문, 반복문
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/WeakFloorRoom.java#L114) `protected void evolve() {`: 행동·상태 갱신, 조건문, 반복문

## 831. [`AquariumRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/AquariumRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.standard` / 81행

### 타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/AquariumRoom.java#L30) `public class AquariumRoom extends StandardRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/AquariumRoom.java#L33) `public int minWidth() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Math.max, Painter.fill, Math.min, Piranha.random
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/AquariumRoom.java#L38) `public int minHeight() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Math.max, Painter.fill, Math.min, Piranha.random
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/AquariumRoom.java#L43) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill, Math.min, Piranha.random
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/AquariumRoom.java#L48) `public boolean canPlaceItem(Point p, Level l) {`: 조회·조건, 반복문; 인접 호출 Painter.fill, Math.min, Piranha.random
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/AquariumRoom.java#L53) `public boolean canPlaceCharacter(Point p, Level l) {`: 조회·조건, 반복문; 인접 호출 Painter.fill, Math.min, Piranha.random
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/AquariumRoom.java#L58) `public void paint(Level level) {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill, Math.min, Piranha.random


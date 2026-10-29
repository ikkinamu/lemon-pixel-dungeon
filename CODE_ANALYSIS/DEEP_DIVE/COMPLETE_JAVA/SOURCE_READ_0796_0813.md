# 실제 Java 소스 정적 분석 796–813

기준 `bd3a990254e4249458816f4879e93ab87275555b`. 모든 항목의 원문을 불러와 타입·상태 변수·메서드와 호출 표현을 조사한다. 기능명은 **정적 의미 추론**이며 AST/런타임 검증이 아니다. 다중행·익명 구조 누락 가능.

## 796. [`SecretRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 125행

### 타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java#L34) `public abstract class SecretRoom extends SpecialRoom {`

### 필드·상수
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java#L47) `private static float[] baseRegionSecrets = new float[]{2f, 2.25f, 2.5f, 2.75f, 3.0f};`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java#L48) `private static int[] regionSecretsThisRun = new int[5];`
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java#L103) `private static final String ROOMS	= "secret_rooms";`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java#L104) `private static final String REGIONS	= "region_secrets";`

### 메서드와 연관 호출
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java#L50) `public static void initForRun(){`: 생성·초기화, 조건문, 반복문; 인접 호출 Random.Float, Random.shuffle, Math.ceil, Math.floor, Random.chances, Reflection.newInstance
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java#L66) `public static int secretsForFloor(int depth){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.Float, Math.ceil, Math.floor, Random.chances, Reflection.newInstance, ShatteredPixelDungeon.reportException
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java#L90) `public static SecretRoom createRoom(){`: 생성·초기화, 조건문, 반복문; 인접 호출 Random.chances, Reflection.newInstance, ShatteredPixelDungeon.reportException
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java#L106) `public static void restoreRoomsFromBundle( Bundle bundle ) {`: 저장·복원, 조건문, 반복문; 인접 호출 ShatteredPixelDungeon.reportException
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java#L119) `public static void storeRoomsInBundle( Bundle bundle ) {`: 저장·복원

## 797. [`SecretRunestoneRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRunestoneRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 101행

### 타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRunestoneRoom.java#L32) `public class SecretRunestoneRoom extends SecretRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRunestoneRoom.java#L35) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.drawLine, Generator.randomUsingDefaults
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRunestoneRoom.java#L87) `public boolean canPlaceWater(Point p) {`: 조회·조건
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRunestoneRoom.java#L92) `public boolean canPlaceGrass(Point p) {`: 조회·조건
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRunestoneRoom.java#L97) `public boolean canPlaceCharacter(Point p, Level l) {`: 조회·조건

## 798. [`SecretSummoningRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretSummoningRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 75행

### 타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretSummoningRoom.java#L33) `public class SecretSummoningRoom extends SecretRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretSummoningRoom.java#L38) `public int maxWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Generator.random, TrapMechanism.revealHiddenTrapChance, Painter.set
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretSummoningRoom.java#L43) `public int maxHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Generator.random, TrapMechanism.revealHiddenTrapChance, Painter.set
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretSummoningRoom.java#L48) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Generator.random, TrapMechanism.revealHiddenTrapChance, Painter.set

## 799. [`SecretWellRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretWellRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 72행

### 타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretWellRoom.java#L33) `public class SecretWellRoom extends SecretRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretWellRoom.java#L39) `public boolean canConnect(Point p) {`: 조회·조건, 조건문; 인접 호출 Painter.fill, Painter.drawLine, Painter.set, Random.element, WellWater.seed
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretWellRoom.java#L44) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.drawLine, Painter.set, Random.element, WellWater.seed

## 800. [`DiamondGooRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/DiamondGooRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.sewerboss` / 74행

### 타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/DiamondGooRoom.java#L30) `public class DiamondGooRoom extends GooBossRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/DiamondGooRoom.java#L33) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillDiamond, Painter.set
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/DiamondGooRoom.java#L70) `public boolean canPlaceWater(Point p) {`: 조회·조건

## 801. [`GooBossRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/GooBossRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.sewerboss` / 126행

### 타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/GooBossRoom.java#L34) `public abstract class GooBossRoom extends StandardRoom {`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/GooBossRoom.java#L66) `public static class GooNest extends CustomTilemap {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/GooBossRoom.java#L37) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.Int
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/GooBossRoom.java#L42) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {`: 조회·조건, 조건문, 반복문; 인접 호출 Random.Int
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/GooBossRoom.java#L46) `public static GooBossRoom randomGooRoom(){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.Int
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/GooBossRoom.java#L59) `protected void setupGooNest( Level level ){`: 생성·초기화, 조건문, 반복문
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/GooBossRoom.java#L73) `public Tilemap create() {`: 생성·초기화, 조건문, 반복문
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/GooBossRoom.java#L121) `public Image image(int tileX, int tileY) {`: 개별 처리(본문 확인)

## 802. [`SewerBossEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.sewerboss` / 69행

### 타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossEntranceRoom.java#L31) `public class SewerBossEntranceRoom extends EntranceRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossEntranceRoom.java#L34) `public int minWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Painter.fill, Painter.set, Painter.drawInside
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossEntranceRoom.java#L39) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Painter.fill, Painter.set, Painter.drawInside
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossEntranceRoom.java#L43) `public void paint(Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Painter.drawInside

## 803. [`SewerBossExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossExitRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.sewerboss` / 138행

### 타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossExitRoom.java#L36) `public class SewerBossExitRoom extends ExitRoom {`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossExitRoom.java#L80) `public static class SewerExit extends CustomTilemap {`
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossExitRoom.java#L111) `public static class SewerExitOverhang extends CustomTilemap {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossExitRoom.java#L39) `public int minWidth() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Math.max, Painter.fill, Painter.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossExitRoom.java#L44) `public int minHeight() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Math.max, Painter.fill, Painter.set
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossExitRoom.java#L48) `public void paint(Level level) {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill, Painter.set
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossExitRoom.java#L96) `public Tilemap create() {`: 생성·초기화, 조건문
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossExitRoom.java#L103) `public Image image(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossExitRoom.java#L126) `public Tilemap create() {`: 생성·초기화
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/SewerBossExitRoom.java#L133) `public Image image(int tileX, int tileY) {`: 개별 처리(본문 확인)

## 804. [`ThickPillarsGooRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/ThickPillarsGooRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.sewerboss` / 59행

### 타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/ThickPillarsGooRoom.java#L30) `public class ThickPillarsGooRoom extends GooBossRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/ThickPillarsGooRoom.java#L33) `public void paint(Level level) {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill, PerimeterRoom.fillPerimiterPaths

## 805. [`ThinPillarsGooRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/ThinPillarsGooRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.sewerboss` / 72행

### 타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/ThinPillarsGooRoom.java#L30) `public class ThinPillarsGooRoom extends GooBossRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/ThinPillarsGooRoom.java#L33) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, PerimeterRoom.fillPerimiterPaths

## 806. [`WalledGooRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/WalledGooRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.sewerboss` / 72행

### 타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/WalledGooRoom.java#L30) `public class WalledGooRoom extends GooBossRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/WalledGooRoom.java#L33) `public void paint(Level level) {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/sewerboss/WalledGooRoom.java#L68) `public boolean canPlaceWater(Point p) {`: 조회·조건

## 807. [`ArmoryRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ArmoryRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 98행

### 타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ArmoryRoom.java#L36) `public class ArmoryRoom extends SpecialRoom {`

### 필드·상수
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ArmoryRoom.java#L82) `private static float[] prizeCats;`

### 메서드와 연관 호출
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ArmoryRoom.java#L38) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Painter.set, Random.IntRange, Random.chances
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ArmoryRoom.java#L83) `private static Item prize( Level level ) {`: 개별 처리(본문 확인); 인접 호출 Random.chances, Generator.randomWeapon, Generator.randomArmor, Generator.randomMissile

## 808. [`CryptRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CryptRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 99행

### 타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CryptRoom.java#L37) `public class CryptRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CryptRoom.java#L39) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.set, Generator.randomArmor, Challenges.isItemBlocked, Glyph.randomCurse
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CryptRoom.java#L74) `private static Item prize( Level level ) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Generator.randomArmor, Challenges.isItemBlocked, Glyph.randomCurse

## 809. [`CrystalChoiceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalChoiceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 139행

### 타입
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalChoiceRoom.java#L38) `public class CrystalChoiceRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalChoiceRoom.java#L41) `public int minWidth() { return 7; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.set, Painter.drawLine
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalChoiceRoom.java#L42) `public int minHeight() { return 7; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.set, Painter.drawLine
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalChoiceRoom.java#L45) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.set, Painter.drawLine

## 810. [`CrystalPathRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalPathRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 319행

### 타입
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalPathRoom.java#L46) `public class CrystalPathRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalPathRoom.java#L49) `public int minWidth() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.drawInside, Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalPathRoom.java#L50) `public int minHeight() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.drawInside, Painter.set
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalPathRoom.java#L53) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.drawInside, Painter.set
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalPathRoom.java#L199) `public int compare(Item a, Item b) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Collections.sort, Random.Int
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalPathRoom.java#L217) `public int compare(Item a, Item b) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.Int, Generator.random
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalPathRoom.java#L255) `public void addRewardItem(Generator.Category cat, ArrayList<Item> items, ArrayList<Item> dupes){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Generator.random, Math.abs
- [L290](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalPathRoom.java#L290) `public boolean canConnect(Point p) {`: 조회·조건, 조건문; 인접 호출 Math.abs
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalPathRoom.java#L305) `public boolean canPlaceGrass(Point p) {`: 조회·조건
- [L310](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalPathRoom.java#L310) `public boolean canPlaceWater(Point p) {`: 조회·조건
- [L315](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalPathRoom.java#L315) `public boolean canPlaceTrap(Point p) {`: 조회·조건

## 811. [`CrystalVaultRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalVaultRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 107행

### 타입
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalVaultRoom.java#L44) `public class CrystalVaultRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalVaultRoom.java#L48) `public int minHeight() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.shuffle, Random.Int, RatSkull.exoticChanceMultiplier, MimicTooth.mimicChanceMultiplier, Random.Float, Mimic.spawnAt, Painter.set
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalVaultRoom.java#L49) `public int maxHeight() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.shuffle, Random.Int, RatSkull.exoticChanceMultiplier, MimicTooth.mimicChanceMultiplier, Random.Float, Mimic.spawnAt, Painter.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalVaultRoom.java#L50) `public int minWidth() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.shuffle, Random.Int, RatSkull.exoticChanceMultiplier, MimicTooth.mimicChanceMultiplier, Random.Float, Mimic.spawnAt, Painter.set
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalVaultRoom.java#L51) `public int maxWidth() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.shuffle, Random.Int, RatSkull.exoticChanceMultiplier, MimicTooth.mimicChanceMultiplier, Random.Float, Mimic.spawnAt, Painter.set
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalVaultRoom.java#L53) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.shuffle, Random.Int, RatSkull.exoticChanceMultiplier, MimicTooth.mimicChanceMultiplier, Random.Float, Mimic.spawnAt, Painter.set
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/CrystalVaultRoom.java#L92) `private Item prize() {`: 개별 처리(본문 확인), 반복문; 인접 호출 Generator.random, Challenges.isItemBlocked, Arrays.asList

## 812. [`DemonSpawnerRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/DemonSpawnerRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 125행

### 타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/DemonSpawnerRoom.java#L36) `public class DemonSpawnerRoom extends SpecialRoom {`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/DemonSpawnerRoom.java#L84) `public static class CustomFloor extends CustomTilemap {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/DemonSpawnerRoom.java#L38) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/DemonSpawnerRoom.java#L63) `public boolean connect(Room room) {`: 개별 처리(본문 확인), 조건문, 반복문
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/DemonSpawnerRoom.java#L70) `public boolean canPlaceTrap(Point p) {`: 조회·조건, 조건문, 반복문
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/DemonSpawnerRoom.java#L75) `public boolean canPlaceWater(Point p) {`: 조회·조건, 조건문, 반복문
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/DemonSpawnerRoom.java#L80) `public boolean canPlaceGrass(Point p) {`: 조회·조건, 조건문, 반복문
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/DemonSpawnerRoom.java#L91) `public Tilemap create() {`: 생성·초기화, 조건문, 반복문

## 813. [`GardenRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/GardenRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special` / 75행

### 타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/GardenRoom.java#L34) `public class GardenRoom extends SpecialRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/GardenRoom.java#L36) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Sungrass.Seed, BlandfruitBush.Seed
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/GardenRoom.java#L67) `private int plantPos( Level level ){`: 개별 처리(본문 확인), 반복문


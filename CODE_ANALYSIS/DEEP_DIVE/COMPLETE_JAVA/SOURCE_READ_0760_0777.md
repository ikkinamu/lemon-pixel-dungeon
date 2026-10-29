# 실제 Java 소스 정적 분석 760–777

기준 `bd3a990254e4249458816f4879e93ab87275555b`. 모든 항목의 원문을 불러와 타입·상태 변수·메서드와 호출 표현을 조사한다. 기능명은 **정적 의미 추론**이며 AST/런타임 검증이 아니다. 다중행·익명 구조 누락 가능.

## 760. [`VaultCircleScanTreasureRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultCircleScanTreasureRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault.treasure` / 182행

### 타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultCircleScanTreasureRoom.java#L36) `public class VaultCircleScanTreasureRoom extends VaultTreasureRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultCircleScanTreasureRoom.java#L39) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.drawInside, Painter.set
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultCircleScanTreasureRoom.java#L172) `public boolean canPlaceGrass(Point p) {`: 조회·조건; 인접 호출 Math.abs
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultCircleScanTreasureRoom.java#L177) `public boolean canConnect(Point p) {`: 조회·조건; 인접 호출 Math.abs

## 761. [`VaultFlamePathRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamePathRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault.treasure` / 196행

### 타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamePathRoom.java#L37) `public class VaultFlamePathRoom extends VaultTreasureRoom {`

### 필드·상수
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamePathRoom.java#L130) `final int LEFT = 0;`
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamePathRoom.java#L131) `final int UP = 1;`
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamePathRoom.java#L132) `final int RIGHT = 2;`
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamePathRoom.java#L133) `final int DOWN = 3;`

### 메서드와 연관 호출
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamePathRoom.java#L40) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.set
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamePathRoom.java#L135) `public void fillGroup(Level level, Rect space, int dir){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.Int, VaultFlameTrap.setupTrap
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamePathRoom.java#L191) `public boolean canConnect(Point p) {`: 조회·조건; 인접 호출 Math.abs

## 762. [`VaultFlamesTreasureRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamesTreasureRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault.treasure` / 117행

### 타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamesTreasureRoom.java#L35) `public class VaultFlamesTreasureRoom extends VaultTreasureRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamesTreasureRoom.java#L38) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.set, VaultFlameTrap.setupTrap, Math.abs, Painter.drawInside
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamesTreasureRoom.java#L106) `public boolean canPlaceGrass(Point p) {`: 조회·조건; 인접 호출 Math.abs
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultFlamesTreasureRoom.java#L111) `public boolean canConnect(Point p) {`: 조회·조건; 인접 호출 Math.abs

## 763. [`VaultHardLaserTreasureRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultHardLaserTreasureRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault.treasure` / 173행

### 타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultHardLaserTreasureRoom.java#L37) `public class VaultHardLaserTreasureRoom extends VaultTreasureRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultHardLaserTreasureRoom.java#L40) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, GameMath.gate, Painter.set

## 764. [`VaultLaserTreasureRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultLaserTreasureRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault.treasure` / 168행

### 타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultLaserTreasureRoom.java#L36) `public class VaultLaserTreasureRoom extends VaultTreasureRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultLaserTreasureRoom.java#L39) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, GameMath.gate, Painter.set

## 765. [`VaultManyScansRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultManyScansRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault.treasure` / 88행

### 타입
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultManyScansRoom.java#L39) `public class VaultManyScansRoom extends VaultTreasureRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultManyScansRoom.java#L42) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Random.Int

## 766. [`VaultMultipleEnemyTreasureRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultMultipleEnemyTreasureRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault.treasure` / 122행

### 타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultMultipleEnemyTreasureRoom.java#L36) `public class VaultMultipleEnemyTreasureRoom extends VaultTreasureRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultMultipleEnemyTreasureRoom.java#L39) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, GameMath.gate
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultMultipleEnemyTreasureRoom.java#L116) `public boolean canConnect(Point p) {`: 조회·조건; 인접 호출 Math.abs

## 767. [`VaultSingleEnemyTreasureRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultSingleEnemyTreasureRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault.treasure` / 91행

### 타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultSingleEnemyTreasureRoom.java#L36) `public class VaultSingleEnemyTreasureRoom extends VaultTreasureRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultSingleEnemyTreasureRoom.java#L39) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside, Reflection.newInstance, Random.oneOf, Random.Int, Math.abs
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultSingleEnemyTreasureRoom.java#L81) `public boolean canPlaceGrass(Point p) {`: 조회·조건; 인접 호출 Math.abs
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultSingleEnemyTreasureRoom.java#L86) `public boolean canConnect(Point p) {`: 조회·조건; 인접 호출 Math.abs

## 768. [`VaultTreasureRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultTreasureRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault.treasure` / 107행

### 타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultTreasureRoom.java#L33) `public abstract class VaultTreasureRoom extends VaultRoom {`

### 필드·상수
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultTreasureRoom.java#L40) `private Door entrance;`

### 메서드와 연관 호출
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultTreasureRoom.java#L36) `public int maxConnections(int direction) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Arrays.asList, Random.shuffle
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultTreasureRoom.java#L42) `public Door entrance() {`: 개별 처리(본문 확인), 조건문; 인접 호출 Arrays.asList, Random.shuffle
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultTreasureRoom.java#L54) `public boolean canPlaceItem(Point p, Level l) {`: 조회·조건, 조건문, 반복문; 인접 호출 Arrays.asList, Random.shuffle, Reflection.newInstance
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultTreasureRoom.java#L59) `public boolean canPlaceCharacter(Point p, Level l) {`: 조회·조건, 조건문, 반복문; 인접 호출 Arrays.asList, Random.shuffle, Reflection.newInstance
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultTreasureRoom.java#L78) `public static void generateRoomList() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.shuffle, Reflection.newInstance
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/treasure/VaultTreasureRoom.java#L102) `public static VaultTreasureRoom nextRoom(){`: 개별 처리(본문 확인); 인접 호출 Reflection.newInstance

## 769. [`VaultAlternatingFireRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultAlternatingFireRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 78행

### 타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultAlternatingFireRoom.java#L32) `public class VaultAlternatingFireRoom extends VaultRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultAlternatingFireRoom.java#L35) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, VaultFlameTrap.setupTrap
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultAlternatingFireRoom.java#L68) `public boolean canPlaceItem(Point p, Level l) {`: 조회·조건
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultAlternatingFireRoom.java#L73) `public boolean canPlaceCharacter(Point p, Level l) {`: 조회·조건

## 770. [`VaultCircleRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultCircleRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 108행

### 타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultCircleRoom.java#L31) `public class VaultCircleRoom extends VaultRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultCircleRoom.java#L34) `public void paint(Level level) {`: 개별 처리(본문 확인); 인접 호출 Painter.fill, Painter.set, Random.Int
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultCircleRoom.java#L103) `public boolean canPlaceCharacter(Point p, Level l) {`: 조회·조건

## 771. [`VaultCrossRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultCrossRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 69행

### 타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultCrossRoom.java#L30) `public class VaultCrossRoom extends VaultRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultCrossRoom.java#L33) `public void paint(Level level) {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill, Painter.set, Math.abs
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultCrossRoom.java#L64) `public boolean canConnect(Point p) {`: 조회·조건; 인접 호출 Math.abs

## 772. [`VaultEnemyCenterRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEnemyCenterRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 142행

### 타입
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEnemyCenterRoom.java#L40) `public class VaultEnemyCenterRoom extends VaultRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEnemyCenterRoom.java#L43) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.drawLine, Random.Int
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEnemyCenterRoom.java#L135) `public boolean canPlaceItem(Point p, Level l) {`: 조회·조건, 조건문; 인접 호출 Math.abs

## 773. [`VaultEntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEntranceRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 191행

### 타입
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEntranceRoom.java#L44) `public class VaultEntranceRoom extends VaultRoom {`
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEntranceRoom.java#L160) `public static class QuestEntranceInternal extends CustomTilemap {`

### 필드·상수
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEntranceRoom.java#L168) `final int TEX_WIDTH = 256;`

### 메서드와 연관 호출
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEntranceRoom.java#L47) `public void paint(Level level) {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill, Painter.set, Painter.drawInside, AmbitiousImpRoom.WallBanners
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEntranceRoom.java#L151) `public boolean isEntrance() {`: 조회·조건; 인접 호출 Messages.get
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEntranceRoom.java#L156) `public boolean canConnect(Point p) {`: 조회·조건; 인접 호출 Messages.get
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEntranceRoom.java#L171) `public Tilemap create() {`: 생성·초기화; 인접 호출 Messages.get
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEntranceRoom.java#L180) `public String name(int tileX, int tileY) {`: 개별 처리(본문 확인); 인접 호출 Messages.get
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultEntranceRoom.java#L185) `public String desc(int tileX, int tileY) {`: 개별 처리(본문 확인); 인접 호출 Messages.get

## 774. [`VaultFinalRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 685행

### 타입
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L66) `public class VaultFinalRoom extends SpecialRoom {`
- [L420](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L420) `public static class MarkerTiles extends CustomTilemap {`
- [L473](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L473) `public static class FinalRoomDoor extends CustomTilemap {`
- [L557](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L557) `public static class FinalRoomDoorOverhang extends CustomTilemap {`
- [L620](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L620) `public static class VaultTreasure extends CustomTilemap {`

### 필드·상수
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L139) `public Point entryDoor;`
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L140) `public Point lockedDoor;`
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L263) `private int warnState = 0;`
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L264) `private boolean lockTriggered = false;`
- [L383](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L383) `private static final String ENTRY_DOOR_X = "entry_door_x";`
- [L384](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L384) `private static final String ENTRY_DOOR_Y = "entry_door_y";`
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L385) `private static final String LOCKED_DOOR_X = "locked_door_x";`
- [L386](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L386) `private static final String LOCKED_DOOR_Y = "locked_door_y";`
- [L387](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L387) `private static final String WARN_STATE = "warn_state";`
- [L388](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L388) `private static final String LOCK_TRIGGERED = "lock_triggered";`
- [L427](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L427) `final int TEX_WIDTH = 256;`

### 메서드와 연관 호출
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L69) `public int minWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.abs
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L74) `public int maxWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.abs
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L79) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.abs
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L84) `public int maxHeight(){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.abs
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L89) `public boolean isExit() {`: 조회·조건, 조건문, 반복문; 인접 호출 Math.abs
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L94) `public boolean canConnect(Point p) {`: 조회·조건, 조건문, 반복문; 인접 호출 Math.abs
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L99) `public boolean canConnect(Room r) {`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L125) `public boolean canPlaceGrass(Point p) {`: 조회·조건, 조건문; 인접 호출 Painter.fill, Painter.fillEllipse
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L130) `public boolean canPlaceWater(Point p) {`: 조회·조건, 조건문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.set
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L135) `public boolean canPlaceItem(Point p, Level l) {`: 조회·조건, 조건문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.set
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L143) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.set
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L266) `public void processHeroStep(Hero hero){`: 행동·상태 갱신, 조건문, 반복문; 인접 호출 Math.max, Math.abs, Actor.findChar, Random.element, Level.set, GameScene.updateMap, GameScene.add, GLog.n
- [L317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L317) `public void call() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 GameScene.show, Messages.titleCase, Messages.get
- [L365](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L365) `public boolean elementalWasSummoned(){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Level.set, GameScene.updateMap
- [L369](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L369) `public void unlock(){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Level.set, GameScene.updateMap
- [L391](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L391) `public void storeInBundle(Bundle bundle) {`: 저장·복원, 조건문
- [L405](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L405) `public void restoreFromBundle(Bundle bundle) {`: 저장·복원, 조건문; 인접 호출 Messages.get
- [L430](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L430) `public Tilemap create() {`: 생성·초기화, 조건문; 인접 호출 Messages.get
- [L437](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L437) `public Image image(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Messages.get
- [L450](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L450) `public String name(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Messages.get
- [L455](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L455) `public String desc(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Messages.get
- [L460](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L460) `public void restoreFromBundle(Bundle bundle) {`: 저장·복원, 조건문
- [L481](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L481) `public Tilemap create() {`: 생성·초기화, 조건문
- [L490](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L490) `protected boolean updateCell(int cell, int[] data){`: 행동·상태 갱신, 조건문
- [L496](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L496) `protected void updateAll(int[] data) {`: 행동·상태 갱신, 조건문; 인접 호출 Messages.lang
- [L528](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L528) `public Image image(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Messages.lang
- [L543](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L543) `public String desc(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Messages.lang
- [L566](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L566) `public Tilemap create() {`: 생성·초기화, 조건문
- [L575](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L575) `protected boolean updateCell(int cell, int[] data){`: 행동·상태 갱신, 조건문
- [L581](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L581) `protected void updateAll(int[] data) {`: 행동·상태 갱신, 조건문
- [L627](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L627) `public Tilemap create() {`: 생성·초기화, 조건문, 반복문
- [L667](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L667) `public Image image(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Messages.get
- [L675](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultFinalRoom.java#L675) `public String desc(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Messages.get

## 775. [`VaultHallwayRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultHallwayRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 172행

### 타입
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultHallwayRoom.java#L39) `public class VaultHallwayRoom extends VaultLongRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultHallwayRoom.java#L42) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill

## 776. [`VaultLasersRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLasersRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 94행

### 타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLasersRoom.java#L32) `public class VaultLasersRoom extends VaultRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLasersRoom.java#L35) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.drawInside, Random.Int, Painter.set, Random.IntRange
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLasersRoom.java#L89) `public boolean canPlaceCharacter(Point p, Level l) {`: 조회·조건

## 777. [`VaultLongRingsRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRingsRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 92행

### 타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRingsRoom.java#L33) `public class VaultLongRingsRoom extends VaultLongRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRingsRoom.java#L36) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRingsRoom.java#L75) `private int randomWander(Level level, int previous){`: 개별 처리(본문 확인), 반복문
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRingsRoom.java#L86) `public boolean canConnect(Room r) {`: 조회·조건


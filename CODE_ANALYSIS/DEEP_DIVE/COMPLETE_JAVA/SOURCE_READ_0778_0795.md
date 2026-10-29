# 실제 Java 소스 정적 분석 778–795

기준 `bd3a990254e4249458816f4879e93ab87275555b`. 모든 항목의 원문을 불러와 타입·상태 변수·메서드와 호출 표현을 조사한다. 기능명은 **정적 의미 추론**이며 AST/런타임 검증이 아니다. 다중행·익명 구조 누락 가능.

## 778. [`VaultLongRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 75행

### 타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRoom.java#L36) `public abstract class VaultLongRoom extends VaultRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRoom.java#L41) `protected boolean wide(){`: 개별 처리(본문 확인), 조건문
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRoom.java#L50) `public int minWidth() {`: 개별 처리(본문 확인)
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRoom.java#L55) `public int maxWidth() {`: 개별 처리(본문 확인)
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRoom.java#L60) `public int minHeight() {`: 개별 처리(본문 확인)
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRoom.java#L65) `public int maxHeight() {`: 개별 처리(본문 확인)
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultLongRoom.java#L70) `public int sizeFactor() {`: 개별 처리(본문 확인)

## 779. [`VaultQuadrantsRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultQuadrantsRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 150행

### 타입
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultQuadrantsRoom.java#L40) `public class VaultQuadrantsRoom extends VaultRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultQuadrantsRoom.java#L43) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.drawInside, Painter.set, Point.distance
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultQuadrantsRoom.java#L144) `public boolean canConnect(Point p) {`: 조회·조건

## 780. [`VaultRingRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRingRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 100행

### 타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRingRoom.java#L37) `public class VaultRingRoom extends VaultRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRingRoom.java#L40) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int

## 781. [`VaultRingsRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRingsRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 106행

### 타입
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRingsRoom.java#L38) `public class VaultRingsRoom extends VaultRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRingsRoom.java#L41) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Char.hasProp

## 782. [`VaultRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 96행

### 타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRoom.java#L33) `public abstract class VaultRoom extends StandardRoom {`

### 필드·상수
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRoom.java#L79) `private static float[] chances = new float[0];`

### 메서드와 연관 호출
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRoom.java#L38) `public float[] sizeCatProbs() {`: 개별 처리(본문 확인), 조건문; 인접 호출 Random.chances
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRoom.java#L43) `public int minHeight() { return 11; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Random.chances, Reflection.newInstance
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRoom.java#L44) `public int maxHeight() { return 11; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Random.chances, Reflection.newInstance
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRoom.java#L47) `public int minWidth() { return 11; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Random.chances, Reflection.newInstance
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRoom.java#L48) `public int maxWidth() { return 11; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Random.chances, Reflection.newInstance
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRoom.java#L52) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain) {`: 조회·조건, 조건문; 인접 호출 Random.chances, Reflection.newInstance
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRoom.java#L57) `public int sizeFactor() {`: 개별 처리(본문 확인), 조건문; 인접 호출 Random.chances, Reflection.newInstance
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRoom.java#L81) `public static void setupChances(){`: 생성·초기화, 조건문; 인접 호출 Random.chances, Reflection.newInstance
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultRoom.java#L85) `public static VaultRoom createRoom(){`: 생성·초기화, 조건문; 인접 호출 Random.chances, Reflection.newInstance

## 783. [`VaultSimpleEnemyTreasureRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultSimpleEnemyTreasureRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 138행

### 타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultSimpleEnemyTreasureRoom.java#L37) `public class VaultSimpleEnemyTreasureRoom extends VaultRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultSimpleEnemyTreasureRoom.java#L40) `public void paint(Level level) {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill, Random.Int
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultSimpleEnemyTreasureRoom.java#L130) `public boolean canPlaceItem(Point p, Level l) {`: 조회·조건, 조건문; 인접 호출 Math.abs

## 784. [`VaultTokensRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultTokensRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.quest.vault` / 243행

### 타입
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultTokensRoom.java#L43) `public class VaultTokensRoom extends VaultLongRoom {`
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultTokensRoom.java#L210) `public static class TokenDoorFloor extends CustomTilemap {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultTokensRoom.java#L46) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillDiamond
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultTokensRoom.java#L166) `public boolean canConnect(Point p) {`: 조회·조건, 조건문, 반복문
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultTokensRoom.java#L178) `public boolean canConnect(Room r) {`: 조회·조건, 조건문, 반복문
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultTokensRoom.java#L199) `public boolean canPlaceItem(Point p, Level l) {`: 조회·조건, 조건문
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultTokensRoom.java#L204) `public boolean canPlaceCharacter(Point p, Level l) {`: 조회·조건, 조건문
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultTokensRoom.java#L218) `public Tilemap create() {`: 생성·초기화, 조건문
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultTokensRoom.java#L227) `protected boolean updateCell(int cell, int[] data){`: 행동·상태 갱신, 조건문
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/quest/vault/VaultTokensRoom.java#L238) `protected void updateAll(int[] data) {`: 행동·상태 갱신

## 785. [`Room.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms` / 488행

### 타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L37) `public abstract class Room extends Rect implements Graph.Node, Bundlable {`
- [L442](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L442) `public static class Door extends Point implements Bundlable {`
- [L444](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L444) `public enum Type {`

### 필드·상수
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L42) `public int distance;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L43) `public int price = 1;`
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L168) `public static final int ALL     = 0;`
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L169) `public static final int LEFT    = 1;`
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L170) `public static final int TOP     = 2;`
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L171) `public static final int RIGHT   = 3;`
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L172) `public static final int BOTTOM  = 4;`
- [L447](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L447) `public Type type = Type.EMPTY;`
- [L460](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L460) `private boolean typeLocked = false;`

### 메서드와 연관 호출
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L45) `public Room(){`: 개별 처리(본문 확인), 조건문, 반복문
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L49) `public Room( Rect other ){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.min
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L53) `public Room set( Room other ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.min
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L74) `public int minWidth(){`: 개별 처리(본문 확인), 조건문; 인접 호출 Math.min, Random.NormalIntRange
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L77) `public int maxWidth() { return -1; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Math.min, Random.NormalIntRange
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L79) `public int minHeight() { return -1; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Math.min, Random.NormalIntRange
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L80) `public int maxHeight() { return -1; }`: 개별 처리(본문 확인), 조건문; 인접 호출 Math.min, Random.NormalIntRange
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L82) `public boolean setSize(){`: 개별 처리(본문 확인), 조건문; 인접 호출 Math.min, Random.NormalIntRange
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L86) `public boolean forceSize( int w, int h ){`: 개별 처리(본문 확인), 조건문; 인접 호출 Math.min, Random.NormalIntRange
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L90) `public boolean setSizeWithLimit( int w, int h ){`: 개별 처리(본문 확인), 조건문; 인접 호출 Math.min, Random.NormalIntRange
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L104) `protected boolean setSize(int minW, int maxW, int minH, int maxH) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Random.NormalIntRange, Random.IntRange
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L120) `public Point pointInside(Point from, int n){`: 개별 처리(본문 확인), 조건문; 인접 호출 Random.IntRange, Random.Int
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L136) `public int width() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.IntRange, Random.Int
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L141) `public int height() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.IntRange, Random.Int
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L145) `public Point random() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.IntRange, Random.Int
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L149) `public Point random( int m ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.IntRange, Random.Int
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L155) `public boolean inside( Point p ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.Int
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L159) `public Point center() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Random.Int
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L174) `public int minConnections(int direction){`: 개별 처리(본문 확인), 조건문, 반복문
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L179) `public int curConnections(int direction){`: 개별 처리(본문 확인), 조건문, 반복문
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L196) `public int remConnections(int direction){`: 개별 처리(본문 확인), 조건문, 반복문
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L201) `public int maxConnections(int direction){`: 개별 처리(본문 확인), 조건문, 반복문
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L207) `public boolean canConnect(Point p){`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.fill
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L213) `public boolean canConnect(int direction){`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.fill
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L218) `public boolean canConnect( Room r ){`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.fill
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L247) `public boolean canMerge(Level l, Room other, Point p, int mergeTerrain){`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.fill
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L252) `public void merge(Level l, Room other, Rect merge, int mergeTerrain){`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L256) `public boolean addNeigbour( Room other ) {`: 개별 처리(본문 확인), 조건문, 반복문
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L270) `public boolean connect( Room room ) {`: 개별 처리(본문 확인), 조건문, 반복문
- [L281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L281) `public void clearConnections(){`: 개별 처리(본문 확인), 조건문, 반복문
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L292) `public boolean isEntrance(){`: 조회·조건, 조건문, 반복문
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L296) `public boolean isExit(){`: 조회·조건, 조건문, 반복문
- [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L302) `public abstract void paint(Level level);`: 개별 처리(본문 확인), 조건문, 반복문
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L305) `public boolean canPlaceWater(Point p){`: 조회·조건, 조건문, 반복문
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L309) `public final ArrayList<Point> waterPlaceablePoints(){`: 개별 처리(본문 확인), 조건문, 반복문
- [L321](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L321) `public boolean canPlaceGrass(Point p){`: 조회·조건, 조건문, 반복문
- [L325](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L325) `public final ArrayList<Point> grassPlaceablePoints(){`: 개별 처리(본문 확인), 조건문, 반복문
- [L337](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L337) `public boolean canPlaceTrap(Point p){`: 조회·조건, 조건문, 반복문
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L341) `public final ArrayList<Point> trapPlaceablePoints(){`: 개별 처리(본문 확인), 조건문, 반복문
- [L353](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L353) `public boolean canPlaceItem(Point p, Level l){`: 조회·조건, 조건문, 반복문
- [L357](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L357) `public final ArrayList<Point> itemPlaceablePoints(Level l){`: 개별 처리(본문 확인), 조건문, 반복문
- [L369](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L369) `public boolean canPlaceCharacter(Point p, Level l){`: 조회·조건, 조건문, 반복문
- [L373](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L373) `public final ArrayList<Point> charPlaceablePoints(Level l){`: 개별 처리(본문 확인), 조건문, 반복문
- [L388](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L388) `public int distance() {`: 개별 처리(본문 확인), 조건문, 반복문
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L393) `public void distance( int value ) {`: 개별 처리(본문 확인), 조건문, 반복문
- [L398](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L398) `public int price() {`: 개별 처리(본문 확인), 조건문, 반복문
- [L403](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L403) `public void price( int value ) {`: 개별 처리(본문 확인), 조건문, 반복문
- [L408](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L408) `public Collection<Room> edges() {`: 개별 처리(본문 확인), 조건문, 반복문
- [L422](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L422) `public void storeInBundle( Bundle bundle ) {`: 저장·복원, 조건문
- [L430](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L430) `public void restoreFromBundle( Bundle bundle ) {`: 저장·복원, 조건문
- [L438](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L438) `public void onLevelLoad( Level level ){`: 이벤트·효과, 조건문
- [L449](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L449) `public Door(){`: 개별 처리(본문 확인), 조건문
- [L452](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L452) `public Door( Point p ){`: 개별 처리(본문 확인), 조건문
- [L456](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L456) `public Door( int x, int y ) {`: 개별 처리(본문 확인), 조건문
- [L462](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L462) `public void lockTypeChanges( boolean lock ){`: 개별 처리(본문 확인), 조건문
- [L466](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L466) `public void set( Type type ) {`: 개별 처리(본문 확인), 조건문
- [L473](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L473) `public void storeInBundle(Bundle bundle) {`: 저장·복원
- [L481](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L481) `public void restoreFromBundle(Bundle bundle) {`: 저장·복원

## 786. [`RatKingRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 259행

### 타입
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L41) `public class RatKingRoom extends SecretRoom {`
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L129) `public static class RatKingRoomDeco extends CustomTilemap {`
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L199) `public static class RatKingStatues extends CustomTilemap {`
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L229) `public static class StatueOverhang extends CustomTilemap {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L44) `public boolean canConnect(Room r) {`: 조회·조건; 인접 호출 Painter.fill
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L50) `public boolean canPlaceWater(Point p) {`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.fill, Painter.set
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L55) `public boolean canPlaceGrass(Point p) {`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.fill, Painter.set
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L60) `public boolean canPlaceTrap(Point p) {`: 조회·조건, 조건문, 반복문; 인접 호출 Painter.fill, Painter.set
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L66) `public int minWidth() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L67) `public int maxWidth() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L68) `public int minHeight() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L69) `public int maxHeight() { return 7; }`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L71) `public void paint(Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L136) `public Tilemap create() {`: 생성·초기화, 조건문, 반복문; 인접 호출 Messages.get
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L161) `public Image image(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Messages.get
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L175) `public String name(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Messages.get
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L187) `public String desc(int tileX, int tileY) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Messages.get
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L206) `public Tilemap create() {`: 생성·초기화, 조건문, 반복문
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/RatKingRoom.java#L236) `public Tilemap create() {`: 생성·초기화, 조건문, 반복문

## 787. [`SecretArtilleryRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretArtilleryRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 56행

### 타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretArtilleryRoom.java#L30) `public class SecretArtilleryRoom extends SecretRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretArtilleryRoom.java#L33) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Bomb.DoubleBomb, Generator.randomMissile

## 788. [`SecretChestChasmRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretChestChasmRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 118행

### 타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretChestChasmRoom.java#L34) `public class SecretChestChasmRoom extends SecretRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretChestChasmRoom.java#L39) `public int minWidth() {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.set, Generator.randomUsingDefaults
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretChestChasmRoom.java#L44) `public int maxWidth() {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.set, Generator.randomUsingDefaults
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretChestChasmRoom.java#L49) `public int minHeight() {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.set, Generator.randomUsingDefaults
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretChestChasmRoom.java#L54) `public int maxHeight() {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.set, Generator.randomUsingDefaults
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretChestChasmRoom.java#L59) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문; 인접 호출 Painter.fill, Painter.set, Generator.randomUsingDefaults

## 789. [`SecretGardenRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretGardenRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 85행

### 타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretGardenRoom.java#L33) `public class SecretGardenRoom extends SecretRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretGardenRoom.java#L35) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Patch.generate, Starflower.Seed, Seedpod.Seed, Dewcatcher.Seed, Random.Int
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretGardenRoom.java#L73) `private int plantPos( Level level ){`: 개별 처리(본문 확인), 반복문
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretGardenRoom.java#L81) `protected int xyToPatchCoords(int x, int y){`: 개별 처리(본문 확인)

## 790. [`SecretHoardRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretHoardRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 84행

### 타입
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretHoardRoom.java#L38) `public class SecretHoardRoom extends SecretRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretHoardRoom.java#L41) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Random.Int, Math.round, Reflection.newInstance, Painter.set
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretHoardRoom.java#L80) `public boolean canPlaceTrap(Point p) {`: 조회·조건

## 791. [`SecretHoneypotRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretHoneypotRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 73행

### 타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretHoneypotRoom.java#L34) `public class SecretHoneypotRoom extends SecretRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretHoneypotRoom.java#L37) `public void paint(Level level) {`: 개별 처리(본문 확인), 반복문; 인접 호출 Painter.fill, Honeypot.ShatteredPot
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretHoneypotRoom.java#L64) `private void placeItem(Item item, Level level){`: 개별 처리(본문 확인), 반복문

## 792. [`SecretLaboratoryRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLaboratoryRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 112행

### 타입
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLaboratoryRoom.java#L50) `public class SecretLaboratoryRoom extends SecretRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLaboratoryRoom.java#L67) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, Blob.seed, Random.IntRange, Random.chances, Random.Float, ExoticCrystals.consumableExoticChance, Reflection.newInstance

## 793. [`SecretLarderRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLarderRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 82행

### 타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLarderRoom.java#L35) `public class SecretLarderRoom extends SecretRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLarderRoom.java#L38) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, BlandfruitBush.Seed
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLarderRoom.java#L43) `public int minWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, BlandfruitBush.Seed
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLarderRoom.java#L48) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.set, BlandfruitBush.Seed

## 794. [`SecretLibraryRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLibraryRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 110행

### 타입
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLibraryRoom.java#L46) `public class SecretLibraryRoom extends SecretRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLibraryRoom.java#L49) `public int minWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Painter.fill, Painter.fillEllipse, Painter.drawInside, Random.IntRange, Random.chances
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLibraryRoom.java#L54) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Math.max, Painter.fill, Painter.fillEllipse, Painter.drawInside, Random.IntRange, Random.chances, Random.Float, ExoticCrystals.consumableExoticChance
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretLibraryRoom.java#L73) `public void paint( Level level ) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Painter.fillEllipse, Painter.drawInside, Random.IntRange, Random.chances, Random.Float, ExoticCrystals.consumableExoticChance, Reflection.newInstance

## 795. [`SecretMazeRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretMazeRoom.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret` / 127행

### 타입
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretMazeRoom.java#L39) `public class SecretMazeRoom extends SecretRoom {`

### 필드·상수
- 탐지 없음

### 메서드와 연관 호출
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretMazeRoom.java#L42) `public int minWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Maze.generate, PathFinder.setMapSize, PathFinder.buildDistanceMap
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretMazeRoom.java#L47) `public int minHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Maze.generate, PathFinder.setMapSize, PathFinder.buildDistanceMap
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretMazeRoom.java#L52) `public int maxWidth() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Maze.generate, PathFinder.setMapSize, PathFinder.buildDistanceMap, Random.Int
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretMazeRoom.java#L57) `public int maxHeight() {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Maze.generate, PathFinder.setMapSize, PathFinder.buildDistanceMap, Random.Int, Generator.randomWeapon
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretMazeRoom.java#L62) `public void paint(Level level) {`: 개별 처리(본문 확인), 조건문, 반복문; 인접 호출 Painter.fill, Maze.generate, PathFinder.setMapSize, PathFinder.buildDistanceMap, Random.Int, Generator.randomWeapon, Generator.randomArmor


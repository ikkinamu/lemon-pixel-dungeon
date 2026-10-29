# Java 소스 구현 분석 1120–1137

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1120. [`v0_9_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_9_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 615행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_9_X_Changes.java#L31) `public class v0_9_X_Changes {`
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_9_X_Changes.java#L224) `"These talents are a bit different than the previous tiers. They require 3 points each, are balanced to encourage specialization, and vary based on cl`
- [L565](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_9_X_Changes.java#L565) `"_-_ Tweaked some interface visuals to be more rounded.\n\n" +`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_9_X_Changes.java#L33) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_9_X_Changes.java#L39) `public static void add_v0_9_2_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L358](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_9_X_Changes.java#L358) `public static void add_v0_9_1_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L509](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_9_X_Changes.java#L509) `public static void add_v0_9_0_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get

## 1121. [`v1_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v1_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 978행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v1_X_Changes.java#L31) `public class v1_X_Changes {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v1_X_Changes.java#L33) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v1_X_Changes.java#L41) `public static void add_v1_4_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v1_X_Changes.java#L266) `public static void add_v1_3_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L443](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v1_X_Changes.java#L443) `public static void add_v1_2_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L629](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v1_X_Changes.java#L629) `public static void add_v1_1_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L804](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v1_X_Changes.java#L804) `public static void add_v1_0_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get

## 1122. [`v2_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 1462행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java#L32) `public class v2_X_Changes {`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java#L60) `"_The game's Journal interface has been completely overhauled!_\n" +`
- [L586](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java#L586) `"_Heroes remains now contain a new unique item that varies based on the class of the hero that died._\n" +`
- [L865](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java#L865) `"_-_ Various errors with class armor conversion and Warrior's broken seal\n" +`
- [L1302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java#L1302) `"_-_ One upgrade being lost when transferring class armor with a warrior's seal attached\n" +`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java#L34) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java#L43) `public static void add_v2_5_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L330](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java#L330) `public static void add_v2_4_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L559](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java#L559) `public static void add_v2_3_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L749](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java#L749) `public static void add_v2_2_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L943](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java#L943) `public static void add_v2_1_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L1173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v2_X_Changes.java#L1173) `public static void add_v2_0_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get, DUELIST.title

## 1123. [`v3_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v3_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 902행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v3_X_Changes.java#L31) `public class v3_X_Changes {`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v3_X_Changes.java#L77) `"This includes a random class and challenges (optionally) in hero select, and random talents, subclass, and armor ability within the game! This add so`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v3_X_Changes.java#L33) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v3_X_Changes.java#L40) `public static void add_v3_3_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v3_X_Changes.java#L252) `public static void add_v3_2_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L484](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v3_X_Changes.java#L484) `public static void add_v3_1_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L709](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v3_X_Changes.java#L709) `public static void add_v3_0_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get

## 1124. [`v4_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v4_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 378행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v4_X_Changes.java#L35) `public class v4_X_Changes {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v4_X_Changes.java#L37) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: DeviceCompat.isiOS, DeviceCompat.getPlatformVersion, WARNING.get
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v4_X_Changes.java#L43) `public static void add_Coming_Soon( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: DeviceCompat.isiOS, DeviceCompat.getPlatformVersion, WARNING.get, Messages.get
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v4_X_Changes.java#L75) `public static void add_v4_0_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get

## 1125. [`WndChanges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChanges.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 47행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChanges.java#L30) `public class WndChanges extends WndTitledMessage {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChanges.java#L32) `public WndChanges( Image icon, String title, String message ) {` — 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChanges.java#L37) `protected void onClick( PointerEvent event ) {` — 이벤트·효과 실행

## 1126. [`WndChangesTabbed.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChangesTabbed.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 124행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChangesTabbed.java#L34) `public class WndChangesTabbed extends WndTabbed {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChangesTabbed.java#L36) `protected static final int WIDTH_MIN    = 120;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChangesTabbed.java#L37) `protected static final int WIDTH_MAX    = 220;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChangesTabbed.java#L38) `protected static final int GAP	= 2;`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChangesTabbed.java#L42) `public WndChangesTabbed(Image icon, String title, String... messages ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.landscape
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChangesTabbed.java#L50) `protected void onClick( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: PixelScene.renderTextBlock, PixelScene.landscape
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChangesTabbed.java#L76) `protected void select(boolean value) {` — 개별 처리, 인접 호출: PixelScene.landscape, Integer.toString
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/WndChangesTabbed.java#L108) `private String numToNumeral(int num){` — 개별 처리, 인접 호출: Integer.toString

## 1127. [`CharHealthIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CharHealthIndicator.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 73행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CharHealthIndicator.java#L28) `public class CharHealthIndicator extends HealthBar {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CharHealthIndicator.java#L30) `private static final int HEIGHT = 1;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CharHealthIndicator.java#L32) `private Char target;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CharHealthIndicator.java#L34) `public CharHealthIndicator( Char c ){` — 개별 처리, 인접 호출: GameScene.add
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CharHealthIndicator.java#L40) `protected void createChildren() {` — 생성·초기화
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CharHealthIndicator.java#L46) `public void update() {` — 행동·상태 갱신
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CharHealthIndicator.java#L61) `public void target( Char ch ) {` — 개별 처리
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CharHealthIndicator.java#L69) `public Char target() {` — 개별 처리

## 1128. [`CheckBox.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CheckBox.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 80행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CheckBox.java#L26) `public class CheckBox extends RedButton {`

### 변수·상수 후보
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CheckBox.java#L28) `private boolean checked = false;`

### 메서드 및 코드 의존 단서
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CheckBox.java#L30) `public CheckBox( String label ) {` — 개별 처리, 인접 호출: Icons.get, PixelScene.align, PixelScene.renderTextBlock
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CheckBox.java#L37) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, PixelScene.renderTextBlock, Icons.get
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CheckBox.java#L63) `public boolean checked() {` — 개별 처리, 인접 호출: Icons.get
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CheckBox.java#L67) `public void checked( boolean value ) {` — 개별 처리, 인접 호출: Icons.get
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CheckBox.java#L75) `protected void onClick() {` — 이벤트·효과 실행

## 1129. [`Compass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Compass.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 72행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Compass.java#L30) `public class Compass extends Image {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Compass.java#L32) `private static final float RAD_2_G	= 180f / 3.1415926f;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Compass.java#L33) `private static final float RADIUS	= 12;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Compass.java#L35) `private int cell;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Compass.java#L36) `private PointF cellCenter;`

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Compass.java#L38) `private PointF lastScroll = new PointF();` — 개별 처리, 인접 호출: COMPASS.get, DungeonTilemap.tileCenterToWorld, Math.atan2
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Compass.java#L40) `public Compass( int cell ) {` — 개별 처리, 인접 호출: COMPASS.get, DungeonTilemap.tileCenterToWorld, Math.atan2
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Compass.java#L52) `public void update() {` — 행동·상태 갱신, 인접 호출: Math.atan2

## 1130. [`CurrencyIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 136행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java#L30) `public class CurrencyIndicator extends Component {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java#L32) `private static final float TIME	= 2f;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java#L34) `private int lastGold = 0;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java#L35) `private int lastEnergy = 0;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java#L37) `private BitmapText gold;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java#L38) `private BitmapText energy;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java#L40) `private float goldTime;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java#L41) `private float energyTime;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java#L43) `public static boolean showGold = false;`

### 메서드 및 코드 의존 단서
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java#L46) `protected void createChildren() {` — 생성·초기화, 인접 호출: Integer.toString
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java#L63) `protected void layout() {` — 개별 처리, 인접 호출: Integer.toString
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CurrencyIndicator.java#L76) `public void update() {` — 행동·상태 갱신, 인접 호출: Integer.toString

## 1131. [`CustomNoteButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 400행.

### 클래스/타입
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L51) `public class CustomNoteButton extends IconButton {`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L82) `private class WndNoteTypeSelect extends WndOptions {`
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L123) `private class WndDepthSelect extends WndTitledMessage {`
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L203) `private static class WndItemtypeSelect extends WndTitledMessage {`
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L273) `public static class CustomNoteWindow extends WndJournalItem {`

### 변수·상수 후보
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L80) `private static WndNoteTypeSelect NOTE_SELECT_INSTANCE;`

### 메서드 및 코드 의존 단서
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L53) `public CustomNoteButton () {` — 개별 처리, 인접 호출: PLUS.get, Notes.getRecords, Notes.customRecordLimit, GameScene.show, INFO.get, Messages.get, SCROLL_COLOR.get
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L61) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Notes.getRecords, Notes.customRecordLimit, GameScene.show, INFO.get, Messages.get, SCROLL_COLOR.get, Notes.CustomRecord
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L76) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, SCROLL_COLOR.get, Notes.CustomRecord, GameScene.show, GameScene.selectItem
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L84) `public WndNoteTypeSelect(){` — 개별 처리, 인접 호출: SCROLL_COLOR.get, Messages.get, Notes.CustomRecord, GameScene.show, GameScene.selectItem, STAIRS.get
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L96) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: Notes.CustomRecord, Messages.get, GameScene.show, GameScene.selectItem, STAIRS.get, Integer.toString
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L112) `public void hide() {` — 개별 처리, 인접 호출: STAIRS.get, Messages.get, Integer.toString, Notes.CustomRecord
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L117) `public void onBackPressed() {` — 이벤트·효과 실행, 인접 호출: STAIRS.get, Messages.get, Integer.toString, Notes.CustomRecord, WndBag.ItemSelector
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L125) `public WndDepthSelect(){` — 개별 처리, 인접 호출: STAIRS.get, Messages.get, Integer.toString, Notes.CustomRecord, WndBag.ItemSelector
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L141) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Notes.CustomRecord, Messages.get, WndBag.ItemSelector, Notes.findCustomRecord
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L158) `private WndBag.ItemSelector itemSelector = new WndBag.ItemSelector() {` — 개별 처리, 인접 호출: Messages.get, Notes.findCustomRecord, Notes.CustomRecord, Messages.titleCase
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L161) `public String textPrompt() {` — 개별 처리, 인접 호출: Messages.get, Notes.findCustomRecord, Notes.CustomRecord, Messages.titleCase
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L166) `public boolean hideAfterSelecting() {` — 개별 처리, 인접 호출: Notes.findCustomRecord, Notes.CustomRecord, Messages.get, Messages.titleCase, SCROLL_COLOR.get
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L171) `public boolean itemSelectable(Item item) {` — 개별 처리, 인접 호출: Notes.findCustomRecord, Notes.CustomRecord, Messages.get, Messages.titleCase, SCROLL_COLOR.get, Reflection.newInstance
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L184) `public void onSelect( Item item ) {` — 이벤트·효과 실행, 인접 호출: Notes.CustomRecord, Messages.get, Messages.titleCase, SCROLL_COLOR.get, Reflection.newInstance, Collections.sort
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L205) `public WndItemtypeSelect() {` — 개별 처리, 인접 호출: SCROLL_COLOR.get, Messages.get, Reflection.newInstance, Collections.sort, Notes.CustomRecord, Messages.titleCase, Notes.findCustomRecord
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L227) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Notes.CustomRecord, Messages.get, Messages.titleCase, Notes.findCustomRecord
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L259) `public int compare(Item i1, Item i2) {` — 개별 처리, 인접 호출: Messages.get, GameScene.show
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L275) `public CustomNoteWindow(Notes.CustomRecord rec, Window parentWindow) {` — 개별 처리, 인접 호출: Messages.get, GameScene.show, Math.min
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L280) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.get, Math.min
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L289) `public void onSelect(boolean positive, String text) {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Math.min, Messages.get
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L311) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.get, WARNING.get, Notes.remove, ShatteredPixelDungeon.scene
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L320) `public void onSelect(boolean positive, String text) {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.get, WARNING.get, Notes.remove, ShatteredPixelDungeon.scene
- [L335](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L335) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, WARNING.get, Messages.get, Notes.remove, ShatteredPixelDungeon.scene, Notes.add
- [L342](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L342) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: Notes.remove, ShatteredPixelDungeon.scene, GameScene.show, Messages.get, Notes.add, INSTANCE.hide
- [L363](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L363) `protected boolean useHighlighting() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.get, Notes.add, INSTANCE.hide, NOTE_SELECT_INSTANCE.onBackPressed, ShatteredPixelDungeon.scene
- [L368](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L368) `private static void addNote(Window parentWindow, Notes.CustomRecord note, String promptTitle, String prompttext){` — 개별 처리, 인접 호출: GameScene.show, Messages.get, Notes.add, INSTANCE.hide, NOTE_SELECT_INSTANCE.onBackPressed, ShatteredPixelDungeon.scene
- [L377](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CustomNoteButton.java#L377) `public void onSelect(boolean positive, String text) {` — 이벤트·효과 실행, 인접 호출: Notes.add, INSTANCE.hide, NOTE_SELECT_INSTANCE.onBackPressed, ShatteredPixelDungeon.scene

## 1132. [`DangerIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 131행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L35) `public class DangerIndicator extends Tag {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L37) `public static final int COLOR	= 0xC03838;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L39) `private BitmapText number;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L40) `private Image icon;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L42) `private int enemyIndex = 0;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L44) `private int lastNumber = -1;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L46) `public static int HEIGHT = 16;`

### 메서드 및 코드 의존 단서
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L48) `public DangerIndicator() {` — 개별 처리, 인접 호출: SKULL.get, PixelScene.align
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L57) `public GameAction keyAction() {` — 개별 처리, 인접 호출: SKULL.get, PixelScene.align, Integer.toString
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L62) `protected void createChildren() {` — 생성·초기화, 인접 호출: SKULL.get, PixelScene.align, Integer.toString
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L73) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, Integer.toString, QuickSlotButton.target
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L82) `private void placeNumber() {` — 개별 처리, 인접 호출: PixelScene.align, Integer.toString, QuickSlotButton.target, AttackIndicator.target
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L89) `public void update() {` — 행동·상태 갱신, 인접 호출: Integer.toString, QuickSlotButton.target, AttackIndicator.target, Messages.titleCase, Messages.get
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L111) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: QuickSlotButton.target, AttackIndicator.target, Messages.titleCase, Messages.get
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/DangerIndicator.java#L127) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get

## 1133. [`ExitButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ExitButton.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 61행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ExitButton.java#L33) `public class ExitButton extends IconButton {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ExitButton.java#L35) `public ExitButton() {` — 개별 처리, 인접 호출: EXIT.get, PixelScene.landscape, DeviceCompat.isDesktop, Game.scene, ShatteredPixelDungeon.switchNoFade, Messages.titleCase, Messages.get
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ExitButton.java#L43) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Game.scene, ShatteredPixelDungeon.switchNoFade, Messages.titleCase, Messages.get
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ExitButton.java#L52) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ExitButton.java#L57) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get

## 1134. [`GameLog.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 184행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L34) `public class GameLog extends Component implements Signal.Listener<String> {`
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L168) `private static class Entry {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L36) `private static final int MAX_LINES = 3;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L40) `private RenderedTextBlock lastEntry;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L41) `private int lastColor;`
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L169) `public String text;`
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L170) `public int color;`

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L38) `private static final Pattern PUNCTUATION = Pattern.compile( ".*[.,;?! ]$" );` — 개별 처리, 인접 호출: SPDSettings.interfaceSize, POSITIVE.length, NEGATIVE.length, WARNING.length
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L45) `public GameLog() {` — 개별 처리, 인접 호출: SPDSettings.interfaceSize, POSITIVE.length, NEGATIVE.length, WARNING.length, HIGHLIGHT.length
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L55) `public synchronized void update() {` — 행동·상태 갱신, 인접 호출: SPDSettings.interfaceSize, POSITIVE.length, NEGATIVE.length, WARNING.length, HIGHLIGHT.length, PixelScene.renderTextBlock
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L57) `synchronized (textsToAdd){` — 개별 처리, 인접 호출: SPDSettings.interfaceSize, POSITIVE.length, NEGATIVE.length, WARNING.length, HIGHLIGHT.length, PixelScene.renderTextBlock
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L136) `private synchronized void recreateLines() {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L144) `public synchronized void newLine() {` — 개별 처리
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L149) `public boolean onSignal( String text ) {` — 이벤트·효과 실행
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L150) `synchronized (textsToAdd) {` — 개별 처리
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L157) `protected void layout() {` — 개별 처리
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L171) `public Entry( String text, int color ) {` — 개별 처리
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L177) `public static void wipe() {` — 개별 처리
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java#L178) `synchronized (textsToAdd) {` — 개별 처리

## 1135. [`HealthBar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 104행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L28) `public class HealthBar extends Component {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L30) `private static final int COLOR_BG	= 0xFFAA0000;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L31) `private static final int COLOR_HP	= 0xFF00EE00;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L32) `private static final int COLOR_SHLD = 0xFFFFFFFF;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L33) `private static final int COLOR_DOT	= 0x66000000;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L35) `private static final int HEIGHT	= 2;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L37) `private ColorBlock Bg;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L38) `private ColorBlock Shld;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L39) `private ColorBlock Hp;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L40) `private ColorBlock Dot;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L42) `private float health;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L43) `private float shield;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L44) `private float incomingDOT;`

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L47) `protected void createChildren() {` — 생성·초기화, 인접 호출: Bg.size, Shld.size, Math.ceil, Hp.size, Dot.size, Math.min, Shld.width
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L64) `protected void layout() {` — 개별 처리, 인접 호출: Bg.size, Shld.size, Math.ceil, Hp.size, Dot.size, Math.min, Shld.width
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L82) `public void level( float value ) {` — 개별 처리, 인접 호출: Math.max
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L86) `public void level( float health, float shield, float DOT ){` — 개별 처리, 인접 호출: Math.max
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HealthBar.java#L93) `public void level(Char c){` — 개별 처리, 인접 호출: Math.max

## 1136. [`HeroIcon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 149행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L32) `public class HeroIcon extends Image {`

### 변수·상수 후보
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L34) `private static TextureFilm film;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L35) `private static final int SIZE = 16;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L38) `public static final int NONE    = 127;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L41) `public static final int BERSERKER   = 0;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L42) `public static final int GLADIATOR   = 1;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L43) `public static final int BATTLEMAGE  = 2;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L44) `public static final int WARLOCK     = 3;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L45) `public static final int ASSASSIN    = 4;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L46) `public static final int FREERUNNER  = 5;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L47) `public static final int SNIPER      = 6;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L48) `public static final int WARDEN      = 7;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L49) `public static final int CHAMPION    = 8;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L50) `public static final int MONK        = 9;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L51) `public static final int PRIEST      = 10;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L52) `public static final int PALADIN     = 11;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L55) `public static final int HEROIC_LEAP     = 16;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L56) `public static final int SHOCKWAVE       = 17;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L57) `public static final int ENDURE          = 18;`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L58) `public static final int ELEMENTAL_BLAST = 19;`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L59) `public static final int WILD_MAGIC      = 20;`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L60) `public static final int WARP_BEACON     = 21;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L61) `public static final int SMOKE_BOMB      = 22;`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L62) `public static final int DEATH_MARK      = 23;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L63) `public static final int SHADOW_CLONE    = 24;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L64) `public static final int SPECTRAL_BLADES = 25;`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L65) `public static final int NATURES_POWER   = 26;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L66) `public static final int SPIRIT_HAWK     = 27;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L67) `public static final int CHALLENGE       = 28;`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L68) `public static final int ELEMENTAL_STRIKE= 29;`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L69) `public static final int FEINT           = 30;`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L70) `public static final int ASCENDED_FORM   = 31;`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L71) `public static final int TRINITY         = 32;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L72) `public static final int POWER_OF_MANY   = 33;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L73) `public static final int RATMOGRIFY      = 34;`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L76) `public static final int GUIDING_LIGHT   = 40;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L77) `public static final int HOLY_WEAPON     = 41;`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L78) `public static final int HOLY_WARD       = 42;`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L79) `public static final int HOLY_INTUITION  = 43;`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L80) `public static final int SHIELD_OF_LIGHT = 44;`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L81) `public static final int RECALL_GLYPH    = 45;`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L82) `public static final int SUNRAY          = 46;`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L83) `public static final int DIVINE_SENSE    = 47;`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L84) `public static final int BLESS           = 48;`
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L85) `public static final int CLEANSE         = 49;`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L86) `public static final int RADIANCE        = 50;`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L87) `public static final int HOLY_LANCE      = 51;`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L88) `public static final int HALLOWED_GROUND = 52;`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L89) `public static final int MNEMONIC_PRAYER = 53;`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L90) `public static final int SMITE           = 54;`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L91) `public static final int LAY_ON_HANDS    = 55;`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L92) `public static final int AURA_OF_PROTECTION = 56;`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L93) `public static final int WALL_OF_LIGHT   = 57;`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L94) `public static final int DIVINE_INTERVENTION = 58;`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L95) `public static final int JUDGEMENT       = 59;`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L96) `public static final int FLASH           = 60;`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L97) `public static final int BODY_FORM       = 61;`
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L98) `public static final int MIND_FORM       = 62;`
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L99) `public static final int SPIRIT_FORM     = 63;`
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L100) `public static final int BEAMING_RAY     = 64;`
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L101) `public static final int LIFE_LINK       = 65;`
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L102) `public static final int STASIS          = 66;`
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L105) `public static final int SPELL_ACTION_OFFSET      = 32;`
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L108) `public static final int BERSERK         = 104;`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L109) `public static final int COMBO           = 105;`
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L110) `public static final int PREPARATION     = 106;`
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L111) `public static final int MOMENTUM        = 107;`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L112) `public static final int SNIPERS_MARK    = 108;`
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L113) `public static final int WEAPON_SWAP     = 109;`
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L114) `public static final int MONK_ABILITIES  = 110;`

### 메서드 및 코드 의존 단서
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L116) `public HeroIcon(HeroSubClass subCls){` — 개별 처리
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L124) `public HeroIcon(ArmorAbility abil){` — 개별 처리
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L132) `public HeroIcon(ActionIndicator.Action action){` — 개별 처리
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java#L140) `public HeroIcon(ClericSpell spell){` — 개별 처리

## 1137. [`IconButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 84행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java#L29) `public class IconButton extends Button {`

### 변수·상수 후보
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java#L31) `protected Image icon;`

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java#L33) `public IconButton(){` — 개별 처리, 인접 호출: PixelScene.align, INSTANCE.play
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java#L37) `public IconButton( Image icon ){` — 개별 처리, 인접 호출: PixelScene.align, INSTANCE.play
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java#L43) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, INSTANCE.play
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java#L54) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java#L60) `protected void onPointerUp() {` — 이벤트·효과 실행
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java#L64) `public void enable( boolean value ) {` — 개별 처리
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java#L69) `public void icon( Image icon ) {` — 개별 처리
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java#L80) `public Image icon(){` — 개별 처리


# Java 소스 구현 분석 1300–1317

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1300. [`Cursor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java)

패키지 `com.watabou.noosa.ui`, 124행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java#L33) `public class Cursor {`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java#L37) `public enum Type {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java#L35) `private static com.badlogic.gdx.graphics.Cursor currentCursor;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java#L43) `public final String file;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java#L51) `private static Type lastType;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java#L52) `private static int lastZoom;`
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java#L98) `private static boolean cursorCaptured = false;`

### 메서드 및 코드 의존 단서
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java#L54) `public static void setCustomCursor(Type type, int zoom){` — 개별 처리, 인접 호출: DeviceCompat.isDesktop, FileUtils.getFileHandle
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java#L100) `public static void captureCursor(boolean captured){` — 개별 처리, 인접 호출: ControllerHandler.controllerPointerActive, ControllerHandler.setControllerPointer, ControllerHandler.updateControllerPointer
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java#L115) `public static PointF getCursorDelta(){` — 조회·판정
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java#L119) `public static boolean isCursorCaptured(){` — 조회·판정

## 1301. [`Visual.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java)

패키지 `com.watabou.noosa`, 298행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L28) `public class Visual extends Gizmo {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L30) `public float x;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L31) `public float y;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L32) `public float width;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L33) `public float height;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L35) `public PointF scale;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L36) `public PointF origin;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L38) `protected float[] matrix;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L40) `public float rm;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L41) `public float gm;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L42) `public float bm;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L43) `public float am;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L44) `public float ra;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L45) `public float ga;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L46) `public float ba;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L47) `public float aa;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L49) `public PointF speed;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L50) `public PointF acc;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L52) `public float angle;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L53) `public float angularSpeed;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L55) `private float lastX, lastY, lastW, lastH, lastA;`

### 메서드 및 코드 의존 단서
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L56) `private PointF lastScale = new PointF(), lastOrigin = new PointF();` — 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L58) `public Visual( float x, float y, float width, float height ) {` — 개별 처리
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L76) `public void update() {` — 행동·상태 갱신, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.rotate, Matrix.scale
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L84) `public void draw() {` — 개별 처리, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.rotate, Matrix.scale
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L109) `protected void updateMatrix() {` — 행동·상태 갱신, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.rotate, Matrix.scale
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L124) `public PointF point() {` — 개별 처리
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L128) `public PointF point( PointF p ) {` — 개별 처리
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L134) `public Point point( Point p ) {` — 개별 처리
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L140) `public PointF center() {` — 개별 처리
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L144) `public PointF center( PointF p ) {` — 개별 처리
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L151) `public PointF center( Visual v ) {` — 개별 처리
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L158) `public void originToCenter() {` — 개별 처리
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L162) `public float width() {` — 개별 처리
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L166) `public float height() {` — 개별 처리
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L170) `protected void updateMotion() {` — 행동·상태 갱신
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L186) `public void alpha( float value ) {` — 개별 처리
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L191) `public float alpha() {` — 개별 처리
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L195) `public void invert() {` — 개별 처리
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L200) `public void lightness( float value ) {` — 개별 처리
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L210) `public void brightness( float value ) {` — 개별 처리
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L214) `public void tint( float r, float g, float b, float strength ) {` — 개별 처리
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L221) `public void tint( int color, float strength ) {` — 개별 처리
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L229) `public void tint( int color ) {` — 개별 처리
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L233) `public void color( float r, float g, float b ) {` — 개별 처리
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L240) `public void color( int color ) {` — 개별 처리
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L244) `public void hardlight( float r, float g, float b ) {` — 개별 처리
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L251) `public void hardlight( int color ) {` — 개별 처리
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L255) `public void resetColor() {` — 개별 처리
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L260) `public boolean overlapsPoint( float x, float y ) {` — 개별 처리
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L264) `public boolean overlapsScreenPoint( int x, int y ) {` — 개별 처리
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java#L275) `public boolean isVisible() {` — 조회·판정

## 1302. [`BArray.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java)

패키지 `com.watabou.utils`, 157행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java#L24) `public class BArray {`

### 변수·상수 후보
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java#L26) `private static boolean[] falseArray;`

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java#L29) `public static void setFalse( boolean[] toBeFalse ){` — 개별 처리, 인접 호출: System.arraycopy
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java#L36) `public static boolean[] and( boolean[] a, boolean[] b, boolean[] result ) {` — 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java#L51) `public static boolean[] or( boolean[] a, boolean[] b, boolean[] result ){` — 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java#L55) `public static boolean[] or( boolean[] a, boolean[] b, int offset, int length, boolean[] result ) {` — 개별 처리
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java#L68) `public static boolean[] not( boolean[] a, boolean[] result ) {` — 개별 처리
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java#L83) `public static boolean[] is( int[] a, boolean[] result, int v1 ) {` — 조회·판정
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java#L98) `public static boolean[] isOneOf( int[] a, boolean[] result, int... v ) {` — 조회·판정
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java#L120) `public static boolean[] isNot( int[] a, boolean[] result, int v1 ) {` — 조회·판정
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java#L135) `public static boolean[] isNotOneOf( int[] a, boolean[] result, int... v ) {` — 조회·판정

## 1303. [`BitmapCache.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapCache.java)

패키지 `com.watabou.utils`, 119행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapCache.java#L30) `public class BitmapCache {`
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapCache.java#L108) `private static class Layer extends HashMap<Object,Pixmap> {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapCache.java#L32) `private static final String DEFAULT	= "__default";`

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapCache.java#L36) `public static Pixmap get( String assetName ) {` — 조회·판정, 인접 호출: Game.reportException
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapCache.java#L40) `public static Pixmap get( String layerName, String assetName ) {` — 조회·판정, 인접 호출: Game.reportException
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapCache.java#L68) `public static Pixmap get( int resID ) {` — 조회·판정, 인접 호출: BitmapFactory.decodeResource
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapCache.java#L72) `public static Pixmap get( String layerName, int resID ) {` — 조회·판정, 인접 호출: BitmapFactory.decodeResource
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapCache.java#L93) `public static void clear( String layerName ) {` — 개별 처리
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapCache.java#L100) `public static void clear() {` — 개별 처리
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapCache.java#L111) `public void clear() {` — 개별 처리

## 1304. [`BitmapFilm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapFilm.java)

패키지 `com.watabou.utils`, 63행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapFilm.java#L28) `public class BitmapFilm {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapFilm.java#L30) `public Pixmap bitmap;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapFilm.java#L34) `public BitmapFilm( Pixmap bitmap ) {` — 개별 처리
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapFilm.java#L39) `public BitmapFilm( Pixmap bitmap, int width ) {` — 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapFilm.java#L43) `public BitmapFilm( Pixmap bitmap, int width, int height ) {` — 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapFilm.java#L55) `public void add( Object id, Rect rect ) {` — 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BitmapFilm.java#L59) `public Rect get( Object id ) {` — 조회·판정

## 1305. [`Bundlable.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundlable.java)

패키지 `com.watabou.utils`, 30행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundlable.java#L24) `public interface Bundlable {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- 없음

## 1306. [`Bundle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java)

패키지 `com.watabou.utils`, 561행.

### 클래스/타입
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L46) `public class Bundle {`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L65) `what methods exist in all versions of org.json. This class is also commented in places`

### 변수·상수 후보
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L48) `private static final String CLASS_NAME = "__className";`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L50) `public static final String DEFAULT_KEY = "key";`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L68) `private JSONObject data;`
- [L483](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L483) `private static final boolean compressByDefault = true;`

### 메서드 및 코드 의존 단서
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L70) `public Bundle() {` — 개별 처리, 인접 호출: JSONObject.keyset
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L74) `public String toString() {` — 개별 처리, 인접 호출: JSONObject.keyset
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L78) `private Bundle( JSONObject data ) {` — 개별 처리, 인접 호출: JSONObject.keyset
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L82) `public boolean isNull() {` — 조회·판정, 인접 호출: JSONObject.keyset
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L86) `public boolean contains( String key ) {` — 개별 처리, 인접 호출: JSONObject.keyset
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L90) `public boolean remove( String key ){` — 개별 처리, 인접 호출: JSONObject.keyset, Reflection.forName
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L95) `public ArrayList<String> getKeys(){` — 조회·판정, 인접 호출: Reflection.forName
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L104) `public boolean getBoolean( String key ) {` — 조회·판정, 인접 호출: Reflection.forName
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L108) `public int getInt( String key ) {` — 조회·판정, 인접 호출: Reflection.forName, Reflection.isMemberClass, Reflection.isStatic, Reflection.newInstance
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L112) `public long getLong( String key ) {` — 조회·판정, 인접 호출: Reflection.forName, Reflection.isMemberClass, Reflection.isStatic, Reflection.newInstance
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L116) `public float getFloat( String key ) {` — 조회·판정, 인접 호출: Reflection.forName, Reflection.isMemberClass, Reflection.isStatic, Reflection.newInstance
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L120) `public String getString( String key ) {` — 조회·판정, 인접 호출: Reflection.forName, Reflection.isMemberClass, Reflection.isStatic, Reflection.newInstance
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L124) `public Class getClass( String key ) {` — 조회·판정, 인접 호출: Reflection.forName, Reflection.isMemberClass, Reflection.isStatic, Reflection.newInstance, Enum.valueOf
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L136) `public Bundle getBundle( String key ) {` — 조회·판정, 인접 호출: Reflection.forName, Reflection.isMemberClass, Reflection.isStatic, Reflection.newInstance, Enum.valueOf, Game.reportException
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L140) `private Bundlable get() {` — 조회·판정, 인접 호출: Reflection.forName, Reflection.isMemberClass, Reflection.isStatic, Reflection.newInstance, Enum.valueOf, Game.reportException
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L162) `public Bundlable get( String key ) {` — 조회·판정, 인접 호출: Enum.valueOf, Game.reportException
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L166) `public <E extends Enum<E>> E getEnum( String key, Class<E> enumClass ) {` — 조회·판정, 인접 호출: Enum.valueOf, Game.reportException
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L178) `public int[] getIntArray( String key ) {` — 조회·판정, 인접 호출: Game.reportException
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L193) `public long[] getLongArray( String key ) {` — 조회·판정, 인접 호출: Game.reportException
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L208) `public float[] getFloatArray( String key ) {` — 조회·판정, 인접 호출: Game.reportException
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L223) `public boolean[] getBooleanArray( String key ) {` — 조회·판정, 인접 호출: Game.reportException, Reflection.forName
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L238) `public String[] getStringArray( String key ) {` — 조회·판정, 인접 호출: Game.reportException, Reflection.forName
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L253) `public Class[] getClassArray( String key ) {` — 조회·판정, 인접 호출: Reflection.forName, Game.reportException
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L273) `public Bundle[] getBundleArray(){` — 조회·판정, 인접 호출: Game.reportException
- [L277](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L277) `public Bundle[] getBundleArray( String key ){` — 조회·판정, 인접 호출: Game.reportException
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L292) `public Collection<Bundlable> getCollection( String key ) {` — 조회·판정, 인접 호출: Game.reportException
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L309) `public void put( String key, boolean value ) {` — 개별 처리, 인접 호출: Game.reportException
- [L317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L317) `public void put( String key, int value ) {` — 개별 처리, 인접 호출: Game.reportException
- [L325](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L325) `public void put( String key, long value ) {` — 개별 처리, 인접 호출: Game.reportException
- [L333](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L333) `public void put( String key, float value ) {` — 개별 처리, 인접 호출: Game.reportException
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L341) `public void put( String key, String value ) {` — 개별 처리, 인접 호출: Game.reportException
- [L349](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L349) `public void put( String key, Class value ){` — 개별 처리, 인접 호출: Game.reportException
- [L357](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L357) `public void put( String key, Bundle bundle ) {` — 개별 처리, 인접 호출: Game.reportException
- [L365](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L365) `public void put( String key, Bundlable object ) {` — 개별 처리, 인접 호출: Game.reportException
- [L378](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L378) `public void put( String key, Enum<?> value ) {` — 개별 처리, 인접 호출: Game.reportException
- [L388](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L388) `public void put( String key, int[] array ) {` — 개별 처리, 인접 호출: Game.reportException
- [L400](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L400) `public void put( String key, long[] array ) {` — 개별 처리, 인접 호출: Game.reportException
- [L412](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L412) `public void put( String key, float[] array ) {` — 개별 처리, 인접 호출: Game.reportException
- [L424](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L424) `public void put( String key, boolean[] array ) {` — 개별 처리, 인접 호출: Game.reportException, Reflection.isMemberClass, Reflection.isStatic
- [L436](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L436) `public void put( String key, String[] array ) {` — 개별 처리, 인접 호출: Game.reportException, Reflection.isMemberClass, Reflection.isStatic
- [L448](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L448) `public void put( String key, Class[] array ){` — 개별 처리, 인접 호출: Game.reportException, Reflection.isMemberClass, Reflection.isStatic
- [L460](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L460) `public void put( String key, Collection<? extends Bundlable> collection ) {` — 개별 처리, 인접 호출: Reflection.isMemberClass, Reflection.isStatic, Game.reportException
- [L487](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L487) `public static Bundle read( InputStream stream ) throws IOException {` — 개별 처리, 인접 호출: Game.reportException
- [L535](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L535) `public static boolean write( Bundle bundle, OutputStream stream ){` — 개별 처리, 인접 호출: Game.reportException
- [L539](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L539) `public static boolean write( Bundle bundle, OutputStream stream, boolean compressed ) {` — 개별 처리, 인접 호출: Game.reportException
- [L556](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L556) `public static void addAlias( Class<?> cl, String alias ) {` — 개별 처리

## 1307. [`Callback.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Callback.java)

패키지 `com.watabou.utils`, 29행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Callback.java#L24) `public interface Callback {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- 없음

## 1308. [`ColorMath.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/ColorMath.java)

패키지 `com.watabou.utils`, 66행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/ColorMath.java#L24) `public class ColorMath {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/ColorMath.java#L26) `public static int interpolate( int A, int B, float p ) {` — 개별 처리, 인접 호출: Random.Float
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/ColorMath.java#L51) `public static int interpolate( float p,  int... colors ) {` — 개별 처리, 인접 호출: Random.Float
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/ColorMath.java#L61) `public static int random( int a, int b ) {` — 개별 처리, 인접 호출: Random.Float

## 1309. [`DeviceCompat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java)

패키지 `com.watabou.utils`, 74행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java#L31) `public class DeviceCompat {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java#L34) `public static int getPlatformVersion(){` — 조회·판정
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java#L38) `public static boolean isAndroid(){` — 조회·판정
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java#L42) `public static boolean isiOS(){` — 조회·판정
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java#L46) `public static boolean isDesktop(){` — 조회·판정
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java#L50) `public static boolean hasHardKeyboard(){` — 조회·판정
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java#L54) `public static boolean isDebug(){` — 조회·판정
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java#L58) `public static void log( String tag, String message ){` — 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java#L64) `public static float getRealPixelScaleX(){` — 조회·판정
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java#L69) `public static float getRealPixelScaleY(){` — 조회·판정

## 1310. [`FileUtils.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java)

패키지 `com.watabou.utils`, 227행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L35) `public class FileUtils {`

### 변수·상수 후보
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L39) `private static Files.FileType defaultFileType = null;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L40) `private static String defaultPath = "";`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L42) `public static void setDefaultFileProperties( Files.FileType type, String path ){` — 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L47) `public static FileHandle getFileHandle( String name ){` — 조회·판정
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L51) `public static FileHandle getFileHandle( Files.FileType type, String name ){` — 조회·판정
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L55) `public static FileHandle getFileHandle( Files.FileType type, String basePath, String name ){` — 조회·판정
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L75) `public static boolean cleanTempFiles(){` — 개별 처리
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L79) `public static boolean cleanTempFiles( String dirName ){` — 개별 처리
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L120) `public static boolean fileExists( String name ){` — 개별 처리, 인접 호출: Arrays.fill
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L126) `public static long fileLength( String name ){` — 개별 처리, 인접 호출: Arrays.fill
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L135) `public static boolean deleteFile( String name ){` — 개별 처리, 인접 호출: Arrays.fill
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L141) `public static void overwriteFile( String name, int bytes ){` — 개별 처리, 인접 호출: Arrays.fill
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L149) `public static boolean dirExists( String name ){` — 개별 처리, 인접 호출: Bundle.read
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L154) `public static boolean deleteDir( String name ){` — 개별 처리, 인접 호출: Bundle.read
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L164) `public static ArrayList<String> filesInDir( String name ){` — 개별 처리, 인접 호출: Bundle.read
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L178) `public static Bundle bundleFromFile( String fileName ) throws IOException{` — 개별 처리, 인접 호출: Bundle.read, Bundle.write
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L191) `private static Bundle bundleFromStream( InputStream input ) throws IOException{` — 개별 처리, 인접 호출: Bundle.read, Bundle.write
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L200) `public static void bundleToFile( String fileName, Bundle bundle ) throws IOException{` — 개별 처리, 인접 호출: Bundle.write
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java#L221) `private static void bundleToStream( OutputStream output, Bundle bundle ) throws IOException{` — 개별 처리, 인접 호출: Bundle.write

## 1311. [`GameMath.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameMath.java)

패키지 `com.watabou.utils`, 47행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameMath.java#L26) `public class GameMath {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameMath.java#L28) `public static float speed( float speed, float acc ) {` — 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameMath.java#L37) `public static float gate( float min, float value, float max ) {` — 개별 처리

## 1312. [`GameSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java)

패키지 `com.watabou.utils`, 142행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L28) `public class GameSettings {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L30) `public static final String DEFAULT_PREFS_FILE = "settings.xml";`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L32) `private static Preferences prefs;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L34) `private static Preferences get() {` — 조회·판정, 인접 호출: GameMath.gate, Game.reportException
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L42) `public static void set( Preferences prefs ){` — 개별 처리, 인접 호출: GameMath.gate, Game.reportException
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L46) `public static boolean contains( String key ){` — 개별 처리, 인접 호출: GameMath.gate, Game.reportException
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L50) `public static int getInt( String key, int defValue ) {` — 조회·판정, 인접 호출: GameMath.gate, Game.reportException
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L54) `public static int getInt( String key, int defValue, int min, int max ) {` — 조회·판정, 인접 호출: GameMath.gate, Game.reportException
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L71) `public static long getLong( String key, long defValue ) {` — 조회·판정, 인접 호출: GameMath.gate, Game.reportException
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L75) `public static long getLong( String key, long defValue, long min, long max ) {` — 조회·판정, 인접 호출: GameMath.gate, Game.reportException
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L92) `public static boolean getBoolean( String key, boolean defValue ) {` — 조회·판정, 인접 호출: Game.reportException
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L101) `public static String getString( String key, String defValue ) {` — 조회·판정, 인접 호출: Game.reportException
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L105) `public static String getString( String key, String defValue, int maxLength ) {` — 조회·판정, 인접 호출: Game.reportException
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L121) `public static void put( String key, int value ) {` — 개별 처리
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L126) `public static void put( String key, long value ) {` — 개별 처리
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L131) `public static void put( String key, boolean value ) {` — 개별 처리
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java#L136) `public static void put( String key, String value ) {` — 개별 처리

## 1313. [`Graph.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Graph.java)

패키지 `com.watabou.utils`, 108행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Graph.java#L29) `public class Graph {`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Graph.java#L96) `public interface Node {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Graph.java#L31) `public static <T extends Node> void setPrice( List<T> nodes, int value ) {` — 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Graph.java#L37) `public static <T extends Node> void buildDistanceMap( Collection<T> nodes, Node focus ) {` — 생성·초기화
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Graph.java#L64) `public static <T extends Node> List<T> buildPath( Collection<T> nodes, T from, T to ) {` — 생성·초기화

## 1314. [`PathFinder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java)

패키지 `com.watabou.utils`, 418행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L27) `public class PathFinder {`
- [L415](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L415) `public static class Path extends LinkedList<Integer> {`

### 변수·상수 후보
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L29) `public static int[] distance;`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L30) `private static int[] maxVal;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L32) `private static boolean[] goals;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L33) `private static int[] queue;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L36) `private static int size = 0;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L37) `private static int width = 0;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L39) `private static int[] dir;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L40) `private static int[] dirLR;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L44) `public static int[] NEIGHBOURS4;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L45) `public static int[] NEIGHBOURS8;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L46) `public static int[] NEIGHBOURS9;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L50) `public static int[] CIRCLE4;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L51) `public static int[] CIRCLE8;`

### 메서드 및 코드 의존 단서
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L53) `public static void setMapSize( int width, int height ) {` — 개별 처리, 인접 호출: Arrays.fill
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L77) `public static Path find( int from, int to, boolean[] passable ) {` — 조회·판정
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L109) `public static int getStep( int from, int to, boolean[] passable ) {` — 조회·판정, 인접 호출: BArray.setFalse
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L132) `public static int getStepBack( int cur, int from, int lookahead, boolean[] passable, boolean canApproachFromPos ) {` — 조회·판정, 인접 호출: BArray.setFalse, Math.min
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L204) `private static boolean buildDistanceMap( int from, int to, boolean[] passable ) {` — 생성·초기화, 인접 호출: System.arraycopy
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L248) `public static void buildDistanceMap( int to, boolean[] passable, int limit ) {` — 생성·초기화, 인접 호출: System.arraycopy
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L284) `private static boolean buildDistanceMap( int from, boolean[] to, boolean[] passable ) {` — 생성·초기화, 인접 호출: System.arraycopy
- [L334](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L334) `private static int buildEscapeDistanceMap( int cur, int from, int lookAhead, boolean[] passable ) {` — 생성·초기화, 인접 호출: System.arraycopy
- [L382](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java#L382) `public static void buildDistanceMap( int to, boolean[] passable ) {` — 생성·초기화, 인접 호출: System.arraycopy

## 1315. [`PlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java)

패키지 `com.watabou.utils`, 188행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L35) `public abstract class PlatformSupport {`

### 변수·상수 후보
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L89) `protected static HashMap<FreeTypeFontGenerator, HashMap<Integer, BitmapFont>> fonts;`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L91) `protected int pageSize;`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L92) `protected PixmapPacker packer;`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L93) `protected boolean systemfont;`

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L37) `public abstract void updateDisplaySize();` — 행동·상태 갱신, 인접 호출: ControllerHandler.isControllerConnected, ControllerHandler.vibrate
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L39) `public boolean supportsFullScreen(){` — 개별 처리, 인접 호출: ControllerHandler.isControllerConnected, ControllerHandler.vibrate
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L47) `public RectF getSafeInsets( int level ){` — 조회·판정, 인접 호출: ControllerHandler.isControllerConnected, ControllerHandler.vibrate
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L57) `public RectF getDisplayCutout(){` — 조회·판정, 인접 호출: ControllerHandler.isControllerConnected, ControllerHandler.vibrate
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L61) `public abstract void updateSystemUI();` — 행동·상태 갱신, 인접 호출: ControllerHandler.isControllerConnected, ControllerHandler.vibrate
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L63) `public abstract boolean connectedToUnmeteredNetwork();` — 개별 처리, 인접 호출: ControllerHandler.isControllerConnected, ControllerHandler.vibrate
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L65) `public abstract boolean supportsVibration();` — 개별 처리, 인접 호출: ControllerHandler.isControllerConnected, ControllerHandler.vibrate
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L67) `public void vibrate( int millis ){` — 개별 처리, 인접 호출: ControllerHandler.isControllerConnected, ControllerHandler.vibrate
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L75) `public void setHonorSilentSwitch( boolean value ){` — 개별 처리
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L79) `public boolean openURI( String uri ){` — 개별 처리
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L83) `public void setOnscreenKeyboardVisible(boolean value, boolean multiline){` — 개별 처리
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L95) `public abstract void setupFontGenerators(int pageSize, boolean systemFont );` — 생성·초기화
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L97) `protected abstract FreeTypeFontGenerator getGeneratorForString( String input );` — 조회·판정
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L99) `public abstract String[] splitforTextBlock( String text, boolean multiline );` — 개별 처리
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L101) `public void resetGenerators(){` — 개별 처리
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L105) `public void resetGenerators( boolean setupAfter ){` — 개별 처리
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L126) `public void reloadGenerators(){` — 개별 처리, 인접 호출: FreeTypeFontGenerator.FreeTypeFontParameter
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java#L146) `public BitmapFont getFont(int size, String text, boolean flipped, boolean border) {` — 조회·판정, 인접 호출: FreeTypeFontGenerator.FreeTypeFontParameter, Game.reportException

## 1316. [`Point.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java)

패키지 `com.watabou.utils`, 100행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L24) `public class Point {`

### 변수·상수 후보
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L26) `public int x;`
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L27) `public int y;`

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L29) `public Point() {` — 개별 처리
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L32) `public Point( int x, int y ) {` — 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L37) `public Point( Point p ) {` — 개별 처리, 인접 호출: Math.sqrt
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L42) `public Point set( int x, int y ) {` — 개별 처리, 인접 호출: Math.sqrt
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L48) `public Point set( Point p ) {` — 개별 처리, 인접 호출: Math.sqrt
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L54) `public Point clone() {` — 개별 처리, 인접 호출: Math.sqrt
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L58) `public Point scale( float f ) {` — 개별 처리, 인접 호출: Math.sqrt
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L64) `public Point offset( int dx, int dy ) {` — 개별 처리, 인접 호출: Math.sqrt
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L70) `public Point offset( Point d ) {` — 개별 처리, 인접 호출: Math.sqrt
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L76) `public boolean isZero(){` — 조회·판정, 인접 호출: Math.sqrt
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L80) `public float length() {` — 개별 처리, 인접 호출: Math.sqrt
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L84) `public static float distance( Point a, Point b ) {` — 개별 처리, 인접 호출: Math.sqrt
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java#L91) `public boolean equals( Object obj ) {` — 개별 처리

## 1317. [`PointF.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java)

패키지 `com.watabou.utils`, 165행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L24) `public class PointF {`

### 변수·상수 후보
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L26) `public static final float PI	= 3.1415926f;`
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L27) `public static final float PI2	= PI * 2;`
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L28) `public static final float G2R	= PI / 180;`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L30) `public float x;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L31) `public float y;`

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L33) `public PointF() {` — 개별 처리
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L36) `public PointF( float x, float y ) {` — 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L41) `public PointF( PointF p ) {` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L46) `public PointF( Point p ) {` — 개별 처리, 인접 호출: Math.cos, Math.sin
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L51) `public PointF clone() {` — 개별 처리, 인접 호출: Math.cos, Math.sin
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L55) `public PointF scale( float f ) {` — 개별 처리, 인접 호출: Math.cos, Math.sin
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L61) `public PointF invScale( float f ) {` — 개별 처리, 인접 호출: Math.cos, Math.sin
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L67) `public PointF set( float x, float y ) {` — 개별 처리, 인접 호출: Math.cos, Math.sin
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L73) `public PointF set( PointF p ) {` — 개별 처리, 인접 호출: Math.cos, Math.sin
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L79) `public PointF set( float v ) {` — 개별 처리, 인접 호출: Math.cos, Math.sin
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L85) `public PointF polar( float a, float l ) {` — 개별 처리, 인접 호출: Math.cos, Math.sin, Math.sqrt
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L91) `public PointF offset( float dx, float dy ) {` — 개별 처리, 인접 호출: Math.sqrt
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L97) `public PointF offset( PointF p ) {` — 개별 처리, 인접 호출: Math.sqrt
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L103) `public PointF negate() {` — 개별 처리, 인접 호출: Math.sqrt, Math.atan2
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L109) `public PointF normalize() {` — 개별 처리, 인접 호출: Math.sqrt, Math.atan2
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L116) `public Point floor() {` — 개별 처리, 인접 호출: Math.sqrt, Math.atan2
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L120) `public boolean isZero(){` — 조회·판정, 인접 호출: Math.sqrt, Math.atan2
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L124) `public float length() {` — 개별 처리, 인접 호출: Math.sqrt, Math.atan2
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L128) `public static PointF sum( PointF a, PointF b ) {` — 개별 처리, 인접 호출: Math.sqrt, Math.atan2
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L132) `public static PointF diff( PointF a, PointF b ) {` — 개별 처리, 인접 호출: Math.sqrt, Math.atan2
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L136) `public static PointF inter( PointF a, PointF b, float d ) {` — 개별 처리, 인접 호출: Math.sqrt, Math.atan2
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L140) `public static float distance( PointF a, PointF b ) {` — 개별 처리, 인접 호출: Math.sqrt, Math.atan2
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L146) `public static float angle( float x, float y ) {` — 개별 처리, 인접 호출: Math.atan2
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L150) `public static float angle( PointF start, PointF end ) {` — 개별 처리, 인접 호출: Math.atan2
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L154) `public static float angle( Point start, Point end ) {` — 개별 처리, 인접 호출: Math.atan2
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java#L159) `public boolean equals(Object o) {` — 개별 처리


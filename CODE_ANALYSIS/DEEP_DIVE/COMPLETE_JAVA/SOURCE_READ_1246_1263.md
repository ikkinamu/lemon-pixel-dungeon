# Java 소스 구현 분석 1246–1263

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1246. [`SmartTexture.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java)

패키지 `com.watabou.gltextures`, 124행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L28) `public class SmartTexture extends Texture {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L30) `public int width;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L31) `public int height;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L33) `public int fModeMin;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L34) `public int fModeMax;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L36) `public int wModeH;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L37) `public int wModeV;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L39) `public Pixmap bitmap;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L41) `public Atlas atlas;`

### 메서드 및 코드 의존 단서
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L43) `public SmartTexture( Pixmap bitmap ) {` — 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L47) `public SmartTexture( Pixmap bitmap, int filtering, int wrapping, boolean premultiplied ) {` — 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L59) `protected void generate() {` — 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L67) `public void filter(int minMode, int maxMode) {` — 개별 처리
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L75) `public void wrap( int s, int t ) {` — 개별 처리
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L83) `public void bitmap( Pixmap bitmap ) {` — 개별 처리
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L91) `public int getPixel( int x, int y ){` — 조회·판정
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L97) `public void reload() {` — 개별 처리
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L103) `public void delete() {` — 개별 처리
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L112) `public RectF uvRect( float left, float top, float right, float bottom ) {` — 개별 처리
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/SmartTexture.java#L120) `public RectF uvRectBySize(float left, float top, float width, float height){` — 개별 처리

## 1247. [`TextureCache.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java)

패키지 `com.watabou.gltextures`, 180행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java#L31) `public class TextureCache {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java#L36) `final String key = "1x1:" + color;`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java#L58) `final String key = "" + colors;`

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java#L35) `public synchronized static SmartTexture createSolid( int color ) {` — 생성·초기화
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java#L56) `public synchronized static SmartTexture createGradient( int... colors ) {` — 생성·초기화
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java#L84) `public synchronized static SmartTexture create( Object key, int width, int height ) {` — 생성·초기화
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java#L103) `public synchronized static void remove( Object key ){` — 개별 처리
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java#L111) `public synchronized static SmartTexture get( Object src ) {` — 조회·판정
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java#L130) `public synchronized static void clear() {` — 개별 처리, 인접 호출: Game.reportException
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java#L139) `public synchronized static void reload() {` — 개별 처리, 인접 호출: Game.reportException
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java#L145) `public static Pixmap getBitmap( Object src ) {` — 조회·판정, 인접 호출: Game.reportException
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java#L175) `public synchronized static boolean contains( Object key ) {` — 개별 처리

## 1248. [`Attribute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Attribute.java)

패키지 `com.watabou.glwrap`, 56행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Attribute.java#L28) `public class Attribute {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Attribute.java#L30) `private int location;`

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Attribute.java#L32) `public Attribute( int location ) {` — 개별 처리
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Attribute.java#L36) `public int location() {` — 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Attribute.java#L40) `public void enable() {` — 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Attribute.java#L44) `public void disable() {` — 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Attribute.java#L48) `public void vertexPointer( int size, int stride, FloatBuffer ptr ) {` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Attribute.java#L52) `public void vertexBuffer( int size, int stride, int offset) {` — 개별 처리

## 1249. [`Blending.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Blending.java)

패키지 `com.watabou.glwrap`, 52행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Blending.java#L26) `public class Blending {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Blending.java#L28) `public static void useDefault(){` — 이벤트·효과 실행
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Blending.java#L33) `public static void enable(){` — 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Blending.java#L37) `public static void disable(){` — 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Blending.java#L42) `public static void setNormalMode(){` — 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Blending.java#L47) `public static void setLightMode(){` — 개별 처리

## 1250. [`Framebuffer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java)

패키지 `com.watabou.glwrap`, 67행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L26) `public class Framebuffer {`

### 변수·상수 후보
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L28) `public static final int COLOR	= Gdx.gl.GL_COLOR_ATTACHMENT0;`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L29) `public static final int DEPTH	= Gdx.gl.GL_DEPTH_ATTACHMENT;`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L30) `public static final int STENCIL	= Gdx.gl.GL_STENCIL_ATTACHMENT;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L34) `private int id;`

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L32) `public static final Framebuffer	system	= new Framebuffer( 0 );` — 개별 처리
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L36) `public Framebuffer() {` — 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L40) `private Framebuffer( int n ) {` — 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L44) `public void bind() {` — 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L48) `public void delete() {` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L52) `public void attach( int point, Texture tex ) {` — 개별 처리
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L57) `public void attach( int point, Renderbuffer buffer ) {` — 개별 처리
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Framebuffer.java#L62) `public boolean status() {` — 개별 처리

## 1251. [`Matrix.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java)

패키지 `com.watabou.glwrap`, 162행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L24) `public class Matrix {`

### 변수·상수 후보
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L26) `public static final float G2RAD = 0.01745329251994329576923690768489f;`
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L102) `final float ax1 = left[0];`
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L103) `final float ay1 = left[1];`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L104) `final float az1 = left[2];`
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L105) `final float aw1 = left[3];`
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L107) `final float ax2 = left[4];`
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L108) `final float ay2 = left[5];`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L109) `final float az2 = left[6];`
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L110) `final float aw2 = left[7];`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L112) `final float ax3 = left[8];`
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L113) `final float ay3 = left[9];`
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L114) `final float az3 = left[10];`
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L115) `final float aw3 = left[11];`
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L117) `final float ax4 = left[12];`
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L118) `final float ay4 = left[13];`
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L119) `final float az4 = left[14];`
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L120) `final float aw4 = left[15];`
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L122) `final float bx1 = right[0];`
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L123) `final float by1 = right[1];`
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L124) `final float bz1 = right[2];`
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L125) `final float bw1 = right[3];`
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L127) `final float bx2 = right[4];`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L128) `final float by2 = right[5];`
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L129) `final float bz2 = right[6];`
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L130) `final float bw2 = right[7];`
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L132) `final float bx3 = right[8];`
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L133) `final float by3 = right[9];`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L134) `final float bz3 = right[10];`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L135) `final float bw3 = right[11];`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L137) `final float bx4 = right[12];`
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L138) `final float by4 = right[13];`
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L139) `final float bz4 = right[14];`
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L140) `final float bw4 = right[15];`

### 메서드 및 코드 의존 단서
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L28) `public static float[] clone( float[] m ) {` — 개별 처리, 인접 호출: System.arraycopy, Math.sin, Math.cos
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L39) `public static void copy( float[] src, float[] dst ) {` — 개별 처리, 인접 호출: System.arraycopy, Math.sin, Math.cos, Math.tan
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L55) `public static void setIdentity( float[] m ) {` — 개별 처리, 인접 호출: System.arraycopy, Math.sin, Math.cos, Math.tan
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L59) `public static void rotate( float[] m, float a ) {` — 개별 처리, 인접 호출: Math.sin, Math.cos, Math.tan
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L73) `public static void skewX( float[] m, float a ) {` — 개별 처리, 인접 호출: Math.tan
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L79) `public static void skewY( float[] m, float a ) {` — 개별 처리, 인접 호출: Math.tan
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L85) `public static void scale( float[] m, float x, float y ) {` — 개별 처리
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L96) `public static void translate( float[] m, float x, float y ) {` — 개별 처리
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java#L101) `public static void multiply( float[] left, float right[], float[] result ) {` — 개별 처리

## 1252. [`Program.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Program.java)

패키지 `com.watabou.glwrap`, 81행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Program.java#L30) `public class Program {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Program.java#L32) `private int handle;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Program.java#L34) `public Program() {` — 개별 처리, 인접 호출: BufferUtils.newIntBuffer, Game.reportException
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Program.java#L38) `public int handle() {` — 개별 처리, 인접 호출: BufferUtils.newIntBuffer, Game.reportException
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Program.java#L42) `public void attach( Shader shader ) {` — 개별 처리, 인접 호출: BufferUtils.newIntBuffer, Game.reportException
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Program.java#L46) `public void link() {` — 개별 처리, 인접 호출: BufferUtils.newIntBuffer, Game.reportException
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Program.java#L56) `public Attribute attribute( String name ) {` — 개별 처리
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Program.java#L60) `public Uniform uniform( String name ) {` — 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Program.java#L64) `public void use() {` — 이벤트·효과 실행
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Program.java#L68) `public void delete() {` — 개별 처리
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Program.java#L72) `public static Program create( Shader ...shaders ) {` — 생성·초기화

## 1253. [`Quad.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java)

패키지 `com.watabou.glwrap`, 162행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L32) `public class Quad {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L37) `public static final short[] VALUES = {0, 1, 2, 0, 2, 3};`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L39) `public static final int SIZE = VALUES.length;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L41) `private static ShortBuffer indices;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L42) `private static int indexSize = 0;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L43) `private static int bufferIndex = -1;`

### 메서드 및 코드 의존 단서
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L45) `public static FloatBuffer create() {` — 생성·초기화, 인접 호출: ByteOrder.nativeOrder
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L52) `public static FloatBuffer createSet( int size ) {` — 생성·초기화, 인접 호출: ByteOrder.nativeOrder
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L60) `public static void setupIndices(){` — 생성·초기화, 인접 호출: ByteOrder.nativeOrder
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L70) `public static void bindIndices(){` — 개별 처리, 인접 호출: ByteOrder.nativeOrder
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L74) `public static void releaseIndices(){` — 개별 처리, 인접 호출: ByteOrder.nativeOrder
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L78) `public static ShortBuffer getIndices( int size ) {` — 조회·판정, 인접 호출: ByteOrder.nativeOrder
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L132) `public static void fillXY( float[] v, float x1, float x2, float y1, float y2 ) {` — 개별 처리
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Quad.java#L147) `public static void fillUV( float[] v, float u1, float u2, float v1, float v2 ) {` — 개별 처리

## 1254. [`Renderbuffer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Renderbuffer.java)

패키지 `com.watabou.glwrap`, 54행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Renderbuffer.java#L26) `public class Renderbuffer {`

### 변수·상수 후보
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Renderbuffer.java#L29) `public static final int DEPTH16		= Gdx.gl.GL_DEPTH_COMPONENT16;`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Renderbuffer.java#L30) `public static final int STENCIL8	= Gdx.gl.GL_STENCIL_INDEX8;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Renderbuffer.java#L32) `private int id;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Renderbuffer.java#L34) `public Renderbuffer() {` — 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Renderbuffer.java#L38) `public int id() {` — 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Renderbuffer.java#L42) `public void bind() {` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Renderbuffer.java#L46) `public void delete() {` — 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Renderbuffer.java#L50) `public void storage( int format, int width, int height ) {` — 개별 처리

## 1255. [`Shader.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Shader.java)

패키지 `com.watabou.glwrap`, 69행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Shader.java#L29) `public class Shader {`

### 변수·상수 후보
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Shader.java#L31) `public static final int VERTEX		= Gdx.gl.GL_VERTEX_SHADER;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Shader.java#L32) `public static final int FRAGMENT	= Gdx.gl.GL_FRAGMENT_SHADER;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Shader.java#L34) `private int handle;`

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Shader.java#L36) `public Shader( int type ) {` — 개별 처리, 인접 호출: BufferUtils.newIntBuffer
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Shader.java#L40) `public int handle() {` — 개별 처리, 인접 호출: BufferUtils.newIntBuffer
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Shader.java#L44) `public void source( String src ) {` — 개별 처리, 인접 호출: BufferUtils.newIntBuffer
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Shader.java#L48) `public void compile() {` — 개별 처리, 인접 호출: BufferUtils.newIntBuffer
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Shader.java#L58) `public void delete() {` — 개별 처리
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Shader.java#L62) `public static Shader createCompiled( int type, String src ) {` — 생성·초기화

## 1256. [`Texture.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java)

패키지 `com.watabou.glwrap`, 171행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L32) `public class Texture {`

### 변수·상수 후보
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L34) `public static final int NEAREST	= Gdx.gl.GL_NEAREST;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L35) `public static final int LINEAR	= Gdx.gl.GL_LINEAR;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L37) `public static final int REPEAT	= Gdx.gl.GL_REPEAT;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L38) `public static final int MIRROR	= Gdx.gl.GL_MIRRORED_REPEAT;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L39) `public static final int CLAMP	= Gdx.gl.GL_CLAMP_TO_EDGE;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L41) `public int id = -1;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L44) `public boolean premultiplied = false;`

### 메서드 및 코드 의존 단서
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L46) `protected void generate(){` — 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L50) `public static void activate( int index ) {` — 행동·상태 갱신
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L54) `public void bind() {` — 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L64) `public static void clear(){` — 개별 처리
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L68) `public void filter( int minMode, int maxMode ) {` — 개별 처리, 인접 호출: ByteOrder.nativeOrder
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L74) `public void wrap( int s, int t ) {` — 개별 처리, 인접 호출: ByteOrder.nativeOrder
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L80) `public void delete() {` — 개별 처리, 인접 호출: ByteOrder.nativeOrder
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L85) `public void bitmap( Pixmap pixmap ) {` — 개별 처리, 인접 호출: ByteOrder.nativeOrder
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L103) `public void pixels( int w, int h, int[] pixels ) {` — 개별 처리, 인접 호출: ByteOrder.nativeOrder
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L126) `public void pixels( int w, int h, byte[] pixels ) {` — 개별 처리, 인접 호출: ByteOrder.nativeOrder
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L150) `public static Texture create( Pixmap pix ) {` — 생성·초기화
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L157) `public static Texture create( int width, int height, int[] pixels ) {` — 생성·초기화
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Texture.java#L164) `public static Texture create( int width, int height, byte[] pixels ) {` — 생성·초기화

## 1257. [`Uniform.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Uniform.java)

패키지 `com.watabou.glwrap`, 65행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Uniform.java#L26) `public class Uniform {`

### 변수·상수 후보
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Uniform.java#L28) `private int location;`

### 메서드 및 코드 의존 단서
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Uniform.java#L30) `public Uniform(int location) {` — 개별 처리
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Uniform.java#L34) `public int location() {` — 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Uniform.java#L38) `public void enable() {` — 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Uniform.java#L42) `public void disable() {` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Uniform.java#L46) `public void value1f(float value) {` — 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Uniform.java#L50) `public void value2f(float v1, float v2) {` — 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Uniform.java#L54) `public void value4f(float v1, float v2, float v3, float v4) {` — 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Uniform.java#L58) `public void valueM3(float[] value) {` — 개별 처리
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Uniform.java#L62) `public void valueM4(float[] value) {` — 개별 처리

## 1258. [`Vertexbuffer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java)

패키지 `com.watabou.glwrap`, 124행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L30) `public class Vertexbuffer {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L32) `private int id;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L33) `private FloatBuffer vertices;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L34) `private int updateStart, updateEnd;`

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L38) `public Vertexbuffer( FloatBuffer vertices ) {` — 개별 처리, 인접 호출: Math.min, Math.max
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L39) `synchronized (buffers) {` — 개별 처리, 인접 호출: Math.min, Math.max
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L51) `public void updateVertices(){` — 행동·상태 갱신, 인접 호출: Math.min, Math.max
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L56) `public void updateVertices( FloatBuffer vertices ){` — 행동·상태 갱신, 인접 호출: Math.min, Math.max
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L61) `public void updateVertices( FloatBuffer vertices, int start, int end){` — 행동·상태 갱신, 인접 호출: Math.min, Math.max
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L75) `public void updateGLData(){` — 행동·상태 갱신
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L91) `public void bind(){` — 개별 처리
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L95) `public void release(){` — 개별 처리
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L99) `public void delete(){` — 개별 처리
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L100) `synchronized (buffers) {` — 개별 처리
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L106) `public static void clear(){` — 개별 처리
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L107) `synchronized (buffers) {` — 개별 처리
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L114) `public static void reload(){` — 개별 처리
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java#L115) `synchronized (buffers) {` — 개별 처리

## 1259. [`ControllerHandler.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java)

패키지 `com.watabou.input`, 301행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L35) `public class ControllerHandler implements ControllerListener {`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L37) `public enum ControllerType {`

### 변수·상수 후보
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L44) `public static ControllerType lastUsedType = ControllerType.OTHER;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L45) `public static boolean controllerActive = false;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L49) `public static final int CONTROLLER_POINTER_ID = 19;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L63) `private static boolean initialized = false;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L64) `private static boolean failedInit = false;`
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L143) `private float L2Trigger = 0f;`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L144) `private float R2Trigger = 0f;`
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L183) `private static boolean controllerPointerActive = false;`
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L184) `private static PointF controllerPointerPos;`
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L218) `public static int DPAD_KEY_OFFSET = 1000;`

### 메서드 및 코드 의존 단서
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L51) `private static void setControllerType(Controller controller){` — 개별 처리, 인접 호출: Controllers.initialize, Controllers.getCurrent, Game.reportException
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L66) `public static boolean controllersSupported() {` — 개별 처리, 인접 호출: Controllers.initialize, Controllers.getCurrent, Game.reportException
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L86) `public static boolean vibrationSupported(){` — 개별 처리, 인접 호출: Controllers.getCurrent, KeyEvent.addKeyEvent
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L95) `public static void vibrate( int millis ){` — 개별 처리, 인접 호출: Controllers.getCurrent, KeyEvent.addKeyEvent
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L101) `public static boolean isControllerConnected(){` — 조회·판정, 인접 호출: Controllers.getCurrent, KeyEvent.addKeyEvent
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L106) `public void connected(Controller controller) {` — 개별 처리, 인접 호출: KeyEvent.addKeyEvent
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L112) `public void disconnected(Controller controller) {` — 개별 처리, 인접 호출: KeyEvent.addKeyEvent
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L117) `public boolean buttonDown(Controller controller, int buttonCode) {` — 개별 처리, 인접 호출: KeyEvent.addKeyEvent
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L129) `public boolean buttonUp(Controller controller, int buttonCode) {` — 개별 처리, 인접 호출: KeyEvent.addKeyEvent
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L140) `public static PointF leftStickPosition = new PointF();` — 개별 처리, 인접 호출: KeyEvent.addKeyEvent
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L141) `public static PointF rightStickPosition = new PointF();` — 개별 처리, 인접 호출: KeyEvent.addKeyEvent
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L147) `public boolean axisMoved(Controller controller, int axisCode, float value) {` — 개별 처리, 인접 호출: KeyEvent.addKeyEvent
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L186) `public static void setControllerPointer( boolean active ){` — 개별 처리, 인접 호출: PointerEvent.currentHoverPos, Cursor.isCursorCaptured, PointerEvent.addPointerEvent, PointerEvent.setHoverPos
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L199) `public static boolean controllerPointerActive(){` — 개별 처리, 인접 호출: Cursor.isCursorCaptured, PointerEvent.addPointerEvent, PointerEvent.setHoverPos
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L203) `public static PointF getControllerPointerPos(){` — 조회·판정, 인접 호출: PointerEvent.addPointerEvent, PointerEvent.setHoverPos
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L207) `public static void updateControllerPointer(PointF pos, boolean sendEvent){` — 행동·상태 갱신, 인접 호출: PointerEvent.addPointerEvent, PointerEvent.setHoverPos
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L221) `public static int buttonToKey(Controller controller, int btnCode){` — 개별 처리
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L247) `public static boolean icControllerKey(int keyCode){` — 개별 처리, 인접 호출: Keys.toString
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java#L265) `public static String customButtonName(int keyCode){` — 개별 처리, 인접 호출: Keys.toString

## 1260. [`GameAction.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java)

패키지 `com.watabou.input`, 70행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L27) `public class GameAction {`

### 변수·상수 후보
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L31) `private int code;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L32) `private String name;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L34) `protected GameAction( String name ){` — 개별 처리, 인접 호출: ALL_ACTIONS.size, ALL_ACTIONS.add
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L41) `public int code(){` — 개별 처리, 인접 호출: ALL_ACTIONS.size
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L45) `public String name(){` — 개별 처리, 인접 호출: ALL_ACTIONS.size
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L50) `public boolean equals(Object o) {` — 개별 처리, 인접 호출: ALL_ACTIONS.size
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L54) `public static final GameAction NONE = new GameAction( "none" );` — 개별 처리, 인접 호출: ALL_ACTIONS.size
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L55) `public static final GameAction BACK = new GameAction( "back" );` — 개별 처리, 인접 호출: ALL_ACTIONS.size
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L57) `public static final GameAction LEFT_CLICK   = new GameAction( "left_click" );` — 개별 처리, 인접 호출: ALL_ACTIONS.size
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L58) `public static final GameAction RIGHT_CLICK  = new GameAction( "right_click" );` — 개별 처리, 인접 호출: ALL_ACTIONS.size
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L59) `public static final GameAction MIDDLE_CLICK = new GameAction( "middle_click" );` — 개별 처리, 인접 호출: ALL_ACTIONS.size
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L61) `public static ArrayList<GameAction> allActions(){` — 개별 처리, 인접 호출: ALL_ACTIONS.size
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java#L65) `public static int totalActions(){` — 개별 처리, 인접 호출: ALL_ACTIONS.size

## 1261. [`InputHandler.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java)

패키지 `com.watabou.input`, 168행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L31) `public class InputHandler extends InputAdapter {`

### 변수·상수 후보
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L33) `private InputMultiplexer multiplexer;`

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L35) `public InputHandler( Input input ){` — 개별 처리, 인접 호출: PointerEvent.currentHoverPos, PointerEvent.processPointerEvents, KeyEvent.processKeyEvents, ScrollEvent.processScrollEvents
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L43) `public void addInputProcessor(InputProcessor processor){` — 개별 처리, 인접 호출: PointerEvent.currentHoverPos, PointerEvent.processPointerEvents, KeyEvent.processKeyEvents, ScrollEvent.processScrollEvents, ControllerHandler.setControllerPointer, KeyBindings.isKeyBound, KeyEvent.addKeyEvent
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L47) `public void removeInputProcessor(InputProcessor processor){` — 개별 처리, 인접 호출: PointerEvent.currentHoverPos, PointerEvent.processPointerEvents, KeyEvent.processKeyEvents, ScrollEvent.processScrollEvents, ControllerHandler.setControllerPointer, KeyBindings.isKeyBound, KeyEvent.addKeyEvent
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L51) `public void emulateTouch(int id, int button, boolean down){` — 개별 처리, 인접 호출: PointerEvent.currentHoverPos, PointerEvent.processPointerEvents, KeyEvent.processKeyEvents, ScrollEvent.processScrollEvents, ControllerHandler.setControllerPointer, KeyBindings.isKeyBound, KeyEvent.addKeyEvent
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L60) `public void emulateDrag(int id){` — 개별 처리, 인접 호출: PointerEvent.currentHoverPos, PointerEvent.processPointerEvents, KeyEvent.processKeyEvents, ScrollEvent.processScrollEvents, ControllerHandler.setControllerPointer, KeyBindings.isKeyBound, KeyEvent.addKeyEvent
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L65) `public void processAllEvents(){` — 행동·상태 갱신, 인접 호출: PointerEvent.processPointerEvents, KeyEvent.processKeyEvents, ScrollEvent.processScrollEvents, ControllerHandler.setControllerPointer, KeyBindings.isKeyBound, KeyEvent.addKeyEvent, PointerEvent.addPointerEvent
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L76) `public synchronized boolean touchDown(int screenX, int screenY, int pointer, int button) {` — 개별 처리, 인접 호출: ControllerHandler.setControllerPointer, KeyBindings.isKeyBound, KeyEvent.addKeyEvent, PointerEvent.addPointerEvent, PointerEvent.addIfExisting
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L95) `public synchronized boolean touchUp(int screenX, int screenY, int pointer, int button) {` — 개별 처리, 인접 호출: KeyBindings.isKeyBound, KeyEvent.addKeyEvent, PointerEvent.addPointerEvent, PointerEvent.addIfExisting, ControllerHandler.controllerPointerActive, ControllerHandler.setControllerPointer, ControllerHandler.getControllerPointerPos
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L106) `public boolean touchCancelled(int screenX, int screenY, int pointer, int button) {` — 개별 처리, 인접 호출: KeyBindings.isKeyBound, KeyEvent.addKeyEvent, PointerEvent.addPointerEvent, PointerEvent.addIfExisting, ControllerHandler.controllerPointerActive, ControllerHandler.setControllerPointer, ControllerHandler.getControllerPointerPos
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L117) `public synchronized boolean touchDragged(int screenX, int screenY, int pointer) {` — 개별 처리, 인접 호출: PointerEvent.addIfExisting, ControllerHandler.controllerPointerActive, ControllerHandler.setControllerPointer, ControllerHandler.getControllerPointerPos, PointerEvent.addPointerEvent, KeyBindings.isKeyBound, KeyEvent.addKeyEvent
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L123) `public boolean mouseMoved(int screenX, int screenY) {` — 개별 처리, 인접 호출: ControllerHandler.controllerPointerActive, ControllerHandler.setControllerPointer, ControllerHandler.getControllerPointerPos, PointerEvent.addPointerEvent, KeyBindings.isKeyBound, KeyEvent.addKeyEvent, ScrollEvent.addScrollEvent
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L139) `public synchronized boolean keyDown( int keyCode ) {` — 개별 처리, 인접 호출: KeyBindings.isKeyBound, KeyEvent.addKeyEvent, ScrollEvent.addScrollEvent, PointerEvent.currentHoverPos
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L149) `public synchronized boolean keyUp( int keyCode ) {` — 개별 처리, 인접 호출: KeyBindings.isKeyBound, KeyEvent.addKeyEvent, ScrollEvent.addScrollEvent, PointerEvent.currentHoverPos
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java#L163) `public boolean scrolled(float amountX, float amountY) {` — 개별 처리, 인접 호출: ScrollEvent.addScrollEvent, PointerEvent.currentHoverPos

## 1262. [`KeyBindings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java)

패키지 `com.watabou.input`, 142행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L31) `public class KeyBindings {`

### 변수·상수 후보
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L62) `public static boolean bindingKey = false;`

### 메서드 및 코드 의존 단서
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L39) `public static LinkedHashMap<Integer, GameAction> getAllBindings(){` — 조회·판정
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L43) `public static void setAllBindings(LinkedHashMap<Integer, GameAction> newBindings){` — 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L47) `public static LinkedHashMap<Integer, GameAction> getAllControllerBindings(){` — 조회·판정
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L51) `public static void setAllControllerBindings(LinkedHashMap<Integer, GameAction> newBindings){` — 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L58) `public static void addHardBinding(int keyCode, GameAction action){` — 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L64) `public static boolean isKeyBound(int keyCode){` — 조회·판정
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L74) `public static GameAction getActionForKey(KeyEvent event){` — 조회·판정, 인접 호출: ControllerHandler.customButtonName
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L85) `public static int getFirstKeyForAction(GameAction action, boolean preferController){` — 조회·판정, 인접 호출: ControllerHandler.customButtonName
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L96) `public static ArrayList<Integer> getKeyboardKeysForAction(GameAction action){` — 조회·판정, 인접 호출: ControllerHandler.customButtonName, Keys.toString
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L106) `public static ArrayList<Integer> getControllerKeysForAction(GameAction action){` — 조회·판정, 인접 호출: ControllerHandler.customButtonName, Keys.toString
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java#L116) `public static String getKeyName( int keyCode ){` — 조회·판정, 인접 호출: ControllerHandler.customButtonName, Keys.toString

## 1263. [`KeyEvent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyEvent.java)

패키지 `com.watabou.input`, 90행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyEvent.java#L29) `public class KeyEvent {`

### 변수·상수 후보
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyEvent.java#L31) `public int code;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyEvent.java#L32) `public boolean pressed;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyEvent.java#L34) `public KeyEvent( int code, boolean pressed ) {` — 개별 처리, 인접 호출: KeyBindings.getActionForKey
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyEvent.java#L45) `public static void addKeyListener( Signal.Listener<KeyEvent> listener ){` — 개별 처리, 인접 호출: KeyBindings.getActionForKey, ControllerHandler.icControllerKey
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyEvent.java#L49) `public static void removeKeyListener( Signal.Listener<KeyEvent> listener ){` — 개별 처리, 인접 호출: KeyBindings.getActionForKey, ControllerHandler.icControllerKey
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyEvent.java#L53) `public static void clearListeners(){` — 개별 처리, 인접 호출: KeyBindings.getActionForKey, ControllerHandler.icControllerKey
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyEvent.java#L60) `public static synchronized void addKeyEvent( KeyEvent event ){` — 개별 처리, 인접 호출: KeyBindings.getActionForKey, ControllerHandler.icControllerKey
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyEvent.java#L64) `public static synchronized void processKeyEvents(){` — 행동·상태 갱신, 인접 호출: KeyBindings.getActionForKey, ControllerHandler.icControllerKey
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyEvent.java#L86) `public static boolean isKeyboardKey(int keyCode){` — 조회·판정, 인접 호출: ControllerHandler.icControllerKey


# Java 소스 구현 분석 1282–1299

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1282. [`PixelParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/PixelParticle.java)

패키지 `com.watabou.noosa.particles`, 69행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/PixelParticle.java#L27) `public class PixelParticle extends PseudoPixel {`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/PixelParticle.java#L61) `public static class Shrinking extends PixelParticle {`

### 변수·상수 후보
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/PixelParticle.java#L29) `protected float size;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/PixelParticle.java#L31) `protected float lifespan;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/PixelParticle.java#L32) `protected float left;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/PixelParticle.java#L34) `public PixelParticle() {` — 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/PixelParticle.java#L40) `public void reset( float x, float y, int color, float size, float lifespan ) {` — 개별 처리
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/PixelParticle.java#L53) `public void update() {` — 행동·상태 갱신
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/PixelParticle.java#L63) `public void update() {` — 행동·상태 갱신

## 1283. [`PointerArea.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java)

패키지 `com.watabou.noosa`, 155행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L27) `public class PointerArea extends Visual implements Signal.Listener<PointerEvent> {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L30) `public Visual target;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L32) `protected PointerEvent curEvent = null;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L33) `protected boolean hovered = false;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L35) `public int blockLevel = BLOCK_WHEN_ACTIVE;`

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L37) `public static final int BLOCK_WHEN_ACTIVE = 1;  //Only block when active (default)` — 행동·상태 갱신, 인접 호출: PointerEvent.addPointerListener
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L38) `public static final int NEVER_BLOCK = 2;        //Never block (handy for buttons in scroll areas)` — 개별 처리, 인접 호출: PointerEvent.addPointerListener
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L40) `public PointerArea( Visual target ) {` — 개별 처리, 인접 호출: PointerEvent.addPointerListener
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L47) `public PointerArea( float x, float y, float width, float height ) {` — 개별 처리, 인접 호출: PointerEvent.addPointerListener
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L57) `public boolean onSignal( PointerEvent event ) {` — 이벤트·효과 실행
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L127) `protected void onPointerDown( PointerEvent event ) { }` — 이벤트·효과 실행, 인접 호출: PointerEvent.removePointerListener, PointerEvent.addPointerListener
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L129) `protected void onPointerUp( PointerEvent event) { }` — 이벤트·효과 실행, 인접 호출: PointerEvent.removePointerListener, PointerEvent.addPointerListener
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L131) `protected void onClick( PointerEvent event ) { }` — 이벤트·효과 실행, 인접 호출: PointerEvent.removePointerListener, PointerEvent.addPointerListener
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L133) `protected void onDrag( PointerEvent event ) { }` — 이벤트·효과 실행, 인접 호출: PointerEvent.removePointerListener, PointerEvent.addPointerListener
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L135) `protected void onHoverStart( PointerEvent event ) { }` — 이벤트·효과 실행, 인접 호출: PointerEvent.removePointerListener, PointerEvent.addPointerListener
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L137) `protected void onHoverEnd( PointerEvent event ) { }` — 이벤트·효과 실행, 인접 호출: PointerEvent.removePointerListener, PointerEvent.addPointerListener
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L139) `public void reset() {` — 개별 처리, 인접 호출: PointerEvent.removePointerListener, PointerEvent.addPointerListener
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L144) `public void givePointerPriority(){` — 개별 처리, 인접 호출: PointerEvent.removePointerListener, PointerEvent.addPointerListener
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java#L150) `public void destroy() {` — 개별 처리, 인접 호출: PointerEvent.removePointerListener

## 1284. [`PseudoPixel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PseudoPixel.java)

패키지 `com.watabou.noosa`, 49행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PseudoPixel.java#L26) `public class PseudoPixel extends Image {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PseudoPixel.java#L28) `public PseudoPixel() {` — 개별 처리, 인접 호출: TextureCache.createSolid
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PseudoPixel.java#L32) `public PseudoPixel( float x, float y, int color ) {` — 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PseudoPixel.java#L41) `public void size( float w, float h ) {` — 개별 처리
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PseudoPixel.java#L45) `public void size( float value ) {` — 개별 처리

## 1285. [`RenderedText.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java)

패키지 `com.watabou.noosa`, 263행.

### 클래스/타입
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L41) `public class RenderedText extends Image {`
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L155) `private static class TextRenderBatch implements Batch {`

### 변수·상수 후보
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L43) `private BitmapFont font = null;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L44) `private int size;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L45) `private String text;`
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L130) `private float renderedHeight = 0;`
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L159) `private static RenderedText textBeingRendered = null;`
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L160) `private static float[] vertices = new float[16];`

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L47) `public RenderedText( ) {` — 개별 처리, 인접 호출: Thread.currentThread
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L51) `public RenderedText( int size ){` — 개별 처리, 인접 호출: Thread.currentThread
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L56) `public RenderedText(String text, int size){` — 개별 처리, 인접 호출: Thread.currentThread
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L63) `public void text( String text ){` — 개별 처리, 인접 호출: Thread.currentThread
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L69) `public String text(){` — 개별 처리, 인접 호출: Thread.currentThread, Game.reportException
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L73) `public void size( int size ){` — 개별 처리, 인접 호출: Thread.currentThread, Game.reportException
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L80) `private synchronized void measure(){` — 개별 처리, 인접 호출: Thread.currentThread, Game.reportException
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L133) `protected void updateMatrix() {` — 행동·상태 갱신, 인접 호출: Matrix.translate, Math.round, Quad.createSet
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L141) `private static TextRenderBatch textRenderer = new TextRenderBatch();` — 개별 처리, 인접 호출: Quad.createSet
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L144) `public synchronized void draw() {` — 개별 처리, 인접 호출: Quad.createSet
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L164) `public void draw(Texture texture, float[] spriteVertices, int offset, int count) {` — 개별 처리, 인접 호출: Quad.createSet, NoosaScript.get
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L225) `public void begin() { }` — 개별 처리
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L226) `public void end() { }` — 개별 처리
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L227) `public void setColor(Color tint) { }` — 개별 처리
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L228) `public void setColor(float r, float g, float b, float a) { }` — 개별 처리
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L229) `public Color getColor() { return null; }` — 조회·판정
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L230) `public void setPackedColor(float packedColor) { }` — 개별 처리
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L231) `public float getPackedColor() { return 0; }` — 조회·판정
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L232) `public void draw(Texture texture, float x, float y, float originX, float originY, float width, float height, float scaleX, float scaleY` — 개별 처리
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L233) `public void draw(Texture texture, float x, float y, float width, float height, int srcX, int srcY, int srcWidth, int srcHeight, boolean` — 개별 처리
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L234) `public void draw(Texture texture, float x, float y, int srcX, int srcY, int srcWidth, int srcHeight) { }` — 개별 처리
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L235) `public void draw(Texture texture, float x, float y, float width, float height, float u, float v, float u2, float v2) { }` — 개별 처리
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L236) `public void draw(Texture texture, float x, float y) { }` — 개별 처리
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L237) `public void draw(Texture texture, float x, float y, float width, float height) { }` — 개별 처리
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L238) `public void draw(TextureRegion region, float x, float y) { }` — 개별 처리
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L239) `public void draw(TextureRegion region, float x, float y, float width, float height) { }` — 개별 처리
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L240) `public void draw(TextureRegion region, float x, float y, float originX, float originY, float width, float height, float scaleX, float s` — 개별 처리
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L241) `public void draw(TextureRegion region, float x, float y, float originX, float originY, float width, float height, float scaleX, float s` — 개별 처리
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L242) `public void draw(TextureRegion region, float width, float height, Affine2 transform) { }` — 개별 처리
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L243) `public void flush() { }` — 개별 처리
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L244) `public void disableBlending() { }` — 개별 처리
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L245) `public void enableBlending() { }` — 개별 처리
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L246) `public void setBlendFunction(int srcFunc, int dstFunc) { }` — 개별 처리
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L247) `public void setBlendFunctionSeparate(int srcFuncColor, int dstFuncColor, int srcFuncAlpha, int dstFuncAlpha) { }` — 개별 처리
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L248) `public int getBlendSrcFunc() { return 0; }` — 조회·판정
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L249) `public int getBlendDstFunc() { return 0; }` — 조회·판정
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L250) `public int getBlendSrcFuncAlpha() { return 0; }` — 조회·판정
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L251) `public int getBlendDstFuncAlpha() { return 0; }` — 조회·판정
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L252) `public Matrix4 getProjectionMatrix() { return null; }` — 조회·판정
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L253) `public Matrix4 getTransformMatrix() { return null; }` — 조회·판정
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L254) `public void setProjectionMatrix(Matrix4 projection) { }` — 개별 처리
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L255) `public void setTransformMatrix(Matrix4 transform) { }` — 개별 처리
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L256) `public void setShader(ShaderProgram shader) { }` — 개별 처리
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L257) `public ShaderProgram getShader() { return null; }` — 조회·판정
- [L258](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L258) `public boolean isBlendingEnabled() { return false; }` — 조회·판정
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L259) `public boolean isDrawing() { return false; }` — 조회·판정
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/RenderedText.java#L260) `public void dispose() { }` — 개별 처리

## 1286. [`Resizable.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Resizable.java)

패키지 `com.watabou.noosa`, 31행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Resizable.java#L24) `public interface Resizable {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Resizable.java#L26) `public void size( float width, float height );` — 개별 처리
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Resizable.java#L27) `public float width();` — 개별 처리
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Resizable.java#L28) `public float height();` — 개별 처리

## 1287. [`Scene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java)

패키지 `com.watabou.noosa`, 76행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java#L29) `public class Scene extends Group {`

### 변수·상수 후보
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java#L31) `private Signal.Listener<KeyEvent> keyListener;`

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java#L33) `public void create() {` — 생성·초기화, 인접 호출: KeyEvent.addKeyListener, KeyBindings.getActionForKey, KeyEvent.removeKeyListener
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java#L36) `public boolean onSignal( KeyEvent event ) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getActionForKey, KeyEvent.removeKeyListener
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java#L48) `public void destroy() {` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java#L53) `public void onPause() {` — 이벤트·효과 실행
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java#L57) `public void onResume(){` — 이벤트·효과 실행
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java#L62) `public void update() {` — 행동·상태 갱신
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java#L67) `public Camera camera() {` — 개별 처리
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java#L71) `protected void onBackPressed() {` — 이벤트·효과 실행

## 1288. [`ScrollArea.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ScrollArea.java)

패키지 `com.watabou.noosa`, 66행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ScrollArea.java#L28) `public class ScrollArea extends PointerArea {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ScrollArea.java#L30) `public ScrollArea( Visual target ){` — 개별 처리, 인접 호출: ScrollEvent.addScrollListener, ScrollEvent.removeScrollListener
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ScrollArea.java#L35) `public ScrollArea(float x, float y, float width, float height ) {` — 개별 처리, 인접 호출: ScrollEvent.addScrollListener, ScrollEvent.removeScrollListener
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ScrollArea.java#L42) `public boolean onSignal(ScrollEvent event) {` — 이벤트·효과 실행, 인접 호출: ScrollEvent.removeScrollListener
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ScrollArea.java#L58) `protected void onScroll( ScrollEvent event ){ }` — 이벤트·효과 실행, 인접 호출: ScrollEvent.removeScrollListener
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ScrollArea.java#L61) `public void destroy() {` — 개별 처리, 인접 호출: ScrollEvent.removeScrollListener

## 1289. [`SkinnedBlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java)

패키지 `com.watabou.noosa`, 130행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L27) `public class SkinnedBlock extends Image {`

### 변수·상수 후보
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L29) `protected float scaleX;`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L30) `protected float scaleY;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L32) `protected float offsetX;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L33) `protected float offsetY;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L35) `public boolean autoAdjust = false;`

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L37) `public SkinnedBlock( float width, float height, Object tx ) {` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L46) `public void frame( RectF frame ) {` — 개별 처리
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L57) `protected void updateFrame() {` — 행동·상태 갱신
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L97) `public void offsetTo( float x, float y ) {` — 개별 처리
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L103) `public void offset( float x, float y ) {` — 개별 처리
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L109) `public float offsetX() {` — 개별 처리
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L113) `public float offsetY() {` — 개별 처리
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L117) `public void scale( float x, float y ) {` — 개별 처리
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java#L123) `public void size( float w, float h ) {` — 개별 처리

## 1290. [`TextInput.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java)

패키지 `com.watabou.noosa`, 266행.

### 클래스/타입
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L49) `public class TextInput extends Component {`

### 변수·상수 후보
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L51) `private Stage stage;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L52) `private Container container;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L53) `private TextField textField;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L55) `private Skin skin;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L57) `private NinePatch bg;`

### 메서드 및 코드 의존 단서
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L59) `public TextInput( NinePatch bg, boolean multiline, int size ){` — 개별 처리, 인접 호출: FileUtils.getFileHandle
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L87) `public void cut() {` — 개별 처리, 인접 호출: TextField.TextFieldListener
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L93) `public void copy() {` — 개별 처리, 인접 호출: TextField.TextFieldListener
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L101) `public void cut() {` — 개별 처리, 인접 호출: TextField.TextFieldListener, TextField.OnscreenKeyboard
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L107) `public void copy() {` — 개별 처리, 인접 호출: TextField.TextFieldListener, TextField.OnscreenKeyboard
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L119) `public void changed(ChangeEvent event, Actor actor) {` — 개별 처리, 인접 호출: TextField.TextFieldListener, TextField.OnscreenKeyboard
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L132) `public void keyTyped (TextField textField, char c){` — 개별 처리, 인접 호출: TextField.OnscreenKeyboard
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L143) `public void show(boolean visible) {` — 개별 처리
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L153) `public void enterPressed(){` — 개별 처리
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L157) `public void onChanged(){` — 이벤트·효과 실행
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L161) `public void onClipBoardUpdate(){` — 이벤트·효과 실행
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L165) `public void setText(String text){` — 개별 처리
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L170) `public void setMaxLength(int maxLength){` — 개별 처리
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L174) `public String getText(){` — 조회·판정
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L178) `public void copyToClipboard(){` — 개별 처리
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L186) `public void pasteFromClipboard(){` — 개별 처리
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L204) `protected void layout() {` — 개별 처리, 인접 호출: Quad.releaseIndices, Script.unuse, Texture.clear
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L238) `public void update() {` — 행동·상태 갱신, 인접 호출: Quad.releaseIndices, Script.unuse, Texture.clear, Quad.bindIndices, Blending.useDefault, DeviceCompat.isDesktop
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L244) `public void draw() {` — 개별 처리, 인접 호출: Quad.releaseIndices, Script.unuse, Texture.clear, Quad.bindIndices, Blending.useDefault, DeviceCompat.isDesktop
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextInput.java#L255) `public synchronized void destroy() {` — 개별 처리, 인접 호출: DeviceCompat.isDesktop

## 1291. [`TextureFilm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java)

패키지 `com.watabou.noosa`, 146행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L30) `public class TextureFilm {`

### 변수·상수 후보
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L34) `private int texWidth;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L35) `private int texHeight;`

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L32) `private static final RectF FULL = new RectF( 0, 0, 1, 1 );` — 개별 처리, 인접 호출: TextureCache.get
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L39) `public TextureFilm( Object tx ) {` — 개별 처리, 인접 호출: TextureCache.get
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L49) `public TextureFilm( SmartTexture texture, int width ) {` — 개별 처리, 인접 호출: TextureCache.get
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L53) `public TextureFilm( Object tx, int width, int height ) {` — 개별 처리, 인접 호출: TextureCache.get
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L73) `public TextureFilm( TextureFilm atlas, Object key, int width, int height ) {` — 개별 처리
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L95) `public TextureFilm( int txWidth, int txHeight, int width, int height){` — 개별 처리
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L114) `public void add( Object id, RectF rect ) {` — 개별 처리
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L118) `public void add( Object id, float left, float top, float right, float bottom){` — 개별 처리
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L127) `public RectF get( Object id ) {` — 조회·판정
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L131) `public float width( Object id ){` — 개별 처리
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L135) `public float width( RectF frame ) {` — 개별 처리
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L139) `public float height( Object id ){` — 개별 처리
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java#L143) `public float height( RectF frame ) {` — 개별 처리

## 1292. [`Tilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java)

패키지 `com.watabou.noosa`, 249행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L35) `public class Tilemap extends Visual {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L37) `protected SmartTexture texture;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L38) `protected TextureFilm tileset;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L40) `protected int[] data;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L41) `protected int mapWidth;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L42) `protected int mapHeight;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L43) `protected int size;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L45) `private float cellW;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L46) `private float cellH;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L48) `protected float[] vertices;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L49) `protected FloatBuffer quads;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L50) `protected Vertexbuffer buffer;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L52) `private volatile Rect updated;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L53) `private boolean fullUpdate;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L54) `private Rect updating;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L55) `private int topLeftUpdating;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L56) `private int bottomRightUpdating;`

### 메서드 및 코드 의존 단서
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L58) `public Tilemap( Object tx, TextureFilm tileset ) {` — 개별 처리, 인접 호출: TextureCache.get, Quad.createSet
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L74) `public void map( int[] data, int cols ) {` — 개별 처리, 인접 호출: Quad.createSet
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L90) `public Image image(int x, int y){` — 개별 처리
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L101) `public synchronized void updateMap(){` — 행동·상태 갱신
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L106) `public synchronized void updateMapCell(int cell){` — 행동·상태 갱신
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L110) `private synchronized void moveToUpdating(){` — 개별 처리
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L115) `protected void updateVertices() {` — 행동·상태 갱신
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L197) `public void draw() {` — 개별 처리, 인접 호출: NoosaScriptNoLighting.get
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L234) `protected NoosaScript script(){` — 개별 처리, 인접 호출: NoosaScriptNoLighting.get
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L239) `public void destroy() {` — 개별 처리
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java#L245) `protected boolean needsRender(int pos){` — 개별 처리

## 1293. [`AlphaTweener.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/AlphaTweener.java)

패키지 `com.watabou.noosa.tweeners`, 46행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/AlphaTweener.java#L26) `public class AlphaTweener extends Tweener {`

### 변수·상수 후보
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/AlphaTweener.java#L28) `public Visual image;`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/AlphaTweener.java#L30) `public float start;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/AlphaTweener.java#L31) `public float delta;`

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/AlphaTweener.java#L33) `public AlphaTweener( Visual image, float alpha, float time ) {` — 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/AlphaTweener.java#L42) `protected void updateValues( float progress ) {` — 행동·상태 갱신

## 1294. [`CameraScrollTweener.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/CameraScrollTweener.java)

패키지 `com.watabou.noosa.tweeners`, 47행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/CameraScrollTweener.java#L27) `public class CameraScrollTweener extends Tweener {`

### 변수·상수 후보
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/CameraScrollTweener.java#L29) `public Camera camera;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/CameraScrollTweener.java#L31) `public PointF start;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/CameraScrollTweener.java#L32) `public PointF end;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/CameraScrollTweener.java#L34) `public CameraScrollTweener( Camera camera, PointF pos, float time ) {` — 개별 처리, 인접 호출: PointF.inter
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/CameraScrollTweener.java#L43) `protected void updateValues( float progress ) {` — 행동·상태 갱신, 인접 호출: PointF.inter

## 1295. [`Delayer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Delayer.java)

패키지 `com.watabou.noosa.tweeners`, 38행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Delayer.java#L24) `public class Delayer extends Tweener {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Delayer.java#L26) `public Delayer() {` — 개별 처리
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Delayer.java#L30) `public Delayer( float time ) {` — 개별 처리
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Delayer.java#L35) `protected void updateValues( float progress ) {` — 행동·상태 갱신

## 1296. [`PosTweener.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/PosTweener.java)

패키지 `com.watabou.noosa.tweeners`, 47행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/PosTweener.java#L27) `public class PosTweener extends Tweener {`

### 변수·상수 후보
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/PosTweener.java#L29) `public Visual visual;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/PosTweener.java#L31) `public PointF start;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/PosTweener.java#L32) `public PointF end;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/PosTweener.java#L34) `public PosTweener( Visual visual, PointF pos, float time ) {` — 개별 처리, 인접 호출: PointF.inter
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/PosTweener.java#L43) `protected void updateValues( float progress ) {` — 행동·상태 갱신, 인접 호출: PointF.inter

## 1297. [`ScaleTweener.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/ScaleTweener.java)

패키지 `com.watabou.noosa.tweeners`, 47행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/ScaleTweener.java#L27) `public class ScaleTweener extends Tweener {`

### 변수·상수 후보
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/ScaleTweener.java#L29) `public Visual visual;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/ScaleTweener.java#L31) `public PointF start;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/ScaleTweener.java#L32) `public PointF end;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/ScaleTweener.java#L34) `public ScaleTweener( Visual visual, PointF scale, float time ) {` — 개별 처리, 인접 호출: PointF.inter
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/ScaleTweener.java#L43) `protected void updateValues( float progress ) {` — 행동·상태 갱신, 인접 호출: PointF.inter

## 1298. [`Tweener.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java)

패키지 `com.watabou.noosa.tweeners`, 85행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java#L27) `abstract public class Tweener extends Gizmo {`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java#L81) `public static interface Listener {`

### 변수·상수 후보
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java#L29) `public Gizmo target;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java#L31) `public float interval;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java#L32) `public float elapsed;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java#L34) `public Listener listener;`

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java#L36) `public Tweener( Gizmo target, float interval ) {` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java#L46) `public void update() {` — 행동·상태 갱신
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java#L69) `public void stop( boolean complete ){` — 개별 처리
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java#L73) `protected void onComplete() {` — 이벤트·효과 실행
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java#L79) `abstract protected void updateValues( float progress );` — 행동·상태 갱신

## 1299. [`Component.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java)

패키지 `com.watabou.noosa.ui`, 110행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L26) `public class Component extends Group {`

### 변수·상수 후보
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L28) `protected float x;`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L29) `protected float y;`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L30) `protected float width;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L31) `protected float height;`

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L33) `public Component() {` — 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L38) `public Component setPos( float x, float y ) {` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L46) `public Component setSize( float width, float height ) {` — 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L54) `public Component setRect( float x, float y, float width, float height ) {` — 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L64) `public boolean inside( float x, float y ) {` — 개별 처리
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L68) `public void fill( Component c ) {` — 개별 처리
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L72) `public float left() {` — 개별 처리
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L76) `public float right() {` — 개별 처리
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L80) `public float centerX() {` — 개별 처리
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L84) `public float top() {` — 개별 처리
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L88) `public float bottom() {` — 개별 처리
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L92) `public float centerY() {` — 개별 처리
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L96) `public float width() {` — 개별 처리
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L100) `public float height() {` — 개별 처리
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L104) `protected void createChildren() {` — 생성·초기화
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java#L107) `protected void layout() {` — 개별 처리


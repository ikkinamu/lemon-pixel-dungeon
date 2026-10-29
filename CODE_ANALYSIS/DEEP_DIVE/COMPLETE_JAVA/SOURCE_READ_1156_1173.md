# Java 소스 구현 분석 1156–1173

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1156. [`ScrollingListPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 205행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L32) `public class ScrollingListPane extends ScrollPane {`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L87) `public static class ListItem extends Component {`
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L167) `public static class ListTitle extends Component {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L36) `private static final int ITEM_HEIGHT	= 18;`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L89) `protected Image icon;`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L90) `protected BitmapText iconLabel;`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L91) `protected RenderedTextBlock label;`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L92) `protected ColorBlock line;`
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L169) `protected RenderedTextBlock label;`
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L170) `protected ColorBlock line;`

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L38) `public ScrollingListPane(){` — 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L43) `public void onClick(float x, float y) {` — 이벤트·효과 실행
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L51) `public void addItem( Image icon, String iconText, String text ){` — 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L55) `public void addItem( ListItem item ){` — 개별 처리
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L61) `public void addTitle( String text ){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L69) `public synchronized void clear() {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L75) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L94) `public ListItem( Image icon, String text ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L98) `public ListItem( Image icon, String iconText, String text ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L117) `public boolean onClick( float x, float y ){` — 이벤트·효과 실행, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L121) `public void hardlight( int color ){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L126) `public void hardlightIcon( int color ){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L131) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L147) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, PixelScene.renderTextBlock
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L172) `public ListTitle (String title){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L178) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingListPane.java#L189) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align

## 1157. [`ScrollPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 240행.

### 클래스/타입
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L41) `public class ScrollPane extends Component {`
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L164) `public class PointerController extends ScrollArea {`

### 변수·상수 후보
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L43) `protected static final int THUMB_COLOR		= 0xFF7b8073;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L44) `protected static final float THUMB_ALPHA	= 0.5f;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L46) `protected PointerController controller;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L47) `protected Signal.Listener<KeyEvent> keyListener;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L48) `protected Component content;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L49) `protected ColorBlock thumb;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L51) `private float keyScroll = 0;`
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L166) `private float dragThreshold;`
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L196) `private boolean dragging = false;`

### 메서드 및 코드 의존 단서
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L53) `public ScrollPane( Component content ) {` — 개별 처리, 인접 호출: Camera.add, KeyEvent.addKeyListener, KeyBindings.getActionForKey, GameMath.gate, Camera.remove, KeyEvent.removeKeyListener
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L67) `public boolean onSignal(KeyEvent keyEvent) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getActionForKey, GameMath.gate, Camera.remove, KeyEvent.removeKeyListener
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L92) `public void destroy() {` — 개별 처리, 인접 호출: Camera.remove, KeyEvent.removeKeyListener
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L98) `public void scrollTo( float x, float y ) {` — 개별 처리
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L117) `public synchronized void update() {` — 행동·상태 갱신
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L125) `protected void createChildren() {` — 생성·초기화
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L135) `protected void layout() {` — 개별 처리
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L157) `public Component content() {` — 개별 처리
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L161) `public void onClick( float x, float y ) {` — 이벤트·효과 실행, 인접 호출: PointF.distance
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L168) `public PointerController() {` — 개별 처리, 인접 호출: PointF.distance
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L174) `protected void onScroll(ScrollEvent event) {` — 이벤트·효과 실행, 인접 호출: PointF.distance, PointF.diff
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L182) `protected void onPointerUp( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: PointF.distance, PointF.diff
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L191) `protected void onClick(PointerEvent event) {` — 이벤트·효과 실행, 인접 호출: PointF.distance, PointF.diff
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L197) `private PointF lastPos = new PointF();` — 개별 처리, 인접 호출: PointF.distance, PointF.diff
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L200) `protected void onDrag( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: PointF.distance, PointF.diff
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollPane.java#L214) `private void scroll( PointF current ){` — 개별 처리, 인접 호출: PointF.diff

## 1158. [`StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 420행.

### 클래스/타입
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L48) `public class StatusPane extends Component {`

### 변수·상수 후보
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L50) `private NinePatch bg;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L51) `private Image avatar;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L52) `private Button heroInfo;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L53) `public static float talentBlink;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L54) `private float warning;`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L58) `private int lastTier = 0;`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L60) `private Image shieldHP;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L61) `private Image hp;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L63) `private BitmapText hpText;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L64) `private Button heroInfoOnBar;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L66) `private Image exp;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L67) `private BitmapText expText;`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L69) `private int lastLvl = -1;`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L71) `private BitmapText level;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L73) `private BuffIndicator buffs;`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L74) `private Compass compass;`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L76) `private BusyIndicator busy;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L77) `private CircleArc counter;`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L79) `private boolean large;`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L82) `public static float heroPaneExtraWidth = 0;`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L83) `private NinePatch heroPaneCutout;`
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L85) `public static int hpBarMaxWidth = 50;`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L86) `private Image hpCutout;`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L88) `public static float[] buffBarRowMaxWidths;`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L89) `public static float[] buffBarRowAdjusts;`
- [L290](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L290) `private static final int[] warningColors = new int[]{0x660000, 0xCC0000, 0x660000};`
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L292) `private int oldHP = 0;`
- [L293](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L293) `private int oldShield = 0;`
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L294) `private int oldMax = 0;`

### 메서드 및 코드 의존 단서
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L91) `public StatusPane( boolean large ){` — 개별 처리, 인접 호출: GameScene.show, Messages.titleCase, Messages.get, HeroSprite.avatar
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L112) `protected void onClick () {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase, Messages.get, HeroSprite.avatar, Dot.hardlight, Dot.alpha
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L118) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, HeroSprite.avatar, Dot.hardlight, Dot.alpha, GameScene.show
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L123) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, HeroSprite.avatar, Dot.hardlight, Dot.alpha, GameScene.show
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L157) `protected void onClick () {` — 이벤트·효과 실행, 인접 호출: GameScene.show
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L189) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align
- [L297](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L297) `public void update() {` — 행동·상태 갱신, 인접 호출: ColorMath.interpolate, Math.abs, Math.cos, Math.min, Dot.width
- [L391](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L391) `public void updateAvatar(){` — 행동·상태 갱신, 인접 호출: HeroSprite.avatar, GameMath.gate, Speck.factory
- [L395](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L395) `public void alpha( float value ){` — 개별 처리, 인접 호출: GameMath.gate, Speck.factory
- [L412](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java#L412) `public void showStarParticles(){` — 개별 처리, 인접 호출: Speck.factory

## 1159. [`StyledButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 180행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L32) `public class StyledButton extends Button {`

### 변수·상수 후보
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L34) `protected NinePatch bg;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L35) `protected RenderedTextBlock text;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L36) `protected Image icon;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L37) `public boolean leftJustify = false;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L39) `public boolean multiline;`

### 메서드 및 코드 의존 단서
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L41) `public StyledButton(Chrome.Type type, String label ) {` — 개별 처리, 인접 호출: Chrome.get, PixelScene.renderTextBlock, PixelScene.align
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L45) `public StyledButton(Chrome.Type type, String label, int size ){` — 개별 처리, 인접 호출: Chrome.get, PixelScene.renderTextBlock, PixelScene.align
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L57) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L103) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L109) `protected void onPointerUp() {` — 이벤트·효과 실행
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L113) `public void enable( boolean value ) {` — 개별 처리
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L119) `public void text( String value ) {` — 개별 처리
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L124) `public String text(){` — 개별 처리
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L128) `public void textColor( int value ) {` — 개별 처리, 인접 호출: Math.max
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L132) `public void icon( Image icon ) {` — 개별 처리, 인접 호출: Math.max
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L143) `public Image icon(){` — 개별 처리, 인접 호출: Math.max
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L147) `public void alpha(float value){` — 개별 처리, 인접 호출: Math.max
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L153) `public float alpha(){` — 개별 처리, 인접 호출: Math.max
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L158) `public float reqWidth() {` — 개별 처리, 인접 호출: Math.max
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java#L169) `public float reqHeight() {` — 개별 처리, 인접 호출: Math.max

## 1160. [`Tag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 108행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L29) `public class Tag extends Button {`

### 변수·상수 후보
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L31) `private float r;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L32) `private float g;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L33) `private float b;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L34) `protected NinePatch bg;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L36) `protected float lightness = 0;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L38) `public static int SIZE = 24;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L40) `protected boolean flipped = false;`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L42) `public Tag( int color ) {` — 개별 처리, 인접 호출: Chrome.get
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L51) `protected void createChildren() {` — 생성·초기화, 인접 호출: Chrome.get
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L61) `protected void onClick() {` — 이벤트·효과 실행
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L66) `protected void layout() {` — 개별 처리
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L75) `public void flash() {` — 개별 처리
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L79) `public void flip(boolean value){` — 개별 처리
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L85) `public void setColor( int color ){` — 개별 처리
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java#L93) `public void update() {` — 행동·상태 갱신

## 1161. [`TalentButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 263행.

### 클래스/타입
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L43) `public class TalentButton extends Button {`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L58) `public enum Mode {`

### 변수·상수 후보
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L45) `public static final int WIDTH = 20;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L46) `public static final int HEIGHT = 26;`

### 메서드 및 코드 의존 단서
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L65) `public TalentButton(int tier, Talent talent, int points, Mode mode){` — 개별 처리, 인접 호출: PixelScene.align
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L81) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.align, WndInfoTalent.TalentButtonCallback, Messages.titleCase, Messages.get
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L92) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, WndInfoTalent.TalentButtonCallback, Messages.titleCase, Messages.get
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L111) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: WndInfoTalent.TalentButtonCallback, Messages.titleCase, Messages.get, INSTANCE.hide, GameScene.show, ScrollOfMetamorphosis.WndMetamorphReplace
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L123) `public String prompt() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, WndInfoTalent.TalentButtonCallback, INSTANCE.hide, GameScene.show, ScrollOfMetamorphosis.WndMetamorphReplace
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L128) `public void call() {` — 개별 처리, 인접 호출: WndInfoTalent.TalentButtonCallback, Messages.titleCase, Messages.get, INSTANCE.hide, GameScene.show, ScrollOfMetamorphosis.WndMetamorphReplace
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L137) `public String prompt() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, INSTANCE.hide, GameScene.show, ScrollOfMetamorphosis.WndMetamorphReplace, WndInfoTalent.TalentButtonCallback
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L142) `public boolean metamorphDesc() {` — 개별 처리, 인접 호출: INSTANCE.hide, GameScene.show, ScrollOfMetamorphosis.WndMetamorphReplace, WndInfoTalent.TalentButtonCallback, Messages.titleCase, Messages.get
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L147) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.hide, GameScene.show, ScrollOfMetamorphosis.WndMetamorphReplace, WndInfoTalent.TalentButtonCallback, Messages.titleCase, Messages.get
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L158) `public String prompt() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L163) `public boolean metamorphDesc() {` — 개별 처리, 인접 호출: ScrollOfMetamorphosis.onMetamorph
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L168) `public void call() {` — 개별 처리, 인접 호출: ScrollOfMetamorphosis.onMetamorph, INSTANCE.hide
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L226) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, Messages.titleCase, Speck.factory
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L233) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase, INSTANCE.play, Speck.factory
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L239) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, INSTANCE.play, Speck.factory
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L243) `public void enable(boolean value ) {` — 개별 처리, 인접 호출: INSTANCE.play, Speck.factory
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentButton.java#L249) `public void upgradeTalent(){` — 개별 처리, 인접 호출: INSTANCE.play, Speck.factory

## 1162. [`TalentIcon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentIcon.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 47행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentIcon.java#L29) `public class TalentIcon extends Image {`

### 변수·상수 후보
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentIcon.java#L31) `private static TextureFilm film;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentIcon.java#L32) `private static final int SIZE = 16;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentIcon.java#L34) `public TalentIcon(Talent talent){` — 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentIcon.java#L38) `public TalentIcon(int icon){` — 개별 처리

## 1163. [`TalentsPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 324행.

### 클래스/타입
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L44) `public class TalentsPane extends ScrollPane {`
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L162) `public static class TalentTierPane extends Component {`

### 변수·상수 후보
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L164) `private int tier;`
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L166) `public RenderedTextBlock title;`

### 메서드 및 코드 의존 단서
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L53) `public TalentsPane( TalentButton.Mode mode ) {` — 개별 처리, 인접 호출: Badges.isUnlocked, Math.min
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L57) `public TalentsPane( TalentButton.Mode mode, ArrayList<LinkedHashMap<Talent, Integer>> talents ) {` — 개별 처리, 인접 호출: Badges.isUnlocked, Math.min
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L125) `protected void layout() {` — 개별 처리, 인접 호출: Math.max
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L172) `public TalentTierPane(LinkedHashMap<Talent, Integer> talents, int tier, TalentButton.Mode mode){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, Messages.get, SHUFFLE.get, GameScene.show, Random.element
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L187) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, SHUFFLE.get, Messages.get, Random.element, Math.abs, Math.cos
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L197) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: Random.element, Math.abs, Math.cos
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L221) `public void update() {` — 행동·상태 갱신, 인접 호출: Math.abs, Math.cos
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L236) `public void upgradeTalent() {` — 개별 처리
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L250) `private void setupStars(){` — 생성·초기화, 인접 호출: Math.min
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TalentsPane.java#L280) `protected void layout() {` — 개별 처리, 인접 호출: Math.min, PixelScene.align

## 1164. [`TargetHealthIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TargetHealthIndicator.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 68행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TargetHealthIndicator.java#L27) `public class TargetHealthIndicator extends HealthBar {`

### 변수·상수 후보
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TargetHealthIndicator.java#L29) `public static TargetHealthIndicator instance;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TargetHealthIndicator.java#L31) `private Char target;`

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TargetHealthIndicator.java#L33) `public TargetHealthIndicator() {` — 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TargetHealthIndicator.java#L40) `public void update() {` — 행동·상태 갱신
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TargetHealthIndicator.java#L56) `public void target( Char ch ) {` — 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TargetHealthIndicator.java#L64) `public Char target() {` — 개별 처리

## 1165. [`TitleBackground.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 741행.

### 클래스/타입
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L40) `public class TitleBackground extends Component {`

### 변수·상수 후보
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L42) `public static float SCROLL_SPEED	= 15f;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L44) `private float density = 1f;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L48) `private static Group archLayer;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L49) `private static ArrayList<Image> archs;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L53) `private static ArrayList<Image> clusters;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L54) `private static Group clusterLayer;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L56) `private static ArrayList<Image> clustersFar;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L57) `private static Group clustersFarLayer;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L61) `private static ArrayList<Image> smallFars;`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L62) `private static Group smallFarLayer;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L66) `private static ArrayList<Image> mids1;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L67) `private static Group mids1Layer;`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L69) `private static ArrayList<Image> mids2;`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L70) `private static Group mids2Layer;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L73) `private static ArrayList<Image> smallCloses;`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L74) `private static Group smallCloseLayer;`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L76) `private static boolean wasLandscape;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L77) `private static float oldBaseScale = 1;`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L78) `private static float oldWidth = 0;`
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L284) `private static final float[] INIT_ARCH_CHANCES = {5, 5, 2, 2, 2, 2};`
- [L343](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L343) `private static final float[] INIT_CLUSTER_CHANCES = {2, 2};`
- [L470](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L470) `private static final float[] INIT_MID_CHANCES = {1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1};`
- [L606](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L606) `private static final float[] INIT_SMALL_CHANCES = {1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1};`

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L47) `private static final TextureFilm ARCH_FILM = new TextureFilm(Assets.Splashes.Title.ARCHS, 333, 100);` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L52) `private static TextureFilm CLUSTER_FILM = new TextureFilm(Assets.Splashes.Title.BACK_CLUSTERS, 450, 250);` — 개별 처리
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L60) `private static TextureFilm SMALL_FILM = new TextureFilm(Assets.Splashes.Title.FRONT_SMALL, 112, 116);` — 개별 처리
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L65) `private static TextureFilm MID_FILM = new TextureFilm(Assets.Splashes.Title.MID_MIXED, 273, 242);` — 개별 처리
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L80) `public static void reset(){` — 개별 처리, 인접 호출: TextureCache.createGradient
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L90) `public TitleBackground(int width, int height){` — 개별 처리, 인접 호출: TextureCache.createGradient
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L98) `protected void setupObjects() {` — 생성·초기화, 인접 호출: TextureCache.createGradient
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L198) `protected Image convertImage(Image oldImg, float newBaseScale){` — 개별 처리
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L211) `protected void convertArchLayer(ArrayList<Image> layerList, Group layerGroup, float newBaseScale){` — 개별 처리
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L235) `protected void convertFloatingLayer(ArrayList<Image> layerList, Group layerGroup, float newBaseScale, float oldWidth){` — 개별 처리
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L254) `public synchronized void update() {` — 행동·상태 갱신, 인접 호출: INIT_ARCH_CHANCES.clone, Random.chances, ARCH_FILM.get
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L285) `private static float[] arch_chances = INIT_ARCH_CHANCES.clone();` — 개별 처리, 인접 호출: Random.chances, INIT_ARCH_CHANCES.clone, ARCH_FILM.get, Random.Int
- [L287](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L287) `public RectF getArchFrame(){` — 조회·판정, 인접 호출: Random.chances, INIT_ARCH_CHANCES.clone, ARCH_FILM.get, Random.Int
- [L299](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L299) `private void updateArchLayer(float scale, float shift){` — 행동·상태 갱신, 인접 호출: Random.Int
- [L344](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L344) `private static float[] cluster_chances = INIT_CLUSTER_CHANCES.clone();` — 개별 처리, 인접 호출: Random.chances, INIT_CLUSTER_CHANCES.clone, CLUSTER_FILM.get, Random.Float, Math.abs
- [L346](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L346) `public RectF getClusterFrame(){` — 조회·판정, 인접 호출: Random.chances, INIT_CLUSTER_CHANCES.clone, CLUSTER_FILM.get, Random.Float, Math.abs
- [L358](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L358) `private void updateClusterFarLayer(float scale, float shift){` — 행동·상태 갱신, 인접 호출: Random.Float, Math.abs
- [L413](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L413) `private void updateClusterLayer(float scale, float shift){` — 행동·상태 갱신, 인접 호출: Random.Float, Math.abs
- [L471](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L471) `private static float[] mid_chances = INIT_MID_CHANCES.clone();` — 개별 처리, 인접 호출: Random.chances, INIT_MID_CHANCES.clone, MID_FILM.get, Random.Float
- [L475](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L475) `public RectF getMidFrame(){` — 조회·판정, 인접 호출: Random.chances, INIT_MID_CHANCES.clone, MID_FILM.get, Random.Float, Math.abs
- [L495](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L495) `private void updateMid1Layer(float scale, float shift){` — 행동·상태 갱신, 인접 호출: Random.Float, Math.abs
- [L550](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L550) `private void updateMid2Layer(float scale, float shift){` — 행동·상태 갱신, 인접 호출: Random.Float, Math.abs
- [L607](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L607) `private static float[] small_chances = INIT_SMALL_CHANCES.clone();` — 개별 처리, 인접 호출: Random.chances, INIT_SMALL_CHANCES.clone, SMALL_FILM.get, Random.Float
- [L611](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L611) `public RectF getSmallFrame(){` — 조회·판정, 인접 호출: Random.chances, INIT_SMALL_CHANCES.clone, SMALL_FILM.get, Random.Float, Math.abs
- [L631](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L631) `private void updateFarSmallLayer(float scale, float shift) {` — 행동·상태 갱신, 인접 호출: Random.Float, Math.abs
- [L686](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java#L686) `private void updateFrontSmallLayer(float scale, float shift){` — 행동·상태 갱신, 인접 호출: Random.Float, Math.abs

## 1166. [`Toast.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 94행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L30) `public class Toast extends Component {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L32) `private static final float MARGIN_HOR	= 2;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L33) `private static final float MARGIN_VER	= 2;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L35) `protected NinePatch bg;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L36) `protected IconButton close;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L37) `protected RenderedTextBlock text;`

### 메서드 및 코드 의존 단서
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L39) `public Toast( String text ) {` — 개별 처리, 인접 호출: Math.max, Chrome.get, Icons.get, PixelScene.renderTextBlock, PixelScene.align
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L48) `protected void createChildren() {` — 생성·초기화, 인접 호출: Chrome.get, Icons.get, PixelScene.renderTextBlock, PixelScene.align
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L55) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L60) `public GameAction keyAction() {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L72) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L88) `public void text( String txt ) {` — 개별 처리
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java#L92) `protected void onClose() {}` — 이벤트·효과 실행

## 1167. [`Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 995행.

### 클래스/타입
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L61) `public class Toolbar extends Component {`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L76) `public enum Mode {`
- [L702](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L702) `private static class Tool extends Button {`
- [L778](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L778) `private static class QuickslotTool extends Tool {`
- [L820](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L820) `public static class SlotSwapTool extends Tool {`
- [L933](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L933) `public static class PickedUpItem extends ItemSprite {`

### 변수·상수 후보
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L63) `private Tool btnWait;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L64) `private Tool btnSearch;`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L65) `private Tool btnInventory;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L66) `private QuickslotTool[] btnQuick;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L67) `private SlotSwapTool btnSwap;`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L69) `private PickedUpItem pickedUp;`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L71) `private boolean lastEnabled = true;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L72) `public boolean examining = false;`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L74) `private static Toolbar instance;`
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L320) `private CurrencyIndicator ind;`
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L322) `private Image arrow;`
- [L704](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L704) `private static final int BGCOLOR = 0x7B8073;`
- [L706](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L706) `private Image base;`
- [L707](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L707) `private Image icon;`
- [L780](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L780) `private QuickSlotButton slot;`
- [L781](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L781) `private int borderLeft = 2;`
- [L782](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L782) `private int borderRight = 2;`
- [L817](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L817) `public static boolean swappedQuickslots = false;`
- [L818](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L818) `public static SlotSwapTool SWAP_INSTANCE;`
- [L822](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L822) `private Image[] icons = new Image[4];`
- [L823](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L823) `private Item[] items = new Item[4];`
- [L935](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L935) `private static final float DURATION = 0.5f;`
- [L937](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L937) `private float startScale;`
- [L938](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L938) `private float startX, startY;`
- [L939](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L939) `private float endX, endY;`
- [L940](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L940) `private float left;`

### 메서드 및 코드 의존 단서
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L82) `public Toolbar() {` — 개별 처리, 인접 호출: QuickSlotButton.autoAim, GameScene.handleCell, GameScene.cancel
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L91) `public synchronized void destroy() {` — 개별 처리, 인접 호출: QuickSlotButton.autoAim, GameScene.handleCell, GameScene.cancel, Messages.titleCase, Messages.get
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L97) `protected void createChildren() {` — 생성·초기화, 인접 호출: QuickSlotButton.autoAim, GameScene.handleCell, GameScene.cancel, Messages.titleCase, Messages.get, KeyBindings.getKeyName, KeyBindings.getFirstKeyForAction
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L109) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: QuickSlotButton.autoAim, GameScene.handleCell, GameScene.cancel, Messages.titleCase, Messages.get, KeyBindings.getKeyName, KeyBindings.getFirstKeyForAction
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L152) `public void onSelect(int idx, boolean alt) {` — 이벤트·효과 실행, 인접 호출: GameScene.selectItem, WndBag.ItemSelector, Messages.get, QuickSlotButton.set, QuickSlotButton.useTargeting
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L162) `public String textPrompt() {` — 개별 처리, 인접 호출: Messages.get, QuickSlotButton.set, QuickSlotButton.useTargeting, GameScene.cancel
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L167) `public boolean itemSelectable(Item item) {` — 개별 처리, 인접 호출: QuickSlotButton.set, QuickSlotButton.useTargeting, GameScene.cancel
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L172) `public void onSelect(Item item) {` — 이벤트·효과 실행, 인접 호출: QuickSlotButton.set, QuickSlotButton.useTargeting, GameScene.cancel
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L192) `public GameAction keyAction() {` — 개별 처리, 인접 호출: GameScene.cancel, Messages.titleCase, Messages.get
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L200) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.cancel, Messages.titleCase, Messages.get
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L208) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, GameScene.cancel
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L213) `public GameAction secondaryTooltipAction() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, GameScene.cancel
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L218) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, GameScene.cancel, Buff.affect
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L222) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.cancel, Buff.affect
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L235) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.cancel, Buff.affect
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L243) `public GameAction keyAction() {` — 개별 처리, 인접 호출: GameScene.cancel, Buff.affect
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L252) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.cancel, Buff.affect, GameScene.selectCell
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L272) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.cancel, GameScene.selectCell, Messages.titleCase, Messages.get
- [L281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L281) `public GameAction keyAction() {` — 개별 처리, 인접 호출: GameScene.cancel, GameScene.selectCell, Messages.titleCase, Messages.get
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L289) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.cancel, GameScene.selectCell, Messages.titleCase, Messages.get, SPDSettings.interfaceSize, GameScene.toggleInvPane, GameScene.show
- [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L302) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, SPDSettings.interfaceSize, GameScene.toggleInvPane, GameScene.cancel, GameScene.show
- [L307](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L307) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, SPDSettings.interfaceSize, GameScene.toggleInvPane, GameScene.cancel, GameScene.show
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L312) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.interfaceSize, GameScene.toggleInvPane, GameScene.cancel, GameScene.show, Messages.titleCase, Messages.get
- [L325](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L325) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.interfaceSize, GameScene.toggleInvPane, GameScene.cancel, GameScene.show, Messages.titleCase, Messages.get, Icons.get
- [L338](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L338) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, GameScene.show, Icons.get, SPDSettings.interfaceSize, PixelScene.align
- [L343](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L343) `public GameAction secondaryTooltipAction() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, GameScene.show, Icons.get, SPDSettings.interfaceSize, PixelScene.align
- [L348](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L348) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, GameScene.show, Icons.get, SPDSettings.interfaceSize, PixelScene.align
- [L353](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L353) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Icons.get, SPDSettings.interfaceSize, PixelScene.align, GameScene.cancel
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L359) `protected void createChildren() {` — 생성·초기화, 인접 호출: Icons.get, SPDSettings.interfaceSize, PixelScene.align, GameScene.cancel, Messages.titleCase
- [L372](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L372) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, GameScene.cancel, Messages.titleCase, KeyBindings.getKeyName, KeyBindings.getFirstKeyForAction, Messages.get, LEFT_CLICK.name
- [L384](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L384) `public void enable(boolean value) {` — 개별 처리, 인접 호출: GameScene.cancel, Messages.titleCase, KeyBindings.getKeyName, KeyBindings.getFirstKeyForAction, Messages.get, LEFT_CLICK.name, Game.scene
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L396) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.cancel, Messages.titleCase, KeyBindings.getKeyName, KeyBindings.getFirstKeyForAction, Messages.get, LEFT_CLICK.name, Game.scene
- [L416](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L416) `public void onSelect(int idx, boolean alt) {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.get, Messages.titleCase, KeyBindings.getKeyName, KeyBindings.getFirstKeyForAction, LEFT_CLICK.name, RIGHT_CLICK.name
- [L461](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L461) `public void onSelect(int idx, boolean alt) {` — 이벤트·효과 실행, 인접 호출: InventoryPane.clearTargetingSlot, Game.scene, SPDSettings.quickSwapper
- [L478](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L478) `public GameAction keyAction() {` — 개별 처리, 인접 호출: SPDSettings.quickSwapper, SPDSettings.interfaceSize
- [L488](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L488) `protected void layout() {` — 개별 처리, 인접 호출: SPDSettings.quickSwapper, SPDSettings.interfaceSize
- [L648](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L648) `public static void updateLayout(){` — 행동·상태 갱신, 인접 호출: CellSelector.Listener
- [L653](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L653) `public void update() {` — 행동·상태 갱신, 인접 호출: CellSelector.Listener, GameScene.examineCell
- [L671](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L671) `public void alpha( float value ){` — 개별 처리, 인접 호출: CellSelector.Listener, GameScene.examineCell, Messages.get
- [L681](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L681) `public void pickup( Item item, int cell ) {` — 개별 처리, 인접 호출: CellSelector.Listener, GameScene.examineCell, Messages.get
- [L688](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L688) `private static CellSelector.Listener informer = new CellSelector.Listener() {` — 개별 처리, 인접 호출: GameScene.examineCell, Messages.get
- [L690](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L690) `public void onSelect( Integer cell ) {` — 이벤트·효과 실행, 인접 호출: GameScene.examineCell, Messages.get
- [L697](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L697) `public String prompt() {` — 개별 처리, 인접 호출: Messages.get
- [L709](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L709) `public Tool( int x, int y, int width, int height ) {` — 개별 처리
- [L716](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L716) `public void frame( int x, int y, int width, int height) {` — 개별 처리
- [L723](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L723) `public void icon( int x, int y, int width, int height){` — 개별 처리
- [L731](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L731) `protected void createChildren() {` — 생성·초기화
- [L739](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L739) `protected void layout() {` — 개별 처리
- [L751](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L751) `public void alpha( float value ){` — 개별 처리
- [L757](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L757) `protected void onPointerDown() {` — 이벤트·효과 실행
- [L762](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L762) `protected void onPointerUp() {` — 이벤트·효과 실행
- [L770](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L770) `public void enable( boolean value ) {` — 개별 처리
- [L784](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L784) `public QuickslotTool( int x, int y, int width, int height, int slotNum ) {` — 개별 처리
- [L791](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L791) `public void border( int left, int right ){` — 개별 처리
- [L798](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L798) `protected void layout() {` — 개별 처리
- [L805](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L805) `public void alpha(float value) {` — 개별 처리, 인접 호출: Icons.get, PixelScene.align
- [L811](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L811) `public void enable( boolean value ) {` — 개별 처리, 인접 호출: Icons.get, PixelScene.align, SPDSettings.flipToolbar
- [L825](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L825) `public SlotSwapTool(int x, int y, int width, int height) {` — 개별 처리, 인접 호출: Icons.get, PixelScene.align, SPDSettings.flipToolbar
- [L832](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L832) `public synchronized void destroy() {` — 개별 처리, 인접 호출: Icons.get, PixelScene.align, SPDSettings.flipToolbar
- [L838](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L838) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Icons.get, PixelScene.align, SPDSettings.flipToolbar
- [L845](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L845) `public void updateVisuals(){` — 행동·상태 갱신, 인접 호출: Icons.get, PixelScene.align, SPDSettings.flipToolbar
- [L906](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L906) `protected void layout() {` — 개별 처리
- [L912](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L912) `public void alpha(float value) {` — 개별 처리
- [L920](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L920) `public void enable(boolean value) {` — 개별 처리, 인접 호출: DungeonTerrainTilemap.raisedTileCenterToWorld
- [L942](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L942) `public PickedUpItem() {` — 개별 처리, 인접 호출: DungeonTerrainTilemap.raisedTileCenterToWorld
- [L952](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L952) `public void reset( Item item, int cell, float endX, float endY ) {` — 개별 처리, 인접 호출: DungeonTerrainTilemap.raisedTileCenterToWorld, Math.sqrt
- [L975](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java#L975) `public void update() {` — 행동·상태 갱신, 인접 호출: Math.sqrt

## 1168. [`Tooltip.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 118행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java#L32) `public class Tooltip extends Component {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java#L36) `private static float tooltipAlpha = -5f;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java#L37) `private static float lastUsedTime = -1;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java#L44) `private Component parent;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java#L45) `private RectF parentDims;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java#L47) `private NinePatch bg;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java#L48) `private RenderedTextBlock text;`

### 메서드 및 코드 의존 단서
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java#L39) `public static void resetLastUsedTime(){` — 개별 처리, 인접 호출: GameMath.gate, Chrome.get, PixelScene.renderTextBlock
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java#L50) `public Tooltip(Component parent, String msg, int maxWidth){` — 개별 처리, 인접 호출: GameMath.gate, Chrome.get, PixelScene.renderTextBlock
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java#L73) `protected void createChildren() {` — 생성·초기화, 인접 호출: Chrome.get, PixelScene.renderTextBlock, Math.min, GameMath.gate
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java#L84) `public synchronized void update() {` — 행동·상태 갱신, 인접 호출: Math.min, GameMath.gate
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java#L106) `protected void layout() {` — 개별 처리

## 1169. [`Window.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 228행.

### 클래스/타입
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L41) `public class Window extends Group implements Signal.Listener<KeyEvent> {`

### 변수·상수 후보
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L43) `protected int width;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L44) `protected int height;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L46) `protected int xOffset;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L47) `protected int yOffset;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L49) `protected PointerArea blocker;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L50) `protected ShadowBox shadow;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L51) `protected NinePatch chrome;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L53) `public static final int WHITE = 0xFFFFFF;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L54) `public static final int TITLE_COLOR = 0xFFFF44;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L55) `public static final int SHPX_COLOR = 0x33BB33;`

### 메서드 및 코드 의존 단서
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L57) `public Window() {` — 개별 처리, 인접 호출: Chrome.get
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L61) `public Window( int width, int height ) {` — 개별 처리, 인접 호출: Chrome.get
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L65) `public Window( int width, int height, NinePatch chrome ) {` — 개별 처리
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L70) `protected void onClick( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: Camera.add
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L122) `public void resize( int w, int h ) {` — 개별 처리
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L147) `public Point getOffset(){` — 조회·판정
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L151) `public final void offset( Point offset ){` — 개별 처리
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L156) `public void offset( int xOffset, int yOffset ){` — 개별 처리
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L169) `public void boundOffsetWithMargin( int margin ){` — 개별 처리, 인접 호출: Camera.remove, KeyEvent.removeKeyListener
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L196) `public void hide() {` — 개별 처리, 인접 호출: Camera.remove, KeyEvent.removeKeyListener, KeyBindings.getActionForKey
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L204) `public void destroy() {` — 개별 처리, 인접 호출: Camera.remove, KeyEvent.removeKeyListener, KeyBindings.getActionForKey
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L212) `public boolean onSignal( KeyEvent event ) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getActionForKey
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java#L223) `public void onBackPressed() {` — 이벤트·효과 실행

## 1170. [`DungeonSeed.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/DungeonSeed.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.utils`, 151행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/DungeonSeed.java#L29) `public class DungeonSeed {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/DungeonSeed.java#L41) `public static long randomSeed(){` — 개별 처리, 인접 호출: Random.Long, Math.pow, Long.toString
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/DungeonSeed.java#L52) `public static long convertFromCode( String code ){` — 개별 처리, 인접 호출: Math.pow, Long.toString
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/DungeonSeed.java#L77) `public static String convertToCode( long seed ){` — 개별 처리, 인접 호출: Long.toString
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/DungeonSeed.java#L110) `public static long convertFromText( String inputText ){` — 개별 처리, 인접 호출: Long.parseLong
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/DungeonSeed.java#L140) `public static String formatText( String inputText ){` — 개별 처리

## 1171. [`GLog.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.utils`, 71행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L28) `public class GLog {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L30) `public static final String TAG = "GAME";`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L32) `public static final String POSITIVE		= "++ ";`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L33) `public static final String NEGATIVE		= "-- ";`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L34) `public static final String WARNING		= "** ";`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L35) `public static final String HIGHLIGHT	= "@@ ";`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L37) `public static final String NEW_LINE	    = "\n";`

### 메서드 및 코드 의존 단서
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L41) `public static void newLine(){` — 개별 처리, 인접 호출: Messages.format, DeviceCompat.log
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L45) `public static void i( String text, Object... args ) {` — 개별 처리, 인접 호출: Messages.format, DeviceCompat.log
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L55) `public static void p( String text, Object... args ) {` — 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L59) `public static void n( String text, Object... args ) {` — 개별 처리
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L63) `public static void w( String text, Object... args ) {` — 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java#L67) `public static void h( String text, Object... args ) {` — 개별 처리

## 1172. [`Holiday.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/Holiday.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.utils`, 258행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/Holiday.java#L27) `public enum Holiday {`

### 변수·상수 후보
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/Holiday.java#L49) `private static Holiday cached;`

### 메서드 및 코드 의존 단서
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/Holiday.java#L50) `public static void clearCachedHoliday(){` — 개별 처리, 인접 호출: GregorianCalendar.getInstance
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/Holiday.java#L54) `public static Holiday getCurrentHoliday(){` — 조회·판정, 인접 호출: GregorianCalendar.getInstance
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/Holiday.java#L62) `public static Holiday getHolidayForDate(GregorianCalendar cal){` — 조회·판정
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/Holiday.java#L124) `public static boolean isLunarNewYear(int year, int dayOfYear){` — 조회·판정
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/Holiday.java#L217) `public static boolean isEaster(int year, int dayOfYear, boolean isLeapYear){` — 조회·판정

## 1173. [`IconTitle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 150행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L35) `public class IconTitle extends Component {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L37) `private static final float FONT_SIZE = 9;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L39) `private static final float GAP = 2;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L41) `protected Image imIcon;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L42) `protected RenderedTextBlock tfLabel;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L43) `protected HealthBar health;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L45) `private float healthLvl = Float.NaN;`

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L47) `public IconTitle() {` — 개별 처리, 인접 호출: Messages.titleCase, PixelScene.renderTextBlock, Float.isNaN
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L51) `public IconTitle( Item item ) {` — 개별 처리, 인접 호출: Messages.titleCase, PixelScene.renderTextBlock, Float.isNaN, Math.max, PixelScene.align
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L59) `public IconTitle( Heap heap ){` — 개별 처리, 인접 호출: Messages.titleCase, PixelScene.renderTextBlock, Float.isNaN, Math.max, PixelScene.align
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L67) `public IconTitle( Image icon, String label ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Float.isNaN, Math.max, PixelScene.align
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L74) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, Float.isNaN, Math.max, PixelScene.align
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L88) `protected void layout() {` — 개별 처리, 인접 호출: Float.isNaN, Math.max, PixelScene.align
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L112) `public float reqWidth(){` — 개별 처리
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L116) `public void icon( Image icon ) {` — 개별 처리
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L123) `public void label( String label ) {` — 개별 처리
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L127) `public void label( String label, int color ) {` — 개별 처리
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L132) `public void color( int color ) {` — 개별 처리
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L136) `public float alpha(){` — 개별 처리
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L140) `public void alpha( float value ){` — 개별 처리
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java#L145) `public void health( float value ) {` — 개별 처리


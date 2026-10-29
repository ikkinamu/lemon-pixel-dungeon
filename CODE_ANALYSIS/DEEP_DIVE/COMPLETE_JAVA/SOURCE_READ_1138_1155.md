# Java 소스 구현 분석 1138–1155

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1138. [`Icons.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Icons.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 529행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Icons.java#L34) `public enum Icons {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Icons.java#L141) `public Image get() {` — 조회·판정, 인접 호출: PixelScene.landscape
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Icons.java#L145) `public static Image get( Icons type ) {` — 조회·판정, 인접 호출: PixelScene.landscape
- [L450](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Icons.java#L450) `private static int runTypeOfsX(){` — 개별 처리
- [L454](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Icons.java#L454) `private static int runTypeOfsY(){` — 개별 처리
- [L463](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Icons.java#L463) `public static Image get( HeroClass cl ) {` — 조회·판정
- [L487](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Icons.java#L487) `public static Image get(Level.Feeling feeling){` — 조회·판정
- [L508](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Icons.java#L508) `public static Image getLarge(Level.Feeling feeling){` — 조회·판정

## 1139. [`InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 711행.

### 클래스/타입
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L61) `public class InventoryPane extends Component {`
- [L491](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L491) `private class InventoryPaneSlot extends InventorySlot {`
- [L609](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L609) `private class BagButton extends IconButton {`

### 변수·상수 후보
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L63) `private NinePatch bg;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L66) `private PointerArea blocker;`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L68) `private Signal.Listener<KeyEvent> keyBlocker;`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L70) `private static InventoryPane instance;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L72) `private ArrayList<InventorySlot> equipped;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L73) `private ArrayList<InventorySlot> bagItems;`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L75) `private Image gold;`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L76) `private BitmapText goldTxt;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L77) `private Image energy;`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L78) `private BitmapText energyTxt;`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L79) `private RenderedTextBlock promptTxt;`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L81) `private ArrayList<BagButton> bags;`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L83) `public static final int WIDTH = 187;`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L84) `public static final int HEIGHT = 82;`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L86) `private static final int SLOT_WIDTH = 17;`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L87) `private static final int SLOT_HEIGHT = 24;`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L89) `private WndBag.ItemSelector selector;`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L91) `public static Bag lastBag;`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L93) `private boolean lastEnabled = true;`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L95) `private static Image crossB;`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L96) `private static Image crossM;`
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L98) `private static boolean targeting = false;`
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L99) `private static InventorySlot targetingSlot = null;`
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L100) `public static Char lastTarget = null;`
- [L611](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L611) `private static final int ACTIVE		= 0x9953564D;`
- [L612](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L612) `private static final int INACTIVE	= 0x9942443D;`
- [L614](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L614) `private ColorBlock bgTop;`
- [L615](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L615) `private ColorBlock bgBottom;`
- [L617](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L617) `private Bag bag;`
- [L618](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L618) `private int index;`

### 메서드 및 코드 의존 단서
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L102) `public InventoryPane(){` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener, Chrome.get, GameScene.centerNextWndOnInvPane, KeyBindings.getActionForKey
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L108) `public synchronized void destroy() {` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener, Chrome.get, GameScene.centerNextWndOnInvPane, KeyBindings.getActionForKey
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L115) `protected void createChildren() {` — 생성·초기화, 인접 호출: Chrome.get, GameScene.centerNextWndOnInvPane, KeyBindings.getActionForKey
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L122) `protected void onClick(PointerEvent event) {` — 이벤트·효과 실행, 인접 호출: GameScene.centerNextWndOnInvPane, KeyBindings.getActionForKey, Icons.get
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L137) `public boolean onSignal(KeyEvent keyEvent) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getActionForKey, GameScene.centerNextWndOnInvPane, Icons.get, PixelScene.renderTextBlock
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L207) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L261) `public void alpha( float value ){` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener, KeyEvent.addKeyListener, WndBag.Placeholder
- [L281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L281) `public static void refresh(){` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener, KeyEvent.addKeyListener, WndBag.Placeholder
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L285) `public void updateInventory(){` — 행동·상태 갱신, 인접 호출: KeyEvent.removeKeyListener, KeyEvent.addKeyListener, WndBag.Placeholder
- [L383](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L383) `public void setSelector(WndBag.ItemSelector selector){` — 개별 처리, 인접 호출: Actor.chars
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L396) `public WndBag.ItemSelector getSelector() {` — 조회·판정, 인접 호출: Actor.chars
- [L400](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L400) `public boolean isSelecting(){` — 조회·판정, 인접 호출: Actor.chars
- [L404](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L404) `public static void clearTargetingSlot(){` — 개별 처리, 인접 호출: Actor.chars
- [L408](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L408) `public static void useTargeting(){` — 이벤트·효과 실행, 인접 호출: Actor.chars
- [L437](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L437) `public static void cancelTargeting(){` — 조회·판정, 인접 호출: Icons.get
- [L446](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L446) `public synchronized void update() {` — 행동·상태 갱신, 인접 호출: Icons.get
- [L477](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L477) `private Image bagIcon(Bag bag ) {` — 개별 처리, 인접 호출: Icons.get, QuickSlotButton.autoAim, GameScene.handleCell, GameScene.centerNextWndOnInvPane
- [L493](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L493) `private InventoryPaneSlot( Item item ){` — 개별 처리, 인접 호출: QuickSlotButton.autoAim, GameScene.handleCell, GameScene.centerNextWndOnInvPane, GameScene.show, QuickSlotButton.set
- [L498](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L498) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: QuickSlotButton.autoAim, GameScene.handleCell, GameScene.centerNextWndOnInvPane, GameScene.show, QuickSlotButton.set
- [L534](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L534) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: QuickSlotButton.set, GameScene.centerNextWndOnInvPane, GameScene.show, InventoryPane.useTargeting
- [L548](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L548) `protected void onMiddleClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.centerNextWndOnInvPane, InventoryPane.useTargeting
- [L578](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L578) `protected void onRightClick() {` — 이벤트·효과 실행, 인접 호출: PointerEvent.currentHoverPos
- [L620](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L620) `public BagButton( Bag bag, int index ){` — 개별 처리, 인접 호출: TextureCache.createSolid
- [L627](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L627) `public void bag( Bag bag ){` — 개별 처리, 인접 호출: TextureCache.createSolid
- [L642](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L642) `protected void createChildren() {` — 생성·초기화, 인접 호출: GameScene.cancel
- [L653](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L653) `protected void layout() {` — 개별 처리, 인접 호출: GameScene.cancel
- [L665](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L665) `public void alpha( float value ){` — 개별 처리, 인접 호출: GameScene.cancel, Messages.titleCase
- [L672](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L672) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.cancel, Messages.titleCase
- [L680](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L680) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.titleCase
- [L696](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L696) `public GameAction secondaryTooltipAction() {` — 개별 처리, 인접 호출: Messages.titleCase
- [L701](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java#L701) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase

## 1140. [`InventorySlot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 130행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java#L35) `public class InventorySlot extends ItemSlot {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java#L37) `private static final int NORMAL		= 0x9953564D;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java#L38) `private static final int EQUIPPED	= 0x9991938C;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java#L40) `private ColorBlock bg;`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java#L42) `public InventorySlot( Item item ) {` — 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java#L48) `protected void createChildren() {` — 생성·초기화, 인접 호출: TextureCache.createSolid
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java#L56) `protected void layout() {` — 개별 처리, 인접 호출: TextureCache.createSolid
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java#L65) `public void alpha(float value) {` — 개별 처리, 인접 호출: TextureCache.createSolid
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java#L71) `public void item( Item item ) {` — 개별 처리, 인접 호출: TextureCache.createSolid
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java#L115) `public Item item(){` — 개별 처리, 인접 호출: INSTANCE.play
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java#L120) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java#L125) `protected void onPointerUp() {` — 이벤트·효과 실행

## 1141. [`ItemButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 109행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L32) `public class ItemButton extends Component {`

### 변수·상수 후보
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L34) `protected NinePatch bg;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L35) `protected ItemSlot slot;`

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L38) `protected void createChildren() {` — 생성·초기화, 인접 호출: Chrome.get, INSTANCE.play
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L46) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L52) `protected void onPointerUp() {` — 이벤트·효과 실행
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L57) `protected void onClick() {` — 이벤트·효과 실행
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L62) `protected boolean onLongClick() {` — 이벤트·효과 실행
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L70) `protected void onClick() {}` — 이벤트·효과 실행
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L72) `protected boolean onLongClick(){` — 이벤트·효과 실행
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L77) `protected void layout() {` — 개별 처리
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L92) `public Item item(){` — 개별 처리
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L96) `public void item( Item item ) {` — 개별 처리
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L100) `public void clear(){` — 개별 처리
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemButton.java#L104) `public ItemSlot slot(){` — 개별 처리

## 1142. [`ItemJournalButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemJournalButton.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 110행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemJournalButton.java#L35) `public class ItemJournalButton extends IconButton {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemJournalButton.java#L40) `public ItemJournalButton(Item item, Window parentWnd){` — 개별 처리, 인접 호출: JOURNAL.get, Notes.findCustomRecord, Notes.getRecords, Notes.customRecordLimit, GameScene.show, INFO.get, Messages.get
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemJournalButton.java#L47) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Notes.findCustomRecord, Notes.getRecords, Notes.customRecordLimit, GameScene.show, INFO.get, Messages.get, Notes.CustomRecord
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemJournalButton.java#L53) `private void customNote(){` — 개별 처리, 인접 호출: Notes.findCustomRecord, Notes.getRecords, Notes.customRecordLimit, GameScene.show, INFO.get, Messages.get, Notes.CustomRecord
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemJournalButton.java#L84) `private static void addNote(Window parentWindow, Notes.CustomRecord note, String promptTitle, String prompttext){` — 개별 처리, 인접 호출: GameScene.show, Messages.get, Notes.add
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemJournalButton.java#L93) `public void onSelect(boolean positive, String text) {` — 이벤트·효과 실행, 인접 호출: Notes.add, GameScene.show

## 1143. [`ItemSlot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 362행.

### 클래스/타입
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L41) `public class ItemSlot extends Button {`

### 변수·상수 후보
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L43) `public static final int DEGRADED	= 0xFF4444;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L44) `public static final int UPGRADED	= 0x44FF44;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L45) `public static final int FADED       = 0x999999;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L46) `public static final int WARNING		= 0xFF8800;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L47) `public static final int ENHANCED	= 0x3399FF;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L48) `public static final int MASTERED	= 0xFFFF44;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L49) `public static final int CURSE_INFUSED	= 0x8800FF;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L51) `private static final float ENABLED	= 1.0f;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L52) `private static final float DISABLED	= 0.3f;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L56) `protected ItemSprite sprite;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L57) `protected Item       item;`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L58) `protected BitmapText status;`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L59) `protected BitmapText extra;`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L60) `protected Image      itemIcon;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L61) `protected BitmapText level;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L63) `private static final String TXT_STRENGTH	= ":%d";`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L64) `private static final String TXT_TYPICAL_STR	= "%d?";`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L66) `private static final String TXT_LEVEL	= "%+d";`

### 메서드 및 코드 의존 단서
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L54) `private Rect margin = new Rect();` — 개별 처리, 인접 호출: Messages.get
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L69) `public static final Item CHEST = new Item() {` — 개별 처리, 인접 호출: Messages.get
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L70) `public int image() { return ItemSpriteSheet.CHEST; }` — 개별 처리, 인접 호출: Messages.get
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L71) `public String name() { return Messages.get(Heap.class, "chest"); }` — 개별 처리, 인접 호출: Messages.get
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L73) `public static final Item LOCKED_CHEST = new Item() {` — 개별 처리, 인접 호출: Messages.get
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L74) `public int image() { return ItemSpriteSheet.LOCKED_CHEST; }` — 개별 처리, 인접 호출: Messages.get
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L75) `public String name() { return Messages.get(Heap.class, "locked_chest"); }` — 개별 처리, 인접 호출: Messages.get
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L77) `public static final Item CRYSTAL_CHEST = new Item() {` — 개별 처리, 인접 호출: Messages.get
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L78) `public int image() { return ItemSpriteSheet.CRYSTAL_CHEST; }` — 개별 처리, 인접 호출: Messages.get
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L79) `public String name() { return Messages.get(Heap.class, "crystal_chest"); }` — 개별 처리, 인접 호출: Messages.get
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L81) `public static final Item TOMB = new Item() {` — 개별 처리, 인접 호출: Messages.get
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L82) `public int image() { return ItemSpriteSheet.TOMB; }` — 개별 처리, 인접 호출: Messages.get
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L83) `public String name() { return Messages.get(Heap.class, "tomb"); }` — 개별 처리, 인접 호출: Messages.get
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L85) `public static final Item SKELETON = new Item() {` — 개별 처리, 인접 호출: Messages.get, PixelScene.align
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L86) `public int image() { return ItemSpriteSheet.BONES; }` — 개별 처리, 인접 호출: Messages.get, PixelScene.align
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L87) `public String name() { return Messages.get(Heap.class, "skeleton"); }` — 개별 처리, 인접 호출: Messages.get, PixelScene.align
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L89) `public static final Item REMAINS = new Item() {` — 개별 처리, 인접 호출: Messages.get, PixelScene.align
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L90) `public int image() { return ItemSpriteSheet.REMAINS; }` — 개별 처리, 인접 호출: Messages.get, PixelScene.align
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L91) `public String name() { return Messages.get(Heap.class, "remains"); }` — 개별 처리, 인접 호출: PixelScene.align
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L94) `public ItemSlot() {` — 개별 처리, 인접 호출: PixelScene.align
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L100) `public ItemSlot( Item item ) {` — 개별 처리, 인접 호출: PixelScene.align
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L106) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.align
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L124) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L175) `public void alpha( float value ){` — 개별 처리
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L184) `public void clear(){` — 개별 처리
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L192) `public void item( Item item ) {` — 개별 처리
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L220) `public void updateText(){` — 행동·상태 갱신, 인접 호출: Messages.format
- [L307](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L307) `public void enable( boolean value ) {` — 개별 처리
- [L326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L326) `public void showExtraInfo( boolean show ){` — 개별 처리, 인접 호출: Messages.titleCase
- [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L336) `public void textVisible( boolean visible ){` — 개별 처리, 인접 호출: Messages.titleCase
- [L348](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L348) `public void setMargins( int left, int top, int right, int bottom){` — 개별 처리, 인접 호출: Messages.titleCase
- [L354](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java#L354) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase

## 1144. [`KeyDisplay.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 225행.

### 클래스/타입
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L44) `public class KeyDisplay extends Visual {`

### 변수·상수 후보
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L46) `private float[] vertices = new float[16];`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L47) `private FloatBuffer quads;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L48) `private Vertexbuffer buffer;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L52) `private boolean dirty = true;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L53) `private int[] keys;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L66) `private int totalKeys = 0;`

### 메서드 및 코드 의존 단서
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L50) `private SmartTexture tx = TextureCache.get(Assets.Interfaces.MENU_BTN);` — 조회·판정, 인접 호출: Notes.getRecords
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L68) `public KeyDisplay() {` — 개별 처리, 인접 호출: Notes.getRecords, NoosaScript.get
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L72) `public void updateKeys(){` — 행동·상태 갱신, 인접 호출: Notes.getRecords, NoosaScript.get
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L91) `public int keyCount(){` — 개별 처리, 인접 호출: NoosaScript.get
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L96) `public void draw() {` — 개별 처리, 인접 호출: NoosaScript.get
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L123) `private void updateVertices(){` — 행동·상태 갱신, 인접 호출: Math.ceil, Quad.createSet
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/KeyDisplay.java#L218) `public void destroy() {` — 개별 처리

## 1145. [`LootIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 123행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java#L30) `public class LootIndicator extends Tag {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java#L32) `private ItemSlot slot;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java#L34) `private Item lastItem = null;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java#L35) `private int lastQuantity = 0;`

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java#L37) `public LootIndicator() {` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java#L46) `protected void createChildren() {` — 생성·초기화
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java#L50) `protected void onClick() {` — 이벤트·효과 실행
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java#L59) `public GameAction keyAction() {` — 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java#L64) `public GameAction secondaryTooltipAction() {` — 개별 처리
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java#L73) `protected void layout() {` — 개별 처리
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java#L87) `public void update() {` — 행동·상태 갱신

## 1146. [`MenuPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 422행.

### 클래스/타입
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L50) `public class MenuPane extends Component {`
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L230) `private static class JournalButton extends Button {`
- [L368](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L368) `private static class MenuButton extends Button {`

### 변수·상수 후보
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L52) `private Image bg;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L54) `private Image depthIcon;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L55) `private BitmapText depthText;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L56) `private Button depthButton;`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L58) `private Image challengeIcon;`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L59) `private BitmapText challengeText;`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L60) `private Button challengeButton;`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L62) `private JournalButton btnJournal;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L63) `private MenuButton btnMenu;`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L65) `private Toolbar.PickedUpItem pickedUp;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L67) `private BitmapText version;`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L68) `private NinePatch versionOverflowBG;`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L70) `private DangerIndicator danger;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L72) `public static final int WIDTH = 31;`
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L232) `private Image bg;`
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L233) `private Image journalIcon;`
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L234) `private KeyDisplay keyIcon;`
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L236) `private Document flashingDoc = null;`
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L237) `private String flashingPage = null;`
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L284) `private float time;`
- [L370](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L370) `private Image image;`

### 메서드 및 코드 의존 단서
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L75) `protected void createChildren() {` — 생성·초기화, 인접 호출: Icons.get, Integer.toString, GameScene.show, Icons.getLarge, Messages.titleCase
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L98) `protected String hoverText() {` — 개별 처리, 인접 호출: GameScene.show, Icons.getLarge, Messages.titleCase, Challenges.activeChallenges, Icons.get, Integer.toString, Messages.get
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L107) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Icons.getLarge, Messages.titleCase, Challenges.activeChallenges, Icons.get, Integer.toString, Messages.get
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L132) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.get, Toolbar.PickedUpItem, PixelScene.align, DeviceCompat.isDesktop, DeviceCompat.isDebug
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L137) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, Toolbar.PickedUpItem, PixelScene.align, DeviceCompat.isDesktop, DeviceCompat.isDebug
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L157) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, DeviceCompat.isDesktop, DeviceCompat.isDebug
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L214) `public void pickup(Item item, int cell) {` — 개별 처리
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L221) `public void flashForPage( Document doc, String page ){` — 개별 처리
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L226) `public void updateKeys(){` — 행동·상태 갱신
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L239) `public JournalButton() {` — 개별 처리, 인접 호출: PixelScene.align
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L247) `public GameAction keyAction() {` — 개별 처리, 인접 호출: PixelScene.align, Math.abs, Math.cos
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L252) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.align, Math.abs, Math.cos
- [L267](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L267) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, Math.abs, Math.cos, Math.min
- [L287](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L287) `public void update() {` — 행동·상태 갱신, 인접 호출: Math.abs, Math.cos, Math.min, INSTANCE.play
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L300) `public void updateKeyDisplay() {` — 행동·상태 갱신, 인접 호출: Math.min, INSTANCE.play, GameScene.show
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L312) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, Math.min, GameScene.show, SPDSettings.intro, GameScene.endIntro
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L318) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: Math.min, GameScene.show, SPDSettings.intro, GameScene.endIntro
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L327) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, SPDSettings.intro, GameScene.endIntro, Messages.titleCase, Messages.get
- [L345](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L345) `public void hide() {` — 개별 처리, 인접 호출: SPDSettings.intro, GameScene.endIntro, GameScene.show, Messages.titleCase, Messages.get
- [L363](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L363) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, INSTANCE.play
- [L372](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L372) `public MenuButton() {` — 개별 처리, 인접 호출: INSTANCE.play, GameScene.show
- [L380](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L380) `protected void createChildren() {` — 생성·초기화, 인접 호출: INSTANCE.play, GameScene.show, Messages.titleCase, Messages.get
- [L388](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L388) `protected void layout() {` — 개별 처리, 인접 호출: INSTANCE.play, GameScene.show, Messages.titleCase, Messages.get
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L396) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, GameScene.show, Messages.titleCase, Messages.get
- [L402](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L402) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase, Messages.get
- [L407](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L407) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase, Messages.get
- [L412](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L412) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get
- [L417](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java#L417) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get

## 1147. [`OptionSlider.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 202행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L34) `public abstract class OptionSlider extends Component {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L36) `private PointerArea pointerArea;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L38) `private RenderedTextBlock title;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L39) `private RenderedTextBlock minTxt;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L40) `private RenderedTextBlock maxTxt;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L43) `private int minVal;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L44) `private int maxVal;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L45) `private int selectedVal;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L47) `private NinePatch sliderNode;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L48) `private NinePatch BG;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L49) `private ColorBlock sliderBG;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L50) `private ColorBlock[] sliderTicks;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L51) `private float tickDist;`

### 메서드 및 코드 의존 단서
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L54) `public OptionSlider(String title, String minTxt, String maxTxt, int minVal, int maxVal){` — 개별 처리, 인접 호출: PixelScene.align
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L77) `protected abstract void onChange();` — 이벤트·효과 실행, 인접 호출: PixelScene.align, Chrome.get, BG.alpha, PixelScene.renderTextBlock, GameMath.gate
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L79) `public int getSelectedValue(){` — 조회·판정, 인접 호출: PixelScene.align, Chrome.get, BG.alpha, PixelScene.renderTextBlock, GameMath.gate
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L83) `public void setSelectedValue(int val) {` — 개별 처리, 인접 호출: PixelScene.align, Chrome.get, BG.alpha, PixelScene.renderTextBlock, GameMath.gate
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L90) `public void enable( boolean value ) {` — 개별 처리, 인접 호출: Chrome.get, BG.alpha, PixelScene.renderTextBlock, GameMath.gate, Math.round, PixelScene.align
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L99) `protected void createChildren() {` — 생성·초기화, 인접 호출: Chrome.get, BG.alpha, PixelScene.renderTextBlock, GameMath.gate, Math.round, PixelScene.align
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L117) `protected void onPointerDown( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: GameMath.gate, Math.round, PixelScene.align, PixelScene.renderTextBlock
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L125) `protected void onPointerUp( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: GameMath.gate, Math.round, PixelScene.align, PixelScene.renderTextBlock
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L141) `protected void onDrag( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: GameMath.gate, PixelScene.renderTextBlock, PixelScene.align
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java#L153) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.align, BG.size

## 1148. [`QuickRecipe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 391행.

### 클래스/타입
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L87) `public class QuickRecipe extends Component {`
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L204) `public class arrow extends IconButton {`

### 변수·상수 후보
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L89) `private ArrayList<Item> ingredients;`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L91) `private ArrayList<ItemSlot> inputs;`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L92) `private QuickRecipe.arrow arrow;`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L93) `private ItemSlot output;`

### 메서드 및 코드 의존 단서
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L95) `public QuickRecipe(Recipe.SimpleRecipe r){` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L99) `public QuickRecipe(Recipe r, ArrayList<Item> inputs, final Item output) {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, Icons.get
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L114) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, Icons.get
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L160) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L174) `protected void layout() {` — 개별 처리
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L196) `private void anonymize(Item item){` — 개별 처리, 인접 호출: Integer.toString, PixelScene.align
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L208) `public arrow(){` — 개별 처리, 인접 호출: Integer.toString, PixelScene.align
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L212) `public arrow( Image icon ){` — 개별 처리, 인접 호출: Integer.toString, PixelScene.align, ShatteredPixelDungeon.scene
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L216) `public arrow( Image icon, int count ){` — 개별 처리, 인접 호출: Integer.toString, PixelScene.align, ShatteredPixelDungeon.scene
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L226) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, ShatteredPixelDungeon.scene, Potion.SeedToPotion, Arrays.asList, Seed.PlaceHolder, WndBag.Placeholder
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L237) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, Potion.SeedToPotion, Arrays.asList, Seed.PlaceHolder, WndBag.Placeholder, Messages.get
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L242) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, Potion.SeedToPotion, Arrays.asList, Seed.PlaceHolder, WndBag.Placeholder, Messages.get, Scroll.ScrollToStone
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L259) `public void hardlightText(int color ){` — 개별 처리, 인접 호출: Potion.SeedToPotion, Arrays.asList, Seed.PlaceHolder, WndBag.Placeholder, Messages.get, Scroll.ScrollToStone, Reflection.newInstance
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L266) `public static ArrayList<QuickRecipe> getRecipes( int pageIdx ){` — 조회·판정, 인접 호출: Potion.SeedToPotion, Arrays.asList, Seed.PlaceHolder, WndBag.Placeholder, Messages.get, Scroll.ScrollToStone, Reflection.newInstance
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L272) `public String name() {` — 개별 처리, 인접 호출: Messages.get, Scroll.ScrollToStone, Reflection.newInstance, Arrays.asList, StewedMeat.oneMeat, StewedMeat.twoMeat, StewedMeat.threeMeat
- [L277](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L277) `public String info() {` — 개별 처리, 인접 호출: Scroll.ScrollToStone, Reflection.newInstance, Arrays.asList, StewedMeat.oneMeat, StewedMeat.twoMeat, StewedMeat.threeMeat, MeatPie.Recipe
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L304) `public String name(){` — 개별 처리, 인접 호출: Messages.get, ExoticPotion.PotionToExotic, Reflection.newInstance, Arrays.asList, ExoticScroll.ScrollToExotic, Bomb.EnhanceBomb, LiquidMetal.Recipe
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickRecipe.java#L309) `public String info() {` — 개별 처리, 인접 호출: ExoticPotion.PotionToExotic, Reflection.newInstance, Arrays.asList, ExoticScroll.ScrollToExotic, Bomb.EnhanceBomb, LiquidMetal.Recipe, MissileWeapon.PlaceHolder

## 1149. [`QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 415행.

### 클래스/타입
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L44) `public class QuickSlotButton extends Button {`

### 변수·상수 후보
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L46) `private static QuickSlotButton[] instance = new QuickSlotButton[QuickSlot.SIZE];`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L47) `private int slotNum;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L49) `private ItemSlot slot;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L51) `private Image crossB;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L52) `private Image crossM;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L54) `public static int targetingSlot = -1;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L55) `public static Char lastTarget = null;`
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L261) `public static int lastVisible = instance.length;`

### 메서드 및 코드 의존 단서
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L57) `public QuickSlotButton( int slotNum ) {` — 개별 처리, 인접 호출: GameScene.handleCell, GameScene.cancel, GameScene.centerNextWndOnInvPane
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L66) `public void destroy() {` — 개별 처리, 인접 호출: GameScene.handleCell, GameScene.cancel, GameScene.centerNextWndOnInvPane
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L72) `public static void reset() {` — 개별 처리, 인접 호출: GameScene.handleCell, GameScene.cancel, GameScene.centerNextWndOnInvPane
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L80) `protected void createChildren() {` — 생성·초기화, 인접 호출: GameScene.handleCell, GameScene.cancel, GameScene.centerNextWndOnInvPane
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L85) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.handleCell, GameScene.cancel, GameScene.centerNextWndOnInvPane
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L111) `protected void onRightClick() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase, Messages.get, TARGET.get
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L116) `protected void onMiddleClick() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase, Messages.get, TARGET.get
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L121) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, TARGET.get
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L125) `public GameAction secondaryTooltipAction(){` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, TARGET.get, PixelScene.align
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L129) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase, Messages.get, TARGET.get, PixelScene.align
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L133) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase, Messages.get, TARGET.get, PixelScene.align
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L137) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase, Messages.get, TARGET.get, PixelScene.align
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L142) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, TARGET.get, PixelScene.align
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L162) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L172) `public void alpha( float value ){` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L177) `public void update() {` — 행동·상태 갱신, 인접 호출: Messages.titleCase, Messages.get, GameScene.cancel, GameScene.selectItem
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L185) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, GameScene.cancel, GameScene.selectItem
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L205) `public GameAction secondaryTooltipAction() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, GameScene.cancel, GameScene.selectItem, WndBag.ItemSelector
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L210) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, GameScene.cancel, GameScene.selectItem, WndBag.ItemSelector
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L219) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.cancel, GameScene.selectItem, WndBag.ItemSelector, Messages.get
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L226) `protected void onRightClick() {` — 이벤트·효과 실행, 인접 호출: WndBag.ItemSelector, Messages.get
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L231) `protected void onMiddleClick() {` — 이벤트·효과 실행, 인접 호출: WndBag.ItemSelector, Messages.get, Item.updateQuickslot
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L236) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: WndBag.ItemSelector, Messages.get, Item.updateQuickslot, Actor.now
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L241) `private WndBag.ItemSelector itemSelector = new WndBag.ItemSelector() {` — 개별 처리, 인접 호출: Messages.get, Item.updateQuickslot, Actor.now, SPDSettings.quickslotWaterskin
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L244) `public String textPrompt() {` — 개별 처리, 인접 호출: Messages.get, Item.updateQuickslot, Actor.now, SPDSettings.quickslotWaterskin
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L249) `public boolean itemSelectable(Item item) {` — 개별 처리, 인접 호출: Item.updateQuickslot, Actor.now, SPDSettings.quickslotWaterskin
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L254) `public void onSelect(Item item) {` — 이벤트·효과 실행, 인접 호출: Item.updateQuickslot, Actor.now, SPDSettings.quickslotWaterskin
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L263) `public static void set(Item item){` — 개별 처리, 인접 호출: Item.updateQuickslot, Actor.now, SPDSettings.quickslotWaterskin
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L273) `public static void set(int slotNum, Item item){` — 개별 처리, 인접 호출: Item.updateQuickslot, Actor.now, SPDSettings.quickslotWaterskin
- [L287](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L287) `private static Item select(int slotNum){` — 개별 처리, 인접 호출: Actor.chars
- [L291](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L291) `public void item( Item item ) {` — 개별 처리, 인접 호출: Actor.chars
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L296) `public void enable( boolean value ) {` — 개별 처리, 인접 호출: Actor.chars
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L305) `private void enableSlot() {` — 개별 처리, 인접 호출: Actor.chars
- [L310](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L310) `public void slotMargins( int left, int top, int right, int bottom){` — 개별 처리, 인접 호출: Actor.chars
- [L314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L314) `public static void useTargeting(int idx){` — 이벤트·효과 실행, 인접 호출: Actor.chars
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L318) `private void useTargeting() {` — 이벤트·효과 실행, 인접 호출: Actor.chars
- [L346](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L346) `public static int autoAim(Char target){` — 개별 처리, 인접 호출: PathFinder.buildDistanceMap, BArray.not, SWAP_INSTANCE.updateVisuals, Actor.now, SPDSettings.quickslotWaterskin
- [L352](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L352) `public static int autoAim(Char target, Item item){` — 개별 처리, 인접 호출: PathFinder.buildDistanceMap, BArray.not, SWAP_INSTANCE.updateVisuals, Actor.now, SPDSettings.quickslotWaterskin
- [L374](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L374) `public static void refresh() {` — 개별 처리, 인접 호출: SWAP_INSTANCE.updateVisuals, Actor.now, SPDSettings.quickslotWaterskin, Char.hasProp
- [L394](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L394) `public static void target( Char target ) {` — 개별 처리, 인접 호출: Char.hasProp
- [L405](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java#L405) `public static void cancel() {` — 조회·판정

## 1150. [`RadialMenu.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 223행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java#L36) `public class RadialMenu extends Window {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java#L50) `public RadialMenu(String title, String desc, String[] optionTexts, Image[] optionIcons){` — 개별 처리, 인접 호출: Chrome.get, SPDSettings.interfaceSize, PixelScene.align
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java#L118) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Cursor.captureCursor
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java#L127) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: Cursor.captureCursor, Cursor.getCursorDelta, Math.abs
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java#L136) `protected void onRightClick() {` — 이벤트·효과 실행, 인접 호출: Cursor.captureCursor, Cursor.getCursorDelta, Math.abs
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java#L149) `public void onSelect(int idx, boolean alt){}` — 이벤트·효과 실행, 인접 호출: Cursor.captureCursor, Cursor.getCursorDelta, Math.abs, PointF.angle, Math.round
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java#L152) `public void destroy() {` — 개별 처리, 인접 호출: Cursor.captureCursor, Cursor.getCursorDelta, Math.abs, PointF.angle, Math.round
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java#L158) `private PointF mousePos = new PointF();` — 개별 처리, 인접 호출: Cursor.getCursorDelta, Math.abs, PointF.angle, Math.round, PixelScene.align
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java#L162) `public synchronized void update() {` — 행동·상태 갱신, 인접 호출: Cursor.getCursorDelta, Math.abs, PointF.angle, Math.round, PixelScene.align
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java#L212) `private static Image getBGTexture(int size, boolean inner){` — 조회·판정

## 1151. [`RedButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RedButton.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 37행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RedButton.java#L26) `public class RedButton extends StyledButton {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RedButton.java#L28) `public RedButton( String label ) {` — 개별 처리
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RedButton.java#L32) `public RedButton( String label, int size ){` — 개별 처리

## 1152. [`RenderedTextBlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 286행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L33) `public class RenderedTextBlock extends Component {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L35) `private int maxWidth = Integer.MAX_VALUE;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L36) `public int nLines;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L41) `protected String text;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L42) `protected String[] tokens = null;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L44) `protected boolean multiline = false;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L46) `private int size;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L47) `private float zoom;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L48) `private int color = -1;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L50) `private int hightlightColor = Window.TITLE_COLOR;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L51) `private boolean highlightingEnabled = true;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L53) `public static final int LEFT_ALIGN = 1;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L54) `public static final int CENTER_ALIGN = 2;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L55) `public static final int RIGHT_ALIGN = 3;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L56) `private int alignment = LEFT_ALIGN;`

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L38) `private static final RenderedText SPACE = new RenderedText();` — 개별 처리
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L39) `private static final RenderedText NEWLINE = new RenderedText();` — 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L58) `public RenderedTextBlock(int size){` — 개별 처리
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L62) `public RenderedTextBlock(String text, int size){` — 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L67) `public void text(String text){` — 개별 처리
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L79) `public void tokens(String... words){` — 개별 처리
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L90) `public void text(String text, int maxWidth){` — 개별 처리
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L96) `public String text(){` — 개별 처리
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L100) `public void maxWidth(int maxWidth){` — 개별 처리
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L108) `public int maxWidth(){` — 개별 처리
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L112) `private synchronized void build(){` — 생성·초기화
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L144) `public synchronized void zoom(float zoom){` — 개별 처리
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L152) `public synchronized void hardlight(int color){` — 개별 처리
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L159) `public synchronized void resetColor(){` — 개별 처리
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L166) `public synchronized void alpha(float value){` — 개별 처리
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L172) `public synchronized void setHightlighting(boolean enabled){` — 개별 처리
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L176) `public synchronized void setHightlighting(boolean enabled, int color){` — 개별 처리
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L184) `public synchronized void invert(){` — 개별 처리
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L199) `public synchronized void align(int align){` — 개별 처리, 인접 호출: Messages.lang
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java#L205) `protected synchronized void layout() {` — 개별 처리, 인접 호출: Messages.lang

## 1153. [`ResumeIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ResumeIndicator.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 93행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ResumeIndicator.java#L32) `public class ResumeIndicator extends Tag {`

### 변수·상수 후보
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ResumeIndicator.java#L34) `private Image icon;`

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ResumeIndicator.java#L36) `public ResumeIndicator() {` — 개별 처리, 인접 호출: Icons.get, PixelScene.align, Messages.titleCase, Messages.get
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ResumeIndicator.java#L46) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Icons.get, PixelScene.align, Messages.titleCase, Messages.get
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ResumeIndicator.java#L51) `protected void createChildren() {` — 생성·초기화, 인접 호출: Icons.get, PixelScene.align, Messages.titleCase, Messages.get
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ResumeIndicator.java#L59) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, Messages.titleCase, Messages.get
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ResumeIndicator.java#L69) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase, Messages.get
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ResumeIndicator.java#L77) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ResumeIndicator.java#L82) `public void update() {` — 행동·상태 갱신

## 1154. [`RightClickMenu.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 215행.

### 클래스/타입
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L41) `public class RightClickMenu extends Component {`

### 변수·상수 후보
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L43) `private NinePatch bg;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L44) `private PointerArea blocker;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L46) `private Image icon;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L47) `private RenderedTextBlock titleText;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L48) `private ColorBlock separator;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L50) `private Button topRightButton;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L52) `private RedButton[] buttons;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L54) `private Item item;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L57) `private Point childOffset;`

### 메서드 및 코드 의존 단서
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L59) `public RightClickMenu(Item item){` — 개별 처리, 인접 호출: Messages.titleCase, Chrome.get, PixelScene.renderTextBlock
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L69) `public RightClickMenu(Image icon, String title, String... options){` — 개별 처리, 인접 호출: Chrome.get, PixelScene.renderTextBlock, GameScene.centerNextWndOnInvPane
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L73) `private void setup(Image icon, String title, String... options){` — 생성·초기화, 인접 호출: Chrome.get, PixelScene.renderTextBlock, GameScene.centerNextWndOnInvPane
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L90) `public boolean onSignal(PointerEvent event) {` — 이벤트·효과 실행, 인접 호출: GameScene.centerNextWndOnInvPane, GameScene.nextWndOffset, InventoryPane.useTargeting
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L107) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.centerNextWndOnInvPane, GameScene.nextWndOffset, InventoryPane.useTargeting
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L123) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.nextWndOffset, InventoryPane.useTargeting, Math.max
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L151) `public void setChildWindowOffset(Point offset){` — 개별 처리, 인접 호출: Math.max
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L155) `public void onSelect(int index){}` — 이벤트·효과 실행, 인접 호출: Math.max
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java#L158) `protected void layout() {` — 개별 처리, 인접 호출: Math.max

## 1155. [`ScrollingGridPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 276행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L33) `public class ScrollingGridPane extends ScrollPane {`
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L168) `public static class GridItem extends Component {`
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L228) `public static class GridHeader extends Component {`

### 변수·상수 후보
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L38) `private static final int ITEM_SIZE	= 17;`
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L170) `protected Image icon;`
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L172) `protected Visual secondIcon;`
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L174) `protected ColorBlock bg;`
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L230) `protected RenderedTextBlock text;`

### 메서드 및 코드 의존 단서
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L41) `public ScrollingGridPane(){` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L46) `public void onClick(float x, float y) {` — 이벤트·효과 실행
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L54) `public void addItem( ScrollingGridPane.GridItem item ){` — 개별 처리, 인접 호출: Math.max
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L59) `public void addHeader( String text ){` — 개별 처리, 인접 호출: Math.max
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L63) `public void addHeader( String text, int size, boolean center ){` — 개별 처리, 인접 호출: Math.max
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L70) `public synchronized void clear() {` — 개별 처리, 인접 호출: Math.max
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L77) `protected void layout() {` — 개별 처리, 인접 호출: Math.max
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L176) `public GridItem( Image icon ) {` — 개별 처리, 인접 호출: PixelScene.align
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L188) `public void addSecondIcon( Visual icon ){` — 개별 처리, 인접 호출: PixelScene.align
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L194) `public void hardLightBG( float r, float g, float b ){` — 개별 처리, 인접 호출: PixelScene.align
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L198) `public boolean onClick( float x, float y ){` — 이벤트·효과 실행, 인접 호출: PixelScene.align, PixelScene.renderTextBlock
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L203) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.align, PixelScene.renderTextBlock
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L209) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, PixelScene.renderTextBlock
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L233) `public GridHeader( String text ){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L237) `public GridHeader( String text, int size, boolean center ){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L247) `protected void createChildren() {` — 생성·초기화
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L252) `protected void layout() {` — 개별 처리
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ScrollingGridPane.java#L266) `public float height() {` — 개별 처리


# Java 소스 구현 분석 1174–1191

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1174. [`WndBadge.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBadge.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 95행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBadge.java#L33) `public class WndBadge extends Window {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBadge.java#L35) `private static final int MAX_WIDTH = 125;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBadge.java#L36) `private static final int MARGIN = 4;`

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBadge.java#L38) `public WndBadge( Badges.Badge badge, boolean unlocked ) {` — 개별 처리, 인접 호출: BadgeBanner.image, PixelScene.renderTextBlock, Badges.showCompletionProgress, Math.max, PixelScene.align
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBadge.java#L87) `protected void onClick( PointerEvent event ) {` — 이벤트·효과 실행

## 1175. [`WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 490행.

### 클래스/타입
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L54) `public class WndBag extends WndTabbed {`
- [L422](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L422) `private class BagTab extends IconTab {`
- [L456](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L456) `public static class Placeholder extends Item {`
- [L478](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L478) `public abstract static class ItemSelector {`

### 변수·상수 후보
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L57) `public static Window INSTANCE;`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L59) `protected static final int COLS_P   = 5;`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L60) `protected static final int COLS_L   = 5;`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L62) `protected static int SLOT_WIDTH_P   = 28;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L63) `protected static int SLOT_WIDTH_L   = 28;`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L65) `protected static int SLOT_HEIGHT_P	= 28;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L66) `protected static int SLOT_HEIGHT_L	= 28;`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L68) `protected static final int SLOT_MARGIN	= 1;`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L70) `protected static final int TITLE_HEIGHT	= 14;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L72) `private ItemSelector selector;`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L74) `private int nCols;`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L75) `private int nRows;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L77) `private int slotWidth;`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L78) `private int slotHeight;`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L80) `protected int count;`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L81) `protected int col;`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L82) `protected int row;`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L84) `private static Bag lastBag;`
- [L424](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L424) `private Bag bag;`
- [L425](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L425) `private int index;`

### 메서드 및 코드 의존 단서
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L86) `public WndBag( Bag bag ) {` — 개별 처리, 인접 호출: INSTANCE.hide, PixelScene.landscape, Math.ceil
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L90) `public WndBag( Bag bag, ItemSelector selector ) {` — 개별 처리, 인접 호출: INSTANCE.hide, PixelScene.landscape, Math.ceil
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L145) `public ItemSelector getSelector() {` — 조회·판정, 인접 호출: PixelScene.align, Integer.toString
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L149) `public static WndBag lastBag(ItemSelector selector ) {` — 개별 처리, 인접 호출: PixelScene.align, Integer.toString
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L162) `public static WndBag getBag( ItemSelector selector ) {` — 조회·판정, 인접 호출: PixelScene.align, Integer.toString, Icons.get
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L176) `protected void placeTitle( Bag bag, int width ){` — 개별 처리, 인접 호출: PixelScene.align, Integer.toString, Icons.get
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L243) `protected void placeItems( Bag container ) {` — 개별 처리
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L280) `protected void placeItem( final Item item ) {` — 개별 처리, 인접 호출: Game.scene
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L289) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Game.scene, PointerEvent.currentHoverPos
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L309) `protected void onRightClick() {` — 이벤트·효과 실행, 인접 호출: PointerEvent.currentHoverPos, QuickSlotButton.set, Game.scene
- [L325](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L325) `public void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: PointerEvent.currentHoverPos, QuickSlotButton.set, Game.scene, KeyBindings.getActionForKey
- [L339](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L339) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: QuickSlotButton.set, Game.scene, KeyBindings.getActionForKey
- [L367](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L367) `public boolean onSignal(KeyEvent event) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getActionForKey, Game.scene, GameScene.show, Icons.get
- [L377](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L377) `public void onBackPressed() {` — 이벤트·효과 실행, 인접 호출: Game.scene, GameScene.show, Icons.get
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L385) `protected void onClick( Tab tab ) {` — 이벤트·효과 실행, 인접 호출: Game.scene, GameScene.show, Icons.get
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L396) `public void hide() {` — 개별 처리, 인접 호출: Icons.get
- [L404](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L404) `protected int tabHeight() {` — 개별 처리, 인접 호출: Icons.get
- [L408](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L408) `private Image icon( Bag bag ) {` — 개별 처리, 인접 호출: Icons.get, Messages.titleCase
- [L427](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L427) `public BagTab( Bag bag, int index ) {` — 개별 처리, 인접 호출: Messages.titleCase
- [L435](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L435) `public GameAction keyAction() {` — 개별 처리, 인접 호출: Messages.titleCase
- [L451](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L451) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase
- [L458](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L458) `public Placeholder(int image ) {` — 개별 처리
- [L463](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L463) `public String name() {` — 개별 처리
- [L468](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L468) `public boolean isIdentified() {` — 조회·판정
- [L473](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L473) `public boolean isEquipped( Hero hero ) {` — 조회·판정
- [L479](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L479) `public abstract String textPrompt();` — 개별 처리
- [L480](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L480) `public Class<?extends Bag> preferredBag(){` — 개별 처리
- [L483](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L483) `public boolean hideAfterSelecting(){` — 개별 처리
- [L486](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L486) `public abstract boolean itemSelectable( Item item );` — 개별 처리
- [L487](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java#L487) `public abstract void onSelect( Item item );` — 이벤트·효과 실행

## 1176. [`WndBlacksmith.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 558행.

### 클래스/타입
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L54) `public class WndBlacksmith extends Window {`
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L207) `protected static class WndReforge extends Window {`
- [L365](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L365) `private class HardenSelector extends WndBag.ItemSelector {`
- [L409](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L409) `private class UpgradeSelector extends WndBag.ItemSelector {`
- [L454](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L454) `public static class WndSmith extends Window {`
- [L507](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L507) `private class RewardWindow extends WndInfoItem {`

### 변수·상수 후보
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L56) `private static final int WIDTH_P = 120;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L57) `private static final int WIDTH_L = 180;`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L59) `private static final int GAP  = 2;`
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L209) `private static final int WIDTH		= 120;`
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L211) `private static final int BTN_SIZE	= 32;`
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L212) `private static final float GAP		= 2;`
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L213) `private static final float BTN_GAP	= 5;`
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L215) `private ItemButton btnPressed;`
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L217) `private ItemButton btnItem1;`
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L218) `private ItemButton btnItem2;`
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L219) `private RedButton btnReforge;`
- [L456](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L456) `private static final int WIDTH      = 128;`
- [L457](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L457) `private static final int BTN_SIZE	= 28;`
- [L458](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L458) `private static final int BTN_GAP	= 4;`
- [L459](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L459) `private static final int GAP		= 2;`

### 메서드 및 코드 의존 단서
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L61) `public WndBlacksmith( Blacksmith troll, Hero hero ) {` — 개별 처리, 인접 호출: PixelScene.landscape, Messages.titleCase, PixelScene.renderTextBlock, Messages.get, GameScene.show, GLog.i, Messages.capitalize
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L82) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase, Messages.get, GLog.i, Messages.capitalize, Quest.rewardsAvailable, Notes.remove
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L91) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: GLog.i, Messages.capitalize, Messages.get, Quest.rewardsAvailable, Notes.remove, GameScene.show, GameScene.selectItem
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L116) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.get, GameScene.selectItem, Messages.titleCase
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L126) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.selectItem, Messages.get, GameScene.show, Messages.titleCase
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L136) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.selectItem, Messages.get, GameScene.show, Messages.titleCase
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L145) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase, Messages.get
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L154) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.get, Messages.titleCase
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L170) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase, Messages.get
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L179) `protected void onSelect(int index) {` — 이벤트·효과 실행
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L221) `public WndReforge( Blacksmith troll, Window wndParent ) {` — 개별 처리, 인접 호출: Messages.titleCase, PixelScene.renderTextBlock, Messages.get, GameScene.selectItem
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L237) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.selectItem, Messages.get, INSTANCE.play, ScrollOfUpgrade.upgrade, Item.evoke
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L247) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.selectItem, Messages.get, INSTANCE.play, ScrollOfUpgrade.upgrade, Item.evoke, Buff.affect
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L257) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, ScrollOfUpgrade.upgrade, Item.evoke, Buff.affect, Badges.validateItemLevelAquired, Item.updateQuickslot, Quest.rewardsAvailable
- [L319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L319) `protected WndBag.ItemSelector itemSelector = new WndBag.ItemSelector() {` — 개별 처리, 인접 호출: Messages.get
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L322) `public String textPrompt() {` — 개별 처리, 인접 호출: Messages.get
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L327) `public Class<?extends Bag> preferredBag(){` — 개별 처리, 인접 호출: Messages.get
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L332) `public boolean itemSelectable(Item item) {` — 개별 처리, 인접 호출: Messages.get
- [L337](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L337) `public void onSelect( Item item ) {` — 이벤트·효과 실행, 인접 호출: Messages.get
- [L368](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L368) `public String textPrompt() {` — 개별 처리, 인접 호출: Messages.get, INSTANCE.play, Item.evoke, Quest.rewardsAvailable, Notes.remove
- [L373](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L373) `public Class<?extends Bag> preferredBag(){` — 개별 처리, 인접 호출: INSTANCE.play, Item.evoke, Quest.rewardsAvailable, Notes.remove, Messages.get
- [L378](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L378) `public boolean itemSelectable(Item item) {` — 개별 처리, 인접 호출: INSTANCE.play, Item.evoke, Quest.rewardsAvailable, Notes.remove, Messages.get
- [L386](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L386) `public void onSelect(Item item) {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, Item.evoke, Quest.rewardsAvailable, Notes.remove, Messages.get
- [L412](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L412) `public String textPrompt() {` — 개별 처리, 인접 호출: Messages.get, INSTANCE.play, ScrollOfUpgrade.upgrade, Item.evoke, Badges.validateItemLevelAquired, Quest.rewardsAvailable, Notes.remove
- [L417](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L417) `public Class<?extends Bag> preferredBag(){` — 개별 처리, 인접 호출: INSTANCE.play, ScrollOfUpgrade.upgrade, Item.evoke, Badges.validateItemLevelAquired, Quest.rewardsAvailable, Notes.remove, Catalog.countUse
- [L422](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L422) `public boolean itemSelectable(Item item) {` — 개별 처리, 인접 호출: INSTANCE.play, ScrollOfUpgrade.upgrade, Item.evoke, Badges.validateItemLevelAquired, Quest.rewardsAvailable, Notes.remove, Catalog.countUse
- [L430](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L430) `public void onSelect(Item item) {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, ScrollOfUpgrade.upgrade, Item.evoke, Badges.validateItemLevelAquired, Quest.rewardsAvailable, Notes.remove, Catalog.countUse
- [L461](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L461) `public WndSmith( Blacksmith troll, Hero hero ){` — 개별 처리, 인접 호출: Messages.titleCase, PixelScene.renderTextBlock, Messages.get, Quest.generateRewards, GameScene.show
- [L486](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L486) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.get, INSTANCE.play, Item.evoke, GLog.i, Messages.capitalize
- [L503](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L503) `public void onBackPressed() {` — 이벤트·효과 실행, 인접 호출: Messages.get, INSTANCE.play, Item.evoke, GLog.i, Messages.capitalize, Quest.rewardsAvailable, Notes.remove
- [L509](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L509) `public RewardWindow( Blacksmith troll, Hero hero, Item item ) {` — 개별 처리, 인접 호출: Messages.get, INSTANCE.play, Item.evoke, GLog.i, Messages.capitalize, Quest.rewardsAvailable, Notes.remove
- [L514](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L514) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, Item.evoke, GLog.i, Messages.capitalize, Messages.get, Quest.rewardsAvailable, Notes.remove
- [L544](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBlacksmith.java#L544) `protected void onClick() {` — 이벤트·효과 실행

## 1177. [`WndChallenges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 114행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java#L37) `public class WndChallenges extends Window {`

### 변수·상수 후보
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java#L39) `private static final int WIDTH		= 120;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java#L40) `private static final int TTL_HEIGHT = 16;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java#L41) `private static final int BTN_HEIGHT = 16;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java#L42) `private static final int GAP        = 1;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java#L44) `private boolean editable;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java#L45) `private ArrayList<CheckBox> boxes;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java#L67) `final String challenge = Challenges.NAME_IDS[i];`

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java#L47) `public WndChallenges( int checked, boolean editable ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.get, PixelScene.align, Messages.titleCase, Icons.get, ShatteredPixelDungeon.scene
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java#L83) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, Messages.get, SPDSettings.challenges
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java#L100) `public void onBackPressed() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.challenges

## 1178. [`WndChooseAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 168행.

### 클래스/타입
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java#L43) `public class WndChooseAbility extends Window {`

### 변수·상수 후보
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java#L45) `private static final int WIDTH		= 130;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java#L46) `private static final float GAP		= 2;`

### 메서드 및 코드 의존 단서
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java#L48) `public WndChooseAbility(final KingsCrown crown, final Armor armor, final Hero hero){` — 개별 처리, 인접 호출: Messages.titleCase, SHUFFLE.get, GameScene.show, Messages.get, Random.oneOf, Math.abs, Math.cos
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java#L61) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, SHUFFLE.get, Messages.get, Random.oneOf, Math.abs, Math.cos, PixelScene.renderTextBlock
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java#L69) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: Random.oneOf, GameScene.show, Math.abs, Math.cos, Messages.get, PixelScene.renderTextBlock, Messages.titleCase
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java#L82) `public void update() {` — 행동·상태 갱신, 인접 호출: Math.abs, Math.cos, Messages.get, PixelScene.renderTextBlock, GameScene.show, Messages.titleCase
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java#L90) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, PixelScene.renderTextBlock, GameScene.show, Messages.titleCase
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java#L111) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase, Messages.get, Icons.get
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java#L119) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: Icons.get, GameScene.show, Messages.get
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java#L142) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.get
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseAbility.java#L154) `protected void onClick() {` — 이벤트·효과 실행

## 1179. [`WndChooseSubclass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 153행.

### 클래스/타입
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java#L42) `public class WndChooseSubclass extends Window {`

### 변수·상수 후보
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java#L44) `private static final int WIDTH		= 130;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java#L45) `private static final float GAP		= 2;`

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java#L47) `public WndChooseSubclass(final TengusMask tome, final Hero hero ) {` — 개별 처리, 인접 호출: SHUFFLE.get, GameScene.show, Messages.get, Random.oneOf, Math.abs, Math.cos
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java#L59) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, SHUFFLE.get, Messages.get, Random.oneOf, Math.abs, Math.cos, PixelScene.renderTextBlock
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java#L67) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: Random.oneOf, GameScene.show, Math.abs, Math.cos, Messages.get, PixelScene.renderTextBlock, Messages.titleCase
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java#L80) `public void update() {` — 행동·상태 갱신, 인접 호출: Math.abs, Math.cos, Messages.get, PixelScene.renderTextBlock, GameScene.show, Messages.titleCase
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java#L88) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, PixelScene.renderTextBlock, GameScene.show, Messages.titleCase, Icons.get
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java#L105) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase, Messages.get, Icons.get
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java#L112) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: Icons.get, GameScene.show, Messages.get
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java#L131) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.get
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChooseSubclass.java#L143) `protected void onClick() {` — 이벤트·효과 실행

## 1180. [`WndClericSpells.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 266행.

### 클래스/타입
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L53) `public class WndClericSpells extends Window {`
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L132) `public class SpellButton extends IconButton {`

### 변수·상수 후보
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L55) `protected static final int WIDTH    = 120;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L57) `public static int BTN_SIZE = 20;`

### 메서드 및 코드 의존 단서
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L59) `public WndClericSpells(HolyTome tome, Hero cleric, boolean info){` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, INFO.get, GameScene.show, PixelScene.renderTextBlock, DeviceCompat.isDesktop, ClericSpell.getSpellList
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L73) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, PixelScene.renderTextBlock, Messages.get, DeviceCompat.isDesktop, ClericSpell.getSpellList
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L140) `public SpellButton(ClericSpell spell, HolyTome tome, boolean info){` — 개별 처리, 인접 호출: Chrome.get
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L158) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase, GLog.w, Messages.get, QuickSlotButton.useTargeting
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L166) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase, GLog.w, Messages.get, QuickSlotButton.useTargeting
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L176) `protected void layout() {` — 개별 처리, 인접 호출: GameScene.show, Messages.titleCase, GLog.w, Messages.get, QuickSlotButton.useTargeting
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L187) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase, GLog.w, Messages.get, QuickSlotButton.useTargeting
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L209) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase, Messages.get, GLog.w, QuickSlotButton.useTargeting, GameScene.show
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L216) `protected void onRightClick() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase, Messages.get, GLog.w, QuickSlotButton.useTargeting, GameScene.show, PointerEvent.currentHoverPos
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L224) `public void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: GLog.w, Messages.get, QuickSlotButton.useTargeting, GameScene.show, Messages.titleCase, PointerEvent.currentHoverPos
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndClericSpells.java#L260) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase

## 1181. [`WndCombo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndCombo.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 90행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndCombo.java#L36) `public class WndCombo extends Window {`

### 변수·상수 후보
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndCombo.java#L38) `private static final int WIDTH_P = 120;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndCombo.java#L39) `private static final int WIDTH_L = 180;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndCombo.java#L41) `private static final int MARGIN  = 2;`

### 메서드 및 코드 의존 단서
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndCombo.java#L43) `public WndCombo( Combo combo ){` — 개별 처리, 인접 호출: PixelScene.landscape, PixelScene.renderTextBlock, Messages.titleCase, Messages.get, ComboMove.values
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndCombo.java#L69) `protected void onClick() {` — 이벤트·효과 실행

## 1182. [`WndDailies.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDailies.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 148행.

### 클래스/타입
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDailies.java#L45) `public class WndDailies extends Window {`

### 변수·상수 후보
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDailies.java#L47) `private static final int WIDTH			= 115;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDailies.java#L48) `private static final int HEIGHT			= 144;`

### 메서드 및 코드 의존 단서
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDailies.java#L50) `public WndDailies(){` — 개별 처리, 인접 호출: CALENDAR.get, Messages.get, Icons.get, ShatteredPixelDungeon.scene, PixelScene.renderTextBlock
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDailies.java#L69) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, PixelScene.renderTextBlock, Messages.get, NumberFormat.getInstance, Messages.locale, TimeZone.getTimeZone, Collections.reverse
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDailies.java#L74) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: PixelScene.renderTextBlock, Messages.get, NumberFormat.getInstance, Messages.locale, TimeZone.getTimeZone, Collections.reverse
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDailies.java#L123) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, PixelScene.renderTextBlock

## 1183. [`WndDocument.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDocument.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 76행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDocument.java#L30) `public class WndDocument extends Window {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDocument.java#L32) `private ScrollingListPane list;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDocument.java#L34) `public WndDocument(Document doc){` — 개별 처리, 인접 호출: Messages.titleCase, ScrollingListPane.ListItem, Messages.get, ShatteredPixelDungeon.scene, Math.min
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndDocument.java#L48) `public boolean onClick(float x, float y) {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, Math.min

## 1184. [`WndEnergizeItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 209행.

### 클래스/타입
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L40) `public class WndEnergizeItem extends WndInfoItem {`

### 변수·상수 후보
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L42) `private static final float GAP		= 2;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L43) `private static final int BTN_HEIGHT	= 18;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L45) `private WndBag owner;`

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L47) `public WndEnergizeItem(Item item, WndBag owner) {` — 개별 처리, 인접 호출: Messages.get, Game.scene, Messages.titleCase
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L58) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Game.scene, Messages.titleCase, Messages.get
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L66) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: Messages.get
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L74) `public void hide() {` — 개별 처리, 인접 호출: Messages.get
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L96) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.get
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L106) `protected void onClick() {` — 이벤트·효과 실행
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L124) `public void hide() {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L134) `public static void energizeAll(Item item ) {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, GLog.h, GameScene.selectItem, WndBag.getBag
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L143) `public static void energizeOne( Item item ) {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, GLog.h, GameScene.selectItem, WndBag.getBag, WndBag.ItemSelector, Messages.get
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L152) `private static void energize(Item item){` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, GLog.h, GameScene.selectItem, WndBag.getBag, WndBag.ItemSelector, Messages.get
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L174) `public static WndBag openItemSelector(){` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, GameScene.selectItem, WndBag.getBag, WndBag.ItemSelector, Messages.get, GameScene.show
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L184) `public static WndBag.ItemSelector selector = new WndBag.ItemSelector() {` — 개별 처리, 인접 호출: Messages.get, ShatteredPixelDungeon.scene, GameScene.show
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L186) `public String textPrompt() {` — 개별 처리, 인접 호출: Messages.get, ShatteredPixelDungeon.scene, GameScene.show
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L191) `public boolean itemSelectable(Item item) {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene, GameScene.show
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java#L196) `public void onSelect(Item item) {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, GameScene.show

## 1185. [`WndError.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndError.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 34행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndError.java#L27) `public class WndError extends WndTitledMessage {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndError.java#L29) `public WndError( String message ) {` — 개별 처리, 인접 호출: WARNING.get, Messages.get

## 1186. [`WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 132행.

### 클래스/타입
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L41) `public class WndGame extends Window {`

### 변수·상수 후보
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L43) `private static final int WIDTH		= 120;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L44) `private static final int BTN_HEIGHT	= 20;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L45) `private static final int GAP		= 2;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L47) `private int pos;`

### 메서드 및 코드 의존 단서
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L49) `public WndGame() {` — 개별 처리, 인접 호출: Messages.get, GameScene.show, Icons.get, GamesInProgress.firstEmpty, ShatteredPixelDungeon.switchScene
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L57) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Icons.get, Messages.get, GamesInProgress.firstEmpty, ShatteredPixelDungeon.switchScene, Game.switchScene
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L68) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Icons.get, Messages.get, GamesInProgress.firstEmpty, ShatteredPixelDungeon.switchScene, Game.switchScene, Dungeon.saveAll
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L81) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GamesInProgress.firstEmpty, ShatteredPixelDungeon.switchScene, Icons.get, Messages.get, Game.switchScene, Dungeon.saveAll, ShatteredPixelDungeon.reportException
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L92) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Game.switchScene, Icons.get, Messages.get, Dungeon.saveAll, ShatteredPixelDungeon.reportException, SPDSettings.intro
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L103) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Dungeon.saveAll, ShatteredPixelDungeon.reportException, Game.switchScene, Icons.get, SPDSettings.intro
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L118) `private void addButton( RedButton btn ) {` — 개별 처리
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java#L124) `private void addButtons( RedButton btn1, RedButton btn2 ) {` — 개별 처리

## 1187. [`WndGameInProgress.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 191행.

### 클래스/타입
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java#L44) `public class WndGameInProgress extends Window {`

### 변수·상수 후보
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java#L46) `private static final int WIDTH    = 120;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java#L48) `private int GAP	  = 6;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java#L50) `private float pos;`

### 메서드 및 코드 의존 단서
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java#L52) `public WndGameInProgress(final int slot){` — 개별 처리, 인접 호출: GamesInProgress.check, HeroSprite.avatar, Messages.get, Game.scene, Icons.get
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java#L54) `final GamesInProgress.Info info = GamesInProgress.check(slot);` — 개별 처리, 인접 호출: HeroSprite.avatar, Messages.get, Game.scene, Icons.get, Hero.maxExp
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java#L77) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Game.scene, Icons.get, Messages.get, Hero.maxExp, DungeonSeed.convertToCode
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java#L118) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ActionIndicator.clearAction, ShatteredPixelDungeon.switchScene, Messages.get, ShatteredPixelDungeon.scene, Icons.get, Dungeon.deleteGame, ShatteredPixelDungeon.switchNoFade
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java#L133) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, Icons.get, Messages.get, Dungeon.deleteGame, ShatteredPixelDungeon.switchNoFade, PixelScene.renderTextBlock, PixelScene.align
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java#L142) `protected void onSelect( int index ) {` — 이벤트·효과 실행, 인접 호출: Dungeon.deleteGame, ShatteredPixelDungeon.switchNoFade, Icons.get, PixelScene.renderTextBlock, PixelScene.align
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java#L163) `private void statSlot( String label, String value ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.align, Integer.toString
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGameInProgress.java#L187) `private void statSlot( String label, int value ) {` — 개별 처리, 인접 호출: Integer.toString

## 1188. [`WndHardNotification.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHardNotification.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 85행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHardNotification.java#L31) `public class WndHardNotification extends WndTitledMessage{`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHardNotification.java#L35) `private double timeLeft;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHardNotification.java#L36) `private String btnMessage;`

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHardNotification.java#L38) `public WndHardNotification( Image icon, String title, String message, String btnMessage, int time) {` — 개별 처리, 인접 호출: Math.ceil
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHardNotification.java#L42) `public WndHardNotification(Component titlebar, String message, String btnMessage, int time) {` — 개별 처리, 인접 호출: Math.ceil
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHardNotification.java#L50) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Math.ceil
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHardNotification.java#L64) `public void update() {` — 행동·상태 갱신, 인접 호출: Math.ceil
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHardNotification.java#L81) `public void onBackPressed() {` — 이벤트·효과 실행

## 1189. [`WndHero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 364행.

### 클래스/타입
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L55) `public class WndHero extends WndTabbed {`
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L138) `private class StatsTab extends Group {`
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L249) `public class TalentsTab extends Component {`
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L268) `private class BuffsTab extends Component {`
- [L316](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L316) `private class BuffSlot extends Component {`

### 변수·상수 후보
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L57) `private static final int WIDTH		= 120;`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L58) `private static final int HEIGHT		= 120;`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L60) `private StatsTab stats;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L61) `private TalentsTab talents;`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L62) `private BuffsTab buffs;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L64) `public static int lastIdx = 0;`
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L140) `private static final int GAP = 6;`
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L142) `private float pos;`
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L270) `private static final int GAP = 2;`
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L272) `private float pos;`
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L273) `private ScrollPane buffList;`
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L318) `private Buff buff;`

### 메서드 및 코드 의존 단서
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L66) `public WndHero() {` — 개별 처리, 인접 호출: Icons.get
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L85) `protected void select( boolean value ) {` — 개별 처리, 인접 호출: Icons.get, KeyBindings.getActionForKey
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L97) `protected void select( boolean value ) {` — 개별 처리, 인접 호출: Icons.get, KeyBindings.getActionForKey
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L105) `protected void select( boolean value ) {` — 개별 처리, 인접 호출: KeyBindings.getActionForKey
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L122) `public boolean onSignal(KeyEvent event) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getActionForKey, HeroSprite.avatar, Messages.get
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L132) `public void offset(int xOffset, int yOffset) {` — 개별 처리, 인접 호출: HeroSprite.avatar, Messages.get, Icons.get, ShatteredPixelDungeon.scene, GameScene.show
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L144) `public StatsTab() {` — 개별 처리, 인접 호출: HeroSprite.avatar, Messages.get, Icons.get, ShatteredPixelDungeon.scene, GameScene.show, Messages.titleCase
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L148) `public void initialize(){` — 생성·초기화, 인접 호출: HeroSprite.avatar, Messages.get, Icons.get, ShatteredPixelDungeon.scene, GameScene.show, Messages.titleCase
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L169) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, GameScene.show, Messages.titleCase, Messages.get, DungeonSeed.convertToCode
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L179) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, DungeonSeed.convertToCode, PixelScene.renderTextBlock
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L216) `private void statSlot( String label, String value ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.align, Integer.toString
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L240) `private void statSlot( String label, int value ) {` — 개별 처리, 인접 호출: Integer.toString
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L244) `public float height() {` — 개별 처리
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L254) `protected void createChildren() {` — 생성·초기화
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L261) `protected void layout() {` — 개별 처리
- [L277](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L277) `protected void createChildren() {` — 생성·초기화
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L283) `public void onClick( float x, float y ) {` — 이벤트·효과 실행
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L296) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, PixelScene.align
- [L301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L301) `private void setupList() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, PixelScene.align
- [L323](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L323) `public BuffSlot( Buff buff ){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, PixelScene.align, GameScene.show
- [L342](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L342) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, GameScene.show
- [L353](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java#L353) `protected boolean onClick ( float x, float y ) {` — 이벤트·효과 실행, 인접 호출: GameScene.show

## 1190. [`WndHeroInfo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 399행.

### 클래스/타입
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L46) `public class WndHeroInfo extends WndTabbed {`
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L154) `private static class HeroInfoTab extends Component {`
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L241) `private static class TalentInfoTab extends Component {`
- [L278](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L278) `private static class SubclassInfoTab extends Component {`
- [L338](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L338) `private static class ArmorAbilityInfoTab extends Component {`

### 변수·상수 후보
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L48) `private HeroInfoTab heroInfo;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L49) `private TalentInfoTab talentInfo;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L50) `private SubclassInfoTab subclassInfo;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L51) `private ArmorAbilityInfoTab abilityInfo;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L53) `private static int WIDTH = 120;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L54) `private static int MIN_HEIGHT = 125;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L55) `private static int MARGIN = 2;`
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L156) `private RenderedTextBlock title;`
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L157) `private RenderedTextBlock[] info;`
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L158) `private Image[] icons;`
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L243) `private RenderedTextBlock title;`
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L244) `private RenderedTextBlock message;`
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L245) `private TalentsPane talentPane;`
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L280) `private RenderedTextBlock title;`
- [L281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L281) `private RenderedTextBlock message;`
- [L282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L282) `private RenderedTextBlock[] subClsDescs;`
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L283) `private IconButton[] subClsInfos;`
- [L340](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L340) `private RenderedTextBlock title;`
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L341) `private RenderedTextBlock message;`
- [L342](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L342) `private RenderedTextBlock[] abilityDescs;`
- [L343](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L343) `private IconButton[] abilityInfos;`

### 메서드 및 코드 의존 단서
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L57) `public WndHeroInfo( HeroClass cl ){` — 개별 처리, 인접 호출: Math.max, Icons.get
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L90) `protected void select(boolean value) {` — 개별 처리, 인접 호출: Math.max, Icons.get, Badges.isUnlocked, DeviceCompat.isDebug
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L103) `protected void select(boolean value) {` — 개별 처리, 인접 호출: Badges.isUnlocked, DeviceCompat.isDebug, Math.max
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L117) `protected void select(boolean value) {` — 개별 처리, 인접 호출: Badges.isUnlocked, DeviceCompat.isDebug, Math.max
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L132) `protected void select(boolean value) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L149) `public void offset(int xOffset, int yOffset) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, Icons.get
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L160) `public HeroInfoTab(HeroClass cls){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, Icons.get, GRASS.get
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L218) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, Math.max, PixelScene.renderTextBlock, Messages.titleCase, Messages.get, Talent.initClassTalents
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L247) `public TalentInfoTab( HeroClass cls ){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, Messages.get, Talent.initClassTalents, Math.max
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L265) `protected void layout() {` — 개별 처리, 인접 호출: Math.max, PixelScene.renderTextBlock, Messages.titleCase, Messages.get, Icons.get, Game.scene
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L285) `public SubclassInfoTab( HeroClass cls ){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, Messages.get, Icons.get, Game.scene
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L304) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Game.scene, Math.max, PixelScene.renderTextBlock, Messages.titleCase, Messages.get
- [L315](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L315) `protected void layout() {` — 개별 처리, 인접 호출: Math.max, PixelScene.renderTextBlock, Messages.titleCase, Messages.get
- [L345](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L345) `public ArmorAbilityInfoTab(HeroClass cls){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, Messages.get, Icons.get, Game.scene
- [L364](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L364) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Game.scene, Math.max
- [L375](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java#L375) `protected void layout() {` — 개별 처리, 인접 호출: Math.max

## 1191. [`WndImpOld.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndImpOld.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 88행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndImpOld.java#L36) `public class WndImpOld extends Window {`

### 변수·상수 후보
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndImpOld.java#L38) `private static final int WIDTH      = 120;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndImpOld.java#L39) `private static final int BTN_HEIGHT = 20;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndImpOld.java#L40) `private static final int GAP        = 2;`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndImpOld.java#L42) `public WndImpOld( final Imp imp, final DwarfToken tokens ) {` — 개별 처리, 인접 호출: Messages.titleCase, PixelScene.renderTextBlock, Messages.get, GLog.i, Messages.capitalize, Quest.oldComplete
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndImpOld.java#L59) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GLog.i, Messages.capitalize, Messages.get, Quest.oldComplete
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndImpOld.java#L69) `private void takeReward( Imp imp, DwarfToken tokens, Item reward ) {` — 개별 처리, 인접 호출: GLog.i, Messages.capitalize, Messages.get, Quest.oldComplete


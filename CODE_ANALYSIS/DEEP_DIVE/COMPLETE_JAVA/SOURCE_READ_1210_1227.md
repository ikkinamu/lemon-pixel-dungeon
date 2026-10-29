# Java 소스 구현 분석 1210–1227

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1210. [`WndQuickBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuickBag.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 185행.

### 클래스/타입
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuickBag.java#L46) `public class WndQuickBag extends Window {`

### 변수·상수 후보
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuickBag.java#L48) `private static Item bag;`

### 메서드 및 코드 의존 단서
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuickBag.java#L50) `public WndQuickBag(Bag bag){` — 개별 처리, 인접 호출: Chrome.get, INSTANCE.hide, PixelScene.landscape, Collections.sort, Math.ceil
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuickBag.java#L100) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Game.scene, QuickSlotButton.useTargeting, PixelScene.renderTextBlock, Messages.titleCase, Messages.get
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuickBag.java#L118) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: Game.scene, PixelScene.renderTextBlock, Messages.titleCase, Messages.get, PixelScene.align
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuickBag.java#L124) `protected String hoverText() {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, Messages.get, PixelScene.align
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuickBag.java#L165) `public int compare( Item lhs, Item rhs ) {` — 개별 처리, 인접 호출: Category.order
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuickBag.java#L177) `public void hide() {` — 개별 처리

## 1211. [`WndRanking.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 642행.

### 클래스/타입
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L70) `public class WndRanking extends WndTabbed {`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L144) `private class RankingTab extends IconTab {`
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L162) `private class StatsTab extends Group {`
- [L328](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L328) `private class TalentsTab extends Group{`
- [L353](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L353) `private class ItemsTab extends Group {`
- [L438](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L438) `private class WndVaultItems extends Window {`
- [L448](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L448) `private class BadgesTab extends Group {`
- [L466](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L466) `private class ChallengesTab extends Group{`
- [L508](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L508) `private class ItemButton extends Button {`
- [L590](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L590) `private class QuickSlotButton extends ItemSlot{`

### 변수·상수 후보
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L72) `private static final int WIDTH			= 115;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L73) `private static final int HEIGHT			= 144;`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L75) `private static WndRanking INSTANCE;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L77) `private String gameID;`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L78) `private Rankings.Record record;`
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L146) `private Group page;`
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L164) `private int GAP	= 4;`
- [L355](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L355) `private float pos;`
- [L477](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L477) `final String challenge = Challenges.NAME_IDS[i];`
- [L510](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L510) `public static final int HEIGHT	= 23;`
- [L512](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L512) `private Item item;`
- [L514](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L514) `private ItemSlot slot;`
- [L515](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L515) `private ColorBlock bg;`
- [L516](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L516) `private RenderedTextBlock name;`
- [L592](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L592) `private Item item;`
- [L593](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L593) `private ColorBlock bg;`

### 메서드 및 코드 의존 단서
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L80) `public WndRanking( final Rankings.Record rec ) {` — 개별 처리, 인접 호출: INSTANCE.hide, Badges.loadGlobal, INSTANCE.loadGameData, Game.reportException
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L105) `public void destroy() {` — 개별 처리, 인접 호출: Icons.get
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L112) `private void createControls() {` — 생성·초기화, 인접 호출: Icons.get
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L148) `public RankingTab( Icons icon, Group page ) {` — 개별 처리, 인접 호출: Icons.get, HeroSprite.avatar, Messages.get, PixelScene.renderTextBlock
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L154) `protected void select( boolean value ) {` — 개별 처리, 인접 호출: HeroSprite.avatar, Messages.get, PixelScene.renderTextBlock
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L166) `public StatsTab() {` — 개별 처리, 인접 호출: HeroSprite.avatar, Messages.get, PixelScene.renderTextBlock, NumberFormat.getInstance, Messages.locale, WARNING.get
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L220) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, Messages.get, Integer.toString, DungeonSeed.convertToCode
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L272) `final Image icon = Icons.get(Icons.SEED);` — 조회·판정, 인접 호출: Messages.get, ShatteredPixelDungeon.scene, SPDSettings.customSeed, DungeonSeed.convertToCode, DungeonSeed.convertFromText, PixelScene.renderTextBlock, PixelScene.align
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L275) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, Messages.get, SPDSettings.customSeed, DungeonSeed.convertToCode, DungeonSeed.convertFromText, PixelScene.renderTextBlock, PixelScene.align
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L283) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: SPDSettings.customSeed, DungeonSeed.convertToCode, DungeonSeed.convertFromText, PixelScene.renderTextBlock, PixelScene.align
- [L303](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L303) `private float statSlot( Group parent, String label, String value, float pos ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L330](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L330) `public TalentsTab(){` — 개별 처리
- [L357](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L357) `public ItemsTab() {` — 개별 처리, 인접 호출: Math.min
- [L417](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L417) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, Badges.filterReplacedBadges
- [L429](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L429) `private void addItem( Item item ) {` — 개별 처리, 인접 호출: Badges.filterReplacedBadges
- [L440](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L440) `public WndVaultItems(){` — 개별 처리, 인접 호출: Badges.filterReplacedBadges, Messages.titleCase, Messages.get
- [L450](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L450) `public BadgesTab() {` — 개별 처리, 인접 호출: Badges.filterReplacedBadges, Messages.titleCase, Messages.get, Icons.get, ShatteredPixelDungeon.scene
- [L468](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L468) `public ChallengesTab(){` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, Icons.get, ShatteredPixelDungeon.scene
- [L492](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L492) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, Messages.get
- [L518](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L518) `public ItemButton( Item item ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L541](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L541) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, PixelScene.align, Messages.titleCase, INSTANCE.play
- [L556](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L556) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, Messages.titleCase, INSTANCE.play, Game.scene
- [L575](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L575) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, Game.scene
- [L580](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L580) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: Game.scene
- [L585](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L585) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Game.scene, INSTANCE.play
- [L609](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L609) `protected void createChildren() {` — 생성·초기화, 인접 호출: INSTANCE.play, Game.scene
- [L617](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L617) `protected void layout() {` — 개별 처리, 인접 호출: INSTANCE.play, Game.scene
- [L627](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L627) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, Game.scene
- [L632](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L632) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: Game.scene
- [L637](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndRanking.java#L637) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Game.scene

## 1212. [`WndResurrect.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 184행.

### 클래스/타입
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L42) `public class WndResurrect extends Window {`

### 변수·상수 후보
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L44) `private static final int WIDTH		= 120;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L45) `private static final int BTN_HEIGHT	= 20;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L46) `private static final float GAP		= 2;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L47) `private static final float BTN_GAP  = 10;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L49) `private static final int BTN_SIZE	= 36;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L51) `public static Object instance;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L53) `private ItemButton btnItem1;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L54) `private ItemButton btnItem2;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L55) `private ItemButton btnPressed;`

### 메서드 및 코드 의존 단서
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L59) `public WndResurrect( final Ankh ankh ) {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, PixelScene.renderTextBlock, GameScene.selectItem, GameScene.show, WARNING.get
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L78) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.selectItem, Messages.get, GameScene.show, WARNING.get
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L89) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.selectItem, Messages.get, GameScene.show, WARNING.get, Catalog.countUse
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L100) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, WARNING.get, Messages.get, Catalog.countUse, Game.switchScene, WndBag.ItemSelector
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L108) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: Catalog.countUse, Game.switchScene, WndBag.ItemSelector, Messages.get
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L125) `private void resurrect( final Ankh ankh ){` — 개별 처리, 인접 호출: Catalog.countUse, Game.switchScene, WndBag.ItemSelector, Messages.get
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L144) `protected WndBag.ItemSelector itemSelector = new WndBag.ItemSelector() {` — 개별 처리, 인접 호출: Messages.get
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L147) `public String textPrompt() {` — 개별 처리, 인접 호출: Messages.get
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L152) `public boolean itemSelectable(Item item) {` — 개별 처리
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L158) `public void onSelect( Item item ) {` — 이벤트·효과 실행
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L175) `public void destroy() {` — 개별 처리
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java#L181) `public void onBackPressed() {` — 이벤트·효과 실행

## 1213. [`WndSadGhost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 160행.

### 클래스/타입
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L41) `public class WndSadGhost extends Window {`
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L132) `private class RewardWindow extends WndInfoItem {`

### 변수·상수 후보
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L43) `private static final int WIDTH		= 120;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L44) `private static final int BTN_SIZE	= 32;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L45) `private static final int BTN_GAP	= 5;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L46) `private static final int GAP		= 2;`

### 메서드 및 코드 의존 단서
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L50) `public WndSadGhost( final Ghost ghost, final int type ) {` — 개별 처리, 인접 호출: Messages.get, PixelScene.renderTextBlock, GameScene.show
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L86) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, GLog.i, Messages.capitalize, Messages.get, Quest.complete
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L96) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, GLog.i, Messages.capitalize, Messages.get, Quest.complete
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L107) `private void selectReward( Item reward ) {` — 개별 처리, 인접 호출: GLog.i, Messages.capitalize, Messages.get, Quest.complete
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L134) `public RewardWindow( Item item ) {` — 개별 처리, 인접 호출: Messages.get
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L139) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.get
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java#L150) `protected void onClick() {` — 이벤트·효과 실행

## 1214. [`WndScoreBreakdown.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndScoreBreakdown.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 122행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndScoreBreakdown.java#L36) `public class WndScoreBreakdown extends Window {`

### 변수·상수 후보
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndScoreBreakdown.java#L38) `private static final int WIDTH			= 115;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndScoreBreakdown.java#L40) `private int GAP	= 4;`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndScoreBreakdown.java#L42) `public WndScoreBreakdown(){` — 개별 처리, 인접 호출: Icons.get, Messages.get, NumberFormat.getInstance, Messages.locale, Messages.decimalFormat
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndScoreBreakdown.java#L92) `private float statSlot(Group parent, String label, String value, float pos, boolean highlight ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndScoreBreakdown.java#L108) `private float addInfo(Group parent, String info, float pos){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock

## 1215. [`WndSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 1262행.

### 클래스/타입
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L56) `public class WndSettings extends WndTabbed {`
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L218) `private static class DisplayTab extends Component {`
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L359) `private static class UITab extends Component {`
- [L655](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L655) `private static class InputTab extends Component{`
- [L777](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L777) `private static class DataTab extends Component{`
- [L880](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L880) `private static class AudioTab extends Component {`
- [L1032](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1032) `private static class LangsTab extends Component{`

### 변수·상수 후보
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L58) `private static final int WIDTH_P	    = 122;`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L59) `private static final int WIDTH_L	    = 223;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L61) `private static final int SLIDER_HEIGHT	= 21;`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L62) `private static final int BTN_HEIGHT	    = 16;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L63) `private static final float GAP          = 1;`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L65) `private DisplayTab  display;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L66) `private UITab       ui;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L67) `private InputTab    input;`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L68) `private DataTab     data;`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L69) `private AudioTab    audio;`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L70) `private LangsTab    langs;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L72) `public static int last_index = 0;`
- [L1034](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1034) `final static int COLS_P = 3;`
- [L1035](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1035) `final static int COLS_L = 6;`
- [L1037](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1037) `final static int BTN_HEIGHT = 11;`
- [L1083](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1083) `final int langIndex = i;`

### 메서드 및 코드 의존 단서
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L74) `public WndSettings() {` — 개별 처리, 인접 호출: PixelScene.landscape, Icons.get, Math.max, DeviceCompat.hasHardKeyboard, ControllerHandler.isControllerConnected
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L88) `protected void select(boolean value) {` — 개별 처리, 인접 호출: Math.max, Icons.get, DeviceCompat.hasHardKeyboard, ControllerHandler.isControllerConnected
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L102) `protected void select(boolean value) {` — 개별 처리, 인접 호출: Math.max, DeviceCompat.hasHardKeyboard, ControllerHandler.isControllerConnected, Icons.get
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L123) `protected void select(boolean value) {` — 개별 처리, 인접 호출: Math.max, Icons.get
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L138) `protected void select(boolean value) {` — 개별 처리, 인접 호출: Math.max, Icons.get, Messages.lang
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L152) `protected void select(boolean value) {` — 개별 처리, 인접 호출: Math.max, Icons.get, Messages.lang, Math.ceil
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L167) `protected void select(boolean value) {` — 개별 처리, 인접 호출: Messages.lang, Math.ceil, ShatteredPixelDungeon.seamlessResetScene, Game.SceneChangeCallback
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L174) `protected void createChildren() {` — 생성·초기화, 인접 호출: Messages.lang, Math.ceil, ShatteredPixelDungeon.seamlessResetScene, Game.SceneChangeCallback
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L203) `public void hide() {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.seamlessResetScene, Game.SceneChangeCallback, PixelScene.renderTextBlock, Messages.get, DeviceCompat.isAndroid, DeviceCompat.isiOS
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L208) `public void beforeCreate() {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.get, DeviceCompat.isAndroid, DeviceCompat.isiOS, SPDSettings.fullscreen
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L212) `public void afterCreate() {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.get, DeviceCompat.isAndroid, DeviceCompat.isiOS, SPDSettings.fullscreen
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L231) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, Messages.get, DeviceCompat.isAndroid, DeviceCompat.isiOS, SPDSettings.fullscreen, SPDSettings.landscape
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L247) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.fullscreen, DeviceCompat.isAndroid, Messages.get, SPDSettings.landscape, SPDSettings.brightness, SPDSettings.visualGrid
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L263) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.landscape, Messages.get, SPDSettings.brightness, SPDSettings.visualGrid, SPDSettings.cameraFollow
- [L278](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L278) `protected void onChange() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.brightness, Messages.get, SPDSettings.visualGrid, SPDSettings.cameraFollow, SPDSettings.screenShake
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L288) `protected void onChange() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.visualGrid, Messages.get, SPDSettings.cameraFollow, SPDSettings.screenShake
- [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L298) `protected void onChange() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.cameraFollow, Messages.get, SPDSettings.screenShake
- [L308](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L308) `protected void onChange() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.screenShake
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L318) `protected void layout() {` — 개별 처리
- [L373](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L373) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, Messages.get, Math.min, SPDSettings.interfaceSize, ShatteredPixelDungeon.seamlessResetScene, Math.ceil, SPDSettings.scale
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L393) `protected void onChange() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.interfaceSize, ShatteredPixelDungeon.seamlessResetScene, Math.ceil, Messages.get, SPDSettings.scale, ShatteredPixelDungeon.scene, PixelScene.renderTextBlock
- [L409](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L409) `protected void onChange() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.scale, ShatteredPixelDungeon.seamlessResetScene, SPDSettings.interfaceSize, Messages.get, ShatteredPixelDungeon.scene, PixelScene.renderTextBlock, SPDSettings.toolbarMode
- [L423](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L423) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, PixelScene.renderTextBlock, Messages.get, SPDSettings.toolbarMode, SPLIT.name, Toolbar.updateLayout, GROUP.name
- [L439](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L439) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.toolbarMode, SPLIT.name, Toolbar.updateLayout, Messages.get, GROUP.name, CENTER.name
- [L454](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L454) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.toolbarMode, GROUP.name, Toolbar.updateLayout, Messages.get, CENTER.name, SPDSettings.quickSwapper, PixelScene.renderTextBlock
- [L469](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L469) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.toolbarMode, CENTER.name, Toolbar.updateLayout, Messages.get, SPDSettings.quickSwapper, PixelScene.renderTextBlock, SPDSettings.flipToolbar
- [L484](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L484) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.quickSwapper, Toolbar.updateLayout, PixelScene.renderTextBlock, Messages.get, SPDSettings.flipToolbar, SPDSettings.flipTags, GameScene.layoutTags
- [L499](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L499) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.flipToolbar, Toolbar.updateLayout, Messages.get, SPDSettings.flipTags, GameScene.layoutTags, PixelScene.align
- [L510](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L510) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.flipTags, GameScene.layoutTags, PixelScene.align, Messages.get
- [L555](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L555) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.flipTags, GameScene.layoutTags, Messages.get, ShatteredPixelDungeon.seamlessResetScene, Game.SceneChangeCallback, SPDSettings.systemFont, SPDSettings.vibration
- [L571](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L571) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.seamlessResetScene, Game.SceneChangeCallback, SPDSettings.systemFont, Messages.get, SPDSettings.vibration, Game.vibrate
- [L575](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L575) `public void beforeCreate() {` — 개별 처리, 인접 호출: SPDSettings.systemFont, Messages.get, SPDSettings.vibration, Game.vibrate
- [L580](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L580) `public void afterCreate() {` — 개별 처리, 인접 호출: SPDSettings.systemFont, Messages.get, SPDSettings.vibration, Game.vibrate
- [L591](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L591) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.vibration, Game.vibrate
- [L607](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L607) `protected void layout() {` — 개별 처리
- [L669](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L669) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, Messages.get, DeviceCompat.hasHardKeyboard, ShatteredPixelDungeon.scene, ControllerHandler.isControllerConnected
- [L681](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L681) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, ControllerHandler.isControllerConnected, Messages.get, SPDSettings.controllerPointerSensitivity
- [L693](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L693) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, Messages.get, SPDSettings.controllerPointerSensitivity, SPDSettings.movementHoldSensitivity
- [L714](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L714) `protected void onChange() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.controllerPointerSensitivity, Messages.get, SPDSettings.movementHoldSensitivity
- [L729](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L729) `protected void onChange() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.movementHoldSensitivity
- [L738](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L738) `protected void layout() {` — 개별 처리
- [L787](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L787) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, Messages.get, SPDSettings.news, News.clearArticles, Updates.supportsUpdates, Updates.supportsUpdatePrompts, SPDSettings.updates
- [L797](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L797) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.news, News.clearArticles, Updates.supportsUpdates, Updates.supportsUpdatePrompts, Messages.get, SPDSettings.updates, Updates.clearUpdate
- [L809](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L809) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.updates, Updates.clearUpdate, Updates.supportsBetaChannel, Messages.get, SPDSettings.betas, DeviceCompat.isDesktop, SPDSettings.WiFi
- [L821](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L821) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.betas, Updates.clearUpdate, DeviceCompat.isDesktop, Messages.get, SPDSettings.WiFi
- [L835](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L835) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.WiFi
- [L846](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L846) `protected void layout() {` — 개별 처리
- [L894](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L894) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, Messages.get, SPDSettings.musicVol, SPDSettings.music, SPDSettings.SFXVol, Random.Int, INSTANCE.play
- [L904](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L904) `protected void onChange() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.musicVol, Messages.get, SPDSettings.music, SPDSettings.SFXVol, Random.Int, INSTANCE.play, Random.oneOf
- [L913](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L913) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.music, Messages.get, SPDSettings.SFXVol, Random.Int, INSTANCE.play, Random.oneOf, SPDSettings.soundFx
- [L926](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L926) `protected void onChange() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.SFXVol, Random.Int, INSTANCE.play, Random.oneOf, Messages.get, SPDSettings.soundFx, DeviceCompat.isiOS
- [L945](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L945) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.soundFx, INSTANCE.play, DeviceCompat.isiOS, Messages.get, SPDSettings.ignoreSilentMode, DeviceCompat.isDesktop, SPDSettings.playMusicInBackground
- [L961](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L961) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.ignoreSilentMode, DeviceCompat.isDesktop, Messages.get, SPDSettings.playMusicInBackground
- [L976](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L976) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.playMusicInBackground
- [L987](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L987) `protected void layout() {` — 개별 처리
- [L1049](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1049) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, Messages.get, Arrays.asList, Languages.values, Languages.matchLocale, Locale.getDefault, Messages.lang
- [L1057](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1057) `final ArrayList<Languages> langs = new ArrayList<>(Arrays.asList(Languages.values()));` — 개별 처리, 인접 호출: Languages.matchLocale, Locale.getDefault, Messages.lang, PixelScene.renderTextBlock, Messages.titleCase, Messages.get, Messages.setup
- [L1064](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1064) `final Languages currLang = Messages.lang();` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, Messages.get, Messages.setup, ShatteredPixelDungeon.seamlessResetScene, Game.SceneChangeCallback, SPDSettings.language
- [L1086](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1086) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.setup, ShatteredPixelDungeon.seamlessResetScene, Game.SceneChangeCallback, SPDSettings.language, GameLog.wipe, PixelScene.renderTextBlock, Messages.get
- [L1091](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1091) `public void beforeCreate() {` — 개별 처리, 인접 호출: SPDSettings.language, GameLog.wipe, PixelScene.renderTextBlock, Messages.get, Messages.titleCase
- [L1097](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1097) `public void afterCreate() {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.get, Messages.titleCase
- [L1130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1130) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase, Messages.get
- [L1210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java#L1210) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.landscape, Math.floor, Math.max

## 1216. [`WndStory.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 114행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L33) `public class WndStory extends Window {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L35) `private static final int WIDTH_P = 125;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L36) `private static final int WIDTH_L = 180;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L37) `private static final int MARGIN = 2;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L39) `private IconTitle ttl;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L40) `private RenderedTextBlock tf;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L42) `private float appearDelay;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L43) `private float disappearDelay;`

### 메서드 및 코드 의존 단서
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L45) `public WndStory( String text ) {` — 개별 처리, 인접 호출: Chrome.get, PixelScene.landscape, PixelScene.renderTextBlock
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L49) `public WndStory(Image icon, String title, String text ) {` — 개별 처리, 인접 호출: Chrome.get, PixelScene.landscape, PixelScene.renderTextBlock
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L71) `protected void onClick( PointerEvent event ) {` — 이벤트·효과 실행
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L81) `public WndStory setDelays(float appearDelay, float disappearDelay){` — 개별 처리
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L93) `public void onBackPressed() {` — 이벤트·효과 실행
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndStory.java#L100) `public void update() {` — 행동·상태 갱신

## 1217. [`WndSupportPrompt.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSupportPrompt.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 97행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSupportPrompt.java#L35) `public class WndSupportPrompt extends Window {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSupportPrompt.java#L37) `protected static final int WIDTH_P    = 120;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSupportPrompt.java#L38) `protected static final int WIDTH_L    = 200;`

### 메서드 및 코드 의존 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSupportPrompt.java#L40) `public WndSupportPrompt(){` — 개별 처리, 인접 호출: PixelScene.landscape, Icons.get, Messages.get, Messages.lang, PixelScene.renderTextBlock, SPDSettings.supportNagged
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSupportPrompt.java#L62) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.supportNagged, Messages.get
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSupportPrompt.java#L79) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDSettings.supportNagged
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSupportPrompt.java#L93) `public void hide() {` — 개별 처리

## 1218. [`WndTabbed.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 292행.

### 클래스/타입
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L42) `public class WndTabbed extends Window {`
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L163) `protected class Tab extends Button {`
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L207) `protected class LabeledTab extends Tab {`
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L244) `protected class IconTab extends Tab {`

### 변수·상수 후보
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L45) `protected Tab selected;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L47) `private Signal.Listener<KeyEvent> tabListener;`
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L165) `protected final int CUT = 5;`
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L167) `protected boolean selected;`
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L169) `protected NinePatch bg;`
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L209) `private RenderedTextBlock btLabel;`
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L246) `protected Image icon;`
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L247) `private RectF defaultFrame;`

### 메서드 및 코드 의존 단서
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L49) `public WndTabbed() {` — 개별 처리, 인접 호출: Chrome.get, KeyEvent.addKeyListener, KeyBindings.getActionForKey, KeyEvent.removeKeyListener
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L54) `public boolean onSignal(KeyEvent keyEvent) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getActionForKey, KeyEvent.removeKeyListener
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L71) `public void destroy() {` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L76) `protected Tab add(Tab tab ) {` — 개별 처리
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L89) `public void select( int index ) {` — 개별 처리
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L93) `public void select( Tab tab ) {` — 개별 처리
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L108) `public void resize( int w, int h ) {` — 개별 처리, 인접 호출: PixelScene.align
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L140) `public void layoutTabs(){` — 개별 처리, 인접 호출: PixelScene.align
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L155) `protected int tabHeight() {` — 개별 처리, 인접 호출: Chrome.get
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L159) `protected void onClick( Tab tab ) {` — 이벤트·효과 실행, 인접 호출: Chrome.get, INSTANCE.play
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L172) `protected void layout() {` — 개별 처리, 인접 호출: Chrome.get, INSTANCE.play
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L182) `protected void select( boolean value ) {` — 개별 처리, 인접 호출: Chrome.get, INSTANCE.play, PixelScene.renderTextBlock
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L199) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, PixelScene.renderTextBlock, PixelScene.align
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L211) `public LabeledTab( String label ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L219) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, PixelScene.align
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L227) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L238) `protected void select( boolean value ) {` — 개별 처리, 인접 호출: PixelScene.align
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L249) `public IconTab( Image icon ){` — 개별 처리, 인접 호출: PixelScene.align
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L257) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.align
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L265) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTabbed.java#L285) `protected void select( boolean value ) {` — 개별 처리

## 1219. [`WndTextInput.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 237행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L36) `public class WndTextInput extends Window {`

### 변수·상수 후보
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L38) `private static final int WIDTH = 135;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L40) `private static final int MARGIN = 1;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L41) `private static final int BUTTON_HEIGHT = 16;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L43) `protected TextInput textBox;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L45) `protected RedButton btnCopy;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L46) `protected RedButton btnPaste;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L52) `final int width;`
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L105) `final float inputHeight;`
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L181) `final RedButton negativeBtn;`

### 메서드 및 코드 의존 단서
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L62) `final RenderedTextBlock txtTitle = PixelScene.renderTextBlock(title, 9);` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Chrome.get
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L72) `final RenderedTextBlock txtBody = PixelScene.renderTextBlock(body, 6);` — 개별 처리, 인접 호출: Chrome.get
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L83) `public void enterPressed() {` — 개별 처리
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L90) `public void onChanged() {` — 이벤트·효과 실행
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L96) `public void onClipBoardUpdate() {` — 이벤트·효과 실행, 인접 호출: COPY.get
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L119) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: COPY.get
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L125) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: COPY.get, PASTE.get
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L131) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: COPY.get, PASTE.get
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L142) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: PASTE.get
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L148) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: PASTE.get
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L154) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: PASTE.get
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L173) `final RedButton positiveBtn = new RedButton(posTxt) {` — 개별 처리, 인접 호출: DeviceCompat.hasHardKeyboard
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L175) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: DeviceCompat.hasHardKeyboard
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L185) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: DeviceCompat.hasHardKeyboard
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L223) `public void offset(int xOffset, int yOffset) {` — 개별 처리
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L230) `public void onSelect(boolean positive, String text){ }` — 이벤트·효과 실행
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java#L233) `public void onBackPressed() {` — 이벤트·효과 실행

## 1220. [`WndTitledMessage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTitledMessage.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 79행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTitledMessage.java#L30) `public class WndTitledMessage extends Window {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTitledMessage.java#L32) `protected static final int WIDTH_MIN    = 120;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTitledMessage.java#L33) `protected static final int WIDTH_MAX    = 220;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTitledMessage.java#L34) `protected static final int GAP	= 2;`

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTitledMessage.java#L36) `public WndTitledMessage( Image icon, String title, String message ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.landscape
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTitledMessage.java#L42) `public WndTitledMessage( Component titlebar, String message ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.landscape
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTitledMessage.java#L71) `protected boolean useHighlighting(){` — 이벤트·효과 실행
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTitledMessage.java#L75) `protected float targetHeight() {` — 개별 처리

## 1221. [`WndTradeItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 306행.

### 클래스/타입
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L48) `public class WndTradeItem extends WndInfoItem {`

### 변수·상수 후보
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L50) `private static final float GAP		= 2;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L51) `private static final int BTN_HEIGHT	= 18;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L53) `private WndBag owner;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L55) `private boolean selling = false;`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L76) `final Shopkeeper finalShop = shop;`

### 메서드 및 코드 의존 단서
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L58) `public WndTradeItem( final Item item, WndBag owner ) {` — 개별 처리, 인접 호출: Actor.chars, PixelScene.renderTextBlock, Messages.get
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L91) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.get
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L107) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.get, Shopkeeper.sellPrice
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L117) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Shopkeeper.sellPrice, Messages.get
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L134) `public WndTradeItem( final Heap heap ) {` — 개별 처리, 인접 호출: Shopkeeper.sellPrice, Messages.get, Math.min, GameScene.show
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L145) `final int price = Shopkeeper.sellPrice( item );` — 개별 처리, 인접 호출: Messages.get, Math.min, GameScene.show, Messages.titleCase
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L149) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.get, Math.min, GameScene.show, Messages.titleCase
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L161) `final MasterThievesArmband.Thievery thievery = Dungeon.hero.buff(MasterThievesArmband.Thievery.class);` — 개별 처리, 인접 호출: Messages.get, Math.min, GameScene.show, Messages.titleCase
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L163) `final float chance = thievery.stealChance(item);` — 개별 처리, 인접 호출: Messages.get, Math.min, GameScene.show, Messages.titleCase
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L164) `final int chargesToUse = thievery.chargesToUse(item);` — 개별 처리, 인접 호출: Messages.get, Math.min, GameScene.show, Messages.titleCase
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L167) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase, Messages.get
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L184) `protected void onSelect(int index) {` — 이벤트·효과 실행, 인접 호출: Messages.get
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L223) `public void hide() {` — 개별 처리, 인접 호출: Shopkeeper.sell, Buff.affect
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L234) `public static void sell( Item item ) {` — 개별 처리, 인접 호출: Buff.affect
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L238) `public static void sell( Item item, Shopkeeper shop ) {` — 개별 처리, 인접 호출: Buff.affect
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L264) `public static void sellOne( Item item ) {` — 개별 처리, 인접 호출: Shopkeeper.sellPrice, Catalog.countUses
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L268) `public static void sellOne( Item item, Shopkeeper shop ) {` — 개별 처리, 인접 호출: Shopkeeper.sellPrice, Catalog.countUses
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java#L292) `private void buy( Heap heap ) {` — 개별 처리, 인접 호출: Shopkeeper.sellPrice, Catalog.countUses

## 1222. [`WndUpgrade.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 555행.

### 클래스/타입
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L58) `public class WndUpgrade extends Window {`

### 변수·상수 후보
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L60) `private static final int WIDTH = 120;`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L62) `private static final float COL_1 = WIDTH/4f;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L63) `private static final float COL_2 = 5*WIDTH/8f;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L64) `private static final float COL_3 = 7*WIDTH/8f;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L66) `private static final int GAP	= 2;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L67) `private static final int ITEMSLOT_SIZE = 18;`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L69) `private Item upgrader;`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L70) `private boolean force;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L72) `private RedButton btnUpgrade;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L73) `private RedButton btnCancel;`

### 메서드 및 코드 의존 단서
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L75) `public WndUpgrade( Item upgrader, Item toUpgrade, boolean force){` — 개별 처리, 인접 호출: Messages.get, PixelScene.renderTextBlock
- [L433](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L433) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ScrollOfUpgrade.upgrade, INSTANCE.play, GameScene.show, Messages.get
- [L463](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L463) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: EXIT.get
- [L489](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L489) `public synchronized void update() {` — 행동·상태 갱신, 인접 호출: Messages.lang, PixelScene.renderTextBlock, PixelScene.align
- [L497](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L497) `public void onBackPressed() {` — 이벤트·효과 실행, 인접 호출: Messages.lang, PixelScene.renderTextBlock, PixelScene.align
- [L506](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L506) `public WndBag.ItemSelector getItemSelector(){` — 조회·판정, 인접 호출: Messages.lang, PixelScene.renderTextBlock, PixelScene.align
- [L515](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L515) `private float fillFields(String title, String msg1, String msg2, float bottom){` — 개별 처리, 인접 호출: Messages.lang, PixelScene.renderTextBlock, PixelScene.align
- [L544](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java#L544) `private float addMessage(String text, int color, float bottom){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock

## 1223. [`WndUseItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUseItem.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 179행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUseItem.java#L33) `public class WndUseItem extends WndInfoItem {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUseItem.java#L35) `private static final float BUTTON_HEIGHT	= 16;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUseItem.java#L37) `private static final float GAP	= 2;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUseItem.java#L39) `public Window owner;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUseItem.java#L40) `public Item item;`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUseItem.java#L42) `public WndUseItem( final Window owner, final Item item ) {` — 개별 처리, 인접 호출: Item.updateQuickslot, InventoryPane.useTargeting
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUseItem.java#L58) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Item.updateQuickslot, InventoryPane.useTargeting
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUseItem.java#L89) `private static float layoutButtons(ArrayList<RedButton> buttons, float width, float y){` — 개별 처리

## 1224. [`WndVictoryCongrats.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndVictoryCongrats.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 144행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndVictoryCongrats.java#L36) `public class WndVictoryCongrats extends Window {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndVictoryCongrats.java#L38) `public WndVictoryCongrats(){` — 개별 처리, 인접 호출: PixelScene.landscape, Messages.get, PixelScene.renderTextBlock, CHALLENGE_COLOR.get, PixelScene.align, Math.max
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndVictoryCongrats.java#L117) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.switchScene, GOLD.get, Messages.get, EXIT.get
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndVictoryCongrats.java#L127) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: EXIT.get
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndVictoryCongrats.java#L140) `public void onBackPressed() {` — 이벤트·효과 실행

## 1225. [`WndWandmaker.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 163행.

### 클래스/타입
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L40) `public class WndWandmaker extends Window {`
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L133) `private class RewardWindow extends WndInfoItem {`

### 변수·상수 후보
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L42) `private static final int WIDTH		= 120;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L43) `private static final int BTN_SIZE	= 32;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L44) `private static final int BTN_GAP	= 5;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L45) `private static final int GAP		= 2;`

### 메서드 및 코드 의존 단서
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L50) `public WndWandmaker( final Wandmaker wandmaker, final Item item ) {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, PixelScene.renderTextBlock, GameScene.show
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L79) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, GLog.i, Messages.capitalize, Messages.get
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L93) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, GLog.i, Messages.capitalize, Messages.get, Messages.titleCase, Quest.complete
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L108) `private void selectReward( Item reward ) {` — 개별 처리, 인접 호출: GLog.i, Messages.capitalize, Messages.get, Messages.titleCase, Quest.complete
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L135) `public RewardWindow( Item item ) {` — 개별 처리, 인접 호출: Messages.get
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L140) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.get
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndWandmaker.java#L151) `protected void onClick() {` — 이벤트·효과 실행

## 1226. [`DesktopLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.desktop`, 195행.

### 클래스/타입
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java#L48) `public class DesktopLauncher {`

### 변수·상수 후보
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java#L66) `final String title;`

### 메서드 및 코드 의존 단서
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java#L50) `public static void main (String[] args) {` — 개별 처리, 인접 호출: DesktopLaunchValidator.verifyValidJVMState, System.getProperty, Thread.setDefaultUncaughtExceptionHandler, Thread.UncaughtExceptionHandler, Game.reportException
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java#L75) `public void uncaughtException(Thread thread, Throwable throwable) {` — 개별 처리, 인접 호출: Game.reportException, TinyFileDialogs.tinyfd_messageBox, System.exit

## 1227. [`DesktopLaunchValidator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLaunchValidator.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.desktop`, 98행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLaunchValidator.java#L32) `public class DesktopLaunchValidator {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLaunchValidator.java#L37) `public static boolean verifyValidJVMState(String[] args){` — 개별 처리, 인접 호출: System.getenv, ManagementFactory.getRuntimeMXBean, System.getProperty


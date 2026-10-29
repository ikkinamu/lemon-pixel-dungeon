# 소모품·무기·방어구·반지·유물 구현 심층 분석

소스 고정 커밋 `d6f487f29ae86d0da317e088e5ad81d52378bc5b`. 실제 Java 본문을 열어 **선언, 상태, 메서드, 주요 클래스 호출을 정적 분석**. 클래스명에 나타난 게임 내 효과가 어떤 수치·조건으로 적용되는지는 연결된 원문에서 확인할 것. 인접 24줄 탐지는 정확한 함수 범위를 판정하는 AST가 아니므로 참고 단서로 사용.

## [items/potions/PotionOfHealing.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java)

- Java 93줄. **타입:** `public class PotionOfHealing extends Potion {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java#L52) | `public void apply( Hero hero ) {` | 효과 적용; 주변 코드에 `Dungeon.isChallenged`, `Buff.affect`, `GLog.p`, `Messages.get` 호출 표현 |
| [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java#L58) | `public static void heal( Char ch ){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Dungeon.isChallenged`, `Buff.affect`, `GLog.p`, `Messages.get`, `Buff.detach` 호출 표현 |
| [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java#L71) | `public static void pharmacophobiaProc( Hero hero ){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Buff.affect`, `Buff.detach` 호출 표현 |
| [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java#L76) | `public static void cure( Char ch ) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Buff.detach` 호출 표현 |
| [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java#L89) | `public int value() {` | 선언 확인(세부 반환/부작용은 본문 참조) |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/potions/PotionOfStrength.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfStrength.java)

- Java 65줄. **타입:** `public class PotionOfStrength extends Potion {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfStrength.java#L43) | `public void apply( Hero hero ) {` | 효과 적용; 주변 코드에 `GLog.p`, `Messages.get`, `Badges.validateStrengthAttained`, `Badges.validateDuelistUnlock` 호출 표현 |
| [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfStrength.java#L56) | `public int value() {` | 선언 확인(세부 반환/부작용은 본문 참조) |
| [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfStrength.java#L61) | `public int energyVal() {` | 선언 확인(세부 반환/부작용은 본문 참조) |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/potions/PotionOfInvisibility.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfInvisibility.java)

- Java 53줄. **타입:** `public class PotionOfInvisibility extends Potion {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfInvisibility.java#L40) | `public void apply( Hero hero ) {` | 효과 적용; 주변 코드에 `Buff.prolong`, `GLog.i`, `Messages.get`, `INSTANCE.play` 호출 표현 |
| [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfInvisibility.java#L48) | `public int value() {` | 선언 확인(세부 반환/부작용은 본문 참조) |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/scrolls/ScrollOfUpgrade.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java)

- Java 174줄. **타입:** `public class ScrollOfUpgrade extends InventoryScroll {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L57) | `protected boolean usableOnItem(Item item) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `GameScene.show`, `GameScene.selectItem` 호출 표현 |
| [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L62) | `protected void onItemSelected( Item item ) {` | 이벤트/효과 트리거; 주변 코드에 `GameScene.show`, `GameScene.selectItem`, `Degrade.detach` 호출 표현 |
| [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L68) | `public void reShowSelector(boolean force){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `GameScene.selectItem`, `Degrade.detach` 호출 표현 |
| [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L74) | `public WndBag.ItemSelector getSelector(boolean force){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Degrade.detach` 호출 표현 |
| [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L80) | `public Item upgradeItem( Item item ){` | 강화; 주변 코드에 `Degrade.detach`, `GLog.w`, `Messages.get` 호출 표현 |
| [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L149) | `public static void upgrade( Hero hero ) {` | 강화; 주변 코드에 `Speck.factory`, `GLog.p`, `Messages.get`, `Badges.validateClericUnlock` 호출 표현 |
| [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L153) | `public static void weakenCurse( Hero hero ){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `GLog.p`, `Messages.get`, `Badges.validateClericUnlock` 호출 표현 |
| [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L158) | `public static void removeCurse( Hero hero ){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `GLog.p`, `Messages.get`, `Badges.validateClericUnlock` 호출 표현 |
| [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L165) | `public int value() {` | 선언 확인(세부 반환/부작용은 본문 참조) |
| [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L170) | `public int energyVal() {` | 선언 확인(세부 반환/부작용은 본문 참조) |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/scrolls/ScrollOfIdentify.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java)

- Java 88줄. **타입:** `public class ScrollOfIdentify extends InventoryScroll {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java#L45) | `protected boolean usableOnItem(Item item) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `ShardOfOblivion.passiveIDDisabled`, `GLog.p`, `Messages.get` 호출 표현 |
| [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java#L50) | `protected void onItemSelected( Item item ) {` | 이벤트/효과 트리거; 주변 코드에 `ShardOfOblivion.passiveIDDisabled`, `GLog.p`, `Messages.get` 호출 표현 |
| [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java#L57) | `public static void IDItem( Item item ){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `ShardOfOblivion.passiveIDDisabled`, `GLog.p`, `Messages.get`, `GLog.i`, `Badges.validateItemLevelAquired` 호출 표현 |
| [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java#L84) | `public int value() {` | 선언 확인(세부 반환/부작용은 본문 참조) |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/scrolls/ScrollOfTeleportation.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java)

- Java 340줄. **타입:** `public class ScrollOfTeleportation extends Scroll {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L60) | `public void doRead() {` | 작동; 주변 코드에 `INSTANCE.play`, `PathFinder.buildDistanceMap`, `BArray.or`, `Actor.findChar`, `GLog.w`, `Messages.get` 호출 표현 |
| [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L72) | `public static boolean teleportToLocation(Char ch, int pos){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `PathFinder.buildDistanceMap`, `BArray.or`, `Actor.findChar`, `GLog.w`, `Messages.get`, `Buff.detach`, `Dungeon.observe` 호출 표현 |
| [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L94) | `public static boolean teleportChar( Char ch ) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Char.hasProp`, `GLog.w`, `Messages.get` 호출 표현 |
| [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L98) | `public static boolean teleportChar( Char ch, Class source ) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Char.hasProp`, `GLog.w`, `Messages.get` 호출 표현 |
| [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L142) | `public static boolean teleportPreferringUnseen( Hero hero ){` | 선언 확인(세부 반환/부작용은 본문 참조) |
| [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L221) | `private static boolean teleportInNonRegularLevel(Char ch, boolean preferNotSeen ){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Char.hasProp`, `GLog.w`, `Messages.get`, `BArray.and`, `PathFinder.buildDistanceMap`, `Actor.findChar` 호출 표현 |
| [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L284) | `public static void appear( Char ch, int pos ) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `INSTANCE.play`, `CellEmitter.get`, `Speck.factory` 호출 표현 |
| [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L318) | `public static void appearVFX( Char ch ){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `INSTANCE.play`, `Speck.factory` 호출 표현 |
| [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L336) | `public int value() {` | 선언 확인(세부 반환/부작용은 본문 참조) |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/wands/WandOfFireblast.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java)

- Java 294줄. **타입:** `public class WandOfFireblast extends DamageWand {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L66) | `public int min(int lvl){` | 선언 확인(세부 반환/부작용은 본문 참조) |
| [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L71) | `public int max(int lvl){` | 선언 확인(세부 반환/부작용은 본문 참조) |
| [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L85) | `public void onZap(Ballistica bolt) {` | 이벤트/효과 트리거; 주변 코드에 `Level.set`, `GameScene.updateMap` 호출 표현 |
| [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L157) | `public void onHit(MagesStaff staff, Char attacker, Char defender, int damage) {` | 이벤트/효과 트리거; 주변 코드에 `Actor.findChar`, `Fire.volumeAt`, `Math.min`, `Wand.procChanceMultiplier`, `Random.Float`, `Math.max` 호출 표현 |
| [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L215) | `public void fx(Ballistica bolt, Callback callback) {` | 선언 확인(세부 반환/부작용은 본문 참조) |
| [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L251) | `protected int chargesPerCast() {` | 충전; 주변 코드에 `GameMath.gate`, `Math.ceil`, `Messages.get` 호출 표현 |
| [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L261) | `public String statsDesc() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Messages.get` 호출 표현 |
| [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L269) | `public String upgradeStat1(int level) {` | 강화 |
| [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L274) | `public String upgradeStat2(int level) {` | 강화 |
| [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L279) | `public String upgradeStat3(int level) {` | 강화 |
| [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L284) | `public void staffFx(MagesStaff.StaffParticle particle) {` | 선언 확인(세부 반환/부작용은 본문 참조) |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/wands/WandOfFrost.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java)

- Java 169줄. **타입:** `public class WandOfFrost extends DamageWand {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L50) | `public int min(int lvl){` | 선언 확인(세부 반환/부작용은 본문 참조) |
| [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L54) | `public int max(int lvl){` | 선언 확인(세부 반환/부작용은 본문 참조) |
| [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L59) | `public void onZap(Ballistica bolt) {` | 이벤트/효과 트리거; 주변 코드에 `Actor.findChar` 호출 표현 |
| [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L113) | `public String upgradeStat2(int level) {` | 강화; 주변 코드에 `Integer.toString`, `MagicMissile.boltFromChar`, `INSTANCE.play`, `Math.floor`, `Random.Float` 호출 표현 |
| [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L118) | `public void fx(Ballistica bolt, Callback callback) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `MagicMissile.boltFromChar`, `INSTANCE.play`, `Math.floor`, `Random.Float`, `Math.max` 호출 표현 |
| [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L128) | `public void onHit(MagesStaff staff, Char attacker, Char defender, int damage) {` | 이벤트/효과 트리거; 주변 코드에 `Math.floor`, `Random.Float`, `Math.max`, `Buff.affect`, `Math.round` 호출 표현 |
| [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L147) | `public boolean act() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Buff.affect`, `Math.round`, `Random.Float` 호출 표현 |
| [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L157) | `public void staffFx(MagesStaff.StaffParticle particle) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Random.Float` 호출 표현 |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/wands/WandOfMagicMissile.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java)

- Java 167줄. **타입:** `public class WandOfMagicMissile extends DamageWand {`; `public static class MagicCharge extends FlavourBuff {`.
- **주요 필드:** [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L102) `public static float DURATION = 4f;`; [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L104) `private int level = 0;`; [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L151) `private static final String LEVEL = "level";`.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L47) | `public int min(int lvl){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Actor.findChar`, `INSTANCE.play`, `Random.Float`, `Buff.prolong` 호출 표현 |
| [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L51) | `public int max(int lvl){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Actor.findChar`, `INSTANCE.play`, `Random.Float`, `Buff.prolong` 호출 표현 |
| [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L56) | `public void onZap(Ballistica bolt) {` | 이벤트/효과 트리거; 주변 코드에 `Actor.findChar`, `INSTANCE.play`, `Random.Float`, `Buff.prolong` 호출 표현 |
| [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L81) | `public void onHit(MagesStaff staff, Char attacker, Char defender, int damage) {` | 이벤트/효과 트리거; 주변 코드에 `SpellSprite.show` 호출 표현 |
| [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L91) | `public int initialCharges() {` | 선언 확인(세부 반환/부작용은 본문 참조) |
| [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L107) | `public void setup(Wand wand){` | 선언 확인(세부 반환/부작용은 본문 참조) |
| [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L115) | `public void detach() {` | 선언 확인(세부 반환/부작용은 본문 참조) |
| [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L120) | `public int level(){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.max` 호출 표현 |
| [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L125) | `public Wand wandJustApplied(){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.max`, `Messages.get` 호출 표현 |
| [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L132) | `public int icon() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.max`, `Messages.get` 호출 표현 |
| [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L137) | `public void tintIcon(Image icon) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.max`, `Messages.get` 호출 표현 |
| [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L142) | `public float iconFadePercent() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.max`, `Messages.get` 호출 표현 |
| [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L147) | `public String desc() {` | 설명 문자열; 주변 코드에 `Messages.get` 호출 표현 |
| [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L154) | `public void storeInBundle(Bundle bundle) {` | 저장 |
| [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L160) | `public void restoreFromBundle(Bundle bundle) {` | 복원 |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/weapon/melee/Sword.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java)

- Java 153줄. **타입:** `public class Sword extends MeleeWeapon {`; `public static class CleaveTracker extends FlavourBuff {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L51) | `protected int baseChargeUse(Hero hero, Char target){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Messages.get`, `Sword.cleaveAbility` 호출 표현 |
| [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L60) | `public String targetingPrompt() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Messages.get`, `Sword.cleaveAbility` 호출 표현 |
| [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L65) | `protected void duelistAbility(Hero hero, Integer target) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Sword.cleaveAbility`, `Messages.get` 호출 표현 |
| [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L72) | `public String abilityInfo() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Messages.get`, `Actor.findChar`, `GLog.w` 호출 표현 |
| [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L81) | `public String upgradeAbilityStat(int level){` | 강화; 주변 코드에 `Actor.findChar`, `GLog.w`, `Messages.get` 호출 표현 |
| [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L86) | `public static void cleaveAbility(Hero hero, Integer target, float dmgMulti, int dmgBoost, MeleeWeapon wep){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Actor.findChar`, `GLog.w`, `Messages.get`, `AttackIndicator.target` 호출 표현 |
| [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L107) | `public void call() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `AttackIndicator.target`, `INSTANCE.play`, `Invisibility.dispel`, `Buff.prolong` 호출 표현 |
| [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L142) | `public int icon() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.max` 호출 표현 |
| [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L147) | `public float iconFadePercent() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.max` 호출 표현 |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/weapon/melee/Dagger.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java)

- Java 145줄. **타입:** `public class Dagger extends MeleeWeapon {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L56) | `public int max(int lvl) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Hero.heroDamageIntRange`, `Math.round` 호출 표현 |
| [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L62) | `public int damageRoll(Char owner) {` | 피해 계산; 주변 코드에 `Hero.heroDamageIntRange`, `Math.round`, `Messages.get` 호출 표현 |
| [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L83) | `public String targetingPrompt() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Messages.get`, `Integer.toString` 호출 표현 |
| [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L87) | `public boolean useTargeting(){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Messages.get`, `Integer.toString` 호출 표현 |
| [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L92) | `protected void duelistAbility(Hero hero, Integer target) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Messages.get`, `Integer.toString`, `PathFinder.buildDistanceMap`, `BArray.or` 호출 표현 |
| [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L97) | `public String abilityInfo() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Messages.get`, `Integer.toString`, `PathFinder.buildDistanceMap`, `BArray.or`, `GLog.w`, `PixelScene.shake` 호출 표현 |
| [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L106) | `public String upgradeAbilityStat(int level) {` | 강화; 주변 코드에 `Integer.toString`, `PathFinder.buildDistanceMap`, `BArray.or`, `GLog.w`, `Messages.get`, `PixelScene.shake`, `Actor.findChar` 호출 표현 |
| [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L110) | `public static void sneakAbility(Hero hero, Integer target, int maxDist, int invisTurns, MeleeWeapon wep){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `PathFinder.buildDistanceMap`, `BArray.or`, `GLog.w`, `Messages.get`, `PixelScene.shake`, `Actor.findChar`, `Buff.prolong` 호출 표현 |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/armor/ClothArmor.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClothArmor.java)

- Java 39줄. **타입:** `public class ClothArmor extends Armor {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClothArmor.java#L34) | `public ClothArmor() {` | 선언 확인(세부 반환/부작용은 본문 참조) |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/armor/PlateArmor.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/PlateArmor.java)

- Java 37줄. **타입:** `public class PlateArmor extends Armor {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/PlateArmor.java#L32) | `public PlateArmor() {` | 선언 확인(세부 반환/부작용은 본문 참조) |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/rings/RingOfMight.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java)

- Java 122줄. **타입:** `public class RingOfMight extends Ring {`; `public class Might extends RingBuff {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L40) | `public boolean doEquip(Hero hero) {` | 작동 |
| [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L50) | `public boolean doUnequip(Hero hero, boolean collect, boolean single) {` | 작동 |
| [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L60) | `public Item upgrade() {` | 강화; 주변 코드에 `Messages.get`, `Messages.decimalFormat`, `Math.pow` 호출 표현 |
| [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L67) | `public Item level(int value) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Messages.get`, `Messages.decimalFormat`, `Math.pow` 호출 표현 |
| [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L73) | `private void updateTargetHT(){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Messages.get`, `Messages.decimalFormat`, `Math.pow`, `Math.min`, `Integer.toString` 호출 표현 |
| [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L79) | `public String statsInfo() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Messages.get`, `Messages.decimalFormat`, `Math.pow`, `Math.min`, `Integer.toString` 호출 표현 |
| [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L94) | `public String upgradeStat1(int level) {` | 강화; 주변 코드에 `Math.min`, `Integer.toString`, `Messages.decimalFormat`, `Math.pow` 호출 표현 |
| [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L100) | `public String upgradeStat2(int level) {` | 강화; 주변 코드에 `Math.min`, `Messages.decimalFormat`, `Math.pow` 호출 표현 |
| [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L106) | `protected RingBuff buff( ) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.pow` 호출 표현 |
| [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L110) | `public static int strengthBonus( Char target ){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.pow` 호출 표현 |
| [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L114) | `public static float HTMultiplier( Char target ){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.pow` 호출 표현 |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/rings/RingOfHaste.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java)

- Java 67줄. **타입:** `public class RingOfHaste extends Ring {`; `public class Haste extends RingBuff {`.
- **주요 필드:** 한 줄 필드 선언 없음.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java#L36) | `public String statsInfo() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Messages.get`, `Messages.decimalFormat`, `Math.pow`, `Math.min` 호출 표현 |
| [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java#L50) | `public String upgradeStat1(int level){` | 강화; 주변 코드에 `Math.min`, `Messages.decimalFormat`, `Math.pow` 호출 표현 |
| [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java#L56) | `protected RingBuff buff( ) {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.pow` 호출 표현 |
| [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java#L60) | `public static float speedMultiplier( Char target ){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.pow` 호출 표현 |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.

## [items/artifacts/ChaliceOfBlood.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java)

- Java 239줄. **타입:** `public class ChaliceOfBlood extends Artifact {`; `public class chaliceRegen extends ArtifactBuff {`.
- **주요 필드:** [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L59) `public static final String AC_PRICK = "PRICK";`.

| 코드 위치 | 메서드 선언 | 해당 기능 영역 / 주변 호출 근거 |
|---|---|---|
| [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L62) | `public ArrayList<String> actions( Hero hero ) {` | 선언 확인(세부 반환/부작용은 본문 참조) |
| [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L74) | `public void execute(Hero hero, String action ) {` | 아이템 명령 처리; 주변 코드에 `Math.pow` 호출 표현 |
| [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L108) | `protected void onSelect(int index) {` | 이벤트/효과 트리거; 주변 코드에 `Math.ceil`, `Math.floor`, `Random.NormalIntRange` 호출 표현 |
| [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L119) | `private int minPrickDmg(){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.ceil`, `Math.floor`, `Random.NormalIntRange` 호출 표현 |
| [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L123) | `private int maxPrickDmg(){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Math.floor`, `Random.NormalIntRange` 호출 표현 |
| [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L127) | `private void prick(Hero hero){` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Random.NormalIntRange`, `GLog.w`, `Messages.get` 호출 표현 |
| [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L171) | `public Item upgrade() {` | 강화 |
| [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L180) | `public void restoreFromBundle(Bundle bundle) {` | 복원; 주변 코드에 `Random.Float` 호출 표현 |
| [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L187) | `protected ArtifactBuff passiveBuff() {` | 선언 확인(세부 반환/부작용은 본문 참조); 주변 코드에 `Random.Float`, `Math.min`, `Integer.toString` 호출 표현 |
| [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L192) | `public void charge(Hero target, float amount) {` | 충전; 주변 코드에 `Random.Float`, `Math.min`, `Integer.toString` 호출 표현 |
| [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L216) | `public String desc() {` | 설명 문자열; 주변 코드에 `Messages.get` 호출 표현 |

**주의:** 부모 클래스 `Item` / `EquipableItem` / `Wand` / `Potion` / `Scroll` 등에서 기본 동작을 상속할 수 있다. 상속과 메서드 재정의, 게임 난수, 대상 버프를 포함하지 않으면 최종 효능을 확정할 수 없다.


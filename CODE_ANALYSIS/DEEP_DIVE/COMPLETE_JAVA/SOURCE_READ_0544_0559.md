# Java 파일별 소스 구현 해설 544–559

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 544. [`CurseInfusion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/CurseInfusion.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 130행 / 타입 2개 / 필드 1개 / 메서드 5개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/CurseInfusion.java#L44) `class CurseInfusion  extends InventorySpell`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/CurseInfusion.java#L109) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/CurseInfusion.java#L111) `int OUT_QUANTITY` 초기식: `4`

### 함수·메서드 역할과 내부 연결

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/CurseInfusion.java#L53) **`usableOnItem(Item item)`**: 개별 처리 / 참조 호출: item.isUpgradable
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/CurseInfusion.java#L58) **`onItemSelected(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: CellEmitter.get, burst, Sample.INSTANCE.play, w.hasGoodEnchant, w.enchant, Weapon.Enchantment.randomCurse, w.enchantment.getClass, updateWand, a.hasGoodGlyph
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/CurseInfusion.java#L100) **`value()`**: 개별 처리
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/CurseInfusion.java#L105) **`energyVal()`**: 개별 처리
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/CurseInfusion.java#L124) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: Catalog.countUse, super.brew

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 545. [`InventorySpell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/InventorySpell.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 109행 / 타입 1개 / 필드 1개 / 메서드 9개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/InventorySpell.java#L37) `class InventorySpell  extends Spell`

### 변수·상수 (단일 행 선언)

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/InventorySpell.java#L48) `Class<?extends Bag> preferredBag` 초기식: `null`

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/InventorySpell.java#L40) **`onCast(Hero hero)`**: 이벤트·효과 실행 / 참조 호출: GameScene.selectItem
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/InventorySpell.java#L44) **`inventoryTitle()`**: 개별 처리 / 참조 호출: Messages.get
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/InventorySpell.java#L50) **`usableOnItem(Item item)`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/InventorySpell.java#L54) **`onItemSelected(Item item)`**: 이벤트·효과 실행
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/InventorySpell.java#L56) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, inventoryTitle, preferredBag, itemSelectable, usableOnItem, onSelect, detach, onItemSelected, curUser.spend
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/InventorySpell.java#L59) **`textPrompt()`**: 개별 처리 / 참조 호출: inventoryTitle
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/InventorySpell.java#L64) **`preferredBag()`**: 개별 처리
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/InventorySpell.java#L69) **`itemSelectable(Item item)`**: 개별 처리 / 참조 호출: usableOnItem
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/InventorySpell.java#L74) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: detach, onItemSelected, curUser.spend, curUser.busy, operate, Sample.INSTANCE.play, Invisibility.dispel, Catalog.countUse, curItem.getClass

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 546. [`MagicalInfusion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/MagicalInfusion.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 142행 / 타입 2개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/MagicalInfusion.java#L45) `class MagicalInfusion  extends InventorySpell`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/MagicalInfusion.java#L128) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/MagicalInfusion.java#L56) **`usableOnItem(Item item)`**: 개별 처리 / 참조 호출: item.isUpgradable
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/MagicalInfusion.java#L61) **`onItemSelected(Item item)`**: 이벤트·효과 실행 / 참조 호출: GameScene.show, WndUpgrade
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/MagicalInfusion.java#L67) **`reShowSelector()`**: 개별 처리 / 참조 호출: GameScene.selectItem
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/MagicalInfusion.java#L72) **`getSelector()`**: 조회·탐색
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/MagicalInfusion.java#L77) **`useAnimation()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: curUser.spend, curUser.busy, operate, Sample.INSTANCE.play, Invisibility.dispel, Catalog.countUse, curItem.getClass, Random.Float, Talent.onScrollUsed
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/MagicalInfusion.java#L91) **`upgradeItem(Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: ScrollOfUpgrade.upgrade, Degrade.detach, upgrade, item.upgrade, GLog.p, Messages.get, Badges.validateItemLevelAquired, Catalog.countUse, item.getClass
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/MagicalInfusion.java#L119) **`value()`**: 개별 처리
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/MagicalInfusion.java#L124) **`energyVal()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 547. [`PhaseShift.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/PhaseShift.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 96행 / 타입 2개 / 필드 1개 / 메서드 4개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/PhaseShift.java#L37) `class PhaseShift  extends TargetedSpell`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/PhaseShift.java#L79) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/PhaseShift.java#L81) `int OUT_QUANTITY` 초기식: `6`

### 함수·메서드 역할과 내부 연결

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/PhaseShift.java#L48) **`affectTarget(Ballistica bolt, Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, ScrollOfTeleportation.teleportChar, beckon, Dungeon.level.randomDestination, Char.hasProp, Buff.affect, GLog.w, Messages.get, onSpellused
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/PhaseShift.java#L49) **`findChar(bolt.collisionPos)`**: 조회·탐색
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/PhaseShift.java#L70) **`value()`**: 개별 처리
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/PhaseShift.java#L75) **`energyVal()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 548. [`ReclaimTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 180행 / 타입 3개 / 필드 3개 / 메서드 8개.

### 타입·상속 선언

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L47) `class ReclaimTrap  extends TargetedSpell`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L135) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L156) `class ReclaimedTrap  extends Buff`

### 변수·상수 (단일 행 선언)

- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L137) `int OUT_QUANTITY` 초기식: `5`
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L162) `Class<?extends Trap> trap`
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L164) `String TRAP` 초기식: `"trap"`

### 함수·메서드 역할과 내부 연결

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L56) **`affectTarget(Ballistica bolt, Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff, detach, level.traps.get, t.disarm, Sample.INSTANCE.play, ScrollOfRecharging.charge, Buff.affect, t.getClass, Bestiary.setSeen
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L97) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, hero.belongings.contains, Dungeon.hero.buff, Messages.get
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L118) **`glowing()`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.contains, Dungeon.hero.buff, Reflection.newInstance
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L126) **`value()`**: 개별 처리
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L131) **`energyVal()`**: 개별 처리
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L150) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: Catalog.countUse, super.brew
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L167) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/ReclaimTrap.java#L173) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getClass

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 549. [`Recycle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Recycle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 121행 / 타입 2개 / 필드 1개 / 메서드 4개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Recycle.java#L45) `class Recycle  extends InventorySpell`
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Recycle.java#L105) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Recycle.java#L107) `int OUT_QUANTITY` 초기식: `12`

### 함수·메서드 역할과 내부 연결

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Recycle.java#L55) **`usableOnItem(Item item)`**: 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Recycle.java#L64) **`onItemSelected(Item item)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Generator.randomUsingDefaults, Reflection.newInstance, ExoticPotion.regToExo.get, result.getClass, ExoticScroll.regToExo.get, TippedDart.randomTipped, item.getClass, Challenges.isItemBlocked, item.detach
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Recycle.java#L96) **`value()`**: 개별 처리
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Recycle.java#L101) **`energyVal()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 550. [`Spell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Spell.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 84행 / 타입 1개 / 필드 3개 / 메서드 5개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Spell.java#L33) `class Spell  extends Item`

### 변수·상수 (단일 행 선언)

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Spell.java#L35) `String AC_CAST` 초기식: `"CAST"`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Spell.java#L38) `float talentFactor` 초기식: `1`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Spell.java#L40) `float talentChance` 초기식: `1`

### 함수·메서드 역할과 내부 연결

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Spell.java#L48) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Spell.java#L55) **`execute(final Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, curUser.buff, GLog.w, Messages.get, onCast
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Spell.java#L72) **`isIdentified()`**: 조건 판정
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Spell.java#L77) **`isUpgradable()`**: 조건 판정
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Spell.java#L81) **`onCast(Hero hero)`**: 이벤트·효과 실행

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 551. [`SummonElemental.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 258행 / 타입 3개 / 필드 4개 / 메서드 12개.

### 타입·상속 선언

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L62) `class SummonElemental  extends Spell`
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L232) `class InvisAlly  extends AllyBuff`
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L242) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L64) `String AC_IMBUE` 초기식: `"IMBUE"`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L72) `Class<? extends Elemental> summonClass` 초기식: `Elemental.AllyNewBornElemental.class`
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L159) `String SUMMON_CLASS` 초기식: `"summon_class"`
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L244) `int OUT_QUANTITY` 초기식: `6`

### 함수·메서드 역할과 내부 연결

- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L75) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L82) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, GameScene.selectItem
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L91) **`onCast(Hero hero)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Actor.findChar, spawnPoints.add, spawnPoints.isEmpty, Actor.chars, ch.buff, ScrollOfTeleportation.appear, Random.element, curUser.spendAndNext, Reflection.newInstance
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L136) **`glowing()`**: 개별 처리 / 조건 분기 / 참조 호출: ItemSprite.Glowing, super.glowing
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L145) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, Messages.get
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L162) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L168) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, bundle.getClass
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L179) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, Messages.get, itemSelectable, item.isIdentified, onSelect, item.detach, Sample.INSTANCE.play, curUser.sprite.emitter, burst
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L181) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L186) **`itemSelectable(Item item)`**: 개별 처리 / 참조 호출: item.isIdentified
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L194) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: item.detach, Sample.INSTANCE.play, curUser.sprite.emitter, burst, curUser.sprite.operate, updateQuickslot
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/SummonElemental.java#L235) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.sprite.remove

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 552. [`TargetedSpell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 121행 / 타입 1개 / 필드 2개 / 메서드 10개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L40) `class TargetedSpell  extends Spell`

### 변수·상수 (단일 행 선언)

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L42) `int collisionProperties` 초기식: `Ballistica.PROJECTILE`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L84) `TargetedSpell curSpell`

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L45) **`onCast(Hero hero)`**: 이벤트·효과 실행 / 참조 호출: GameScene.selectCell
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L49) **`affectTarget(Ballistica bolt, Hero hero)`**: 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L51) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: MagicMissile.boltFromChar, Sample.INSTANCE.play
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L60) **`onSpellused()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: detach, Invisibility.dispel, updateQuickslot, curUser.spendAndNext, timeToCast, Catalog.countUse, getClass, Random.Float, Talent.onScrollUsed
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L71) **`timeToCast()`**: 개별 처리
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L75) **`Listener()`**: 개별 처리 / 조건 분기 / 참조 호출: onSelect, Ballistica, curUser.sprite.zap, Actor.findChar, QuickSlotButton.target, curUser.busy, curSpell.fx, Callback, call
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L78) **`onSelect(Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Ballistica, curUser.sprite.zap, Actor.findChar, QuickSlotButton.target, curUser.busy, curSpell.fx, Callback, call, curSpell.affectTarget
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L91) **`Ballistica(curUser.pos, target, curSpell.collisionProperties)`**: 개별 처리
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L105) **`call()`**: 개별 처리 / 참조 호출: curSpell.affectTarget
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TargetedSpell.java#L115) **`prompt()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 553. [`TelekineticGrab.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TelekineticGrab.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 167행 / 타입 2개 / 필드 1개 / 메서드 5개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TelekineticGrab.java#L42) `class TelekineticGrab  extends TargetedSpell`
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TelekineticGrab.java#L150) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TelekineticGrab.java#L152) `int OUT_QUANTITY` 초기식: `8`

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TelekineticGrab.java#L51) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: MagicMissile.boltFromChar, Sample.INSTANCE.play
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TelekineticGrab.java#L61) **`timeToCast()`**: 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TelekineticGrab.java#L67) **`affectTarget(Ballistica bolt, Hero hero)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.findChar, bolt.path.size, bolt.path.get, ch.buff, grabOne, item.doPickUp, item.pickupDelay, GLog.i, Messages.capitalize
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TelekineticGrab.java#L141) **`value()`**: 개별 처리
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/TelekineticGrab.java#L146) **`energyVal()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 554. [`UnstableSpell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/UnstableSpell.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 172행 / 타입 2개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/UnstableSpell.java#L49) `class UnstableSpell  extends Spell`
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/UnstableSpell.java#L131) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/UnstableSpell.java#L93) **`onCast(Hero hero)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: detach, updateQuickslot, Reflection.newInstance, Random.chances, hero.visibleEnemies, nonCombatScrolls.contains, s.getClass, combatScrolls.contains, s.anonymize
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/UnstableSpell.java#L122) **`value()`**: 개별 처리
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/UnstableSpell.java#L127) **`energyVal()`**: 개별 처리
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/UnstableSpell.java#L134) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: ExoticScroll.regToExo.containsKey, i.getClass, ExoticScroll.regToExo.containsValue
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/UnstableSpell.java#L152) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/UnstableSpell.java#L157) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 반복 / 참조 호출: i.quantity, sampleOutput
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/UnstableSpell.java#L167) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: UnstableSpell

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 555. [`WildEnergy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/WildEnergy.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 105행 / 타입 2개 / 필드 1개 / 메서드 5개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/WildEnergy.java#L42) `class WildEnergy  extends TargetedSpell`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/WildEnergy.java#L84) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/WildEnergy.java#L86) `int OUT_QUANTITY` 초기식: `5`

### 함수·메서드 역할과 내부 연결

- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/WildEnergy.java#L54) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: CursedWand.cursedZap
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/WildEnergy.java#L59) **`affectTarget(Ballistica bolt, final Hero hero)`**: 개별 처리 / 참조 호출: Sample.INSTANCE.play, ScrollOfRecharging.charge, SpellSprite.show, hero.belongings.charge, ArtifactRecharge.chargeArtifacts, Buff.affect, extend, onSpellused
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/WildEnergy.java#L75) **`value()`**: 개별 처리
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/WildEnergy.java#L80) **`energyVal()`**: 개별 처리
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/WildEnergy.java#L99) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: Catalog.countUse, super.brew

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 556. [`InventoryStone.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 125행 / 타입 1개 / 필드 2개 / 메서드 13개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L37) `class InventoryStone  extends Runestone`

### 변수·상수 (단일 행 선언)

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L43) `String AC_USE` 초기식: `"USE"`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L82) `Class<?extends Bag> preferredBag` 초기식: `null`

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L46) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L53) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, hero.buff, activate
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L61) **`activate(int cell)`**: 시간·상태 갱신 / 참조 호출: GameScene.selectItem
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L65) **`directActivate()`**: 개별 처리 / 참조 호출: GameScene.selectItem
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L69) **`useAnimation()`**: 이벤트·효과 실행 / 참조 호출: curUser.spend, curUser.busy, curUser.sprite.operate, Sample.INSTANCE.play, Invisibility.dispel
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L78) **`inventoryTitle()`**: 개별 처리 / 참조 호출: Messages.get
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L84) **`usableOnItem(Item item)`**: 개별 처리
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L88) **`onItemSelected(Item item)`**: 이벤트·효과 실행
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L90) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, inventoryTitle, preferredBag, itemSelectable, usableOnItem, onSelect, onItemSelected
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L93) **`textPrompt()`**: 개별 처리 / 참조 호출: inventoryTitle
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L98) **`preferredBag()`**: 개별 처리
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L103) **`itemSelectable(Item item)`**: 개별 처리 / 참조 호출: usableOnItem
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/InventoryStone.java#L108) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: onItemSelected

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 557. [`Runestone.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 110행 / 타입 2개 / 필드 1개 / 메서드 10개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L33) `class Runestone  extends Item`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L88) `class PlaceHolder  extends Runestone`

### 변수·상수 (단일 행 선언)

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L42) `boolean anonymous` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L43) **`anonymize()`**: 개별 처리
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L49) **`onThrow(int cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Dungeon.hero.buff, Actor.findChar, super.onThrow, Catalog.countUse, getClass, Talent.onRunestoneUsed, activate, Dungeon.level.pressCell, Invisibility.dispel
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L66) **`activate(int cell)`**: 시간·상태 갱신
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L69) **`isUpgradable()`**: 조건 판정
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L74) **`isIdentified()`**: 조건 판정
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L79) **`value()`**: 개별 처리
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L84) **`energyVal()`**: 개별 처리
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L95) **`activate(int cell)`**: 시간·상태 갱신
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L100) **`isSimilar(Item item)`**: 조건 판정
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java#L105) **`info()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 558. [`StoneOfAggression.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAggression.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 100행 / 타입 2개 / 필드 1개 / 메서드 4개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAggression.java#L37) `class StoneOfAggression  extends Runestone`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAggression.java#L59) `class Aggression  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAggression.java#L61) `float DURATION` 초기식: `20f`

### 함수·메서드 역할과 내부 연결

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAggression.java#L44) **`activate(int cell)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Actor.findChar, Char.hasProp, Buff.prolong, CellEmitter.center, start, Speck.factory, Sample.INSTANCE.play
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAggression.java#L69) **`icon()`**: 개별 처리
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAggression.java#L74) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAggression.java#L79) **`detach()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.isAlive, m.isTargeting, m.aggro, isTargeting, aggro, super.detach

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 559. [`StoneOfAugmentation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 178행 / 타입 2개 / 필드 4개 / 메서드 11개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L41) `class StoneOfAugmentation  extends InventoryStone`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L94) `class WndAugment  extends Window`

### 변수·상수 (단일 행 선언)

- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L96) `int WIDTH` 초기식: `120`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L97) `int MARGIN` 초기식: `2`
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L98) `int BUTTON_WIDTH` 초기식: `WIDTH - MARGIN * 2`
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L99) `int BUTTON_HEIGHT` 초기식: `18`

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L49) **`usableOnItem(Item item)`**: 개별 처리 / 참조 호출: ScrollOfEnchantment.enchantable
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L54) **`onItemSelected(Item item)`**: 이벤트·효과 실행 / 참조 호출: GameScene.show, WndAugment
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L60) **`apply(Weapon weapon, Weapon.Augment augment)`**: 개별 처리 / 조건 분기 / 참조 호출: useAnimation, ScrollOfUpgrade.upgrade, curItem.detach, Catalog.countUse, getClass, Talent.onRunestoneUsed
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L72) **`apply(Armor armor, Armor.Augment augment)`**: 개별 처리 / 조건 분기 / 참조 호출: useAnimation, ScrollOfUpgrade.upgrade, curItem.detach, Catalog.countUse, getClass, Talent.onRunestoneUsed
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L85) **`value()`**: 개별 처리
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L90) **`energyVal()`**: 개별 처리
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L101) **`WndAugment(final Item toAugment)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: IconTitle, titlebar.setRect, add, Messages.get, PixelScene.renderTextBlock, tfMesage.maxWidth, tfMesage.setPos, titlebar.bottom, tfMesage.bottom
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L128) **`onClick()`**: 이벤트·효과 실행 / 참조 호출: hide, StoneOfAugmentation.this.apply
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L145) **`onClick()`**: 이벤트·효과 실행 / 참조 호출: hide, StoneOfAugmentation.this.apply
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L160) **`onClick()`**: 이벤트·효과 실행 / 참조 호출: hide, activate
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java#L172) **`onBackPressed()`**: 이벤트·효과 실행 / 참조 호출: super.onBackPressed, activate

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":30,"fields":26,"methods":120}

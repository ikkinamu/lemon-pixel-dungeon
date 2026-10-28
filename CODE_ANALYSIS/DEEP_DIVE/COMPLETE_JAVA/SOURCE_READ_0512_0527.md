# Java 파일별 소스 구현 해설 512–527

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 512. [`RingOfSharpshooting.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfSharpshooting.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 78행 / 타입 2개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfSharpshooting.java#L29) `class RingOfSharpshooting  extends Ring`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfSharpshooting.java#L75) `class Aim  extends RingBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfSharpshooting.java#L36) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, soloBuffedBonus, Messages.decimalFormat, Math.pow, soloBonus, isEquipped, combinedBuffedBonus, combinedBonus
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfSharpshooting.java#L51) **`upgradeStat1(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Integer.toString
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfSharpshooting.java#L57) **`upgradeStat2(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Messages.decimalFormat, Math.pow
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfSharpshooting.java#L63) **`buff()`**: 개별 처리 / 참조 호출: Aim
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfSharpshooting.java#L67) **`levelDamageBonus(Char target)`**: 개별 처리 / 참조 호출: getBuffedBonus
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfSharpshooting.java#L71) **`durabilityMultiplier(Char target)`**: 개별 처리 / 참조 호출: Math.pow, getBonus

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 513. [`RingOfTenacity.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfTenacity.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 69행 / 타입 2개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfTenacity.java#L29) `class RingOfTenacity  extends Ring`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfTenacity.java#L65) `class Tenacity  extends RingBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfTenacity.java#L36) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, Math.pow, soloBuffedBonus, isEquipped, combinedBuffedBonus
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfTenacity.java#L50) **`upgradeStat1(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Messages.decimalFormat, Math.pow
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfTenacity.java#L56) **`buff()`**: 개별 처리 / 참조 호출: Tenacity
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfTenacity.java#L60) **`damageMultiplier(Char t)`**: 전투 관련 / 참조 호출: Math.pow, getBuffedBonus

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 514. [`RingOfWealth.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 326행 / 타입 4개 / 필드 5개 / 메서드 13개.

### 타입·상속 선언

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L56) `class RingOfWealth  extends Ring`
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L311) `class Wealth  extends RingBuff`
- [L314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L314) `class TriesToDropTracker  extends CounterBuff`
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L320) `class DropsToEquipTracker  extends CounterBuff`

### 변수·상수 (단일 행 선언)

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L63) `float triesToDrop` 초기식: `Float.MIN_VALUE`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L64) `int dropsToRare` 초기식: `Integer.MIN_VALUE`
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L85) `String TRIES_TO_DROP` 초기식: `"tries_to_drop"`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L86) `String DROPS_TO_RARE` 초기식: `"drops_to_rare"`
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L170) `int latestDropTier` 초기식: `0`

### 함수·메서드 역할과 내부 연결

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L66) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, Math.pow, soloBuffedBonus, isEquipped, combinedBuffedBonus
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L80) **`upgradeStat1(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Messages.decimalFormat, Math.pow
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L89) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L96) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getFloat, bundle.getInt
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L103) **`buff()`**: 개별 처리 / 참조 호출: Wealth
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L107) **`dropChanceMultiplier(Char target)`**: 개별 처리 / 참조 호출: Math.pow, getBuffedBonus
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L111) **`tryForBonusDrop(Char target, int tries)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: getBuffedBonus, target.buff, Buff.affect, triesToDrop.countUp, Random.NormalIntRange, dropsToEquip.countUp, triesToDrop.countDown, triesToDrop.count, dropsToEquip.count
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L172) **`showFlareForBonusDrop(Visual vis)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Flare, color, show
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L193) **`genConsumableDrop(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Float, genLowValueConsumable, genMidValueConsumable, genHighValueConsumable
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L210) **`genLowValueConsumable()`**: 개별 처리 / 상태 선택 / 참조 호출: Random.Int, Gold, random, i.quantity, Generator.randomUsingDefaults
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L224) **`genMidValueConsumable()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Random.Int, genLowValueConsumable, i.quantity, Generator.randomUsingDefaults, Reflection.newInstance, ExoticPotion.regToExo.get, i.getClass, ExoticScroll.regToExo.get, UnstableBrew
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L252) **`genHighValueConsumable()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Random.Int, genMidValueConsumable, Bomb.DoubleBomb, i.quantity, StoneOfEnchantment, Random.Float, ExoticCrystals.consumableExoticChance, PotionOfDivineInspiration, PotionOfExperience
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java#L270) **`genEquipmentDrop(int level)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Random.Int, Generator.randomWeapon, w.hasGoodEnchant, w.enchant, w.hasCurseEnchant, Generator.randomArmor, a.hasGoodGlyph, a.inscribe, a.hasCurseGlyph

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 515. [`ExoticScroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 152행 / 타입 2개 / 필드 0개 / 메서드 9개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java#L44) `class ExoticScroll  extends Scroll`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java#L121) `class ScrollToExotic  extends Recipe`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java#L88) **`isKnown()`**: 조건 판정 / 참조 호출: handler.isKnown, exoToReg.get, this.getClass
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java#L93) **`setKnown()`**: 상태 갱신 / 조건 분기 / 참조 호출: isKnown, handler.know, exoToReg.get, this.getClass, updateQuickslot
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java#L101) **`reset()`**: 생성·초기화 / 조건 분기 / 참조 호출: super.reset, handler.contains, exoToReg.get, this.getClass, handler.image, handler.label
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java#L111) **`value()`**: 개별 처리 / 참조 호출: Reflection.newInstance, exoToReg.get, getClass, value
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java#L117) **`energyVal()`**: 개별 처리 / 참조 호출: Reflection.newInstance, exoToReg.get, getClass, energyVal
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java#L124) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기 / 참조 호출: ingredients.size, regToExo.containsKey, ingredients.get, getClass
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java#L133) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java#L138) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 반복 / 참조 호출: i.quantity, Reflection.newInstance, regToExo.get, ingredients.get, getClass
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java#L147) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: Reflection.newInstance, regToExo.get, ingredients.get, getClass

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 516. [`ScrollOfAntiMagic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfAntiMagic.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 47행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfAntiMagic.java#L29) `class ScrollOfAntiMagic  extends ExoticScroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfAntiMagic.java#L36) **`doRead()`**: 개별 처리 / 참조 호출: detach, Buff.affect, Flare, color, show, identify, readAnimation

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 517. [`ScrollOfChallenge.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 212행 / 타입 2개 / 필드 3개 / 메서드 12개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L45) `class ScrollOfChallenge  extends ExoticScroll`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L70) `class ChallengeArena  extends Buff`

### 변수·상수 (단일 행 선언)

- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L75) `float DURATION` 초기식: `100`
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L183) `String ARENA_POSITIONS` 초기식: `"arena_positions"`
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L184) `String LEFT` 초기식: `"left"`

### 함수·메서드 역할과 내부 연결

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L52) **`doRead()`**: 개별 처리 / 반복 / 참조 호출: detach, level.mobs.toArray, mob.beckon, Buff.affect, setup, identify, curUser.sprite.centerEmitter, start, Speck.factory
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L83) **`icon()`**: 개별 처리
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L88) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L93) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L98) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L103) **`desc()`**: 개별 처리 / 참조 호출: Messages.get
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L107) **`setup(int pos)`**: 생성·초기화 / 조건 분기·반복 / 참조 호출: Dungeon.level.length, Dungeon.level.cellToPoint, ShadowCaster.castShadow, Dungeon.level.width, PathFinder.buildDistanceMap, BArray.or, arenaPositions.contains, arenaPositions.add, fx
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L146) **`extend(float duration)`**: 개별 처리
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L151) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: arenaPositions.contains, detach, BuffIndicator.refreshHero, spend
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L168) **`fx(boolean on)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: CellEmitter.get, e.pour, arenaEmitters.add, arenaEmitters.clear
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L187) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 반복 / 참조 호출: super.storeInBundle, arenaPositions.size, arenaPositions.get, bundle.put
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java#L199) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 반복 / 참조 호출: super.restoreFromBundle, bundle.getIntArray, arenaPositions.add, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 518. [`ScrollOfDivination.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfDivination.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 156행 / 타입 2개 / 필드 1개 / 메서드 1개.

### 타입·상속 선언

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfDivination.java#L46) `class ScrollOfDivination  extends ExoticScroll`
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfDivination.java#L125) `class WndDivination  extends Window`

### 변수·상수 (단일 행 선언)

- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfDivination.java#L127) `int WIDTH` 초기식: `120`

### 함수·메서드 역할과 내부 연결

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfDivination.java#L53) **`doRead()`**: 개별 처리 / 조건 분기·반복·상태 선택 / 참조 호출: detach, sprite.parent.add, Identification, curUser.sprite.center, offset, Sample.INSTANCE.play, Potion.getUnknown, Scroll.getUnknown, Ring.getUnknown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 519. [`ScrollOfDread.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfDread.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 63행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfDread.java#L35) `class ScrollOfDread  extends ExoticScroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfDread.java#L42) **`doRead()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: detach, Flare, color, show, Sample.INSTANCE.play, level.mobs.toArray, mob.isImmune, Buff.affect, curUser.id

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 520. [`ScrollOfEnchantment.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 308행 / 타입 4개 / 필드 5개 / 메서드 25개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L45) `class ScrollOfEnchantment  extends ExoticScroll`
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L151) `class WndEnchantSelect  extends WndOptions`
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L213) `class WndGlyphSelect  extends WndOptions`
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L275) `class WndConfirmCancel  extends WndOptions`

### 변수·상수 (단일 행 선언)

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L55) `boolean identifiedByUse` 초기식: `false`
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L153) `Weapon wep`
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L154) `Weapon.Enchantment[] enchantments`
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L215) `Armor arm`
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L216) `Armor.Glyph[] glyphs`

### 함수·메서드 역할과 내부 연결

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L58) **`doRead()`**: 개별 처리 / 조건 분기 / 참조 호출: isKnown, identify, detach, GameScene.selectItem
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L69) **`enchantable(Item item)`**: 개별 처리 / 참조 호출: item.isUpgradable
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L74) **`confirmCancelation()`**: 개별 처리 / 상태 선택 / 참조 호출: GameScene.show, WndOptions, ItemSprite, Messages.titleCase, name, Messages.get, onSelect, curUser.spendAndNext, GameScene.selectItem
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L81) **`onSelect(int index)`**: 이벤트·효과 실행 / 상태 선택 / 참조 호출: curUser.spendAndNext, GameScene.selectItem
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L92) **`onBackPressed()`**: 이벤트·효과 실행
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L96) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, Messages.get, preferredBag, itemSelectable, enchantable, onSelect, curItem.detach, enchantment.getClass, Weapon.Enchantment.randomCommon
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L99) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L104) **`preferredBag()`**: 개별 처리
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L109) **`itemSelectable(Item item)`**: 개별 처리 / 참조 호출: enchantable
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L114) **`onSelect(final Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: curItem.detach, enchantment.getClass, Weapon.Enchantment.randomCommon, Weapon.Enchantment.randomUncommon, Weapon.Enchantment.random, getClass, GameScene.show, WndEnchantSelect, glyph.getClass
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L157) **`WndEnchantSelect()`**: 개별 처리
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L161) **`WndEnchantSelect(Weapon wep, Weapon.Enchantment ench1, Weapon.Enchantment ench2, Weapon.Enchantment ench3)`**: 개별 처리 / 참조 호출: ItemSprite, ScrollOfEnchantment, Messages.titleCase, name, Messages.get, ench1.name, ench2.name, ench3.name
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L180) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: wep.enchant, GLog.p, Messages.get, readAnimation, Sample.INSTANCE.play, Enchanting.show, GameScene.show, WndConfirmCancel
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L194) **`hasInfo(int index)`**: 조건 판정
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L199) **`onInfo(int index)`**: 이벤트·효과 실행 / 참조 호출: GameScene.show, WndTitledMessage, Icons.get, Messages.titleCase, name, desc
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L207) **`onBackPressed()`**: 이벤트·효과 실행
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L219) **`WndGlyphSelect()`**: 개별 처리
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L223) **`WndGlyphSelect(Armor arm, Armor.Glyph glyph1, Armor.Glyph glyph2, Armor.Glyph glyph3)`**: 개별 처리 / 참조 호출: ItemSprite, ScrollOfEnchantment, Messages.titleCase, name, Messages.get, glyph1.name, glyph2.name, glyph3.name
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L242) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: arm.inscribe, GLog.p, Messages.get, readAnimation, Sample.INSTANCE.play, Enchanting.show, GameScene.show, WndConfirmCancel
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L256) **`hasInfo(int index)`**: 조건 판정
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L261) **`onInfo(int index)`**: 이벤트·효과 실행 / 참조 호출: GameScene.show, WndTitledMessage, Icons.get, Messages.titleCase, name, desc
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L269) **`onBackPressed()`**: 이벤트·효과 실행
- [L277](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L277) **`WndConfirmCancel()`**: 개별 처리 / 참조 호출: ItemSprite, ScrollOfEnchantment, Messages.titleCase, name, Messages.get
- [L286](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L286) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onSelect, GameScene.show, WndEnchantSelect, WndGlyphSelect
- [L303](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfEnchantment.java#L303) **`onBackPressed()`**: 이벤트·효과 실행

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 521. [`ScrollOfForesight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfForesight.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 50행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfForesight.java#L30) `class ScrollOfForesight  extends ExoticScroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfForesight.java#L37) **`doRead()`**: 개별 처리 / 참조 호출: detach, Sample.INSTANCE.play, Buff.affect, identify, readAnimation

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 522. [`ScrollOfMetamorphosis.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 284행 / 타입 3개 / 필드 5개 / 메서드 14개.

### 타입·상속 선언

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L49) `class ScrollOfMetamorphosis  extends ExoticScroll`
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L107) `class WndMetamorphChoose  extends Window`
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L174) `class WndMetamorphReplace  extends Window`

### 변수·상수 (단일 행 선언)

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L57) `boolean identifiedByUse` 초기식: `false`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L109) `WndMetamorphChoose INSTANCE`
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L176) `WndMetamorphReplace INSTANCE`
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L178) `Talent replacing`
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L179) `int tier`

### 함수·메서드 역할과 내부 연결

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L60) **`doRead()`**: 개별 처리 / 조건 분기 / 참조 호출: isKnown, identify, detach, GameScene.show, WndMetamorphChoose
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L71) **`onMetamorph(Talent oldTalent, Talent newTalent)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: readAnimation, Sample.INSTANCE.play, curUser.sprite.emitter, start, Speck.factory, Transmuting.show, Dungeon.hero.hasTalent, Talent.onTalentUpgraded
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L84) **`confirmCancelation(Window chooseWindow, boolean byID)`**: 개별 처리 / 상태 선택 / 참조 호출: GameScene.show, WndOptions, ItemSprite, Messages.titleCase, name, Messages.get, onSelect, curUser.spendAndNext, chooseWindow.hide
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L91) **`onSelect(int index)`**: 이벤트·효과 실행 / 상태 선택 / 참조 호출: curUser.spendAndNext, chooseWindow.hide
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L103) **`onBackPressed()`**: 이벤트·효과 실행
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L113) **`WndMetamorphChoose()`**: 개별 처리 / 반복 / 참조 호출: IconTitle, title.color, title.setRect, add, title.bottom, PixelScene.renderTextBlock, Messages.get, text.maxWidth, text.setPos
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L152) **`hide()`**: 개별 처리 / 참조 호출: super.hide
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L158) **`onBackPressed()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: confirmCancelation, super.onBackPressed
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L168) **`offset(int xOffset, int yOffset)`**: 개별 처리 / 참조 호출: super.offset, pane.setPos, pane.left, pane.top
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L183) **`WndMetamorphReplace()`**: 개별 처리 / 조건 분기 / 참조 호출: setup, hide
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L197) **`WndMetamorphReplace(Talent replacing, int tier)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: curItem.detach, hero.talents.get, keySet, HeroClass.values, Talent.initClassTalents, clsTalents.get, clsTalentsAtTier.toArray, curTalentsAtTier.contains, clsTalentsAtTier.remove
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L239) **`setup(Talent replacing, int tier, LinkedHashMap<Talent, Integer> replaceOptions)`**: 생성·초기화 / 참조 호출: IconTitle, title.color, title.setRect, add, title.bottom, PixelScene.renderTextBlock, Messages.get, text.maxWidth, text.setPos
- [L267](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L267) **`hide()`**: 개별 처리 / 조건 분기 / 참조 호출: super.hide
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMetamorphosis.java#L275) **`onBackPressed()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: confirmCancelation, super.onBackPressed

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 523. [`ScrollOfMysticalEnergy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMysticalEnergy.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 56행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMysticalEnergy.java#L32) `class ScrollOfMysticalEnergy  extends ExoticScroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfMysticalEnergy.java#L39) **`doRead()`**: 개별 처리 / 참조 호출: detach, Buff.affect, set, Sample.INSTANCE.play, SpellSprite.show, identify, ScrollOfRecharging.charge, readAnimation

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 524. [`ScrollOfPassage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfPassage.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 61행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfPassage.java#L33) `class ScrollOfPassage  extends ExoticScroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfPassage.java#L40) **`doRead()`**: 개별 처리 / 조건 분기 / 참조 호출: detach, identify, readAnimation, Dungeon.interfloorTeleportAllowed, GLog.w, Messages.get, Level.beforeTransition, Math.max, Game.switchScene

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 525. [`ScrollOfPrismaticImage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfPrismaticImage.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 73행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfPrismaticImage.java#L36) `class ScrollOfPrismaticImage  extends ExoticScroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfPrismaticImage.java#L43) **`doRead()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: detach, level.mobs.toArray, m.sprite.showStatusWithIcon, Integer.toString, Stasis.getStasisAlly, Buff.affect, set, PrismaticGuard.maxHP, identify

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 526. [`ScrollOfPsionicBlast.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfPsionicBlast.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 90행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfPsionicBlast.java#L40) `class ScrollOfPsionicBlast  extends ExoticScroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfPsionicBlast.java#L47) **`doRead()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: detach, GameScene.flash, Sample.INSTANCE.play, GLog.i, Messages.get, level.mobs.toArray, targets.add, mob.damage, Math.round

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 527. [`ScrollOfSirensSong.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfSirensSong.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.exotic` / 본문 145행 / 타입 2개 / 필드 1개 / 메서드 6개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfSirensSong.java#L42) `class ScrollOfSirensSong  extends ExoticScroll`
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfSirensSong.java#L125) `class Enthralled  extends AllyBuff`

### 변수·상수 (단일 행 선언)

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfSirensSong.java#L48) `boolean identifiedByUse` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfSirensSong.java#L51) **`doRead()`**: 개별 처리 / 조건 분기 / 참조 호출: isKnown, identify, detach, GameScene.selectCell
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfSirensSong.java#L62) **`Listener()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: onSelect, isKnown, Actor.findChar, GLog.w, Messages.get, curUser.sprite.centerEmitter, start, Speck.factory, Sample.INSTANCE.play
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfSirensSong.java#L65) **`onSelect(Integer cell)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: isKnown, Actor.findChar, GLog.w, Messages.get, curUser.sprite.centerEmitter, start, Speck.factory, Sample.INSTANCE.play, Sample.INSTANCE.playDelayed
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfSirensSong.java#L119) **`prompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfSirensSong.java#L133) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.sprite.remove
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfSirensSong.java#L139) **`icon()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":30,"fields":20,"methods":97}

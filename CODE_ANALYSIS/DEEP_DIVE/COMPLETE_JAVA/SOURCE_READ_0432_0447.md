# Java 파일별 소스 구현 해설 432–447

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 432. [`GoldenKey.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/GoldenKey.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.keys` / 본문 42행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/GoldenKey.java#L26) `class GoldenKey  extends Key`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/GoldenKey.java#L32) **`GoldenKey()`**: 개별 처리
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/GoldenKey.java#L36) **`GoldenKey(int depth)`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 433. [`IronKey.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/IronKey.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.keys` / 본문 42행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/IronKey.java#L26) `class IronKey  extends Key`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/IronKey.java#L32) **`IronKey()`**: 개별 처리
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/IronKey.java#L36) **`IronKey(int depth)`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 434. [`Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.keys` / 본문 96행 / 타입 1개 / 필드 3개 / 메서드 6개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java#L36) `class Key  extends Item`

### 변수·상수 (단일 행 선언)

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java#L38) `float TIME_TO_UNLOCK` 초기식: `1f`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java#L46) `int depth`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java#L71) `String DEPTH` 초기식: `"depth"`

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java#L49) **`isSimilar(Item item)`**: 조건 판정 / 참조 호출: super.isSimilar
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java#L54) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: Catalog.setSeen, getClass, Statistics.itemTypesDiscovered.add, GameScene.pickUpJournal, Notes.add, Sample.INSTANCE.play, hero.spendAndNext, pickupDelay, GameScene.updateKeyDisplay
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java#L74) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java#L80) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java#L86) **`isUpgradable()`**: 조건 판정
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java#L91) **`isIdentified()`**: 조건 판정

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 435. [`WornKey.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/WornKey.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.keys` / 본문 71행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/WornKey.java#L35) `class WornKey  extends Key`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/WornKey.java#L41) **`WornKey()`**: 개별 처리
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/WornKey.java#L45) **`WornKey(int depth)`**: 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/WornKey.java#L51) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기·예외 처리 / 참조 호출: SPDSettings.supportNagged, Dungeon.saveAll, Game.runOnRenderThread, Callback, call, ShatteredPixelDungeon.scene, add, WndSupportPrompt, ShatteredPixelDungeon.reportException
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/WornKey.java#L57) **`call()`**: 개별 처리 / 참조 호출: ShatteredPixelDungeon.scene, add, WndSupportPrompt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 436. [`KindofMisc.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindofMisc.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 201행 / 타입 1개 / 필드 2개 / 메서드 5개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindofMisc.java#L38) `class KindofMisc  extends EquipableItem`

### 변수·상수 (단일 행 선언)

- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindofMisc.java#L70) `KindofMisc[] miscs` 초기식: `new KindofMisc[3]`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindofMisc.java#L75) `boolean[] enabled` 초기식: `new boolean[3]`

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindofMisc.java#L41) **`doEquip(final Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.show, WndOptions, ItemSprite, Messages.get, Messages.titleCase, title, onSelect, Dungeon.quickslot.getSlot, backpack.items.remove
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindofMisc.java#L96) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Dungeon.quickslot.getSlot, backpack.items.remove, equipped.doUnequip, backpack.items.add, doEquip, Dungeon.quickslot.setSlot, defaultAction, updateQuickslot
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindofMisc.java#L128) **`enabled(int index)`**: 개별 처리
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindofMisc.java#L173) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doUnequip
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindofMisc.java#L194) **`isEquipped(Hero hero)`**: 조건 판정 / 참조 호출: hero.belongings.artifact, hero.belongings.misc, hero.belongings.ring

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 437. [`KindOfWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 294행 / 타입 1개 / 필드 3개 / 메서드 19개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L44) `class KindOfWeapon  extends EquipableItem`

### 변수·상수 (단일 행 선언)

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L46) `String hitSound` 초기식: `Assets.Sounds.HIT`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L47) `float hitSoundPitch` 초기식: `1f`
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L99) `boolean isSwiftEquipping` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L50) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: action.equals, Messages.titleCase, belongings.weapon.trueName, Messages.get, belongings.secondWep.trueName, primaryName.length, primaryName.substring, secondaryName.length, secondaryName.substring
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L65) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onSelect, Dungeon.quickslot.getSlot, doEquip, equipSecondary, Dungeon.quickslot.setSlot, updateQuickslot, defaultAction
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L95) **`isEquipped(Hero hero)`**: 조건 판정 / 참조 호출: hero.belongings.weapon, hero.belongings.secondWep
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L101) **`timeToEquip(Hero hero)`**: 개별 처리 / 참조 호출: super.timeToEquip
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L106) **`doEquip(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.contains, hero.hasTalent, hero.buff, hasSecondUse, Random.Int, hero.pointsInTalent, GLog.p, Messages.get, detachAll
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L161) **`equipSecondary(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.contains, hero.hasTalent, hero.buff, hasSecondUse, detachAll, belongings.secondWep.doUnequip, activate, Talent.onItemEquipped, Badges.validateDuelistUnlock
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L209) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doUnequip
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L234) **`min()`**: 개별 처리 / 참조 호출: min, buffedLvl
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L238) **`max()`**: 개별 처리 / 참조 호출: max, buffedLvl
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L242) **`min(int lvl)`**: 개별 처리
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L243) **`max(int lvl)`**: 개별 처리
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L245) **`damageRoll(Char owner)`**: 전투 관련 / 조건 분기 / 참조 호출: Hero.heroDamageIntRange, min, max, Random.NormalIntRange
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L253) **`accuracyFactor(Char owner, Char target)`**: 개별 처리
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L257) **`delayFactor(Char owner)`**: 개별 처리
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L261) **`reachFactor(Char owner)`**: 개별 처리
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L265) **`canReach(Char owner, int target)`**: 조건 판정 / 조건 분기·반복 / 참조 호출: reachFactor, Dungeon.level.distance, BArray.not, Actor.chars, PathFinder.buildDistanceMap
- [L281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L281) **`defenseFactor(Char owner)`**: 전투 관련
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L285) **`proc(Char attacker, Char defender, int damage)`**: 개별 처리
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java#L289) **`hitSound(float pitch)`**: 전투 관련 / 참조 호출: Sample.INSTANCE.play

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 438. [`KingsCrown.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KingsCrown.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 130행 / 타입 1개 / 필드 1개 / 메서드 5개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KingsCrown.java#L44) `class KingsCrown  extends Item`

### 변수·상수 (단일 행 선언)

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KingsCrown.java#L46) `String AC_WEAR` 초기식: `"WEAR"`

### 함수·메서드 역할과 내부 연결

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KingsCrown.java#L57) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KingsCrown.java#L64) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, hero.belongings.armor, GameScene.show, WndChooseAbility, GLog.w, Messages.get
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KingsCrown.java#L81) **`isUpgradable()`**: 조건 판정
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KingsCrown.java#L86) **`isIdentified()`**: 조건 판정
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KingsCrown.java#L90) **`upgradeArmor(Hero hero, Armor armor, ArmorAbility ability)`**: 개별 처리 / 조건 분기 / 참조 호출: detach, Catalog.countUse, getClass, hero.sprite.emitter, burst, Speck.factory, hero.spend, hero.busy, GLog.p

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 439. [`LiquidMetal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 246행 / 타입 2개 / 필드 1개 / 메서드 16개.

### 타입·상속 선언

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L48) `class LiquidMetal  extends Item`
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L191) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe`

### 변수·상수 (단일 행 선언)

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L60) `String AC_APPLY` 초기식: `"APPLY"`

### 함수·메서드 역할과 내부 연결

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L63) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L70) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, GameScene.selectItem
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L83) **`onThrow(int cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onThrow, Dungeon.level.pressCell, GLog.i, Messages.get, Sample.INSTANCE.play, Splash.at
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L101) **`isUpgradable()`**: 조건 판정
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L106) **`isIdentified()`**: 조건 판정
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L111) **`value()`**: 개별 처리
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L115) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, Messages.get, preferredBag, itemSelectable, onSelect, Math.pow, m.level, m.durabilityLeft, Math.ceil
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L118) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L123) **`preferredBag()`**: 개별 처리
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L128) **`itemSelectable(Item item)`**: 개별 처리
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L133) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Math.pow, m.level, m.durabilityLeft, Math.ceil, m.durabilityPerUse, m.quantity, m.defaultQuantity, quantity, Catalog.countUses
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L194) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: ingredients.size, ingredients.get
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L202) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L207) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기 / 참조 호출: sampleOutput, ingredients.get, result.quantity, metalQuantity, m.quantity, Buff.affect, levelThresholds.put
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L221) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기 / 참조 호출: ingredients.get, LiquidMetal, quantity, metalQuantity
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java#L231) **`metalQuantity(MissileWeapon m)`**: 개별 처리 / 조건 분기 / 참조 호출: m.defaultQuantity, Math.pow, Math.min, m.level, m.quantity, m.durabilityLeft, Math.round

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 440. [`LostBackpack.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LostBackpack.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 88행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LostBackpack.java#L39) `class LostBackpack  extends Item`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LostBackpack.java#L48) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: hero.buff, detach, hero.belongings.getItem, i.keptThroughLostInventory, i.isEquipped, activate, hero.hasTalent, holster.contains, charge

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 441. [`AquaBrew.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/AquaBrew.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.brews` / 본문 80행 / 타입 2개 / 필드 1개 / 메서드 3개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/AquaBrew.java#L29) `class AquaBrew  extends Brew`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/AquaBrew.java#L63) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/AquaBrew.java#L65) `int OUT_QUANTITY` 초기식: `8`

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/AquaBrew.java#L38) **`shatter(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: GeyserTrap, Ballistica, aim.path.size, aim.path.get, geyser.activate
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/AquaBrew.java#L54) **`value()`**: 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/AquaBrew.java#L59) **`energyVal()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 442. [`BlizzardBrew.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/BlizzardBrew.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.brews` / 본문 74행 / 타입 2개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/BlizzardBrew.java#L34) `class BlizzardBrew  extends Brew`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/BlizzardBrew.java#L60) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/BlizzardBrew.java#L41) **`shatter(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: splash, Sample.INSTANCE.play, GameScene.add, Blob.seed

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 443. [`Brew.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/Brew.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.brews` / 본문 68행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/Brew.java#L30) `class Brew  extends Potion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/Brew.java#L33) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.remove
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/Brew.java#L40) **`defaultAction()`**: 개별 처리
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/Brew.java#L45) **`doThrow(Hero hero)`**: 개별 처리 / 참조 호출: GameScene.selectCell
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/Brew.java#L50) **`shatter(int cell)`**: 개별 처리
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/Brew.java#L53) **`isKnown()`**: 조건 판정
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/Brew.java#L58) **`value()`**: 개별 처리
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/Brew.java#L63) **`energyVal()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 444. [`CausticBrew.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/CausticBrew.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.brews` / 본문 88행 / 타입 2개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/CausticBrew.java#L42) `class CausticBrew  extends Brew`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/CausticBrew.java#L69) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/CausticBrew.java#L49) **`shatter(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: splash, Sample.INSTANCE.play, PathFinder.buildDistanceMap, BArray.not, Splash.at, Actor.findChar, Buff.affect, set
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/CausticBrew.java#L82) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: Catalog.countUse, super.brew

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 445. [`InfernalBrew.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/InfernalBrew.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.brews` / 본문 75행 / 타입 2개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/InfernalBrew.java#L34) `class InfernalBrew  extends Brew`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/InfernalBrew.java#L61) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/InfernalBrew.java#L41) **`shatter(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: splash, Sample.INSTANCE.play, GameScene.add, Blob.seed

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 446. [`ShockingBrew.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/ShockingBrew.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.brews` / 본문 70행 / 타입 2개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/ShockingBrew.java#L35) `class ShockingBrew  extends Brew`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/ShockingBrew.java#L56) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/ShockingBrew.java#L42) **`shatter(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: splash, Sample.INSTANCE.play, PathFinder.buildDistanceMap, BArray.not, GameScene.add, Blob.seed

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 447. [`UnstableBrew.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.brews` / 본문 176행 / 타입 2개 / 필드 0개 / 메서드 11개.

### 타입·상속 선언

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L49) `class UnstableBrew  extends Brew`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L134) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L56) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L63) **`defaultAction()`**: 개별 처리
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L83) **`apply(Hero hero)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.isChallenged, potionChances.put, Reflection.newInstance, Random.chances, mustThrowPots.contains, p.getClass, p.anonymize, p.apply
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L105) **`shatter(int cell)`**: 개별 처리 / 반복 / 참조 호출: Reflection.newInstance, Random.chances, mustThrowPots.contains, p.getClass, canThrowPots.contains, p.anonymize, p.shatter
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L119) **`isKnown()`**: 조건 판정
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L125) **`value()`**: 개별 처리
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L130) **`energyVal()`**: 개별 처리
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L137) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: ExoticPotion.regToExo.containsKey, i.getClass, ExoticPotion.regToExo.containsValue
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L155) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L160) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 반복 / 참조 호출: i.quantity, sampleOutput
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/UnstableBrew.java#L170) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: UnstableBrew

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":23,"fields":11,"methods":86}

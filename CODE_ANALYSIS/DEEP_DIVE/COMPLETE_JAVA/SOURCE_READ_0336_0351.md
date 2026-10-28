# Java 파일별 소스 구현 해설 336–351

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 336. [`Ankh.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 135행 / 타입 1개 / 필드 3개 / 메서드 12개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L37) `class Ankh  extends Item`

### 변수·상수 (단일 행 선언)

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L39) `String AC_BLESS` 초기식: `"BLESS"`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L49) `boolean blessed` 초기식: `false`
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L116) `String BLESSED` 초기식: `"blessed"`

### 함수·메서드 역할과 내부 연결

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L52) **`isUpgradable()`**: 조건 판정
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L57) **`isIdentified()`**: 조건 판정
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L62) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, hero.belongings.getItem, waterskin.isFull, actions.add
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L71) **`execute(final Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, hero.belongings.getItem, waterskin.empty, GLog.p, Messages.get, hero.spend, hero.busy, Sample.INSTANCE.play
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L94) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, super.desc
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L101) **`isBlessed()`**: 조건 판정
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L105) **`bless()`**: 개별 처리
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L109) **`Glowing(0xFFFFCC)`**: 개별 처리
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L112) **`glowing()`**: 개별 처리 / 참조 호출: isBlessed
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L119) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L125) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getBoolean
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java#L131) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 337. [`ArcaneResin.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 201행 / 타입 2개 / 필드 1개 / 메서드 15개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L44) `class ArcaneResin  extends Item`
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L150) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe`

### 변수·상수 (단일 행 선언)

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L56) `String AC_APPLY` 초기식: `"APPLY"`

### 함수·메서드 역할과 내부 연결

- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L59) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L66) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, GameScene.selectItem
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L79) **`isUpgradable()`**: 조건 판정
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L84) **`isIdentified()`**: 조건 판정
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L89) **`value()`**: 개별 처리 / 참조 호출: quantity
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L93) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, Messages.get, preferredBag, itemSelectable, item.isIdentified, onSelect, w.level, GLog.w, quantity
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L96) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L101) **`preferredBag()`**: 개별 처리
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L106) **`itemSelectable(Item item)`**: 개별 처리 / 참조 호출: item.isIdentified
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L111) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: w.level, GLog.w, Messages.get, quantity, Catalog.countUses, detachAll, w.updateLevel, Item.updateQuickslot, curUser.sprite.operate
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L153) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: ingredients.size, ingredients.get
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L161) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L166) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기 / 참조 호출: sampleOutput, ingredients.get, result.quantity, resinQuantity, w.quantity
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L179) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기 / 참조 호출: ingredients.get, ArcaneResin, quantity, resinQuantity
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ArcaneResin.java#L189) **`resinQuantity(Wand w)`**: 개별 처리 / 조건 분기 / 참조 호출: w.level, Dungeon.hero.hasTalent, Dungeon.hero.pointsInTalent

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 338. [`Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor` / 본문 920행 / 타입 3개 / 필드 22개 / 메서드 62개.

### 타입·상속 선언

- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L88) `class Armor  extends EquipableItem`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L92) `enum Augment`
- [L792](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L792) `class Glyph  implements Bundlable`

### 변수·상수 (단일 행 선언)

- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L90) `String AC_DETACH` 초기식: `"DETACH"`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L97) `float evasionFactor`
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L98) `float defenceFactor`
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L114) `Augment augment` 초기식: `Augment.NONE`
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L116) `Glyph glyph`
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L117) `boolean glyphHardened` 초기식: `false`
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L118) `boolean curseInfusionBonus` 초기식: `false`
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L119) `boolean masteryPotionBonus` 초기식: `false`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L121) `BrokenSeal seal`
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L123) `int tier`
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L125) `int USES_TO_ID` 초기식: `10`
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L126) `float usesLeftToID` 초기식: `USES_TO_ID`
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L127) `float availableUsesToID` 초기식: `USES_TO_ID/2f`
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L133) `String USES_LEFT_TO_ID` 초기식: `"uses_left_to_id"`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L134) `String AVAILABLE_USES` 초기식: `"available_uses"`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L135) `String GLYPH` 초기식: `"glyph"`
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L136) `String GLYPH_HARDENED` 초기식: `"glyph_hardened"`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L137) `String CURSE_INFUSION_BONUS` 초기식: `"curse_infusion_bonus"`
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L138) `String MASTERY_POTION_BONUS` 초기식: `"mastery_potion_bonus"`
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L139) `String SEAL` 초기식: `"seal"`
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L140) `String AUGMENT` 초기식: `"augment"`
- [L411](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L411) `boolean testingNoArmDefSkill` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L105) **`evasionFactor(int level)`**: 개별 처리 / 참조 호출: Math.round
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L109) **`defenseFactor(int level)`**: 전투 관련 / 참조 호출: Math.round
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L129) **`Armor(int tier)`**: 개별 처리
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L143) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L156) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, inscribe, bundle.get, bundle.getBoolean, bundle.getEnum
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L170) **`reset()`**: 생성·초기화 / 참조 호출: super.reset
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L179) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, actions.add
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L186) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, detachSeal, GLog.i, Messages.get, hero.sprite.operate, detaching.collect, Dungeon.level.drop, updateQuickslot
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L202) **`collect(Bag container)`**: 개별 처리 / 조건 분기 / 참조 호출: super.collect, Dungeon.hero.isAlive, isIdentified, Catalog.setSeen, glyph.getClass, Statistics.itemTypesDiscovered.add
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L215) **`identify(boolean byHero)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.isAlive, Catalog.setSeen, glyph.getClass, Statistics.itemTypesDiscovered.add, super.identify
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L223) **`setIDReady()`**: 상태 갱신
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L227) **`readyToIdentify()`**: 개별 처리 / 참조 호출: isIdentified
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L232) **`doEquip(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.hasTalent, Random.Int, hero.pointsInTalent, GLog.p, Messages.get, detach, belongings.armor.doUnequip, equipCursed, GLog.n
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L271) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onSelect, seal.affixToArmor, updateQuickslot, super.hide
- [L281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L281) **`hide()`**: 개별 처리
- [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L302) **`activate(Char ch)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Buff.affect, setArmor
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L306) **`affixSeal(BrokenSeal seal)`**: 개별 처리 / 조건 분기 / 참조 호출: seal.level, trueLevel, level, Badges.validateItemLevelAquired, seal.getGlyph, inscribe, isEquipped, Buff.affect, setArmor
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L322) **`detachSeal()`**: 개별 처리 / 조건 분기 / 참조 호출: isEquipped, Dungeon.hero.buff, sealBuff.setArmor, detaching.level, degrade, detaching.canTransferGlyph, inscribe, detaching.setGlyph
- [L347](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L347) **`checkSeal()`**: 조건 판정
- [L352](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L352) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doUnequip, updateArmor, hero.buff, sealBuff.setArmor
- [L371](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L371) **`isEquipped(Hero hero)`**: 조건 판정 / 참조 호출: hero.belongings.armor
- [L375](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L375) **`DRMax()`**: 개별 처리 / 참조 호출: DRMax, buffedLvl
- [L379](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L379) **`DRMax(int lvl)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.isChallenged, augment.defenseFactor
- [L392](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L392) **`DRMin()`**: 개별 처리 / 참조 호출: DRMin, buffedLvl
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L396) **`DRMin(int lvl)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.isChallenged, DRMax
- [L413](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L413) **`evasionFactor(Char owner, float evasion)`**: 개별 처리 / 조건 분기 / 참조 호출: hasGlyph, Stone.testingEvasion, STRReq, STR, Math.pow, owner.buff, momentum.evasionBonus, Math.max, augment.evasionFactor
- [L433](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L433) **`speedFactor(Char owner, float speed)`**: 개별 처리 / 조건 분기 / 참조 호출: STRReq, STR, Math.pow
- [L445](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L445) **`level()`**: 개별 처리 / 조건 분기 / 참조 호출: super.level
- [L454](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L454) **`upgrade()`**: 개별 처리 / 참조 호출: upgrade
- [L458](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L458) **`upgrade(boolean inscribe)`**: 개별 처리 / 조건 분기 / 참조 호출: inscribe, Glyph.random, level, Random.Float, Math.pow, hasCurseGlyph, Random.Int, Dungeon.hero.hasTalent, Dungeon.hero.pointsInTalent
- [L498](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L498) **`proc(Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: defender.buff, Dungeon.hero.buff, glyph, trinityGlyph.getClass, glyph.getClass, isEquipped, hasCurseGlyph, glyph.proc, trinityGlyph.proc
- [L564](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L564) **`onHeroGainExp(float levelPercent, Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Talent.itemIDSpeedFactor, isEquipped, Math.min
- [L573](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L573) **`name()`**: 개별 처리 / 조건 분기 / 참조 호출: isEquipped, hasCurseGlyph, Dungeon.hero.buff, Messages.get, super.name, glyph.curse, glyph.name
- [L584](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L584) **`info()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: super.info, Messages.get, DRMin, DRMax, STRReq, Dungeon.hero.STR, isEquipped, hasCurseGlyph, Dungeon.hero.buff
- [L644](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L644) **`emitter()`**: 개별 처리 / 조건 분기 / 참조 호출: super.emitter, Emitter, emitter.pos, ItemSpriteSheet.film.width, ItemSpriteSheet.film.height, emitter.pour, Speck.factory
- [L654](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L654) **`random()`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int, level, Random.pushGenerator, Random.Long, Random.Float, ParchmentScrap.curseChanceMultiplier, inscribe, Glyph.randomCurse, ParchmentScrap.enchantChanceMultiplier
- [L686](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L686) **`STRReq()`**: 개별 처리 / 참조 호출: STRReq, level
- [L690](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L690) **`STRReq(int lvl)`**: 개별 처리 / 조건 분기 / 참조 호출: STRReq
- [L698](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L698) **`STRReq(int tier, int lvl)`**: 개별 처리 / 참조 호출: Math.max, Math.round, Math.sqrt
- [L706](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L706) **`value()`**: 개별 처리 / 조건 분기 / 참조 호출: hasGoodGlyph, hasCurseGlyph, level
- [L725](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L725) **`inscribe(Glyph glyph)`**: 개별 처리 / 조건 분기 / 참조 호출: glyph.curse, updateQuickslot, seal.setGlyph, isIdentified, Dungeon.hero.isAlive, hero.belongings.contains, Catalog.setSeen, glyph.getClass, Statistics.itemTypesDiscovered.add
- [L742](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L742) **`inscribe()`**: 개별 처리 / 참조 호출: glyph.getClass, Glyph.random, inscribe
- [L750](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L750) **`hasGlyph(Class<?extends Glyph> type, Char owner)`**: 조건 판정 / 조건 분기 / 참조 호출: owner.buff, glyph.curse, isEquipped, glyph, getClass, equals, glyph.getClass
- [L772](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L772) **`hasGoodGlyph()`**: 조건 판정 / 참조 호출: glyph.curse
- [L776](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L776) **`hasCurseGlyph()`**: 조건 판정 / 참조 호출: glyph.curse
- [L780](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L780) **`Glowing(0xFFFF00)`**: 개별 처리
- [L783](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L783) **`glowing()`**: 개별 처리 / 조건 분기 / 참조 호출: isEquipped, hasCurseGlyph, Dungeon.hero.buff, glyph.curse, glyph.glowing
- [L815](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L815) **`proc(Armor armor, Char attacker, Char defender, int damage)`**: 개별 처리
- [L817](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L817) **`procChanceMultiplier(Char defender)`**: 개별 처리 / 참조 호출: genericProcChanceMultiplier
- [L821](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L821) **`genericProcChanceMultiplier(Char defender)`**: 개별 처리 / 조건 분기 / 참조 호출: RingOfArcana.enchantPowerMultiplier, Dungeon.hero.buff, Dungeon.level.distance, defender.buff, Dungeon.hero.pointsInTalent
- [L833](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L833) **`name()`**: 개별 처리 / 조건 분기 / 참조 호출: curse, name, Messages.get
- [L840](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L840) **`name(String armorName)`**: 개별 처리 / 참조 호출: Messages.get
- [L844](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L844) **`desc()`**: 개별 처리 / 참조 호출: Messages.get
- [L848](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L848) **`curse()`**: 개별 처리
- [L853](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L853) **`restoreFromBundle(Bundle bundle)`**: 저장·복원
- [L857](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L857) **`storeInBundle(Bundle bundle)`**: 저장·복원
- [L860](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L860) **`glowing()`**: 개별 처리
- [L863](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L863) **`random(Class<? extends Glyph> ... toIgnore)`**: 개별 처리 / 상태 선택 / 참조 호출: Random.chances, randomCommon, randomUncommon, randomRare
- [L875](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L875) **`randomCommon(Class<? extends Glyph> ... toIgnore)`**: 개별 처리 / 조건 분기 / 참조 호출: Arrays.asList, glyphs.removeAll, glyphs.isEmpty, random, Reflection.newInstance, Random.element
- [L886](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L886) **`randomUncommon(Class<? extends Glyph> ... toIgnore)`**: 개별 처리 / 조건 분기 / 참조 호출: Arrays.asList, glyphs.removeAll, glyphs.isEmpty, random, Reflection.newInstance, Random.element
- [L897](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L897) **`randomRare(Class<? extends Glyph> ... toIgnore)`**: 개별 처리 / 조건 분기 / 참조 호출: Arrays.asList, glyphs.removeAll, glyphs.isEmpty, random, Reflection.newInstance, Random.element
- [L908](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java#L908) **`randomCurse(Class<? extends Glyph> ... toIgnore)`**: 개별 처리 / 조건 분기 / 참조 호출: Arrays.asList, glyphs.removeAll, glyphs.isEmpty, random, Reflection.newInstance, Random.element

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 339. [`ClassArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor` / 본문 351행 / 타입 2개 / 필드 6개 / 메서드 19개.

### 타입·상속 선언

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L51) `class ClassArmor  extends Armor`
- [L321](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L321) `class Charger  extends Buff`

### 변수·상수 (단일 행 선언)

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L53) `String AC_ABILITY` 초기식: `"ABILITY"`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L54) `String AC_TRANSFER` 초기식: `"TRANSFER"`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L64) `Charger charger`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L65) `float charge` 초기식: `0`
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L146) `String ARMOR_TIER` 초기식: `"armortier"`
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L147) `String CHARGE` 초기식: `"charge"`

### 함수·메서드 역할과 내부 연결

- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L67) **`ClassArmor()`**: 개별 처리
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L72) **`activate(Char ch)`**: 시간·상태 갱신 / 참조 호출: super.activate, Charger, charger.attachTo
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L79) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doUnequip, charger.detach
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L94) **`targetingPos(Hero user, int dst)`**: 개별 처리 / 참조 호출: user.armorAbility.targetedPos
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L98) **`upgrade(Hero owner, Armor armor)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: WarriorArmor, RogueArmor, MageArmor, HuntressArmor, DuelistArmor, ClericArmor, classArmor.level, armor.trueLevel, classArmor.inscribe
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L150) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L157) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getFloat
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L164) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, actions.add
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L174) **`actionName(String action, Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: action.equals, Messages.upperCase, hero.armorAbility.name, super.actionName
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L183) **`status()`**: 개별 처리 / 참조 호출: Messages.format, Math.floor
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L188) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, GameScene.show, WndChooseAbility, isEquipped, GLog.w, Messages.get, hero.armorAbility.chargeUse, hero.armorAbility.useTargeting
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L215) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: GameScene.selectItem, WndBag.ItemSelector, textPrompt, Messages.get, itemSelectable, onSelect, armor.detach, updateArmor, level
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L219) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L224) **`itemSelectable(Item item)`**: 개별 처리
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L229) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: armor.detach, updateArmor, level, armor.trueLevel, armor.checkSeal, inscribe, checkSeal, seal.level, trueLevel
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L296) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, hero.belongings.contains, ability.shortDesc, ability.chargeUse, Messages.get, Messages.decimalFormat
- [L317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L317) **`value()`**: 개별 처리
- [L324](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L324) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, cooldown, target.cooldown, spend
- [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java#L336) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Regeneration.regenOn, RingOfEnergy.armorChargeMultiplier, updateQuickslot, spend

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 340. [`ClericArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClericArmor.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor` / 본문 33행 / 타입 1개 / 필드 0개 / 메서드 0개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClericArmor.java#L26) `class ClericArmor  extends ClassArmor`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- 검출 없음

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 341. [`ClothArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClothArmor.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor` / 본문 39행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClothArmor.java#L26) `class ClothArmor  extends Armor`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClothArmor.java#L34) **`ClothArmor()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 342. [`AntiEntropy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/AntiEntropy.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor.curses` / 본문 71행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/AntiEntropy.java#L37) `class AntiEntropy  extends Glyph`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/AntiEntropy.java#L39) **`Glowing(0x000000)`**: 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/AntiEntropy.java#L42) **`proc(Armor armor, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: procChanceMultiplier, Random.Float, Freezing.affect, Buff.affect, reignite, defender.sprite.emitter, burst
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/AntiEntropy.java#L62) **`glowing()`**: 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/AntiEntropy.java#L67) **`curse()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 343. [`Bulk.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Bulk.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor.curses` / 본문 64행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Bulk.java#L31) `class Bulk  extends Armor.Glyph`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Bulk.java#L33) **`Glowing(0x000000)`**: 개별 처리
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Bulk.java#L36) **`proc(Armor armor, Char attacker, Char defender, int damage)`**: 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Bulk.java#L42) **`speedBoost(Char owner, int level)`**: 개별 처리 / 조건 분기 / 참조 호출: owner.sprite.emitter, startDelayed, genericProcChanceMultiplier
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Bulk.java#L55) **`glowing()`**: 개별 처리
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Bulk.java#L60) **`curse()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 344. [`Corrosion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Corrosion.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor.curses` / 본문 64행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Corrosion.java#L34) `class Corrosion  extends Armor.Glyph`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Corrosion.java#L36) **`Glowing(0x000000)`**: 개별 처리
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Corrosion.java#L39) **`proc(Armor armor, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: procChanceMultiplier, Random.Float, Splash.at, Actor.findChar, Buff.affect, set
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Corrosion.java#L55) **`glowing()`**: 개별 처리
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Corrosion.java#L60) **`curse()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 345. [`Displacement.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Displacement.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor.curses` / 본문 56행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Displacement.java#L30) `class Displacement  extends Armor.Glyph`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Displacement.java#L32) **`Glowing(0x000000)`**: 개별 처리
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Displacement.java#L35) **`proc(Armor armor, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: procChanceMultiplier, Random.Float, ScrollOfTeleportation.teleportChar
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Displacement.java#L47) **`glowing()`**: 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Displacement.java#L52) **`curse()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 346. [`Metabolism.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Metabolism.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor.curses` / 본문 77행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Metabolism.java#L36) `class Metabolism  extends Glyph`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Metabolism.java#L38) **`Glowing(0x000000)`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Metabolism.java#L41) **`proc(Armor armor, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: procChanceMultiplier, Random.Float, Math.min, Buff.affect, hunger.isStarving, hunger.affectHunger, defender.sprite.showStatusWithIcon, Integer.toString
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Metabolism.java#L68) **`glowing()`**: 개별 처리
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Metabolism.java#L73) **`curse()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 347. [`Multiplicity.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Multiplicity.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor.curses` / 본문 159행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Multiplicity.java#L49) `class Multiplicity  extends Armor.Glyph`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Multiplicity.java#L51) **`Glowing(0x000000)`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Multiplicity.java#L54) **`proc(Armor armor, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: procChanceMultiplier, Random.Float, Actor.findChar, spawnPoints.add, spawnPoints.size, Random.Int, MirrorImage, duplicate, getOriginal
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Multiplicity.java#L115) **`duplicate(Mob toDuplicate)`**: 개별 처리 / 조건 분기 / 참조 호출: getOriginal, Actor.fixTime, Reflection.newInstance, toDuplicate.getClass, Bundle, toDuplicate.storeInBundle, m.restoreFromBundle, m.remove
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Multiplicity.java#L150) **`glowing()`**: 개별 처리
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Multiplicity.java#L155) **`curse()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 348. [`Overgrowth.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Overgrowth.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor.curses` / 본문 74행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Overgrowth.java#L35) `class Overgrowth  extends Armor.Glyph`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Overgrowth.java#L37) **`Glowing(0x000000)`**: 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Overgrowth.java#L40) **`proc(Armor armor, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: procChanceMultiplier, Random.Float, Generator.randomUsingDefaults, couch, p.activate, CellEmitter.get, burst
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Overgrowth.java#L65) **`glowing()`**: 개별 처리
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Overgrowth.java#L70) **`curse()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 349. [`Stench.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Stench.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor.curses` / 본문 59행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Stench.java#L32) `class Stench  extends Armor.Glyph`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Stench.java#L34) **`Glowing(0x000000)`**: 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Stench.java#L37) **`proc(Armor armor, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: procChanceMultiplier, Random.Float, GameScene.add, Blob.seed
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Stench.java#L50) **`glowing()`**: 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Stench.java#L55) **`curse()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 350. [`DuelistArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/DuelistArmor.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor` / 본문 33행 / 타입 1개 / 필드 0개 / 메서드 0개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/DuelistArmor.java#L26) `class DuelistArmor  extends ClassArmor`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- 검출 없음

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 351. [`Affection.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Affection.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor.glyphs` / 본문 64행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Affection.java#L34) `class Affection  extends Glyph`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Affection.java#L36) **`Glowing(0xFF4488)`**: 개별 처리
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Affection.java#L39) **`proc(Armor armor, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, armor.buffedLvl, procChanceMultiplier, Random.Float, Buff.affect, Math.round, defender.id, attacker.sprite.centerEmitter, start
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Affection.java#L60) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":20,"fields":32,"methods":146}

# Java 파일별 소스 구현 해설 464–479

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 464. [`PotionOfMastery.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfMastery.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.exotic` / 본문 137행 / 타입 1개 / 필드 1개 / 메서드 7개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfMastery.java#L42) `class PotionOfMastery  extends ExoticPotion`

### 변수·상수 (단일 행 선언)

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfMastery.java#L52) `boolean identifiedByUse` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfMastery.java#L56) **`drink(final Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: isKnown, identify, detach, GameScene.selectItem
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfMastery.java#L69) **`ItemSelector()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: textPrompt, Messages.get, itemSelectable, onSelect, GameScene.show, WndOptions, ItemSprite, Messages.titleCase, name
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfMastery.java#L72) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfMastery.java#L77) **`itemSelectable(Item item)`**: 개별 처리
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfMastery.java#L84) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기·상태 선택 / 참조 호출: GameScene.show, WndOptions, ItemSprite, Messages.titleCase, name, Messages.get, onSelect, curUser.spendAndNext, GameScene.selectItem
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfMastery.java#L93) **`onSelect(int index)`**: 이벤트·효과 실행 / 상태 선택 / 참조 호출: curUser.spendAndNext, GameScene.selectItem
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfMastery.java#L104) **`onBackPressed()`**: 이벤트·효과 실행

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 465. [`PotionOfShielding.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfShielding.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.exotic` / 본문 53행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfShielding.java#L34) `class PotionOfShielding  extends ExoticPotion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfShielding.java#L41) **`apply(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: identify, Dungeon.isChallenged, PotionOfHealing.pharmacophobiaProc, Buff.affect, setShield, hero.sprite.showStatusWithIcon, Integer.toString

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 466. [`PotionOfShroudingFog.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfShroudingFog.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.exotic` / 본문 63행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfShroudingFog.java#L33) `class PotionOfShroudingFog  extends ExoticPotion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfShroudingFog.java#L40) **`shatter(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: splash, identify, Sample.INSTANCE.play, GameScene.add, Blob.seed

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 467. [`PotionOfSnapFreeze.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfSnapFreeze.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.exotic` / 본문 65행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfSnapFreeze.java#L35) `class PotionOfSnapFreeze  extends ExoticPotion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfSnapFreeze.java#L42) **`shatter(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: splash, identify, Sample.INSTANCE.play, Freezing.affect, Actor.findChar, Buff.prolong

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 468. [`PotionOfStamina.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfStamina.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.exotic` / 본문 45행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfStamina.java#L30) `class PotionOfStamina  extends ExoticPotion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfStamina.java#L37) **`apply(Hero hero)`**: 개별 처리 / 참조 호출: identify, Buff.prolong, SpellSprite.show

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 469. [`PotionOfStormClouds.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfStormClouds.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions.exotic` / 본문 62행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfStormClouds.java#L33) `class PotionOfStormClouds  extends ExoticPotion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfStormClouds.java#L40) **`shatter(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: splash, identify, Sample.INSTANCE.play, GameScene.add, Blob.seed

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 470. [`Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 568행 / 타입 3개 / 필드 8개 / 메서드 42개.

### 타입·상속 선언

- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L82) `class Potion  extends Item`
- [L450](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L450) `class PlaceHolder  extends Potion`
- [L468](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L468) `class SeedToPotion  extends Recipe`

### 변수·상수 (단일 행 선언)

- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L84) `String AC_DRINK` 초기식: `"DRINK"`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L87) `String AC_CHOOSE` 초기식: `"CHOOSE"`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L89) `float TIME_TO_DRINK` 초기식: `1f`
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L136) `ItemStatusHandler<Potion> handler`
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L138) `String color`
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L141) `float talentFactor` 초기식: `1`
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L143) `float talentChance` 초기식: `1`
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L192) `boolean anonymous` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L151) **`initColors()`**: 생성·초기화
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L155) **`clearColors()`**: 상태 갱신
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L159) **`save(Bundle bundle)`**: 저장·복원 / 참조 호출: handler.save
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L163) **`saveSelectively(Bundle bundle, ArrayList<Item> items)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: classes.contains, ExoticPotion.exoToReg.get, i.getClass, classes.add, handler.saveClassesSelectively
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L180) **`restore(Bundle bundle)`**: 저장·복원
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L184) **`Potion()`**: 개별 처리 / 참조 호출: reset
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L193) **`anonymize()`**: 개별 처리 / 조건 분기 / 참조 호출: isKnown
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L199) **`reset()`**: 생성·초기화 / 조건 분기 / 참조 호출: super.reset, handler.contains, handler.image, handler.label
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L211) **`defaultAction()`**: 개별 처리 / 조건 분기 / 참조 호출: isKnown, mustThrowPots.contains, this.getClass, canThrowPots.contains
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L222) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L229) **`execute(final Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, GameScene.show, WndUseItem, isKnown, mustThrowPots.contains, getClass, WndOptions, ItemSprite
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L247) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: drink
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L263) **`doThrow(final Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: isKnown, mustThrowPots.contains, this.getClass, canThrowPots.contains, GameScene.show, WndOptions, ItemSprite, Messages.get, onSelect
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L275) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Potion.super.doThrow
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L288) **`drink(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: detach, hero.spend, hero.busy, apply, Sample.INSTANCE.play, hero.sprite.operate, Catalog.countUse, getClass, Random.Float
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L309) **`onThrow(int cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onThrow, Dungeon.level.pressCell, shatter, mustThrowPots.contains, getClass, canThrowPots.contains, Catalog.countUse, Random.Float, Talent.onPotionUsed
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L332) **`apply(Hero hero)`**: 개별 처리 / 참조 호출: shatter
- [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L336) **`shatter(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: splash, GLog.i, Messages.get, Sample.INSTANCE.play
- [L345](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L345) **`cast(final Hero user, int dst)`**: 이벤트·효과 실행 / 참조 호출: super.cast
- [L349](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L349) **`isKnown()`**: 조건 판정 / 참조 호출: handler.isKnown
- [L353](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L353) **`setKnown()`**: 상태 갱신 / 조건 분기 / 참조 호출: isKnown, handler.know, updateQuickslot, Dungeon.hero.isAlive, Catalog.setSeen, getClass, Statistics.itemTypesDiscovered.add
- [L368](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L368) **`identify(boolean byHero)`**: 개별 처리 / 조건 분기 / 참조 호출: super.identify, isKnown, setKnown
- [L378](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L378) **`name()`**: 개별 처리 / 참조 호출: isKnown, super.name, Messages.get
- [L383](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L383) **`info()`**: 개별 처리 / 참조 호출: handler.isKnown, desc, super.info
- [L389](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L389) **`desc()`**: 개별 처리 / 참조 호출: isKnown, super.desc, Messages.get
- [L394](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L394) **`isIdentified()`**: 조건 판정 / 참조 호출: isKnown
- [L399](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L399) **`isUpgradable()`**: 조건 판정
- [L403](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L403) **`getKnown()`**: 조회·탐색 / 참조 호출: handler.known
- [L407](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L407) **`getUnknown()`**: 조회·탐색 / 참조 호출: handler.unknown
- [L411](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L411) **`allKnown()`**: 개별 처리 / 참조 호출: handler.known, size
- [L415](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L415) **`splashColor()`**: 개별 처리 / 참조 호출: ItemSprite.pick
- [L419](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L419) **`splash(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: level.blobs.get, fire.clear, Actor.findChar, Buff.detach, Splash.at, ch.sprite.center, splashColor
- [L441](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L441) **`value()`**: 개별 처리
- [L446](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L446) **`energyVal()`**: 개별 처리
- [L457](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L457) **`isSimilar(Item item)`**: 조건 판정 / 참조 호출: ExoticPotion.regToExo.containsKey, item.getClass, ExoticPotion.regToExo.containsValue
- [L463](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L463) **`info()`**: 개별 처리
- [L487](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L487) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: ingredients.size, ingredient.quantity, types.containsKey, ingredient.getClass
- [L503](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L503) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L508](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L508) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: testIngredients, ingredient.quantity, seeds.contains, i.getClass, seeds.add, seeds.size, Random.Int, Generator.randomUsingDefaults, Reflection.newInstance
- [L552](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L552) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: WndBag.Placeholder, name, Messages.get, info
- [L556](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L556) **`name()`**: 개별 처리 / 참조 호출: Messages.get
- [L561](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java#L561) **`info()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 471. [`PotionOfExperience.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfExperience.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 58행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfExperience.java#L30) `class PotionOfExperience  extends Potion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfExperience.java#L41) **`apply(Hero hero)`**: 개별 처리 / 참조 호출: identify, hero.sprite.showStatusWithIcon, Integer.toString, hero.maxExp, hero.earnExp, getClass, Flare, color, show
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfExperience.java#L49) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfExperience.java#L54) **`energyVal()`**: 개별 처리 / 참조 호출: isKnown, super.energyVal

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 472. [`PotionOfFrost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfFrost.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 64행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfFrost.java#L33) `class PotionOfFrost  extends Potion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfFrost.java#L40) **`shatter(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: splash, identify, Sample.INSTANCE.play, GameScene.add, Blob.seed
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfFrost.java#L60) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 473. [`PotionOfHaste.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHaste.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 52행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHaste.java#L32) `class PotionOfHaste  extends Potion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHaste.java#L39) **`apply(Hero hero)`**: 개별 처리 / 참조 호출: identify, GLog.w, Messages.get, Buff.prolong, SpellSprite.show
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHaste.java#L48) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 474. [`PotionOfHealing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 93행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java#L43) `class PotionOfHealing  extends Potion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java#L52) **`apply(Hero hero)`**: 개별 처리 / 참조 호출: identify, cure, heal
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java#L58) **`heal(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.isChallenged, pharmacophobiaProc, Buff.affect, healing.setHeal, GLog.p, Messages.get
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java#L71) **`pharmacophobiaProc(Hero hero)`**: 개별 처리 / 참조 호출: Buff.affect, set
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java#L76) **`cure(Char ch)`**: 개별 처리 / 참조 호출: Buff.detach
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java#L89) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 475. [`PotionOfInvisibility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfInvisibility.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 53행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfInvisibility.java#L33) `class PotionOfInvisibility  extends Potion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfInvisibility.java#L40) **`apply(Hero hero)`**: 개별 처리 / 참조 호출: identify, Buff.prolong, GLog.i, Messages.get, Sample.INSTANCE.play
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfInvisibility.java#L48) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 476. [`PotionOfLevitation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLevitation.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 69행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLevitation.java#L37) `class PotionOfLevitation  extends Potion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLevitation.java#L44) **`shatter(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: splash, identify, Sample.INSTANCE.play, GameScene.add, Blob.seed
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLevitation.java#L58) **`apply(Hero hero)`**: 개별 처리 / 참조 호출: identify, Buff.prolong, GLog.i, Messages.get
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLevitation.java#L65) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 477. [`PotionOfLiquidFlame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLiquidFlame.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 64행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLiquidFlame.java#L33) `class PotionOfLiquidFlame  extends Potion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLiquidFlame.java#L40) **`shatter(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: splash, identify, Sample.INSTANCE.play, GameScene.add, Blob.seed
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLiquidFlame.java#L60) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 478. [`PotionOfMindVision.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfMindVision.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 58행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfMindVision.java#L33) `class PotionOfMindVision  extends Potion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfMindVision.java#L40) **`apply(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: identify, Buff.prolong, SpellSprite.show, Dungeon.observe, level.mobs.size, GLog.i, Messages.get
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfMindVision.java#L54) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 479. [`PotionOfParalyticGas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfParalyticGas.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 57행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfParalyticGas.java#L32) `class PotionOfParalyticGas  extends Potion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfParalyticGas.java#L39) **`shatter(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: splash, identify, Sample.INSTANCE.play, GameScene.add, Blob.seed
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfParalyticGas.java#L53) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":18,"fields":9,"methods":77}

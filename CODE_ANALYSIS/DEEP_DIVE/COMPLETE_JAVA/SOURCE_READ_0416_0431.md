# Java 파일별 소스 구현 해설 416–431

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 416. [`PhantomMeat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/PhantomMeat.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.food` / 본문 63행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/PhantomMeat.java#L34) `class PhantomMeat  extends Food`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/PhantomMeat.java#L42) **`satisfy(Hero hero)`**: 개별 처리 / 참조 호출: super.satisfy, effect
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/PhantomMeat.java#L47) **`value()`**: 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/PhantomMeat.java#L51) **`effect(Hero hero)`**: 개별 처리 / 참조 호출: Barkskin.conditionallyAppend, Buff.affect, Math.min, hero.sprite.showStatusWithIcon, Integer.toString, PotionOfHealing.cure

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 417. [`SmallRation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/SmallRation.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.food` / 본문 39행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/SmallRation.java#L27) `class SmallRation  extends Food`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/SmallRation.java#L35) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 418. [`StewedMeat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/StewedMeat.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.food` / 본문 80행 / 타입 4개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/StewedMeat.java#L28) `class StewedMeat  extends Food`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/StewedMeat.java#L40) `class oneMeat  extends Recipe.SimpleRecipe`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/StewedMeat.java#L52) `class twoMeat  extends Recipe.SimpleRecipe`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/StewedMeat.java#L67) `class threeMeat  extends Recipe.SimpleRecipe`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/StewedMeat.java#L36) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 419. [`SupplyRation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/SupplyRation.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.food` / 본문 77행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/SupplyRation.java#L34) `class SupplyRation  extends Food`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/SupplyRation.java#L44) **`eatingTime()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.hasTalent
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/SupplyRation.java#L58) **`satisfy(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: super.satisfy, Math.min, hero.sprite.showStatusWithIcon, hero.belongings.getItem, cloak.directCharge, ScrollOfRecharging.charge
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/SupplyRation.java#L72) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 420. [`Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 975행 / 타입 2개 / 필드 18개 / 메서드 26개.

### 타입·상속 선언

- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L219) `class Generator`
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L221) `enum Category`

### 변수·상수 (단일 행 선언)

- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L254) `Class<?>[] classes`
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L260) `float[] probs`
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L261) `float[] defaultProbs` 초기식: `null`
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L265) `float[] defaultProbs2` 초기식: `null`
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L266) `boolean using2ndProbs` 초기식: `false`
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L268) `float[] defaultProbsTotal` 초기식: `null`
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L272) `Long seed` 초기식: `null`
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L273) `int dropped` 초기식: `0`
- [L278](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L278) `float firstProb`
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L279) `float secondProb`
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L280) `Class<? extends Item> superClass`
- [L621](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L621) `boolean usingFirstDeck` 초기식: `false`
- [L893](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L893) `String FIRST_DECK` 초기식: `"first_deck"`
- [L894](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L894) `String GENERAL_PROBS` 초기식: `"general_probs"`
- [L895](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L895) `String CATEGORY_PROBS` 초기식: `"_probs"`
- [L896](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L896) `String CATEGORY_USING_PROBS2` 초기식: `"_using_probs2"`
- [L897](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L897) `String CATEGORY_SEED` 초기식: `"_seed"`
- [L898](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L898) `String CATEGORY_DROPPED` 초기식: `"_dropped"`

### 함수·메서드 역할과 내부 연결

- [L282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L282) **`Category(float firstProb, float secondProb, Class<? extends Item> superClass)`**: 개별 처리
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L300) **`order(Item item)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: values, subOrderings.get, subOrdering.size, subOrdering.get, isInstance, superClass.isInstance, item.image
- [L625](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L625) **`fullReset()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Random.Int, generalReset, Category.values, reset, Random.Long
- [L638](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L638) **`generalReset()`**: 개별 처리 / 반복 / 참조 호출: Category.values, categoryProbs.put, defaultCatProbs.put
- [L645](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L645) **`reset(Category cat)`**: 생성·초기화 / 조건 분기 / 참조 호출: cat.defaultProbs2.clone, cat.defaultProbs.clone
- [L658](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L658) **`undoDrop(Item item)`**: 개별 처리 / 참조 호출: undoDrop, item.getClass
- [L662](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L662) **`undoDrop(Class cls)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Category.values, cls.isAssignableFrom
- [L675](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L675) **`random()`**: 개별 처리 / 조건 분기 / 참조 호출: Random.chances, generalReset, categoryProbs.put, categoryProbs.get, randomUsingDefaults, random
- [L694](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L694) **`randomUsingDefaults()`**: 개별 처리 / 참조 호출: randomUsingDefaults, Random.chances
- [L698](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L698) **`random(Category cat)`**: 개별 처리 / 조건 분기·반복·상태 선택 / 참조 호출: randomArmor, randomWeapon, randomMissile, randomArtifact, randomUsingDefaults, Random.pushGenerator, Random.Long, Random.chances, reset
- [L746](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L746) **`randomUsingDefaults(Category cat)`**: 개별 처리 / 조건 분기 / 참조 호출: randomWeapon, randomMissile, random, Reflection.newInstance, Random.chances, ExoticPotion.regToExo.containsKey, Random.Float, ExoticCrystals.consumableExoticChance, ExoticPotion.regToExo.get
- [L772](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L772) **`random(Class<? extends Item> cl)`**: 개별 처리 / 참조 호출: Reflection.newInstance, random
- [L776](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L776) **`randomArmor()`**: 개별 처리 / 참조 호출: randomArmor
- [L780](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L780) **`randomArmor(int floorSet)`**: 개별 처리 / 참조 호출: GameMath.gate, Reflection.newInstance, Random.chances, a.random
- [L797](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L797) **`randomWeapon()`**: 개별 처리 / 참조 호출: randomWeapon
- [L801](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L801) **`randomWeapon(int floorSet)`**: 개별 처리 / 참조 호출: randomWeapon
- [L805](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L805) **`randomWeapon(boolean useDefaults)`**: 개별 처리 / 참조 호출: randomWeapon
- [L809](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L809) **`randomWeapon(int floorSet, boolean useDefaults)`**: 개별 처리 / 조건 분기 / 참조 호출: GameMath.gate, randomUsingDefaults, Random.chances, random
- [L830](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L830) **`randomMissile()`**: 개별 처리 / 참조 호출: randomMissile
- [L834](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L834) **`randomMissile(int floorSet)`**: 개별 처리 / 참조 호출: randomMissile
- [L838](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L838) **`randomMissile(boolean useDefaults)`**: 개별 처리 / 참조 호출: randomMissile
- [L842](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L842) **`randomMissile(int floorSet, boolean useDefaults)`**: 개별 처리 / 조건 분기 / 참조 호출: GameMath.gate, randomUsingDefaults, Random.chances, random
- [L856](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L856) **`randomArtifact()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Random.pushGenerator, Random.Long, Random.chances, Random.popGenerator, Reflection.newInstance, random
- [L882](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L882) **`removeArtifact(Class<?extends Artifact> artifact)`**: 상태 갱신 / 조건 분기·반복 / 참조 호출: equals
- [L900](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L900) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: bundle.put, categoryProbs.values, toArray, Category.values, cat.name, toLowerCase
- [L926](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L926) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: fullReset, bundle.getBoolean, bundle.contains, bundle.getFloatArray, Category.values, categoryProbs.put, cat.name, toLowerCase, bundle.getLong

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 421. [`Gold.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Gold.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 96행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Gold.java#L39) `class Gold  extends Item`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Gold.java#L46) **`Gold()`**: 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Gold.java#L50) **`Gold(int value)`**: 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Gold.java#L55) **`actions(Hero hero)`**: 시간·상태 갱신
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Gold.java#L60) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 참조 호출: Catalog.setSeen, getClass, Statistics.itemTypesDiscovered.add, Badges.validateGoldCollected, GameScene.pickUp, hero.sprite.showStatusWithIcon, Integer.toString, hero.spendAndNext, pickupDelay
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Gold.java#L80) **`isUpgradable()`**: 조건 판정
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Gold.java#L85) **`isIdentified()`**: 조건 판정
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Gold.java#L90) **`random()`**: 개별 처리 / 참조 호출: Random.IntRange

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 422. [`Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 468행 / 타입 2개 / 필드 14개 / 메서드 19개.

### 타입·상속 선언

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L60) `class Heap  implements Bundlable`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L62) `enum Type`

### 변수·상수 (단일 행 선언)

- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L72) `Type type` 초기식: `Type.HEAP`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L74) `int pos` 초기식: `0`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L76) `ItemSprite sprite`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L77) `boolean seen` 초기식: `false`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L78) `boolean haunted` 초기식: `false`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L79) `boolean autoExplored` 초기식: `false`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L80) `boolean hidden` 초기식: `false`
- [L421](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L421) `String POS` 초기식: `"pos"`
- [L422](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L422) `String SEEN` 초기식: `"seen"`
- [L423](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L423) `String TYPE` 초기식: `"type"`
- [L424](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L424) `String ITEMS` 초기식: `"items"`
- [L425](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L425) `String HAUNTED` 초기식: `"haunted"`
- [L426](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L426) `String AUTO_EXPLORED` 초기식: `"auto_explored"`
- [L427](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L427) `String HIDDEN` 초기식: `"hidden"`

### 함수·메서드 역할과 내부 연결

- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L84) **`open(Hero hero)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Wraith.spawnAround, CellEmitter.center, start, Speck.factory, Wraith.spawnAt, hero.sprite.emitter, burst, hero.damage, hero.isAlive
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L118) **`setHauntedIfCursed()`**: 상태 갱신 / 조건 분기·반복
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L129) **`size()`**: 개별 처리 / 참조 호출: items.size
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L133) **`pickUp()`**: 개별 처리 / 조건 분기 / 참조 호출: items.isEmpty, destroy, items.removeFirst, sprite.view, place
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L149) **`peek()`**: 개별 처리 / 참조 호출: items.peek
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L153) **`drop(Item item)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: i.isSimilar, i.merge, items.remove, items.add, peek, items.addFirst, sprite.view, place, Dart
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L190) **`replace(Item a, Item b)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: items.indexOf, items.remove, i.isSimilar, i.merge, items.add
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L205) **`remove(Item a)`**: 상태 갱신 / 조건 분기 / 참조 호출: items.remove, items.isEmpty, destroy, sprite.view, place
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L215) **`burn()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: items.toArray, items.remove, replace, ChargrilledMeat.cook, explode, explodesDestructively, burnFX, evaporateFX, isEmpty
- [L267](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L267) **`explode()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: sprite.link, sprite.drop, items.toArray, item.isUpgradable, items.remove, shatter, destroyPot, explode, explodesDestructively
- [L321](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L321) **`freeze()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: items.toArray, replace, FrozenCarpaccio.cook, items.remove, shatter, fuse.freeze, isEmpty, destroy, sprite.view
- [L350](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L350) **`burnFX(int pos)`**: 개별 처리 / 참조 호출: CellEmitter.get, burst, Sample.INSTANCE.play
- [L355](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L355) **`evaporateFX(int pos)`**: 개별 처리 / 참조 호출: CellEmitter.get, burst, Speck.factory
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L359) **`isEmpty()`**: 조건 판정 / 참조 호출: items.size
- [L363](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L363) **`destroy()`**: 개별 처리 / 조건 분기 / 참조 호출: level.heaps.remove, sprite.kill, items.clear
- [L371](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L371) **`title()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: peek, size, Messages.get, Shopkeeper.sellPrice, i.title, title
- [L397](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L397) **`info()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Messages.get, peek, info
- [L431](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L431) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: bundle.getInt, bundle.getBoolean, Type.valueOf, bundle.getString, bundle.getCollection, items.removeAll, Collections.singleton, items.toArray, document
- [L457](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L457) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: bundle.put

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 423. [`Honeypot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 258행 / 타입 2개 / 필드 1개 / 메서드 20개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L42) `class Honeypot  extends Item`
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L154) `class ShatteredPot  extends Item`

### 변수·상수 (단일 행 선언)

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L44) `String AC_SHATTER` 초기식: `"SHATTER"`

### 함수·메서드 역할과 내부 연결

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L56) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L63) **`execute(final Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, hero.sprite.zap, detach, Catalog.countUse, getClass, shatter, item.collect, Dungeon.level.drop
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L88) **`onThrow(int cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onThrow, Catalog.countUse, getClass, Dungeon.level.drop, shatter
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L97) **`shatter(Char owner, int pos)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Sample.INSTANCE.play, Splash.at, Actor.findChar, candidates.add, candidates.size, Random.element, Bee, bee.spawn, Dungeon.scalingDepth
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L139) **`isUpgradable()`**: 조건 판정
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L144) **`isIdentified()`**: 조건 판정
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L149) **`value()`**: 개별 처리
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L162) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doPickUp, pickupPot
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L172) **`doDrop(Hero hero)`**: 개별 처리 / 참조 호출: super.doDrop, dropPot
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L178) **`onThrow(int cell)`**: 이벤트·효과 실행 / 참조 호출: super.onThrow, dropPot
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L183) **`pickupPot(Char holder)`**: 개별 처리 / 반복 / 참조 호출: findBees, updateBee
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L189) **`dropPot(Char holder, int dropPos)`**: 개별 처리 / 반복 / 참조 호출: findBees, updateBee
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L195) **`movePot(int oldpos, int movePos)`**: 개별 처리 / 반복 / 참조 호출: findBees, updateBee
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L201) **`destroyPot(int potPos)`**: 개별 처리 / 반복 / 참조 호출: findBees, updateBee
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L207) **`updateBee(Bee bee, int cell, Char holder)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: bee.setPotInfo
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L213) **`findBees(int potPos)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: Actor.chars, potPos, bees.add, bees.size
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L228) **`findBees(Char potHolder)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: Actor.chars, potHolderID, potHolder.id, bees.add, bees.size
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L243) **`isUpgradable()`**: 조건 판정
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L248) **`isIdentified()`**: 조건 판정
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java#L253) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 424. [`Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 728행 / 타입 1개 / 필드 32개 / 메서드 73개.

### 타입·상속 선언

- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L61) `class Item  implements Bundlable`

### 변수·상수 (단일 행 선언)

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L63) `String TXT_TO_STRING_LVL` 초기식: `"%s %+d"`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L64) `String TXT_TO_STRING_X` 초기식: `"%s x%d"`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L66) `float TIME_TO_THROW` 초기식: `1.0f`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L67) `float TIME_TO_PICK_UP` 초기식: `1.0f`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L68) `float TIME_TO_DROP` 초기식: `1.0f`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L70) `String AC_DROP` 초기식: `"DROP"`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L71) `String AC_THROW` 초기식: `"THROW"`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L73) `String defaultAction`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L74) `boolean usesTargeting`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L77) `int image` 초기식: `0`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L78) `int icon` 초기식: `-1`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L80) `boolean stackable` 초기식: `false`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L81) `int quantity` 초기식: `1`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L82) `boolean dropsDownHeap` 초기식: `false`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L84) `int level` 초기식: `0`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L86) `boolean levelKnown` 초기식: `false`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L88) `boolean cursed`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L89) `boolean cursedKnown`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L92) `boolean unique` 초기식: `false`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L96) `boolean keptThoughLostInvent` 초기식: `false`
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L99) `boolean bones` 초기식: `false`
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L101) `int customNoteID` 초기식: `-1`
- [L580](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L580) `String QUANTITY` 초기식: `"quantity"`
- [L581](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L581) `String LEVEL` 초기식: `"level"`
- [L582](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L582) `String LEVEL_KNOWN` 초기식: `"levelKnown"`
- [L583](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L583) `String CURSED` 초기식: `"cursed"`
- [L584](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L584) `String CURSED_KNOWN` 초기식: `"cursedKnown"`
- [L585](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L585) `String QUICKSLOT` 초기식: `"quickslotpos"`
- [L586](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L586) `String KEPT_LOST` 초기식: `"kept_lost"`
- [L587](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L587) `String CUSTOM_NOTE_ID` 초기식: `"custom_note_id"`
- [L708](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L708) `Hero curUser` 초기식: `null`
- [L709](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L709) `Item curItem` 초기식: `null`

### 함수·메서드 역할과 내부 연결

- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L105) **`compare(Item lhs, Item rhs)`**: 개별 처리 / 참조 호출: Generator.Category.order
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L110) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: actions.add
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L117) **`actionName(String action, Hero hero)`**: 시간·상태 갱신 / 참조 호출: Messages.get
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L121) **`doPickUp(Hero hero)`**: 개별 처리 / 참조 호출: doPickUp
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L125) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: collect, GameScene.pickUp, Sample.INSTANCE.play, hero.spendAndNext, pickupDelay
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L138) **`doDrop(Hero hero)`**: 개별 처리 / 참조 호출: hero.spendAndNext, Dungeon.level.drop, detachAll, sprite.drop
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L145) **`reset()`**: 생성·초기화
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L149) **`keptThroughLostInventory()`**: 개별 처리
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L153) **`doThrow(Hero hero)`**: 개별 처리 / 참조 호출: GameScene.selectCell
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L157) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: GameScene.cancel, action.equals, belongings.backpack.contains, isEquipped, doDrop, doThrow
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L179) **`defaultAction()`**: 개별 처리
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L183) **`execute(Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: defaultAction, execute
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L190) **`onThrow(int cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Dungeon.level.drop, heap.isEmpty, heap.sprite.drop
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L198) **`merge(Item other)`**: 개별 처리 / 조건 분기 / 참조 호출: isSimilar
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L206) **`collect(Bag container)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: items.contains, canHold, collect, container.canHold, isSimilar, item.merge, item.updateQuickslot, Dungeon.hero.isAlive, Badges.validateItemLevelAquired
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L252) **`act()`**: 시간·상태 갱신 / 참조 호출: Dungeon.level.drop, sprite.drop, Actor.remove
- [L282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L282) **`collect()`**: 개별 처리 / 참조 호출: collect
- [L287](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L287) **`split(int amount)`**: 개별 처리 / 조건 분기 / 참조 호출: quantity, Reflection.newInstance, getClass, Bundle, this.storeInBundle, split.restoreFromBundle, split.quantity
- [L308](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L308) **`duplicate()`**: 개별 처리 / 조건 분기 / 참조 호출: Reflection.newInstance, getClass, Bundle, this.storeInBundle, dupe.restoreFromBundle
- [L319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L319) **`detach(Bag container)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.quickslot.convertToPlaceholder, detachAll, split, updateQuickslot, detached.onDetach
- [L345](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L345) **`detachAll(Bag container)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.quickslot.clearItem, container.items.remove, item.onDetach, container.grabItems, updateQuickslot, bag.contains, detachAll
- [L367](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L367) **`isSimilar(Item item)`**: 조건 판정 / 참조 호출: getClass, item.getClass
- [L371](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L371) **`onDetach()`**: 이벤트·효과 실행
- [L374](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L374) **`trueLevel()`**: 개별 처리
- [L379](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L379) **`level()`**: 개별 처리
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L385) **`buffedLvl()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.buff, isEquipped, hero.belongings.contains, Degrade.reduceLevel, level
- [L395](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L395) **`level(int value)`**: 개별 처리 / 참조 호출: updateQuickslot
- [L403](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L403) **`upgrade()`**: 개별 처리 / 참조 호출: updateQuickslot
- [L412](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L412) **`upgrade(int n)`**: 개별 처리 / 반복 / 참조 호출: upgrade
- [L420](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L420) **`degrade()`**: 개별 처리
- [L427](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L427) **`degrade(int n)`**: 개별 처리 / 반복 / 참조 호출: degrade
- [L435](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L435) **`visiblyUpgraded()`**: 개별 처리 / 참조 호출: level
- [L439](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L439) **`buffedVisiblyUpgraded()`**: 개별 처리 / 참조 호출: buffedLvl
- [L443](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L443) **`visiblyCursed()`**: 개별 처리
- [L447](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L447) **`isUpgradable()`**: 조건 판정
- [L451](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L451) **`isIdentified()`**: 조건 판정
- [L455](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L455) **`isEquipped(Hero hero)`**: 조건 판정
- [L459](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L459) **`identify()`**: 개별 처리 / 참조 호출: identify
- [L463](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L463) **`identify(boolean byHero)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.isAlive, Catalog.setSeen, getClass, Statistics.itemTypesDiscovered.add, Item.updateQuickslot
- [L477](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L477) **`onHeroGainExp(float levelPercent, Hero hero)`**: 이벤트·효과 실행
- [L481](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L481) **`evoke(Hero hero)`**: 개별 처리 / 참조 호출: hero.sprite.emitter, burst, Speck.factory
- [L485](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L485) **`title()`**: 개별 처리 / 조건 분기 / 참조 호출: name, visiblyUpgraded, Messages.format
- [L499](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L499) **`name()`**: 개별 처리 / 참조 호출: trueName
- [L503](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L503) **`trueName()`**: 개별 처리 / 참조 호출: Messages.get
- [L507](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L507) **`image()`**: 개별 처리
- [L511](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L511) **`glowing()`**: 개별 처리
- [L515](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L515) **`emitter()`**: 개별 처리
- [L517](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L517) **`info()`**: 개별 처리 / 조건 분기 / 참조 호출: Notes.findCustomRecord, Messages.get, note.title, replace, desc, getClass
- [L536](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L536) **`desc()`**: 개별 처리 / 참조 호출: Messages.get
- [L540](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L540) **`quantity()`**: 개별 처리
- [L544](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L544) **`quantity(int value)`**: 개별 처리
- [L550](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L550) **`value()`**: 개별 처리
- [L555](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L555) **`energyVal()`**: 개별 처리
- [L559](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L559) **`virtual()`**: 개별 처리 / 조건 분기 / 참조 호출: Reflection.newInstance, getClass
- [L568](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L568) **`random()`**: 개별 처리
- [L572](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L572) **`status()`**: 개별 처리 / 참조 호출: Integer.toString
- [L576](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L576) **`updateQuickslot()`**: 시간·상태 갱신
- [L590](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L590) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: bundle.put, Dungeon.quickslot.contains, Dungeon.quickslot.getSlot
- [L604](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L604) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: bundle.getInt, bundle.getBoolean, upgrade, degrade, bundle.contains, Dungeon.quickslot.setSlot
- [L629](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L629) **`targetingPos(Hero user, int dst)`**: 개별 처리 / 참조 호출: throwPos
- [L633](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L633) **`throwPos(Hero user, int dst)`**: 개별 처리 / 참조 호출: Ballistica
- [L637](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L637) **`throwSound()`**: 개별 처리 / 참조 호출: Sample.INSTANCE.play
- [L641](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L641) **`cast(final Hero user, final int dst)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: throwPos, user.sprite.zap, user.busy, throwSound, Actor.findChar, QuickSlotButton.target, castDelay, sprite.parent.recycle, reset
- [L643](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L643) **`throwPos(user, dst)`**: 개별 처리
- [L652](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L652) **`castDelay(user, cell)`**: 이벤트·효과 실행
- [L661](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L661) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Item.this.detach, i.onThrow, curUser.hasTalent, curUser.buff, Sample.INSTANCE.play, Buff.affect, curUser.pointsInTalent, user.buff, detach
- [L689](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L689) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Item.this.detach, user.spend, i.onThrow, user.next
- [L700](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L700) **`castDelay(Char user, int cell)`**: 이벤트·효과 실행
- [L704](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L704) **`pickupDelay()`**: 개별 처리
- [L710](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L710) **`setCurrent(Hero hero)`**: 상태 갱신
- [L715](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L715) **`Listener()`**: 개별 처리 / 조건 분기 / 참조 호출: onSelect, curItem.cast, prompt, Messages.get
- [L717](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L717) **`onSelect(Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: curItem.cast
- [L723](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L723) **`prompt()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 425. [`ItemStatusHandler.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 217행 / 타입 1개 / 필드 6개 / 메서드 18개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L35) `class ItemStatusHandler <T extends Item>`

### 변수·상수 (단일 행 선언)

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L37) `Class<? extends T>[] items`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L38) `LinkedHashMap<Class<? extends T>, String> itemLabels`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L39) `LinkedHashMap<String, Integer> labelImages`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L40) `LinkedHashSet<Class<? extends T>> known`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L77) `String PFX_LABEL` 초기식: `"_label"`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L78) `String PFX_KNOWN` 초기식: `"_known"`

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L42) **`ItemStatusHandler(Class<? extends T>[] items, HashMap<String, Integer> labelImages)`**: 개별 처리 / 반복 / 참조 호출: labelImages.keySet, Random.Int, labelsLeft.size, itemLabels.put, labelsLeft.get, labelsLeft.remove
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L64) **`ItemStatusHandler(Class<? extends T>[] items, HashMap<String, Integer> labelImages, Bundle bundle)`**: 개별 처리 / 참조 호출: labelImages.keySet, restore
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L80) **`save(Bundle bundle)`**: 저장·복원 / 반복 / 참조 호출: getSimpleName, bundle.put, itemLabels.get, known.contains
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L88) **`saveSelectively(Bundle bundle, ArrayList<Item> itemsToSave)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: Arrays.asList, items.contains, item.getClass, items.get, items.indexOf, cls.getSimpleName, bundle.put, itemLabels.get, known.contains
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L100) **`saveClassesSelectively(Bundle bundle, ArrayList<Class<?extends Item>> clsToSave)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: Arrays.asList, items.contains, items.get, items.indexOf, toSave.getSimpleName, bundle.put, itemLabels.get, known.contains
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L112) **`restore(Bundle bundle, ArrayList<String> labelsLeft)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: item.getSimpleName, bundle.contains, bundle.getString, itemLabels.put, labelsLeft.remove, bundle.getBoolean, known.add, unlabelled.add, Random.Int
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L153) **`contains(T item)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: item.getClass, equals
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L162) **`contains(Class<?extends T> itemCls)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: itemCls.equals
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L171) **`image(T item)`**: 개별 처리 / 참조 호출: labelImages.get, label
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L175) **`image(Class<?extends T> itemCls)`**: 개별 처리 / 참조 호출: labelImages.get, label
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L179) **`label(T item)`**: 개별 처리 / 참조 호출: itemLabels.get, item.getClass
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L183) **`label(Class<?extends T> itemCls)`**: 개별 처리 / 참조 호출: itemLabels.get
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L187) **`isKnown(T item)`**: 조건 판정 / 참조 호출: known.contains, item.getClass
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L191) **`isKnown(Class<?extends T> itemCls)`**: 조건 판정 / 참조 호출: known.contains
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L195) **`know(T item)`**: 개별 처리 / 참조 호출: known.add, item.getClass
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L199) **`know(Class<?extends T> itemCls)`**: 개별 처리 / 참조 호출: known.add
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L203) **`known()`**: 개별 처리
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java#L207) **`unknown()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: known.contains, result.add

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 426. [`AlchemyPage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/AlchemyPage.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.journal` / 본문 44행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/AlchemyPage.java#L28) `class AlchemyPage  extends DocumentPage`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/AlchemyPage.java#L35) **`document()`**: 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/AlchemyPage.java#L40) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, document, pageTitle, page

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 427. [`DocumentPage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.journal` / 본문 95행 / 타입 1개 / 필드 2개 / 메서드 8개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java#L34) `class DocumentPage  extends Item`

### 변수·상수 (단일 행 선언)

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java#L42) `String page`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java#L81) `String PAGE` 초기식: `"page"`

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java#L40) **`document()`**: 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java#L44) **`page(String page)`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java#L48) **`page()`**: 개별 처리
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java#L53) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.pickUpJournal, GameScene.flashForDocument, document, page, pageIdx, isLoreDoc, findPage, Sample.INSTANCE.play, hero.spendAndNext
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java#L72) **`isUpgradable()`**: 조건 판정
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java#L77) **`isIdentified()`**: 조건 판정
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java#L84) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put, page
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java#L90) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getString

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 428. [`Guidebook.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/Guidebook.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.journal` / 본문 81행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/Guidebook.java#L39) `class Guidebook  extends Item`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/Guidebook.java#L46) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: Document.ADVENTURERS_GUIDE.findPage, GameScene.pickUpJournal, GameLog.wipe, GLog.i, Messages.capitalize, Messages.get, name, SPDSettings.interfaceSize, GLog.p
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/Guidebook.java#L71) **`isUpgradable()`**: 조건 판정
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/Guidebook.java#L76) **`isIdentified()`**: 조건 판정

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 429. [`GuidePage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/GuidePage.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.journal` / 본문 44행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/GuidePage.java#L28) `class GuidePage  extends DocumentPage`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/GuidePage.java#L35) **`document()`**: 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/GuidePage.java#L40) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, document, pageTitle, page

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 430. [`RegionLorePage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.journal` / 본문 95행 / 타입 6개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java#L27) `class RegionLorePage`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java#L39) `class Sewers  extends DocumentPage`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java#L50) `class Prison  extends DocumentPage`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java#L61) `class Caves  extends DocumentPage`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java#L72) `class City  extends DocumentPage`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java#L83) `class Halls  extends DocumentPage`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java#L29) **`pageForDoc(Document doc)`**: 개별 처리 / 상태 선택 / 참조 호출: RegionLorePage.Sewers, RegionLorePage.Prison, RegionLorePage.Caves, RegionLorePage.City, RegionLorePage.Halls
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java#L45) **`document()`**: 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java#L56) **`document()`**: 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java#L67) **`document()`**: 개별 처리
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java#L78) **`document()`**: 개별 처리
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java#L89) **`document()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 431. [`CrystalKey.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/CrystalKey.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.keys` / 본문 42행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/CrystalKey.java#L26) `class CrystalKey  extends Key`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/CrystalKey.java#L32) **`CrystalKey()`**: 개별 처리
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/CrystalKey.java#L36) **`CrystalKey(int depth)`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":27,"fields":73,"methods":194}

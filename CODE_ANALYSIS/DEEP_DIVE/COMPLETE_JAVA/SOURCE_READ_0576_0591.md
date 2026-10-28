# Java 파일별 소스 구현 해설 576–591

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 576. [`ExoticCrystals.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ExoticCrystals.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 61행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ExoticCrystals.java#L27) `class ExoticCrystals  extends Trinket`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ExoticCrystals.java#L34) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ExoticCrystals.java#L40) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, consumableExoticChance, buffedLvl
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ExoticCrystals.java#L48) **`consumableExoticChance()`**: 개별 처리 / 참조 호출: consumableExoticChance, trinketLevel
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ExoticCrystals.java#L52) **`consumableExoticChance(int level)`**: 개별 처리 / 조건 분기

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 577. [`EyeOfNewt.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/EyeOfNewt.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 77행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/EyeOfNewt.java#L27) `class EyeOfNewt  extends Trinket`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/EyeOfNewt.java#L34) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/EyeOfNewt.java#L40) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, visionRangeMultiplier, buffedLvl, mindVisionRange
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/EyeOfNewt.java#L52) **`visionRangeMultiplier()`**: 개별 처리 / 참조 호출: visionRangeMultiplier, trinketLevel
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/EyeOfNewt.java#L56) **`visionRangeMultiplier(int level)`**: 개별 처리 / 조건 분기
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/EyeOfNewt.java#L64) **`mindVisionRange()`**: 개별 처리 / 참조 호출: mindVisionRange, trinketLevel
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/EyeOfNewt.java#L68) **`mindVisionRange(int level)`**: 개별 처리 / 조건 분기

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 578. [`FerretTuft.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/FerretTuft.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 62행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/FerretTuft.java#L28) `class FerretTuft  extends Trinket`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/FerretTuft.java#L35) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/FerretTuft.java#L41) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, evasionMultiplier, buffedLvl
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/FerretTuft.java#L49) **`evasionMultiplier()`**: 개별 처리 / 참조 호출: evasionMultiplier, trinketLevel
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/FerretTuft.java#L53) **`evasionMultiplier(int level)`**: 개별 처리 / 조건 분기

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 579. [`MimicTooth.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MimicTooth.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 81행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MimicTooth.java#L27) `class MimicTooth  extends Trinket`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MimicTooth.java#L34) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MimicTooth.java#L40) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, mimicChanceMultiplier, buffedLvl, ebonyMimicChance
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MimicTooth.java#L52) **`mimicChanceMultiplier()`**: 개별 처리 / 참조 호출: mimicChanceMultiplier, trinketLevel
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MimicTooth.java#L56) **`mimicChanceMultiplier(int level)`**: 개별 처리 / 조건 분기
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MimicTooth.java#L64) **`stealthyMimics()`**: 개별 처리 / 참조 호출: trinketLevel
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MimicTooth.java#L68) **`ebonyMimicChance()`**: 개별 처리 / 참조 호출: ebonyMimicChance, trinketLevel
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MimicTooth.java#L72) **`ebonyMimicChance(int level)`**: 개별 처리 / 조건 분기

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 580. [`MossyClump.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 122행 / 타입 1개 / 필드 3개 / 메서드 7개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java#L33) `class MossyClump  extends Trinket`

### 변수·상수 (단일 행 선언)

- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java#L69) `int shuffles` 초기식: `0`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java#L94) `String FEELS` 초기식: `"feels"`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java#L95) `String SHUFFLES` 초기식: `"shuffles"`

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java#L40) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java#L46) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, overrideNormalLevelChance, buffedLvl
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java#L54) **`overrideNormalLevelChance()`**: 개별 처리 / 참조 호출: overrideNormalLevelChance, trinketLevel
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java#L58) **`overrideNormalLevelChance(int level)`**: 개별 처리 / 조건 분기
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java#L71) **`getNextFeeling()`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: hero.belongings.getItem, clump.levelFeels.isEmpty, Random.pushGenerator, clump.levelFeels.add, Random.shuffle, Random.popGenerator, clump.levelFeels.remove
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java#L98) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: super.storeInBundle, levelFeels.isEmpty, levelFeels.size, levelFeels.get, bundle.put
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java#L111) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: super.restoreFromBundle, levelFeels.clear, bundle.contains, bundle.getBooleanArray, levelFeels.add, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 581. [`ParchmentScrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ParchmentScrap.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 86행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ParchmentScrap.java#L27) `class ParchmentScrap  extends Trinket`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ParchmentScrap.java#L34) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ParchmentScrap.java#L40) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, enchantChanceMultiplier, buffedLvl, Messages.decimalFormat, curseChanceMultiplier
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ParchmentScrap.java#L48) **`enchantChanceMultiplier()`**: 개별 처리 / 참조 호출: enchantChanceMultiplier, trinketLevel
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ParchmentScrap.java#L52) **`enchantChanceMultiplier(int level)`**: 개별 처리 / 상태 선택
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ParchmentScrap.java#L67) **`curseChanceMultiplier()`**: 개별 처리 / 참조 호출: curseChanceMultiplier, trinketLevel
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ParchmentScrap.java#L71) **`curseChanceMultiplier(int level)`**: 개별 처리 / 상태 선택

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 582. [`PetrifiedSeed.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/PetrifiedSeed.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 86행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/PetrifiedSeed.java#L27) `class PetrifiedSeed  extends Trinket`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/PetrifiedSeed.java#L34) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/PetrifiedSeed.java#L40) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, stoneInsteadOfSeedChance, buffedLvl, grassLootMultiplier
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/PetrifiedSeed.java#L52) **`grassLootMultiplier()`**: 개별 처리 / 참조 호출: grassLootMultiplier, trinketLevel
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/PetrifiedSeed.java#L56) **`grassLootMultiplier(int level)`**: 개별 처리 / 조건 분기
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/PetrifiedSeed.java#L64) **`stoneInsteadOfSeedChance()`**: 개별 처리 / 참조 호출: stoneInsteadOfSeedChance, trinketLevel
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/PetrifiedSeed.java#L71) **`stoneInsteadOfSeedChance(int level)`**: 개별 처리 / 상태 선택

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 583. [`RatSkull.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/RatSkull.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 61행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/RatSkull.java#L27) `class RatSkull  extends Trinket`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/RatSkull.java#L34) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/RatSkull.java#L40) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, exoticChanceMultiplier, buffedLvl
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/RatSkull.java#L48) **`exoticChanceMultiplier()`**: 개별 처리 / 참조 호출: exoticChanceMultiplier, trinketLevel
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/RatSkull.java#L52) **`exoticChanceMultiplier(int level)`**: 개별 처리 / 조건 분기

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 584. [`SaltCube.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/SaltCube.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 86행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/SaltCube.java#L27) `class SaltCube  extends Trinket`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/SaltCube.java#L34) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/SaltCube.java#L40) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, hungerGainMultiplier, buffedLvl, healthRegenMultiplier
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/SaltCube.java#L54) **`hungerGainMultiplier()`**: 개별 처리 / 참조 호출: hungerGainMultiplier, trinketLevel
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/SaltCube.java#L58) **`hungerGainMultiplier(int level)`**: 개별 처리 / 조건 분기
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/SaltCube.java#L66) **`healthRegenMultiplier()`**: 개별 처리 / 참조 호출: healthRegenMultiplier, trinketLevel
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/SaltCube.java#L70) **`healthRegenMultiplier(int level)`**: 개별 처리 / 상태 선택

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 585. [`ShardOfOblivion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 227행 / 타입 3개 / 필드 3개 / 메서드 17개.

### 타입·상속 선언

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L47) `class ShardOfOblivion  extends Trinket`
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L142) `class WandUseTracker  extends FlavourBuff`
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L167) `class ThrownUseTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L53) `String AC_IDENTIFY` 초기식: `"IDENTIFY"`
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L148) `float DURATION` 초기식: `50f`
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L173) `float DURATION` 초기식: `50f`

### 함수·메서드 역할과 내부 연결

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L56) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L62) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, buffedLvl
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L71) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L78) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: action.equals, GameScene.selectItem, super.execute
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L88) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, Messages.get, itemSelectable, item.isIdentified, item.isUpgradable, onSelect, readyToIdentify, item.isEquipped, curUser.pointsInTalent
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L90) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L95) **`itemSelectable(Item item)`**: 개별 처리 / 참조 호출: item.isIdentified, item.isUpgradable
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L100) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: readyToIdentify, item.isEquipped, curUser.pointsInTalent, item.identify, Badges.validateItemLevelAquired, curUser.sprite.operate, Sample.INSTANCE.play, sprite.parent.add, Identification
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L138) **`passiveIDDisabled()`**: 개별 처리 / 참조 호출: trinketLevel
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L151) **`icon()`**: 개별 처리
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L156) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L161) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L176) **`icon()`**: 개별 처리
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L181) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L186) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L192) **`lootChanceMultiplier()`**: 개별 처리 / 참조 호출: lootChanceMultiplier, trinketLevel
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java#L196) **`lootChanceMultiplier(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.weapon, isIdentified, hero.belongings.secondWep, hero.belongings.armor, hero.belongings.ring, hero.belongings.misc, Dungeon.hero.buff, Math.min

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 586. [`ThirteenLeafClover.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ThirteenLeafClover.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 72행 / 타입 1개 / 필드 1개 / 메서드 5개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ThirteenLeafClover.java#L28) `class ThirteenLeafClover  extends Trinket`

### 변수·상수 (단일 행 선언)

- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ThirteenLeafClover.java#L61) `float MAX_CHANCE` 초기식: `0.6f`

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ThirteenLeafClover.java#L35) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ThirteenLeafClover.java#L41) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Math.round, alterHeroDamageChance, buffedLvl
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ThirteenLeafClover.java#L49) **`alterHeroDamageChance()`**: 개별 처리 / 참조 호출: alterHeroDamageChance, trinketLevel
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ThirteenLeafClover.java#L53) **`alterHeroDamageChance(int level)`**: 개별 처리 / 조건 분기
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ThirteenLeafClover.java#L63) **`alterDamageRoll(int min, int max)`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Float

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 587. [`TrapMechanism.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 135행 / 타입 1개 / 필드 3개 / 메서드 9개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L33) `class TrapMechanism  extends Trinket`

### 변수·상수 (단일 행 선언)

- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L81) `int shuffles` 초기식: `0`
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L106) `String FEELS` 초기식: `"feels"`
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L107) `String SHUFFLES` 초기식: `"shuffles"`

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L40) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L46) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, overrideNormalLevelChance, buffedLvl, revealHiddenTrapChance
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L54) **`overrideNormalLevelChance()`**: 개별 처리 / 참조 호출: overrideNormalLevelChance, trinketLevel
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L58) **`overrideNormalLevelChance(int level)`**: 개별 처리 / 조건 분기
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L66) **`revealHiddenTrapChance()`**: 개별 처리 / 참조 호출: revealHiddenTrapChance, trinketLevel
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L70) **`revealHiddenTrapChance(int level)`**: 개별 처리 / 조건 분기
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L83) **`getNextFeeling()`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: hero.belongings.getItem, mech.levelFeels.isEmpty, Random.pushGenerator, mech.levelFeels.add, Random.shuffle, Random.popGenerator, mech.levelFeels.remove
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L110) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: super.storeInBundle, levelFeels.isEmpty, levelFeels.size, levelFeels.get, bundle.put
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java#L123) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: super.restoreFromBundle, levelFeels.clear, bundle.contains, bundle.getBooleanArray, levelFeels.add, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 588. [`Trinket.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 138행 / 타입 3개 / 필드 0개 / 메서드 15개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L33) `class Trinket  extends Item`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L81) `class PlaceHolder  extends Trinket`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L109) `class UpgradeTrinket  extends Recipe`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L42) **`isUpgradable()`**: 조건 판정
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L46) **`upgradeEnergyCost()`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L48) **`trinketLevel(Class<? extends Trinket> trinketType)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.getItem, trinket.buffedLvl
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L63) **`info()`**: 개별 처리 / 참조 호출: super.info, statsDesc
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L69) **`statsDesc()`**: 개별 처리
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L71) **`energyVal()`**: 개별 처리
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L76) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L88) **`upgradeEnergyCost()`**: 개별 처리
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L93) **`isSimilar(Item item)`**: 조건 판정
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L98) **`info()`**: 개별 처리
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L103) **`statsDesc()`**: 개별 처리
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L112) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: ingredients.size, ingredients.get, level
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L117) **`cost(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: ingredients.get, upgradeEnergyCost
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L122) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: ingredients.get, duplicate, quantity, result.upgrade, Catalog.countUse, result.getClass
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java#L133) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: ingredients.get, duplicate, upgrade

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 589. [`TrinketCatalyst.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 266행 / 타입 5개 / 필드 6개 / 메서드 16개.

### 타입·상속 선언

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L55) `class TrinketCatalyst  extends Item`
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L110) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe`
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L146) `class RandomTrinket  extends Item`
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L154) `class WndTrinket  extends Window`
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L203) `class RewardWindow  extends WndInfoItem`

### 변수·상수 (단일 행 선언)

- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L91) `String ROLLED_TRINKETS` 초기식: `"rolled_trinkets"`
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L156) `int WIDTH` 초기식: `120`
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L157) `int BTN_SIZE` 초기식: `24`
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L158) `int BTN_GAP` 초기식: `4`
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L159) `int GAP` 초기식: `2`
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L161) `int NUM_TRINKETS` 초기식: `4`

### 함수·메서드 역할과 내부 연결

- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L64) **`isIdentified()`**: 조건 판정
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L69) **`isUpgradable()`**: 조건 판정
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L74) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doPickUp, Document.ADVENTURERS_GUIDE.isPageRead, GameScene.flashForDocument
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L87) **`hasRolledTrinkets()`**: 조건 판정 / 참조 호출: rolledTrinkets.isEmpty
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L94) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, rolledTrinkets.isEmpty, bundle.put
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L102) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, rolledTrinkets.clear, bundle.contains, rolledTrinkets.addAll, bundle.getCollection
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L113) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: ingredients.size, ingredients.get
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L118) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L123) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 예외 처리 / 참조 호출: ingredients.get, duplicate, newCata.collect, quantity, ShatteredPixelDungeon.scene, addToFront, WndTrinket, Dungeon.saveAll, RuntimeException
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L141) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: Trinket.PlaceHolder
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L163) **`WndTrinket(TrinketCatalyst cata)`**: 개별 처리 / 반복 / 참조 호출: IconTitle, titlebar.icon, ItemSprite, titlebar.label, Messages.titleCase, Messages.get, titlebar.setRect, add, PixelScene.renderTextBlock
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L184) **`onClick()`**: 이벤트·효과 실행 / 참조 호출: ShatteredPixelDungeon.scene, addToFront, RewardWindow, item
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L199) **`onBackPressed()`**: 이벤트·효과 실행
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L205) **`RewardWindow(Item item)`**: 개별 처리 / 조건 분기·예외 처리 / 참조 호출: RedButton, Messages.get, onClick, RewardWindow.this.hide, WndTrinket.this.hide, Generator.random, hero.belongings.getItem, cata.detach, Catalog.countUse
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L210) **`onClick()`**: 이벤트·효과 실행 / 조건 분기·예외 처리 / 참조 호출: RewardWindow.this.hide, WndTrinket.this.hide, Generator.random, hero.belongings.getItem, cata.detach, Catalog.countUse, cata.getClass, result.identify, ShatteredPixelDungeon.scene
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java#L253) **`onClick()`**: 이벤트·효과 실행 / 참조 호출: hide

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 590. [`VialOfBlood.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/VialOfBlood.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 98행 / 타입 1개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/VialOfBlood.java#L28) `class VialOfBlood  extends Trinket`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/VialOfBlood.java#L35) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/VialOfBlood.java#L41) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, totalHealMultiplier, buffedLvl, Integer.toString, maxHealPerTurn
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/VialOfBlood.java#L55) **`delayBurstHealing()`**: 개별 처리 / 참조 호출: trinketLevel
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/VialOfBlood.java#L59) **`bloodVialLevel()`**: 개별 처리 / 참조 호출: trinketLevel
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/VialOfBlood.java#L63) **`totalHealMultiplier()`**: 개별 처리 / 참조 호출: totalHealMultiplier, trinketLevel
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/VialOfBlood.java#L67) **`totalHealMultiplier(int level)`**: 개별 처리 / 조건 분기
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/VialOfBlood.java#L75) **`maxHealPerTurn()`**: 개별 처리 / 참조 호출: maxHealPerTurn, trinketLevel
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/VialOfBlood.java#L79) **`maxHealPerTurn(int level)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Math.round

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 591. [`WondrousResin.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/WondrousResin.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 83행 / 타입 1개 / 필드 1개 / 메서드 6개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/WondrousResin.java#L27) `class WondrousResin  extends Trinket`

### 변수·상수 (단일 행 선언)

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/WondrousResin.java#L53) `boolean forcePositive` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/WondrousResin.java#L34) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/WondrousResin.java#L40) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, positiveCurseEffectChance, buffedLvl, extraCurseEffectChance
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/WondrousResin.java#L55) **`positiveCurseEffectChance()`**: 개별 처리 / 조건 분기 / 참조 호출: positiveCurseEffectChance, trinketLevel
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/WondrousResin.java#L62) **`positiveCurseEffectChance(int level)`**: 개별 처리 / 조건 분기
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/WondrousResin.java#L70) **`extraCurseEffectChance()`**: 개별 처리 / 참조 호출: extraCurseEffectChance, trinketLevel
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/WondrousResin.java#L74) **`extraCurseEffectChance(int level)`**: 개별 처리 / 조건 분기

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":24,"fields":17,"methods":126}

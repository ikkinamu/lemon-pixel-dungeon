# Java 파일별 소스 구현 해설 480–495

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 480. [`PotionOfPurity.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfPurity.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 105행 / 타입 1개 / 필드 2개 / 메서드 3개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfPurity.java#L42) `class PotionOfPurity  extends Potion`

### 변수·상수 (단일 행 선언)

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfPurity.java#L44) `int DISTANCE` 초기식: `3`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfPurity.java#L46) `ArrayList<Class> affectedBlobs`

### 함수·메서드 역할과 내부 연결

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfPurity.java#L55) **`shatter(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: PathFinder.buildDistanceMap, BArray.not, level.blobs.get, blobs.add, Dungeon.level.length, blob.clear, CellEmitter.get, burst, Speck.factory
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfPurity.java#L93) **`apply(Hero hero)`**: 개별 처리 / 참조 호출: GLog.w, Messages.get, Buff.prolong, SpellSprite.show, identify
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfPurity.java#L101) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 481. [`PotionOfStrength.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfStrength.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 65행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfStrength.java#L32) `class PotionOfStrength  extends Potion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfStrength.java#L43) **`apply(Hero hero)`**: 개별 처리 / 참조 호출: identify, hero.sprite.showStatusWithIcon, GLog.p, Messages.get, hero.STR, Badges.validateStrengthAttained, Badges.validateDuelistUnlock
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfStrength.java#L56) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfStrength.java#L61) **`energyVal()`**: 개별 처리 / 참조 호출: isKnown, super.energyVal

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 482. [`PotionOfToxicGas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfToxicGas.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.potions` / 본문 57행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfToxicGas.java#L32) `class PotionOfToxicGas  extends Potion`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfToxicGas.java#L39) **`shatter(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: splash, identify, Sample.INSTANCE.play, GameScene.add, Blob.seed
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfToxicGas.java#L53) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 483. [`CeremonialCandle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.quest` / 본문 203행 / 타입 1개 / 필드 3개 / 메서드 9개.

### 타입·상속 선언

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L48) `class CeremonialCandle  extends Item`

### 변수·상수 (단일 행 선언)

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L51) `int ritualPos`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L95) `boolean aflame` 초기식: `false`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L97) `String AFLAME` 초기식: `"aflame"`

### 함수·메서드 역할과 내부 연결

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L63) **`isUpgradable()`**: 조건 판정
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L68) **`isIdentified()`**: 조건 판정
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L73) **`doDrop(Hero hero)`**: 개별 처리 / 참조 호출: super.doDrop, checkCandles
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L80) **`onThrow(int cell)`**: 이벤트·효과 실행 / 참조 호출: super.onThrow, checkCandles
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L87) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doPickUp
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L100) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L106) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getBoolean
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L112) **`emitter()`**: 개별 처리 / 조건 분기 / 참조 호출: Emitter, emitter.pos, emitter.pour, super.emitter
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CeremonialCandle.java#L123) **`checkCandles()`**: 조건 판정 / 조건 분기·반복 / 참조 호출: room, level.heaps.get, Dungeon.level.width, h.sprite.view, place, h.items.toArray, h.remove, Elemental.NewbornFireElemental, Actor.findChar

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 484. [`CorpseDust.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.quest` / 본문 217행 / 타입 3개 / 필드 3개 / 메서드 14개.

### 타입·상속 선언

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L46) `class CorpseDust  extends Item`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L90) `class DustGhostSpawner  extends Buff`
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L185) `class DustWraith  extends Wraith`

### 변수·상수 (단일 행 선언)

- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L170) `String SPAWNPOWER` 초기식: `"spawnpower"`
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L187) `int atkCount` 초기식: `0`
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L201) `String ATK_COUNT` 초기식: `"atk_count"`

### 함수·메서드 역할과 내부 연결

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L58) **`actions(Hero hero)`**: 시간·상태 갱신
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L63) **`isUpgradable()`**: 조건 판정
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L68) **`isIdentified()`**: 조건 판정
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L73) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doPickUp, GLog.n, Messages.get, Buff.affect
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L83) **`onDetach()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Dungeon.hero.buff, spawner.dispel
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L100) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: belongings.getItem, spend, Math.min, Math.round, Dungeon.level.length, Actor.findChar, Dungeon.level.distance, candidates.add, candidates.isEmpty
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L148) **`dispel()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: detach, level.mobs.toArray, mob.die, Game.runOnRenderThread, Callback, call, Music.INSTANCE.fadeOut, Dungeon.level.playLevelMusic
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L157) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Music.INSTANCE.fadeOut, Callback, call, Dungeon.level.playLevelMusic
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L160) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.playLevelMusic
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L173) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L179) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L190) **`attack(Char enemy, float dmgMulti, float dmgBonus, float accMulti)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attack
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L204) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java#L210) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 485. [`DarkGold.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DarkGold.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.quest` / 본문 46행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DarkGold.java#L27) `class DarkGold  extends Item`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DarkGold.java#L37) **`isUpgradable()`**: 조건 판정
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DarkGold.java#L42) **`isIdentified()`**: 조건 판정

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 486. [`DwarfToken.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DwarfToken.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.quest` / 본문 70행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DwarfToken.java#L31) `class DwarfToken  extends Item`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DwarfToken.java#L41) **`isUpgradable()`**: 조건 판정
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DwarfToken.java#L46) **`isIdentified()`**: 조건 판정
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DwarfToken.java#L51) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: GLog.i, Messages.get, hero.next, super.doPickUp
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DwarfToken.java#L61) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Imp.Quest.isOld, Messages.get, super.desc

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 487. [`Embers.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Embers.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.quest` / 본문 51행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Embers.java#L28) `class Embers  extends Item`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Embers.java#L37) **`isUpgradable()`**: 조건 판정
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Embers.java#L42) **`isIdentified()`**: 조건 판정
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Embers.java#L47) **`glowing()`**: 개별 처리 / 참조 호출: ItemSprite.Glowing

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 488. [`EscapeCrystal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.quest` / 본문 373행 / 타입 1개 / 필드 7개 / 메서드 14개.

### 타입·상속 선언

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L58) `class EscapeCrystal  extends Item`

### 변수·상수 (단일 행 선언)

- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L68) `String AC_USE` 초기식: `"USE"`
- [L295](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L295) `String BELONGINGS` 초기식: `"belongings"`
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L296) `String QUICKSLOTS` 초기식: `"quickslots"`
- [L297](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L297) `String GOLD` 초기식: `"gold"`
- [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L298) `String ENERGY` 초기식: `"energy"`
- [L357](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L357) `Bundle storedItems`
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L359) `String STORED_ITEMS` 초기식: `"stored_items"`

### 함수·메서드 역할과 내부 연결

- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L71) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: actions.add
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L78) **`execute(final Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: super.execute, action.equals, Imp.Quest.isOld, leaveVault, hero.belongings.getItem, Dungeon.level.levelExplorePercent, Math.min, tokens.quantity, room
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L162) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: GameScene.selectItem, WndBag.ItemSelector, textPrompt, Messages.get, itemSelectable, wandClass, item.level, checkSeal, onSelect
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L168) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L173) **`itemSelectable(Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: wandClass, item.level, checkSeal
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L200) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Messages.get, checkSeal, item.quantity, item.duplicate, quantity, GameScene.show, WndOptions, ItemSprite, Messages.titleCase
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L222) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: leaveVault, super.onSelect
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L257) **`leaveVault(Item preserve, int score)`**: 개별 처리 / 조건 분기 / 참조 호출: Sample.INSTANCE.play, Dungeon.hero.live, checkSeal, seal.getGlyph, detachSeal, inscribe, Reflection.newInstance, wandClass, w.identify
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L300) **`storeHeroBelongings(Hero hero)`**: 저장·복원 / 참조 호출: Bundle, hero.belongings.storeInBundle, storedItems.put, Dungeon.quickslot.storePlaceholders, Dungeon.quickslot.reset, updateQuickslot, hero.belongings.clear
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L320) **`restoreHeroBelongings(Hero hero, Item preserve)`**: 저장·복원 / 조건 분기 / 참조 호출: preserve.detachAll, hero.belongings.clear, Dungeon.quickslot.reset, Dungeon.quickslot.restorePlaceholders, storedItems.getBundle, updateQuickslot, hero.belongings.restoreFromBundle, storedItems.getInt, preserve.collect
- [L348](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L348) **`isUpgradable()`**: 조건 판정
- [L353](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L353) **`isIdentified()`**: 조건 판정
- [L362](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L362) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L368](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java#L368) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getBundle

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 489. [`GooBlob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/GooBlob.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.quest` / 본문 54행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/GooBlob.java#L27) `class GooBlob  extends Item`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/GooBlob.java#L35) **`isUpgradable()`**: 조건 판정
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/GooBlob.java#L40) **`isIdentified()`**: 조건 판정
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/GooBlob.java#L45) **`value()`**: 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/GooBlob.java#L50) **`energyVal()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 490. [`ImpStatue.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/ImpStatue.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.quest` / 본문 46행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/ImpStatue.java#L27) `class ImpStatue  extends Item`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/ImpStatue.java#L37) **`isUpgradable()`**: 조건 판정
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/ImpStatue.java#L42) **`isIdentified()`**: 조건 판정

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 491. [`MetalShard.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/MetalShard.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.quest` / 본문 54행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/MetalShard.java#L27) `class MetalShard  extends Item`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/MetalShard.java#L35) **`isUpgradable()`**: 조건 판정
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/MetalShard.java#L40) **`isIdentified()`**: 조건 판정
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/MetalShard.java#L45) **`value()`**: 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/MetalShard.java#L50) **`energyVal()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 492. [`Pickaxe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Pickaxe.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.quest` / 본문 148행 / 타입 1개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Pickaxe.java#L48) `class Pickaxe  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Pickaxe.java#L62) **`STRReq(int lvl)`**: 개별 처리 / 참조 호출: super.STRReq
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Pickaxe.java#L67) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, actions.remove
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Pickaxe.java#L77) **`keptThroughLostInventory()`**: 개별 처리 / 참조 호출: super.keptThroughLostInventory
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Pickaxe.java#L82) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Pickaxe.java#L87) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, hero.isCharmedBy, GLog.w, Messages.get, hero.canAttack, hero.sprite.attack, Callback, call, Char.hasProp
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Pickaxe.java#L108) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Char.hasProp, augment.damageFactor, buffedLvl, beforeAbilityUsed, AttackIndicator.target, hero.attack, enemy.isAlive, Buff.affect, onAbilityKill
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Pickaxe.java#L137) **`abilityInfo()`**: 개별 처리 / 참조 호출: buffedLvl, Messages.get, augment.damageFactor, min, max
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Pickaxe.java#L142) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 493. [`VaultBeacon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/VaultBeacon.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.quest` / 본문 58행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/VaultBeacon.java#L32) `class VaultBeacon  extends Spell`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/VaultBeacon.java#L42) **`onCast(Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: ScrollOfTeleportation.teleportToLocation, Dungeon.level.entrance, hero.spendAndNext, Catalog.countUse, getClass, detach
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/VaultBeacon.java#L50) **`Glowing(0xFFFFFF)`**: 개별 처리
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/VaultBeacon.java#L53) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 494. [`Recipe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 272행 / 타입 3개 / 필드 5개 / 메서드 11개.

### 타입·상속 선언

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L66) `class Recipe`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L77) `class SimpleRecipe  extends Recipe`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L80) `class should  be unique`

### 변수·상수 (단일 행 선언)

- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L80) `Class<?extends Item>[] inputs`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L81) `int[] inQuantity`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L83) `int cost`
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L85) `Class<?extends Item> output`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L86) `int outQuantity`

### 함수·메서드 역할과 내부 연결

- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L68) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L70) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L72) **`brew(ArrayList<Item> ingredients)`**: 개별 처리
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L74) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L90) **`getIngredients()`**: 조회·탐색 / 반복 / 참조 호출: Reflection.newInstance, ingredient.quantity, result.add
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L101) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: inQuantity.clone, ingredient.isIdentified, ingredient.getClass, ingredient.quantity
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L124) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L129) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: testIngredients, inQuantity.clone, ingredient.getClass, ingredient.quantity, sampleOutput
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L153) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 예외 처리 / 참조 호출: Reflection.newInstance, result.quantity, ShatteredPixelDungeon.reportException
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L222) **`findRecipes(ArrayList<Item> ingredients)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: recipe.testIngredients, result.add, ingredients.size
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java#L257) **`usableInRecipe(Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: item.isUpgradable

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 495. [`BowFragment.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/BowFragment.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.remains` / 본문 79행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/BowFragment.java#L39) `class BowFragment  extends RemainsItem`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/BowFragment.java#L46) **`doEffect(Hero hero)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: grassCells.add, Random.shuffle, Level.set, GameScene.updateMap, CellEmitter.get, burst, grassCells.size, grassCells.remove, level.plants.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":20,"fields":20,"methods":87}

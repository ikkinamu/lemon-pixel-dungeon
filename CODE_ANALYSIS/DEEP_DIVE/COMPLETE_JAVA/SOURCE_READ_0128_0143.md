# Java 파일별 소스 구현 해설 128–143

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 128. [`ElementalBlast.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/ElementalBlast.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.mage` / 본문 470행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/ElementalBlast.java#L90) `class ElementalBlast  extends ArmorAbility`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/ElementalBlast.java#L131) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.width, Math.max, Dungeon.level.height, Ballistica, hero.belongings.getItem, wandClass, GLog.w, Messages.get, hero.pointsInTalent
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/ElementalBlast.java#L192) **`pointsInTalent(Talent.ELEMENTAL_POWER)`**: 개별 처리
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/ElementalBlast.java#L202) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: level.blobs.get, GameScene.add, Blob.seed, Level.set, GameScene.updateMap, freeze.clear, fire.clear, Dungeon.level.discover, GameScene.discoverTile
- [L444](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/ElementalBlast.java#L444) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, Game.scene, hero.belongings.getItem, staff.wandClass
- [L461](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/ElementalBlast.java#L461) **`icon()`**: 개별 처리
- [L466](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/ElementalBlast.java#L466) **`talents()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 129. [`WarpBeacon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.mage` / 본문 283행 / 타입 2개 / 필드 3개 / 메서드 10개.

### 타입·상속 선언

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L57) `class WarpBeacon  extends ArmorAbility`
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L231) `class WarpBeaconTracker  extends Buff`

### 변수·상수 (단일 행 선언)

- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L252) `String POS` 초기식: `"pos"`
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L253) `String DEPTH` 초기식: `"depth"`
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L254) `String BRANCH` 초기식: `"branch"`

### 함수·메서드 역할과 내부 연결

- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L64) **`targetingPrompt()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.buff, Dungeon.hero.hasTalent, Messages.get, super.targetingPrompt
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L73) **`targetedPos(Char user, int dst)`**: 개별 처리
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L78) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: hero.buff, GameScene.show, WndOptions, Image, Messages.titleCase, name, Messages.get, onSelect, hero.hasTalent
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L84) **`buff(WarpBeaconTracker.class)`**: 개별 처리
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L95) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: hero.hasTalent, GLog.w, Messages.get, chargeUse, Dungeon.hero.pointsInTalent, armor.updateQuickslot, Actor.findChar, hero.shielding, hero.pointsInTalent
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L244) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: CellEmitter.center, e.pour
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L257) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L265) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L274) **`icon()`**: 개별 처리
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java#L279) **`talents()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 130. [`WildMagic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.mage` / 본문 269행 / 타입 2개 / 필드 0개 / 메서드 13개.

### 타입·상속 선언

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L49) `class WildMagic  extends ArmorAbility`
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L133) `class WildMagicTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L56) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L61) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: GLog.w, Messages.get, hero.belongings.getAllItems, Random.shuffle, Math.pow, hero.pointsInTalent, wands.toArray, wands.remove, Dungeon.hero.pointsInTalent
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L137) **`zapWand(ArrayList<Wand> wands, Hero hero, int cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: wands.remove, Ballistica, cur.collisionProperties, hero.sprite.zap, cur.tryToZap, cur.fx, Callback, call, cur.onZap
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L149) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: cur.onZap, Random.Float, WondrousResin.extraCurseEffectChance, sprite.parent.add, Delayer, onComplete, CursedWand.cursedZap, Ballistica, Callback
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L155) **`onComplete()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: CursedWand.cursedZap, Ballistica, Callback, call, afterZap
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L163) **`call()`**: 개별 처리 / 참조 호출: afterZap
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L181) **`call()`**: 개별 처리 / 참조 호출: afterZap
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L199) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: sprite.parent.add, Delayer, onComplete, afterZap
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L203) **`onComplete()`**: 이벤트·효과 실행 / 참조 호출: afterZap
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L218) **`afterZap(Wand cur, ArrayList<Wand> wands, Hero hero, int target)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.pow, hero.pointsInTalent, wildMagicActor.next, Actor.findChar, wands.isEmpty, hero.isAlive, Actor.add, Actor, act
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L237) **`act()`**: 시간·상태 갱신 / 참조 호출: zapWand, Actor.remove
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L260) **`icon()`**: 개별 처리
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java#L265) **`talents()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 131. [`Ratmogrify.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities` / 본문 342행 / 타입 2개 / 필드 6개 / 메서드 19개.

### 타입·상속 선언

- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L59) `class Ratmogrify  extends ArmorAbility`
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L191) `class TransmogRat  extends Mob`

### 변수·상수 (단일 행 선언)

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L66) `boolean useRatroicEnergy` 초기식: `false`
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L200) `Mob original`
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L201) `boolean allied`
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L233) `float timeLeft` 초기식: `6f`
- [L319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L319) `String ORIGINAL` 초기식: `"original"`
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L320) `String ALLIED` 초기식: `"allied"`

### 함수·메서드 역할과 내부 연결

- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L69) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L74) **`targetedPos(Char user, int dst)`**: 개별 처리
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L79) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Actor.findChar, GLog.w, Messages.get, hero.hasTalent, spawnPoints.add, hero.pointsInTalent, spawnPoints.size, Random.index, Rat
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L182) **`icon()`**: 개별 처리
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L187) **`talents()`**: 개별 처리
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L203) **`setup(Mob original)`**: 생성·초기화 / 조건 분기 / 참조 호출: original.clearTime
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L225) **`getOriginal()`**: 조회·탐색 / 조건 분기
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L236) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: getOriginal, GameScene.add, destroy, sprite.killAndErase, CellEmitter.get, burst, Speck.factory, Sample.INSTANCE.play, super.act
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L254) **`spend(float time)`**: 개별 처리 / 조건 분기 / 참조 호출: super.spend
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L259) **`makeAlly()`**: 개별 처리 / 조건 분기 / 참조 호출: AllyBuff.affectAndLoot
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L270) **`attackSkill(Char target)`**: 전투 관련 / 참조 호출: original.attackSkill
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L274) **`drRoll()`**: 개별 처리 / 참조 호출: original.drRoll
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L279) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: original.damageRoll, Dungeon.hero.hasTalent, Math.pow, Dungeon.hero.pointsInTalent
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L288) **`attackDelay()`**: 전투 관련 / 참조 호출: original.attackDelay
- [L293](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L293) **`rollToDropLoot()`**: 개별 처리 / 참조 호출: original.rollToDropLoot
- [L299](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L299) **`destroy()`**: 개별 처리 / 조건 분기 / 참조 호출: super.destroy, Bestiary.setSeen, original.getClass, Bestiary.countEncounter, Notes.remove, original.landmark
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L311) **`name()`**: 개별 처리 / 참조 호출: Messages.get, original.name
- [L323](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L323) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L330](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java#L330) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.get, bundle.getBoolean

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 132. [`DeathMark.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.rogue` / 본문 243행 / 타입 3개 / 필드 2개 / 메서드 16개.

### 타입·상속 선언

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L49) `class DeathMark  extends ArmorAbility`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L137) `class DoubleMarkTracker  extends FlavourBuff`
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L149) `class DeathMarkTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L151) `float DURATION` 초기식: `5f`
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L227) `String INITIAL_HP` 초기식: `"initial_hp"`

### 함수·메서드 역할과 내부 연결

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L56) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L61) **`targetedPos(Char user, int dst)`**: 개별 처리
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L66) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: super.chargeUse, hero.buff, Math.pow, hero.pointsInTalent
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L76) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Actor.findChar, GLog.w, Messages.get, Buff.affect, setInitialHP, chargeUse, armor.updateQuickslot, hero.sprite.zap, hero.next
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L109) **`processFearTheReaper(Char ch)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: ch.buff, Dungeon.hero.hasTalent, Dungeon.hero.pointsInTalent, Buff.prolong, Dungeon.hero.id, BArray.not, PathFinder.buildDistanceMap, Actor.chars
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L140) **`icon()`**: 개별 처리
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L145) **`talents()`**: 개별 처리
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L161) **`icon()`**: 개별 처리
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L166) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L171) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L175) **`setInitialHP(int hp)`**: 상태 갱신 / 조건 분기
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L182) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L192) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: super.detach, target.isAlive, target.sprite.flash, target.sprite.bloodBurstA, target.sprite.center, Sample.INSTANCE.play, target.die, Math.round, Dungeon.hero.pointsInTalent
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L210) **`detachOnDeath()`**: 개별 처리 / 조건 분기 / 참조 호출: super.detach, target.isAlive, target.sprite.flash, target.sprite.bloodBurstA, target.sprite.center, Sample.INSTANCE.play, Math.round, Dungeon.hero.pointsInTalent, hero.sprite.showStatusWithIcon
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L230) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java#L236) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 133. [`ShadowClone.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.rogue` / 본문 415행 / 타입 3개 / 필드 2개 / 메서드 31개.

### 타입·상속 선언

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L57) `class ShadowClone  extends ArmorAbility`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L144) `class ShadowAlly  extends DirectableAlly`
- [L345](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L345) `class ShadowSprite  extends MobSprite`

### 변수·상수 (단일 행 선언)

- [L330](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L330) `String DEF_SKILL` 초기식: `"def_skill"`
- [L347](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L347) `Emitter smoke`

### 함수·메서드 역할과 내부 연결

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L60) **`targetingPrompt()`**: 개별 처리 / 조건 분기 / 참조 호출: getShadowAlly, super.targetingPrompt, Messages.get
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L69) **`useTargeting()`**: 이벤트·효과 실행
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L78) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: getShadowAlly, super.chargeUse
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L87) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: getShadowAlly, ally.directTocell, Actor.findChar, spawnPoints.add, spawnPoints.isEmpty, chargeUse, armor.updateQuickslot, ShadowAlly, Random.element
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L126) **`icon()`**: 개별 처리
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L131) **`talents()`**: 개별 처리
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L135) **`getShadowAlly()`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: Actor.chars
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L156) **`ShadowAlly()`**: 개별 처리
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L160) **`ShadowAlly(int heroLevel)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, Dungeon.hero.pointsInTalent
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L172) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.act, sprite.looping, sprite.idle
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L183) **`defendPos(int cell)`**: 개별 처리 / 참조 호출: GLog.i, Messages.get, super.defendPos
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L189) **`followHero()`**: 개별 처리 / 참조 호출: GLog.i, Messages.get, super.followHero
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L195) **`targetChar(Char ch)`**: 개별 처리 / 참조 호출: GLog.i, Messages.get, super.targetChar
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L201) **`attackSkill(Char target)`**: 전투 관련
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L206) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: Random.NormalIntRange, Dungeon.hero.damageRoll, Dungeon.hero.attackDelay, Math.round, Dungeon.hero.pointsInTalent
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L218) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, Random.Int, Dungeon.hero.pointsInTalent, hero.belongings.weapon, proc
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L229) **`drRoll()`**: 개별 처리 / 조건 분기 / 참조 호출: super.drRoll, Dungeon.hero.drRoll, Math.round, Dungeon.hero.pointsInTalent
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L240) **`glyphLevel(Class<? extends Armor.Glyph> cls)`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int, Dungeon.hero.pointsInTalent, Math.max, super.glyphLevel, Dungeon.hero.glyphLevel
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L249) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.defenseProc, Random.Int, Dungeon.hero.pointsInTalent, hero.belongings.armor, proc
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L260) **`speed()`**: 개별 처리 / 조건 분기 / 참조 호출: super.speed, Dungeon.level.distance
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L274) **`canInteract(Char c)`**: 조건 판정 / 조건 분기 / 참조 호출: super.canInteract, Dungeon.level.distance, Dungeon.hero.pointsInTalent
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L285) **`interact(Char c)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.hasTalent, super.interact, properties, contains, c.properties, PathFinder.buildDistanceMap, BArray.or, appear, Dungeon.observe
- [L314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L314) **`appear(Char ch, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: ch.sprite.interruptMotion, Sample.INSTANCE.play, ch.move, ch.sprite.place, ch.sprite.emitter, burst
- [L333](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L333) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L339](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L339) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L349](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L349) **`ShadowSprite()`**: 개별 처리 / 참조 호출: texture, HeroClass.ROGUE.spritesheet, TextureFilm, HeroSprite.tiers, Animation, idle.frames, run.frames, die.frames, attack.frames
- [L373](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L373) **`onComplete(Tweener tweener)`**: 이벤트·효과 실행 / 참조 호출: super.onComplete
- [L378](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L378) **`resetColor()`**: 생성·초기화 / 참조 호출: super.resetColor, alpha, brightness
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L385) **`link(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: super.link, emitter, smoke.pour
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L396) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update
- [L406](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java#L406) **`kill()`**: 개별 처리 / 조건 분기 / 참조 호출: super.kill

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 134. [`SmokeBomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.rogue` / 본문 236행 / 타입 3개 / 필드 0개 / 메서드 10개.

### 타입·상속 선언

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L60) `class SmokeBomb  extends ArmorAbility`
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L165) `class NinjaLog  extends NPC`
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L201) `class NinjaLogSprite  extends MobSprite`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L67) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L72) **`useTargeting()`**: 이벤트·효과 실행
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L77) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.hasTalent, super.chargeUse, Math.pow, hero.pointsInTalent
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L87) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: PixelScene.shake, PathFinder.buildDistanceMap, BArray.or, Actor.findChar, GLog.w, Messages.get, chargeUse, Item.updateQuickslot, hero.hasTalent
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L156) **`icon()`**: 개별 처리
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L161) **`talents()`**: 개별 처리
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L181) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange, Dungeon.hero.pointsInTalent
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L203) **`NinjaLogSprite()`**: 개별 처리 / 참조 호출: texture, TextureFilm, Animation, idle.frames, idle.clone, attack.clone, die.frames, play
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L225) **`showAlert()`**: 개별 처리
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java#L230) **`blood()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 135. [`Endure.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.warrior` / 본문 190행 / 타입 2개 / 필드 6개 / 메서드 12개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L45) `class Endure  extends ArmorAbility`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L71) `class EndureTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L77) `boolean enduring` 초기식: `true`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L79) `int damageBonus` 초기식: `0`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L80) `int hitsLeft` 초기식: `0`
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L159) `String ENDURING` 초기식: `"enduring"`
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L160) `String DAMAGE_BONUS` 초기식: `"damage_bonus"`
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L161) `String HITS_LEFT` 초기식: `"hits_left"`

### 함수·메서드 역할과 내부 연결

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L52) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: hero.buff, detach, Buff.prolong, combo.addTime, hero.sprite.operate, chargeUse, armor.updateQuickslot, Invisibility.dispel, hero.spendAndNext
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L83) **`icon()`**: 개별 처리
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L88) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L93) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L98) **`desc()`**: 개별 처리 / 참조 호출: Messages.get
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L102) **`adjustDamageTaken(float damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.hasTalent, Math.pow, Dungeon.hero.pointsInTalent
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L117) **`endEnduring()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.hero.pointsInTalent, Actor.chars, Dungeon.level.distance, target.sprite.centerEmitter, start, Speck.factory, Sample.INSTANCE.play, SpellSprite.show, detach
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L145) **`damageFactor(float damage)`**: 전투 관련 / 조건 분기 / 참조 호출: detach
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L164) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L172) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getBoolean, bundle.getInt
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L181) **`icon()`**: 개별 처리
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java#L186) **`talents()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 136. [`HeroicLeap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/HeroicLeap.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.warrior` / 본문 148행 / 타입 2개 / 필드 1개 / 메서드 6개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/HeroicLeap.java#L45) `class HeroicLeap  extends ArmorAbility`
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/HeroicLeap.java#L136) `class DoubleJumpTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/HeroicLeap.java#L88) `int dest` 초기식: `cell`

### 함수·메서드 역할과 내부 연결

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/HeroicLeap.java#L52) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/HeroicLeap.java#L57) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: super.chargeUse, hero.buff, Math.pow, hero.pointsInTalent
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/HeroicLeap.java#L67) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: PixelScene.shake, Ballistica, Actor.findChar, route.path.get, chargeUse, armor.updateQuickslot, hero.busy, hero.sprite.jump, Callback
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/HeroicLeap.java#L92) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: hero.move, Dungeon.level.occupyCell, Dungeon.observe, GameScene.updateFog, Actor.findChar, hero.hasTalent, Hero.heroDamageIntRange, hero.pointsInTalent, Math.round
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/HeroicLeap.java#L139) **`icon()`**: 개별 처리
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/HeroicLeap.java#L144) **`talents()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 137. [`Shockwave.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Shockwave.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.warrior` / 본문 164행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Shockwave.java#L50) `class Shockwave  extends ArmorAbility`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Shockwave.java#L57) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Shockwave.java#L62) **`targetedPos(Char user, int dst)`**: 개별 처리 / 참조 호출: Ballistica
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Shockwave.java#L67) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: GLog.w, Messages.get, hero.busy, chargeUse, Item.updateQuickslot, Ballistica, hero.pointsInTalent, Math.min, ConeAOE
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Shockwave.java#L110) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.findChar, hero.STR, Hero.heroDamageIntRange, Math.round, hero.pointsInTalent, ch.drRoll, Buff.affect, Random.Int, hero.attackProc
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Shockwave.java#L155) **`icon()`**: 개별 처리
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Shockwave.java#L160) **`talents()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 138. [`Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero` / 본문 483행 / 타입 3개 / 필드 21개 / 메서드 29개.

### 타입·상속 선언

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L50) `class Belongings  implements Iterable<Item>`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L54) `class Backpack  extends Bag`
- [L422](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L422) `class ItemIterator  implements Iterator<Item>`

### 변수·상수 (단일 행 선언)

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L52) `Hero owner`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L73) `Backpack backpack`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L82) `KindOfWeapon weapon` 초기식: `null`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L83) `Armor armor` 초기식: `null`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L84) `Artifact artifact` 초기식: `null`
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L85) `KindofMisc misc` 초기식: `null`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L86) `Ring ring` 초기식: `null`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L89) `KindOfWeapon thrownWeapon` 초기식: `null`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L92) `KindOfWeapon abilityWeapon` 초기식: `null`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L95) `KindOfWeapon secondWep` 초기식: `null`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L109) `boolean lostInvent`
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L168) `String WEAPON` 초기식: `"weapon"`
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L169) `String ARMOR` 초기식: `"armor"`
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L170) `String ARTIFACT` 초기식: `"artifact"`
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L171) `String MISC` 초기식: `"misc"`
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L172) `String RING` 초기식: `"ring"`
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L174) `String SECOND_WEP` 초기식: `"second_wep"`
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L188) `boolean bundleRestoring` 초기식: `false`
- [L424](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L424) `int index` 초기식: `0`
- [L428](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L428) `Item[] equipped` 초기식: `{weapon, armor, artifact, misc, ring, secondWep}`
- [L429](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L429) `int backpackIndex` 초기식: `equipped.length`

### 함수·메서드 역할과 내부 연결

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L58) **`capacity()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.capacity
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L75) **`Belongings(Hero owner)`**: 개별 처리 / 참조 호출: Backpack
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L102) **`attackingWeapon()`**: 전투 관련 / 조건 분기 / 참조 호출: weapon
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L110) **`lostInventory(boolean val)`**: 개별 처리
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L114) **`lostInventory()`**: 개별 처리
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L118) **`weapon()`**: 개별 처리 / 조건 분기 / 참조 호출: lostInventory, weapon.keptThroughLostInventory
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L126) **`armor()`**: 개별 처리 / 조건 분기 / 참조 호출: lostInventory, armor.keptThroughLostInventory
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L134) **`artifact()`**: 개별 처리 / 조건 분기 / 참조 호출: lostInventory, artifact.keptThroughLostInventory
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L142) **`misc()`**: 개별 처리 / 조건 분기 / 참조 호출: lostInventory, misc.keptThroughLostInventory
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L150) **`ring()`**: 개별 처리 / 조건 분기 / 참조 호출: lostInventory, ring.keptThroughLostInventory
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L158) **`secondWep()`**: 개별 처리 / 조건 분기 / 참조 호출: lostInventory, secondWep.keptThroughLostInventory
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L176) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: backpack.storeInBundle, bundle.put
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L190) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: backpack.clear, backpack.restoreFromBundle, bundle.get, weapon, activate, armor, artifact, misc, ring
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L216) **`clear()`**: 상태 갱신 / 참조 호출: backpack.clear
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L225) **`preview(GamesInProgress.Info info, Bundle bundle)`**: 개별 처리 / 조건 분기 / 참조 호출: bundle.contains, bundle.get
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L239) **`getBags()`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: result.add
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L285) **`contains(Item contains)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: lostInventory, item.keptThroughLostInventory
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L300) **`getSimilar(Item similar)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: lostInventory, similar.isSimilar, item.keptThroughLostInventory
- [L315](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L315) **`getAllSimilar(Item similar)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: lostInventory, similar.isSimilar, item.keptThroughLostInventory, result.add
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L332) **`identify()`**: 개별 처리 / 반복 / 참조 호출: item.identify
- [L338](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L338) **`observe()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: weapon, ShardOfOblivion.passiveIDDisabled, setIDReady, identify, Badges.validateItemLevelAquired, secondWep, armor, artifact, misc
- [L395](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L395) **`uncurseEquipped()`**: 개별 처리 / 참조 호출: ScrollOfRemoveCurse.uncurse, armor, weapon, artifact, misc, ring, secondWep
- [L399](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L399) **`randomUnequipped()`**: 개별 처리 / 조건 분기 / 참조 호출: owner.buff, Random.element
- [L405](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L405) **`charge(float charge)`**: 개별 처리 / 반복 / 참조 호출: owner.buffs, charger.gainCharge
- [L418](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L418) **`iterator()`**: 개별 처리 / 참조 호출: ItemIterator
- [L426](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L426) **`iterator()`**: 개별 처리
- [L432](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L432) **`hasNext()`**: 조건 판정 / 조건 분기·반복 / 참조 호출: backpackIterator.hasNext
- [L444](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L444) **`next()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: backpackIterator.next
- [L457](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java#L457) **`remove()`**: 상태 갱신 / 상태 선택 / 참조 호출: backpackIterator.remove

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 139. [`Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero` / 본문 2685행 / 타입 2개 / 필드 36개 / 메서드 89개.

### 타입·상속 선언

- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L197) `class Hero  extends Char`
- [L2681](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2681) `interface Doom`

### 변수·상수 (단일 행 선언)

- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L205) `int MAX_LEVEL` 초기식: `30`
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L207) `int STARTING_STR` 초기식: `10`
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L209) `float TIME_TO_REST` 초기식: `1f`
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L210) `float TIME_TO_SEARCH` 초기식: `2f`
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L211) `float HUNGER_FOR_SEARCH` 초기식: `6f`
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L213) `HeroClass heroClass` 초기식: `HeroClass.ROGUE`
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L214) `HeroSubClass subClass` 초기식: `HeroSubClass.NONE`
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L215) `ArmorAbility armorAbility` 초기식: `null`
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L219) `int attackSkill` 초기식: `10`
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L220) `int defenseSkill` 초기식: `5`
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L222) `boolean ready` 초기식: `false`
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L223) `boolean damageInterrupt` 초기식: `true`
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L224) `HeroAction curAction` 초기식: `null`
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L225) `HeroAction lastAction` 초기식: `null`
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L228) `Char attackTarget`
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L230) `boolean resting` 초기식: `false`
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L232) `Belongings belongings`
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L234) `int STR`
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L236) `float awareness`
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L238) `int lvl` 초기식: `1`
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L239) `int exp` 초기식: `0`
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L241) `int HTBoost` 초기식: `0`
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L243) `ArrayList<Mob> visibleEnemies`
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L294) `String CLASS` 초기식: `"class"`
- [L295](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L295) `String SUBCLASS` 초기식: `"subClass"`
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L296) `String ABILITY` 초기식: `"armorAbility"`
- [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L298) `String ATTACK` 초기식: `"attackSkill"`
- [L299](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L299) `String DEFENSE` 초기식: `"defenseSkill"`
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L300) `String STRENGTH` 초기식: `"STR"`
- [L301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L301) `String LEVEL` 초기식: `"lvl"`
- [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L302) `String EXPERIENCE` 초기식: `"exp"`
- [L303](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L303) `String HTBOOST` 초기식: `"htboost"`
- [L1003](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1003) `boolean canSelfTrample` 초기식: `false`
- [L1112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1112) `boolean waitOrPickup` 초기식: `false`
- [L1806](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1806) `boolean walkingToVisibleTrapInFog` 초기식: `false`
- [L2314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2314) `Berserk berserk`

### 함수·메서드 역할과 내부 연결

- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L249) **`Hero()`**: 개별 처리 / 참조 호출: Belongings
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L260) **`updateHT(boolean boostHP)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: RingOfMight.HTMultiplier, Math.round, buff, boost, Math.max, Math.min
- [L277](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L277) **`STR()`**: 개별 처리 / 조건 분기 / 참조 호출: RingOfMight.strengthBonus, buff, buff.boost, hasTalent, Math.floor, pointsInTalent
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L306) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put, Talent.storeTalentsInBundle, belongings.storeInBundle
- [L329](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L329) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: bundle.getInt, super.restoreFromBundle, bundle.getEnum, bundle.get, Talent.restoreTalentsFromBundle, belongings.restoreFromBundle
- [L351](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L351) **`preview(GamesInProgress.Info info, Bundle bundle)`**: 개별 처리 / 참조 호출: bundle.getInt, bundle.getEnum, Belongings.preview
- [L363](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L363) **`hasTalent(Talent talent)`**: 조건 판정 / 참조 호출: pointsInTalent
- [L367](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L367) **`pointsInTalent(Talent talent)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: tier.keySet, tier.get
- [L376](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L376) **`upgradeTalent(Talent talent)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: tier.keySet, tier.put, tier.get, Talent.onTalentUpgraded
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L385) **`talentPointsSpent(int tier)`**: 개별 처리 / 반복 / 참조 호출: talents.get, values
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L393) **`talentPointsAvailable(int tier)`**: 개별 처리 / 조건 분기 / 참조 호출: talentPointsSpent, bonusTalentPoints
- [L405](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L405) **`bonusTalentPoints(int tier)`**: 개별 처리 / 조건 분기 / 참조 호출: buff, isBoosted
- [L418](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L418) **`className()`**: 개별 처리 / 참조 호출: heroClass.title, subClass.title
- [L423](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L423) **`name()`**: 개별 처리 / 조건 분기 / 참조 호출: buff, getDisguise, title, className
- [L432](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L432) **`hitSound(float pitch)`**: 전투 관련 / 조건 분기 / 참조 호출: RingOfForce.fightingUnarmed, belongings.attackingWeapon, hitSound, RingOfForce.getBuffedBonus, super.hitSound, GameMath.gate, STR
- [L444](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L444) **`blockSound(float pitch)`**: 개별 처리 / 조건 분기 / 참조 호출: belongings.weapon, defenseFactor, Sample.INSTANCE.play, super.blockSound
- [L452](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L452) **`live()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: buffs, b.detach, Buff.affect
- [L460](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L460) **`tier()`**: 개별 처리 / 조건 분기 / 참조 호출: belongings.armor
- [L471](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L471) **`shoot(Char enemy, MissileWeapon wep)`**: 개별 처리 / 조건 분기 / 참조 호출: attack, Invisibility.dispel, Buff.affect, hit, addHit
- [L497](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L497) **`attack(Char enemy, float dmgMulti, float dmgBonus, float accMulti)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attack, belongings.attackingWeapon, buff, detach
- [L511](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L511) **`attackSkill(Char target)`**: 전투 관련 / 조건 분기·상태 선택 / 참조 호출: belongings.attackingWeapon, RingOfAccuracy.accuracyMultiplier, hasTalent, buff, pointsInTalent, freerunning, RingOfForce.fightingUnarmed, Math.max, Math.round
- [L568](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L568) **`defenseSkill(Char enemy)`**: 전투 관련 / 조건 분기 / 참조 호출: buff, canAttack, isCharmedBy, Buff.affect, RingOfEvasion.evasionMultiplier, pointsInTalent, belongings.armor, evasionFactor, hasGlyph
- [L614](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L614) **`defenseVerb()`**: 전투 관련 / 조건 분기 / 참조 호출: buff, getComboCount, pointsInTalent, parry.detach, Messages.get, BuffIndicator.refreshHero, Sample.INSTANCE.play, Random.Float, detach
- [L643](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L643) **`drRoll()`**: 개별 처리 / 조건 분기 / 참조 호출: super.drRoll, belongings.armor, Random.NormalIntRange, DRMin, DRMax, STR, STRReq, belongings.weapon, RingOfForce.fightingUnarmed
- [L669](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L669) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: belongings.attackingWeapon, RingOfForce.fightingUnarmed, wep.damageRoll, RingOfForce.armedDamageBonus, RingOfForce.damageRoll, RingOfForce.unarmedGetsWeaponAugment, augment.damageFactor, buff, emp.detach
- [L705](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L705) **`heroDamageIntRange(int min, int max)`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Float, ThirteenLeafClover.alterHeroDamageChance, ThirteenLeafClover.alterDamageRoll, Random.NormalIntRange
- [L714](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L714) **`speed()`**: 개별 처리 / 조건 분기 / 참조 호출: super.speed, RingOfHaste.speedMultiplier, belongings.armor, speedFactor, buff, sprint, momentum.freerunning, momentum.speedMultiplier, pointsInTalent
- [L744](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L744) **`canSurpriseAttack()`**: 조건 판정 / 조건 분기 / 참조 호출: belongings.attackingWeapon, RingOfForce.fightingUnarmed, STR, STRReq, super.canSurpriseAttack
- [L754](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L754) **`canAttack(Char enemy)`**: 조건 판정 / 조건 분기·반복 / 참조 호출: Actor.chars, contains, Dungeon.level.adjacent, hero.belongings.attackingWeapon, wep.canReach, buff, BArray.not, PathFinder.buildDistanceMap
- [L782](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L782) **`attackDelay()`**: 전투 관련 / 조건 분기 / 참조 호출: buff, detach, RingOfForce.fightingUnarmed, belongings.attackingWeapon, delayFactor, RingOfFuror.attackSpeedMultiplier, RingOfForce.unarmedGetsWeaponAugment, augment.delayFactor
- [L815](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L815) **`spend(float time)`**: 개별 처리 / 참조 호출: super.spend
- [L820](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L820) **`spendConstant(float time)`**: 개별 처리 / 참조 호출: super.spendConstant
- [L824](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L824) **`spendAndNextConstant(float time)`**: 개별 처리 / 참조 호출: busy, spendConstant, next
- [L830](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L830) **`spendAndNext(float time)`**: 개별 처리 / 참조 호출: busy, spend, next
- [L837](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L837) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: buff, endEnduring, Dungeon.observe, Dungeon.level.updateFieldOfView, checkVisibleMobs, BuffIndicator.refreshHero, BuffIndicator.refreshBoss, spendAndNext, spendConstant
- [L933](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L933) **`busy()`**: 개별 처리
- [L937](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L937) **`ready()`**: 개별 처리 / 조건 분기 / 참조 호출: sprite.looping, sprite.idle, AttackIndicator.updateState, GameScene.ready, SPDSettings.vaultInjureWarns, ShatteredPixelDungeon.runOnRenderThread, Callback, call, Messages.get
- [L958](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L958) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, GameScene.show, WndOptions, ImpSprite, Messages.titleCase, onSelect, super.onSelect, onBackPressed
- [L971](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L971) **`onSelect(int index)`**: 이벤트·효과 실행 / 참조 호출: super.onSelect
- [L976](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L976) **`onBackPressed()`**: 이벤트·효과 실행
- [L985](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L985) **`interrupt()`**: 개별 처리 / 조건 분기 / 참조 호출: isAlive, GameScene.resetKeyHold
- [L996](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L996) **`resume()`**: 개별 처리 / 참조 호출: next
- [L1004](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1004) **`canSelfTrample()`**: 조건 판정 / 참조 호출: level.plants.get
- [L1014](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1014) **`actMove(HeroAction.Move action)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: getCloser, canSelfTrample, Dungeon.level.pressCell, spendAndNext, speed, ready
- [L1032](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1032) **`actInteract(HeroAction.Interact action)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: ch.isAlive, ch.canInteract, ready, sprite.turnTo, ch.interact, Char.hasProp, getCloser
- [L1056](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1056) **`actBuy(HeroAction.Buy action)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: ready, level.heaps.get, heap.size, Game.runOnRenderThread, Callback, call, GameScene.show, WndTradeItem, getCloser
- [L1066](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1066) **`call()`**: 개별 처리 / 참조 호출: GameScene.show, WndTradeItem
- [L1084](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1084) **`actAlchemy(HeroAction.Alchemy action)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.level.distance, ready, buff, kit.isCursed, GLog.w, Messages.get, AlchemyScene.clearToolkit, ShatteredPixelDungeon.switchScene, getCloser
- [L1114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1114) **`actPickUp(HeroAction.PickUp action)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: level.heaps.get, heap.peek, item.doPickUp, heap.pickUp, MissileWeapon.UpgradedSetTracker.pickupValid, belongings.getItem, existing.quantity, GLog.p, Messages.get
- [L1195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1195) **`actOpenChest(HeroAction.OpenChest action)`**: 시간·상태 갱신 / 조건 분기·상태 선택 / 참조 호출: Dungeon.level.adjacent, level.heaps.get, Notes.keyCount, GoldenKey, CrystalKey, GLog.w, Messages.get, ready, Sample.INSTANCE.play
- [L1248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1248) **`actUnlock(HeroAction.Unlock action)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, Notes.keyCount, IronKey, belongings.getItem, GLog.i, Messages.get, ready, CrystalKey, WornKey
- [L1312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1312) **`actMine(HeroAction.Mine action)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.adjacent, Dungeon.level.insideMap, sprite.attack, Callback, call, DarkGold, gold.doPickUp, hero.belongings.getItem, existing.quantity
- [L1322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1322) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: DarkGold, gold.doPickUp, hero.belongings.getItem, existing.quantity, GLog.p, Messages.get, GLog.i, spend, Dungeon.level.drop
- [L1387](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1387) **`onComplete()`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Splash.at, Level.set, Sample.INSTANCE.play, GameScene.updateMap, spendAndNext, ready
- [L1429](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1429) **`actTransition(HeroAction.LvlTransition action)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.level.getTransition, PixelScene.shake, ready, transition.inside, Dungeon.level.activateTransition, getCloser
- [L1458](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1458) **`actAttack(HeroAction.Attack action)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: isCharmedBy, GLog.w, Messages.get, ready, attackTarget.isAlive, canAttack, hasTalent, buff, pointsInTalent
- [L1501](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1501) **`attackTarget()`**: 전투 관련
- [L1505](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1505) **`rest(boolean fullRest)`**: 개별 처리 / 조건 분기 / 참조 호출: spendAndNextConstant, hasTalent, buff, Buff.affect, sprite.showStatus, Messages.get
- [L1524](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1524) **`attackProc(final Char enemy, int damage)`**: 전투 관련 / 조건 분기·상태 선택 / 참조 호출: super.attackProc, RingOfForce.fightingUnarmed, RingOfForce.unarmedGetsWeaponEnchantment, belongings.attackingWeapon, Talent.onAttackProc, wep.proc, buff, enchant, proc
- [L1562](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1562) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: enemy.isAlive, hasTalent, Math.min, pointsInTalent, wep.buffedLvl, Buff.prolong, set, enemy.id, Actor.remove
- [L1586](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1586) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: Buff.affect, berserk.damage, belongings.armor, proc, buff, glyph, ClothArmor, Math.round, Armor.Glyph.genericProcChanceMultiplier
- [L1615](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1615) **`glyphLevel(Class<? extends Armor.Glyph> cls)`**: 개별 처리 / 조건 분기 / 참조 호출: belongings.armor, hasGlyph, Math.max, super.glyphLevel, belongings.armor.buffedLvl, buff, glyph, getClass
- [L1628](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1628) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: buff, interrupt, this.buff, Buff.detach, GLog.w, Messages.get, endure.adjustDamageTaken, thorns.proc, pointsInTalent
- [L1715](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1715) **`checkVisibleMobs()`**: 조건 판정 / 조건 분기·반복 / 참조 호출: level.mobs.toArray, m.landmark, Notes.add, visible.add, visibleEnemies.contains, mindVisionEnemies.contains, QuickSlotButton.autoAim, Ballistica, distance
- [L1794](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1794) **`visibleEnemies()`**: 개별 처리 / 참조 호출: visibleEnemies.size
- [L1798](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1798) **`visibleEnemy(int index)`**: 개별 처리 / 참조 호출: visibleEnemies.get, visibleEnemies.size
- [L1802](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1802) **`getVisibleEnemies()`**: 조회·탐색
- [L1808](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1808) **`getCloser(final int target)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: PixelScene.shake, Dungeon.level.adjacent, Actor.findChar, level.traps.get, path.isEmpty, path.getFirst, path.getLast, path.get, Dungeon.level.length
- [L1920](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L1920) **`handle(int cell)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Dungeon.level.length, Dungeon.level.updateFieldOfView, level.traps.get, Actor.findChar, level.heaps.get, HeroAction.Alchemy, Char.hasProp, heroShouldInteract, HeroAction.Interact
- [L2010](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2010) **`earnExp(int exp, Class source)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: maxExp, buff, chains.gainExp, horn.gainCharge, kit.gainCharge, armband.gainCharge, berserk.recover, i.onHeroGainExp, countDown
- [L2110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2110) **`maxExp()`**: 개별 처리 / 참조 호출: maxExp
- [L2114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2114) **`maxExp(int lvl)`**: 개별 처리
- [L2118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2118) **`isStarving()`**: 조건 판정 / 참조 호출: Buff.affect, isStarving
- [L2123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2123) **`add(Buff buff)`**: 상태 갱신 / 조건 분기 / 참조 호출: buff, super.add, buff.heroMessage, GLog.w, interrupt, BuffIndicator.refreshHero
- [L2150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2150) **`remove(Buff buff)`**: 상태 갱신 / 조건 분기 / 참조 호출: super.remove, BuffIndicator.refreshHero
- [L2159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2159) **`onRemove()`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: buffs, Actor.remove, buff.detach
- [L2171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2171) **`die(Object cause)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: belongings.getAllItems, i.isBlessed, interrupt, ankh.isBlessed, PotionOfHealing.cure, Buff.prolong, SpellSprite.show, GameScene.flash, Sample.INSTANCE.play
- [L2218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2218) **`call()`**: 개별 처리 / 참조 호출: GameScene.show, WndResurrect
- [L2241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2241) **`reallyDie(Object cause)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.length, Dungeon.level.discover, Bones.leave, Dungeon.observe, GameScene.updateFog, hero.belongings.identify, level.heaps.get, passable.add, Collections.shuffle
- [L2298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2298) **`call()`**: 개별 처리 / 참조 호출: GameScene.gameOver, Sample.INSTANCE.play
- [L2317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2317) **`isAlive()`**: 조건 판정 / 조건 분기 / 참조 호출: buff, berserk.berserking, super.isAlive
- [L2329](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2329) **`move(int step, boolean travelling)`**: 개별 처리 / 조건 분기 / 참조 호출: super.move, Sample.INSTANCE.play, Random.Float
- [L2354](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2354) **`onAttackComplete()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onAttackComplete, AttackIndicator.target, attack, Invisibility.dispel, spend, attackDelay, Buff.affect, hit, addHit
- [L2386](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2386) **`onMotionComplete()`**: 이벤트·효과 실행 / 참조 호출: GameScene.checkKeyHold
- [L2391](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2391) **`onOperateComplete()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: buff, skele.isCursed, Random.Int, GLog.n, Messages.get, spendAndNext, Buff.affect, affectHunger, Dungeon.level.distance
- [L2490](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2490) **`search(boolean intentional)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: isAlive, pointsInTalent, hasTalent, buff, Dungeon.level.cellToPoint, talisman.isCursed, Math.max, Math.min, Dungeon.level.height
- [L2641](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2641) **`resurrect()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: live, belongings.getItem, Buff.affect, i.isEquipped, activate, i.keptThroughLostInventory, hasTalent, holster.contains, charge
- [L2676](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2676) **`next()`**: 개별 처리 / 조건 분기 / 참조 호출: isAlive, super.next
- [L2682](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L2682) **`onDeath()`**: 이벤트·효과 실행

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 140. [`HeroAction.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero` / 본문 92행 / 타입 11개 / 필드 3개 / 메서드 10개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L26) `class HeroAction`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L30) `class Move  extends HeroAction`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L36) `class PickUp  extends HeroAction`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L42) `class OpenChest  extends HeroAction`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L48) `class Buy  extends HeroAction`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L54) `class Interact  extends HeroAction`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L61) `class Unlock  extends HeroAction`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L67) `class LvlTransition  extends HeroAction`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L73) `class Mine  extends HeroAction`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L79) `class Alchemy  extends HeroAction`
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L85) `class Attack  extends HeroAction`

### 변수·상수 (단일 행 선언)

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L28) `int dst`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L55) `Char ch`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L86) `Char target`

### 함수·메서드 역할과 내부 연결

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L31) **`Move(int dst)`**: 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L37) **`PickUp(int dst)`**: 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L43) **`OpenChest(int dst)`**: 개별 처리
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L49) **`Buy(int dst)`**: 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L56) **`Interact(Char ch)`**: 개별 처리
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L62) **`Unlock(int door)`**: 개별 처리
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L68) **`LvlTransition(int stairs)`**: 개별 처리
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L74) **`Mine(int wall)`**: 개별 처리
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L80) **`Alchemy(int pot)`**: 개별 처리
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java#L87) **`Attack(Char target)`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 141. [`HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero` / 본문 355행 / 타입 1개 / 필드 1개 / 메서드 17개.

### 타입·상속 선언

- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L85) `enum HeroClass`

### 변수·상수 (단일 행 선언)

- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L94) `HeroSubClass[] subClasses`

### 함수·메서드 역할과 내부 연결

- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L100) **`initHero(Hero hero)`**: 생성·초기화 / 조건 분기·반복·상태 선택 / 참조 호출: Talent.initClassTalents, ClothArmor, identify, Challenges.isItemBlocked, Food, i.collect, VelvetPouch, collect, LimitedDrops.VELVET_POUCH.drop
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L156) **`masteryBadge()`**: 개별 처리 / 상태 선택
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L174) **`initWarrior(Hero hero)`**: 생성·초기화 / 조건 분기 / 참조 호출: WornShortsword, identify, ThrowingStone, stones.identify, collect, Dungeon.quickslot.setSlot, belongings.armor.affixSeal, BrokenSeal, Catalog.setSeen
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L190) **`initMage(Hero hero)`**: 생성·초기화 / 참조 호출: MagesStaff, WandOfMagicMissile, identify, belongings.weapon.activate, Dungeon.quickslot.setSlot, ScrollOfUpgrade, PotionOfLiquidFlame
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L204) **`initRogue(Hero hero)`**: 생성·초기화 / 참조 호출: Dagger, identify, CloakOfShadows, belongings.artifact.activate, ThrowingKnife, knives.identify, collect, Dungeon.quickslot.setSlot, ScrollOfMagicMapping
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L221) **`initHuntress(Hero hero)`**: 생성·초기화 / 참조 호출: Gloves, identify, SpiritBow, bow.identify, collect, Dungeon.quickslot.setSlot, PotionOfMindVision, ScrollOfLullaby
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L233) **`initDuelist(Hero hero)`**: 생성·초기화 / 참조 호출: Rapier, identify, belongings.weapon.activate, ThrowingSpike, spikes.quantity, collect, Dungeon.quickslot.setSlot, PotionOfStrength, ScrollOfMirrorImage
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L248) **`initCleric(Hero hero)`**: 생성·초기화 / 참조 호출: Cudgel, identify, belongings.weapon.activate, HolyTome, belongings.artifact.activate, Dungeon.quickslot.setSlot, PotionOfPurity, ScrollOfRemoveCurse
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L263) **`title()`**: 개별 처리 / 참조 호출: Messages.get, name
- [L267](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L267) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, name
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L271) **`shortDesc()`**: 개별 처리 / 참조 호출: Messages.get, name
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L275) **`subClasses()`**: 개별 처리
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L279) **`armorAbilities()`**: 개별 처리 / 상태 선택 / 참조 호출: HeroicLeap, Shockwave, Endure, ElementalBlast, WildMagic, WarpBeacon, SmokeBomb, DeathMark, ShadowClone
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L296) **`spritesheet()`**: 개별 처리 / 상태 선택
- [L313](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L313) **`splashArt()`**: 개별 처리 / 상태 선택
- [L330](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L330) **`isUnlocked()`**: 조건 판정 / 조건 분기·상태 선택 / 참조 호출: DeviceCompat.isDebug, Badges.isUnlocked
- [L350](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java#L350) **`unlockMsg()`**: 개별 처리 / 참조 호출: shortDesc, Messages.get, name

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 142. [`HeroSubClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero` / 본문 89행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java#L31) `enum HeroSubClass`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java#L59) **`title()`**: 개별 처리 / 참조 호출: Messages.get, name
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java#L63) **`shortDesc()`**: 개별 처리 / 참조 호출: Messages.get, name
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java#L67) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, name, Game.scene, hero.belongings.getItem, staff.wandClass, desc.replaceAll
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java#L84) **`icon()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 143. [`AuraOfProtection.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 114행 / 타입 2개 / 필드 2개 / 메서드 9개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L38) `class AuraOfProtection  extends ClericSpell`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L79) `class AuraBuff  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L81) `float DURATION` 초기식: `20f`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L83) `Emitter particles`

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L40) **`AuraOfProtection()`**: 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L43) **`icon()`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L48) **`desc()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent, Messages.get, chargeUse
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L55) **`chargeUse(Hero hero)`**: 개별 처리
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L60) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L65) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 참조 호출: Buff.affect, Sample.INSTANCE.play, hero.spend, hero.busy, hero.sprite.operate, onSpellCast
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L90) **`icon()`**: 개별 처리
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L95) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.emitter, particles.pos, particles.pour, Speck.factory
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java#L107) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":41,"fields":83,"methods":287}

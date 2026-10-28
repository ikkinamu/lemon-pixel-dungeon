# Java 파일별 소스 구현 해설 16–31

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 16. [`Inferno.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Inferno.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 99행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Inferno.java#L30) `class Inferno  extends Blob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Inferno.java#L33) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: super.evolve, level.blobs.get, Dungeon.level.width, fire.clear, freeze.clear, bliz.clear, Fire.burn, Dungeon.level.destroy, GameScene.updateMap
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Inferno.java#L87) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour, Speck.factory
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Inferno.java#L94) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 17. [`ParalyticGas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ParalyticGas.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 70행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ParalyticGas.java#L33) `class ParalyticGas  extends Blob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ParalyticGas.java#L41) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: super.evolve, Dungeon.level.width, Actor.findChar, ch.isImmune, this.getClass, Buff.prolong
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ParalyticGas.java#L59) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour, Speck.factory
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ParalyticGas.java#L66) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 18. [`Regrowth.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Regrowth.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 82행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Regrowth.java#L35) `class Regrowth  extends Blob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Regrowth.java#L38) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: super.evolve, Dungeon.level.width, Actor.findChar, level.plants.get, Level.set, GameScene.updateMap, ch.isImmune, this.getClass, Buff.prolong
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Regrowth.java#L76) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.start

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 19. [`SacrificialFire.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 233행 / 타입 2개 / 필드 5개 / 메서드 9개.

### 타입·상속 선언

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L52) `class SacrificialFire  extends Blob`
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L216) `class Marked  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L63) `int bonusSpawns` 초기식: `3`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L65) `Item prize`
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L127) `String BONUS_SPAWNS` 초기식: `"bonus_spawns"`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L128) `String PRIZE` 초기식: `"prize"`
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L218) `float DURATION` 초기식: `2f`

### 함수·메서드 역할과 내부 연결

- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L68) **`landmark()`**: 개별 처리
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L73) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.width, Dungeon.level.insideMap, Actor.findChar, ch.buff, CellEmitter.get, burst, Buff.prolong, Dungeon.level.mobCount, Dungeon.level.spawnMob
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L113) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, curEmitter.pour
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L123) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L131) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L138) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.contains, bundle.get
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L144) **`setPrize(Item prize)`**: 상태 갱신
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L148) **`sacrifice(Char ch)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Random.IntRange, Badges.validateDeathFromSacrifice, CellEmitter.get, burst, Sample.INSTANCE.play, GLog.w, Messages.get, clear, Notes.remove
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java#L221) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: target.isAlive, level.blobs.get, fire.sacrifice, super.detach

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 20. [`SmokeScreen.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SmokeScreen.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 42행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SmokeScreen.java#L28) `class SmokeScreen  extends Blob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SmokeScreen.java#L31) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour, Speck.factory
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SmokeScreen.java#L37) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 21. [`StenchGas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/StenchGas.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 80행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/StenchGas.java#L36) `class StenchGas  extends Blob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/StenchGas.java#L39) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: super.evolve, Dungeon.level.width, Actor.findChar, ch.isImmune, this.getClass, ch.buff, Buff.prolong
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/StenchGas.java#L69) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour, Speck.factory
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/StenchGas.java#L76) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 22. [`StormCloud.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/StormCloud.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 73행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/StormCloud.java#L31) `class StormCloud  extends Blob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/StormCloud.java#L34) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: super.evolve, level.blobs.get, Dungeon.level.width, Dungeon.level.setCellToWater, fire.clear, Actor.findChar, ch.isImmune, getClass, Char.hasProp
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/StormCloud.java#L62) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour, Speck.factory
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/StormCloud.java#L68) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 23. [`ToxicGas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 79행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java#L34) `class ToxicGas  extends Blob implements Hero.Doom`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java#L37) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: super.evolve, Dungeon.scalingDepth, Dungeon.level.width, Actor.findChar, ch.isImmune, this.getClass, ch.damage
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java#L59) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour, Speck.factory
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java#L66) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java#L71) **`onDeath()`**: 이벤트·효과 실행 / 참조 호출: Badges.validateDeathFromGas, Dungeon.fail, GLog.n, Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 24. [`VaultFlameTraps.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 186행 / 타입 1개 / 필드 7개 / 메서드 7개.

### 타입·상속 선언

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L46) `class VaultFlameTraps  extends Blob`

### 변수·상수 (단일 행 선언)

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L48) `int[] afterTriggerCooldowns`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L49) `int[] curCooldowns`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L50) `int[] triggersAfterCooldown`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L76) `long SFXLastPlayed` 초기식: `0`
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L149) `String AFTER_TRIGGER_CDS` 초기식: `"after_trigger_cds"`
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L150) `String CUR_COOLDOWNS` 초기식: `"cur_cooldowns"`
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L151) `String TRIGGERS` 초기식: `"triggers"`

### 함수·메서드 역할과 내부 연결

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L55) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: super.act, seed
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L79) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.width, Actor.findChar, ch.isImmune, getClass, Sample.INSTANCE.play, Buff.affect, reignite, level.heaps.get, heap.burn
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L135) **`seed(Level level, int cell, int amount)`**: 개별 처리 / 조건 분기 / 참조 호출: super.seed, level.length, Arrays.fill
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L154) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L164) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, bundle.getIntArray
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L174) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.bound.set, emitter.pour
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/VaultFlameTraps.java#L181) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 25. [`WaterOfAwareness.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfAwareness.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 105행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfAwareness.java#L42) `class WaterOfAwareness  extends WellWater`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfAwareness.java#L45) **`affectHero(Hero hero)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Sample.INSTANCE.play, emitter.parent.add, Identification, hero.sprite.center, hero.belongings.observe, Dungeon.level.length, Dungeon.level.discover, GameScene.discoverTile, Buff.affect
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfAwareness.java#L76) **`affectItem(Item item, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: item.isIdentified, ScrollOfIdentify.IDItem, Sample.INSTANCE.play, emitter.parent.add, Identification, DungeonTilemap.tileCenterToWorld
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfAwareness.java#L90) **`landmark()`**: 개별 처리
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfAwareness.java#L95) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour, Speck.factory
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfAwareness.java#L101) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 26. [`WaterOfHealth.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfHealth.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 117행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfHealth.java#L48) `class WaterOfHealth  extends WellWater`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfHealth.java#L51) **`affectHero(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.isAlive, Sample.INSTANCE.play, PotionOfHealing.cure, hero.belongings.uncurseEquipped, hero.buff, satisfy, VialOfBlood.delayBurstHealing, Buff.affect, healing.setHeal
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfHealth.java#L80) **`affectItem(Item item, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: isFull, fill, CellEmitter.get, start, Speck.factory, Sample.INSTANCE.play, isBlessed, bless, ScrollOfRemoveCurse.uncursable
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfHealth.java#L102) **`landmark()`**: 개별 처리
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfHealth.java#L107) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.start, Speck.factory
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WaterOfHealth.java#L113) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 27. [`Web.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 115행 / 타입 1개 / 필드 0개 / 메서드 9개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java#L34) `class Web  extends Blob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java#L42) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: l.width, cellsToFlagUpdate.add
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java#L62) **`seed(Level level, int cell, int amount)`**: 개별 처리 / 참조 호출: super.seed, level.updateCellFlags
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java#L68) **`affectChar(Char ch)`**: 개별 처리 / 참조 호출: Buff.prolong
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java#L73) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java#L80) **`clear(int cell)`**: 상태 갱신 / 조건 분기 / 참조 호출: super.clear, Dungeon.level.updateCellFlags
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java#L87) **`fullyClear()`**: 개별 처리 / 참조 호출: super.fullyClear, Dungeon.level.buildFlagMaps
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java#L93) **`onBuildFlagMaps(Level l)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: l.length, onUpdateCellFlags
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java#L102) **`onUpdateCellFlags(Level l, int cell)`**: 이벤트·효과 실행 / 조건 분기
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java#L111) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 28. [`WellWater.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WellWater.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.blobs` / 본문 145행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WellWater.java#L35) `class WellWater  extends Blob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WellWater.java#L42) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.width, Dungeon.level.insideMap
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WellWater.java#L56) **`affect(int pos)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: affectHero, clear, level.heaps.get, heap.peek, affectItem, oldItem.quantity, heap.drop, heap.replace, heap.sprite.link
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WellWater.java#L107) **`affectHero(Hero hero)`**: 개별 처리
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WellWater.java#L109) **`affectItem(Item item, int pos)`**: 개별 처리
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WellWater.java#L111) **`affectCell(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: level.blobs.get, water.affect, Level.set, GameScene.updateMap, water.landmark, Notes.remove

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 29. [`Adrenaline.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Adrenaline.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 53행 / 타입 1개 / 필드 1개 / 메서드 3개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Adrenaline.java#L27) `class Adrenaline  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Adrenaline.java#L35) `float DURATION` 초기식: `10f`

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Adrenaline.java#L38) **`icon()`**: 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Adrenaline.java#L43) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Adrenaline.java#L48) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 30. [`AdrenalineSurge.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 107행 / 타입 1개 / 필드 5개 / 메서드 11개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L29) `class AdrenalineSurge  extends Buff`

### 변수·상수 (단일 행 선언)

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L31) `float DURATION` 초기식: `200f`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L37) `int boost`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L38) `float interval`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L90) `String BOOST` 초기식: `"boost"`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L91) `String INTERVAL` 초기식: `"interval"`

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L40) **`reset(int boost, float interval)`**: 생성·초기화 / 참조 호출: spend, cooldown
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L46) **`delay(float value)`**: 개별 처리 / 참조 호출: spend
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L50) **`boost()`**: 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L55) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: spend, detach
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L66) **`icon()`**: 개별 처리
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L71) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L76) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L81) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString, visualcooldown
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L86) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, dispTurns, visualcooldown
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L94) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java#L101) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getFloat

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 31. [`AllyBuff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AllyBuff.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 86행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AllyBuff.java#L37) `class AllyBuff  extends Buff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AllyBuff.java#L44) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, target.buff, detach
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AllyBuff.java#L58) **`affectAndLoot(Mob enemy, Hero hero, Class<?extends AllyBuff> buffCls)`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.affect, enemy.buff, enemy.rollToDropLoot, Badges.validateMonstersSlain, Bestiary.setSeen, enemy.getClass, Bestiary.countEncounter, AscensionChallenge.processEnemyKill, hero.sprite.showStatusWithIcon

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":17,"fields":18,"methods":76}

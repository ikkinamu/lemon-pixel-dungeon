# Java 파일별 소스 구현 해설 384–399

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 384. [`SkeletonKey.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 688행 / 타입 4개 / 필드 5개 / 메서드 35개.

### 타입·상속 선언

- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L64) `class SkeletonKey  extends Artifact`
- [L431](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L431) `class keyRecharge  extends ArtifactBuff`
- [L480](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L480) `class KeyWall  extends Blob`
- [L570](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L570) `class KeyReplacementTracker  extends Buff`

### 변수·상수 (단일 행 선언)

- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L78) `String AC_INSERT` 초기식: `"INSERT"`
- [L572](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L572) `int[] ironKeysNeeded, goldenKeysNeeded, crystalKeysNeeded`
- [L666](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L666) `String IRON_NEEDED` 초기식: `"iron_needed"`
- [L667](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L667) `String GOLDEN_NEEDED` 초기식: `"golden_needed"`
- [L668](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L668) `String CRYSTAL_NEEDED` 초기식: `"crystal_needed"`

### 함수·메서드 역할과 내부 연결

- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L81) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, hero.buff, actions.add
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L92) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, hero.buff, action.equals, isEquipped, GLog.i, Messages.get, GLog.w, GameScene.selectCell
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L115) **`gainExp(int xpGain)`**: 개별 처리 / 조건 분기 / 참조 호출: level, upgrade, GLog.p, Messages.get, Catalog.countUse
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L130) **`Listener()`**: 개별 처리 / 조건 분기 / 참조 호출: onSelect, GLog.w, Messages.get, Dungeon.level.adjacent, GLog.i, Sample.INSTANCE.play, curUser.sprite.operate, Callback, call
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L133) **`onSelect(Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: GLog.w, Messages.get, Dungeon.level.adjacent, GLog.i, Sample.INSTANCE.play, curUser.sprite.operate, Callback, call, Buff.affect
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L159) **`call()`**: 개별 처리 / 참조 호출: Buff.affect, processIronLockOpened, Level.set, GameScene.updateMap, gainExp, Talent.onArtifactUsed, curUser.spendAndNext, curUser.sprite.idle
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L178) **`call()`**: 개별 처리 / 참조 호출: Level.set, GameScene.updateMap, curUser.spendAndNext, curUser.sprite.idle
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L197) **`call()`**: 개별 처리 / 참조 호출: Buff.affect, processCrystalLockOpened, Level.set, GameScene.updateMap, gainExp, Talent.onArtifactUsed, Sample.INSTANCE.play, CellEmitter.get, start
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L260) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Level.set, GameScene.updateMap, gainExp, Talent.onArtifactUsed, curUser.spendAndNext, curUser.sprite.idle, level.heaps.get, candidates.add, candidates.isEmpty
- [L297](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L297) **`call()`**: 개별 처리 / 참조 호출: Buff.affect, processGoldLockOpened, level.heaps.get, open, gainExp, Talent.onArtifactUsed, curUser.spendAndNext, curUser.sprite.idle
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L318) **`call()`**: 개별 처리 / 참조 호출: Buff.affect, processCrystalLockOpened, level.heaps.get, open, gainExp, Talent.onArtifactUsed, curUser.spendAndNext, curUser.sprite.idle
- [L361](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L361) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: placeWall, gainExp, Dungeon.observe, GameScene.updateFog, Sample.INSTANCE.play, Talent.onArtifactUsed, curUser.spendAndNext, curUser.sprite.idle
- [L391](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L391) **`prompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L397](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L397) **`passiveBuff()`**: 개별 처리 / 참조 호출: keyRecharge
- [L402](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L402) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, updateQuickslot
- [L417](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L417) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, isEquipped, Messages.get
- [L433](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L433) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: target.buff, Regeneration.regenOn, RingOfEnergy.artifactChargeMultiplier, updateQuickslot, spend
- [L462](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L462) **`upgrade()`**: 개별 처리 / 참조 호출: level, super.upgrade
- [L467](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L467) **`placeWall(int pos, int knockbackDIR)`**: 개별 처리 / 조건 분기 / 참조 호출: level.blobs.get, GameScene.add, Blob.seed, Actor.findChar, WandOfBlastWave.throwChar, Ballistica, artifactProc, visiblyUpgraded
- [L487](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L487) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: l.width, Math.min, cellsToFlagUpdate.add, Dungeon.observe
- [L519](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L519) **`seed(Level level, int cell, int amount)`**: 개별 처리 / 참조 호출: super.seed, level.updateCellFlags
- [L525](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L525) **`clear(int cell)`**: 상태 갱신 / 조건 분기 / 참조 호출: super.clear, Dungeon.level.updateCellFlags
- [L532](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L532) **`fullyClear()`**: 개별 처리 / 참조 호출: super.fullyClear, Dungeon.level.buildFlagMaps
- [L538](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L538) **`onBuildFlagMaps(Level l)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: l.length, onUpdateCellFlags
- [L547](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L547) **`onUpdateCellFlags(Level l, int cell)`**: 이벤트·효과 실행 / 조건 분기
- [L558](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L558) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour
- [L564](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L564) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get
- [L584](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L584) **`setupKeysForDepth()`**: 생성·초기화 / 조건 분기·반복 / 참조 호출: level.heaps.valueList, Dungeon.level.length
- [L607](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L607) **`clearDepth()`**: 상태 갱신
- [L613](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L613) **`processIronLockOpened()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: setupKeysForDepth, processExcessKeys
- [L621](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L621) **`processGoldLockOpened()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: setupKeysForDepth, processExcessKeys
- [L629](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L629) **`processCrystalLockOpened()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: setupKeysForDepth, processExcessKeys
- [L637](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L637) **`processExcessKeys()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Notes.keyCount, IronKey, Notes.remove, GoldenKey, CrystalKey, GameScene.updateKeyDisplay, GLog.i, Messages.get
- [L671](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L671) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L679](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java#L679) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getIntArray

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 385. [`TalismanOfForesight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 433행 / 타입 4개 / 필드 11개 / 메서드 21개.

### 타입·상속 선언

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L55) `class TalismanOfForesight  extends Artifact`
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L272) `class Foresight  extends ArtifactBuff`
- [L371](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L371) `class CharAwareness  extends FlavourBuff`
- [L398](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L398) `class HeapAwareness  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L70) `String AC_SCRY` 초기식: `"SCRY"`
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L256) `String WARN` 초기식: `"warn"`
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L270) `boolean warn` 초기식: `false`
- [L373](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L373) `int charID`
- [L375](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L375) `String CHAR_ID` 초기식: `"char_id"`
- [L400](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L400) `int pos`
- [L401](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L401) `int depth` 초기식: `Dungeon.depth`
- [L402](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L402) `int branch` 초기식: `Dungeon.branch`
- [L404](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L404) `String POS` 초기식: `"pos"`
- [L405](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L405) `String DEPTH` 초기식: `"depth"`
- [L406](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L406) `String BRANCH` 초기식: `"branch"`

### 함수·메서드 역할과 내부 연결

- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L73) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, hero.buff, actions.add
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L84) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, hero.buff, action.equals, isEquipped, GLog.i, Messages.get, GameScene.selectCell
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L97) **`passiveBuff()`**: 개별 처리 / 참조 호출: Foresight
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L102) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, GLog.p, Messages.get, updateQuickslot
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L120) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, isEquipped, Messages.get
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L135) **`maxDist()`**: 개별 처리 / 참조 호출: Math.min, level
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L139) **`Listener()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: onSelect, Dungeon.level.adjacent, Dungeon.level.trueDistance, maxDist, Ballistica, trajectory.path.size, trajectory.path.get, Math.round, Math.pow
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L142) **`onSelect(Integer target)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Dungeon.level.adjacent, Dungeon.level.trueDistance, maxDist, Ballistica, trajectory.path.size, trajectory.path.get, Math.round, Math.pow, ConeAOE
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L251) **`prompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L259) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L265) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getBoolean
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L275) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: spend, checkAwareness, target.buff, Regeneration.regenOn, level, RingOfEnergy.artifactChargeMultiplier, GLog.p, Messages.get, updateQuickslot
- [L303](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L303) **`checkAwareness()`**: 조건 판정 / 조건 분기·반복 / 참조 호출: Dungeon.level.width, Dungeon.level.height, level.traps.get, target.buff, GLog.w, Messages.get, interrupt
- [L355](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L355) **`charge(int boost)`**: 개별 처리 / 조건 분기 / 참조 호출: target.buff, Math.min, updateQuickslot
- [L363](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L363) **`icon()`**: 개별 처리 / 조건 분기
- [L378](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L378) **`detach()`**: 개별 처리 / 참조 호출: super.detach, Dungeon.observe, GameScene.updateFog
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L385) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L391](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L391) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L409](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L409) **`detach()`**: 개별 처리 / 참조 호출: super.detach, Dungeon.observe, GameScene.updateFog
- [L416](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L416) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L424](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java#L424) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 386. [`TimekeepersHourglass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 547행 / 타입 5개 / 필드 6개 / 메서드 35개.

### 타입·상속 선언

- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L59) `class TimekeepersHourglass  extends Artifact`
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L252) `class hourglassRecharge  extends ArtifactBuff`
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L284) `class timeStasis  extends ArtifactBuff`
- [L351](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L351) `class timeFreeze  extends ArtifactBuff`
- [L501](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L501) `class sandBag  extends Item`

### 변수·상수 (단일 행 선언)

- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L79) `String AC_ACTIVATE` 초기식: `"ACTIVATE"`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L82) `int sandBags` 초기식: `0`
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L222) `String SANDBAGS` 초기식: `"sandbags"`
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L223) `String BUFF` 초기식: `"buff"`
- [L474](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L474) `String PRESSES` 초기식: `"presses"`
- [L475](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L475) `String TURNSTOCOST` 초기식: `"turnsToCost"`

### 함수·메서드 역할과 내부 연결

- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L74) **`resetForTrinity(int visibleLevel)`**: 생성·초기화 / 참조 호출: super.resetForTrinity
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L85) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, hero.buff, actions.add
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L97) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: super.execute, hero.buff, action.equals, isEquipped, GLog.i, Messages.get, activeBuff.detach, GameScene.show, WndOptions
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L121) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: GLog.i, Messages.get, GameScene.flash, Sample.INSTANCE.play, timeStasis, Talent.onArtifactUsed, activeBuff.attachTo, level.mobs.toArray, artifactProc
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L157) **`activate(Char ch)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.activate, activeBuff.attachTo
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L164) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doUnequip, activeBuff.detach
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L176) **`passiveBuff()`**: 개별 처리 / 참조 호출: hourglassRecharge
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L181) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, updateQuickslot
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L196) **`upgrade()`**: 개별 처리 / 반복 / 참조 호출: level, super.upgrade
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L207) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, isEquipped, level, Messages.get
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L226) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L235) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.contains, bundle.getBundle, buffBundle.contains, timeFreeze, timeStasis, activeBuff.restoreFromBundle
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L254) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: target.buff, Regeneration.regenOn, RingOfEnergy.artifactChargeMultiplier, Random.Int, spend, updateQuickslot
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L292) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, Invisibility.dispel, Math.min, spend, Buff.affect, hunger.isStarving, hunger.satisfy, target.next, updateQuickslot
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L327) **`act()`**: 시간·상태 갱신 / 참조 호출: detach
- [L333](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L333) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: super.detach, Dungeon.observe
- [L342](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L342) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.sprite.remove
- [L361](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L361) **`processTime(float time)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: updateQuickslot, detach
- [L379](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L379) **`setDelayedPress(int cell)`**: 상태 갱신 / 조건 분기 / 참조 호출: presses.contains, presses.add
- [L384](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L384) **`triggerPresses()`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Actor.add, Actor, act, level.plants.get, p.trigger, level.traps.get, t.trigger, Actor.remove
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L393) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: level.plants.get, p.trigger, level.traps.get, t.trigger, Actor.remove
- [L410](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L410) **`disarmPresses()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: level.plants.get, Dungeon.level.uproot, level.traps.get, t.disarm
- [L426](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L426) **`detach()`**: 개별 처리 / 참조 호출: updateQuickslot, super.detach, triggerPresses, target.next
- [L435](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L435) **`fx(boolean on)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: level.mobs.toArray, mob.sprite.add, mob.sprite.remove
- [L450](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L450) **`icon()`**: 개별 처리
- [L455](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L455) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L460](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L460) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max
- [L465](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L465) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L470](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L470) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, Messages.decimalFormat, Math.max
- [L478](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L478) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 반복 / 참조 호출: super.storeInBundle, presses.size, presses.get, bundle.put
- [L490](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L490) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 반복 / 참조 호출: super.restoreFromBundle, bundle.getIntArray, presses.add, bundle.getFloat
- [L508](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L508) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: Catalog.setSeen, getClass, Statistics.itemTypesDiscovered.add, hero.belongings.getItem, hourglass.upgrade, Catalog.countUses, hourglass.getClass, Sample.INSTANCE.play, hourglass.level
- [L530](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L530) **`value()`**: 개별 처리
- [L535](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L535) **`isUpgradable()`**: 조건 판정
- [L540](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java#L540) **`isIdentified()`**: 조건 판정

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 387. [`UnstableSpellbook.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 418행 / 타입 3개 / 필드 5개 / 메서드 26개.

### 타입·상속 선언

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L66) `class UnstableSpellbook  extends Artifact`
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L224) `class ExploitHandler  extends Buff`
- [L343](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L343) `class bookRecharge  extends ArtifactBuff`

### 변수·상수 (단일 행 선언)

- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L80) `String AC_READ` 초기식: `"READ"`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L81) `String AC_ADD` 초기식: `"ADD"`
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L162) `Scroll fScroll` 초기식: `scroll`
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L227) `Scroll scroll`
- [L324](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L324) `String SCROLLS` 초기식: `"scrolls"`

### 함수·메서드 역할과 내부 연결

- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L85) **`UnstableSpellbook()`**: 개별 처리 / 참조 호출: setupScrolls
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L91) **`setupScrolls()`**: 생성·초기화 / 반복 / 참조 호출: scrolls.clear, SCROLL.defaultProbsTotal.clone, Random.chances, scrolls.add, scrolls.remove
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L108) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, hero.buff, actions.add, level
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L120) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, hero.buff, action.equals, GLog.w, Messages.get, isEquipped, GLog.i, doReadEffect, GameScene.selectItem
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L141) **`doReadEffect(Hero hero)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Generator.randomUsingDefaults, Random.Int, scroll.anonymize, scrolls.contains, scroll.getClass, Buff.affect, GameScene.show, WndOptions, ItemSprite
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L164) **`affect(hero, ExploitHandler.class)`**: 개별 처리
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L173) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: handler.detach, Reflection.newInstance, ExoticScroll.regToExo.get, fScroll.getClass, scroll.anonymize, checkForArtifactProc, scroll.doRead, Talent.onArtifactUsed, fScroll.doRead
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L193) **`onBackPressed()`**: 이벤트·효과 실행
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L206) **`checkForArtifactProc(Hero user, Scroll scroll)`**: 조건 판정 / 조건 분기·반복 / 참조 호출: level.mobs.toArray, artifactProc, visiblyUpgraded
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L230) **`act()`**: 시간·상태 갱신 / 참조 호출: scroll.anonymize, Game.runOnRenderThread, Callback, call, scroll.doRead, Item.updateQuickslot, detach
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L237) **`call()`**: 개별 처리 / 참조 호출: scroll.doRead, Item.updateQuickslot
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L247) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L253) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.get
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L260) **`passiveBuff()`**: 개별 처리 / 참조 호출: bookRecharge
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L265) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, updateQuickslot
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L280) **`upgrade()`**: 개별 처리 / 반복 / 참조 호출: level, scrolls.isEmpty, scrolls.size, scrolls.remove, super.upgrade
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L292) **`resetForTrinity(int visibleLevel)`**: 생성·초기화 / 반복 / 참조 호출: super.resetForTrinity, setupScrolls, scrolls.isEmpty, scrolls.size, level, scrolls.remove
- [L301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L301) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, isEquipped, Messages.get, level, scrolls.size, scrolls.get
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L327) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put, scrolls.toArray, scrolls.size
- [L333](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L333) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: super.restoreFromBundle, scrolls.clear, bundle.contains, bundle.getClassArray, scrolls.add
- [L345](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L345) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: target.buff, Regeneration.regenOn, RingOfEnergy.artifactChargeMultiplier, updateQuickslot, spend
- [L373](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L373) **`ItemSelector()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: textPrompt, Messages.get, preferredBag, itemSelectable, item.isIdentified, scrolls.contains, item.getClass, onSelect, scrolls.size
- [L376](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L376) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L381](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L381) **`preferredBag()`**: 개별 처리
- [L386](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L386) **`itemSelectable(Item item)`**: 개별 처리 / 참조 호출: item.isIdentified, scrolls.contains, item.getClass
- [L391](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java#L391) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: item.isIdentified, scrolls.size, scrolls.get, equals, item.getClass, hero.sprite.operate, hero.busy, hero.spend, Sample.INSTANCE.play

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 388. [`Bag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bags` / 본문 259행 / 타입 2개 / 필드 7개 / 메서드 19개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L38) `class Bag  extends Item implements Iterable<Item>`
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L216) `class ItemIterator  implements Iterator<Item>`

### 변수·상수 (단일 행 선언)

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L40) `String AC_OPEN` 초기식: `"OPEN"`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L50) `Char owner`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L59) `Item quickUseItem`
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L155) `String ITEMS` 초기식: `"inventory"`
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L164) `boolean loading`
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L218) `int index` 초기식: `0`
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L219) `Iterator<Item> nested` 초기식: `null`

### 함수·메서드 역할과 내부 연결

- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L54) **`capacity()`**: 개별 처리
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L62) **`targetingPos(Hero user, int dst)`**: 개별 처리 / 조건 분기 / 참조 호출: quickUseItem.targetingPos, super.targetingPos
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L71) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, items.isEmpty, GameScene.show, WndQuickBag
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L84) **`collect(Bag container)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: grabItems, Dungeon.quickslot.replacePlaceholder, super.collect, Badges.validateAllBagsBought
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L106) **`onDetach()`**: 이벤트·효과 실행 / 반복 / 참조 호출: Dungeon.quickslot.clearItem, updateQuickslot
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L114) **`grabItems()`**: 개별 처리 / 조건 분기 / 참조 호출: grabItems
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L120) **`grabItems(Bag container)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: container.items.toArray, canHold, Dungeon.quickslot.getSlot, item.detachAll, item.collect, Dungeon.quickslot.setSlot
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L136) **`isUpgradable()`**: 조건 판정
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L141) **`isIdentified()`**: 조건 판정
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L145) **`clear()`**: 상태 갱신 / 참조 호출: items.clear
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L149) **`resurrect()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: items.toArray, items.remove
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L158) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L167) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: super.restoreFromBundle, bundle.getCollection, collect, items.add
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L182) **`contains(Item item)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: contains
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L193) **`canHold(Item item)`**: 조건 판정 / 조건 분기·반복 / 참조 호출: owner.buff, item.keptThroughLostInventory, items.contains, items.size, capacity, item.isSimilar
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L212) **`iterator()`**: 개별 처리 / 참조 호출: ItemIterator
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L222) **`hasNext()`**: 조건 판정 / 조건 분기 / 참조 호출: nested.hasNext, items.size
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L231) **`next()`**: 개별 처리 / 조건 분기 / 참조 호출: nested.hasNext, nested.next, items.get, iterator
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L250) **`remove()`**: 상태 갱신 / 조건 분기 / 참조 호출: nested.remove, items.remove

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 389. [`MagicalHolster.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/MagicalHolster.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bags` / 본문 88행 / 타입 1개 / 필드 2개 / 메서드 5개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/MagicalHolster.java#L30) `class MagicalHolster  extends Bag`

### 변수·상수 (단일 행 선언)

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/MagicalHolster.java#L36) `float HOLSTER_SCALE_FACTOR` 초기식: `0.85f`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/MagicalHolster.java#L37) `float HOLSTER_DURABILITY_FACTOR` 초기식: `1.2f`

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/MagicalHolster.java#L40) **`canHold(Item item)`**: 조건 판정 / 조건 분기 / 참조 호출: super.canHold
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/MagicalHolster.java#L48) **`capacity()`**: 개별 처리
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/MagicalHolster.java#L53) **`collect(Bag container)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.collect, charge
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/MagicalHolster.java#L71) **`onDetach()`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: super.onDetach, stopCharging
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/MagicalHolster.java#L83) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 390. [`PotionBandolier.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/PotionBandolier.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bags` / 본문 55행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/PotionBandolier.java#L30) `class PotionBandolier  extends Bag`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/PotionBandolier.java#L37) **`canHold(Item item)`**: 조건 판정 / 조건 분기 / 참조 호출: super.canHold
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/PotionBandolier.java#L45) **`capacity()`**: 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/PotionBandolier.java#L50) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 391. [`ScrollHolder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/ScrollHolder.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bags` / 본문 70행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/ScrollHolder.java#L33) `class ScrollHolder  extends Bag`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/ScrollHolder.java#L40) **`canHold(Item item)`**: 조건 판정 / 조건 분기 / 참조 호출: super.canHold
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/ScrollHolder.java#L49) **`capacity()`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/ScrollHolder.java#L54) **`onDetach()`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: super.onDetach, Notes.remove
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/ScrollHolder.java#L65) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 392. [`VelvetPouch.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/VelvetPouch.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bags` / 본문 57행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/VelvetPouch.java#L31) `class VelvetPouch  extends Bag`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/VelvetPouch.java#L38) **`canHold(Item item)`**: 조건 판정 / 조건 분기 / 참조 호출: super.canHold
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/VelvetPouch.java#L47) **`capacity()`**: 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/VelvetPouch.java#L52) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 393. [`ArcaneBomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ArcaneBomb.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bombs` / 본문 143행 / 타입 2개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ArcaneBomb.java#L40) `class ArcaneBomb  extends Bomb`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ArcaneBomb.java#L96) `class ArcaneBombFuse  extends Fuse`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ArcaneBomb.java#L47) **`explodesDestructively()`**: 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ArcaneBomb.java#L52) **`explosionRange()`**: 개별 처리
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ArcaneBomb.java#L57) **`createFuse()`**: 생성·초기화 / 참조 호출: ArcaneBombFuse
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ArcaneBomb.java#L62) **`explode(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.explode, PathFinder.buildDistanceMap, BArray.not, explosionRange, CellEmitter.get, burst, Actor.findChar, affected.add, Math.round
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ArcaneBomb.java#L90) **`value()`**: 개별 처리
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ArcaneBomb.java#L102) **`ignite(Bomb bomb)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.ignite, Actor.add, Actor, act, level.heaps.valueList, heap.items.contains, PathFinder.buildDistanceMap, BArray.not, bomb.explosionRange
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ArcaneBomb.java#L107) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: level.heaps.valueList, heap.items.contains, PathFinder.buildDistanceMap, BArray.not, bomb.explosionRange, CellEmitter.get, e.pour, gooWarnEmitters.add, Actor.remove
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ArcaneBomb.java#L134) **`snuff()`**: 개별 처리 / 반복 / 참조 호출: super.snuff, gooWarnEmitters.clear

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 394. [`Bomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bombs` / 본문 450행 / 타입 5개 / 필드 5개 / 메서드 27개.

### 타입·상속 선언

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L66) `class Bomb  extends Item`
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L275) `class ConjuredBomb  extends Bomb`
- [L277](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L277) `class Fuse  extends Actor`
- [L333](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L333) `class DoubleBomb  extends Bomb`
- [L354](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L354) `class EnhanceBomb  extends Recipe`

### 변수·상수 (단일 행 선언)

- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L77) `Fuse fuse`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L80) `boolean lightingFuse` 초기식: `false`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L82) `String AC_LIGHTTHROW` 초기식: `"LIGHTTHROW"`
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L259) `String FUSE` 초기식: `"fuse"`
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L283) `Bomb bomb`

### 함수·메서드 역할과 내부 연결

- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L85) **`isSimilar(Item item)`**: 조건 판정 / 참조 호출: super.isSimilar
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L89) **`explodesDestructively()`**: 개별 처리
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L93) **`explosionRange()`**: 개별 처리
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L98) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L105) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: action.equals, super.execute
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L116) **`createFuse()`**: 생성·초기화 / 참조 호출: Fuse
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L121) **`onThrow(int cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Actor.addDelayed, createFuse, ignite, super.onThrow
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L129) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: GLog.w, Messages.get, fuse.snuff, super.doPickUp
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L138) **`explode(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: fuse.snuff, Sample.INSTANCE.play, explodesDestructively, CellEmitter.center, burst, Dungeon.level.length, BArray.not, BArray.or, PathFinder.buildDistanceMap
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L219) **`isUpgradable()`**: 조건 판정
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L224) **`isIdentified()`**: 조건 판정
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L229) **`random()`**: 개별 처리 / 상태 선택 / 참조 호출: Random.Int, DoubleBomb
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L239) **`glowing()`**: 개별 처리 / 참조 호출: ItemSprite.Glowing
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L244) **`value()`**: 개별 처리
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L249) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.scalingDepth, Messages.get
- [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L262) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L268) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, Actor.add, bundle.get, ignite
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L285) **`ignite(Bomb bomb)`**: 개별 처리
- [L291](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L291) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: snuff, level.heaps.valueList, heap.items.contains, trigger
- [L314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L314) **`trigger(Heap heap)`**: 이벤트·효과 실행 / 참조 호출: heap.remove, Catalog.countUse, bomb.getClass, bomb.explode, snuff
- [L321](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L321) **`freeze()`**: 개별 처리 / 참조 호출: snuff
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L327) **`snuff()`**: 개별 처리 / 참조 호출: Actor.remove
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L341) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: Bomb, bomb.quantity, bomb.doPickUp, SPDSettings.language, hero.sprite.showStatus
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L393) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: i.isIdentified, i.getClass, equals, validIngredients.containsKey
- [L410](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L410) **`cost(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: validIngredients.containsKey, i.getClass, bombCosts.get, validIngredients.get
- [L420](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L420) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: i.quantity, validIngredients.containsKey, i.getClass, Reflection.newInstance, validIngredients.get, Catalog.countUse
- [L440](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java#L440) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: validIngredients.containsKey, i.getClass, Reflection.newInstance, validIngredients.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 395. [`Firebomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Firebomb.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bombs` / 본문 71행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Firebomb.java#L36) `class Firebomb  extends Bomb`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Firebomb.java#L43) **`explosionRange()`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Firebomb.java#L48) **`explode(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.explode, PathFinder.buildDistanceMap, BArray.not, explosionRange, GameScene.add, Blob.seed, CellEmitter.get, burst, Sample.INSTANCE.play
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Firebomb.java#L66) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 396. [`FlashBangBomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/FlashBangBomb.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bombs` / 본문 100행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/FlashBangBomb.java#L47) `class FlashBangBomb  extends Bomb`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/FlashBangBomb.java#L54) **`explosionRange()`**: 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/FlashBangBomb.java#L59) **`explode(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.explode, PathFinder.buildDistanceMap, BArray.not, explosionRange, Actor.findChar, affected.add, Math.round, Random.NormalIntRange, Dungeon.scalingDepth
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/FlashBangBomb.java#L95) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 397. [`FrostBomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/FrostBomb.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bombs` / 본문 68행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/FrostBomb.java#L36) `class FrostBomb  extends Bomb`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/FrostBomb.java#L43) **`explosionRange()`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/FrostBomb.java#L48) **`explode(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.explode, PathFinder.buildDistanceMap, BArray.not, explosionRange, GameScene.add, Blob.seed, Actor.findChar, Buff.affect
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/FrostBomb.java#L63) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 398. [`HolyBomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/HolyBomb.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bombs` / 본문 92행 / 타입 2개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/HolyBomb.java#L39) `class HolyBomb  extends Bomb`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/HolyBomb.java#L84) `class HolyDamage`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/HolyBomb.java#L46) **`explosionRange()`**: 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/HolyBomb.java#L51) **`explode(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.explode, Flare, show, DungeonTilemap.tileCenterToWorld, PathFinder.buildDistanceMap, BArray.not, explosionRange, Actor.findChar, affected.add
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/HolyBomb.java#L87) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 399. [`Noisemaker.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bombs` / 본문 165행 / 타입 2개 / 필드 4개 / 메서드 9개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L36) `class Noisemaker  extends Bomb`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L62) `class NoisemakerFuse  extends Fuse`

### 변수·상수 (단일 행 선언)

- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L64) `boolean triggered` 초기식: `false`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L66) `int left`
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L141) `String LEFT` 초기식: `"left"`
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L142) `String TRIGGERED` 초기식: `"triggered"`

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L43) **`explosionRange()`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L48) **`createFuse()`**: 생성·초기화 / 참조 호출: NoisemakerFuse
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L53) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doPickUp
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L69) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: super.act, level.heaps.valueList, heap.items.contains, trigger, Actor.findChar, heap.items.remove, heap.items.isEmpty, heap.destroy, spend
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L123) **`trigger(Heap heap)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.trigger
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L132) **`freeze()`**: 개별 처리 / 조건 분기 / 참조 호출: super.freeze
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L145) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L152) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getBoolean
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Noisemaker.java#L160) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":36,"fields":45,"methods":207}

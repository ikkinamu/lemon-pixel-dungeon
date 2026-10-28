# Java 파일별 소스 구현 해설 592–607

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 592. [`CursedWand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 1294행 / 타입 34개 / 필드 3개 / 메서드 73개.

### 타입·상속 선언

- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L120) `class CursedWand`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L144) `class CursedEffect`
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L220) `class BurnAndFreeze  extends CursedEffect`
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L237) `class SpawnRegrowth  extends CursedEffect`
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L249) `class RandomTeleport  extends CursedEffect`
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L280) `class RandomGas  extends CursedEffect`
- [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L302) `class RandomAreaEffect  extends CursedEffect`
- [L323](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L323) `class Bubbles  extends CursedEffect`
- [L350](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L350) `class RandomWand  extends CursedEffect`
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L385) `class SelfOoze  extends CursedEffect`
- [L438](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L438) `class RandomPlant  extends CursedEffect`
- [L466](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L466) `class HealthTransfer  extends CursedEffect`
- [L518](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L518) `class Explosion  extends CursedEffect`
- [L527](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L527) `class LightningBolt  extends CursedEffect`
- [L598](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L598) `class Geyser  extends CursedEffect`
- [L610](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L610) `class SummonSheep  extends CursedEffect`
- [L619](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L619) `class Levitate  extends CursedEffect`
- [L638](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L638) `class Alarm  extends CursedEffect`
- [L689](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L689) `class SheepPolymorph  extends CursedEffect`
- [L728](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L728) `class CurseEquipment  extends CursedEffect`
- [L746](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L746) `class InterFloorTeleport  extends CursedEffect`
- [L781](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L781) `class SummonMonsters  extends CursedEffect`
- [L795](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L795) `class FireBall  extends CursedEffect`
- [L835](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L835) `class ConeOfColors  extends CursedEffect`
- [L947](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L947) `class MassInvuln  extends CursedEffect`
- [L972](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L972) `class Petrify  extends CursedEffect`
- [L1025](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1025) `class ForestFire  extends CursedEffect`
- [L1046](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1046) `class SpawnGoldenMimic  extends CursedEffect`
- [L1093](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1093) `class AbortRetryFail  extends CursedEffect`
- [L1141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1141) `class RandomTransmogrify  extends CursedEffect`
- [L1189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1189) `class HeroShapeShift  extends CursedEffect`
- [L1211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1211) `class SuperNova  extends CursedEffect`
- [L1227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1227) `class SinkHole  extends CursedEffect`
- [L1273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1273) `class GravityChaos  extends CursedEffect`

### 변수·상수 (단일 행 선언)

- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L164) `float[] EFFECT_CAT_CHANCES` 초기식: `new float[]{60, 30, 9, 1}`
- [L352](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L352) `Wand wand`
- [L837](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L837) `ConeAOE cone` 초기식: `null`

### 함수·메서드 역할과 내부 연결

- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L122) **`cursedZap(final Item origin, final Char user, final Ballistica bolt, final Callback afterZap)`**: 개별 처리 / 참조 호출: Random.Float, WondrousResin.positiveCurseEffectChance, randomValidEffect, effect.FX, Callback, call, effect.effect, afterZap.call
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L129) **`call()`**: 개별 처리 / 참조 호출: effect.effect, afterZap.call
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L136) **`tryForWandProc(Char target, Item origin)`**: 개별 처리 / 조건 분기 / 참조 호출: Wand.wandProc, origin.buffedLvl
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L146) **`valid(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L150) **`FX(final Item origin, final Char user, final Ballistica bolt, final Callback callback)`**: 개별 처리 / 참조 호출: MagicMissile.boltFromChar, Sample.INSTANCE.play
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L159) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L166) **`randomEffect()`**: 개별 처리 / 상태 선택 / 참조 호출: Random.chances, randomCommonEffect, randomUncommonEffect, randomRareEffect, randomVeryRareEffect
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L179) **`randomValidEffect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 상태 선택 / 참조 호출: Random.chances, randomValidCommonEffect, randomValidUncommonEffect, randomValidRareEffect, randomValidVeryRareEffect
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L208) **`randomCommonEffect()`**: 개별 처리 / 참조 호출: Random.element
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L212) **`randomValidCommonEffect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 반복 / 참조 호출: Random.element, effect.valid
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L222) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, Random.Int, Buff.affect, reignite, tryForWandProc
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L239) **`effect(Item origin, Char user, Ballistica bolt, boolean postiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, Dungeon.level.pressCell, GameScene.add, Blob.seed, tryForWandProc
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L251) **`valid(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, Char.hasProp
- [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L262) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, Char.hasProp, Random.Int, ScrollOfTeleportation.teleportChar, tryForWandProc
- [L282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L282) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Sample.INSTANCE.play, tryForWandProc, Actor.findChar, Dungeon.level.pressCell, Random.Int, GameScene.add, Blob.seed
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L304) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: tryForWandProc, Actor.findChar, Dungeon.level.pressCell, Random.Int, BurningTrap, set, activate, ChillingTrap, ShockingTrap
- [L326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L326) **`FX(Item origin, Char user, Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: MagicMissile.boltFromChar, Sample.INSTANCE.play
- [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L336) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.findChar, Dungeon.level.pressCell, tryForWandProc, CellEmitter.get, start, Speck.factory
- [L355](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L355) **`valid(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 참조 호출: super.valid
- [L361](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L361) **`FX(Item origin, Char user, Ballistica bolt, Callback callback)`**: 개별 처리 / 조건 분기 / 참조 호출: Generator.randomUsingDefaults, wand.fx
- [L369](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L369) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Generator.randomUsingDefaults, wand.upgrade, origin.level, Dungeon.scalingDepth, wand.onZap
- [L388](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L388) **`FX(Item origin, Char user, Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: callback.call
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L393) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: PathFinder.buildDistanceMap, BArray.not, Splash.at, Actor.findChar, Buff.affect, set, Sample.INSTANCE.play
- [L426](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L426) **`randomUncommonEffect()`**: 개별 처리 / 참조 호출: Random.element
- [L430](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L430) **`randomValidUncommonEffect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 반복 / 참조 호출: Random.element, effect.valid
- [L441](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L441) **`valid(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: level.traps.get, Dungeon.isChallenged
- [L455](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L455) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: valid, tryForWandProc, Actor.findChar, Dungeon.level.plant, Generator.randomUsingDefaults
- [L469](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L469) **`valid(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 참조 호출: Actor.findChar
- [L474](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L474) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, Dungeon.scalingDepth, Random.Int, Math.min, toHeal.sprite.emitter, burst, Speck.factory, toHeal.sprite.showStatusWithIcon, Integer.toString
- [L475](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L475) **`findChar(bolt.collisionPos)`**: 조회·탐색
- [L520](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L520) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 참조 호출: Bomb.ConjuredBomb, explode, tryForWandProc, Actor.findChar
- [L530](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L530) **`FX(Item origin, Char user, Ballistica bolt, Callback callback)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, sprite.parent.addToFront, Lightning, user.sprite.center, ch.sprite.center, DungeonTilemap.raisedTileCenterToWorld, Sample.INSTANCE.play, callback.call
- [L542](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L542) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: sprite.parent.add, Lightning, Dungeon.level.width, Actor.findChar, affected.add, affected.contains, tryForWandProc, Buff.prolong, ScrollOfRecharging.charge
- [L600](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L600) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 참조 호출: tryForWandProc, Actor.findChar, GeyserTrap, geyser.activate
- [L612](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L612) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 참조 호출: tryForWandProc, Actor.findChar, FlockTrap, set, activate
- [L622](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L622) **`valid(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 참조 호출: Actor.findChar
- [L627](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L627) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, Char.hasProp, Buff.affect
- [L641](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L641) **`FX(Item origin, Char user, Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: callback.call
- [L646](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L646) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: mob.beckon, user.sprite.centerEmitter, start, Speck.factory, Buff.affect, setup, Sample.INSTANCE.play
- [L677](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L677) **`randomRareEffect()`**: 개별 처리 / 참조 호출: Random.element
- [L681](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L681) **`randomValidRareEffect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 반복 / 참조 호출: Random.element, effect.valid
- [L692](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L692) **`valid(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, ch.properties, contains
- [L706](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L706) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: valid, Actor.findChar, Sheep, sheep.initialize, ch.destroy, ch.sprite.killAndErase, level.mobs.remove, TargetHealthIndicator.instance.target, GameScene.add
- [L731](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L731) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, Buff.affect, CursingTrap.curse
- [L749](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L749) **`FX(Item origin, Char user, Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: callback.call
- [L754](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L754) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.interfloorTeleportAllowed, Math.max, Random.chances, Level.beforeTransition, Game.switchScene, ScrollOfTeleportation.teleportChar
- [L784](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L784) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: ScrollOfMirrorImage.spawnImages, SummoningTrap, set, activate
- [L798](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L798) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.cellToPoint, Dungeon.level.length, ShadowCaster.castShadow, Dungeon.level.width, tryForWandProc, Actor.findChar, CellEmitter.get, burst, Buff.affect
- [L840](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L840) **`FX(Item origin, Char user, Ballistica bolt, Callback callback)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Ballistica, ConeAOE, sprite.parent.recycle, reset, ray.path.get, MagicMissile.boltFromChar, longestRay.path.get, Sample.INSTANCE.play
- [L873](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L873) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·반복·상태 선택 / 참조 호출: Actor.findChar, affectedChars.add, tryForWandProc, Random.NormalIntRange, Dungeon.scalingDepth, Random.Int, Buff.affect, burning.reignite, ch.damage
- [L950](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L950) **`FX(Item origin, Char user, Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: callback.call
- [L955](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L955) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 반복 / 참조 호출: Actor.chars, Buff.affect, Flare, color, show, GameScene.flash, Sample.INSTANCE.play, GLog.p, Messages.get
- [L975](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L975) **`valid(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리
- [L980](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L980) **`FX(Item origin, Char user, Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: callback.call
- [L985](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L985) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 참조 호출: Buff.affect, Sample.INSTANCE.play, user.sprite.emitter, burst, Speck.factory, GLog.w, Messages.get
- [L1013](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1013) **`randomVeryRareEffect()`**: 개별 처리 / 참조 호출: Random.element
- [L1017](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1017) **`randomValidVeryRareEffect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 반복 / 참조 호출: Random.element, effect.valid
- [L1027](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1027) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.length, GameScene.add, Blob.seed, Flare, color, show, Sample.INSTANCE.play, GLog.p, Messages.get
- [L1048](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1048) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.findChar, candidates.add, candidates.isEmpty, Random.element, Mimic.spawnAt, mimic.stopHiding, Sample.INSTANCE.play, CellEmitter.get, burst
- [L1096](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1096) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·예외 처리 / 참조 호출: Dungeon.saveAll, Messages.lang, ShatteredPixelDungeon.runOnRenderThread, Callback, call, GameScene.show, WndOptions, Icons.get, onSelect
- [L1108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1108) **`call()`**: 개별 처리 / 참조 호출: GameScene.show, WndOptions, Icons.get, onSelect, Game.instance.finish, onBackPressed
- [L1118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1118) **`onSelect(int index)`**: 이벤트·효과 실행 / 참조 호출: Game.instance.finish
- [L1123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1123) **`onBackPressed()`**: 이벤트·효과 실행
- [L1144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1144) **`valid(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.contains
- [L1155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1155) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: GameScene.show, ScrollOfMetamorphosis.WndMetamorphChoose, hero.belongings.contains, origin.isEquipped, doUnequip, origin.detach, Generator.randomUsingDefaults, Random.oneOf, result.isUpgradable
- [L1192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1192) **`valid(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 참조 호출: Actor.findChar
- [L1197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1197) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.affect, GLog.w, Messages.get, Actor.findChar
- [L1213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1213) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.append, GLog.p, Messages.get, GLog.w
- [L1230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1230) **`valid(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.bossLevel
- [L1239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1239) **`FX(Item origin, Char user, Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: callback.call
- [L1244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1244) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: BArray.not, BArray.or, PathFinder.buildDistanceMap, CellEmitter.floor, burst, positions.add, Buff.append, p.setPositions, GLog.p
- [L1276](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1276) **`FX(Item origin, Char user, Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: callback.call
- [L1281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/CursedWand.java#L1281) **`effect(Item origin, Char user, Ballistica bolt, boolean positiveOnly)`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.append, Sample.INSTANCE.play, GLog.p, Messages.get, GLog.w

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 593. [`DamageWand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/DamageWand.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 78행 / 타입 1개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/DamageWand.java#L33) `class DamageWand  extends Wand`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/DamageWand.java#L35) **`min()`**: 개별 처리 / 참조 호출: min, buffedLvl
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/DamageWand.java#L39) **`min(int lvl)`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/DamageWand.java#L41) **`max()`**: 개별 처리 / 참조 호출: max, buffedLvl
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/DamageWand.java#L45) **`max(int lvl)`**: 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/DamageWand.java#L47) **`damageRoll()`**: 전투 관련 / 참조 호출: damageRoll, buffedLvl
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/DamageWand.java#L51) **`damageRoll(int lvl)`**: 전투 관련 / 조건 분기 / 참조 호출: Hero.heroDamageIntRange, min, max, Dungeon.hero.buff, emp.detach, Sample.INSTANCE.play
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/DamageWand.java#L66) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, min, max
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/DamageWand.java#L74) **`upgradeStat1(int level)`**: 개별 처리 / 참조 호출: min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 594. [`Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 884행 / 타입 3개 / 필드 24개 / 메서드 63개.

### 타입·상속 선언

- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L76) `class Wand  extends Item`
- [L642](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L642) `class PlaceHolder  extends Wand`
- [L801](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L801) `class Charger  extends Buff`

### 변수·상수 (단일 행 선언)

- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L78) `String AC_ZAP` 초기식: `"ZAP"`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L80) `float TIME_TO_ZAP` 초기식: `1f`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L83) `int curCharges` 초기식: `maxCharges`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L84) `float partialCharge` 초기식: `0f`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L86) `Charger charger`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L88) `boolean curChargeKnown` 초기식: `false`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L90) `boolean curseInfusionBonus` 초기식: `false`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L91) `int resinBonus` 초기식: `0`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L93) `int USES_TO_ID` 초기식: `10`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L94) `float usesLeftToID` 초기식: `USES_TO_ID`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L95) `float availableUsesToID` 초기식: `USES_TO_ID/2f`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L97) `int collisionProperties` 초기식: `Ballistica.MAGIC_BOLT`
- [L595](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L595) `String USES_LEFT_TO_ID` 초기식: `"uses_left_to_id"`
- [L596](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L596) `String AVAILABLE_USES` 초기식: `"available_uses"`
- [L597](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L597) `String CUR_CHARGES` 초기식: `"curCharges"`
- [L598](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L598) `String CUR_CHARGE_KNOWN` 초기식: `"curChargeKnown"`
- [L599](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L599) `String PARTIALCHARGE` 초기식: `"partialCharge"`
- [L600](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L600) `String CURSE_INFUSION_BONUS` 초기식: `"curse_infusion_bonus"`
- [L601](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L601) `String RESIN_BONUS` 초기식: `"resin_bonus"`
- [L672](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L672) `Wand curWand`
- [L803](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L803) `float BASE_CHARGE_DELAY` 초기식: `10f`
- [L804](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L804) `float SCALING_CHARGE_ADDITION` 초기식: `40f`
- [L805](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L805) `float NORMAL_SCALE_FACTOR` 초기식: `0.875f`
- [L807](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L807) `float CHARGE_BUFF_BONUS` 초기식: `0.25f`

### 함수·메서드 역할과 내부 연결

- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L82) **`initialCharges()`**: 생성·초기화
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L106) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, actions.add
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L116) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, GameScene.selectCell
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L130) **`targetingPos(Hero user, int dst)`**: 개별 처리 / 조건 분기 / 참조 호출: Ballistica
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L138) **`onZap(Ballistica attack)`**: 이벤트·효과 실행
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L140) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L143) **`procChanceMultiplier(Char attacker)`**: 개별 처리 / 조건 분기 / 참조 호출: attacker.buff, pointsInTalent
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L150) **`tryToZap(Hero owner, int target)`**: 개별 처리 / 조건 분기 / 참조 호출: owner.buff, GLog.w, Messages.get, chargesPerCast
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L167) **`collect(Bag container)`**: 개별 처리 / 조건 분기 / 참조 호출: super.collect, charge
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L181) **`gainCharge(float amt)`**: 개별 처리 / 참조 호출: gainCharge
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L185) **`gainCharge(float amt, boolean overcharge)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Math.min, updateQuickslot
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L195) **`charge(Char owner)`**: 개별 처리 / 조건 분기 / 참조 호출: Charger, charger.attachTo
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L200) **`charge(Char owner, float chargeScaleFactor)`**: 개별 처리 / 참조 호출: charge, charger.setScaleFactor
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L205) **`wandProc(Char target, int chargesUsed)`**: 개별 처리 / 참조 호출: wandProc, buffedLvl
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L210) **`wandProc(Char target, int wandLevel, int chargesUsed)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.hasTalent, Dungeon.hero.pointsInTalent, Buff.append, target.id, Random.Float, Math.pow, SoulMark.prolong, target.buff, detach
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L247) **`onDetach()`**: 이벤트·효과 실행 / 참조 호출: stopCharging
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L251) **`stopCharging()`**: 개별 처리 / 조건 분기 / 참조 호출: charger.detach
- [L258](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L258) **`level(int value)`**: 개별 처리 / 참조 호출: super.level, updateLevel
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L265) **`identify(boolean byHero)`**: 개별 처리 / 참조 호출: super.identify, updateQuickslot
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L275) **`setIDReady()`**: 상태 갱신
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L279) **`readyToIdentify()`**: 개별 처리 / 참조 호출: isIdentified
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L283) **`onHeroGainExp(float levelPercent, Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Talent.itemIDSpeedFactor, isIdentified, Math.min
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L292) **`info()`**: 개별 처리 / 조건 분기 / 참조 호출: super.info, statsDesc, Messages.get, isIdentified
- [L316](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L316) **`statsDesc()`**: 개별 처리 / 참조 호출: Messages.get
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L320) **`upgradeStat1(int level)`**: 개별 처리
- [L324](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L324) **`upgradeStat2(int level)`**: 개별 처리
- [L328](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L328) **`upgradeStat3(int level)`**: 개별 처리
- [L333](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L333) **`isIdentified()`**: 조건 판정 / 참조 호출: super.isIdentified
- [L338](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L338) **`status()`**: 개별 처리 / 조건 분기
- [L347](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L347) **`level()`**: 개별 처리 / 조건 분기 / 참조 호출: updateLevel, super.level
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L359) **`upgrade()`**: 개별 처리 / 조건 분기 / 참조 호출: super.upgrade, Random.Int, updateLevel, Math.min, updateQuickslot
- [L379](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L379) **`degrade()`**: 개별 처리 / 참조 호출: super.degrade, updateLevel, updateQuickslot
- [L389](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L389) **`buffedLvl()`**: 개별 처리 / 조건 분기 / 참조 호출: super.buffedLvl, hero.belongings.contains, Dungeon.hero.buff, Degrade.reduceLevel, charger.target.buff, hasTalent, pointsInTalent, Random.Int, Math.min
- [L428](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L428) **`updateLevel()`**: 시간·상태 갱신 / 참조 호출: Math.min, initialCharges, level
- [L433](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L433) **`initialCharges()`**: 생성·초기화
- [L437](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L437) **`chargesPerCast()`**: 개별 처리
- [L441](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L441) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: MagicMissile.boltFromChar, Sample.INSTANCE.play
- [L450](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L450) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 참조 호출: particle.color, particle.setLifespan, particle.speed.polar, Random.Float, particle.setSize, particle.radiateXY
- [L458](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L458) **`wandUsed()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: isIdentified, Math.min, Talent.itemIDSpeedFactor, Dungeon.hero.pointsInTalent, ShardOfOblivion.passiveIDDisabled, GLog.p, Messages.get, name, setIDReady
- [L547](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L547) **`random()`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int, level, Random.Float
- [L570](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L570) **`glowing()`**: 개별 처리 / 조건 분기 / 참조 호출: ItemSprite.Glowing
- [L577](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L577) **`value()`**: 개별 처리 / 조건 분기 / 참조 호출: level
- [L604](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L604) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L616](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L616) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getBoolean, updateLevel, bundle.getFloat
- [L631](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L631) **`reset()`**: 생성·초기화 / 참조 호출: super.reset
- [L637](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L637) **`collisionProperties(int target)`**: 개별 처리 / 조건 분기
- [L649](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L649) **`isSimilar(Item item)`**: 조건 판정
- [L654](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L654) **`onZap(Ballistica attack)`**: 이벤트·효과 실행
- [L655](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L655) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행
- [L658](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L658) **`info()`**: 개별 처리
- [L663](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L663) **`Listener()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: onSelect, Ballistica, curWand.collisionProperties, curUser.hasTalent, curUser.buff, GLog.w, Messages.get, curUser.pointsInTalent, Buff.affect
- [L666](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L666) **`onSelect(Integer target)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Ballistica, curWand.collisionProperties, curUser.hasTalent, curUser.buff, GLog.w, Messages.get, curUser.pointsInTalent, Buff.affect, setShield
- [L679](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L679) **`Ballistica(curUser.pos, target, curWand.collisionProperties(target))`**: 개별 처리
- [L762](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L762) **`call()`**: 개별 처리 / 참조 호출: curWand.wandUsed
- [L768](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L768) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: curWand.onZap, Random.Float, WondrousResin.extraCurseEffectChance, CursedWand.cursedZap, Ballistica, Callback, call, curWand.wandUsed
- [L776](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L776) **`call()`**: 개별 처리 / 참조 호출: curWand.wandUsed
- [L796](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L796) **`prompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L812](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L812) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, cooldown, target.cooldown, spend
- [L824](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L824) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: target.buff, recharge, updateQuickslot, spend
- [L843](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L843) **`recharge()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Math.max, Math.pow, Regeneration.regenOn, RingOfEnergy.wandChargeMultiplier, target.buffs, bonus.remainder
- [L860](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L860) **`wand()`**: 개별 처리
- [L864](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L864) **`gainCharge(float charge)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: updateQuickslot
- [L879](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java#L879) **`setScaleFactor(float value)`**: 상태 갱신

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 595. [`WandOfBlastWave.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 296행 / 타입 4개 / 필드 6개 / 메서드 16개.

### 타입·상속 선언

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L56) `class WandOfBlastWave  extends DamageWand`
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L195) `class Knockback`
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L212) `class BWaveOnHitTracker  extends FlavourBuff`
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L238) `class BlastWave  extends Image`

### 변수·상수 (단일 행 선언)

- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L156) `int finalDist` 초기식: `dist`
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L157) `boolean finalCollided` 초기식: `collided && collideDmg`
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L158) `int initialpos` 초기식: `ch.pos`
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L240) `float TIME_TO_FADE` 초기식: `0.2f`
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L242) `float time`
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L243) `float size`

### 함수·메서드 역할과 내부 연결

- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L64) **`min(int lvl)`**: 개별 처리
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L68) **`max(int lvl)`**: 개별 처리
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L73) **`onZap(Ballistica bolt)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Sample.INSTANCE.play, BlastWave.blast, level.traps.get, Dungeon.level.pressCell, Actor.findChar, wandProc, chargesPerCast, ch.damage, damageRoll
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L120) **`throwChar(final Char ch, final Ballistica trajectory, int power, boolean closeDoors, boolean collideDmg, Object cause)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: ch.properties, contains, Math.min, Char.hasProp, trajectory.path.get, Actor.findChar, Actor.add, Pushing, Callback
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L152) **`get(dist)`**: 조회·탐색
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L161) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, ch.sprite.place, ch.isActive, ch.damage, Random.NormalIntRange, Knockback, Paralysis.prolong, Badges.validateDeathFromFriendlyMagic, GLog.n
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L198) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: defender.buff, detach, Hero.heroDamageIntRange, buffedLvl, defender.damage, Math.round, procChanceMultiplier, BlastWave.blast, Sample.INSTANCE.play
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L215) **`upgradeStat2(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L220) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: MagicMissile.boltFromChar, Sample.INSTANCE.play
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L230) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 참조 호출: particle.color, particle.setLifespan, particle.speed.polar, Random.Float, particle.setSize, particle.radiateXY
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L245) **`BlastWave()`**: 개별 처리 / 참조 호출: Effects.get, origin.set
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L250) **`reset(int pos, float size)`**: 생성·초기화 / 참조 호출: revive, Dungeon.level.width, resetColor, scale.set
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L264) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, kill, alpha
- [L276](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L276) **`blast(int pos)`**: 개별 처리 / 참조 호출: blast
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L280) **`blast(int pos, float radius)`**: 개별 처리 / 참조 호출: blast
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java#L284) **`blast(int pos, float radius, int hardLight)`**: 개별 처리 / 조건 분기 / 참조 호출: parent.recycle, parent.bringToFront, b.reset, b.hardlight

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 596. [`WandOfCorrosion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorrosion.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 138행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorrosion.java#L49) `class WandOfCorrosion  extends Wand`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorrosion.java#L58) **`onZap(Ballistica bolt)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Blob.seed, buffedLvl, CellEmitter.get, burst, Speck.factory, gas.setStrength, getClass, GameScene.add, Sample.INSTANCE.play
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorrosion.java#L82) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: MagicMissile.boltFromChar, Sample.INSTANCE.play
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorrosion.java#L93) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Math.max, buffedLvl, procChanceMultiplier, Random.Float, Buff.affect, set, CellEmitter.center, burst
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorrosion.java#L111) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 참조 호출: particle.color, ColorMath.random, particle.setLifespan, particle.acc.set, particle.setSize, particle.shuffleXY
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorrosion.java#L121) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, buffedLvl
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorrosion.java#L129) **`upgradeStat1(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorrosion.java#L134) **`upgradeStat2(int level)`**: 개별 처리 / 참조 호출: Messages.decimalFormat

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 597. [`WandOfCorruption.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 285행 / 타입 1개 / 필드 2개 / 메서드 8개.

### 타입·상속 선언

- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java#L79) `class WandOfCorruption  extends Wand`

### 변수·상수 (단일 행 선언)

- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java#L89) `float MINOR_DEBUFF_WEAKEN` 초기식: `1/4f`
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java#L108) `float MAJOR_DEBUFF_WEAKEN` 초기식: `1/2f`

### 함수·메서드 역할과 내부 연결

- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java#L127) **`onZap(Ballistica bolt)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Actor.findChar, buffedLvl, Dungeon.scalingDepth, AscensionChallenge.AscensionCorruptResist, Math.pow, enemy.buffs, MAJOR_DEBUFFS.containsKey, buff.getClass, MINOR_DEBUFFS.containsKey
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java#L195) **`debuffEnemy(Mob enemy, HashMap<Class<? extends Buff>, Float> category)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: enemy.buffs, debuffs.containsKey, existing.getClass, debuffs.put, debuffs.keySet, debuffs.get, enemy.isImmune, Random.chances, Buff.append
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java#L222) **`corruptEnemy(Mob enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: enemy.buff, GLog.w, Messages.get, enemy.isImmune, Corruption.corruptionHeal, AllyBuff.affectAndLoot, Buff.affect
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java#L239) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Math.max, buffedLvl, procChanceMultiplier, Random.Float, Buff.prolong, Math.round
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java#L255) **`upgradeStat1(int level)`**: 개별 처리 / 참조 호출: Messages.decimalFormat
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java#L260) **`upgradeStat2(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java#L265) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: MagicMissile.boltFromChar, Sample.INSTANCE.play
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java#L275) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 참조 호출: particle.color, particle.setLifespan, particle.speed.set, particle.setSize, particle.shuffleXY

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 598. [`WandOfDisintegration.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 166행 / 타입 1개 / 필드 0개 / 메서드 9개.

### 타입·상속 선언

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java#L46) `class WandOfDisintegration  extends DamageWand`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java#L55) **`min(int lvl)`**: 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java#L59) **`max(int lvl)`**: 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java#L64) **`targetingPos(Hero user, int dst)`**: 개별 처리 / 조건 분기 / 참조 호출: super.targetingPos
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java#L73) **`onZap(Ballistica beam)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: buffedLvl, Math.min, distance, level.blobs.get, beam.subPath, Actor.findChar, chars.add, Dungeon.level.destroy, GameScene.updateMap
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java#L133) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java#L137) **`distance()`**: 개별 처리 / 참조 호출: buffedLvl
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java#L142) **`upgradeStat2(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java#L147) **`fx(Ballistica beam, Callback callback)`**: 개별 처리 / 참조 호출: beam.path.get, Math.min, distance, sprite.parent.add, Beam.DeathRay, curUser.sprite.center, DungeonTilemap.raisedTileCenterToWorld, Sample.INSTANCE.play, callback.call
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java#L156) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 참조 호출: particle.color, particle.setLifespan, particle.acc.set, particle.setSize, particle.shuffleXY

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 599. [`WandOfFireblast.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 294행 / 타입 1개 / 필드 0개 / 메서드 11개.

### 타입·상속 선언

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L56) `class WandOfFireblast  extends DamageWand`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L66) **`min(int lvl)`**: 개별 처리 / 참조 호출: chargesPerCast
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L71) **`max(int lvl)`**: 개별 처리 / 상태 선택 / 참조 호출: chargesPerCast
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L85) **`onZap(Ballistica bolt)`**: 이벤트·효과 실행 / 조건 분기·반복·상태 선택 / 참조 호출: Level.set, GameScene.updateMap, Dungeon.level.adjacent, adjacentCells.add, level.heaps.get, burn, GameScene.add, Blob.seed, chargesPerCast
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L157) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Actor.findChar, buff, Fire.volumeAt, Math.min, Wand.procChanceMultiplier, Random.Float, Math.max, level.blobs.get, CellEmitter.center
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L215) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: chargesPerCast, ConeAOE, sprite.parent.recycle, reset, ray.path.get, MagicMissile.boltFromChar, longestRay.path.get, Sample.INSTANCE.play
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L251) **`chargesPerCast()`**: 개별 처리 / 조건 분기 / 참조 호출: charger.target.buff, GameMath.gate, Math.ceil
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L261) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, chargesPerCast, min, max
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L269) **`upgradeStat1(int level)`**: 개별 처리
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L274) **`upgradeStat2(int level)`**: 개별 처리
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L279) **`upgradeStat3(int level)`**: 개별 처리
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java#L284) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 참조 호출: particle.color, particle.setLifespan, particle.acc.set, particle.setSize, particle.shuffleXY

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 600. [`WandOfFrost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 169행 / 타입 1개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L44) `class WandOfFrost  extends DamageWand`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L50) **`min(int lvl)`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L54) **`max(int lvl)`**: 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L59) **`onZap(Ballistica bolt)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: level.heaps.get, heap.freeze, level.blobs.get, fire.clear, eternalFire.clear, bolt.path.size, bolt.path.get, Actor.findChar, damageRoll
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L113) **`upgradeStat2(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L118) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: MagicMissile.boltFromChar, Sample.INSTANCE.play
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L128) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: defender.buff, Math.floor, chill.cooldown, procChanceMultiplier, Random.Float, Math.max, FlavourBuff, act, Buff.affect
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L147) **`act()`**: 시간·상태 갱신 / 참조 호출: Buff.affect, Math.round, super.act
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java#L157) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 참조 호출: particle.color, particle.setLifespan, Random.Float, particle.speed.polar, particle.acc.set, particle.setSize, particle.radiateXY

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 601. [`WandOfLightning.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 216행 / 타입 2개 / 필드 1개 / 메서드 9개.

### 타입·상속 선언

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java#L52) `class WandOfLightning  extends DamageWand`
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java#L124) `class LightningCharge  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java#L130) `float DURATION` 초기식: `10f`

### 함수·메서드 역할과 내부 연결

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java#L62) **`min(int lvl)`**: 개별 처리
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java#L66) **`max(int lvl)`**: 개별 처리
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java#L71) **`onZap(Ballistica bolt)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: affected.toArray, affected.remove, ch.buff, affected.size, PixelScene.shake, ch.sprite.centerEmitter, burst, ch.sprite.flash, wandProc
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java#L106) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: buffedLvl, procChanceMultiplier, Random.Float, Math.max, FlavourBuff.prolong, attacker.sprite.centerEmitter, burst, attacker.sprite.flash, Sample.INSTANCE.play
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java#L133) **`icon()`**: 개별 처리
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java#L138) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java#L143) **`arc(Char ch)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: curUser.buff, PathFinder.buildDistanceMap, BArray.not, Actor.findChar, affected.contains, hitThisArc.add, affected.addAll, arcs.add, Lightning.Arc
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java#L173) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 조건 분기 / 참조 호출: affected.clear, arcs.clear, Actor.findChar, affected.add, arcs.add, Lightning.Arc, curUser.sprite.center, ch.sprite.center, arc
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java#L201) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 참조 호출: particle.color, particle.setLifespan, particle.acc.set, particle.speed.polar, Random.Float, particle.setSize, particle.shuffleXY

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 602. [`WandOfLivingEarth.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 485행 / 타입 4개 / 필드 9개 / 메서드 29개.

### 타입·상속 선언

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L56) `class WandOfLivingEarth  extends DamageWand`
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L261) `class RockArmor  extends Buff`
- [L365](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L365) `class EarthGuardian  extends NPC`
- [L463](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L463) `class Wandering  extends Mob.Wandering`

### 변수·상수 (단일 행 선언)

- [L267](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L267) `int wandLevel`
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L268) `int armor`
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L270) `float powerOfManyTurns` 초기식: `0`
- [L343](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L343) `String WAND_LEVEL` 초기식: `"wand_level"`
- [L344](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L344) `String ARMOR` 초기식: `"armor"`
- [L346](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L346) `String POWER_TURNS` 초기식: `"power_turns"`
- [L384](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L384) `int wandLevel` 초기식: `-1`
- [L446](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L446) `String DEFENSE` 초기식: `"defense"`
- [L447](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L447) `String WAND_LEVEL` 초기식: `"wand_level"`

### 함수·메서드 역할과 내부 연결

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L63) **`min(int lvl)`**: 개별 처리
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L68) **`max(int lvl)`**: 개별 처리
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L73) **`onZap(Ballistica bolt)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Actor.findChar, damageRoll, Stasis.getStasisAlly, curUser.buff, Buff.affect, buff.addArmor, buffedLvl, guardian.sprite.centerEmitter, burst
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L201) **`upgradeStat2(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L206) **`upgradeStat3(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.isChallenged
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L215) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 참조 호출: MagicMissile.boltFromChar, Sample.INSTANCE.play
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L225) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Math.round, procChanceMultiplier, guardian.sprite.centerEmitter, burst, buffedLvl, guardian.setInfo, attacker.sprite.centerEmitter, Buff.affect, addArmor
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L246) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int, particle.color, ColorMath.random, particle.setLifespan, particle.setSize, particle.shuffleXY, Random.Float
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L273) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: BuffIndicator.refreshHero, spend
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L285) **`addArmor(int wandLevel, int toAdd)`**: 상태 갱신 / 참조 호출: Math.max, Math.min, armorToGuardian
- [L291](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L291) **`armorToGuardian()`**: 개별 처리
- [L295](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L295) **`absorb(int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: detach
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L306) **`isEmpowered()`**: 조건 판정
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L311) **`icon()`**: 개별 처리
- [L316](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L316) **`tintIcon(Image icon)`**: 개별 처리 / 조건 분기 / 참조 호출: isEmpowered, icon.hardlight, icon.brightness
- [L325](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L325) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, armorToGuardian
- [L330](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L330) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L335](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L335) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, armorToGuardian, isEmpowered
- [L349](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L349) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L357](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L357) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getFloat
- [L386](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L386) **`setInfo(Hero hero, int wandLevel, int healthToAdd)`**: 상태 갱신 / 조건 분기 / 참조 호출: sprite.showStatusWithIcon, Integer.toString, Math.min
- [L400](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L400) **`attackSkill(Char target)`**: 전투 관련
- [L406](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L406) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: aggro, super.attackProc
- [L412](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L412) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange, Dungeon.scalingDepth
- [L417](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L417) **`drRoll()`**: 개별 처리 / 조건 분기 / 참조 호출: super.drRoll, Dungeon.isChallenged, Random.NormalIntRange
- [L427](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L427) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, Actor.chars, contains, Dungeon.isChallenged
- [L450](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L450) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L457](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L457) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L466](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java#L466) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Buff.affect, addArmor, buff, cooldown, hero.sprite.centerEmitter, burst, destroy, sprite.die, super.act

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 603. [`WandOfMagicMissile.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 167행 / 타입 2개 / 필드 4개 / 메서드 15개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L41) `class WandOfMagicMissile  extends DamageWand`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L95) `class MagicCharge  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L102) `float DURATION` 초기식: `4f`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L104) `int level` 초기식: `0`
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L105) `Wand wandJustApplied`
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L151) `String LEVEL` 초기식: `"level"`

### 함수·메서드 역할과 내부 연결

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L47) **`min(int lvl)`**: 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L51) **`max(int lvl)`**: 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L56) **`onZap(Ballistica bolt)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Actor.findChar, wandProc, chargesPerCast, ch.damage, damageRoll, Sample.INSTANCE.play, Random.Float, ch.sprite.burst, buffedLvl
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L81) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: SpellSprite.show, attacker.buffs, c.wand, c.gainCharge, procChanceMultiplier
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L91) **`initialCharges()`**: 생성·초기화
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L107) **`setup(Wand wand)`**: 생성·초기화 / 조건 분기 / 참조 호출: wand.buffedLvl
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L115) **`detach()`**: 개별 처리 / 참조 호출: super.detach, updateQuickslot
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L120) **`level()`**: 개별 처리
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L125) **`wandJustApplied()`**: 개별 처리
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L132) **`icon()`**: 개별 처리
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L137) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L142) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L147) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, level, dispTurns
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L154) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java#L160) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 604. [`WandOfPrismaticLight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 180행 / 타입 1개 / 필드 0개 / 메서드 10개.

### 타입·상속 선언

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java#L52) `class WandOfPrismaticLight  extends DamageWand`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java#L60) **`min(int lvl)`**: 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java#L64) **`max(int lvl)`**: 개별 처리
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java#L69) **`onZap(Ballistica beam)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: affectMap, Dungeon.isChallenged, Buff.prolong, buffedLvl, Actor.findChar, wandProc, chargesPerCast, affectTarget
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java#L87) **`affectTarget(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: damageRoll, Random.Int, buffedLvl, Buff.prolong, ch.sprite.emitter, burst, Speck.factory, ch.properties, contains
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java#L109) **`affectMap(Ballistica beam)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: beam.subPath, Dungeon.level.insideMap, Dungeon.level.discover, GameScene.discoverTile, ScrollOfMagicMapping.discover, CellEmitter.center, burst, Random.IntRange, Sample.INSTANCE.play
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java#L142) **`upgradeStat2(int level)`**: 개별 처리 / 참조 호출: Messages.decimalFormat
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java#L147) **`upgradeStat3(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.isChallenged, Integer.toString
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java#L156) **`fx(Ballistica beam, Callback callback)`**: 개별 처리 / 참조 호출: sprite.parent.add, Beam.LightRay, curUser.sprite.center, DungeonTilemap.raisedTileCenterToWorld, Sample.INSTANCE.play, callback.call
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java#L164) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행 / 참조 호출: Buff.prolong, Math.round, staff.buffedLvl, procChanceMultiplier
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java#L170) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 참조 호출: particle.color, Random.Int, particle.setLifespan, particle.speed.polar, Random.Float, particle.setSize, particle.radiateXY

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 605. [`WandOfRegrowth.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 513행 / 타입 6개 / 필드 6개 / 메서드 27개.

### 타입·상속 선언

- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L61) `class WandOfRegrowth  extends Wand`
- [L340](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L340) `class Dewcatcher  extends Plant`
- [L373](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L373) `class Seed  extends Plant.Seed`
- [L380](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L380) `class Seedpod  extends Plant`
- [L409](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L409) `class Seed  extends Plant.Seed`
- [L417](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L417) `class Lotus  extends NPC`

### 변수·상수 (단일 행 선언)

- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L70) `int totChrgUsed` 초기식: `0`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L71) `int chargesOverLimit` 초기식: `0`
- [L323](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L323) `String TOTAL` 초기식: `"totChrgUsed"`
- [L324](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L324) `String OVER` 초기식: `"chargesOverLimit"`
- [L429](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L429) `int wandLvl` 초기식: `0`
- [L497](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L497) `String WAND_LVL` 초기식: `"wand_lvl"`

### 함수·메서드 역할과 내부 연결

- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L77) **`tryToZap(Hero owner, int target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.tryToZap
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L87) **`onZap(Ballistica bolt)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: chargeLimit, chargesPerCast, Math.round, buffedLvl, cells.iterator, i.hasNext, i.next, i.remove, Char.hasProp
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L203) **`chargeLimit(int heroLvl)`**: 개별 처리 / 참조 호출: chargeLimit, level
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L207) **`chargeLimit(int heroLvl, int wndLvl)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L219) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Math.max, staff.buffedLvl, Math.round, procChanceMultiplier, Buff.affect, boost
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L244) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: chargesPerCast, ConeAOE, sprite.parent.recycle, reset, ray.path.get, MagicMissile.boltFromChar, longestRay.path.get, Sample.INSTANCE.play
- [L278](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L278) **`chargesPerCast()`**: 개별 처리 / 조건 분기 / 참조 호출: charger.target.buff, GameMath.gate, Math.ceil
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L288) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, chargesPerCast, isIdentified, chargeLimit, Math.max
- [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L298) **`upgradeStat1(int level)`**: 개별 처리 / 참조 호출: Messages.decimalFormat
- [L303](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L303) **`upgradeStat2(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Integer.toString, chargeLimit
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L312) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 참조 호출: particle.color, ColorMath.random, particle.setLifespan, particle.setSize, particle.shuffleXY, Random.Float
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L327) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L334](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L334) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L347](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L347) **`activate(Char ch)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Random.NormalIntRange, Dungeon.level.entrance, Dungeon.level.exit, candidates.add, candidates.isEmpty, Random.element, level.heaps.get, Dungeon.level.drop, Dewdrop
- [L387](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L387) **`activate(Char ch)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Random.NormalIntRange, Dungeon.level.entrance, Dungeon.level.exit, candidates.add, candidates.isEmpty, Random.element, Dungeon.level.drop, Generator.randomUsingDefaults, sprite.drop
- [L431](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L431) **`setLevel(int lvl)`**: 상태 갱신
- [L436](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L436) **`inRange(int pos)`**: 개별 처리 / 참조 호출: Dungeon.level.trueDistance
- [L440](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L440) **`seedPreservation()`**: 개별 처리 / 참조 호출: Math.min
- [L445](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L445) **`canInteract(Char c)`**: 조건 판정
- [L450](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L450) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.act, destroy, sprite.die
- [L462](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L462) **`damage(int dmg, Object src)`**: 전투 관련
- [L467](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L467) **`add(Buff buff)`**: 상태 갱신
- [L472](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L472) **`destroy()`**: 개별 처리 / 참조 호출: super.destroy, Dungeon.observe, GameScene.updateFog
- [L479](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L479) **`isInvulnerable(Class effect)`**: 조건 판정
- [L488](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L488) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, Actor.chars, contains, Math.round, seedPreservation
- [L500](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L500) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L506](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java#L506) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 606. [`WandOfTransfusion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 231행 / 타입 1개 / 필드 2개 / 메서드 13개.

### 타입·상속 선언

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L53) `class WandOfTransfusion  extends DamageWand`

### 변수·상수 (단일 행 선언)

- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L71) `boolean freeCharge` 초기식: `false`
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L216) `String FREECHARGE` 초기식: `"freecharge"`

### 함수·메서드 역할과 내부 연결

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L62) **`min(int level)`**: 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L67) **`max(int level)`**: 개별 처리
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L74) **`onZap(Ballistica beam)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: beam.subPath, CellEmitter.center, burst, Actor.findChar, wandProc, chargesPerCast, ch.buff, Math.round, buffedLvl
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L149) **`damageHero(int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: curUser.damage, curUser.isAlive, Badges.validateDeathFromFriendlyMagic, Dungeon.fail, GLog.n, Messages.get
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L161) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: defender.buff, attacker.id, Math.round, buffedLvl, procChanceMultiplier, Buff.affect, setShield, attacker.sprite.showStatusWithIcon, Integer.toString
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L174) **`fx(Ballistica beam, Callback callback)`**: 개별 처리 / 참조 호출: sprite.parent.add, Beam.HealthRay, curUser.sprite.center, DungeonTilemap.raisedTileCenterToWorld, Sample.INSTANCE.play, callback.call
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L182) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 참조 호출: particle.color, particle.setLifespan, particle.speed.polar, Random.Float, particle.setSize, particle.radiateXY
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L192) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, Messages.get, buffedLvl, min, max
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L201) **`upgradeStat1(int level)`**: 개별 처리 / 참조 호출: Math.round, Integer.toString
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L207) **`upgradeStat2(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L212) **`upgradeStat3(int level)`**: 개별 처리 / 참조 호출: super.upgradeStat1
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L219) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getBoolean
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java#L225) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 607. [`WandOfWarding.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.wands` / 본문 521행 / 타입 3개 / 필드 7개 / 메서드 32개.

### 타입·상속 선언

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L57) `class WandOfWarding  extends Wand`
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L233) `class Ward  extends NPC`
- [L299](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L299) `class WardSentry  extends Ward`

### 변수·상수 (단일 행 선언)

- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L78) `boolean wardAvailable` 초기식: `true`
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L235) `int tier` 초기식: `1`
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L236) `int wandLevel` 초기식: `1`
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L238) `int totalZaps` 초기식: `0`
- [L499](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L499) `String TIER` 초기식: `"tier"`
- [L500](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L500) `String WAND_LEVEL` 초기식: `"wand_level"`
- [L501](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L501) `String TOTAL_ZAPS` 초기식: `"total_zaps"`

### 함수·메서드 역할과 내부 연결

- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L65) **`collisionProperties(int target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.collisionProperties
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L72) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 참조 호출: super.execute
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L81) **`tryToZap(Hero owner, int target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.tryToZap, Actor.chars, Stasis.getStasisAlly, curUser.buffs, wand, level, Actor.findChar, GLog.w, Messages.get
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L126) **`onZap(Ballistica bolt)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Actor.findChar, bolt.path.get, GLog.w, Messages.get, Dungeon.level.pressCell, upgrade, buffedLvl, wandHeal, ch.sprite.emitter
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L171) **`fx(Ballistica bolt, Callback callback)`**: 개별 처리 / 조건 분기 / 참조 호출: MagicMissile.boltFromChar, m.setSpeed, Sample.INSTANCE.play
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L185) **`onHit(MagesStaff staff, Char attacker, Char defender, int damage)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Math.max, staff.buffedLvl, procChanceMultiplier, Random.Float, Actor.chars, wandHeal, ch.sprite.emitter, burst
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L206) **`staffFx(MagesStaff.StaffParticle particle)`**: 개별 처리 / 참조 호출: particle.color, particle.setLifespan, particle.speed.polar, Random.Float, particle.setSize, particle.radiateXY
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L216) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, level
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L224) **`upgradeStat1(int level)`**: 개별 처리
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L229) **`upgradeStat2(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L253) **`name()`**: 개별 처리 / 참조 호출: Messages.get
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L257) **`upgrade(int wandLevel)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: wandHeal, Actor.chars, contains, Bestiary.setSeen, updateTier, sprite.place, GameScene.updateFog
- [L301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L301) **`wandHeal(int wandLevel)`**: 개별 처리 / 참조 호출: wandHeal
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L305) **`wandHeal(int wandLevel, float healFactor)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Math.round, Random.IntRange, Math.max, Math.min, sprite.showStatusWithIcon, Integer.toString
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L341) **`defenseSkill(Char enemy)`**: 전투 관련 / 조건 분기 / 참조 호출: Dungeon.scalingDepth, super.defenseSkill
- [L349](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L349) **`drRoll()`**: 개별 처리 / 조건 분기 / 참조 호출: super.drRoll, Math.round, Random.NormalIntRange, Dungeon.scalingDepth
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L359) **`canAttack(Char enemy)`**: 조건 판정 / 참조 호출: Ballistica
- [L364](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L364) **`doAttack(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: sprite.zap, zap
- [L375](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L375) **`zap()`**: 이벤트·효과 실행 / 조건 분기·상태 선택 / 참조 호출: spend, Hero.heroDamageIntRange, enemy.damage, enemy.isAlive, Wand.wandProc, Badges.validateDeathFromFriendlyMagic, GLog.n, Messages.capitalize, Messages.get
- [L411](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L411) **`onZapComplete()`**: 이벤트·효과 실행 / 참조 호출: zap, next
- [L417](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L417) **`getCloser(int target)`**: 조회·탐색
- [L422](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L422) **`getFurther(int target)`**: 조회·탐색
- [L427](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L427) **`sprite()`**: 개별 처리 / 참조 호출: super.sprite, sprite.linkVisuals
- [L434](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L434) **`updateSpriteState()`**: 시간·상태 갱신 / 참조 호출: super.updateSpriteState, updateTier, sprite.place
- [L441](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L441) **`destroy()`**: 개별 처리 / 참조 호출: super.destroy, Dungeon.observe, GameScene.updateFog
- [L448](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L448) **`canInteract(Char c)`**: 조건 판정
- [L453](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L453) **`interact(Char c)`**: 개별 처리 / 조건 분기 / 참조 호출: Game.runOnRenderThread, Callback, call, GameScene.show, WndOptions, sprite, Messages.get, onSelect, die
- [L459](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L459) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.show, WndOptions, sprite, Messages.get, onSelect, die
- [L466](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L466) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: die
- [L478](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L478) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.chars, contains, Messages.get
- [L504](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L504) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L512](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java#L512) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":66,"fields":64,"methods":338}

# Java 소스 구현 분석 922–939

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 922. [`CursingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/CursingTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 134행.

### 클래스/타입
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/CursingTrap.java#L44) `public class CursingTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/CursingTrap.java#L52) `public void activate() {` — 행동·상태 갱신, 인접 호출: CellEmitter.get, INSTANCE.play
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/CursingTrap.java#L71) `public static void curse(Hero hero){` — 개별 처리, 인접 호출: Collections.shuffle, EquipableItem.equipCursed, GLog.n, Messages.get
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/CursingTrap.java#L116) `private static void curse(Item item){` — 개별 처리, 인접 호출: Enchantment.randomCurse, Glyph.randomCurse, Item.updateQuickslot

## 923. [`DisarmingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DisarmingTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 118행.

### 클래스/타입
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DisarmingTrap.java#L41) `public class DisarmingTrap extends Trap{`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DisarmingTrap.java#L49) `public void activate() {` — 행동·상태 갱신, 인접 호출: GameScene.updateFog, INSTANCE.play, CellEmitter.get, Speck.factory, Actor.findChar, PathFinder.buildDistanceMap

## 924. [`DisintegrationTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DisintegrationTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 105행.

### 클래스/타입
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DisintegrationTrap.java#L42) `public class DisintegrationTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DisintegrationTrap.java#L53) `public void activate() {` — 행동·상태 갱신, 인접 호출: Actor.findChar, Math.max, Actor.chars, Buff.prolong, INSTANCE.play, ShatteredPixelDungeon.scene, Beam.DeathRay

## 925. [`DistortionTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DistortionTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 164행.

### 클래스/타입
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DistortionTrap.java#L53) `public class DistortionTrap extends Trap{`

### 변수·상수 후보
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DistortionTrap.java#L55) `private static final float DELAY = 2f;`

### 메서드 및 코드 의존 단서
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DistortionTrap.java#L63) `public void activate() {` — 행동·상태 갱신, 인접 호출: Random.Int, Actor.findChar, Random.index, Dungeon.bossLevel

## 926. [`ExplosiveTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ExplosiveTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 55행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ExplosiveTrap.java#L32) `public class ExplosiveTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ExplosiveTrap.java#L40) `public void activate() {` — 행동·상태 갱신, 인접 호출: Actor.findChar, Buff.prolong, Badges.validateDeathFromFriendlyMagic

## 927. [`FlashingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FlashingTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 72행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FlashingTrap.java#L36) `public class FlashingTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FlashingTrap.java#L47) `public void activate() {` — 행동·상태 갱신, 인접 호출: Actor.findChar, Math.max, Buff.affect, Buff.prolong, GameScene.flash, INSTANCE.play

## 928. [`FlockTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FlockTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 86행.

### 클래스/타입
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FlockTrap.java#L40) `public class FlockTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FlockTrap.java#L49) `public void activate() {` — 행동·상태 갱신, 인접 호출: PathFinder.buildDistanceMap, BArray.not, Actor.findChar, GameScene.add, CellEmitter.get, Speck.factory, Bestiary.setSeen

## 929. [`FrostTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FrostTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 63행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FrostTrap.java#L37) `public class FrostTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FrostTrap.java#L45) `public void activate() {` — 행동·상태 갱신, 인접 호출: Splash.at, INSTANCE.play, PathFinder.buildDistanceMap, BArray.not, GameScene.add, Blob.seed, Actor.findChar

## 930. [`GatewayTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GatewayTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 165행.

### 클래스/타입
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GatewayTrap.java#L43) `public class GatewayTrap extends Trap {`

### 변수·상수 후보
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GatewayTrap.java#L53) `private int telePos = -1;`
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GatewayTrap.java#L151) `private static final String TELE_POS = "tele_pos";`

### 메서드 및 코드 의존 단서
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GatewayTrap.java#L56) `public void activate() {` — 행동·상태 갱신, 인접 호출: Actor.findChar, ScrollOfTeleportation.teleportChar, Buff.prolong, Random.shuffle
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GatewayTrap.java#L154) `public void storeInBundle(Bundle bundle) {` — 저장·복원
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GatewayTrap.java#L160) `public void restoreFromBundle(Bundle bundle) {` — 저장·복원

## 931. [`GeyserTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GeyserTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 152행.

### 클래스/타입
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GeyserTrap.java#L44) `public class GeyserTrap extends Trap {`

### 변수·상수 후보
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GeyserTrap.java#L51) `public int centerKnockBackDirection = -1;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GeyserTrap.java#L52) `public Object source = this;`

### 메서드 및 코드 의존 단서
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GeyserTrap.java#L55) `public void activate() {` — 행동·상태 갱신, 인접 호출: Splash.at, DungeonTilemap.tileCenterToWorld, INSTANCE.play, PathFinder.buildDistanceMap, BArray.not, Random.Int, Actor.findChar

## 932. [`GnollRockfallTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GnollRockfallTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 119행.

### 클래스/타입
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GnollRockfallTrap.java#L50) `public class GnollRockfallTrap extends RockfallTrap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GnollRockfallTrap.java#L53) `public void activate() {` — 행동·상태 갱신, 인접 호출: PathFinder.buildDistanceMap, BArray.not, CellEmitter.get, Speck.factory, Actor.findChar, Buff.prolong, Random.NormalIntRange

## 933. [`GrimTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrimTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 143행.

### 클래스/타입
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrimTrap.java#L42) `public class GrimTrap extends Trap {`

### 변수·상수 후보
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrimTrap.java#L94) `final Char finalTarget = target;`
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrimTrap.java#L103) `final int finalDmg = damage;`

### 메서드 및 코드 의존 단서
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrimTrap.java#L53) `public void activate() {` — 행동·상태 갱신, 인접 호출: Actor.add, Actor.remove, Actor.findChar, Math.max, Actor.chars, Buff.prolong, Math.round
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrimTrap.java#L63) `protected boolean act() {` — 행동·상태 갱신, 인접 호출: Actor.remove, Actor.findChar, Math.max, Actor.chars, Buff.prolong, Math.round, Math.min
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrimTrap.java#L111) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play, Badges.validateDeathFromGrimOrDisintTrap, Dungeon.fail, GLog.n, Messages.get, Badges.validateDeathFromFriendlyMagic, CellEmitter.get

## 934. [`GrippingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrippingTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 61행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrippingTrap.java#L32) `public class GrippingTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrippingTrap.java#L43) `public void activate() {` — 행동·상태 갱신, 인접 호출: Actor.findChar, Buff.prolong, Math.max, Buff.affect, Wound.hit

## 935. [`GuardianTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GuardianTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 118행.

### 클래스/타입
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GuardianTrap.java#L38) `public class GuardianTrap extends Trap {`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GuardianTrap.java#L72) `public static class Guardian extends Statue {`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GuardianTrap.java#L104) `public static class GuardianSprite extends StatueSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GuardianTrap.java#L46) `public void activate() {` — 행동·상태 갱신, 인접 호출: GLog.w, Messages.get, CellEmitter.center, Speck.factory, INSTANCE.play, GameScene.add, Generator.randomUsingDefaults
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GuardianTrap.java#L84) `public void createWeapon( boolean useDecks ) {` — 생성·초기화, 인접 호출: Generator.randomUsingDefaults
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GuardianTrap.java#L92) `public void beckon(int cell) {` — 개별 처리
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GuardianTrap.java#L106) `public GuardianSprite(){` — 개별 처리
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GuardianTrap.java#L112) `public void resetColor() {` — 개별 처리

## 936. [`OozeTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/OozeTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 57행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/OozeTrap.java#L33) `public class OozeTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/OozeTrap.java#L41) `public void activate() {` — 행동·상태 갱신, 인접 호출: Splash.at, Actor.findChar, Buff.affect, Buff.prolong

## 937. [`PitfallTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 176행.

### 클래스/타입
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L43) `public class PitfallTrap extends Trap {`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L79) `public static class DelayedPit extends FlavourBuff {`

### 변수·상수 후보
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L85) `public int[] positions = new int[0];`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L86) `public int depth;`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L87) `public int branch;`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L89) `public boolean ignoreAllies = false;`
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L150) `private static final String POSITIONS = "positions";`
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L151) `private static final String DEPTH = "depth";`
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L152) `private static final String BRANCH = "branch";`
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L154) `private static final String IGNORE_ALLIES = "ignore_allies";`

### 메서드 및 코드 의존 단서
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L51) `public void activate() {` — 행동·상태 갱신, 인접 호출: Dungeon.bossLevel, GLog.w, Messages.get, Buff.append, CellEmitter.floor, GLog.n
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L92) `public boolean act() {` — 행동·상태 갱신, 인접 호출: CellEmitter.floor, Actor.findChar, Char.hasProp, Chasm.mobFall, Dungeon.dropToChasm, GameScene.discard, Chasm.heroFall
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L143) `public void setPositions(ArrayList<Integer> positions){` — 개별 처리
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L157) `public void storeInBundle(Bundle bundle) {` — 저장·복원
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java#L166) `public void restoreFromBundle(Bundle bundle) {` — 저장·복원

## 938. [`PoisonDartTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PoisonDartTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 149행.

### 클래스/타입
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PoisonDartTrap.java#L44) `public class PoisonDartTrap extends Trap {`

### 변수·상수 후보
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PoisonDartTrap.java#L108) `final Char finalTarget = target;`

### 메서드 및 코드 의존 단서
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PoisonDartTrap.java#L54) `protected int poisonAmount(){` — 개별 처리, 인접 호출: Math.round, Actor.add, Actor.remove, Actor.findChar, Math.max, Actor.chars
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PoisonDartTrap.java#L58) `protected boolean canTarget( Char ch ){` — 조회·판정, 인접 호출: Actor.add, Actor.remove, Actor.findChar, Math.max, Actor.chars
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PoisonDartTrap.java#L63) `public void activate() {` — 행동·상태 갱신, 인접 호출: Actor.add, Actor.remove, Actor.findChar, Math.max, Actor.chars, Buff.prolong
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PoisonDartTrap.java#L73) `protected boolean act() {` — 행동·상태 갱신, 인접 호출: Actor.remove, Actor.findChar, Math.max, Actor.chars, Buff.prolong, ShatteredPixelDungeon.scene, Random.NormalIntRange
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PoisonDartTrap.java#L113) `public void call() {` — 개별 처리, 인접 호출: Random.NormalIntRange, Dungeon.fail, GLog.n, Messages.get, Badges.validateDeathFromFriendlyMagic, Buff.affect, INSTANCE.play

## 939. [`RockfallTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/RockfallTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.levels.traps`, 123행.

### 클래스/타입
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/RockfallTrap.java#L47) `public class RockfallTrap extends Trap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/RockfallTrap.java#L58) `public void activate() {` — 행동·상태 갱신, 인접 호출: PathFinder.buildDistanceMap, BArray.not, CellEmitter.get, Speck.factory, Actor.findChar, Buff.prolong, Random.NormalIntRange


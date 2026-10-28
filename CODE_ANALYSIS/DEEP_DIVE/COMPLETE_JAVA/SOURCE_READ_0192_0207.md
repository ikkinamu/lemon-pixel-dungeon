# Java 파일별 소스 구현 해설 192–207

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 192. [`DM201.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 133행 / 타입 2개 / 필드 1개 / 메서드 9개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java#L35) `class DM201  extends DM200`
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java#L111) `class Hunting  extends Mob.Hunting`

### 변수·상수 (단일 행 선언)

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java#L52) `boolean threatened` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java#L48) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java#L55) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, super.damage
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java#L65) **`onZapComplete()`**: 이벤트·효과 실행 / 참조 호출: zap, next
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java#L70) **`zap()`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: spend, GameScene.add, Blob.seed, setStrength
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java#L84) **`canVent(int target)`**: 조건 판정
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java#L89) **`getCloser(int target)`**: 조회·탐색
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java#L94) **`getFurther(int target)`**: 조회·탐색
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java#L99) **`rollToDropLoot()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.rollToDropLoot, Random.Int, Dungeon.level.drop, MetalShard, sprite.drop
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM201.java#L114) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: sprite.zap, zap, super.act

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 193. [`DM300.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 708행 / 타입 2개 / 필드 17개 / 메서드 30개.

### 타입·상속 선언

- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L79) `class DM300  extends Mob`
- [L687](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L687) `class FallingRockBuff  extends DelayedRockFall`

### 변수·상수 (단일 행 선언)

- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L108) `int pylonsActivated` 초기식: `0`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L109) `boolean supercharged` 초기식: `false`
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L110) `boolean chargeAnnounced` 초기식: `false`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L112) `int MIN_COOLDOWN` 초기식: `5`
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L115) `int turnsSinceLastAbility` 초기식: `-1`
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L118) `int lastAbility` 초기식: `0`
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L119) `int NONE` 초기식: `0`
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L120) `int GAS` 초기식: `1`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L121) `int ROCKS` 초기식: `2`
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L123) `String PYLONS_ACTIVATED` 초기식: `"pylons_activated"`
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L124) `String SUPERCHARGED` 초기식: `"supercharged"`
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L125) `String CHARGE_ANNOUNCED` 초기식: `"charge_announced"`
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L127) `String TURNS_SINCE_LAST_ABILITY` 초기식: `"turns_since_last_ability"`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L128) `String ABILITY_COOLDOWN` 초기식: `"ability_cooldown"`
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L130) `String LAST_ABILITY` 초기식: `"last_ability"`
- [L412](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L412) `int rockCenter`
- [L473](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L473) `boolean invulnWarned` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L94) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L99) **`attackSkill(Char target)`**: 전투 관련
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L104) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L116) **`NormalIntRange(MIN_COOLDOWN, MAX_COOLDOWN)`**: 개별 처리
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L133) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L144) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getBoolean, BossHealthBar.assignBoss, totalPylonsToActivate, BossHealthBar.bleed
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L160) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.act, Dungeon.level.length, Dungeon.level.updateFieldOfView, enemy.isAlive, Dungeon.level.adjacent, Dungeon.findStep, beckon, ConeAOE, Ballistica
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L305) **`attack(Char enemy, float dmgMulti, float dmgBonus, float accMulti)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attack
- [L313](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L313) **`chooseEnemy()`**: 개별 처리 / 조건 분기 / 참조 호출: super.chooseEnemy
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L322) **`move(int step, boolean travelling)`**: 개별 처리 / 조건 분기 / 참조 호출: super.move, PixelScene.shake, CavesBossLevel.PylonEnergy.volumeAt, buff, GLog.w, Messages.get, Sample.INSTANCE.play, sprite.emitter, start
- [L349](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L349) **`speed()`**: 개별 처리 / 참조 호출: super.speed
- [L354](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L354) **`notice()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.notice, BossHealthBar.isAssigned, BossHealthBar.assignBoss, yell, Messages.get, Actor.chars, sayBoss
- [L368](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L368) **`onZapComplete()`**: 이벤트·효과 실행 / 참조 호출: ventGas, next
- [L373](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L373) **`ventGas(Char target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.hero.interrupt, Ballistica, Dungeon.isChallenged, Actor.addDelayed, Actor, act, GameScene.add, Blob.seed, trajectory.subPath
- [L384](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L384) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: GameScene.add, Blob.seed, trajectory.subPath, Math.ceil, Actor.remove
- [L404](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L404) **`onSlamComplete()`**: 이벤트·효과 실행 / 참조 호출: dropRocks, next
- [L409](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L409) **`dropRocks(Char target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.hero.interrupt, Dungeon.level.adjacent, Ballistica, WandOfBlastWave.throwChar, trajectory.path.get, Math.min, Dungeon.level.distance, Random.Int, Blob.volumeAt
- [L476](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L476) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: BossHealthBar.isAssigned, notice, super.damage, isInvulnerable, src.getClass, Dungeon.hero.buff, isImmune, Dungeon.isChallenged, lock.addTime
- [L510](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L510) **`totalPylonsToActivate()`**: 개별 처리 / 참조 호출: Dungeon.isChallenged
- [L515](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L515) **`isInvulnerable(Class effect)`**: 조건 판정 / 조건 분기 / 참조 호출: GLog.w, Messages.get, super.isInvulnerable
- [L523](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L523) **`supercharge()`**: 개별 처리 / 참조 호출: activatePylon, spend, Dungeon.isChallenged, yell, Messages.get, sprite.showStatus, updateChargeState, charge
- [L537](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L537) **`isSupercharged()`**: 조건 판정
- [L541](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L541) **`loseSupercharge()`**: 개별 처리 / 조건 분기 / 참조 호출: updateChargeState, Math.min, totalPylonsToActivate, yell, Messages.get, BossHealthBar.bleed, Game.runOnRenderThread, Callback, call
- [L555](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L555) **`call()`**: 개별 처리 / 참조 호출: Music.INSTANCE.fadeOut, Callback, call, Music.INSTANCE.play
- [L558](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L558) **`call()`**: 개별 처리 / 참조 호출: Music.INSTANCE.play
- [L568](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L568) **`isAlive()`**: 조건 판정 / 참조 호출: super.isAlive, totalPylonsToActivate
- [L573](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L573) **`die(Object cause)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.die, GameScene.bossSlain, Dungeon.level.unseal, Random.chances, Random.Int, Dungeon.level.drop, MetalShard, sprite.drop, Badges.validateBossSlain
- [L605](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L605) **`getCloser(int target)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: super.getCloser, Dungeon.level.adjacent, Actor.findChar, Dungeon.level.trueDistance, Sample.INSTANCE.play, Dungeon.level.cellToPoint, CavesBossLevel.diggableArea.inside, Level.set, GameScene.updateMap
- [L666](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L666) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: super.description, Messages.get
- [L690](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM300.java#L690) **`affectChar(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.isChallenged, ch.damage, Random.NormalIntRange, ch.isAlive, Buff.prolong, Dungeon.fail, GLog.n, Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 194. [`DwarfKing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 812행 / 타입 8개 / 필드 20개 / 메서드 30개.

### 타입·상속 선언

- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L80) `class DwarfKing  extends Mob`
- [L604](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L604) `class DKGhoul  extends Ghoul`
- [L617](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L617) `class DKMonk  extends Monk`
- [L624](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L624) `class DKWarlock  extends Warlock`
- [L639](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L639) `class DKGolem  extends Golem`
- [L646](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L646) `class Summoning  extends Buff`
- [L770](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L770) `class KingDamager  extends Buff`
- [L797](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L797) `class DKBarrior  extends Barrier`

### 변수·상수 (단일 행 선언)

- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L108) `int phase` 초기식: `1`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L109) `int summonsMade` 초기식: `0`
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L111) `float summonCooldown` 초기식: `0`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L112) `float abilityCooldown` 초기식: `0`
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L116) `int lastAbility` 초기식: `0`
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L117) `int NONE` 초기식: `0`
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L118) `int LINK` 초기식: `1`
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L119) `int TELE` 초기식: `2`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L121) `String PHASE` 초기식: `"phase"`
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L122) `String SUMMONS_MADE` 초기식: `"summons_made"`
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L124) `String SUMMON_CD` 초기식: `"summon_cd"`
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L125) `String ABILITY_CD` 초기식: `"ability_cd"`
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L126) `String LAST_ABILITY` 초기식: `"last_ability"`
- [L648](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L648) `int delay`
- [L649](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L649) `int pos`
- [L650](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L650) `Class<?extends Mob> summon`
- [L652](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L652) `Emitter particles`
- [L749](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L749) `String DELAY` 초기식: `"delay"`
- [L750](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L750) `String POS` 초기식: `"pos"`
- [L751](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L751) `String SUMMON` 초기식: `"summon"`

### 함수·메서드 역할과 내부 연결

- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L94) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L99) **`attackSkill(Char target)`**: 전투 관련
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L104) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L129) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L139) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getFloat, properties.add, BossHealthBar.assignBoss, BossHealthBar.bleed
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L154) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: throwItems, summonSubject, Dungeon.isChallenged, Random.NormalIntRange, spend, Random.Int, lifeLinkSubject, teleportSubject, sprite.centerEmitter
- [L303](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L303) **`summonSubject(int delay)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.isChallenged, summonSubject, Random.Int
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L327) **`summonSubject(int delay, Class<?extends Mob> type)`**: 개별 처리 / 조건 분기 / 참조 호출: Summoning, getSummoningPos, s.attachTo
- [L337](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L337) **`getSubjects()`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: subjects.add
- [L347](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L347) **`lifeLinkSubject()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: getSubjects, m.buffs, id, Dungeon.level.distance, Buff.append, furthest.id, yell, Messages.get, Random.IntRange
- [L374](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L374) **`teleportSubject()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: getSubjects, Dungeon.level.distance, Ballistica, trajectory.path.get, Actor.findChar, Dungeon.level.trueDistance, Actor.add, Pushing, ScrollOfTeleportation.appear
- [L433](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L433) **`notice()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.notice, BossHealthBar.isAssigned, BossHealthBar.assignBoss, yell, Messages.get, Actor.chars, sayBoss
- [L447](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L447) **`isInvulnerable(Class effect)`**: 조건 판정 / 조건 분기 / 참조 호출: super.isInvulnerable
- [L456](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L456) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: RingOfForce.fightingUnarmed, Dungeon.hero.buff, isInvulnerable, src.getClass, super.damage, Buff.affect, deferred.extend, sprite.showStatus, Messages.get
- [L528](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L528) **`call()`**: 개별 처리 / 참조 호출: Music.INSTANCE.fadeOut, Callback, call, Music.INSTANCE.play
- [L531](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L531) **`call()`**: 개별 처리 / 참조 호출: Music.INSTANCE.play
- [L543](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L543) **`isAlive()`**: 조건 판정 / 참조 호출: super.isAlive
- [L548](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L548) **`die(Object cause)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: GameScene.bossSlain, super.die, level.heaps.get, Dungeon.level.drop, Dungeon.level.width, h.destroy, KingsCrown, sprite.drop, Badges.validateBossSlain
- [L596](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L596) **`isImmune(Class effect)`**: 조건 판정 / 조건 분기 / 참조 호출: buff, super.isImmune
- [L611](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L611) **`act()`**: 시간·상태 갱신 / 참조 호출: super.act
- [L631](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L631) **`zap()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.zap
- [L654](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L654) **`getPos()`**: 조회·탐색
- [L659](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L659) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: particles.burst, Sample.INSTANCE.play, Speck.factory, Actor.findChar, candidates.add, candidates.isEmpty, Random.element, die, Reflection.newInstance
- [L730](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L730) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: CellEmitter.get, particles.pour, Speck.factory
- [L754](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L754) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L762](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L762) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getClass
- [L777](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L777) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: detach, spend
- [L786](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L786) **`detach()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.detach, Dungeon.isChallenged, m.damage
- [L800](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L800) **`act()`**: 시간·상태 갱신 / 참조 호출: incShield, super.act
- [L806](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java#L806) **`icon()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 195. [`EbonyMimic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/EbonyMimic.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 122행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/EbonyMimic.java#L44) `class EbonyMimic  extends Mimic`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/EbonyMimic.java#L51) **`name()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, super.name
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/EbonyMimic.java#L60) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, super.description
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/EbonyMimic.java#L69) **`stealthy()`**: 개별 처리
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/EbonyMimic.java#L73) **`stopHiding()`**: 개별 처리 / 조건 분기 / 참조 호출: sprite.idle, Actor.chars, contains, GLog.w, Messages.get, CellEmitter.get, burst, Speck.factory, Sample.INSTANCE.play
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/EbonyMimic.java#L89) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: Math.round, super.damageRoll
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/EbonyMimic.java#L98) **`generatePrize(boolean useDecks)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.generatePrize, items.add, Generator.randomUsingDefaults, hasCurseEnchant, enchant, hasCurseGlyph, inscribe, i.level, i.upgrade

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 196. [`Elemental.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 620행 / 타입 7개 / 필드 5개 / 메서드 43개.

### 타입·상속 선언

- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L68) `class Elemental  extends Mob`
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L227) `class FireElemental  extends Elemental`
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L260) `class NewbornFireElemental  extends FireElemental`
- [L470](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L470) `class AllyNewBornElemental  extends NewbornFireElemental`
- [L480](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L480) `class FrostElemental  extends Elemental`
- [L508](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L508) `class ShockElemental  extends Elemental`
- [L558](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L558) `class ChaosElemental  extends Elemental`

### 변수·상수 (단일 행 선언)

- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L80) `boolean summonedALly`
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L205) `String COOLDOWN` 초기식: `"cooldown"`
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L206) `String SUMMONED_ALLY` 초기식: `"summoned_ally"`
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L270) `int targetingPos` 초기식: `-1`
- [L454](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L454) `String TARGETING_POS` 초기식: `"targeting_pos"`

### 함수·메서드 역할과 내부 연결

- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L83) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: Random.NormalIntRange, Math.max, Dungeon.scalingDepth
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L93) **`attackSkill(Char target)`**: 전투 관련 / 조건 분기 / 참조 호출: Math.max, Dungeon.scalingDepth
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L102) **`setSummonedALly()`**: 상태 갱신 / 참조 호출: Math.max, Dungeon.scalingDepth
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L111) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L115) **`NormalIntRange(3, 5)`**: 개별 처리
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L118) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.act
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L127) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L133) **`canAttack(Char enemy)`**: 조건 판정 / 조건 분기 / 참조 호출: super.canAttack, Ballistica
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L141) **`doAttack(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, Ballistica, super.doAttack, sprite.zap, zap
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L162) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 참조 호출: super.attackProc, meleeProc
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L169) **`zap()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: spend, Invisibility.dispel, hit, rangedProc, enemy.sprite.showStatus, enemy.defenseVerb, Random.NormalIntRange
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L185) **`onZapComplete()`**: 이벤트·효과 실행 / 참조 호출: zap, next
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L191) **`add(Buff buff)`**: 상태 갱신 / 조건 분기 / 참조 호출: harmfulBuffs.contains, buff.getClass, damage, Random.NormalIntRange, super.add
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L200) **`meleeProc(Char enemy, int damage)`**: 개별 처리
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L201) **`rangedProc(Char enemy)`**: 개별 처리
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L209) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L216) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, bundle.getInt, bundle.getBoolean, setSummonedALly
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L242) **`meleeProc(Char enemy, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int, Buff.affect, reignite, Splash.at, enemy.sprite.center, sprite.blood
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L250) **`rangedProc(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.affect, reignite, Splash.at, enemy.sprite.center, sprite.blood
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L273) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Ballistica, sprite.zap, zap, super.act
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L296) **`canAttack(Char enemy)`**: 조건 판정 / 조건 분기 / 참조 호출: super.canAttack, Ballistica
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L304) **`doAttack(Char enemy)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.doAttack, Ballistica, candidates.add, candidates.isEmpty, Random.element, GameMath.gate, attackDelay, Math.ceil, Dungeon.hero.cooldown
- [L356](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L356) **`zap()`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: spend, Invisibility.dispel, CellEmitter.get, burst, GameScene.add, Blob.seed, Actor.findChar, Buff.affect, reignite
- [L388](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L388) **`attackSkill(Char target)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackSkill
- [L397](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L397) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: Random.NormalIntRange, super.damageRoll
- [L406](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L406) **`meleeProc(Char enemy, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: super.meleeProc
- [L414](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L414) **`die(Object cause)`**: 개별 처리 / 조건 분기 / 참조 호출: super.die, Dungeon.level.drop, Embers, sprite.drop, Game.runOnRenderThread, Callback, call, Music.INSTANCE.fadeOut, Dungeon.level.playLevelMusic
- [L422](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L422) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Music.INSTANCE.fadeOut, Callback, call, Dungeon.level.playLevelMusic
- [L425](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L425) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.playLevelMusic
- [L437](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L437) **`reset()`**: 생성·초기화
- [L442](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L442) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: super.description, Messages.get
- [L457](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L457) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L463](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L463) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L494](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L494) **`meleeProc(Char enemy, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int, Freezing.freeze, Splash.at, enemy.sprite.center, sprite.blood
- [L502](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L502) **`rangedProc(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: Freezing.freeze, Splash.at, enemy.sprite.center, sprite.blood
- [L520](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L520) **`meleeProc(Char enemy, int damage)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Shocking.arc, affected.remove, ch.damage, Math.round, Shocking, ch.isAlive, Badges.validateDeathFromEnemyMagic, Dungeon.fail, GLog.n
- [L550](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L550) **`rangedProc(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.affect, GameScene.flash
- [L568](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L568) **`meleeProc(Char enemy, int damage)`**: 개별 처리 / 참조 호출: Ballistica, CursedWand.randomValidEffect, effect
- [L576](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L576) **`zap()`**: 이벤트·효과 실행 / 참조 호출: spend, Invisibility.dispel, rangedProc, Random.NormalIntRange
- [L588](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L588) **`onZapComplete()`**: 이벤트·효과 실행 / 참조 호출: zap
- [L594](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L594) **`rangedProc(Char enemy)`**: 개별 처리 / 참조 호출: CursedWand.cursedZap, Ballistica, Callback, call, next
- [L597](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L597) **`call()`**: 개별 처리 / 참조 호출: next
- [L604](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java#L604) **`random()`**: 개별 처리 / 조건 분기 / 참조 호출: RatSkull.exoticChanceMultiplier, Random.Float

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 197. [`Eye.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 287행 / 타입 3개 / 필드 7개 / 메서드 13개.

### 타입·상속 선언

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L48) `class Eye  extends Mob`
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L165) `class DeathGaze`
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L275) `class Hunting  extends Mob.Hunting`

### 변수·상수 (단일 행 선언)

- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L85) `Ballistica beam`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L86) `int beamTarget` 초기식: `-1`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L87) `int beamCooldown`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L88) `boolean beamCharged`
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L248) `String BEAM_TARGET` 초기식: `"beamTarget"`
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L249) `String BEAM_COOLDOWN` 초기식: `"beamCooldown"`
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L250) `String BEAM_CHARGED` 초기식: `"beamCharged"`

### 함수·메서드 역할과 내부 연결

- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L71) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L76) **`attackSkill(Char target)`**: 전투 관련
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L81) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L91) **`canAttack(Char enemy)`**: 조건 판정 / 조건 분기 / 참조 호출: Ballistica, isCharmedBy, super.canAttack, aim.subPath, contains
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L111) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: sprite.idle, Ballistica, sprite.turnTo, super.act
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L126) **`doAttack(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: Ballistica, beam.subPath, contains, super.doAttack, charge, spend, attackDelay, sprite.zap, sprite.idle
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L153) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: super.damage
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L159) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L167) **`deathGaze()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Random.IntRange, Invisibility.dispel, beam.subPath, Dungeon.level.destroy, GameScene.updateMap, Actor.findChar, hit, Random.NormalIntRange, Math.round
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L223) **`createLoot()`**: 생성·초기화 / 조건 분기·반복·상태 선택 / 참조 호출: Random.Int, Dewdrop, level.heaps.get, Dungeon.level.drop, sprite.drop, Generator.randomUsingDefaults
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L253) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L261) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, bundle.getInt, bundle.getBoolean
- [L277](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Eye.java#L277) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: canAttack, doAttack, super.act

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 198. [`FetidRat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FetidRat.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 111행 / 타입 2개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FetidRat.java#L37) `class FetidRat  extends Rat`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FetidRat.java#L93) `class Wandering  extends Mob.Wandering`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FetidRat.java#L55) **`attackSkill(Char target)`**: 전투 관련
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FetidRat.java#L60) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FetidRat.java#L65) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, Random.Int, Buff.affect, set
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FetidRat.java#L79) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 참조 호출: GameScene.add, Blob.seed, super.defenseProc
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FetidRat.java#L87) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die, Ghost.Quest.process
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FetidRat.java#L95) **`randomDestination()`**: 개별 처리 / 조건 분기 / 참조 호출: super.randomDestination, PathFinder.buildDistanceMap

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 199. [`FungalCore.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalCore.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 57행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalCore.java#L27) `class FungalCore  extends Mob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalCore.java#L42) **`reset()`**: 생성·초기화
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalCore.java#L47) **`spawningWeight()`**: 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalCore.java#L52) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die, Blacksmith.Quest.beatBoss

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 200. [`FungalSentry.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 123행 / 타입 2개 / 필드 0개 / 메서드 10개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java#L32) `class FungalSentry  extends Mob`
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java#L99) `class Waiting  extends Mob.Wandering`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java#L50) **`reset()`**: 생성·초기화
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java#L55) **`spawningWeight()`**: 개별 처리
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java#L60) **`getCloser(int target)`**: 조회·탐색
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java#L65) **`getFurther(int target)`**: 조회·탐색
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java#L70) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java#L76) **`canAttack(Char enemy)`**: 조건 판정 / 참조 호출: super.canAttack, Ballistica
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java#L84) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 참조 호출: Buff.affect, extend, super.attackProc
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java#L90) **`attackSkill(Char target)`**: 전투 관련
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java#L102) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: noticeEnemy, continueWandering
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSentry.java#L116) **`noticeEnemy()`**: 개별 처리 / 참조 호출: spend, super.noticeEnemy

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 201. [`FungalSpinner.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSpinner.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 75행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSpinner.java#L33) `class FungalSpinner  extends Spinner`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSpinner.java#L46) **`applyWebToCell(int cell)`**: 개별 처리 / 참조 호출: GameScene.add, Blob.seed
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSpinner.java#L51) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: Math.round, super.damage
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FungalSpinner.java#L66) **`attackProc(Char enemy, int damage)`**: 전투 관련

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 202. [`Ghoul.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 378행 / 타입 4개 / 필드 9개 / 메서드 21개.

### 타입·상속 선언

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L43) `class Ghoul  extends Mob`
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L198) `class Sleeping  extends Mob.Sleeping`
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L212) `class Wandering  extends Mob.Wandering`
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L235) `class GhoulLifeLink  extends Buff`

### 변수·상수 (단일 행 선언)

- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L84) `int timesDowned` 초기식: `0`
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L85) `int partnerID` 초기식: `-1`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L87) `String PARTNER_ID` 초기식: `"partner_id"`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L88) `String TIMES_DOWNED` 초기식: `"times_downed"`
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L150) `boolean beingLifeLinked` 초기식: `false`
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L237) `Ghoul ghoul`
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L238) `int turnsToRevive`
- [L340](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L340) `String GHOUL` 초기식: `"ghoul"`
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L341) `String LEFT` 초기식: `"left"`

### 함수·메서드 역할과 내부 연결

- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L65) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L70) **`attackSkill(Char target)`**: 전투 관련
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L75) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L80) **`spawningWeight()`**: 개별 처리
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L91) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L98) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L105) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.width, Actor.findChar, Char.hasProp, candidates.add, candidates.isEmpty, Ghoul, this.id, child.id, Random.element
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L153) **`die(Object cause)`**: 개별 처리 / 조건 분기 / 참조 호출: GhoulLifeLink.searchForHost, Actor.remove, level.mobs.remove, Buff.append, set, crumple, super.die
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L171) **`isAlive()`**: 조건 판정 / 참조 호출: super.isAlive
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L176) **`isActive()`**: 조건 판정 / 참조 호출: isAlive
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L181) **`onRemove()`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: buffs, Buff.prolong, buff.detach, super.onRemove
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L200) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Actor.findById, super.act
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L215) **`continueWandering()`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findById, Dungeon.level.distance, getCloser, spend, speed, moveSprite, super.continueWandering
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L241) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: detach, Dungeon.level.length, Dungeon.level.updateFieldOfView, Dungeon.level.distance, super.detach, ghoul.die, target.buff, Actor.findChar, Char.hasProp
- [L308](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L308) **`updateVisibility()`**: 시간·상태 갱신 / 조건 분기
- [L314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L314) **`set(int turns, Ghoul ghoul)`**: 상태 갱신
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L320) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.addSprite, crumple
- [L328](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L328) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: super.detach, searchForHost, attachTo, timeToNow, ghoul.die
- [L344](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L344) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L351](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L351) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.get, bundle.getInt
- [L358](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java#L358) **`searchForHost(Ghoul dieing)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: Actor.chars, ch.buff, Dungeon.level.length, Dungeon.level.updateFieldOfView, Dungeon.level.distance

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 203. [`Gnoll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Gnoll.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 59행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Gnoll.java#L29) `class Gnoll  extends Mob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Gnoll.java#L45) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Gnoll.java#L50) **`attackSkill(Char target)`**: 전투 관련
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Gnoll.java#L55) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 204. [`GnollExile.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 207행 / 타입 3개 / 필드 2개 / 메서드 11개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L41) `class GnollExile  extends Gnoll`
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L146) `class Passive  extends Mob.Wandering`
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L198) `class Wandering  extends Mob.Wandering`

### 변수·상수 (단일 행 선언)

- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L143) `int seenNotifyCooldown` 초기식: `0`
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L183) `String SEEN_NOTIF_CD` 초기식: `"seen_notif_cd"`

### 함수·메서드 역할과 내부 연결

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L60) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L65) **`attackSkill(Char target)`**: 전투 관련
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L70) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L75) **`canAttack(Char enemy)`**: 조건 판정 / 조건 분기·반복 / 참조 호출: Dungeon.level.adjacent, Dungeon.level.distance, BArray.not, Actor.chars, PathFinder.buildDistanceMap, super.canAttack
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L99) **`rollToDropLoot()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.rollToDropLoot, items.add, Generator.randomUsingDefaults, Random.Int, Dungeon.level.drop, sprite.drop
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L121) **`beckon(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: super.beckon
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L133) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: super.description, Messages.get
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L149) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: buffs, GLog.p, Messages.get, GLog.w, noticeEnemy, continueWandering
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L186) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L192) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollExile.java#L200) **`noticeEnemy()`**: 개별 처리 / 참조 호출: GLog.w, Messages.get, super.noticeEnemy

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 205. [`GnollGeomancer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 918행 / 타입 6개 / 필드 15개 / 메서드 39개.

### 타입·상속 선언

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L66) `class GnollGeomancer  extends Mob`
- [L554](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L554) `class Sleeping  extends Mob.Sleeping`
- [L562](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L562) `class Hunting  extends Mob.Hunting`
- [L764](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L764) `class Boulder  extends Item`
- [L836](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L836) `class GnollRockFall  extends DelayedRockFall`
- [L864](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L864) `class RockArmor  extends ShieldBuff`

### 변수·상수 (단일 행 선언)

- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L91) `boolean lastAbilityWasRockfall`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L93) `int[] throwingRocksFromPos` 초기식: `null`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L94) `int throwingRockToPos` 초기식: `-1`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L96) `int sapperID` 초기식: `-1`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L97) `int[] sapperSpawns` 초기식: `null`
- [L297](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L297) `boolean inFinalBracket` 초기식: `false`
- [L697](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L697) `int rocksInFlight` 초기식: `0`
- [L772](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L772) `int rockCenter` 초기식: `target.pos`
- [L866](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L866) `String HITS` 초기식: `"hits"`
- [L868](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L868) `String ABILITY_COOLDOWN` 초기식: `"ability_cooldown"`
- [L869](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L869) `String LAST_ABILITY_WAS_ROCKFALL` 초기식: `"last_ability_was_rockfall"`
- [L871](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L871) `String ROCK_FROM_POS` 초기식: `"rock_from_pos"`
- [L872](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L872) `String ROCK_TO_POS` 초기식: `"rock_to_pos"`
- [L874](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L874) `String SAPPER_ID` 초기식: `"sapper_id"`
- [L875](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L875) `String SAPPER_SPAWNS` 초기식: `"sapper_spawns"`

### 함수·메서드 역할과 내부 연결

- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L90) **`NormalIntRange(3, 5)`**: 개별 처리
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L100) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: GnollGeomancer.doRockThrowAttack, spend, super.act
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L134) **`isInvulnerable(Class effect)`**: 조건 판정 / 참조 호출: super.isInvulnerable, buff, hasSapper
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L141) **`add(Buff buff)`**: 상태 갱신 / 조건 분기 / 참조 호출: super.add
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L151) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L156) **`attackSkill(Char target)`**: 전투 관련
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L161) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L166) **`reset()`**: 생성·초기화
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L171) **`spawningWeight()`**: 개별 처리
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L176) **`heroShouldInteract()`**: 개별 처리 / 참조 호출: super.heroShouldInteract, buff
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L181) **`getCloser(int target)`**: 조회·탐색
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L186) **`getFurther(int target)`**: 조회·탐색
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L193) **`interact(Char c)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: buff, super.interact, hero.belongings.getItem, hero.sprite.attack, Callback, call, p.damageRoll, Math.min, shielding
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L197) **`getItem(Pickaxe.class)`**: 조회·탐색
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L205) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: p.damageRoll, Math.min, buff, shielding, damage, sprite.bloodBurstA, hero.sprite.center, sprite.flash, GLog.w
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L269) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: super.damage, BossHealthBar.bleed, carveRockAndDash, Buff.affect, setShield
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L300) **`isAlive()`**: 조건 판정 / 참조 호출: super.isAlive
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L305) **`linkSapper(GnollSapper sapper)`**: 개별 처리 / 조건 분기 / 참조 호출: sapper.id, setupArmor
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L312) **`hasSapper()`**: 조건 판정 / 참조 호출: Actor.findById, isAlive
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L318) **`loseSapper()`**: 개별 처리 / 조건 분기 / 참조 호출: loseArmor
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L327) **`carveRockAndDash()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.distance, Dungeon.level.trueDistance, Ballistica, path.path.get, Actor.findChar, level.traps.get, candidates.add, candidates.isEmpty, Random.element
- [L487](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L487) **`spreadDiamondAOE(ArrayList<Integer> currentCells)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.insideMap, spreadCells.contains, currentCells.contains, spreadCells.add
- [L500](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L500) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, super.description, buff, hasSapper
- [L517](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L517) **`die(Object cause)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.die, Blacksmith.Quest.beatBoss, Sample.INSTANCE.playDelayed, PixelScene.shake, GameScene.bossSlain, Game.runOnRenderThread, Callback, call, Music.INSTANCE.fadeOut
- [L526](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L526) **`call()`**: 개별 처리 / 참조 호출: Music.INSTANCE.fadeOut, Callback, call, Music.INSTANCE.end
- [L529](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L529) **`call()`**: 개별 처리 / 참조 호출: Music.INSTANCE.end
- [L546](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L546) **`beckon(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: super.beckon
- [L557](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L557) **`awaken(boolean enemyInFOV)`**: 개별 처리
- [L565](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L565) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: chooseEnemy, act, spend, Dungeon.level.distance, hasSapper, buff, enemy.buff, Actor.findById, aggro
- [L657](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L657) **`prepRockThrowAttack(Char target, Char source)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.length, Ballistica, candidateRocks.add, Actor.chars, candidateRocks.remove, candidateRocks.isEmpty, candidateRocks.get, Dungeon.level.trueDistance
- [L700](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L700) **`doRockThrowAttack(Char source, int from, int to)`**: 개별 처리 / 조건 분기 / 참조 호출: Level.set, GameScene.updateMap, source.sprite.attack, Callback, call, source.sprite.idle, Ballistica, Sample.INSTANCE.play, sprite.parent.recycle
- [L706](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L706) **`call()`**: 개별 처리 / 참조 호출: source.sprite.idle
- [L718](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L718) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Splash.at, Sample.INSTANCE.play, Actor.findChar, PixelScene.shake, ch.damage, Random.NormalIntRange, GnollGeomancer.Boulder, ch.isAlive, Buff.prolong
- [L771](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L771) **`prepRockFallAttack(Char target, Char source, int range, boolean avoidBarricades)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Random.Int, level.traps.containsKey, Dungeon.level.width, Dungeon.level.insideMap, Actor.findChar, Dungeon.level.distance, rockCells.add, GameMath.gate, Math.ceil
- [L827](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L827) **`call()`**: 개별 처리 / 참조 호출: source.sprite.idle
- [L839](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L839) **`affectChar(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: ch.damage, Random.NormalIntRange, ch.isAlive, Buff.prolong, Dungeon.fail, GLog.n, Messages.get
- [L853](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L853) **`affectCell(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, Dungeon.level.entrance, Random.Int, Level.set, GameScene.updateMap
- [L878](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L878) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L897](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java#L897) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getBoolean, bundle.contains, bundle.getIntArray, BossHealthBar.assignBoss

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 206. [`GnollGuard.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 165행 / 타입 2개 / 필드 2개 / 메서드 14개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L35) `class GnollGuard  extends Mob`
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L153) `class Wandering  extends Mob.Wandering`

### 변수·상수 (단일 행 선언)

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L52) `int sapperID` 초기식: `-1`
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L139) `String SAPPER_ID` 초기식: `"sapper_id"`

### 함수·메서드 역할과 내부 연결

- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L54) **`linkSapper(GnollSapper sapper)`**: 개별 처리 / 조건 분기 / 참조 호출: sapper.id, setupArmor
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L61) **`hasSapper()`**: 조건 판정 / 참조 호출: Actor.findById, isAlive
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L67) **`loseSapper()`**: 개별 처리 / 조건 분기 / 참조 호출: loseArmor
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L77) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: hasSapper, super.damage
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L83) **`incomingDOT()`**: 개별 처리 / 조건 분기 / 참조 호출: super.incomingDOT, hasSapper
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L95) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, Random.NormalIntRange
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L104) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, Dungeon.level.adjacent, GLog.n, Messages.get
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L113) **`attackSkill(Char target)`**: 전투 관련
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L118) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L123) **`canAttack(Char enemy)`**: 조건 판정 / 참조 호출: Dungeon.level.distance, Ballistica
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L131) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: hasSapper, super.description, Messages.get
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L142) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L148) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGuard.java#L155) **`randomDestination()`**: 개별 처리 / 조건 분기 / 참조 호출: hasSapper, Actor.findById, super.randomDestination

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 207. [`GnollSapper.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 272행 / 타입 3개 / 필드 11개 / 메서드 16개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L37) `class GnollSapper  extends Mob`
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L150) `class Hunting  extends Mob.Hunting`
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L230) `class Wandering  extends Mob.Wandering`

### 변수·상수 (단일 행 선언)

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L58) `int spawnPos`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L59) `int partnerID` 초기식: `-1`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L62) `boolean lastAbilityWasRockfall` 초기식: `false`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L64) `int throwingRockFromPos` 초기식: `-1`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L65) `int throwingRockToPos` 초기식: `-1`
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L237) `String SPAWN_POS` 초기식: `"spawn_pos"`
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L238) `String PARTNER_ID` 초기식: `"partner_id"`
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L240) `String ABILITY_COOLDOWN` 초기식: `"ability_cooldown"`
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L241) `String LAST_ABILITY_WAS_ROCKFALL` 초기식: `"last_ability_was_rockfall"`
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L243) `String ROCK_FROM_POS` 초기식: `"rock_from_pos"`
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L244) `String ROCK_TO_POS` 초기식: `"rock_to_pos"`

### 함수·메서드 역할과 내부 연결

- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L61) **`NormalIntRange(4, 6)`**: 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L67) **`linkPartner(Char c)`**: 개별 처리 / 조건 분기 / 참조 호출: losePartner, c.id, linkSapper
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L77) **`losePartner()`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findById, loseSapper
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L88) **`getPartner()`**: 조회·탐색 / 참조 호출: Actor.findById
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L93) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die, losePartner
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L99) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L104) **`attackSkill(Char target)`**: 전투 관련
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L109) **`damage(int dmg, Object src)`**: 전투 관련 / 참조 호출: super.damage
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L115) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L120) **`reset()`**: 생성·초기화
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L125) **`spawningWeight()`**: 개별 처리
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L130) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: GnollGeomancer.doRockThrowAttack, spend, super.act
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L152) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.distance, super.act, getPartner, losePartner, Actor.findById, partner.notice, partner.aggro, GnollGeomancer.prepRockThrowAttack, Random.Int
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L232) **`randomDestination()`**: 개별 처리
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L247) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollSapper.java#L260) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getBoolean

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":48,"fields":89,"methods":257}

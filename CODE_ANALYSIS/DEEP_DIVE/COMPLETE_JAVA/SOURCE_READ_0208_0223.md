# Java 파일별 소스 구현 해설 208–223

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 208. [`GnollTrickster.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 177행 / 타입 2개 / 필드 2개 / 메서드 10개.

### 타입·상속 선언

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L43) `class GnollTrickster  extends Gnoll`
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L147) `class Wandering  extends Mob.Wandering`

### 변수·상수 (단일 행 선언)

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L63) `int combo` 초기식: `0`
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L162) `String COMBO` 초기식: `"combo"`

### 함수·메서드 역할과 내부 연결

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L66) **`attackSkill(Char target)`**: 전투 관련
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L71) **`canAttack(Char enemy)`**: 조건 판정 / 참조 호출: Dungeon.level.adjacent, super.canAttack, Ballistica
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L77) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, Random.Int, enemy.buff, GameScene.add, Blob.seed, Buff.affect, reignite, set
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L107) **`getCloser(int target)`**: 조회·탐색 / 조건 분기 / 참조 호출: getFurther, super.getCloser
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L117) **`aggro(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.length, super.aggro
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L127) **`createLoot()`**: 생성·초기화 / 조건 분기 / 참조 호출: super.createLoot, drop.level, drop.hasCurseEnchant, drop.enchant, drop.identify, drop.quantity
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L141) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die, Ghost.Quest.process
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L149) **`randomDestination()`**: 개별 처리 / 조건 분기 / 참조 호출: super.randomDestination, PathFinder.buildDistanceMap
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L165) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L171) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 209. [`GoldenMimic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GoldenMimic.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 110행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GoldenMimic.java#L44) `class GoldenMimic  extends Mimic`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GoldenMimic.java#L51) **`name()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, super.name
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GoldenMimic.java#L60) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: MimicTooth.stealthyMimics, Messages.get, super.description
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GoldenMimic.java#L72) **`stopHiding()`**: 개별 처리 / 조건 분기 / 참조 호출: sprite.idle, Actor.chars, contains, GLog.w, Messages.get, CellEmitter.get, burst, Speck.factory, Sample.INSTANCE.play
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GoldenMimic.java#L85) **`setLevel(int level)`**: 상태 갱신 / 참조 호출: super.setLevel, Math.round
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GoldenMimic.java#L90) **`generatePrize(boolean useDecks)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.generatePrize, hasCurseEnchant, enchant, hasCurseGlyph, inscribe, i.level, Random.Int, i.upgrade

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 210. [`Golem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 258행 / 타입 3개 / 필드 6개 / 메서드 14개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L40) `class Golem  extends Mob`
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L185) `class Wandering  extends Mob.Wandering`
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L208) `class Hunting  extends Mob.Hunting`

### 변수·상수 (단일 행 선언)

- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L99) `boolean teleporting` 초기식: `false`
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L100) `int selfTeleCooldown` 초기식: `0`
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L101) `int enemyTeleCooldown` 초기식: `0`
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L103) `String TELEPORTING` 초기식: `"teleporting"`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L104) `String SELF_COOLDOWN` 초기식: `"self_cooldown"`
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L105) `String ENEMY_COOLDOWN` 초기식: `"enemy_cooldown"`

### 함수·메서드 역할과 내부 연결

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L62) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L67) **`attackSkill(Char target)`**: 전투 관련
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L72) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L77) **`lootChance()`**: 개별 처리 / 참조 호출: super.lootChance, Math.pow
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L84) **`rollToDropLoot()`**: 개별 처리 / 참조 호출: Imp.Quest.oldProcess, super.rollToDropLoot
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L89) **`createLoot()`**: 생성·초기화 / 조건 분기 / 참조 호출: Generator.randomWeapon, Generator.randomArmor
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L108) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L116) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getBoolean, bundle.getInt
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L124) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: teleParticles, Actor.findChar, ScrollOfTeleportation.appear, Dungeon.level.randomDestination, spend, super.act
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L142) **`onZapComplete()`**: 이벤트·효과 실행 / 참조 호출: teleportEnemy, next
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L147) **`teleportEnemy()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: spend, Actor.findChar, Dungeon.level.trueDistance, enemy.buff, ScrollOfTeleportation.appear, interrupt, Dungeon.observe, GameScene.updateFog
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L175) **`canTele(int target)`**: 조건 판정 / 조건 분기 / 참조 호출: PathFinder.buildDistanceMap, BArray.not, Dungeon.level.distance
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L188) **`continueWandering()`**: 개별 처리 / 조건 분기 / 참조 호출: getCloser, spend, speed, moveSprite, Dungeon.bossLevel, teleParticles, randomDestination
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Golem.java#L211) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: canAttack, super.act, handleRecentAttackers, act, distance, Random.Int, Char.hasProp, canTele, sprite.zap

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 211. [`Goo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 351행 / 타입 1개 / 필드 4개 / 메서드 17개.

### 타입·상속 선언

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L51) `class Goo  extends Mob`

### 변수·상수 (단일 행 선언)

- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L64) `int pumpedUp` 초기식: `0`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L65) `int healInc` 초기식: `1`
- [L326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L326) `String PUMPEDUP` 초기식: `"pumpedup"`
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L327) `String HEALINC` 초기식: `"healinc"`

### 함수·메서드 역할과 내부 연결

- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L68) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: Random.NormalIntRange
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L84) **`attackSkill(Char target)`**: 전투 관련 / 조건 분기
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L92) **`defenseSkill(Char enemy)`**: 전투 관련 / 참조 호출: super.defenseSkill
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L97) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L102) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: sprite.idle, Dungeon.hero.buff, Dungeon.isChallenged, lock.removeTime, sprite.showStatusWithIcon, Integer.toString, BossHealthBar.bleed, spray, Math.min
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L142) **`canAttack(Char enemy)`**: 조건 판정 / 조건 분기 / 참조 호출: Dungeon.level.distance, Ballistica, super.canAttack
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L155) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, Random.Int, Buff.affect, set, enemy.sprite.burst, PixelScene.shake
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L170) **`updateSpriteState()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.updateSpriteState, pumpUp
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L179) **`doAttack(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: pumpUp, spend, attackDelay, Random.Int, pumpAttack, sprite.attack, triggerEmitters, attack, Invisibility.dispel
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L231) **`attack(Char enemy, float dmgMulti, float dmgBonus, float accMulti)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attack
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L244) **`getCloser(int target)`**: 조회·탐색 / 조건 분기 / 참조 호출: sprite.idle, super.getCloser
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L253) **`getFurther(int target)`**: 조회·탐색 / 조건 분기 / 참조 호출: sprite.idle, super.getFurther
- [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L262) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: BossHealthBar.isAssigned, BossHealthBar.assignBoss, Dungeon.level.seal, super.damage, BossHealthBar.bleed, sprite.showStatus, Messages.get, spray, yell
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L283) **`die(Object cause)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.die, Dungeon.level.unseal, GameScene.bossSlain, Dungeon.level.drop, WornKey, sprite.drop, Random.chances, Random.Int, GooBlob
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L312) **`notice()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.notice, BossHealthBar.isAssigned, BossHealthBar.assignBoss, Dungeon.level.seal, yell, Messages.get, Actor.chars, sayBoss
- [L330](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L330) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L339](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L339) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt, BossHealthBar.assignBoss, BossHealthBar.bleed

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 212. [`GreatCrab.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GreatCrab.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 136행 / 타입 2개 / 필드 1개 / 메서드 5개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GreatCrab.java#L40) `class GreatCrab  extends Crab`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GreatCrab.java#L121) `class Wandering  extends Mob.Wandering`

### 변수·상수 (단일 행 선언)

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GreatCrab.java#L60) `int moving` 초기식: `0`

### 함수·메서드 역할과 내부 연결

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GreatCrab.java#L63) **`getCloser(int target)`**: 조회·탐색 / 조건 분기 / 참조 호출: super.getCloser
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GreatCrab.java#L76) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: GLog.n, Messages.get, sprite.showStatus, Sample.INSTANCE.play, Random.Float, super.damage
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GreatCrab.java#L95) **`defenseSkill(Char enemy)`**: 전투 관련 / 조건 분기 / 참조 호출: Sample.INSTANCE.play, Random.Float, GLog.n, Messages.get, super.defenseSkill
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GreatCrab.java#L115) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die, Ghost.Quest.process
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GreatCrab.java#L123) **`randomDestination()`**: 개별 처리 / 조건 분기 / 참조 호출: super.randomDestination, PathFinder.buildDistanceMap

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 213. [`Guard.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 193행 / 타입 2개 / 필드 3개 / 메서드 12개.

### 타입·상속 선언

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L43) `class Guard  extends Mob`
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L174) `class Hunting  extends Mob.Hunting`

### 변수·상수 (단일 행 선언)

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L46) `boolean chainsUsed` 초기식: `false`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L94) `int newPosFinal` 초기식: `newPos`
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L160) `String CHAINSUSED` 초기식: `"chainsused"`

### 함수·메서드 역할과 내부 연결

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L66) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L70) **`chain(int target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: enemy.properties, contains, Ballistica, chain.path.size, chain.path.get, chain.subPath, Actor.findChar, Char.hasProp, yell
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L105) **`call()`**: 개별 처리 / 참조 호출: Actor.add, Pushing, Callback, call, pullEnemy, next
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L107) **`call()`**: 개별 처리 / 참조 호출: pullEnemy
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L123) **`pullEnemy(Char enemy, int pullPos)`**: 개별 처리 / 조건 분기 / 참조 호출: enemy.sprite.place, Dungeon.level.occupyCell, Cripple.prolong, Dungeon.hero.interrupt, Dungeon.observe, GameScene.updateFog
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L138) **`attackSkill(Char target)`**: 전투 관련
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L143) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L148) **`lootChance()`**: 개별 처리 / 참조 호출: super.lootChance, Math.pow
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L155) **`createLoot()`**: 생성·초기화 / 참조 호출: super.createLoot
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L163) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L169) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getBoolean
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L176) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: isCharmedBy, canAttack, Dungeon.level.distance, chain, super.act

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 214. [`HermitCrab.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/HermitCrab.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 55행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/HermitCrab.java#L28) `class HermitCrab  extends Crab`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/HermitCrab.java#L41) **`rollToDropLoot()`**: 개별 처리 / 조건 분기 / 참조 호출: super.rollToDropLoot, Dungeon.level.drop, Generator.randomArmor, sprite.drop
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/HermitCrab.java#L50) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 215. [`Mimic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 362행 / 타입 1개 / 필드 6개 / 메서드 28개.

### 타입·상속 선언

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L51) `class Mimic  extends Mob`

### 변수·상수 (단일 행 선언)

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L53) `int level`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L67) `ArrayList<Item> items`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L69) `boolean stealthy` 초기식: `false`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L71) `String LEVEL` 초기식: `"level"`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L72) `String ITEMS` 초기식: `"items"`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L73) `String STEALTHY` 초기식: `"stealthy"`

### 함수·메서드 역할과 내부 연결

- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L76) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L85) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: bundle.contains, bundle.getCollection, bundle.getInt, adjustStats, bundle.getBoolean, super.restoreFromBundle
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L99) **`add(Buff buff)`**: 상태 갱신 / 조건 분기 / 참조 호출: super.add, stopHiding, sprite.idle
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L112) **`name()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, super.name
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L121) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: MimicTooth.stealthyMimics, Messages.get, super.description
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L134) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: sprite.idle, GLog.w, Messages.get, CellEmitter.get, burst, Speck.factory, Sample.INSTANCE.play, super.act
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L148) **`sprite()`**: 개별 처리 / 조건 분기 / 참조 호출: super.sprite, sprite.hideMimic
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L155) **`interact(Char c)`**: 개별 처리 / 조건 분기 / 참조 호출: super.interact, stopHiding, Dungeon.hero.busy, hero.sprite.operate, Dungeon.hero.buff, doAttack, sprite.idle, Dungeon.hero.spendAndNext
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L176) **`onAttackComplete()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onAttackComplete, Dungeon.hero.spendAndNext
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L186) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: stopHiding, super.defenseProc
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L195) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: stopHiding, super.damage
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L204) **`die(Object cause)`**: 개별 처리 / 조건 분기 / 참조 호출: stopHiding, super.die
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L212) **`stopHiding()`**: 개별 처리 / 조건 분기 / 참조 호출: sprite.idle, Actor.chars, contains, GLog.w, Messages.get, CellEmitter.get, burst, Speck.factory, Sample.INSTANCE.play
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L225) **`stealthy()`**: 개별 처리
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L230) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: Random.NormalIntRange
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L239) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L244) **`beckon(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: super.beckon
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L251) **`attackSkill(Char target)`**: 전투 관련 / 조건 분기
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L259) **`setLevel(int level)`**: 상태 갱신 / 참조 호출: adjustStats
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L264) **`adjustStats(int level)`**: 개별 처리
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L272) **`rollToDropLoot()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.drop, sprite.drop, super.rollToDropLoot
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L284) **`spawningWeight()`**: 개별 처리
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L289) **`reset()`**: 생성·초기화 / 조건 분기
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L294) **`spawnAt(int pos, Item... items)`**: 개별 처리 / 참조 호출: spawnAt
- [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L298) **`spawnAt(int pos, Class mimicType, Item... items)`**: 개별 처리 / 참조 호출: spawnAt
- [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L302) **`spawnAt(int pos, boolean useDecks, Item... items)`**: 개별 처리 / 참조 호출: spawnAt
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L306) **`spawnAt(int pos, Class mimicType, boolean useDecks, Item... items)`**: 개별 처리 / 조건 분기 / 참조 호출: GoldenMimic, CrystalMimic, EbonyMimic, Mimic, Arrays.asList, m.setLevel, Dungeon.scalingDepth, m.generatePrize, MimicTooth.stealthyMimics
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L332) **`generatePrize(boolean useDecks)`**: 개별 처리 / 조건 분기·반복·상태 선택 / 참조 호출: Random.Int, Gold, random, Generator.randomMissile, Generator.randomArmor, Generator.randomWeapon, Generator.random, Generator.randomUsingDefaults, Challenges.isItemBlocked

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 216. [`Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 1817행 / 타입 11개 / 필드 37개 / 메서드 85개.

### 타입·상속 선언

- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L111) `class Mob  extends Char`
- [L1215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1215) `interface AiState`
- [L1219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1219) `class Sleeping  implements AiState`
- [L1301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1301) `class Wandering  implements AiState`
- [L1358](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1358) `class Hunting  implements AiState`
- [L1449](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1449) `class Investigating  extends Wandering`
- [L1474](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1474) `class Fleeing  implements AiState`
- [L1526](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1526) `class Passive  implements AiState`
- [L1572](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1572) `class StealthGameplayInvestigating  extends Investigating`
- [L1604](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1604) `class StealthGameplayWandering  extends Wandering`
- [L1678](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1678) `class StealthGameplaySleeping  extends Sleeping`

### 변수·상수 (단일 행 선언)

- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L125) `AiState state` 초기식: `SLEEPING`
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L127) `Class<? extends CharSprite> spriteClass`
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L129) `int target` 초기식: `-1`
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L131) `int defenseSkill` 초기식: `0`
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L133) `int EXP` 초기식: `1`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L134) `int maxLvl` 초기식: `Hero.MAX_LEVEL-1`
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L136) `Char enemy`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L137) `int enemyID` 초기식: `-1`
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L138) `boolean enemySeen`
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L139) `boolean alerted` 초기식: `false`
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L141) `float TIME_TO_WAKE_UP` 초기식: `1f`
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L143) `boolean firstAdded` 초기식: `true`
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L154) `String STATE` 초기식: `"state"`
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L155) `String SEEN` 초기식: `"seen"`
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L156) `String TARGET` 초기식: `"target"`
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L157) `String MAX_LVL` 초기식: `"max_lvl"`
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L159) `String ENEMY_ID` 초기식: `"enemy_id"`
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L161) `String SWARM_TIME` 초기식: `"swarm_time"`
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L164) `String USING_STEALTH` 초기식: `"using_stealth"`
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L165) `String INVEST_TURNS` 초기식: `"invest_turns"`
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L166) `String WANDER_POSITIONS` 초기식: `"wander_positions"`
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L167) `String WANDER_POS_IDX` 초기식: `"wander_pos_idx"`
- [L315](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L315) `float timeSeenAt` 초기식: `Float.MAX_VALUE`
- [L355](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L355) `boolean intelligentAlly` 초기식: `false`
- [L1135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1135) `Object loot` 초기식: `null`
- [L1136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1136) `float lootChance` 초기식: `0`
- [L1221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1221) `String TAG` 초기식: `"SLEEPING"`
- [L1303](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1303) `String TAG` 초기식: `"WANDERING"`
- [L1360](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1360) `String TAG` 초기식: `"HUNTING"`
- [L1420](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1420) `boolean recursing` 초기식: `false`
- [L1451](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1451) `String TAG` 초기식: `"INVESTIGATING"`
- [L1476](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1476) `String TAG` 초기식: `"FLEEING"`
- [L1528](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1528) `String TAG` 초기식: `"PASSIVE"`
- [L1567](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1567) `boolean usingStealthGamePlay`
- [L1570](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1570) `int investigatingTurns`
- [L1601](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1601) `int wanderPosIdx` 초기식: `0`
- [L1602](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1602) `int[] wanderPositions`

### 함수·메서드 역할과 내부 연결

- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L119) **`Sleeping()`**: 개별 처리
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L120) **`Hunting()`**: 개별 처리
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L121) **`Investigating()`**: 개별 처리
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L122) **`Wandering()`**: 개별 처리
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L123) **`Fleeing()`**: 개별 처리
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L124) **`Passive()`**: 개별 처리
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L144) **`onAdd()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Math.round, AscensionChallenge.statModifier
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L170) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put, enemy.id
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L208) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getBoolean, activateSteathGameplayBehaviour, bundle.getInt, bundle.contains, bundle.getIntArray, bundle.getString, state.equals, bundle.getFloat
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L254) **`restoreEnemy()`**: 저장·복원 / 조건 분기 / 참조 호출: Actor.findById
- [L258](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L258) **`sprite()`**: 개별 처리 / 참조 호출: Reflection.newInstance
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L263) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.act, sprite.showAlert, sprite.hideAlert, sprite.hideLost, sprite.hideInvestigate, processSwarmIntel, spend, buff, chooseEnemy
- [L317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L317) **`processSwarmIntel(boolean enemyInFOV)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.isChallenged, now, swarmAlertRange, Dungeon.level.distance, mob.beckon, Buff.affect
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L341) **`swarmAlertRange()`**: 개별 처리 / 참조 호출: Math.max, now, GameMath.gate
- [L347](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L347) **`fixTime(float decrement)`**: 개별 처리 / 조건 분기 / 참조 호출: swarmAlertRange, super.fixTime
- [L357](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L357) **`chooseEnemy()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: buff, Actor.findById, enemy.buff, Actor.chars, ch.buff, enemy.isAlive, contains, enemy.id, enemy.isInvulnerable
- [L527](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L527) **`add(Buff buff)`**: 상태 갱신 / 조건 분기 / 참조 호출: super.add, postpone
- [L543](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L543) **`remove(Buff buff)`**: 상태 갱신 / 조건 분기 / 참조 호출: super.remove, buff, sprite.showStatus, Messages.get
- [L559](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L559) **`canAttack(Char enemy)`**: 조건 판정 / 조건 분기·반복 / 참조 호출: Dungeon.level.adjacent, buffs, buff.canAttackWithExtraReach
- [L571](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L571) **`cellIsPathable(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: buff, Char.hasProp, Actor.findChar
- [L591](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L591) **`getCloser(int target)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: Dungeon.level.insideMap, Dungeon.level.adjacent, cellIsPathable, path.isEmpty, path.getFirst, path.size, Dungeon.level.distance, path.getLast, path.removeLast
- [L715](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L715) **`getFurther(int target)`**: 조회·탐색 / 조건 분기 / 참조 호출: Dungeon.flee, move
- [L733](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L733) **`move(int step, boolean travelling)`**: 개별 처리 / 조건 분기 / 참조 호출: super.move, Dungeon.level.distance, PathFinder.buildDistanceMap, GameScene.updateFog, sprite, sprite.parent.add, movementShadow.point, DungeonTilemap.raisedTileCenterToWorld, movementShadow.width
- [L762](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L762) **`updateValues(float progress)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Math.pow, super.updateValues
- [L771](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L771) **`onComplete()`**: 이벤트·효과 실행
- [L783](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L783) **`updateSpriteState()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.updateSpriteState, Dungeon.hero.buff, sprite.add
- [L790](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L790) **`attackDelay()`**: 전투 관련 / 조건 분기 / 참조 호출: buff
- [L796](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L796) **`doAttack(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: sprite.attack, attack, Invisibility.dispel, spend, attackDelay
- [L811](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L811) **`onAttackComplete()`**: 이벤트·효과 실행 / 참조 호출: attack, Invisibility.dispel, spend, attackDelay, super.onAttackComplete
- [L819](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L819) **`defenseSkill(Char enemy)`**: 전투 관련 / 조건 분기 / 참조 호출: buff, h.belongings.attackingWeapon, STRReq, h.STR, surprisedBy
- [L843](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L843) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: belongings.attackingWeapon, Badges.validateHuntressUnlock, surprisedBy, Badges.validateRogueUnlock, hero.belongings.attackingWeapon, Sample.INSTANCE.playDelayed, Sample.INSTANCE.play, enemy.buff, Wound.hit
- [L902](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L902) **`speed()`**: 개별 처리 / 참조 호출: super.speed, AscensionChallenge.enemySpeedModifier
- [L906](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L906) **`surprisedBy(Char enemy)`**: 개별 처리 / 참조 호출: surprisedBy
- [L910](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L910) **`surprisedBy(Char enemy, boolean attacking)`**: 개별 처리 / 참조 호출: Dungeon.level.length, enemy.canSurpriseAttack
- [L917](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L917) **`heroShouldInteract()`**: 개별 처리 / 참조 호출: buff
- [L921](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L921) **`aggro(Char ch)`**: 개별 처리 / 조건 분기
- [L928](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L928) **`clearEnemy()`**: 상태 갱신 / 조건 분기
- [L934](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L934) **`isTargeting(Char ch)`**: 조건 판정
- [L939](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L939) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: isInvulnerable, src.getClass, aggro, recentlyAttackedBy.add, super.damage
- [L966](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L966) **`destroy()`**: 개별 처리 / 조건 분기 / 참조 호출: super.destroy, level.mobs.remove, Dungeon.hero.buff, Dungeon.observe, GameScene.updateFog, Dungeon.hero.isAlive, Badges.validateMonstersSlain, Bestiary.setSeen, getClass
- [L1022](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1022) **`die(Object cause)`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int, buff, Badges.validateHazardAssists, rollToDropLoot, Dungeon.hero.hasTalent, Random.Float, Dungeon.hero.pointsInTalent, Buff.affect, Dungeon.hero.buff
- [L1075](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1075) **`lootChance()`**: 개별 처리 / 조건 분기 / 참조 호출: RingOfWealth.dropChanceMultiplier, Dungeon.hero.buff, Math.pow, prep.attackLevel, Dungeon.hero.pointsInTalent, ShardOfOblivion.lootChanceMultiplier
- [L1096](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1096) **`rollToDropLoot()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: buff, stolen.itemWasStolen, Random.Float, lootChance, createLoot, Dungeon.level.drop, sprite.drop, Ring.getBuffedBonus, properties.contains
- [L1139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1139) **`createLoot()`**: 생성·초기화 / 조건 분기 / 참조 호출: Generator.randomUsingDefaults, ExoticPotion.regToExo.containsKey, Random.Float, ExoticCrystals.consumableExoticChance, Generator.random, ExoticPotion.regToExo.get, ExoticScroll.regToExo.containsKey, ExoticScroll.regToExo.get
- [L1168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1168) **`spawningWeight()`**: 개별 처리
- [L1172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1172) **`reset()`**: 생성·초기화
- [L1176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1176) **`beckon(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: notice
- [L1186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1186) **`description()`**: 개별 처리 / 참조 호출: Messages.get
- [L1190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1190) **`info()`**: 개별 처리 / 반복 / 참조 호출: description, buffs, Messages.titleCase, b.name, b.desc
- [L1200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1200) **`notice()`**: 개별 처리 / 참조 호출: sprite.showAlert
- [L1204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1204) **`yell(String str)`**: 개별 처리 / 참조 호출: GLog.newLine, GLog.n, Messages.titleCase, name
- [L1211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1211) **`landmark()`**: 개별 처리
- [L1224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1224) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: buffs, awaken, spend, Actor.chars, detectionChance, Dungeon.hero.hasTalent, distance, Dungeon.hero.pointsInTalent, Random.Float
- [L1281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1281) **`detectionChance(Char enemy)`**: 개별 처리 / 참조 호출: distance, enemy.stealth
- [L1285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1285) **`awaken(boolean enemyInFOV)`**: 개별 처리 / 조건 분기 / 참조 호출: notice, Dungeon.level.randomDestination, spend
- [L1306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1306) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Random.Float, detectionChance, noticeEnemy, continueWandering
- [L1319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1319) **`detectionChance(Char enemy)`**: 개별 처리 / 참조 호출: distance, enemy.stealth
- [L1323](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1323) **`noticeEnemy()`**: 개별 처리 / 참조 호출: notice
- [L1334](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1334) **`continueWandering()`**: 개별 처리 / 조건 분기 / 참조 호출: getCloser, spend, speed, moveSprite, randomDestination
- [L1349](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1349) **`randomDestination()`**: 개별 처리 / 참조 호출: Dungeon.level.randomDestination
- [L1363](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1363) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: isCharmedBy, canAttack, recentlyAttackedBy.clear, doAttack, handleRecentAttackers, act, sprite.showLost, randomDestination, spend
- [L1402](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1402) **`handleRecentAttackers()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: recentlyAttackedBy.isEmpty, ch.isActive, Actor.chars, contains, isCharmedBy, canAttack, Dungeon.level.distance, recentlyAttackedBy.clear
- [L1424](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1424) **`handleUnreachableTarget(boolean enemyInFOV, boolean justAlerted)`**: 개별 처리 / 조건 분기 / 참조 호출: chooseEnemy, act, spend, sprite.showLost, randomDestination
- [L1454](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1454) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.level.distance, sprite.showLost, randomDestination, spend, super.act
- [L1479](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1479) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Random.Int, Dungeon.level.distance, escaped, spend, getFurther, speed, moveSprite, nowhereToRun
- [L1509](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1509) **`escaped()`**: 개별 처리
- [L1514](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1514) **`nowhereToRun()`**: 개별 처리 / 조건 분기 / 참조 호출: buff, sprite.showStatus, Messages.get
- [L1531](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1531) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 참조 호출: spend
- [L1544](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1544) **`activateSteathGameplayBehaviour()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: StealthGameplayInvestigating, StealthGameplayWandering, StealthGameplaySleeping
- [L1575](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1575) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.act
- [L1586](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1586) **`detectionChance(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: distance, enemy.stealth
- [L1595](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1595) **`setupStealthGameplayWanderPositions(int[] wanderPositions, int startingIdx)`**: 생성·초기화
- [L1607](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1607) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 참조 호출: super.act
- [L1612](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1612) **`detectionChance(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, distance, enemy.stealth, PointF.angle, Dungeon.level.cellToPoint, Math.abs, Dungeon.level.distance, Math.pow
- [L1638](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1638) **`noticeEnemy()`**: 개별 처리 / 조건 분기 / 참조 호출: super.noticeEnemy, sprite.showInvestigate, spend, Buff.affect, id
- [L1653](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1653) **`randomDestination()`**: 개별 처리 / 조건 분기 / 참조 호출: sprite.idle
- [L1681](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1681) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.act
- [L1690](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1690) **`awaken(boolean enemyInFOV)`**: 개별 처리 / 조건 분기 / 참조 호출: super.awaken, sprite.showInvestigate, Buff.affect, id
- [L1707](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1707) **`detectionChance(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.pow, distance, enemy.stealth
- [L1719](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1719) **`holdAllies(Level level)`**: 개별 처리 / 참조 호출: holdAllies
- [L1723](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1723) **`holdAllies(Level level, int holdFromPos)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: heldAllies.clear, level.mobs.toArray, PowerOfMany.getPoweredAlly, clearDefensingPos, level.mobs.remove, heldAllies.add, Dungeon.level.distance
- [L1745](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1745) **`restoreAllies(Level level, int pos)`**: 저장·복원 / 참조 호출: restoreAllies
- [L1749](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1749) **`restoreAllies(Level level, int pos, int gravitatePos)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: heldAllies.isEmpty, level.findMob, candidatePositions.add, Collections.shuffle, Collections.sort, compare, Dungeon.level.distance, Stasis.getStasisAlly, level.mobs.toArray
- [L1765](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1765) **`compare(Integer t1, Integer t2)`**: 개별 처리 / 참조 호출: Dungeon.level.distance
- [L1812](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1812) **`clearHeldAllies()`**: 상태 갱신 / 참조 호출: heldAllies.clear

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 217. [`MobSpawner.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/MobSpawner.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 277행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/MobSpawner.java#L33) `class MobSpawner  extends Actor`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/MobSpawner.java#L39) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.level.mobCount, Dungeon.level.mobLimit, Dungeon.level.spawnMob, spend, Dungeon.level.respawnCooldown
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/MobSpawner.java#L57) **`resetCooldown()`**: 생성·초기화 / 참조 호출: spend, cooldown, Dungeon.level.respawnCooldown
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/MobSpawner.java#L62) **`getMobRotation(int depth)`**: 조회·탐색 / 참조 호출: standardMobRotation, addRareMobs, swapMobAlts, Random.shuffle
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/MobSpawner.java#L71) **`standardMobRotation(int depth)`**: 개별 처리 / 상태 선택 / 참조 호출: Arrays.asList, Shaman.random
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/MobSpawner.java#L215) **`addRareMobs(int depth, ArrayList<Class<?extends Mob>> rotation)`**: 상태 갱신 / 조건 분기·상태 선택 / 참조 호출: Random.Float, rotation.add
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/MobSpawner.java#L244) **`swapMobAlts(ArrayList<Class<?extends Mob>> rotation)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: RatSkull.exoticChanceMultiplier, rotation.size, Random.Float, rotation.get, RARE_ALTS.get, rotation.set

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 218. [`Monk.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 161행 / 타입 2개 / 필드 2개 / 메서드 14개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L37) `class Monk  extends Mob`
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L143) `class Focus  extends Buff`

### 변수·상수 (단일 행 선언)

- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L81) `float focusCooldown` 초기식: `0`
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L129) `String FOCUS_COOLDOWN` 초기식: `"focus_cooldown"`

### 함수·메서드 역할과 내부 연결

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L55) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L60) **`attackSkill(Char target)`**: 전투 관련
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L65) **`attackDelay()`**: 전투 관련 / 참조 호출: super.attackDelay
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L70) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L75) **`rollToDropLoot()`**: 개별 처리 / 참조 호출: Imp.Quest.oldProcess, super.rollToDropLoot
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L84) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.act, buff, Buff.affect
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L93) **`spend(float time)`**: 개별 처리 / 참조 호출: super.spend
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L99) **`move(int step, boolean travelling)`**: 개별 처리 / 조건 분기 / 참조 호출: super.move
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L107) **`defenseSkill(Char enemy)`**: 전투 관련 / 조건 분기 / 참조 호출: buff, super.defenseSkill
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L115) **`defenseVerb()`**: 전투 관련 / 조건 분기 / 참조 호출: buff, super.defenseVerb, f.detach, Sample.INSTANCE.play, Random.Float, Random.NormalFloat, Messages.get
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L132) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L138) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L151) **`icon()`**: 개별 처리
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L156) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 219. [`Necromancer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 444행 / 타입 5개 / 필드 9개 / 메서드 15개.

### 타입·상속 선언

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L50) `class Necromancer  extends Mob`
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L264) `class SummoningBlockDamage`
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L266) `class Hunting  extends Mob.Hunting`
- [L409](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L409) `class NecroSkeleton  extends Skeleton`
- [L428](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L428) `class NecroSkeletonSprite  extends SkeletonSprite`

### 변수·상수 (단일 행 선언)

- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L69) `boolean summoning` 초기식: `false`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L70) `int summoningPos` 초기식: `-1`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L72) `boolean firstSummon` 초기식: `true`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L74) `NecroSkeleton mySkeleton`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L75) `int storedSkeletonID` 초기식: `-1`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L134) `String SUMMONING` 초기식: `"summoning"`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L135) `String FIRST_SUMMON` 초기식: `"first_summon"`
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L136) `String SUMMONING_POS` 초기식: `"summoning_pos"`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L137) `String MY_SKELETON` 초기식: `"my_skeleton"`

### 함수·메서드 역할과 내부 연결

- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L78) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: cancelSummoning, super.act
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L87) **`aggro(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: super.aggro, mySkeleton.isAlive, level.mobs.contains, mySkeleton.aggro
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L97) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L102) **`lootChance()`**: 개별 처리 / 참조 호출: super.lootChance
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L107) **`createLoot()`**: 생성·초기화 / 참조 호출: super.createLoot
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L113) **`die(Object cause)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findById, mySkeleton.isAlive, mySkeleton.die, super.die
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L130) **`canAttack(Char enemy)`**: 조건 판정
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L140) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put, mySkeleton.id
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L155) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getBoolean, bundle.contains, bundle.getInt
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L167) **`onZapComplete()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: mySkeleton.isAlive, sprite.parent.add, Beam.HealthRay, sprite.center, mySkeleton.sprite.center, Sample.INSTANCE.play, Math.min, mySkeleton.sprite.showStatusWithIcon, Integer.toString
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L199) **`summonMinion()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.findChar, hasProp, Dungeon.level.trueDistance, Char.hasProp, Actor.add, Pushing, Dungeon.level.occupyCell, blocker.damage, Random.NormalIntRange
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L269) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Actor.findById, summonMinion, mySkeleton.isAlive, level.mobs.contains, Dungeon.level.distance, BArray.not, BArray.or, PathFinder.buildDistanceMap, Actor.findChar
- [L424](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L424) **`spawningWeight()`**: 개별 처리
- [L430](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L430) **`NecroSkeletonSprite()`**: 개별 처리 / 참조 호출: brightness
- [L436](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L436) **`resetColor()`**: 생성·초기화 / 참조 호출: super.resetColor, brightness

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 220. [`Blacksmith.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 480행 / 타입 2개 / 필드 39개 / 메서드 26개.

### 타입·상속 선언

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L53) `class Blacksmith  extends NPC`
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L200) `class Quest`

### 변수·상수 (단일 행 선언)

- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L109) `String msg1Final` 초기식: `msg1`
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L110) `String msg2Final` 초기식: `msg2`
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L202) `int type` 초기식: `0`
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L203) `int CRYSTAL` 초기식: `1`
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L204) `int GNOLL` 초기식: `2`
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L205) `int FUNGI` 초기식: `3`
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L208) `boolean spawned`
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L209) `boolean given`
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L210) `boolean started`
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L211) `boolean bossBeaten`
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L212) `boolean completed`
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L215) `int favor`
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L216) `Item pickaxe`
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L217) `boolean freePickaxe`
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L218) `int reforges`
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L219) `int hardens`
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L220) `int upgrades`
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L221) `int smiths`
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L224) `ArrayList<Item> smithRewards`
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L225) `Weapon.Enchantment smithEnchant`
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L226) `Armor.Glyph smithGlyph`
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L250) `String NODE` 초기식: `"blacksmith"`
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L252) `String TYPE` 초기식: `"type"`
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L253) `String ALTERNATIVE` 초기식: `"alternative"`
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L255) `String SPAWNED` 초기식: `"spawned"`
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L256) `String GIVEN` 초기식: `"given"`
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L257) `String STARTED` 초기식: `"started"`
- [L258](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L258) `String BOSS_BEATEN` 초기식: `"boss_beaten"`
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L259) `String COMPLETED` 초기식: `"completed"`
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L261) `String FAVOR` 초기식: `"favor"`
- [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L262) `String PICKAXE` 초기식: `"pickaxe"`
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L263) `String FREE_PICKAXE` 초기식: `"free_pickaxe"`
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L264) `String REFORGES` 초기식: `"reforges"`
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L265) `String HARDENS` 초기식: `"hardens"`
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L266) `String UPGRADES` 초기식: `"upgrades"`
- [L267](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L267) `String SMITHS` 초기식: `"smiths"`
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L268) `String SMITH_REWARDS` 초기식: `"smith_rewards"`
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L269) `String ENCHANT` 초기식: `"enchant"`
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L270) `String GLYPH` 초기식: `"glyph"`

### 함수·메서드 역할과 내부 연결

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L62) **`landmark()`**: 개별 처리 / 참조 호출: Quest.completed, Quest.rewardsAvailable
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L67) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.hero.buff, die, Notes.remove, landmark, Quest.rewardsAvailable, Quest.completed, super.act
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L79) **`interact(Char c)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: sprite.turnTo, Messages.get, Game.runOnRenderThread, Callback, call, GameScene.show, WndQuest, hide, super.hide
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L113) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.show, WndQuest, hide, super.hide, Pickaxe, pick.doPickUp, GLog.i, Messages.capitalize, Messages.get
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L116) **`hide()`**: 개별 처리 / 조건 분기 / 참조 호출: super.hide, Pickaxe, pick.doPickUp, GLog.i, Messages.capitalize, Messages.get, pick.name, Dungeon.level.drop, sprite.drop
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L152) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.show, WndBlacksmith.WndSmith, WndBlacksmith
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L171) **`tell(String text)`**: 개별 처리 / 참조 호출: Game.runOnRenderThread, Callback, call, GameScene.show, WndQuest
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L174) **`call()`**: 개별 처리 / 참조 호출: GameScene.show, WndQuest
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L181) **`defenseSkill(Char enemy)`**: 전투 관련
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L186) **`damage(int dmg, Object src)`**: 전투 관련
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L191) **`add(Buff buff)`**: 상태 갱신
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L196) **`reset()`**: 생성·초기화
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L228) **`reset()`**: 생성·초기화 / 참조 호출: Pickaxe, identify
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L272) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: Bundle, node.put, bundle.put
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L306) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: bundle.getBundle, node.isNull, node.getBoolean, node.getInt, node.contains, node.get, node.getCollection, reset
- [L347](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L347) **`spawn(ArrayList<Room> rooms)`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int, rooms.add, BlacksmithRoom, Random.IntRange, generateRewards
- [L363](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L363) **`generateRewards(boolean useDecks)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: smithRewards.add, Generator.randomWeapon, smithRewards.get, getClass, toUndo.add, smithRewards.remove, Generator.undoDrop, Generator.randomMissile, Generator.randomArmor
- [L415](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L415) **`Type()`**: 개별 처리
- [L419](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L419) **`given()`**: 개별 처리
- [L423](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L423) **`started()`**: 개별 처리
- [L427](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L427) **`start()`**: 개별 처리
- [L431](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L431) **`beatBoss()`**: 개별 처리
- [L435](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L435) **`bossBeaten()`**: 개별 처리
- [L439](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L439) **`completed()`**: 개별 처리
- [L443](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L443) **`complete()`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.getItem, Math.min, gold.quantity, gold.detachAll, pick.isEquipped, pick.doUnequip, pick.detach
- [L472](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java#L472) **`rewardsAvailable()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 221. [`DirectableAlly.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 174행 / 타입 3개 / 필드 5개 / 메서드 10개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L30) `class DirectableAlly  extends NPC`
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L117) `class Wandering  extends Mob.Wandering`
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L159) `class Hunting  extends Mob.Hunting`

### 변수·상수 (단일 행 선언)

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L44) `boolean attacksAutomatically` 초기식: `true`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L46) `int defendingPos` 초기식: `-1`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L47) `boolean movingToDefendPos` 초기식: `false`
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L100) `String DEFEND_POS` 초기식: `"defend_pos"`
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L101) `String MOVING_TO_DEFEND` 초기식: `"moving_to_defend"`

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L49) **`defendPos(int cell)`**: 개별 처리 / 참조 호출: aggro
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L56) **`clearDefensingPos()`**: 상태 갱신
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L61) **`followHero()`**: 개별 처리 / 참조 호출: aggro
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L68) **`targetChar(Char ch)`**: 개별 처리 / 참조 호출: aggro
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L76) **`aggro(Char ch)`**: 개별 처리 / 조건 분기
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L83) **`directTocell(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, defendPos, followHero, targetChar
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L104) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L111) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, bundle.getInt, bundle.getBoolean
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L120) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: canAttack, notice, getCloser, spend, speed, moveSprite
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java#L162) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: canAttack, super.act

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 222. [`Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 410행 / 타입 3개 / 필드 19개 / 메서드 26개.

### 타입·상속 선언

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L58) `class Ghost  extends NPC`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L72) `class Wandering  extends Mob.Wandering`
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L216) `class Quest`

### 변수·상수 (단일 행 선언)

- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L218) `boolean spawned`
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L220) `int type`
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L222) `boolean given`
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L223) `boolean processed`
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L225) `int depth`
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L227) `Weapon weapon`
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L228) `Armor armor`
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L229) `Weapon.Enchantment enchant`
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L230) `Armor.Glyph glyph`
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L241) `String NODE` 초기식: `"sadGhost"`
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L243) `String SPAWNED` 초기식: `"spawned"`
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L244) `String TYPE` 초기식: `"type"`
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L245) `String GIVEN` 초기식: `"given"`
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L246) `String PROCESSED` 초기식: `"processed"`
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L247) `String DEPTH` 초기식: `"depth"`
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L248) `String WEAPON` 초기식: `"weapon"`
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L249) `String ARMOR` 초기식: `"armor"`
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L250) `String ENCHANT` 초기식: `"enchant"`
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L251) `String GLYPH` 초기식: `"glyph"`

### 함수·메서드 역할과 내부 연결

- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L74) **`randomDestination()`**: 개별 처리 / 조건 분기 / 참조 호출: super.randomDestination, level.heaps.get, Dungeon.level.exit
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L85) **`landmark()`**: 개별 처리
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L90) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.hero.buff, die, Notes.remove, landmark, super.act
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L100) **`defenseSkill(Char enemy)`**: 전투 관련
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L105) **`speed()`**: 개별 처리
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L110) **`chooseEnemy()`**: 개별 처리
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L115) **`damage(int dmg, Object src)`**: 전투 관련
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L120) **`add(Buff buff)`**: 상태 갱신
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L125) **`reset()`**: 생성·초기화
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L130) **`interact(Char c)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: sprite.turnTo, Sample.INSTANCE.play, super.interact, Game.runOnRenderThread, Callback, call, GameScene.show, WndSadGhost, WndQuest
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L144) **`call()`**: 개별 처리 / 참조 호출: GameScene.show, WndSadGhost
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L151) **`call()`**: 개별 처리 / 상태 선택 / 참조 호출: GameScene.show, WndQuest, Messages.get
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L192) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.show, WndQuest, hide, super.hide, Music.INSTANCE.fadeOut, Callback, call, Dungeon.level.playLevelMusic
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L195) **`hide()`**: 개별 처리 / 조건 분기 / 참조 호출: super.hide, Music.INSTANCE.fadeOut, Callback, call, Dungeon.level.playLevelMusic
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L199) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.playLevelMusic
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L232) **`reset()`**: 생성·초기화
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L253) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: Bundle, node.put, bundle.put
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L279) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: bundle.getBundle, node.isNull, node.getBoolean, node.getInt, node.get, node.contains, reset
- [L303](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L303) **`spawn(SewerLevel level, Room room)`**: 개별 처리 / 조건 분기·반복·상태 선택 / 참조 호출: Random.Int, Ghost, level.pointToCell, room.random, level.exit, level.mobs.add, Random.chances, LeatherArmor, MailArmor
- [L367](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L367) **`process()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: GLog.n, Messages.get, Sample.INSTANCE.play, Game.runOnRenderThread, Callback, call, Music.INSTANCE.fadeOut, Dungeon.level.playLevelMusic
- [L376](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L376) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Music.INSTANCE.fadeOut, Callback, call, Dungeon.level.playLevelMusic
- [L379](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L379) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.playLevelMusic
- [L390](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L390) **`active()`**: 시간·상태 갱신
- [L394](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L394) **`complete()`**: 개별 처리 / 참조 호출: Notes.remove
- [L401](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L401) **`processed()`**: 시간·상태 갱신
- [L405](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java#L405) **`completed()`**: 개별 처리 / 참조 호출: processed

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 223. [`Imp.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 402행 / 타입 2개 / 필드 21개 / 메서드 24개.

### 타입·상속 선언

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L55) `class Imp  extends NPC`
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L204) `class Quest`

### 변수·상수 (단일 행 선언)

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L63) `boolean seenBefore` 초기식: `false`
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L206) `boolean spawned`
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L209) `boolean oldQuest` 초기식: `false`
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L210) `boolean alternative`
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L213) `boolean given`
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L214) `boolean completed`
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L215) `Item reward`
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L219) `int hazardFreebies`
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L220) `boolean mirrorUsed` 초기식: `false`
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L221) `int score`
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L234) `String NODE` 초기식: `"demon"`
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L236) `String SPAWNED` 초기식: `"spawned"`
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L238) `String OLD_QUEST` 초기식: `"old_quest"`
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L239) `String ALTERNATIVE` 초기식: `"alternative"`
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L240) `String REWARD` 초기식: `"reward"`
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L242) `String GIVEN` 초기식: `"given"`
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L243) `String COMPLETED` 초기식: `"completed"`
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L245) `String HAZRD_FREEBIES` 초기식: `"hazard_freebies"`
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L246) `String SCORE` 초기식: `"score"`
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L247) `String REWARD_OPTIONS` 초기식: `"reward_options"`
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L248) `String MIRROR_USED` 초기식: `"mirror_used"`

### 함수·메서드 역할과 내부 연결

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L66) **`landmark()`**: 개별 처리 / 참조 호출: Quest.isCompleted
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L71) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.hero.buff, die, Quest.isCompleted, Dungeon.level.drop, throwItems, flee, yell, Messages.get, Messages.titleCase
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L100) **`defenseSkill(Char enemy)`**: 전투 관련
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L105) **`damage(int dmg, Object src)`**: 전투 관련
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L110) **`add(Buff buff)`**: 상태 갱신
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L115) **`reset()`**: 생성·초기화
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L120) **`interact(Char c)`**: 개별 처리 / 조건 분기 / 참조 호출: sprite.turnTo, hero.belongings.getItem, tokens.quantity, Game.runOnRenderThread, Callback, call, GameScene.show, WndImpOld, tell
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L136) **`call()`**: 개별 처리 / 참조 호출: GameScene.show, WndImpOld
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L157) **`call()`**: 개별 처리 / 참조 호출: GameScene.show, WndQuest, Messages.get, hide, super.hide, tell
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L160) **`hide()`**: 개별 처리 / 참조 호출: super.hide, tell, Messages.get
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L187) **`tell(String text)`**: 개별 처리 / 참조 호출: Game.runOnRenderThread, Callback, call, GameScene.show, WndQuest
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L190) **`call()`**: 개별 처리 / 참조 호출: GameScene.show, WndQuest
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L196) **`flee()`**: 개별 처리 / 참조 호출: yell, Messages.get, Messages.titleCase, Dungeon.hero.name, destroy, sprite.die
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L223) **`reset()`**: 생성·초기화
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L251) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: Bundle, node.put, bundle.put
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L274) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: bundle.getBundle, node.isNull, node.getBoolean, node.contains, rewardOptions.clear, node.getInt, node.getCollection, node.get
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L305) **`spawn(ArrayList<Room> rooms)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Random.Int, rooms.add, AmbitiousImpRoom, rewardOptions.clear, Generator.randomArtifact, artif.identify, transferUpgrade, Generator.random, artif.level
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L359) **`given()`**: 개별 처리
- [L363](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L363) **`isOld()`**: 조건 판정
- [L367](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L367) **`oldProcess(Mob mob)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.drop, DwarfToken, sprite.drop
- [L377](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L377) **`oldComplete()`**: 개별 처리 / 참조 호출: Notes.remove
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L385) **`complete(int score)`**: 개별 처리 / 참조 호출: Notes.remove
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L393) **`isCompleted()`**: 조건 판정
- [L397](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java#L397) **`earnedShop()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":42,"fields":154,"methods":299}

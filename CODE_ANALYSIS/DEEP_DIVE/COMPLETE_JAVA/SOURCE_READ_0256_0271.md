# Java 파일별 소스 구현 해설 256–271

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 256. [`Slime.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Slime.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 85행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Slime.java#L33) `class Slime  extends Mob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Slime.java#L48) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Slime.java#L53) **`attackSkill(Char target)`**: 전투 관련
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Slime.java#L58) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: AscensionChallenge.statModifier, Math.sqrt, super.damage
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Slime.java#L70) **`lootChance()`**: 개별 처리 / 참조 호출: super.lootChance, Math.pow
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Slime.java#L77) **`createLoot()`**: 생성·초기화 / 참조 호출: Generator.randomUsingDefaults, w.level

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 257. [`Snake.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 73행 / 타입 1개 / 필드 1개 / 메서드 3개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java#L33) `class Snake  extends Mob`

### 변수·상수 (단일 행 선언)

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java#L58) `int dodges` 초기식: `0`

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java#L49) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java#L54) **`attackSkill(Char target)`**: 전투 관련
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java#L61) **`defenseVerb()`**: 전투 관련 / 조건 분기 / 참조 호출: Document.ADVENTURERS_GUIDE.isPageRead, Badges.isUnlocked, GameScene.flashForDocument, super.defenseVerb

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 258. [`SpectralNecromancer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/SpectralNecromancer.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 166행 / 타입 1개 / 필드 1개 / 메서드 6개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/SpectralNecromancer.java#L40) `class SpectralNecromancer  extends Necromancer`

### 변수·상수 (단일 행 선언)

- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/SpectralNecromancer.java#L84) `String WRAITH_IDS` 초기식: `"wraith_ids"`

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/SpectralNecromancer.java#L49) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: cancelSummoning, super.act
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/SpectralNecromancer.java#L60) **`rollToDropLoot()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.rollToDropLoot, Random.Int, Dungeon.level.drop, ScrollOfRemoveCurse, sprite.drop
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/SpectralNecromancer.java#L73) **`die(Object cause)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.findById, die, super.die
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/SpectralNecromancer.java#L87) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 반복 / 참조 호출: super.storeInBundle, wraithIDs.size, bundle.put
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/SpectralNecromancer.java#L95) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 반복 / 참조 호출: super.restoreFromBundle, wraithIDs.clear, bundle.getIntArray, wraithIDs.add
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/SpectralNecromancer.java#L104) **`summonMinion()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.findChar, hasProp, Dungeon.level.trueDistance, Char.hasProp, Actor.add, Pushing, Dungeon.level.occupyCell, blocker.damage, Random.NormalIntRange

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 259. [`Spinner.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 275행 / 타입 3개 / 필드 5개 / 메서드 14개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L41) `class Spinner  extends Mob`
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L227) `class Hunting  extends Mob.Hunting`
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L248) `class Fleeing  extends Mob.Fleeing`

### 변수·상수 (단일 행 선언)

- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L74) `int webCoolDown` 초기식: `0`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L75) `int lastEnemyPos` 초기식: `-1`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L77) `String WEB_COOLDOWN` 초기식: `"web_cooldown"`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L78) `String LAST_ENEMY_POS` 초기식: `"last_enemy_pos"`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L134) `boolean shotWebVisually` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L60) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L65) **`attackSkill(Char target)`**: 전투 관련
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L70) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L81) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L88) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L95) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.act
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L120) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, Random.Int, Random.IntRange, Math.round, AscensionChallenge.statModifier, Buff.affect, set
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L136) **`webPos()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: canAttack, Ballistica, b.path.size, b.path.get
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L180) **`shootWeb()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: webPos, left, right, applyWebToCell, Dungeon.hero.interrupt, next
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L207) **`applyWebToCell(int cell)`**: 개별 처리 / 참조 호출: GameScene.add, Blob.seed
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L211) **`left(int direction)`**: 개별 처리
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L215) **`right(int direction)`**: 개별 처리
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L230) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: webPos, sprite.zap, shootWeb, super.act
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Spinner.java#L251) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: buff, enemy.buff, webPos, sprite.zap, shootWeb, super.act

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 260. [`Statue.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 225행 / 타입 1개 / 필드 3개 / 메서드 22개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L41) `class Statue  extends Mob`

### 변수·상수 (단일 행 선언)

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L52) `Weapon weapon`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L54) `boolean levelGenStatue` 초기식: `true`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L78) `String WEAPON` 초기식: `"weapon"`

### 함수·메서드 역할과 내부 연결

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L56) **`Statue()`**: 개별 처리
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L63) **`createWeapon(boolean useDecks)`**: 생성·초기화 / 조건 분기 / 참조 호출: Generator.random, Generator.randomUsingDefaults, weapon.enchant, Enchantment.random
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L74) **`weapon()`**: 개별 처리
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L81) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L87) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.get
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L93) **`damageRoll()`**: 전투 관련 / 참조 호출: weapon.damageRoll
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L98) **`attackSkill(Char target)`**: 전투 관련 / 참조 호출: weapon.accuracyFactor
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L103) **`attackDelay()`**: 전투 관련 / 참조 호출: super.attackDelay, weapon.delayFactor
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L108) **`canAttack(Char enemy)`**: 조건 판정 / 참조 호출: super.canAttack, weapon.canReach
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L113) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange, weapon.defenseFactor
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L118) **`add(Buff buff)`**: 상태 갱신 / 조건 분기 / 참조 호출: super.add
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L129) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: super.damage
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L139) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, weapon.proc, enemy.isAlive, Dungeon.fail, GLog.n, Messages.capitalize, Messages.get, name
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L150) **`beckon(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: super.beckon
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L157) **`die(Object cause)`**: 개별 처리 / 조건 분기 / 참조 호출: buff, weapon.identify, Dungeon.level.drop, sprite.drop, super.die
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L167) **`landmark()`**: 개별 처리
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L172) **`destroy()`**: 개별 처리 / 조건 분기 / 참조 호출: landmark, Notes.remove, super.destroy
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L180) **`spawningWeight()`**: 개별 처리
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L185) **`reset()`**: 생성·초기화
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L190) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, weapon.name
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L202) **`random()`**: 개별 처리 / 참조 호출: random
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java#L206) **`random(boolean useDecks)`**: 개별 처리 / 조건 분기 / 참조 호출: RatSkull.exoticChanceMultiplier, Random.Float, ArmoredStatue, Statue, Random.pushGenerator, Random.Long, statue.createWeapon, Random.popGenerator

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 261. [`Succubus.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 200행 / 타입 1개 / 필드 2개 / 메서드 9개.

### 타입·상속 선언

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java#L51) `class Succubus  extends Mob`

### 변수·상수 (단일 행 선언)

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java#L53) `int blinkCooldown` 초기식: `0`
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java#L186) `String BLINK_CD` 초기식: `"blink_cd"`

### 함수·메서드 역할과 내부 연결

- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java#L72) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java#L77) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, enemy.buff, sprite.showStatusWithIcon, Integer.toString, Buff.affect, setShield, Sample.INSTANCE.play, Random.Int, id
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java#L111) **`getCloser(int target)`**: 조회·탐색 / 조건 분기 / 참조 호출: Dungeon.level.distance, blink, spend, speed, super.getCloser
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java#L129) **`blink(int target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Ballistica, Actor.findChar, route.path.get, properties, contains, candidates.add, candidates.size, Random.element, Random.IntRange
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java#L163) **`attackSkill(Char target)`**: 전투 관련
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java#L168) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java#L173) **`createLoot()`**: 생성·초기화 / 반복 / 참조 호출: Random.oneOf, Reflection.newInstance
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java#L189) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Succubus.java#L195) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 262. [`Swarm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 157행 / 타입 1개 / 필드 2개 / 메서드 9개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java#L40) `class Swarm  extends Mob`

### 변수·상수 (단일 행 선언)

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java#L57) `float SPLIT_DELAY` 초기식: `1f`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java#L61) `String GENERATION` 초기식: `"generation"`

### 함수·메서드 역할과 내부 연결

- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java#L64) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java#L70) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java#L77) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java#L83) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java#L88) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: Dungeon.level.width, Actor.findChar, properties, contains, candidates.add, candidates.size, split, Random.element, GameScene.add
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java#L123) **`attackSkill(Char target)`**: 전투 관련
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java#L127) **`split()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Swarm, buff, Buff.affect, reignite, set, buffs, b.getClass
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java#L146) **`lootChance()`**: 개별 처리 / 참조 호출: super.lootChance
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Swarm.java#L152) **`createLoot()`**: 생성·초기화 / 참조 호출: super.createLoot

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 263. [`Tengu.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 1143행 / 타입 9개 / 필드 26개 / 메서드 52개.

### 타입·상속 선언

- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L85) `class Tengu  extends Mob`
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L385) `class Hunting  extends Mob.Hunting`
- [L607](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L607) `class BombAbility  extends Buff`
- [L708](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L708) `class BombItem  extends Item`
- [L766](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L766) `class FireAbility  extends Buff`
- [L846](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L846) `class FireBlob  extends Blob`
- [L975](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L975) `class ShockerAbility  extends Buff`
- [L1041](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1041) `class ShockerBlob  extends Blob`
- [L1102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1102) `class ShockerItem  extends Item`

### 변수·상수 (단일 행 선언)

- [L356](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L356) `String LAST_ABILITY` 초기식: `"last_ability"`
- [L357](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L357) `String ABILITIES_USED` 초기식: `"abilities_used"`
- [L358](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L358) `String ARENA_JUMPS` 초기식: `"arena_jumps"`
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L359) `String ABILITY_COOLDOWN` 초기식: `"ability_cooldown"`
- [L436](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L436) `Char throwingChar`
- [L438](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L438) `int lastAbility` 초기식: `-1`
- [L439](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L439) `int abilitiesUsed` 초기식: `0`
- [L440](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L440) `int arenaJumps` 초기식: `0`
- [L443](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L443) `int abilityCooldown` 초기식: `2`
- [L445](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L445) `int BOMB_ABILITY` 초기식: `0`
- [L446](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L446) `int FIRE_ABILITY` 초기식: `1`
- [L447](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L447) `int SHOCKER_ABILITY` 초기식: `2`
- [L589](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L589) `int finalTargetCell` 초기식: `targetCell`
- [L609](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L609) `int bombPos` 초기식: `-1`
- [L610](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L610) `int timer` 초기식: `3`
- [L691](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L691) `String BOMB_POS` 초기식: `"bomb_pos"`
- [L692](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L692) `String TIMER` 초기식: `"timer"`
- [L768](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L768) `int direction`
- [L769](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L769) `int[] curCells`
- [L829](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L829) `String DIRECTION` 초기식: `"direction"`
- [L830](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L830) `String CUR_CELLS` 초기식: `"cur_cells"`
- [L957](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L957) `int finalTargetCell` 초기식: `targetCell`
- [L977](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L977) `int shockerPos`
- [L978](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L978) `Boolean shockingOrdinals` 초기식: `null`
- [L1024](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1024) `String SHOCKER_POS` 초기식: `"shocker_pos"`
- [L1025](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1025) `String SHOCKING_ORDINALS` 초기식: `"shocking_ordinals"`

### 함수·메서드 역할과 내부 연결

- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L102) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L107) **`attackSkill(Char target)`**: 전투 관련 / 조건 분기 / 참조 호출: Dungeon.level.adjacent
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L116) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L124) **`add(Buff buff)`**: 상태 갱신 / 조건 분기 / 참조 호출: Actor.chars, contains, super.add
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L132) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: level.mobs.contains, state, super.damage, Dungeon.hero.buff, isImmune, src.getClass, isInvulnerable, Dungeon.isChallenged, lock.addTime
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L170) **`act()`**: 시간·상태 갱신 / 참조 호출: Actor.remove, progress
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L196) **`act()`**: 시간·상태 갱신 / 참조 호출: Actor.remove, jump
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L207) **`isAlive()`**: 조건 판정 / 참조 호출: super.isAlive, level.mobs.contains
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L212) **`die(Object cause)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.drop, TengusMask, sprite.drop, GameScene.bossSlain, super.die, Badges.validateBossSlain, Badges.validateBossChallengeCompleted, hero.belongings.getItem, beacon.upgrade
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L236) **`canAttack(Char enemy)`**: 조건 판정 / 참조 호출: Ballistica
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L240) **`jump()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.length, Dungeon.level.updateFieldOfView, chooseEnemy, level.state, level.cleanTenguCell, randomTenguCellPos, level.trueDistance, Actor.findChar, CellEmitter.get
- [L331](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L331) **`notice()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.notice, BossHealthBar.isAssigned, BossHealthBar.assignBoss, BossHealthBar.bleed, yell, Messages.get, Dungeon.hero.name, Actor.chars, sayBoss
- [L362](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L362) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L371](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L371) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt, BossHealthBar.assignBoss, BossHealthBar.bleed
- [L388](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L388) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: isCharmedBy, canAttack, canUseAbility, useAbility, recentlyAttackedBy.clear, doAttack, handleUnreachableTarget
- [L408](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L408) **`handleUnreachableTarget(boolean enemyInFOV, boolean justAlerted)`**: 개별 처리 / 조건 분기 / 참조 호출: chooseEnemy, act, canUseAbility, useAbility, spend
- [L450](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L450) **`canUseAbility()`**: 조건 판정 / 조건 분기 / 참조 호출: targetAbilityUses, Dungeon.isChallenged, Random.IntRange
- [L482](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L482) **`targetAbilityUses()`**: 개별 처리 / 참조 호출: Math.max
- [L492](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L492) **`useAbility()`**: 이벤트·효과 실행 / 조건 분기·반복·상태 선택 / 참조 호출: Dungeon.isChallenged, Random.Int, throwBomb, throwFire, throwShocker, targetAbilityUses, spend
- [L566](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L566) **`throwBomb(final Char thrower, final Char target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: thrower.buffs, Dungeon.level.trueDistance, BombAbility.BombItem, thrower.sprite.zap, sprite.parent.recycle, reset, Callback, call, item.onThrow
- [L591](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L591) **`BombItem()`**: 개별 처리
- [L599](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L599) **`call()`**: 개별 처리 / 참조 호출: item.onThrow, thrower.next
- [L615](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L615) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: smokeEmitters.isEmpty, fx, DungeonTilemap.raisedTileCenterToWorld, FloatingText.show, PathFinder.buildDistanceMap, BArray.not, Actor.findChar, Random.NormalIntRange, Dungeon.scalingDepth
- [L674](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L674) **`fx(boolean on)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: PathFinder.buildDistanceMap, BArray.not, CellEmitter.get, e.pour, smokeEmitters.add, e.burst
- [L695](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L695) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L702](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L702) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L718](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L718) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 참조 호출: GLog.w, Messages.get
- [L724](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L724) **`onThrow(int cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onThrow, Buff.append
- [L735](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L735) **`emitter()`**: 개별 처리 / 참조 호출: Emitter, emitter.pos, emitter.pour
- [L749](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L749) **`throwFire(final Char thrower, final Char target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Ballistica, aim.path.get, thrower.sprite.zap, Buff.append, thrower.sprite.emitter, start, Speck.factory
- [L774](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L774) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: toCells.clear, spreadFromCell, FireBlob.volumeAt, toCells.remove, toCells.isEmpty, detach, toCells.size, GameScene.add, Blob.seed
- [L809](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L809) **`spreadFromCell(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: left, toCells.add, right
- [L821](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L821) **`left(int direction)`**: 개별 처리
- [L825](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L825) **`right(int direction)`**: 개별 처리
- [L833](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L833) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L840](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L840) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.contains, bundle.getIntArray
- [L854](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L854) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.width, GameMath.gate, Actor.findChar, ch.isImmune, Buff.affect, reignite, level.heaps.get, heap.burn, level.plants.get
- [L914](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L914) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour, Speck.factory
- [L921](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L921) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get
- [L932](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L932) **`throwShocker(final Char thrower, final Char target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.distance, thrower.buffs, Dungeon.level.trueDistance, ShockerAbility.ShockerItem, thrower.sprite.zap, sprite.parent.recycle, reset, Callback, call
- [L959](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L959) **`ShockerItem()`**: 개별 처리
- [L967](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L967) **`call()`**: 개별 처리 / 참조 호출: item.onThrow, thrower.next
- [L981](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L981) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Random.Int, spreadblob, sprite.parent.add, Lightning, Dungeon.level.width, Dungeon.level.distance, Sample.INSTANCE.play, spend
- [L1015](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1015) **`spreadblob()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: GameScene.add, Blob.seed
- [L1028](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1028) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L1035](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1035) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.contains, bundle.getBoolean
- [L1049](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1049) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.width, Actor.findChar, ch.damage, Dungeon.scalingDepth, Electricity, ch.isAlive, Dungeon.fail, GLog.n, Messages.get
- [L1090](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1090) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour
- [L1097](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1097) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get
- [L1112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1112) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 참조 호출: GLog.w, Messages.get
- [L1118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1118) **`onThrow(int cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onThrow, Buff.append, buff.spendToWhole
- [L1132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java#L1132) **`emitter()`**: 개별 처리 / 참조 호출: Emitter, emitter.pos, emitter.pour

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 264. [`Thief.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 231행 / 타입 3개 / 필드 2개 / 메서드 16개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L39) `class Thief  extends Mob`
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L182) `class Wandering  extends Mob.Wandering`
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L197) `class Fleeing  extends Mob.Fleeing`

### 변수·상수 (단일 행 선언)

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L41) `Item item`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L61) `String ITEM` 초기식: `"item"`

### 함수·메서드 역할과 내부 연결

- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L64) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L70) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.get
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L76) **`speed()`**: 개별 처리 / 조건 분기 / 참조 호출: super.speed
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L82) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L87) **`attackDelay()`**: 전투 관련 / 참조 호출: super.attackDelay
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L92) **`lootChance()`**: 개별 처리 / 참조 호출: super.lootChance, Math.pow
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L99) **`rollToDropLoot()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.drop, sprite.drop, dropPot, super.rollToDropLoot
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L110) **`createLoot()`**: 생성·초기화 / 참조 호출: super.createLoot
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L116) **`attackSkill(Char target)`**: 전투 관련
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L121) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L126) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, steal
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L138) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: Dungeon.level.drop, Gold, sprite.drop, super.defenseProc
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L146) **`steal(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.randomUnequipped, toSteal.level, GLog.w, Messages.get, toSteal.name, Dungeon.quickslot.convertToPlaceholder, Item.updateQuickslot, toSteal.detach, shatter
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L172) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: super.description, Messages.get, item.name
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L185) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.act
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java#L199) **`escaped()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.distance, Dungeon.level.randomRespawnCell, sprite.place, CellEmitter.get, burst, Speck.factory, GLog.n, Messages.get, item.name

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 265. [`TormentedSpirit.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/TormentedSpirit.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 87행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/TormentedSpirit.java#L38) `class TormentedSpirit  extends Wraith`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/TormentedSpirit.java#L46) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange, Math.round
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/TormentedSpirit.java#L52) **`attackSkill(Char target)`**: 전투 관련 / 참조 호출: Math.round
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/TormentedSpirit.java#L56) **`cleanse()`**: 개별 처리 / 조건 분기 / 참조 호출: Sample.INSTANCE.play, yell, Messages.get, Random.Int, Generator.randomWeapon, enchant, Generator.randomArmor, inscribe, prize.level

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 266. [`Warlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Warlock.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 154행 / 타입 2개 / 필드 1개 / 메서드 8개.

### 타입·상속 선언

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Warlock.java#L43) `class Warlock  extends Mob`
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Warlock.java#L103) `class DarkBolt`

### 변수·상수 (단일 행 선언)

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Warlock.java#L45) `float TIME_TO_ZAP` 초기식: `1f`

### 함수·메서드 역할과 내부 연결

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Warlock.java#L63) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Warlock.java#L68) **`attackSkill(Char target)`**: 전투 관련
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Warlock.java#L73) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Warlock.java#L78) **`canAttack(Char enemy)`**: 조건 판정 / 참조 호출: super.canAttack, Ballistica
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Warlock.java#L83) **`doAttack(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, Ballistica, super.doAttack, sprite.zap, zap
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Warlock.java#L105) **`zap()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: spend, Invisibility.dispel, hit, Random.Int, Buff.prolong, Sample.INSTANCE.play, Random.NormalIntRange, Math.round, AscensionChallenge.statModifier
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Warlock.java#L132) **`onZapComplete()`**: 이벤트·효과 실행 / 참조 호출: zap, next
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Warlock.java#L138) **`createLoot()`**: 생성·초기화 / 조건 분기·반복 / 참조 호출: Random.Int, PotionOfHealing, Generator.randomUsingDefaults

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 267. [`Wraith.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 176행 / 타입 1개 / 필드 3개 / 메서드 12개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L40) `class Wraith  extends Mob`

### 변수·상수 (단일 행 선언)

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L42) `float SPAWN_DELAY` 초기식: `2f`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L44) `int level`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L60) `String LEVEL` 초기식: `"level"`

### 함수·메서드 역할과 내부 연결

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L63) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L69) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, adjustStats
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L76) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L81) **`attackSkill(Char target)`**: 전투 관련
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L85) **`adjustStats(int level)`**: 개별 처리 / 참조 호출: attackSkill
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L92) **`spawningWeight()`**: 개별 처리
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L97) **`reset()`**: 생성·초기화
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L102) **`spawnAround(int pos)`**: 개별 처리 / 참조 호출: spawnAround
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L106) **`spawnAround(int pos, Class<? extends Wraith> wraithClass)`**: 개별 처리 / 반복 / 참조 호출: spawnAt
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L112) **`spawnAt(int pos)`**: 개별 처리 / 참조 호출: spawnAt
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L116) **`spawnAt(int pos, Class<? extends Wraith> wraithClass)`**: 개별 처리 / 참조 호출: spawnAt
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java#L120) **`spawnAt(int pos, Class<? extends Wraith> wraithClass, boolean allowAdjacent)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.findChar, candidates.add, candidates.isEmpty, Random.element, RatSkull.exoticChanceMultiplier, Random.Float, TormentedSpirit, Wraith, Reflection.newInstance

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 268. [`YogDzewa.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 694행 / 타입 5개 / 필드 14개 / 메서드 24개.

### 타입·상속 선언

- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L67) `class YogDzewa  extends Mob`
- [L641](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L641) `class Larva  extends Mob`
- [L675](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L675) `class YogRipper  extends RipperDemon`
- [L681](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L681) `class YogEye  extends Eye`
- [L687](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L687) `class YogScorpio  extends Scorpio`

### 변수·상수 (단일 행 선언)

- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L87) `int phase` 초기식: `0`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L89) `float abilityCooldown`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L90) `int MIN_ABILITY_CD` 초기식: `10`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L91) `int MAX_ABILITY_CD` 초기식: `15`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L93) `float summonCooldown`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L94) `int MIN_SUMMON_CD` 초기식: `10`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L95) `int MAX_SUMMON_CD` 초기식: `15`
- [L587](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L587) `String PHASE` 초기식: `"phase"`
- [L589](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L589) `String ABILITY_CD` 초기식: `"ability_cd"`
- [L590](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L590) `String SUMMON_CD` 초기식: `"summon_cd"`
- [L592](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L592) `String FIST_SUMMONS` 초기식: `"fist_summons"`
- [L593](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L593) `String REGULAR_SUMMONS` 초기식: `"regular_summons"`
- [L594](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L594) `String CHALLENGE_SUMMONS` 초기식: `"challenges_summons"`
- [L596](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L596) `String TARGETED_CELLS` 초기식: `"targeted_cells"`

### 함수·메서드 역할과 내부 연결

- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L97) **`getPairedFist(Class fist)`**: 조회·탐색 / 조건 분기
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L156) **`attackSkill(Char target)`**: 전투 관련
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L161) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.length, Dungeon.level.updateFieldOfView, throwItems, sprite.hideAlert, sprite.hideLost, chooseEnemy, enemy.isAlive, Dungeon.level.distance, Dungeon.observe
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L359) **`processFistDeath()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: findFist, yell, Messages.get, BossHealthBar.bleed, Game.runOnRenderThread, Callback, call, Music.INSTANCE.fadeOut, Music.INSTANCE.play
- [L369](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L369) **`call()`**: 개별 처리 / 참조 호출: Music.INSTANCE.fadeOut, Callback, call, Music.INSTANCE.play
- [L372](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L372) **`call()`**: 개별 처리 / 참조 호출: Music.INSTANCE.play
- [L382](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L382) **`isAlive()`**: 조건 판정 / 참조 호출: super.isAlive
- [L387](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L387) **`isInvulnerable(Class effect)`**: 조건 판정 / 참조 호출: findFist, super.isInvulnerable
- [L392](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L392) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: super.damage, findFist, Math.max, updateVisibility, GLog.n, Messages.get, sprite.showStatus, addFist, Reflection.newInstance
- [L442](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L442) **`addFist(YogFist fist)`**: 상태 갱신 / 조건 분기 / 참조 호출: Dungeon.level.exit, CellEmitter.get, burst, Dungeon.level.width, Dungeon.isChallenged, Actor.findChar, die, GameScene.add, Actor.add
- [L474](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L474) **`updateVisibility(Level level)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: isAlive, Math.max, Dungeon.isChallenged, Math.min, Dungeon.hero.buff, Dungeon.observe
- [L491](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L491) **`findFist()`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: Actor.chars
- [L501](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L501) **`beckon(int cell)`**: 개별 처리
- [L505](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L505) **`clearEnemy()`**: 상태 갱신
- [L510](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L510) **`aggro(Char ch)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: level.mobs.clone, Dungeon.level.distance, mob.aggro
- [L523](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L523) **`die(Object cause)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: level.mobs.clone, mob.die, updateVisibility, GameScene.bossSlain, Dungeon.isChallenged, Badges.validateBossChallengeCompleted, Badges.validateTakingTheMick, Dungeon.level.unseal, super.die
- [L553](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L553) **`notice()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: BossHealthBar.isAssigned, BossHealthBar.assignBoss, yell, Messages.get, Actor.chars, sayBoss, Game.runOnRenderThread, Callback, call
- [L564](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L564) **`call()`**: 개별 처리 / 참조 호출: Music.INSTANCE.play
- [L577](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L577) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: super.description, Messages.get
- [L599](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L599) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 반복 / 참조 호출: super.storeInBundle, bundle.put, fistSummons.toArray, challengeSummons.toArray, regularSummons.toArray, targetedCells.size, targetedCells.get
- [L618](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L618) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: super.restoreFromBundle, bundle.getInt, BossHealthBar.assignBoss, BossHealthBar.bleed, bundle.getFloat, fistSummons.clear, Collections.addAll, bundle.getClassArray, challengeSummons.clear
- [L658](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L658) **`attackSkill(Char target)`**: 전투 관련
- [L663](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L663) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L668](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogDzewa.java#L668) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 269. [`YogFist.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 646행 / 타입 9개 / 필드 4개 / 메서드 36개.

### 타입·상속 선언

- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L65) `class YogFist  extends Mob`
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L216) `class BurningFist  extends YogFist`
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L289) `class SoiledFist  extends YogFist`
- [L399](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L399) `class RottingFist  extends YogFist`
- [L466](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L466) `class RustedFist  extends YogFist`
- [L501](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L501) `class BrightFist  extends YogFist`
- [L517](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L517) `class LightBeam`
- [L569](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L569) `class DarkFist  extends YogFist`
- [L583](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L583) `class DarkBolt`

### 변수·상수 (단일 행 선언)

- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L83) `float rangedCooldown`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L84) `boolean canRangedInMelee` 초기식: `true`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L112) `boolean invulnWarned` 초기식: `false`
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L202) `String RANGED_COOLDOWN` 초기식: `"ranged_cooldown"`

### 함수·메서드 역할과 내부 연결

- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L86) **`incrementRangedCooldown()`**: 개별 처리 / 참조 호출: Random.NormalFloat
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L91) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: beckon, super.act
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L104) **`canAttack(Char enemy)`**: 조건 판정 / 조건 분기 / 참조 호출: Ballistica, super.canAttack
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L114) **`isNearYog()`**: 조건 판정 / 참조 호출: Dungeon.level.exit, Dungeon.level.width, Dungeon.level.distance
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L120) **`isInvulnerable(Class effect)`**: 조건 판정 / 조건 분기 / 참조 호출: isNearYog, GLog.w, Messages.get, super.isInvulnerable
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L129) **`doAttack(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, super.doAttack, incrementRangedCooldown, sprite.zap, zap
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L149) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: super.damage, Dungeon.hero.buff, isImmune, src.getClass, isInvulnerable, Dungeon.isChallenged, lock.addTime
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L162) **`die(Object cause)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.die, Actor.chars, processFistDeath
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L171) **`zap()`**: 이벤트·효과 실행
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L173) **`onZapComplete()`**: 이벤트·효과 실행 / 참조 호출: zap, next
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L179) **`attackSkill(Char target)`**: 전투 관련
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L184) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L189) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L198) **`description()`**: 개별 처리 / 참조 호출: Messages.get
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L205) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L211) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getFloat
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L225) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: super.act, Level.set, GameScene.updateMap, CellEmitter.get, burst, Speck.factory, Random.chances, Random.Int, Fire.volumeAt
- [L258](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L258) **`zap()`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: spend, Level.set, GameScene.updateMap, CellEmitter.get, burst, Speck.factory, Buff.affect, reignite, Fire.volumeAt
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L296) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: super.act, Random.chances, Random.Int, Level.set, GameScene.updateMap, CellEmitter.get, burst, Dungeon.observe, canSpreadGrass
- [L326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L326) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: Math.round, src.getClass, super.damage
- [L345](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L345) **`incomingDOT()`**: 개별 처리 / 조건 분기 / 참조 호출: super.incomingDOT, buff, b.totalIncomingDMG
- [L360](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L360) **`zap()`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: spend, Invisibility.dispel, hit, Buff.affect, enemy.sprite.showStatus, enemy.defenseVerb, canSpreadGrass, Random.Int, Level.set
- [L391](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L391) **`canSpreadGrass(int cell)`**: 조건 판정 / 참조 호출: Dungeon.level.exit, Dungeon.level.width, Dungeon.level.distance
- [L408](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L408) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: GameScene.add, Blob.seed, sprite.showStatusWithIcon, Integer.toString, Math.min, super.act
- [L421](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L421) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: isInvulnerable, src.getClass, buff, Math.round, resist, Bleeding, b.attachTo, b.set, sprite.showStatus
- [L443](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L443) **`zap()`**: 이벤트·효과 실행 / 참조 호출: spend, GameScene.add, Blob.seed
- [L449](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L449) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, Random.Int, Buff.affect, set, enemy.sprite.burst
- [L476](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L476) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L481](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L481) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: isInvulnerable, src.getClass, Math.round, resist, Buff.affect, extend, sprite.showStatus, Messages.get, super.damage
- [L494](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L494) **`zap()`**: 이벤트·효과 실행 / 참조 호출: spend, Buff.affect
- [L512](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L512) **`incrementRangedCooldown()`**: 개별 처리
- [L520](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L520) **`zap()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: spend, Invisibility.dispel, hit, enemy.damage, Random.NormalIntRange, LightBeam, Buff.prolong, enemy.isAlive, Badges.validateDeathFromEnemyMagic
- [L544](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L544) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: super.damage, isAlive, Buff.prolong, Random.Int, Dungeon.level.length, Actor.findChar, PathFinder.getStep, Dungeon.level.exit, ScrollOfTeleportation.appear
- [L578](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L578) **`incrementRangedCooldown()`**: 개별 처리
- [L586](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L586) **`zap()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: spend, Invisibility.dispel, hit, enemy.damage, Random.NormalIntRange, DarkBolt, enemy.buff, l.weaken, enemy.isAlive
- [L614](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java#L614) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: super.damage, isAlive, Dungeon.hero.buff, l.detach, Random.Int, Dungeon.level.length, Actor.findChar, PathFinder.getStep, Dungeon.level.exit

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 270. [`Assets.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon` / 본문 351행 / 타입 11개 / 필드 255개 / 메서드 0개.

### 타입·상속 선언

- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L24) `class Assets`
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L26) `class Effects`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L34) `class Environment`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L71) `class Fonts`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L75) `class Interfaces`
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L108) `class Messages`
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L120) `class Music`
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L159) `class Sounds`
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L246) `class Splashes`
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L260) `class Title`
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L268) `class Sprites`

### 변수·상수 (단일 행 선언)

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L27) `String EFFECTS` 초기식: `"effects/effects.png"`
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L28) `String FIREBALL` 초기식: `"effects/fireball.png"`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L29) `String SPECKS` 초기식: `"effects/specks.png"`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L30) `String SPELL_ICONS` 초기식: `"effects/spell_icons.png"`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L31) `String TEXT_ICONS` 초기식: `"effects/text_icons.png"`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L35) `String TERRAIN_FEATURES` 초기식: `"environment/terrain_features.png"`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L36) `String RAISED_TERRAIN` 초기식: `"environment/raised_terrain.png"`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L38) `String VISUAL_GRID` 초기식: `"environment/visual_grid.png"`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L39) `String WALL_BLOCKING` 초기식: `"environment/wall_blocking.png"`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L40) `String OCCLUSION_SHADOWS` 초기식: `"environment/occlusion_shadows.png"`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L42) `String TILES_SEWERS` 초기식: `"environment/tiles_sewers.png"`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L43) `String TILES_PRISON` 초기식: `"environment/tiles_prison.png"`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L44) `String TILES_CAVES` 초기식: `"environment/tiles_caves.png"`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L45) `String TILES_CITY` 초기식: `"environment/tiles_city.png"`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L46) `String TILES_HALLS` 초기식: `"environment/tiles_halls.png"`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L48) `String TILES_CAVES_CRYSTAL` 초기식: `"environment/tiles_caves_crystal.png"`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L49) `String TILES_CAVES_GNOLL` 초기식: `"environment/tiles_caves_gnoll.png"`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L51) `String WATER_SEWERS` 초기식: `"environment/water0.png"`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L52) `String WATER_PRISON` 초기식: `"environment/water1.png"`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L53) `String WATER_CAVES` 초기식: `"environment/water2.png"`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L54) `String WATER_CITY` 초기식: `"environment/water3.png"`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L55) `String WATER_HALLS` 초기식: `"environment/water4.png"`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L57) `String CARPET` 초기식: `"environment/custom_tiles/carpet.png"`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L58) `String RAT_KING_ROOM` 초기식: `"environment/custom_tiles/rat_king_room.png"`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L59) `String WEAK_FLOOR` 초기식: `"environment/custom_tiles/weak_floor.png"`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L60) `String SEWER_BOSS` 초기식: `"environment/custom_tiles/sewer_boss.png"`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L61) `String PRISON_QUEST` 초기식: `"environment/custom_tiles/prison_quest.png"`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L62) `String PRISON_EXIT` 초기식: `"environment/custom_tiles/prison_exit.png"`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L63) `String CAVES_QUEST` 초기식: `"environment/custom_tiles/caves_quest.png"`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L64) `String CAVES_BOSS` 초기식: `"environment/custom_tiles/caves_boss.png"`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L65) `String CITY_QUEST` 초기식: `"environment/custom_tiles/city_quest.png"`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L66) `String CITY_BOSS` 초기식: `"environment/custom_tiles/city_boss.png"`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L67) `String HALLS_SP` 초기식: `"environment/custom_tiles/halls_special.png"`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L72) `String PIXELFONT` 초기식: `"fonts/pixel_font.png"`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L76) `String ARCS_BG` 초기식: `"interfaces/arcs1.png"`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L77) `String ARCS_FG` 초기식: `"interfaces/arcs2.png"`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L79) `String BANNERS` 초기식: `"interfaces/banners.png"`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L80) `String BADGES` 초기식: `"interfaces/badges.png"`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L81) `String LOCKED` 초기식: `"interfaces/locked_badge.png"`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L83) `String CHROME` 초기식: `"interfaces/chrome.png"`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L84) `String ICONS` 초기식: `"interfaces/icons.png"`
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L85) `String STATUS` 초기식: `"interfaces/status_pane.png"`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L86) `String MENU` 초기식: `"interfaces/menu_pane.png"`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L87) `String MENU_BTN` 초기식: `"interfaces/menu_button.png"`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L88) `String TOOLBAR` 초기식: `"interfaces/toolbar.png"`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L89) `String SHADOW` 초기식: `"interfaces/shadow.png"`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L90) `String BOSSHP` 초기식: `"interfaces/boss_hp.png"`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L92) `String SURFACE` 초기식: `"interfaces/surface.png"`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L94) `String BUFFS_SMALL` 초기식: `"interfaces/buffs.png"`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L95) `String BUFFS_LARGE` 초기식: `"interfaces/large_buffs.png"`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L97) `String TALENT_ICONS` 초기식: `"interfaces/talent_icons.png"`
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L98) `String TALENT_BUTTON` 초기식: `"interfaces/talent_button.png"`
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L100) `String HERO_ICONS` 초기식: `"interfaces/hero_icons.png"`
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L102) `String RADIAL_MENU` 초기식: `"interfaces/radial_menu.png"`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L104) `String CHANGE_ICONS` 초기식: `"interfaces/change_icons.png"`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L109) `String ACTORS` 초기식: `"messages/actors/actors"`
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L110) `String ITEMS` 초기식: `"messages/items/items"`
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L111) `String JOURNAL` 초기식: `"messages/journal/journal"`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L112) `String LEVELS` 초기식: `"messages/levels/levels"`
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L113) `String MISC` 초기식: `"messages/misc/misc"`
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L114) `String PLANTS` 초기식: `"messages/plants/plants"`
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L115) `String SCENES` 초기식: `"messages/scenes/scenes"`
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L116) `String UI` 초기식: `"messages/ui/ui"`
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L117) `String WINDOWS` 초기식: `"messages/windows/windows"`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L121) `String THEME_1` 초기식: `"music/theme_1.ogg"`
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L122) `String THEME_2` 초기식: `"music/theme_2.ogg"`
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L123) `String THEME_FINALE` 초기식: `"music/theme_finale.ogg"`
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L125) `String SEWERS_1` 초기식: `"music/sewers_1.ogg"`
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L126) `String SEWERS_2` 초기식: `"music/sewers_2.ogg"`
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L127) `String SEWERS_3` 초기식: `"music/sewers_3.ogg"`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L128) `String SEWERS_TENSE` 초기식: `"music/sewers_tense.ogg"`
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L129) `String SEWERS_BOSS` 초기식: `"music/sewers_boss.ogg"`
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L131) `String PRISON_1` 초기식: `"music/prison_1.ogg"`
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L132) `String PRISON_2` 초기식: `"music/prison_2.ogg"`
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L133) `String PRISON_3` 초기식: `"music/prison_3.ogg"`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L134) `String PRISON_TENSE` 초기식: `"music/prison_tense.ogg"`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L135) `String PRISON_BOSS` 초기식: `"music/prison_boss.ogg"`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L137) `String CAVES_1` 초기식: `"music/caves_1.ogg"`
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L138) `String CAVES_2` 초기식: `"music/caves_2.ogg"`
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L139) `String CAVES_3` 초기식: `"music/caves_3.ogg"`
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L140) `String CAVES_TENSE` 초기식: `"music/caves_tense.ogg"`
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L141) `String CAVES_BOSS` 초기식: `"music/caves_boss.ogg"`
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L142) `String CAVES_BOSS_FINALE` 초기식: `"music/caves_boss_finale.ogg"`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L144) `String CITY_1` 초기식: `"music/city_1.ogg"`
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L145) `String CITY_2` 초기식: `"music/city_2.ogg"`
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L146) `String CITY_3` 초기식: `"music/city_3.ogg"`
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L147) `String CITY_TENSE` 초기식: `"music/city_tense.ogg"`
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L148) `String CITY_BOSS` 초기식: `"music/city_boss.ogg"`
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L149) `String CITY_BOSS_FINALE` 초기식: `"music/city_boss_finale.ogg"`
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L151) `String HALLS_1` 초기식: `"music/halls_1.ogg"`
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L152) `String HALLS_2` 초기식: `"music/halls_2.ogg"`
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L153) `String HALLS_3` 초기식: `"music/halls_3.ogg"`
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L154) `String HALLS_TENSE` 초기식: `"music/halls_tense.ogg"`
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L155) `String HALLS_BOSS` 초기식: `"music/halls_boss.ogg"`
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L156) `String HALLS_BOSS_FINALE` 초기식: `"music/halls_boss_finale.ogg"`
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L160) `String CLICK` 초기식: `"sounds/click.mp3"`
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L161) `String BADGE` 초기식: `"sounds/badge.mp3"`
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L162) `String GOLD` 초기식: `"sounds/gold.mp3"`
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L164) `String OPEN` 초기식: `"sounds/door_open.mp3"`
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L165) `String UNLOCK` 초기식: `"sounds/unlock.mp3"`
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L166) `String ITEM` 초기식: `"sounds/item.mp3"`
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L167) `String DEWDROP` 초기식: `"sounds/dewdrop.mp3"`
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L168) `String STEP` 초기식: `"sounds/step.mp3"`
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L169) `String WATER` 초기식: `"sounds/water.mp3"`
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L170) `String GRASS` 초기식: `"sounds/grass.mp3"`
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L171) `String TRAMPLE` 초기식: `"sounds/trample.mp3"`
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L172) `String STURDY` 초기식: `"sounds/sturdy.mp3"`
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L174) `String HIT` 초기식: `"sounds/hit.mp3"`
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L175) `String MISS` 초기식: `"sounds/miss.mp3"`
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L176) `String HIT_SLASH` 초기식: `"sounds/hit_slash.mp3"`
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L177) `String HIT_STAB` 초기식: `"sounds/hit_stab.mp3"`
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L178) `String HIT_CRUSH` 초기식: `"sounds/hit_crush.mp3"`
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L179) `String HIT_MAGIC` 초기식: `"sounds/hit_magic.mp3"`
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L180) `String HIT_STRONG` 초기식: `"sounds/hit_strong.mp3"`
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L181) `String HIT_PARRY` 초기식: `"sounds/hit_parry.mp3"`
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L182) `String HIT_ARROW` 초기식: `"sounds/hit_arrow.mp3"`
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L183) `String ATK_SPIRITBOW` 초기식: `"sounds/atk_spiritbow.mp3"`
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L184) `String ATK_CROSSBOW` 초기식: `"sounds/atk_crossbow.mp3"`
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L185) `String HEALTH_WARN` 초기식: `"sounds/health_warn.mp3"`
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L186) `String HEALTH_CRITICAL` 초기식: `"sounds/health_critical.mp3"`
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L188) `String DESCEND` 초기식: `"sounds/descend.mp3"`
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L189) `String EAT` 초기식: `"sounds/eat.mp3"`
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L190) `String READ` 초기식: `"sounds/read.mp3"`
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L191) `String LULLABY` 초기식: `"sounds/lullaby.mp3"`
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L192) `String DRINK` 초기식: `"sounds/drink.mp3"`
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L193) `String SHATTER` 초기식: `"sounds/shatter.mp3"`
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L194) `String ZAP` 초기식: `"sounds/zap.mp3"`
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L195) `String LIGHTNING` 초기식: `"sounds/lightning.mp3"`
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L196) `String LEVELUP` 초기식: `"sounds/levelup.mp3"`
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L197) `String DEATH` 초기식: `"sounds/death.mp3"`
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L198) `String CHALLENGE` 초기식: `"sounds/challenge.mp3"`
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L199) `String CURSED` 초기식: `"sounds/cursed.mp3"`
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L200) `String TRAP` 초기식: `"sounds/trap.mp3"`
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L201) `String EVOKE` 초기식: `"sounds/evoke.mp3"`
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L202) `String TOMB` 초기식: `"sounds/tomb.mp3"`
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L203) `String ALERT` 초기식: `"sounds/alert.mp3"`
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L204) `String MELD` 초기식: `"sounds/meld.mp3"`
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L205) `String BOSS` 초기식: `"sounds/boss.mp3"`
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L206) `String BLAST` 초기식: `"sounds/blast.mp3"`
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L207) `String PLANT` 초기식: `"sounds/plant.mp3"`
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L208) `String RAY` 초기식: `"sounds/ray.mp3"`
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L209) `String BEACON` 초기식: `"sounds/beacon.mp3"`
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L210) `String TELEPORT` 초기식: `"sounds/teleport.mp3"`
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L211) `String CHARMS` 초기식: `"sounds/charms.mp3"`
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L212) `String MASTERY` 초기식: `"sounds/mastery.mp3"`
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L213) `String PUFF` 초기식: `"sounds/puff.mp3"`
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L214) `String ROCKS` 초기식: `"sounds/rocks.mp3"`
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L215) `String BURNING` 초기식: `"sounds/burning.mp3"`
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L216) `String FALLING` 초기식: `"sounds/falling.mp3"`
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L217) `String GHOST` 초기식: `"sounds/ghost.mp3"`
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L218) `String SECRET` 초기식: `"sounds/secret.mp3"`
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L219) `String BONES` 초기식: `"sounds/bones.mp3"`
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L220) `String BEE` 초기식: `"sounds/bee.mp3"`
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L221) `String DEGRADE` 초기식: `"sounds/degrade.mp3"`
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L222) `String MIMIC` 초기식: `"sounds/mimic.mp3"`
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L223) `String DEBUFF` 초기식: `"sounds/debuff.mp3"`
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L224) `String CHARGEUP` 초기식: `"sounds/chargeup.mp3"`
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L225) `String GAS` 초기식: `"sounds/gas.mp3"`
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L226) `String CHAINS` 초기식: `"sounds/chains.mp3"`
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L227) `String SCAN` 초기식: `"sounds/scan.mp3"`
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L228) `String SHEEP` 초기식: `"sounds/sheep.mp3"`
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L229) `String MINE` 초기식: `"sounds/mine.mp3"`
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L247) `String WARRIOR` 초기식: `"splashes/warrior.jpg"`
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L248) `String MAGE` 초기식: `"splashes/mage.jpg"`
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L249) `String ROGUE` 초기식: `"splashes/rogue.jpg"`
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L250) `String HUNTRESS` 초기식: `"splashes/huntress.jpg"`
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L251) `String DUELIST` 초기식: `"splashes/duelist.jpg"`
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L252) `String CLERIC` 초기식: `"splashes/cleric.jpg"`
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L254) `String SEWERS` 초기식: `"splashes/sewers.jpg"`
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L255) `String PRISON` 초기식: `"splashes/prison.jpg"`
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L256) `String CAVES` 초기식: `"splashes/caves.jpg"`
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L257) `String CITY` 초기식: `"splashes/city.jpg"`
- [L258](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L258) `String HALLS` 초기식: `"splashes/halls.jpg"`
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L261) `String ARCHS` 초기식: `"splashes/title/archs.png"`
- [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L262) `String BACK_CLUSTERS` 초기식: `"splashes/title/back_clusters.png"`
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L263) `String MID_MIXED` 초기식: `"splashes/title/mid_mixed.png"`
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L264) `String FRONT_SMALL` 초기식: `"splashes/title/front_small.png"`
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L269) `String ITEMS` 초기식: `"sprites/items.png"`
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L270) `String ITEM_ICONS` 초기식: `"sprites/item_icons.png"`
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L272) `String WARRIOR` 초기식: `"sprites/warrior.png"`
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L273) `String MAGE` 초기식: `"sprites/mage.png"`
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L274) `String ROGUE` 초기식: `"sprites/rogue.png"`
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L275) `String HUNTRESS` 초기식: `"sprites/huntress.png"`
- [L276](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L276) `String DUELIST` 초기식: `"sprites/duelist.png"`
- [L277](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L277) `String CLERIC` 초기식: `"sprites/cleric.png"`
- [L278](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L278) `String AVATARS` 초기식: `"sprites/avatars.png"`
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L279) `String PET` 초기식: `"sprites/pet.png"`
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L280) `String AMULET` 초기식: `"sprites/amulet.png"`
- [L282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L282) `String RAT` 초기식: `"sprites/rat.png"`
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L283) `String BRUTE` 초기식: `"sprites/brute.png"`
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L284) `String SPINNER` 초기식: `"sprites/spinner.png"`
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L285) `String DM300` 초기식: `"sprites/dm300.png"`
- [L286](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L286) `String WRAITH` 초기식: `"sprites/wraith.png"`
- [L287](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L287) `String UNDEAD` 초기식: `"sprites/undead.png"`
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L288) `String KING` 초기식: `"sprites/king.png"`
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L289) `String PIRANHA` 초기식: `"sprites/piranha.png"`
- [L290](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L290) `String EYE` 초기식: `"sprites/eye.png"`
- [L291](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L291) `String GNOLL` 초기식: `"sprites/gnoll.png"`
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L292) `String CRAB` 초기식: `"sprites/crab.png"`
- [L293](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L293) `String GOO` 초기식: `"sprites/goo.png"`
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L294) `String SWARM` 초기식: `"sprites/swarm.png"`
- [L295](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L295) `String SKELETON` 초기식: `"sprites/skeleton.png"`
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L296) `String SHAMAN` 초기식: `"sprites/shaman.png"`
- [L297](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L297) `String THIEF` 초기식: `"sprites/thief.png"`
- [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L298) `String TENGU` 초기식: `"sprites/tengu.png"`
- [L299](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L299) `String SHEEP` 초기식: `"sprites/sheep.png"`
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L300) `String KEEPER` 초기식: `"sprites/shopkeeper.png"`
- [L301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L301) `String BAT` 초기식: `"sprites/bat.png"`
- [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L302) `String ELEMENTAL` 초기식: `"sprites/elemental.png"`
- [L303](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L303) `String MONK` 초기식: `"sprites/monk.png"`
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L304) `String WARLOCK` 초기식: `"sprites/warlock.png"`
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L305) `String GOLEM` 초기식: `"sprites/golem.png"`
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L306) `String STATUE` 초기식: `"sprites/statue.png"`
- [L307](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L307) `String SUCCUBUS` 초기식: `"sprites/succubus.png"`
- [L308](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L308) `String SCORPIO` 초기식: `"sprites/scorpio.png"`
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L309) `String FISTS` 초기식: `"sprites/yog_fists.png"`
- [L310](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L310) `String YOG` 초기식: `"sprites/yog.png"`
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L311) `String LARVA` 초기식: `"sprites/larva.png"`
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L312) `String GHOST` 초기식: `"sprites/ghost.png"`
- [L313](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L313) `String MAKER` 초기식: `"sprites/wandmaker.png"`
- [L314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L314) `String TROLL` 초기식: `"sprites/blacksmith.png"`
- [L315](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L315) `String IMP` 초기식: `"sprites/imp.png"`
- [L316](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L316) `String RATKING` 초기식: `"sprites/ratking.png"`
- [L317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L317) `String BEE` 초기식: `"sprites/bee.png"`
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L318) `String MIMIC` 초기식: `"sprites/mimic.png"`
- [L319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L319) `String ROT_LASH` 초기식: `"sprites/rot_lasher.png"`
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L320) `String ROT_HEART` 초기식: `"sprites/rot_heart.png"`
- [L321](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L321) `String GUARD` 초기식: `"sprites/guard.png"`
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L322) `String WARDS` 초기식: `"sprites/wards.png"`
- [L323](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L323) `String GUARDIAN` 초기식: `"sprites/guardian.png"`
- [L324](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L324) `String SLIME` 초기식: `"sprites/slime.png"`
- [L325](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L325) `String SNAKE` 초기식: `"sprites/snake.png"`
- [L326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L326) `String NECRO` 초기식: `"sprites/necromancer.png"`
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L327) `String GHOUL` 초기식: `"sprites/ghoul.png"`
- [L328](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L328) `String RIPPER` 초기식: `"sprites/ripper.png"`
- [L329](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L329) `String SPAWNER` 초기식: `"sprites/spawner.png"`
- [L330](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L330) `String DM100` 초기식: `"sprites/dm100.png"`
- [L331](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L331) `String PYLON` 초기식: `"sprites/pylon.png"`
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L332) `String DM200` 초기식: `"sprites/dm200.png"`
- [L333](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L333) `String LOTUS` 초기식: `"sprites/lotus.png"`
- [L334](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L334) `String NINJA_LOG` 초기식: `"sprites/ninja_log.png"`
- [L335](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L335) `String SPIRIT_HAWK` 초기식: `"sprites/spirit_hawk.png"`
- [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L336) `String SENTRY` 초기식: `"sprites/sentry.png"`
- [L337](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L337) `String CRYSTAL_WISP` 초기식: `"sprites/crystal_wisp.png"`
- [L338](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L338) `String CRYSTAL_GUARDIAN` 초기식: `"sprites/crystal_guardian.png"`
- [L339](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L339) `String CRYSTAL_SPIRE` 초기식: `"sprites/crystal_spire.png"`
- [L340](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L340) `String GNOLL_GUARD` 초기식: `"sprites/gnoll_guard.png"`
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L341) `String GNOLL_SAPPER` 초기식: `"sprites/gnoll_sapper.png"`
- [L342](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L342) `String GNOLL_GEOMANCER` 초기식: `"sprites/gnoll_geomancer.png"`
- [L343](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L343) `String FUNGAL_SPINNER` 초기식: `"sprites/fungal_spinner.png"`
- [L344](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L344) `String FUNGAL_SENTRY` 초기식: `"sprites/fungal_sentry.png"`
- [L345](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L345) `String FUNGAL_CORE` 초기식: `"sprites/fungal_core.png"`
- [L346](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L346) `String VAULT_TOKENS_DOOR` 초기식: `"sprites/vault_tokens_door.png"`
- [L347](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L347) `String VAULT_MIRROR` 초기식: `"sprites/vault_mirror.png"`
- [L348](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java#L348) `String VAULT_BOSS_ELEMENTAL` 초기식: `"sprites/vault_boss_elemental.png"`

### 함수·메서드 역할과 내부 연결

- 검출 없음

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 271. [`Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon` / 본문 1390행 / 타입 3개 / 필드 7개 / 메서드 64개.

### 타입·상속 선언

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L58) `class Badges`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L60) `enum BadgeType`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L67) `enum Badge`

### 변수·상수 (단일 행 선언)

- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L212) `boolean meta`
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L214) `int image`
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L215) `BadgeType type`
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L239) `HashSet<Badge> global`
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L242) `boolean saveNeeded` 초기식: `false`
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L249) `String BADGES_FILE` 초기식: `"badges.dat"`
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L250) `String BADGES` 초기식: `"badges"`

### 함수·메서드 역할과 내부 연결

- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L230) **`title()`**: 개별 처리 / 참조 호출: Messages.get, name
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L234) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, name
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L244) **`reset()`**: 생성·초기화 / 참조 호출: local.clear, loadGlobal
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L270) **`restore(Bundle bundle)`**: 저장·복원 / 조건 분기·반복·예외 처리 / 참조 호출: bundle.getStringArray, renamedBadges.containsKey, renamedBadges.get, removedBadges.contains, badges.add, Badge.valueOf, ShatteredPixelDungeon.reportException, addReplacedBadges
- [L295](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L295) **`store(Bundle bundle, HashSet<Badge> badges)`**: 저장·복원 / 반복 / 참조 호출: addReplacedBadges, badges.size, badge.name, bundle.put
- [L307](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L307) **`loadLocal(Bundle bundle)`**: 저장·복원 / 참조 호출: restore
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L311) **`saveLocal(Bundle bundle)`**: 저장·복원 / 참조 호출: store
- [L315](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L315) **`loadGlobal()`**: 저장·복원 / 조건 분기·예외 처리 / 참조 호출: FileUtils.bundleFromFile, restore
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L327) **`saveGlobal()`**: 저장·복원 / 참조 호출: saveGlobal
- [L331](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L331) **`saveGlobal(boolean force)`**: 저장·복원 / 조건 분기·예외 처리 / 참조 호출: Bundle, store, FileUtils.bundleToFile, ShatteredPixelDungeon.reportException
- [L346](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L346) **`totalUnlocked(boolean global)`**: 개별 처리 / 조건 분기 / 참조 호출: Badges.global.size, Badges.local.size
- [L351](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L351) **`validateMonstersSlain()`**: 개별 처리 / 조건 분기 / 참조 호출: local.contains, local.add, unlock, displayBadge
- [L382](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L382) **`validateGoldCollected()`**: 개별 처리 / 조건 분기 / 참조 호출: local.contains, unlock, local.add, displayBadge
- [L414](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L414) **`validateLevelReached()`**: 개별 처리 / 조건 분기 / 참조 호출: local.contains, local.add, unlock, displayBadge
- [L445](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L445) **`validateStrengthAttained()`**: 개별 처리 / 조건 분기 / 참조 호출: local.contains, local.add, unlock, displayBadge
- [L476](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L476) **`validateFoodEaten()`**: 개별 처리 / 조건 분기 / 참조 호출: local.contains, local.add, unlock, displayBadge
- [L507](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L507) **`validateItemsCrafted()`**: 개별 처리 / 조건 분기 / 참조 호출: local.contains, local.add, unlock, displayBadge
- [L538](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L538) **`validateHazardAssists()`**: 개별 처리 / 조건 분기 / 참조 호출: local.contains, local.add, displayBadge
- [L545](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L545) **`validatePiranhasKilled()`**: 개별 처리 / 조건 분기 / 참조 호출: local.contains, local.add, displayBadge
- [L556](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L556) **`validateItemLevelAquired(Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: validateDuelistUnlock, local.contains, item.level, local.add, unlock, displayBadge
- [L601](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L601) **`validateAllBagsBought(Item bag)`**: 개별 처리 / 조건 분기 / 참조 호출: local.add, local.contains, displayBadge
- [L632](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L632) **`validateCatalogBadges()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Catalog.values, cat.totalSeen, cat.totalItems, Bestiary.values, cat.totalEntities, Document.values, doc.isLoreDoc, doc.pageNames, doc.isPageFound
- [L712](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L712) **`validateDeathFromFire()`**: 개별 처리 / 참조 호출: local.add, displayBadge, validateDeathFromAll
- [L720](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L720) **`validateDeathFromPoison()`**: 개별 처리 / 참조 호출: local.add, displayBadge, validateDeathFromAll
- [L728](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L728) **`validateDeathFromGas()`**: 개별 처리 / 참조 호출: local.add, displayBadge, validateDeathFromAll
- [L736](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L736) **`validateDeathFromHunger()`**: 개별 처리 / 참조 호출: local.add, displayBadge, validateDeathFromAll
- [L744](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L744) **`validateDeathFromFalling()`**: 개별 처리 / 참조 호출: local.add, displayBadge, validateDeathFromAll
- [L752](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L752) **`validateDeathFromEnemyMagic()`**: 개별 처리 / 참조 호출: local.add, displayBadge, validateDeathFromAll
- [L760](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L760) **`validateDeathFromFriendlyMagic()`**: 개별 처리 / 참조 호출: local.add, displayBadge, validateDeathFromAll
- [L768](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L768) **`validateDeathFromSacrifice()`**: 개별 처리 / 참조 호출: local.add, displayBadge, validateDeathFromAll
- [L776](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L776) **`validateDeathFromGrimOrDisintTrap()`**: 개별 처리 / 참조 호출: local.add, displayBadge, validateDeathFromAll
- [L784](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L784) **`validateDeathFromAll()`**: 개별 처리 / 조건 분기 / 참조 호출: isUnlocked, displayBadge
- [L838](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L838) **`validateBossSlain()`**: 개별 처리 / 조건 분기·반복·상태 선택 / 참조 호출: local.add, displayBadge, firstBossClassBadges.get, unlock, firstBossClassBadges.values, isUnlocked, thirdBossSubclassBadges.get, thirdBossSubclassBadges.values, hero.belongings.getItem
- [L910](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L910) **`validateBossChallengeCompleted()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: local.add, displayBadge
- [L936](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L936) **`validateMastery()`**: 개별 처리 / 상태 선택 / 참조 호출: unlock
- [L963](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L963) **`validateRatmogrify()`**: 개별 처리 / 참조 호출: unlock
- [L967](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L967) **`validateMageUnlock()`**: 개별 처리 / 조건 분기 / 참조 호출: isUnlocked, displayBadge
- [L973](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L973) **`validateRogueUnlock()`**: 개별 처리 / 조건 분기 / 참조 호출: isUnlocked, displayBadge
- [L979](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L979) **`validateHuntressUnlock()`**: 개별 처리 / 조건 분기 / 참조 호출: isUnlocked, displayBadge
- [L985](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L985) **`validateDuelistUnlock()`**: 개별 처리 / 조건 분기 / 참조 호출: isUnlocked, STRReq, Dungeon.hero.STR, belongings.weapon.isIdentified, displayBadge
- [L1002](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1002) **`validateClericUnlock()`**: 개별 처리 / 조건 분기 / 참조 호출: isUnlocked, displayBadge
- [L1008](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1008) **`validateMasteryCombo(int n)`**: 개별 처리 / 조건 분기 / 참조 호출: local.contains, local.add, displayBadge
- [L1016](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1016) **`validateVictory()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: local.add, displayBadge, victoryClassBadges.get, unlock, victoryClassBadges.values, isUnlocked
- [L1049](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1049) **`validateTakingTheMick(Object cause)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.attackingWeapon, level, local.add, displayBadge
- [L1058](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1058) **`validateNoKilling()`**: 개별 처리 / 조건 분기 / 참조 호출: local.contains, local.add, displayBadge
- [L1067](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1067) **`validateGrimWeapon()`**: 개별 처리 / 조건 분기 / 참조 호출: local.contains, local.add, displayBadge
- [L1075](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1075) **`validateManyBuffs()`**: 개별 처리 / 조건 분기 / 참조 호출: local.contains, local.add, displayBadge
- [L1083](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1083) **`validateGamesPlayed()`**: 개별 처리 / 조건 분기 / 참조 호출: unlock, displayBadge
- [L1108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1108) **`validateHighScore(int score)`**: 개별 처리 / 조건 분기 / 참조 호출: local.add, unlock, displayBadge
- [L1138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1138) **`validateHappyEnd()`**: 개별 처리 / 조건 분기 / 참조 호출: local.add, displayBadge, hero.belongings.getItem, AscensionChallenge.qualifiedForPacifist
- [L1153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1153) **`validateChampion(int challenges)`**: 개별 처리 / 조건 분기 / 참조 호출: unlock, local.add, displayBadge
- [L1171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1171) **`displayBadge(Badge badge)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.customSeedText.isEmpty, isUnlocked, GLog.h, Messages.get, badge.title, GLog.newLine, unlock, badge.desc, PixelScene.showBadge
- [L1194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1194) **`isUnlocked(Badge badge)`**: 조건 판정 / 참조 호출: global.contains
- [L1198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1198) **`allUnlocked()`**: 개별 처리 / 참조 호출: loadGlobal
- [L1203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1203) **`disown(Badge badge)`**: 개별 처리 / 참조 호출: loadGlobal, global.remove
- [L1209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1209) **`unlock(Badge badge)`**: 개별 처리 / 조건 분기 / 참조 호출: isUnlocked, Dungeon.customSeedText.isEmpty, global.add
- [L1216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1216) **`filterReplacedBadges(boolean global)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: badges.iterator, iterator.hasNext, iterator.next, iterator.remove, Collections.sort, filterReplacedBadges
- [L1276](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1276) **`filterReplacedBadges(List<Badge> badges)`**: 개별 처리 / 반복 / 참조 호출: leaveBest
- [L1289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1289) **`leaveBest(Collection<Badge> list, Badge...badges)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: list.contains, list.remove
- [L1300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1300) **`filterBadgesWithoutPrerequisites(List<Badges.Badge> badges)`**: 개별 처리 / 반복 / 참조 호출: leaveWorst, Collections.sort
- [L1315](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1315) **`leaveWorst(Collection<Badge> list, Badge...badges)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: list.contains, list.remove
- [L1326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1326) **`addReplacedBadges(Collection<Badges.Badge> badges)`**: 상태 갱신 / 반복 / 참조 호출: addLower
- [L1339](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1339) **`addLower(Collection<Badge> list, Badge...badges)`**: 상태 갱신 / 조건 분기·반복 / 참조 호출: list.contains, list.add
- [L1351](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java#L1351) **`showCompletionProgress(Badge badge)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: isUnlocked, HeroClass.values, firstBossClassBadges.get, Messages.titleCase, cls.title, victoryClassBadges.get, HeroSubClass.values, thirdBossSubclassBadges.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":53,"fields":326,"methods":283}

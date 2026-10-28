# Java 파일별 소스 구현 해설 224–239

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 224. [`ImpShopkeeper.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/ImpShopkeeper.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 52행 / 타입 1개 / 필드 1개 / 메서드 1개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/ImpShopkeeper.java#L29) `class ImpShopkeeper  extends Shopkeeper`

### 변수·상수 (단일 행 선언)

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/ImpShopkeeper.java#L35) `boolean seenBefore` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/ImpShopkeeper.java#L38) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.hero.buff, yell, Messages.get, Messages.titleCase, Dungeon.hero.name, super.act

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 225. [`MirrorImage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 233행 / 타입 2개 / 필드 4개 / 메서드 13개.

### 타입·상속 선언

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L50) `class MirrorImage  extends NPC`
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L222) `class MirrorInvis  extends Invisibility`

### 변수·상수 (단일 행 선언)

- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L65) `Hero hero`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L66) `int heroID`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L67) `int armTier`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L89) `String HEROID` 초기식: `"hero_id"`

### 함수·메서드 역할과 내부 연결

- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L70) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Actor.findById, die, sprite.killAndErase, hero.tier, updateArmor, super.act
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L92) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L98) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L103) **`duplicate(Hero hero)`**: 개별 처리 / 참조 호출: this.hero.id, Buff.affect
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L110) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: hero.belongings.weapon, damageRoll, hero.damageRoll
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L121) **`attackSkill(Char target)`**: 전투 관련 / 조건 분기 / 참조 호출: RingOfAccuracy.accuracyMultiplier, hero.belongings.attackingWeapon, accuracyFactor
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L132) **`defenseSkill(Char enemy)`**: 전투 관련 / 조건 분기 / 참조 호출: RingOfEvasion.evasionMultiplier, super.defenseSkill
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L146) **`attackDelay()`**: 전투 관련 / 참조 호출: hero.attackDelay
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L151) **`canAttack(Char enemy)`**: 조건 판정 / 참조 호출: super.canAttack, hero.belongings.weapon, canReach
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L156) **`drRoll()`**: 개별 처리 / 조건 분기 / 참조 호출: super.drRoll, hero.belongings.weapon, Random.NormalIntRange, defenseFactor
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L166) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, buff, buff.detach, aggro, hero.belongings.weapon, proc, enemy.isAlive, Dungeon.fail, GLog.n
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L202) **`sprite()`**: 개별 처리 / 조건 분기 / 참조 호출: super.sprite, Actor.findById, hero.tier, updateArmor
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java#L229) **`icon()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 226. [`NPC.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/NPC.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 51행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/NPC.java#L28) `class NPC  extends Mob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/NPC.java#L39) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Bestiary.setSeen, getClass, super.act
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/NPC.java#L48) **`beckon(int cell)`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 227. [`PrismaticImage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 264행 / 타입 2개 / 필드 6개 / 메서드 15개.

### 타입·상속 선언

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L47) `class PrismaticImage  extends NPC`
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L245) `class Wandering  extends Mob.Wandering`

### 변수·상수 (단일 행 선언)

- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L65) `Hero hero`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L66) `int heroID`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L67) `int armTier`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L69) `int deathTimer` 초기식: `-1`
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L127) `String HEROID` 초기식: `"hero_id"`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L128) `String TIMER` 초기식: `"timer"`

### 함수·메서드 역할과 내부 연결

- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L72) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: isAlive, sprite.alpha, spend, destroy, sprite.die, sprite.remove, sprite.resetColor, Actor.findById, hero.tier
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L111) **`die(Object cause)`**: 개별 처리 / 조건 분기 / 참조 호출: super.die, sprite.add
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L123) **`isActive()`**: 조건 판정 / 참조 호출: isAlive
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L131) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L138) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L144) **`duplicate(Hero hero, int HP)`**: 개별 처리 / 참조 호출: this.hero.id, PrismaticGuard.maxHP
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L152) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: Random.NormalIntRange
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L161) **`attackSkill(Char target)`**: 전투 관련 / 조건 분기 / 참조 호출: RingOfAccuracy.accuracyMultiplier
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L171) **`defenseSkill(Char enemy)`**: 전투 관련 / 조건 분기 / 참조 호출: RingOfEvasion.evasionMultiplier, hero.belongings.armor, evasionFactor, super.defenseSkill
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L188) **`drRoll()`**: 개별 처리 / 조건 분기 / 참조 호출: super.drRoll, hero.drRoll
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L198) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: hero.belongings.armor, proc, super.defenseProc
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L206) **`glyphLevel(Class<? extends Armor.Glyph> cls)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, super.glyphLevel, hero.glyphLevel
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L215) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: aggro, super.attackProc
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L225) **`sprite()`**: 개별 처리 / 조건 분기 / 참조 호출: super.sprite, Actor.findById, hero.tier, updateArmor
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java#L248) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Buff.affect, set, destroy, CellEmitter.get, start, Speck.factory, sprite.die, Sample.INSTANCE.play, super.act

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 228. [`RatKing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 183행 / 타입 1개 / 필드 0개 / 메서드 13개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L41) `class RatKing  extends NPC`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L50) **`defenseSkill(Char enemy)`**: 전투 관련
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L55) **`speed()`**: 개별 처리
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L60) **`chooseEnemy()`**: 개별 처리
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L65) **`damage(int dmg, Object src)`**: 전투 관련
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L70) **`add(Buff buff)`**: 상태 갱신
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L75) **`reset()`**: 생성·초기화
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L82) **`onAdd()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onAdd, yell, Messages.get
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L90) **`landmark()`**: 개별 처리
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L95) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.level.exit, destroy, sprite.killAndErase, Dungeon.level.entrance, super.act
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L117) **`interact(Char c)`**: 개별 처리 / 조건 분기 / 참조 호출: sprite.turnTo, super.interact, hero.belongings.getItem, notice, yell, Messages.get, hero.belongings.armor, Badges.validateRatmogrify, Game.runOnRenderThread
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L136) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.show, WndOptions, sprite, Messages.titleCase, name, Messages.get, onSelect, crown.upgradeArmor, hero.belongings.armor
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L146) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: crown.upgradeArmor, hero.belongings.armor, Ratmogrify, resetAnims, yell, Messages.get, GameScene.show, WndInfoArmorAbility
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/RatKing.java#L171) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, Holiday.getCurrentHoliday, super.description

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 229. [`Sheep.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 106행 / 타입 1개 / 필드 3개 / 메서드 8개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java#L36) `class Sheep  extends NPC`

### 변수·상수 (단일 행 선언)

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java#L38) `String[] LINE_KEYS` 초기식: `{"Baa!", "Baa?", "Baa.", "Baa..."}`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java#L44) `float lifespan`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java#L93) `String LIFESPAN` 초기식: `"lifespan"`

### 함수·메서드 역할과 내부 연결

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java#L47) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Bestiary.setSeen, getClass, destroy, sprite.die
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java#L58) **`initialize(float lifespan)`**: 생성·초기화 / 참조 호출: spend, Random.Float
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java#L64) **`defenseSkill(Char enemy)`**: 전투 관련
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java#L69) **`damage(int dmg, Object src)`**: 전투 관련
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java#L74) **`add(Buff buff)`**: 상태 갱신
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java#L79) **`interact(Char c)`**: 개별 처리 / 조건 분기 / 참조 호출: Bestiary.setSeen, getClass, sprite.showStatus, Messages.get, Random.element, Dungeon.hero.spendAndNext, Sample.INSTANCE.play, Random.Float, spend
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java#L96) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java#L102) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 230. [`Shopkeeper.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 350행 / 타입 1개 / 필드 4개 / 메서드 26개.

### 타입·상속 선언

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L62) `class Shopkeeper  extends NPC`

### 변수·상수 (단일 행 선언)

- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L70) `int MAX_BUYBACK_HISTORY` 초기식: `3`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L73) `int turnsSinceHarmed` 초기식: `-1`
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L327) `String BUYBACK_ITEMS` 초기식: `"buyback_items"`
- [L329](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L329) `String TURNS_SINCE_HARMED` 초기식: `"turns_since_harmed"`

### 함수·메서드 역할과 내부 연결

- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L76) **`landmark()`**: 개별 처리
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L81) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: sprite.turnTo, spend, super.act
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L93) **`damage(int dmg, Object src)`**: 전투 관련 / 참조 호출: processHarm
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L98) **`add(Buff buff)`**: 상태 갱신 / 조건 분기 / 참조 호출: processHarm
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L105) **`processHarm()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: yell, Messages.get, Actor.add, Actor, act, BlobImmunity, immunities, level.blobs.get, blobs.add
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L123) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: BlobImmunity, immunities, level.blobs.get, blobs.add, PathFinder.buildDistanceMap, BArray.not, Dungeon.level.length, blob.clear, CellEmitter.get
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L164) **`flee()`**: 개별 처리 / 조건 분기 / 참조 호출: destroy, Notes.remove, landmark, GLog.newLine, GLog.n, Messages.get, sprite.killAndErase, CellEmitter.get, burst
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L178) **`destroy()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.destroy, level.heaps.valueList, ShatteredPixelDungeon.scene, CellEmitter.get, burst, heap.size, heap.destroy, heap.items.remove
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L196) **`reset()`**: 생성·초기화
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L201) **`sellPrice(Item item)`**: 개별 처리 / 참조 호출: item.value
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L205) **`sell()`**: 개별 처리 / 참조 호출: GameScene.selectItem
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L209) **`canSell(Item item)`**: 조건 판정 / 조건 분기 / 참조 호출: item.value, checkSeal, item.isEquipped
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L217) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, Messages.get, itemSelectable, Shopkeeper.canSell, onSelect, Dungeon.hero.isAlive, sell, GameScene.show, WndTradeItem
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L219) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L224) **`itemSelectable(Item item)`**: 개별 처리 / 참조 호출: Shopkeeper.canSell
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L229) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Dungeon.hero.isAlive, sell, GameScene.show, WndTradeItem
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L238) **`interact(Char c)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Game.runOnRenderThread, Callback, call, buybackItems.size, PixelScene.landscape, Messages.get, item.value, Messages.titleCase, item.title
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L244) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: buybackItems.size, PixelScene.landscape, Messages.get, item.value, Messages.titleCase, item.title, length, substring, GameScene.show
- [L258](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L258) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onSelect, sell, GameScene.show, WndTitledMessage, sprite, Messages.titleCase, name, chatText, GLog.i
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L279) **`enabled(int index)`**: 개별 처리 / 조건 분기 / 참조 호출: buybackItems.get, value, super.enabled
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L288) **`hasIcon(int index)`**: 조건 판정
- [L293](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L293) **`getIcon(int index)`**: 조회·탐색 / 조건 분기 / 참조 호출: ItemSprite, buybackItems.get
- [L301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L301) **`hide()`**: 개별 처리 / 참조 호출: super.hide
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L311) **`chatText()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Dungeon.hero.buff, Messages.get, hero.heroClass.name
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L332) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L339](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java#L339) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: super.restoreFromBundle, buybackItems.clear, bundle.contains, bundle.getCollection, buybackItems.add, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 231. [`VaultLaser.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 235행 / 타입 1개 / 필드 16개 / 메서드 7개.

### 타입·상속 선언

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L46) `class VaultLaser  extends NPC`

### 변수·상수 (단일 행 선언)

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L55) `int[] laserDirs`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L56) `int laserDirIdx`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L58) `int curCooldown`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L59) `int afterShotCooldown`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L61) `int shotsAfterCooldown` 초기식: `1`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L62) `int shotsFired` 초기식: `0`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L65) `boolean giveWarning` 초기식: `true`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L68) `long SFXLastPlayed` 초기식: `0`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L71) `boolean seen` 초기식: `false`
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L193) `String LASER_DIRS` 초기식: `"laser_dirs"`
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L194) `String LASER_DIR_IDX` 초기식: `"laser_dir_idx"`
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L196) `String AFTER_SHOT_COOLDOWN` 초기식: `"after_shot_cooldown"`
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L197) `String CUR_COOLDOWN` 초기식: `"cur_cooldown"`
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L199) `String SHOTS` 초기식: `"shots"`
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L200) `String SHOTS_FIRED` 초기식: `"shots_fired"`
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L202) `String WARNING` 초기식: `"warning"`

### 함수·메서드 역할과 내부 연결

- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L74) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Bestiary.setSeen, getClass, Ballistica, beam.subPath, Dungeon.level.destroy, GameScene.updateMap, Actor.findChar, ch.damage, Random.NormalIntRange
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L174) **`isImmune(Class effect)`**: 조건 판정
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L179) **`isInvulnerable(Class effect)`**: 조건 판정
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L184) **`reset()`**: 생성·초기화
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L189) **`interact(Char c)`**: 개별 처리
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L205) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultLaser.java#L217) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getIntArray, bundle.getInt, bundle.contains, bundle.getBoolean, Random.IntRange

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 232. [`VaultMirror.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 208행 / 타입 2개 / 필드 2개 / 메서드 11개.

### 타입·상속 선언

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L50) `class VaultMirror  extends NPC`
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L198) `class MirrorSword  extends Greatsword`

### 변수·상수 (단일 행 선언)

- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L67) `Item reward` 초기식: `null`
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L180) `String REWARD` 초기식: `"reward"`

### 함수·메서드 역할과 내부 연결

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L60) **`throwItems()`**: 개별 처리 / 조건 분기 / 참조 호출: level.heaps.get, Dungeon.level.drop, heap.pickUp, Dungeon.level.width, sprite.drop
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L69) **`createReward(HeroClass cls)`**: 생성·초기화 / 상태 선택 / 참조 호출: Random.pushGenerator, Random.Long, BrokenSeal, upgrade, identify, setGlyph, Armor.Glyph.random, MagesStaff, enchant
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L102) **`interact(Char c)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: ShatteredPixelDungeon.runOnRenderThread, Callback, call, Messages.get, GameScene.show, WndOptions, sprite, Messages.titleCase, name
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L106) **`call()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Messages.get, GameScene.show, WndOptions, sprite, Messages.titleCase, name, onSelect, super.onSelect, WndTitledMessage
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L137) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onSelect, GameScene.show, WndTitledMessage, sprite, Messages.titleCase, name, Messages.get, reward.doPickUp, GLog.i
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L161) **`defenseSkill(Char enemy)`**: 전투 관련
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L166) **`damage(int dmg, Object src)`**: 전투 관련
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L171) **`add(Buff buff)`**: 상태 갱신
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L176) **`reset()`**: 생성·초기화
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L183) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultMirror.java#L191) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, bundle.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 233. [`VaultSentry.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 311행 / 타입 1개 / 필드 22개 / 메서드 7개.

### 타입·상속 선언

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L48) `class VaultSentry  extends NPC`

### 변수·상수 (단일 행 선언)

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L56) `float scanWidth`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L57) `float scanLength`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L58) `int[][] scanDirs`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L59) `int scanDirIdx`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L62) `int curCooldown` 초기식: `1`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L63) `int afterScanCooldown` 초기식: `1`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L65) `int scansAfterCooldown` 초기식: `1`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L66) `int scansMade` 초기식: `0`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L69) `boolean giveWarning` 초기식: `false`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L72) `long SFXLastPlayed` 초기식: `0`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L75) `boolean seen` 초기식: `false`
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L243) `String SCAN_WIDTH` 초기식: `"scan_width"`
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L244) `String SCAN_LENGTH` 초기식: `"scan_length"`
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L245) `String SCAN_DIR_IDX` 초기식: `"scan_dir_idx"`
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L246) `String SCAN_DIRS` 초기식: `"scan_dirs_"`
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L247) `String SCAN_DIRS_LEN` 초기식: `"scan_dirs_len"`
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L249) `String AFTER_SCAN_COOLDOWN` 초기식: `"after_shot_cooldown"`
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L250) `String CUR_COOLDOWN` 초기식: `"cur_cooldown"`
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L252) `String SCANS` 초기식: `"shots"`
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L253) `String SCANS_MADE` 초기식: `"shots_fired"`
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L255) `String WARNING` 초기식: `"warning"`
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L257) `String RECENT_ZAPS` 초기식: `"recent_zaps"`

### 함수·메서드 역할과 내부 연결

- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L80) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Bestiary.setSeen, getClass, Dungeon.level.length, Dungeon.level.updateFieldOfView, Ballistica, ConeAOE, scan.cells.isEmpty, aim.path.size, scan.cells.add
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L224) **`isImmune(Class effect)`**: 조건 판정
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L229) **`isInvulnerable(Class effect)`**: 조건 판정
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L234) **`reset()`**: 생성·초기화
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L239) **`interact(Char c)`**: 개별 처리
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L260) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 반복 / 참조 호출: super.storeInBundle, bundle.put, recentZaps.size, recentZaps.get
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultSentry.java#L284) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: super.restoreFromBundle, bundle.getFloat, bundle.getInt, bundle.getIntArray, bundle.contains, bundle.getBoolean, recentZaps.clear, recentZaps.add

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 234. [`VaultTokenDoor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultTokenDoor.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 139행 / 타입 1개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultTokenDoor.java#L45) `class VaultTokenDoor  extends NPC`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultTokenDoor.java#L55) **`throwItems()`**: 개별 처리 / 조건 분기 / 참조 호출: level.heaps.get, Dungeon.level.drop, heap.pickUp, Dungeon.level.width, sprite.drop
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultTokenDoor.java#L63) **`interact(Char c)`**: 개별 처리 / 조건 분기 / 참조 호출: h.belongings.getItem, description, Messages.get, tokens.quantity, ShatteredPixelDungeon.runOnRenderThread, Callback, call, GameScene.show, WndOptions
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultTokenDoor.java#L82) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: tokens.quantity, GameScene.show, WndOptions, sprite, Messages.titleCase, name, Messages.get, onSelect, super.onSelect
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultTokenDoor.java#L90) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onSelect, c.sprite.operate, Sample.INSTANCE.play, Sample.INSTANCE.playDelayed, GLog.p, Messages.get, VaultTokenDoor.this.destroy, Level.set, GameScene.updateMap
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultTokenDoor.java#L120) **`defenseSkill(Char enemy)`**: 전투 관련
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultTokenDoor.java#L125) **`damage(int dmg, Object src)`**: 전투 관련
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultTokenDoor.java#L130) **`add(Buff buff)`**: 상태 갱신
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/VaultTokenDoor.java#L135) **`reset()`**: 생성·초기화

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 235. [`Wandmaker.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs` / 본문 463행 / 타입 2개 / 필드 15개 / 메서드 18개.

### 타입·상속 선언

- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L61) `class Wandmaker  extends NPC`
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L217) `class Quest`

### 변수·상수 (단일 행 선언)

- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L195) `String msg1Final` 초기식: `msg1`
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L196) `String msg2Final` 초기식: `msg2`
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L219) `int type`
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L224) `boolean spawned`
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L226) `boolean given`
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L228) `Wand wand1`
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L229) `Wand wand2`
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L239) `String NODE` 초기식: `"wandmaker"`
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L241) `String SPAWNED` 초기식: `"spawned"`
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L242) `String TYPE` 초기식: `"type"`
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L243) `String GIVEN` 초기식: `"given"`
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L244) `String WAND1` 초기식: `"wand1"`
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L245) `String WAND2` 초기식: `"wand2"`
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L247) `String RITUALPOS` 초기식: `"ritualpos"`
- [L295](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L295) `boolean questRoomSpawned`

### 함수·메서드 역할과 내부 연결

- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L70) **`landmark()`**: 개별 처리
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L75) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.hero.buff, die, super.act
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L84) **`defenseSkill(Char enemy)`**: 전투 관련
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L89) **`damage(int dmg, Object src)`**: 전투 관련
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L94) **`add(Buff buff)`**: 상태 갱신
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L99) **`reset()`**: 생성·초기화
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L104) **`interact(Char c)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: sprite.turnTo, hero.belongings.getItem, Game.runOnRenderThread, Callback, call, GameScene.show, WndWandmaker, Messages.get, Messages.titleCase
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L130) **`call()`**: 개별 처리 / 참조 호출: GameScene.show, WndWandmaker
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L149) **`call()`**: 개별 처리 / 참조 호출: GameScene.show, WndQuest
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L200) **`call()`**: 개별 처리 / 참조 호출: GameScene.show, WndQuest, hide, super.hide
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L203) **`hide()`**: 개별 처리 / 참조 호출: super.hide, GameScene.show, WndQuest
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L231) **`reset()`**: 생성·초기화
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L249) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: Bundle, node.put, bundle.put
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L273) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: bundle.getBundle, node.isNull, node.getBoolean, node.getInt, node.get, reset
- [L297](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L297) **`spawnWandmaker(Level level, Room room)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Wandmaker, level.pointToCell, room.random, level.entrance, level.traps.get, level.mobs.add, Generator.random, wand1.upgrade, wand2.getClass
- [L353](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L353) **`spawnRoom(ArrayList<Room> rooms)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Random.Int, rooms.add, MassGraveRoom, RitualSiteRoom, RotGardenRoom
- [L379](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L379) **`active()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: room, Dungeon.hero.buffs, hero.belongings.getItem, quantity, level.heaps.valueList, i.quantity
- [L451](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java#L451) **`complete()`**: 개별 처리 / 조건 분기 / 참조 호출: Notes.remove

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 236. [`PhantomPiranha.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/PhantomPiranha.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 125행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/PhantomPiranha.java#L40) `class PhantomPiranha  extends Piranha`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/PhantomPiranha.java#L50) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: Dungeon.level.adjacent, Math.round, super.damage, isAlive, Actor.findChar, candidates.add, candidates.isEmpty, ScrollOfTeleportation.appear, Random.element
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/PhantomPiranha.java#L83) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 참조 호출: super.defenseProc
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/PhantomPiranha.java#L88) **`dieOnLand()`**: 개별 처리 / 조건 분기 / 참조 호출: teleportAway, super.dieOnLand
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/PhantomPiranha.java#L94) **`teleportAway()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.length, Actor.findChar, inFOVCandidates.add, outFOVCandidates.add, outFOVCandidates.isEmpty, GLog.i, Messages.get, ScrollOfTeleportation.appear, Random.element

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 237. [`Piranha.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 215행 / 타입 4개 / 필드 0개 / 메서드 16개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L42) `class Piranha  extends Mob`
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L169) `class Sleeping  extends Mob.Sleeping`
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L181) `class Wandering  extends Mob.Wandering`
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L193) `class Hunting  extends Mob.Hunting`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L62) **`Piranha()`**: 개별 처리
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L70) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: buff, sprite.emitter, burst, Speck.factory, dieOnLand, super.act
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L84) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L89) **`attackSkill(Char target)`**: 전투 관련
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L94) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L99) **`surprisedBy(Char enemy, boolean attacking)`**: 개별 처리 / 조건 분기 / 참조 호출: canSurpriseAttack, Dungeon.level.length, Dungeon.level.updateFieldOfView, super.surprisedBy
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L110) **`dieOnLand()`**: 개별 처리 / 참조 호출: die
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L115) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die, Badges.validatePiranhasKilled
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L123) **`spawningWeight()`**: 개별 처리
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L128) **`reset()`**: 생성·초기화
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L133) **`getCloser(int target)`**: 조회·탐색 / 조건 분기 / 참조 호출: Dungeon.findStep, BArray.and, move
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L149) **`getFurther(int target)`**: 조회·탐색 / 조건 분기 / 참조 호출: Dungeon.flee, BArray.and, move
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L171) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: PathFinder.buildDistanceMap, super.act
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L183) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: PathFinder.buildDistanceMap, super.act
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L196) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: PathFinder.buildDistanceMap, super.act
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L206) **`random()`**: 개별 처리 / 조건 분기 / 참조 호출: RatSkull.exoticChanceMultiplier, Random.Float, PhantomPiranha, Piranha

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 238. [`Pylon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 237행 / 타입 1개 / 필드 2개 / 메서드 14개.

### 타입·상속 선언

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L49) `class Pylon  extends Mob`

### 변수·상수 (단일 행 선언)

- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L219) `String ALIGNMENT` 초기식: `"alignment"`
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L220) `String TARGET_NEIGHBOUR` 초기식: `"target_neighbour"`

### 함수·메서드 역할과 내부 연결

- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L69) **`Int(8)`**: 개별 처리
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L72) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.length, Dungeon.level.updateFieldOfView, throwItems, sprite.hideAlert, sprite.hideLost, chooseEnemy, enemy.isAlive, spend, shockCells.add
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L135) **`shockChar(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: ch.sprite.flash, ch.damage, Random.NormalIntRange, Electricity, ch.isAlive, Dungeon.fail, GLog.n, Messages.get
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L151) **`activate()`**: 시간·상태 갱신 / 참조 호출: activate
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L158) **`sprite()`**: 개별 처리 / 조건 분기 / 참조 호출: super.sprite, p.activate
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L165) **`beckon(int cell)`**: 개별 처리
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L170) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L179) **`interact(Char c)`**: 개별 처리
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L184) **`add(Buff buff)`**: 상태 갱신 / 조건 분기 / 참조 호출: super.add
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L193) **`isInvulnerable(Class effect)`**: 조건 판정 / 참조 호출: super.isInvulnerable
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L199) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: Math.sqrt, Dungeon.hero.buff, isImmune, src.getClass, isInvulnerable, Dungeon.isChallenged, lock.addTime, super.damage
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L214) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die, eliminatePylon
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L223) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Pylon.java#L230) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: bundle.getEnum, super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 239. [`VaultBossElemental.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.quest.vault` / 본문 1510행 / 타입 9개 / 필드 37개 / 메서드 59개.

### 타입·상속 선언

- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L81) `class VaultBossElemental  extends Mob`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L137) `enum ElementalForm`
- [L545](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L545) `class PinCushionRemover  extends Buff`
- [L762](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L762) `class FireWall  extends Buff`
- [L900](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L900) `class FrostResist  extends Buff`
- [L918](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L918) `class FrostCone  extends Buff`
- [L1033](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1033) `class FrostVortex  extends Buff`
- [L1275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1275) `class ShockResist  extends Buff`
- [L1319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1319) `class LightningChase  extends Buff`

### 변수·상수 (단일 행 선언)

- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L143) `ElementalForm form` 초기식: `null`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L144) `float[] formChances` 초기식: `new float[]{2, 2, 2}`
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L148) `int spTargetCell` 초기식: `-1`
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L150) `int lastEnemyPos` 초기식: `-1`
- [L343](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L343) `boolean weakAnnounced` 초기식: `false`
- [L507](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L507) `String FORM` 초기식: `"elemental_form"`
- [L509](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L509) `String ENV_ATK_COOLDOWN` 초기식: `"env_atk_cooldown"`
- [L510](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L510) `String SP_ATK_COOLDOWN` 초기식: `"sp_atk_cooldown"`
- [L511](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L511) `String SP_TARGET_CELL` 초기식: `"sp_target_cell"`
- [L513](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L513) `String LAST_ENEMY_POS` 초기식: `"last_enemy_pos"`
- [L514](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L514) `String LIGHTNING_OFS` 초기식: `"lightning_ofs"`
- [L552](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L552) `boolean preferGrouping` 초기식: `false`
- [L764](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L764) `int[] cells` 초기식: `new int[0]`
- [L765](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L765) `int direction`
- [L767](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L767) `int left` 초기식: `11`
- [L850](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L850) `String CELLS` 초기식: `"cells"`
- [L851](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L851) `String DIRECTION` 초기식: `"direction"`
- [L852](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L852) `String LEFT` 초기식: `"left"`
- [L920](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L920) `int startPos`
- [L922](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L922) `int distance` 초기식: `2`
- [L997](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L997) `String START_POS` 초기식: `"start_pos"`
- [L998](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L998) `String CELLS` 초기식: `"cells"`
- [L999](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L999) `String DISTANCE` 초기식: `"distance"`
- [L1035](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1035) `int targetCell` 초기식: `-1`
- [L1036](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1036) `int distance` 초기식: `-1000`
- [L1038](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1038) `boolean fullVortex` 초기식: `false`
- [L1039](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1039) `boolean altDirection` 초기식: `false`
- [L1184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1184) `String TARGET_CELL` 초기식: `"target_cell"`
- [L1185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1185) `String DISTANCE` 초기식: `"distance"`
- [L1187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1187) `String FULL_VORTEX` 초기식: `"full_vortex"`
- [L1188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1188) `String ALT_DIR` 초기식: `"alt_direction"`
- [L1214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1214) `int lightningOfs`
- [L1321](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1321) `float lastSFXTime` 초기식: `-1`
- [L1484](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1484) `String DIRECTION` 초기식: `"direction"`
- [L1485](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1485) `String CUR_CELL` 초기식: `"cur_cell"`
- [L1486](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1486) `String MID_CELL` 초기식: `"mid_cell"`
- [L1487](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1487) `String END_CELL` 초기식: `"end_cell"`

### 함수·메서드 역할과 내부 연결

- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L93) **`VaultBossElemental()`**: 개별 처리 / 참조 호출: ElementalForm.values, Random.Int, form.ordinal
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L100) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: Random.NormalIntRange
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L110) **`attackSkill(Char target)`**: 전투 관련
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L115) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L120) **`defenseSkill(Char enemy)`**: 전투 관련 / 조건 분기 / 참조 호출: belongings.attackingWeapon, Dungeon.level.adjacent, super.defenseSkill
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L146) **`NormalIntRange(10, 15)`**: 개별 처리
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L147) **`NormalIntRange(6, 10)`**: 개별 처리
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L152) **`changeForm()`**: 개별 처리 / 반복 / 참조 호출: ElementalForm.values, Random.chances, newForm.ordinal, setElementalForm
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L161) **`curForm()`**: 개별 처리
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L165) **`setElementalForm(ElementalForm form)`**: 상태 갱신 / 조건 분기·반복 / 참조 호출: Buff.affect, updateForm, AttackIndicator.target, sprite.emitter, e.pos, e.burst, Sample.INSTANCE.play, buffs, b.detach
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L216) **`aggro(Char ch)`**: 개별 처리 / 참조 호출: super.aggro
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L222) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.level.length, Dungeon.level.updateFieldOfView, chooseEnemy, sprite.zap, zap, spend, GameMath.gate, attackDelay, Math.ceil
- [L299](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L299) **`zap()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: spend, Invisibility.dispel, doFireBall, doFrostCone, doLightningBolt, Random.NormalIntRange
- [L319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L319) **`onZapComplete()`**: 이벤트·효과 실행 / 참조 호출: zap, next
- [L325](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L325) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: hero.belongings.attackingWeapon, sprite.parent.addToFront, Lightning, sprite.center, enemy.sprite.center, enemy.damage, Random.IntRange, Shocking, Sample.INSTANCE.play
- [L346](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L346) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: AntiMagic.RESISTS.contains, src.getClass, GLog.w, Messages.get, hero.belongings.attackingWeapon, GLog.p, Sample.INSTANCE.play, hero.belongings.charge, Math.ceil
- [L428](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L428) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die, Dungeon.level.unseal, GameScene.bossSlain
- [L435](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L435) **`sprite()`**: 개별 처리 / 조건 분기 / 참조 호출: changeForm, super.sprite, setForm
- [L447](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L447) **`add(Buff buff)`**: 상태 갱신 / 조건 분기 / 참조 호출: Buff.affect, damage, Random.NormalIntRange, super.add
- [L469](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L469) **`properties()`**: 개별 처리 / 조건 분기 / 참조 호출: props.add
- [L482](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L482) **`resist(Class effect)`**: 개별 처리 / 조건 분기 / 참조 호출: super.resist
- [L490](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L490) **`description()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: super.description, Messages.get
- [L517](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L517) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L530](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L530) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getEnum, bundle.getInt, BossHealthBar.assignBoss
- [L555](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L555) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: target.buff, detach, PathFinder.buildDistanceMap, Dungeon.level.length, Dungeon.level.distance, candidates.add, Math.abs, candidates.toArray, candidates.remove
- [L618](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L618) **`setupFireBall(Char enemy)`**: 생성·초기화 / 조건 분기·반복 / 참조 호출: Dungeon.level.adjacent, Random.Int, buff, Actor.findChar, GameScene.targetedCell, cooldown
- [L654](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L654) **`doFireBall(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Sample.INSTANCE.play, CellEmitter.get, burst, GameScene.add, Blob.seed, Actor.findChar, Buff.affect, reignite
- [L677](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L677) **`setupFireWall()`**: 생성·초기화 / 조건 분기·반복 / 참조 호출: Buff.append, room, r.center, Dungeon.level.cellToPoint, wallDistances.add, wallDistances.clone, Collections.shuffle, Collections.sort, Random.Int
- [L772](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L772) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.insideMap, CellEmitter.get, burst, Actor.findChar, Buff.affect, reignite, Sample.INSTANCE.play, detach, updateFX
- [L805](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L805) **`updateFX()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: emitters.clear, Dungeon.level.insideMap, CellEmitter.get, pour.pour, emitters.add, CellEmitter.center
- [L839](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L839) **`fx(boolean on)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: updateFX, emitters.clear
- [L855](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L855) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L863](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L863) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getIntArray, bundle.getInt
- [L875](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L875) **`setupFrostCone(Char enemy)`**: 생성·초기화 / 조건 분기·반복 / 참조 호출: Ballistica, ConeAOE, Dungeon.level.trueDistance, GameScene.targetedCell, cooldown
- [L889](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L889) **`doFrostCone(int cell)`**: 개별 처리 / 참조 호출: Buff.append, Ballistica, ConeAOE
- [L907](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L907) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: target.buff, spend, target.cooldown, detach
- [L927](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L927) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: cells.toArray, Dungeon.level.trueDistance, CellEmitter.get, burst, Actor.findChar, ch.buff, ch.damage, Random.NormalIntRange, Frost
- [L970](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L970) **`updateFX()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: emitters.clear, Dungeon.level.trueDistance, CellEmitter.get, e.pour, emitters.add
- [L986](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L986) **`fx(boolean on)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: updateFX, emitters.clear
- [L1002](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1002) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 반복 / 참조 호출: super.storeInBundle, bundle.put, cells.size
- [L1017](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1017) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 반복 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getIntArray, cells.add
- [L1028](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1028) **`setupFrostVortex()`**: 생성·초기화 / 참조 호출: Buff.append
- [L1044](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1044) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: getFurthestValid, Math.min, Random.Int, cells.addAll, getCells, updateFX, cells.isEmpty, detach, CellEmitter.get
- [L1104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1104) **`updateFX()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: emitters.clear, cells.addAll, getCells, CellEmitter.get, pour.pour, emitters.add
- [L1136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1136) **`fx(boolean on)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: updateFX, emitters.clear
- [L1147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1147) **`getFurthestValid(int start, int dirX, int dirY)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: Dungeon.level.width, Dungeon.level.insideMap
- [L1161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1161) **`getCells(int start, int dist, int dirX, int dirY)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: Math.abs, getFurthestValid, Dungeon.level.width, cells.add, Dungeon.level.insideMap
- [L1191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1191) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L1200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1200) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getBoolean
- [L1216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1216) **`setupLightningBolt(Char enemy)`**: 생성·초기화 / 반복 / 참조 호출: Random.Int, Ballistica, bolt.subPath, GameScene.targetedCell, cooldown
- [L1232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1232) **`doLightningBolt(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Ballistica, bolt.subPath, CellEmitter.get, burst, affectedCells.add, Actor.findChar, ch.buff, ch.damage, Random.NormalIntRange
- [L1282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1282) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: target.buff, spend, target.cooldown, detach
- [L1294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1294) **`setupLightningChase()`**: 생성·초기화 / 조건 분기 / 참조 호출: room, r.center, Random.Int, Buff.append, Dungeon.level.width
- [L1332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1332) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: PointF, Dungeon.level.cellToPoint, PointF.angle, Dungeon.level.pointToCell, curPos.floor, CellEmitter.get, burst, Actor.findChar, ch.buff
- [L1429](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1429) **`shockChar(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: ch.damage, Random.NormalIntRange, Electricity, Buff.prolong, Buff.affect, ch.sprite.centerEmitter, burst, ch.sprite.flash, Sample.INSTANCE.play
- [L1446](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1446) **`updateFX()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: emitters.clear, Dungeon.level.insideMap, CellEmitter.get, e.pour, emitters.add
- [L1473](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1473) **`fx(boolean on)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: updateFX, emitters.clear
- [L1490](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1490) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L1499](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java#L1499) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":31,"fields":112,"methods":222}

# Java 파일별 소스 구현 해설 640–655

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 640. [`Dagger.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 145행 / 타입 1개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L43) `class Dagger  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L56) **`max(int lvl)`**: 개별 처리
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L62) **`damageRoll(Char owner)`**: 전투 관련 / 조건 분기 / 참조 호출: hero.attackTarget, surprisedBy, max, min, augment.damageFactor, Hero.heroDamageIntRange, Math.round, hero.STR, STRReq
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L83) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L87) **`useTargeting()`**: 이벤트·효과 실행
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L92) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: sneakAbility, buffedLvl
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L97) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, buffedLvl
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L106) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java#L110) **`sneakAbility(Hero hero, Integer target, int maxDist, int invisTurns, MeleeWeapon wep)`**: 개별 처리 / 조건 분기 / 참조 호출: PathFinder.buildDistanceMap, BArray.or, GLog.w, Messages.get, PixelScene.shake, Actor.findChar, wep.beforeAbilityUsed, Buff.prolong, hero.sprite.turnTo

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 641. [`Dirk.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dirk.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 97행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dirk.java#L31) `class Dirk  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dirk.java#L42) **`max(int lvl)`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dirk.java#L48) **`damageRoll(Char owner)`**: 전투 관련 / 조건 분기 / 참조 호출: hero.attackTarget, surprisedBy, max, min, augment.damageFactor, Hero.heroDamageIntRange, Math.round, hero.STR, STRReq
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dirk.java#L69) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dirk.java#L73) **`useTargeting()`**: 이벤트·효과 실행
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dirk.java#L78) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: Dagger.sneakAbility, buffedLvl
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dirk.java#L83) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, buffedLvl
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dirk.java#L92) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Integer.toString

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 642. [`Flail.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 196행 / 타입 2개 / 필드 3개 / 메서드 14개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L39) `class Flail  extends MeleeWeapon`
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L143) `class SpinAbilityTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L57) `int spinBoost` 초기식: `0`
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L149) `int spins` 초기식: `0`
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L181) `String SPINS` 초기식: `"spins"`

### 함수·메서드 역할과 내부 연결

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L52) **`max(int lvl)`**: 개별 처리 / 참조 호출: Math.round
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L60) **`damageRoll(Char owner)`**: 전투 관련 / 조건 분기 / 참조 호출: super.damageRoll, Sample.INSTANCE.play
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L68) **`accuracyFactor(Char owner, Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: owner.buff, Actor.add, Actor, act, target.isAlive, onAbilityKill, Actor.remove, spin.detach, augment.damageFactor
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L74) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: target.isAlive, onAbilityKill, Actor.remove
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L97) **`baseChargeUse(Hero hero, Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.buff
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L106) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff, GLog.w, Messages.get, beforeAbilityUsed, Buff.affect, Buff.prolong, Sample.INSTANCE.play, hero.sprite.operate, hero.spendAndNext
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L130) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: buffedLvl, Messages.get, augment.damageFactor
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L139) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: augment.damageFactor
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L152) **`icon()`**: 개별 처리
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L157) **`tintIcon(Image icon)`**: 개별 처리 / 상태 선택 / 참조 호출: icon.hardlight
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L172) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L177) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, Math.round, dispTurns
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L184) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java#L190) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 643. [`Gauntlet.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gauntlet.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 73행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gauntlet.java#L29) `class Gauntlet  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gauntlet.java#L41) **`max(int lvl)`**: 개별 처리 / 참조 호출: Math.round
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gauntlet.java#L47) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gauntlet.java#L52) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, buffedLvl, Sai.comboStrikeAbility
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gauntlet.java#L59) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: buffedLvl, Messages.get, augment.damageFactor
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gauntlet.java#L68) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: augment.damageFactor

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 644. [`Glaive.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Glaive.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 75행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Glaive.java#L29) `class Glaive  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Glaive.java#L42) **`max(int lvl)`**: 개별 처리 / 참조 호출: Math.round
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Glaive.java#L48) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Glaive.java#L53) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, Math.round, buffedLvl, Spear.spikeAbility
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Glaive.java#L59) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Math.round, augment.damageFactor, min, max
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Glaive.java#L65) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, buffedLvl, Messages.get, augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 645. [`Gloves.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gloves.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 75행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gloves.java#L29) `class Gloves  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gloves.java#L43) **`max(int lvl)`**: 개별 처리 / 참조 호출: Math.round
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gloves.java#L49) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gloves.java#L54) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, buffedLvl, Sai.comboStrikeAbility
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gloves.java#L61) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: buffedLvl, Messages.get, augment.damageFactor
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gloves.java#L70) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: augment.damageFactor

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 646. [`Greataxe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greataxe.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 132행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greataxe.java#L37) `class Greataxe  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greataxe.java#L48) **`max(int lvl)`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greataxe.java#L54) **`STRReq(int lvl)`**: 개별 처리 / 조건 분기 / 참조 호출: STRReq
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greataxe.java#L63) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greataxe.java#L68) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 조건 분기 / 참조 호출: GLog.w, Messages.get, Actor.findChar, hero.isCharmedBy, hero.canAttack, hero.sprite.attack, Callback, call, beforeAbilityUsed
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greataxe.java#L94) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: beforeAbilityUsed, AttackIndicator.target, augment.damageFactor, buffedLvl, hero.attack, Sample.INSTANCE.play, Invisibility.dispel, enemy.isAlive, hero.next
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greataxe.java#L118) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: buffedLvl, Messages.get, augment.damageFactor, min, max
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greataxe.java#L127) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 647. [`Greatshield.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatshield.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 84행 / 타입 1개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatshield.java#L29) `class Greatshield  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatshield.java#L38) **`max(int lvl)`**: 개별 처리 / 참조 호출: Math.round
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatshield.java#L44) **`defenseFactor(Char owner)`**: 전투 관련 / 참조 호출: DRMax
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatshield.java#L48) **`DRMax()`**: 개별 처리 / 참조 호출: DRMax, buffedLvl
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatshield.java#L53) **`DRMax(int lvl)`**: 개별 처리
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatshield.java#L57) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, buffedLvl
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatshield.java#L66) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: RoundShield.guardAbility, buffedLvl
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatshield.java#L71) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, buffedLvl
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatshield.java#L80) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Integer.toString

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 648. [`Greatsword.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatsword.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 77행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatsword.java#L30) `class Greatsword  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatsword.java#L41) **`baseChargeUse(Hero hero, Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatsword.java#L50) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatsword.java#L55) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, buffedLvl, Sword.cleaveAbility
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatsword.java#L62) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: buffedLvl, Messages.get, augment.damageFactor, min, max
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatsword.java#L71) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 649. [`HandAxe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/HandAxe.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 74행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/HandAxe.java#L29) `class HandAxe  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/HandAxe.java#L41) **`max(int lvl)`**: 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/HandAxe.java#L47) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/HandAxe.java#L52) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, Math.round, buffedLvl, Mace.heavyBlowAbility
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/HandAxe.java#L59) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, buffedLvl, Messages.get, augment.damageFactor, min, max
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/HandAxe.java#L68) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Math.round, augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 650. [`Katana.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Katana.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 79행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Katana.java#L30) `class Katana  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Katana.java#L41) **`max(int lvl)`**: 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Katana.java#L47) **`defenseFactor(Char owner)`**: 전투 관련
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Katana.java#L52) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Katana.java#L57) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, Math.round, buffedLvl, Rapier.lungeAbility
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Katana.java#L64) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, buffedLvl, Messages.get, augment.damageFactor, min, max
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Katana.java#L73) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Math.round, augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 651. [`Longsword.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Longsword.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 76행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Longsword.java#L30) `class Longsword  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Longsword.java#L41) **`baseChargeUse(Hero hero, Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Longsword.java#L50) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Longsword.java#L55) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, buffedLvl, Sword.cleaveAbility
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Longsword.java#L62) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: buffedLvl, Messages.get, augment.damageFactor, min, max
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Longsword.java#L71) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 652. [`Mace.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Mace.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 132행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Mace.java#L40) `class Mace  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Mace.java#L52) **`max(int lvl)`**: 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Mace.java#L58) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Mace.java#L63) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, Math.round, buffedLvl, Mace.heavyBlowAbility
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Mace.java#L70) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, buffedLvl, Messages.get, augment.damageFactor, min, max
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Mace.java#L79) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Math.round, augment.damageFactor, min, max
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Mace.java#L84) **`heavyBlowAbility(Hero hero, Integer target, float dmgMulti, int dmgBoost, MeleeWeapon wep)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, hero.isCharmedBy, GLog.w, Messages.get, hero.canAttack, surprisedBy, Math.min, hero.sprite.attack, Callback
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Mace.java#L113) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: wep.beforeAbilityUsed, AttackIndicator.target, hero.attack, Sample.INSTANCE.play, enemy.isAlive, Buff.affect, wep.onAbilityKill, Invisibility.dispel, hero.spendAndNext

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 653. [`MagesStaff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 562행 / 타입 2개 / 필드 8개 / 메서드 46개.

### 타입·상속 선언

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L62) `class MagesStaff  extends MeleeWeapon`
- [L512](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L512) `class StaffParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L64) `Wand wand`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L66) `String AC_IMBUE` 초기식: `"IMBUE"`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L67) `String AC_ZAP` 초기식: `"ZAP"`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L69) `float STAFF_SCALE_FACTOR` 초기식: `0.75f`
- [L374](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L374) `String WAND` 초기식: `"wand"`
- [L514](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L514) `float minSize`
- [L515](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L515) `float maxSize`
- [L516](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L516) `float sizeJitter` 초기식: `0`

### 함수·메서드 역할과 내부 연결

- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L85) **`MagesStaff()`**: 개별 처리
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L90) **`max(int lvl)`**: 개별 처리 / 참조 호출: Math.round
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L95) **`MagesStaff(Wand wand)`**: 개별 처리 / 참조 호출: wand.identify, updateWand
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L105) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, actions.add
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L115) **`defaultAction()`**: 개별 처리
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L120) **`activate(Char ch)`**: 시간·상태 갱신 / 참조 호출: super.activate, applyWandChargeBuff
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L126) **`targetingPos(Hero user, int dst)`**: 개별 처리 / 조건 분기 / 참조 호출: wand.targetingPos, super.targetingPos
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L135) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, GameScene.selectItem, GameScene.show, WndUseItem, hasCurseEnchant, wand.execute
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L158) **`buffedVisiblyUpgraded()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, super.buffedVisiblyUpgraded, wand.buffedVisiblyUpgraded
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L167) **`proc(Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: hasTalent, ArtifactRecharge.chargeArtifacts, hero.pointsInTalent, attacker.buff, Math.round, Dungeon.hero.pointsInTalent, ScrollOfRecharging.charge, wand.onHit, empoweredStrike.detach
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L195) **`reachFactor(Char owner)`**: 개별 처리 / 조건 분기 / 참조 호출: super.reachFactor, Math.round, Wand.procChanceMultiplier
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L206) **`collect(Bag container)`**: 개별 처리 / 조건 분기 / 참조 호출: super.collect, applyWandChargeBuff
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L218) **`onDetach()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: wand.stopCharging
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L222) **`imbueWand(Wand wand, Char owner)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.hasTalent, Buff.affect, counter.count, counter.countUp, this.wand.level, this.wand.collect, Dungeon.level.drop, GLog.newLine, GLog.p
- [L282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L282) **`gainCharge(float amt)`**: 개별 처리 / 참조 호출: gainCharge
- [L286](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L286) **`gainCharge(float amt, boolean overcharge)`**: 개별 처리 / 조건 분기 / 참조 호출: wand.gainCharge
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L292) **`applyWandChargeBuff(Char owner)`**: 개별 처리 / 조건 분기 / 참조 호출: wand.charge
- [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L298) **`wandClass()`**: 개별 처리 / 참조 호출: wand.getClass
- [L303](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L303) **`upgrade(boolean enchant)`**: 개별 처리 / 참조 호출: super.upgrade, updateWand
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L312) **`degrade()`**: 개별 처리 / 참조 호출: super.degrade, updateWand
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L320) **`updateWand(boolean levelled)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: wand.level, level, Math.min, updateQuickslot
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L332) **`status()`**: 개별 처리 / 조건 분기 / 참조 호출: super.status, wand.status
- [L338](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L338) **`name()`**: 개별 처리 / 조건 분기 / 참조 호출: super.name, Messages.get, enchantment.curse, enchantment.name
- [L348](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L348) **`info()`**: 개별 처리 / 조건 분기 / 참조 호출: super.info, Messages.get, hasCurseEnchant, wand.statsDesc
- [L365](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L365) **`emitter()`**: 개별 처리 / 조건 분기 / 참조 호출: Emitter, emitter.pos, emitter.pour
- [L377](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L377) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L383](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L383) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.get, Math.min
- [L392](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L392) **`value()`**: 개별 처리
- [L397](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L397) **`enchant(Enchantment ench)`**: 개별 처리 / 조건 분기 / 참조 호출: ench.curse, updateWand, super.enchant
- [L405](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L405) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, Messages.get, preferredBag, itemSelectable, onSelect, item.trueLevel, trueLevel, item.isIdentified, Dungeon.hero.hasTalent
- [L408](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L408) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L413](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L413) **`preferredBag()`**: 개별 처리
- [L418](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L418) **`itemSelectable(Item item)`**: 개별 처리
- [L423](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L423) **`onSelect(final Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: item.trueLevel, trueLevel, Messages.get, item.isIdentified, Dungeon.hero.hasTalent, Dungeon.hero.buff, GameScene.show, WndOptions, ItemSprite
- [L462](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L462) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: applyWand
- [L472](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L472) **`applyWand(Wand wand)`**: 개별 처리 / 참조 호출: Sample.INSTANCE.play, curUser.sprite.emitter, burst, evoke, Dungeon.quickslot.clearItem, wand.detach, GLog.p, Messages.get, wand.name
- [L488](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L488) **`Factory()`**: 개별 처리 / 조건 분기 / 참조 호출: emit, emitter.getFirstAvailable, StaffParticle, emitter.add, c.reset, lightMode
- [L491](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L491) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 조건 분기 / 참조 호출: emitter.getFirstAvailable, StaffParticle, emitter.add, c.reset
- [L502](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L502) **`lightMode()`**: 개별 처리
- [L518](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L518) **`StaffParticle()`**: 개별 처리
- [L522](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L522) **`reset(float x, float y)`**: 생성·초기화 / 조건 분기 / 참조 호출: revive, speed.set, wand.staffFx
- [L535](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L535) **`setSize(float minSize, float maxSize)`**: 상태 갱신
- [L540](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L540) **`setLifespan(float life)`**: 상태 갱신
- [L544](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L544) **`shuffleXY(float amt)`**: 개별 처리 / 참조 호출: Random.Float
- [L549](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L549) **`radiateXY(float amt)`**: 개별 처리 / 참조 호출: Math.hypot
- [L556](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java#L556) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, size, Random.Float

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 654. [`MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 588행 / 타입 2개 / 필드 7개 / 메서드 40개.

### 타입·상속 선언

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L63) `class MeleeWeapon  extends Weapon`
- [L416](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L416) `class Charger  extends Buff implements ActionIndicator.Action`

### 변수·상수 (단일 행 선언)

- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L65) `String AC_ABILITY` 초기식: `"ABILITY"`
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L247) `int tier`
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L269) `boolean evaluatingTwinUpgrades` 초기식: `false`
- [L423](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L423) `int charges` 초기식: `2`
- [L424](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L424) `float partialCharge`
- [L506](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L506) `String CHARGES` 초기식: `"charges"`
- [L507](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L507) `String PARTIALCHARGE` 초기식: `"partialCharge"`

### 함수·메서드 역할과 내부 연결

- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L68) **`activate(Char ch)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.activate, Buff.affect
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L76) **`defaultAction()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.hasTalent, super.defaultAction
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L86) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, actions.add
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L95) **`actionName(String action, Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: action.equals, Messages.upperCase, Messages.get, super.actionName
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L104) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, isEquipped, hero.hasTalent, hero.buff, hasSecondUse, execute, GLog.w, Messages.get
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L135) **`onSelect(Integer cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: duelistAbility, updateQuickslot
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L143) **`prompt()`**: 개별 처리 / 참조 호출: targetingPrompt
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L153) **`targetingPrompt()`**: 개별 처리
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L157) **`useTargeting()`**: 이벤트·효과 실행 / 참조 호출: targetingPrompt
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L162) **`targetingPos(Hero user, int dst)`**: 개별 처리
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L166) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L170) **`beforeAbilityUsed(Hero hero, Char target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Buff.affect, abilityChargeUse, hero.hasTalent, hero.pointsInTalent, setShield, hero.sprite.showStatusWithIcon, Integer.toString, updateQuickslot
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L191) **`afterAbilityUsed(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.hasTalent, Buff.prolong, hero.cooldown, hero.buff, getClass, Buff.affect, tracker.detach, charger.gainCharge, hero.pointsInTalent
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L232) **`onAbilityKill(Hero hero, Char killed)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.hasTalent, Buff.affect, set, hero.pointsInTalent
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L239) **`baseChargeUse(Hero hero, Char target)`**: 개별 처리
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L243) **`abilityChargeUse(Hero hero, Char target)`**: 개별 처리 / 참조 호출: baseChargeUse
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L250) **`min(int lvl)`**: 개별 처리
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L256) **`max(int lvl)`**: 개별 처리
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L261) **`STRReq(int lvl)`**: 개별 처리 / 조건 분기 / 참조 호출: STRReq
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L271) **`buffedLvl()`**: 개별 처리 / 조건 분기 / 참조 호출: isEquipped, Dungeon.hero.hasTalent, hero.belongings.weapon, hero.belongings.secondWep, other.buffedLvl, Dungeon.hero.pointsInTalent, super.buffedLvl
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L294) **`damageRoll(Char owner)`**: 전투 관련 / 조건 분기 / 참조 호출: augment.damageFactor, super.damageRoll, STR, STRReq, Hero.heroDamageIntRange
- [L307](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L307) **`info()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: super.info, Messages.get, augment.damageFactor, min, max, STRReq, Dungeon.hero.STR, statsInfo, statsInfo.equals
- [L372](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L372) **`statsInfo()`**: 개별 처리 / 참조 호출: Messages.get
- [L376](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L376) **`abilityInfo()`**: 개별 처리 / 참조 호출: Messages.get
- [L380](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L380) **`upgradeAbilityStat(int level)`**: 개별 처리
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L385) **`status()`**: 개별 처리 / 조건 분기 / 참조 호출: isEquipped, Dungeon.hero.buff, buff.chargeCap, super.status
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L396) **`value()`**: 개별 처리 / 조건 분기 / 참조 호출: hasGoodEnchant, hasCurseEnchant, level
- [L427](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L427) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: chargeCap, Regeneration.regenOn, Dungeon.hero.buff, pointsInTalent, target.buff, updateQuickslot, ActionIndicator.setAction, spend
- [L470](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L470) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: ActionIndicator.setAction
- [L477](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L477) **`detach()`**: 개별 처리 / 참조 호출: super.detach, ActionIndicator.clearAction
- [L482](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L482) **`chargeCap()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min
- [L491](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L491) **`gainCharge(float charge)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: chargeCap, updateQuickslot
- [L510](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L510) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L517](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L517) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getFloat
- [L524](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L524) **`actionName()`**: 시간·상태 갱신 / 참조 호출: Messages.get
- [L529](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L529) **`actionIcon()`**: 시간·상태 갱신
- [L534](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L534) **`primaryVisual()`**: 개별 처리 / 조건 분기 / 참조 호출: HeroIcon, ItemSprite
- [L546](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L546) **`secondaryVisual()`**: 개별 처리 / 조건 분기 / 참조 호출: HeroIcon, ItemSprite, ico.scale.set, PixelScene.align, ico.brightness
- [L559](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L559) **`indicatorColor()`**: 개별 처리
- [L564](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java#L564) **`doAction()`**: 개별 처리 / 조건 분기 / 참조 호출: backpack.items.size, belongings.backpack.capacity, GLog.w, Messages.get, hero.sprite.operate, Sample.INSTANCE.play, ActionIndicator.setAction, Item.updateQuickslot, AttackIndicator.updateState

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 655. [`Quarterstaff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Quarterstaff.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 97행 / 타입 2개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Quarterstaff.java#L33) `class Quarterstaff  extends MeleeWeapon`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Quarterstaff.java#L78) `class DefensiveStance  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Quarterstaff.java#L44) **`max(int lvl)`**: 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Quarterstaff.java#L50) **`defenseFactor(Char owner)`**: 전투 관련
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Quarterstaff.java#L55) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: beforeAbilityUsed, Buff.prolong, buffedLvl, hero.sprite.operate, hero.next, afterAbilityUsed
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Quarterstaff.java#L65) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, buffedLvl
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Quarterstaff.java#L74) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Quarterstaff.java#L86) **`icon()`**: 개별 처리
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Quarterstaff.java#L91) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":20,"fields":18,"methods":180}

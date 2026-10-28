# Java 파일별 소스 구현 해설 656–671

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 656. [`Rapier.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 179행 / 타입 1개 / 필드 1개 / 메서드 9개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java#L42) `class Rapier  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java#L129) `int dest` 초기식: `lungeCell`

### 함수·메서드 역할과 내부 연결

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java#L55) **`max(int lvl)`**: 개별 처리
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java#L61) **`defenseFactor(Char owner)`**: 전투 관련
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java#L66) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java#L71) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, Math.round, buffedLvl, lungeAbility
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java#L78) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, buffedLvl, Messages.get, augment.damageFactor, min, max
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java#L87) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Math.round, augment.damageFactor, min, max
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java#L92) **`lungeAbility(Hero hero, Integer target, float dmgMulti, int dmgBoost, MeleeWeapon wep)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.findChar, hero.isCharmedBy, GLog.w, Messages.get, Dungeon.level.distance, wep.reachFactor, PixelScene.shake, Dungeon.level.trueDistance, hero.busy
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java#L135) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Door.leave, Dungeon.level.occupyCell, Dungeon.observe, hero.canAttack, hero.sprite.attack, Callback, call, wep.beforeAbilityUsed, AttackIndicator.target
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java#L147) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: wep.beforeAbilityUsed, AttackIndicator.target, hero.attack, Sample.INSTANCE.play, enemy.isAlive, wep.onAbilityKill, Invisibility.dispel, hero.spendAndNext, hero.attackDelay

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 657. [`RoundShield.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 143행 / 타입 2개 / 필드 2개 / 메서드 14개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L36) `class RoundShield  extends MeleeWeapon`
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L101) `class GuardTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L108) `boolean hasBlocked` 초기식: `false`
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L129) `String BLOCKED` 초기식: `"blocked"`

### 함수·메서드 역할과 내부 연결

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L47) **`max(int lvl)`**: 개별 처리 / 참조 호출: Math.round
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L53) **`defenseFactor(Char owner)`**: 전투 관련 / 참조 호출: DRMax
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L57) **`DRMax()`**: 개별 처리 / 참조 호출: DRMax, buffedLvl
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L62) **`DRMax(int lvl)`**: 개별 처리
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L66) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, buffedLvl
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L75) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: RoundShield.guardAbility, buffedLvl
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L80) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, buffedLvl
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L89) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L93) **`guardAbility(Hero hero, int duration, MeleeWeapon wep)`**: 개별 처리 / 참조 호출: wep.beforeAbilityUsed, Buff.prolong, hero.sprite.operate, hero.spendAndNext, wep.afterAbilityUsed
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L111) **`icon()`**: 개별 처리
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L116) **`tintIcon(Image icon)`**: 개별 처리 / 조건 분기 / 참조 호출: icon.tint, icon.resetColor
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L125) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L132) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java#L138) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getBoolean

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 658. [`RunicBlade.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RunicBlade.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 128행 / 타입 2개 / 필드 1개 / 메서드 6개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RunicBlade.java#L39) `class RunicBlade  extends MeleeWeapon`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RunicBlade.java#L121) `class RunicSlashTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RunicBlade.java#L123) `float boost` 초기식: `2f`

### 함수·메서드 역할과 내부 연결

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RunicBlade.java#L53) **`max(int lvl)`**: 개별 처리 / 참조 호출: Math.round
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RunicBlade.java#L59) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RunicBlade.java#L64) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, hero.isCharmedBy, GLog.w, Messages.get, Buff.affect, buffedLvl, hero.canAttack, tracker.detach, hero.sprite.attack
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RunicBlade.java#L89) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: beforeAbilityUsed, AttackIndicator.target, hero.attack, Sample.INSTANCE.play, enemy.isAlive, onAbilityKill, tracker.detach, Invisibility.dispel, hero.spendAndNext
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RunicBlade.java#L107) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, buffedLvl
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RunicBlade.java#L116) **`upgradeAbilityStat(int level)`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 659. [`Sai.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 222행 / 타입 2개 / 필드 7개 / 메서드 15개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L42) `class Sai  extends MeleeWeapon`
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L133) `class ComboStrikeTracker  extends Buff`

### 변수·상수 (단일 행 선언)

- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L139) `int DURATION` 초기식: `5`
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L140) `float comboTime` 초기식: `0f`
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L141) `float initialTime` 초기식: `5f`
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L142) `int hits` 초기식: `0`
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L200) `String TIME` 초기식: `"combo_time"`
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L201) `String INITIAL_TIME` 초기식: `"initial_time"`
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L202) `String RECENT_HITS` 초기식: `"recent_hits"`

### 함수·메서드 역할과 내부 연결

- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L54) **`max(int lvl)`**: 개별 처리 / 참조 호출: Math.round
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L60) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L65) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, buffedLvl, Sai.comboStrikeAbility
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L72) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: buffedLvl, Messages.get, augment.damageFactor
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L81) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: augment.damageFactor
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L85) **`comboStrikeAbility(Hero hero, Integer target, float multiPerHit, int boostPerHit, MeleeWeapon wep)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, hero.isCharmedBy, GLog.w, Messages.get, hero.canAttack, hero.sprite.attack, Callback, call, wep.beforeAbilityUsed
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L106) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: wep.beforeAbilityUsed, AttackIndicator.target, hero.buff, buff.detach, hero.attack, enemy.isAlive, wep.onAbilityKill, Invisibility.dispel, hero.spendAndNext
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L145) **`icon()`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.weapon, hero.belongings.secondWep
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L159) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: spend, detach
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L168) **`addHit(Char enemy)`**: 상태 갱신 / 조건 분기 / 참조 호출: enemy.isAlive, enemy.buff, icon, GLog.p, Messages.get
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L186) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L191) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L196) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, dispTurns
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L205) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java#L213) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 660. [`Scimitar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Scimitar.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 92행 / 타입 2개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Scimitar.java#L32) `class Scimitar  extends MeleeWeapon`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Scimitar.java#L73) `class SwordDance  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Scimitar.java#L44) **`max(int lvl)`**: 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Scimitar.java#L50) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: beforeAbilityUsed, Buff.prolong, buffedLvl, hero.sprite.operate, hero.next, afterAbilityUsed
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Scimitar.java#L60) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, buffedLvl
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Scimitar.java#L69) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Scimitar.java#L81) **`icon()`**: 개별 처리
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Scimitar.java#L86) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 661. [`Shortsword.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Shortsword.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 76행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Shortsword.java#L30) `class Shortsword  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Shortsword.java#L41) **`baseChargeUse(Hero hero, Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Shortsword.java#L50) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Shortsword.java#L55) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, buffedLvl, Sword.cleaveAbility
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Shortsword.java#L62) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: buffedLvl, Messages.get, augment.damageFactor, min, max
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Shortsword.java#L71) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 662. [`Sickle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sickle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 128행 / 타입 2개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sickle.java#L39) `class Sickle  extends MeleeWeapon`
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sickle.java#L125) `class HarvestBleedTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sickle.java#L51) **`max(int lvl)`**: 개별 처리 / 참조 호출: Math.round
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sickle.java#L57) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sickle.java#L62) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, Math.round, buffedLvl, Sickle.harvestAbility
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sickle.java#L69) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, buffedLvl, Messages.get, augment.damageFactor
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sickle.java#L79) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Integer.toString, augment.damageFactor, Math.round
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sickle.java#L83) **`harvestAbility(Hero hero, Integer target, float bleedMulti, int bleedBoost, MeleeWeapon wep)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, hero.isCharmedBy, GLog.w, Messages.get, hero.canAttack, hero.sprite.attack, Callback, call, wep.beforeAbilityUsed
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sickle.java#L105) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: wep.beforeAbilityUsed, AttackIndicator.target, Buff.affect, hero.attack, Sample.INSTANCE.play, Invisibility.dispel, hero.spendAndNext, hero.attackDelay, enemy.isAlive

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 663. [`Spear.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Spear.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 132행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Spear.java#L40) `class Spear  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Spear.java#L53) **`max(int lvl)`**: 개별 처리 / 참조 호출: Math.round
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Spear.java#L59) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Spear.java#L64) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, Math.round, buffedLvl, Spear.spikeAbility
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Spear.java#L71) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, buffedLvl, Messages.get, augment.damageFactor, min, max
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Spear.java#L80) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Math.round, augment.damageFactor, min, max
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Spear.java#L85) **`spikeAbility(Hero hero, Integer target, float dmgMulti, int dmgBoost, MeleeWeapon wep)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, hero.isCharmedBy, GLog.w, Messages.get, hero.canAttack, Dungeon.level.adjacent, hero.sprite.attack, Callback, call
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Spear.java#L106) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: wep.beforeAbilityUsed, AttackIndicator.target, hero.attack, enemy.isAlive, Pushing.pushingExistsForChar, Ballistica, trajectory.path.get, trajectory.path.size, WandOfBlastWave.throwChar

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 664. [`Sword.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 153행 / 타입 2개 / 필드 0개 / 메서드 9개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L40) `class Sword  extends MeleeWeapon`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L135) `class CleaveTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L51) **`baseChargeUse(Hero hero, Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L60) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L65) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, buffedLvl, Sword.cleaveAbility
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L72) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: buffedLvl, Messages.get, augment.damageFactor, min, max
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L81) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: augment.damageFactor, min, max
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L86) **`cleaveAbility(Hero hero, Integer target, float dmgMulti, int dmgBoost, MeleeWeapon wep)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, hero.isCharmedBy, GLog.w, Messages.get, hero.canAttack, hero.sprite.attack, Callback, call, wep.beforeAbilityUsed
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L107) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: wep.beforeAbilityUsed, AttackIndicator.target, hero.attack, Sample.INSTANCE.play, Invisibility.dispel, enemy.isAlive, hero.next, wep.onAbilityKill, hero.buff
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L142) **`icon()`**: 개별 처리
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java#L147) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 665. [`WarHammer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarHammer.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 74행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarHammer.java#L29) `class WarHammer  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarHammer.java#L41) **`max(int lvl)`**: 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarHammer.java#L47) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarHammer.java#L52) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, Math.round, buffedLvl, Mace.heavyBlowAbility
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarHammer.java#L58) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Math.round, augment.damageFactor, min, max
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarHammer.java#L64) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, buffedLvl, Messages.get, augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 666. [`WarScythe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarScythe.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 74행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarScythe.java#L29) `class WarScythe  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarScythe.java#L41) **`max(int lvl)`**: 개별 처리 / 참조 호출: Math.round
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarScythe.java#L47) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarScythe.java#L52) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, Math.round, buffedLvl, Sickle.harvestAbility
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarScythe.java#L59) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, buffedLvl, Messages.get, augment.damageFactor
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarScythe.java#L69) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Integer.toString, augment.damageFactor, Math.round

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 667. [`Whip.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Whip.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 112행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Whip.java#L37) `class Whip  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Whip.java#L49) **`max(int lvl)`**: 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Whip.java#L55) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.chars, hero.isCharmedBy, hero.canAttack, targets.add, Dungeon.level.trueDistance, targets.isEmpty, GLog.w, Messages.get, throwSound
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Whip.java#L83) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: beforeAbilityUsed, hero.attack, ch.isAlive, onAbilityKill, Invisibility.dispel, hero.spendAndNext, hero.attackDelay, afterAbilityUsed
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Whip.java#L100) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, augment.damageFactor, min, max
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Whip.java#L108) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 668. [`WornShortsword.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WornShortsword.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 79행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WornShortsword.java#L30) `class WornShortsword  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WornShortsword.java#L43) **`baseChargeUse(Hero hero, Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WornShortsword.java#L52) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WornShortsword.java#L57) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, buffedLvl, Sword.cleaveAbility
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WornShortsword.java#L64) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: buffedLvl, Messages.get, augment.damageFactor, min, max
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WornShortsword.java#L73) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 669. [`Bolas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Bolas.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles` / 본문 59행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Bolas.java#L30) `class Bolas  extends MissileWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Bolas.java#L42) **`min(int lvl)`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Bolas.java#L48) **`max(int lvl)`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Bolas.java#L54) **`proc(Char attacker, Char defender, int damage)`**: 개별 처리 / 참조 호출: Buff.prolong, super.proc

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 670. [`AdrenalineDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/AdrenalineDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 62행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/AdrenalineDart.java#L31) `class AdrenalineDart  extends TippedDart`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/AdrenalineDart.java#L38) **`damageRoll(Char owner)`**: 전투 관련 / 조건 분기 / 참조 호출: attackTarget, super.damageRoll
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/AdrenalineDart.java#L48) **`proc(Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.prolong, super.proc

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 671. [`BlindingDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/BlindingDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 47행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/BlindingDart.java#L30) `class BlindingDart  extends TippedDart`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/BlindingDart.java#L37) **`proc(Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.affect, super.proc

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":22,"fields":11,"methods":104}

# Java 파일별 소스 구현 해설 624–639

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 624. [`Crystal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 246행 / 타입 2개 / 필드 6개 / 메서드 12개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L44) `class Crystal  extends Weapon.Enchantment`
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L219) `class CrystalRepair  extends Buff`

### 변수·상수 (단일 행 선언)

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L50) `float durability` 초기식: `100`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L54) `float visualDurability` 초기식: `100`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L56) `boolean thrownWeapon` 초기식: `false`
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L201) `String DURABILITY` 초기식: `"durability"`
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L202) `String VISUAL_DUR` 초기식: `"visual_dur"`
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L203) `String THROWN_WEP` 초기식: `"thrown_wep"`

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L46) **`Glowing(0x0088FF)`**: 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L47) **`Glowing(0x0088FF, 0.5f)`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L48) **`Glowing(0x0088FF, 0.25f)`**: 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L59) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: setThrownWep, Math.min, weapon.buffedLvl, Random.NormalFloat, weapon.delayFactor, GameMath.gate, GLog.w, Messages.get, Math.max
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L123) **`setThrownWep()`**: 상태 갱신
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L127) **`setDurability(float amount)`**: 상태 갱신
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L131) **`repair(Weapon w, boolean inRose, float amount)`**: 개별 처리 / 조건 분기 / 참조 호출: durabilityLeft, repair, GLog.p, Messages.get, Math.min, Math.max, Item.updateQuickslot
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L174) **`glowing()`**: 개별 처리 / 조건 분기
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L185) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, Messages.get
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L206) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: bundle.getFloat, bundle.getBoolean
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L213) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: bundle.put
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java#L226) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Regeneration.regenOn, belongings.getAllItems, repair, belongings.getItem, rose.ghostWeapon, spend

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 625. [`Elastic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Elastic.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 71행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Elastic.java#L33) `class Elastic  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Elastic.java#L35) **`Glowing(0xFF00FF)`**: 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Elastic.java#L38) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, weapon.buffedLvl, procChanceMultiplier, Random.Float, Ballistica, trajectory.path.get, trajectory.path.size, WandOfBlastWave.throwChar, Math.round
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Elastic.java#L66) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 626. [`Eldritch.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Eldritch.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 75행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Eldritch.java#L35) `class Eldritch  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Eldritch.java#L37) **`Glowing(0x222222)`**: 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Eldritch.java#L40) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Math.max, weapon.buffedLvl, procChanceMultiplier, Random.Float, Actor.chars, Buff.affect, attacker.id, Flare, color
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Eldritch.java#L71) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 627. [`Grim.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Grim.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 84행 / 타입 2개 / 필드 2개 / 메서드 4개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Grim.java#L32) `class Grim  extends Weapon.Enchantment`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Grim.java#L67) `class GrimTracker  extends Buff`

### 변수·상수 (단일 행 선언)

- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Grim.java#L73) `float maxChance`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Grim.java#L74) `boolean qualifiesForBadge`

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Grim.java#L34) **`Glowing(0x000000)`**: 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Grim.java#L37) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: defender.isImmune, Math.max, weapon.buffedLvl, procChanceMultiplier, Buff.affect, attacker.buff, weapon.hasEnchant
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Grim.java#L63) **`glowing()`**: 개별 처리
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Grim.java#L77) **`act()`**: 시간·상태 갱신 / 참조 호출: detach

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 628. [`Kinetic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 147행 / 타입 3개 / 필드 3개 / 메서드 14개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L34) `class Kinetic  extends Weapon.Enchantment`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L57) `class KineticTracker  extends Buff`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L72) `class ConservedDamage  extends Buff`

### 변수·상수 (단일 행 선언)

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L63) `int conservedDamage`
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L99) `float preservedDamage`
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L127) `String PRESERVED_DAMAGE` 초기식: `"preserve_damage"`

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L36) **`Glowing(0xFFFF00)`**: 개별 처리
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L39) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: attacker.buff, damageBonus, Buff.affect
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L53) **`glowing()`**: 개별 처리
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L66) **`act()`**: 시간·상태 갱신 / 참조 호출: detach
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L79) **`icon()`**: 개별 처리
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L84) **`tintIcon(Image icon)`**: 개별 처리 / 조건 분기 / 참조 호출: icon.hardlight
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L95) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString, damageBonus
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L101) **`setBonus(int bonus)`**: 상태 갱신
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L105) **`damageBonus()`**: 전투 관련 / 참조 호출: Math.ceil
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L110) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Math.max, detach, spend
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L118) **`delay(float value)`**: 개별 처리 / 참조 호출: spend
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L123) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, damageBonus
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L130) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java#L136) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, bundle.getFloat, cooldown, spend

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 629. [`Lucky.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 97행 / 타입 2개 / 필드 1개 / 메서드 7개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java#L34) `class Lucky  extends Weapon.Enchantment`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java#L80) `class LuckProc  extends Buff`

### 변수·상수 (단일 행 선언)

- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java#L82) `int ringLevel` 초기식: `-5`

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java#L36) **`Glowing(0x00FF00)`**: 개별 처리
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java#L39) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, weapon.buffedLvl, procChanceMultiplier, Random.Float, Buff.affect, Math.round, defender.buff, detach
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java#L65) **`genLoot()`**: 개별 처리 / 참조 호출: RingOfWealth.genConsumableDrop
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java#L70) **`showFlare(Visual vis)`**: 개별 처리 / 참조 호출: RingOfWealth.showFlareForBonusDrop
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java#L75) **`glowing()`**: 개별 처리
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java#L85) **`act()`**: 시간·상태 갱신 / 참조 호출: detach
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java#L90) **`genLoot()`**: 개별 처리 / 참조 호출: detach, RingOfWealth.genConsumableDrop

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 630. [`Projecting.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Projecting.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 45행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Projecting.java#L28) `class Projecting  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Projecting.java#L30) **`Glowing(0x8844CC)`**: 개별 처리
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Projecting.java#L33) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Projecting.java#L40) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 631. [`Shocking.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Shocking.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 107행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Shocking.java#L39) `class Shocking  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Shocking.java#L41) **`Glowing(0xFFFFFF, 0.5f)`**: 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Shocking.java#L44) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Math.max, weapon.buffedLvl, procChanceMultiplier, Random.Float, affected.clear, arcs.clear, arc, affected.remove, ch.damage
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Shocking.java#L75) **`glowing()`**: 개별 처리
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Shocking.java#L83) **`arc(Char attacker, Char defender, int dist, ArrayList<Char> affected, ArrayList<Lightning.Arc> arcs)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: defender.sprite.centerEmitter, burst, defender.sprite.flash, PathFinder.buildDistanceMap, BArray.not, Actor.findChar, affected.contains, hitThisArc.add, affected.addAll

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 632. [`Unstable.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Unstable.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 71행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Unstable.java#L30) `class Unstable  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Unstable.java#L32) **`Glowing(0x999999)`**: 개별 처리
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Unstable.java#L53) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: attacker.buff, damageBonus, detach, Reflection.newInstance, Random.oneOf, proc
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Unstable.java#L67) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 633. [`Vampiric.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vampiric.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 72행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vampiric.java#L33) `class Vampiric  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vampiric.java#L35) **`Glowing(0x660022)`**: 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vampiric.java#L38) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: procChanceMultiplier, Random.Float, Math.max, Math.round, Math.min, attacker.isAlive, attacker.sprite.showStatusWithIcon, Integer.toString
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vampiric.java#L68) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 634. [`Venomous.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Venomous.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 69행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Venomous.java#L33) `class Venomous  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Venomous.java#L35) **`Glowing(0x4400AA)`**: 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Venomous.java#L38) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, weapon.buffedLvl, procChanceMultiplier, Random.Float, defender.buff, Buff.affect, poison.delay, poison.extend, CellEmitter.center
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Venomous.java#L65) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 635. [`Vorpal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vorpal.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 74행 / 타입 2개 / 필드 1개 / 메서드 4개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vorpal.java#L32) `class Vorpal  extends Weapon.Enchantment`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vorpal.java#L55) `class VorpalTracker  extends Buff`

### 변수·상수 (단일 행 선언)

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vorpal.java#L60) `float powerMulti`

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vorpal.java#L34) **`Glowing(0xAA6666)`**: 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vorpal.java#L37) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: defender.isImmune, procChanceMultiplier, Random.Float, Math.max, Buff.affect
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vorpal.java#L63) **`act()`**: 시간·상태 갱신 / 참조 호출: detach
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vorpal.java#L70) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 636. [`AssassinsBlade.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/AssassinsBlade.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 96행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/AssassinsBlade.java#L31) `class AssassinsBlade  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/AssassinsBlade.java#L42) **`max(int lvl)`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/AssassinsBlade.java#L48) **`damageRoll(Char owner)`**: 전투 관련 / 조건 분기 / 참조 호출: hero.attackTarget, surprisedBy, max, min, augment.damageFactor, Hero.heroDamageIntRange, Math.round, hero.STR, STRReq
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/AssassinsBlade.java#L69) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/AssassinsBlade.java#L73) **`useTargeting()`**: 이벤트·효과 실행
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/AssassinsBlade.java#L78) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: Dagger.sneakAbility, buffedLvl
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/AssassinsBlade.java#L83) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, buffedLvl
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/AssassinsBlade.java#L92) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Integer.toString

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 637. [`BattleAxe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/BattleAxe.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 74행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/BattleAxe.java#L29) `class BattleAxe  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/BattleAxe.java#L41) **`max(int lvl)`**: 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/BattleAxe.java#L47) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/BattleAxe.java#L52) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, Math.round, buffedLvl, Mace.heavyBlowAbility
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/BattleAxe.java#L59) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, buffedLvl, Messages.get, augment.damageFactor, min, max
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/BattleAxe.java#L68) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Math.round, augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 638. [`Crossbow.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 184행 / 타입 2개 / 필드 0개 / 메서드 14개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L37) `class Crossbow  extends MeleeWeapon`
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L169) `class ChargedShot  extends Buff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L50) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doUnequip, hero.buff, hero.belongings.weapon, hero.belongings.secondWep, detach
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L65) **`accuracyFactor(Char owner, Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: owner.buff, Actor.add, Actor, act, target.isAlive, onAbilityKill, Actor.remove, super.accuracyFactor
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L70) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: target.isAlive, onAbilityKill, Actor.remove
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L85) **`proc(Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: super.proc, Dungeon.hero.buff, hero.belongings.attackingWeapon, Ballistica, trajectory.path.get, trajectory.path.size, WandOfBlastWave.throwChar, attacker.buff, detach
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L110) **`max(int lvl)`**: 개별 처리
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L115) **`dartMin()`**: 개별 처리 / 참조 호출: dartMin, buffedLvl
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L119) **`dartMin(int lvl)`**: 개별 처리
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L124) **`dartMax()`**: 개별 처리 / 참조 호출: dartMax, buffedLvl
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L128) **`dartMax(int lvl)`**: 개별 처리
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L133) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, dartMin, dartMax
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L142) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff, GLog.w, Messages.get, beforeAbilityUsed, Buff.affect, hero.sprite.operate, hero.next, afterAbilityUsed
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L156) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, buffedLvl
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L165) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Integer.toString
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java#L177) **`icon()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 639. [`Cudgel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Cudgel.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee` / 본문 76행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Cudgel.java#L29) `class Cudgel  extends MeleeWeapon`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Cudgel.java#L43) **`max(int lvl)`**: 개별 처리
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Cudgel.java#L49) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Cudgel.java#L54) **`duelistAbility(Hero hero, Integer target)`**: 개별 처리 / 참조 호출: augment.damageFactor, Math.round, buffedLvl, Mace.heavyBlowAbility
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Cudgel.java#L61) **`abilityInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, buffedLvl, Messages.get, augment.damageFactor, min, max
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Cudgel.java#L70) **`upgradeAbilityStat(int level)`**: 개별 처리 / 참조 호출: Math.round, augment.damageFactor, min, max

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":23,"fields":13,"methods":94}

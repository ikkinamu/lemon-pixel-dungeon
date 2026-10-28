# Java 파일별 소스 구현 해설 608–623

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 608. [`Waterskin.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 197행 / 타입 1개 / 필드 6개 / 메서드 12개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L39) `class Waterskin  extends Item`

### 변수·상수 (단일 행 선언)

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L41) `int MAX_VOLUME` 초기식: `20`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L43) `String AC_DRINK` 초기식: `"DRINK"`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L45) `float TIME_TO_DRINK` 초기식: `1f`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L47) `String TXT_STATUS` 초기식: `"%d/%d"`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L57) `int volume` 초기식: `0`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L59) `String VOLUME` 초기식: `"volume"`

### 함수·메서드 역할과 내부 연결

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L62) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L68) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L74) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, actions.add
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L83) **`execute(final Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, VialOfBlood.delayBurstHealing, VialOfBlood.totalHealMultiplier, hero.buff, shielding, Math.round, hero.pointsInTalent, hero.hasTalent
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L139) **`info()`**: 개별 처리 / 조건 분기 / 참조 호출: super.info, Messages.get, isFull
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L155) **`empty()`**: 개별 처리 / 참조 호출: updateQuickslot
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L161) **`isUpgradable()`**: 조건 판정
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L166) **`isIdentified()`**: 조건 판정
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L170) **`isFull()`**: 조건 판정
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L174) **`collectDew(Dewdrop dew)`**: 개별 처리 / 조건 분기 / 참조 호출: GLog.i, Messages.get, GLog.p, updateQuickslot
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L186) **`fill()`**: 개별 처리 / 참조 호출: updateQuickslot
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java#L192) **`status()`**: 개별 처리 / 참조 호출: Messages.format

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 609. [`Annoying.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Annoying.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.curses` / 본문 73행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Annoying.java#L37) `class Annoying  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Annoying.java#L39) **`Glowing(0x000000)`**: 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Annoying.java#L42) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: procChanceMultiplier, Random.Float, level.mobs.toArray, mob.beckon, attacker.sprite.centerEmitter, start, Speck.factory, Sample.INSTANCE.play, Invisibility.dispel
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Annoying.java#L64) **`curse()`**: 개별 처리
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Annoying.java#L69) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 610. [`Dazzling.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Dazzling.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.curses` / 본문 71행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Dazzling.java#L36) `class Dazzling  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Dazzling.java#L38) **`Glowing(0x000000)`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Dazzling.java#L41) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: procChanceMultiplier, Random.Float, Actor.chars, Buff.prolong, GameScene.flash, Sample.INSTANCE.play
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Dazzling.java#L62) **`curse()`**: 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Dazzling.java#L67) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 611. [`Displacing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Displacing.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.curses` / 본문 70행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Displacing.java#L34) `class Displacing  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Displacing.java#L36) **`Glowing(0x000000)`**: 개별 처리
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Displacing.java#L39) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: procChanceMultiplier, Random.Float, defender.properties, contains, ScrollOfTeleportation.teleportChar, CellEmitter.get, start, Speck.factory
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Displacing.java#L60) **`curse()`**: 개별 처리
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Displacing.java#L65) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 612. [`Explosive.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.curses` / 본문 159행 / 타입 2개 / 필드 2개 / 메서드 11개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L40) `class Explosive  extends Weapon.Enchantment`
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L156) `class ExplosiveCurseBomb  extends Bomb.ConjuredBomb`

### 변수·상수 (단일 행 선언)

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L45) `int durability` 초기식: `100`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L144) `String DURABILITY` 초기식: `"durability"`

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L42) **`Glowing(0x000000)`**: 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L43) **`Glowing(0x000000, 0.5f)`**: 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L44) **`Glowing(0x000000, 0.25f)`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L48) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Math.round, Random.IntRange, procChanceMultiplier, attacker.sprite.showStatus, Messages.get, GLog.w, attacker.sprite.emitter, burst, Item.updateQuickslot
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L105) **`merge(Explosive other)`**: 개별 처리
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L111) **`clear()`**: 상태 갱신
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L116) **`curse()`**: 개별 처리
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L121) **`glowing()`**: 개별 처리 / 조건 분기
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L132) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, Messages.get
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L147) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: bundle.getInt
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java#L152) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: bundle.put

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 613. [`Friendly.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Friendly.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.curses` / 본문 70행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Friendly.java#L32) `class Friendly  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Friendly.java#L34) **`Glowing(0x000000)`**: 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Friendly.java#L37) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: attacker.buff, defender.id, procChanceMultiplier, Random.Float, Buff.affect, attacker.sprite.centerEmitter, start, Speck.factory, attacker.id
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Friendly.java#L60) **`curse()`**: 개별 처리
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Friendly.java#L65) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 614. [`Polarized.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Polarized.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.curses` / 본문 55행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Polarized.java#L29) `class Polarized  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Polarized.java#L31) **`Glowing(0x000000)`**: 개별 처리
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Polarized.java#L34) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: procChanceMultiplier, Random.Float, Math.round
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Polarized.java#L46) **`curse()`**: 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Polarized.java#L51) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 615. [`Pressurized.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Pressurized.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.curses` / 본문 71행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Pressurized.java#L32) `class Pressurized  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Pressurized.java#L34) **`Glowing(0x000000)`**: 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Pressurized.java#L37) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: procChanceMultiplier, Random.Float, GeyserTrap, Ballistica, aim.path.size, aim.path.get, geyser.activate
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Pressurized.java#L61) **`curse()`**: 개별 처리
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Pressurized.java#L66) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 616. [`Sacrificial.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Sacrificial.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.curses` / 본문 61행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Sacrificial.java#L31) `class Sacrificial  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Sacrificial.java#L33) **`Glowing(0x000000)`**: 개별 처리
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Sacrificial.java#L36) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: procChanceMultiplier, Random.Float, Math.pow, Buff.affect, set, Math.max, getClass
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Sacrificial.java#L51) **`curse()`**: 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Sacrificial.java#L56) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 617. [`Wayward.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.curses` / 본문 88행 / 타입 2개 / 필드 1개 / 메서드 7개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java#L33) `class Wayward  extends Weapon.Enchantment`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java#L61) `class WaywardBuff  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java#L68) `float DURATION` 초기식: `10f`

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java#L35) **`Glowing(0x000000)`**: 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java#L38) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: procChanceMultiplier, attacker.buff, Buff.detach, Random.Float, Buff.prolong
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java#L51) **`curse()`**: 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java#L56) **`glowing()`**: 개별 처리
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java#L71) **`icon()`**: 개별 처리
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java#L76) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java#L81) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 618. [`Wondrous.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wondrous.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.curses` / 본문 64행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wondrous.java#L33) `class Wondrous  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wondrous.java#L35) **`Glowing(0x000000)`**: 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wondrous.java#L38) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: procChanceMultiplier, Random.Float, WondrousResin.positiveCurseEffectChance, Ballistica, defender.sprite.emitter, burst, CursedWand.randomValidEffect, effect
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wondrous.java#L54) **`curse()`**: 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wondrous.java#L59) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 619. [`Blazing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blazing.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 76행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blazing.java#L34) `class Blazing  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blazing.java#L36) **`Glowing(0xFF4400)`**: 개별 처리
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blazing.java#L39) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, weapon.buffedLvl, procChanceMultiplier, Random.Float, defender.buff, Buff.affect, reignite, Random.NormalIntRange, Dungeon.scalingDepth
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blazing.java#L72) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 620. [`Blocking.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 147행 / 타입 2개 / 필드 2개 / 메서드 13개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L40) `class Blocking  extends Weapon.Enchantment`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L71) `class BlockBuff  extends ShieldBuff`

### 변수·상수 (단일 행 선언)

- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L79) `float left` 초기식: `5f`
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L132) `String LEFT` 초기식: `"left"`

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L42) **`Glowing(0x0000FF)`**: 개별 처리
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L45) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, weapon.buffedLvl, procChanceMultiplier, Random.Float, Buff.affect, Math.round, b.setShield, attacker.sprite.showStatusWithIcon, Integer.toString
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L67) **`glowing()`**: 개별 처리
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L82) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: HoldFast.buffDecayFactor, detach, spend
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L93) **`setShield(int shield)`**: 상태 갱신 / 참조 호출: super.setShield
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L99) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.buff, target.sprite.remove
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L108) **`icon()`**: 개별 처리
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L113) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L118) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L123) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L128) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, shielding, dispTurns
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L135) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java#L141) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getFloat

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 621. [`Blooming.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blooming.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 118행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blooming.java#L39) `class Blooming  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blooming.java#L41) **`Glowing(0x008800)`**: 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blooming.java#L44) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Math.max, weapon.buffedLvl, procChanceMultiplier, Random.Float, Math.ceil, Math.floor, plantGrass, positions.add, Random.shuffle
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blooming.java#L96) **`plantGrass(int cell)`**: 개별 처리 / 조건 분기 / 참조 호출: level.plants.get, Regeneration.regenOn, Level.set, GameScene.updateMap, CellEmitter.get, burst
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blooming.java#L114) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 622. [`Chilling.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Chilling.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 72행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Chilling.java#L33) `class Chilling  extends Weapon.Enchantment`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Chilling.java#L35) **`Glowing(0x00FFFF)`**: 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Chilling.java#L38) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, weapon.buffedLvl, procChanceMultiplier, Random.Float, defender.buff, Math.min, existing.cooldown, Buff.affect, Splash.at
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Chilling.java#L67) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 623. [`Corrupting.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Corrupting.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.enchantments` / 본문 109행 / 타입 2개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Corrupting.java#L36) `class Corrupting  extends Weapon.Enchantment`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Corrupting.java#L63) `class CorruptingTracker  extends Buff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Corrupting.java#L38) **`Glowing(0x440066)`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Corrupting.java#L41) **`proc(Weapon weapon, Char attacker, Char defender, int damage)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, weapon.buffedLvl, procChanceMultiplier, Random.Float, defender.isImmune, defender.buff, defender.isAlive, Buff.affect
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Corrupting.java#L72) **`act()`**: 시간·상태 갱신 / 참조 호출: detach
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Corrupting.java#L78) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: target.isAlive, Multiplicity.duplicate, target.sprite.killAndErase, corrupted.timeToNow, GameScene.add, Corruption.corruptionHeal, Buff.affect, Math.round, super.detach
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Corrupting.java#L105) **`glowing()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":20,"fields":11,"methods":90}

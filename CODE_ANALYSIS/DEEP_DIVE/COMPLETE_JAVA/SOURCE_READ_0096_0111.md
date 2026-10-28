# Java 파일별 소스 구현 해설 96–111

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 96. [`RevealedArea.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 87행 / 타입 1개 / 필드 4개 / 메서드 7개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java#L32) `class RevealedArea  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java#L38) `int pos, depth, branch`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java#L67) `String BRANCH` 초기식: `"branch"`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java#L68) `String DEPTH` 초기식: `"depth"`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java#L69) `String POS` 초기식: `"pos"`

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java#L41) **`detach()`**: 개별 처리 / 참조 호출: GameScene.updateFog, super.detach
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java#L47) **`icon()`**: 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java#L52) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java#L57) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent, Math.max, visualcooldown
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java#L63) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, visualcooldown
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java#L72) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java#L80) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 97. [`Roots.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 62행 / 타입 1개 / 필드 1개 / 메서드 4개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java#L27) `class Roots  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java#L29) `float DURATION` 초기식: `5f`

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java#L37) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java#L47) **`detach()`**: 개별 처리 / 참조 호출: super.detach
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java#L53) **`icon()`**: 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java#L58) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 98. [`ScrollEmpower.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 95행 / 타입 1개 / 필드 2개 / 메서드 10개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L30) `class ScrollEmpower  extends Buff`

### 변수·상수 (단일 행 선언)

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L36) `int left` 초기식: `0`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L81) `String LEFT` 초기식: `"left"`

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L38) **`reset(int left)`**: 생성·초기화 / 참조 호출: Math.max, Item.updateQuickslot
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L43) **`use()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: detach
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L51) **`detach()`**: 개별 처리 / 참조 호출: super.detach, Item.updateQuickslot
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L57) **`icon()`**: 개별 처리
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L62) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L67) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L72) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L77) **`desc()`**: 개별 처리 / 참조 호출: Messages.get
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L84) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java#L90) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 99. [`Shadows.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 129행 / 타입 1개 / 필드 2개 / 메서드 9개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java#L33) `class Shadows  extends Invisibility`

### 변수·상수 (단일 행 선언)

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java#L35) `float left`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java#L37) `String LEFT` 초기식: `"left"`

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java#L45) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java#L52) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getFloat
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java#L58) **`attachTo(Char target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.adjacent, super.attachTo, Sample.INSTANCE.play, Dungeon.observe
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java#L78) **`detach()`**: 개별 처리 / 참조 호출: super.detach, Dungeon.observe
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java#L84) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: target.isAlive, spend, detach, Dungeon.level.adjacent
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java#L110) **`prolong()`**: 개별 처리
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java#L115) **`icon()`**: 개별 처리
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java#L120) **`iconFadePercent()`**: 개별 처리
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java#L125) **`desc()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 100. [`ShieldBuff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 154행 / 타입 1개 / 필드 4개 / 메서드 14개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L33) `class ShieldBuff  extends Buff`

### 변수·상수 (단일 행 선언)

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L35) `int shielding`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L42) `int shieldUsePriority` 초기식: `0`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L43) `boolean detachesAtZero` 초기식: `true`
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L139) `String SHIELDING` 초기식: `"shielding"`

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L46) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L56) **`detach()`**: 개별 처리 / 참조 호출: super.detach
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L61) **`shielding()`**: 개별 처리
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L65) **`setShield(int shield)`**: 상태 갱신 / 조건 분기
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L70) **`incShield()`**: 개별 처리 / 참조 호출: incShield
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L74) **`incShield(int amt)`**: 개별 처리 / 조건 분기
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L80) **`delay(float value)`**: 개별 처리 / 참조 호출: spend
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L84) **`decShield()`**: 개별 처리 / 참조 호출: decShield
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L88) **`decShield(int amt)`**: 개별 처리 / 조건 분기
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L94) **`absorbDamage(int dmg)`**: 개별 처리 / 조건 분기 / 참조 호출: detach
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L109) **`processDamage(Char target, int damage, Object src)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: target.buffs, buffs.isEmpty, Collections.sort, compare, buff.shielding, buff.absorbDamage, hasTalent, Buff.affect
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L120) **`compare(ShieldBuff a, ShieldBuff b)`**: 개별 처리
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L142) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java#L148) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 101. [`Sleep.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Sleep.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 34행 / 타입 1개 / 필드 1개 / 메서드 1개.

### 타입·상속 선언

- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Sleep.java#L24) `class Sleep  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Sleep.java#L31) `float SWS` 초기식: `1.5f`

### 함수·메서드 역할과 내부 연결

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Sleep.java#L27) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.idle

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 102. [`Slow.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 52행 / 타입 1개 / 필드 1개 / 메서드 3개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java#L27) `class Slow  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java#L34) `float DURATION` 초기식: `10f`

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java#L37) **`icon()`**: 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java#L42) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java#L47) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 103. [`SnipersMark.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 141행 / 타입 1개 / 필드 5개 / 메서드 10개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L36) `class SnipersMark  extends FlavourBuff implements ActionIndicator.Action`

### 변수·상수 (단일 행 선언)

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L38) `int object` 초기식: `0`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L39) `float percentDmgBonus` 초기식: `0`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L41) `String OBJECT` 초기식: `"object"`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L42) `String BONUS` 초기식: `"bonus"`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L44) `float DURATION` 초기식: `4f`

### 함수·메서드 역할과 내부 연결

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L50) **`set(int object, float bonus)`**: 상태 갱신 / 조건 분기 / 참조 호출: hero.belongings.getItem, ActionIndicator.setAction
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L60) **`detach()`**: 개별 처리 / 참조 호출: super.detach, ActionIndicator.clearAction
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L66) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L73) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getFloat
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L80) **`icon()`**: 개별 처리
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L85) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L90) **`actionName()`**: 시간·상태 갱신 / 조건 분기·상태 선택 / 참조 호출: hero.belongings.getItem, Messages.get
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L106) **`actionIcon()`**: 시간·상태 갱신
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L111) **`indicatorColor()`**: 개별 처리
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java#L116) **`doAction()`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.getItem, bow.knockArrow, Actor.findById, QuickSlotButton.autoAim, arrow.cast, detach

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 104. [`SoulMark.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SoulMark.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 58행 / 타입 1개 / 필드 1개 / 메서드 4개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SoulMark.java#L28) `class SoulMark  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SoulMark.java#L30) `float DURATION` 초기식: `10f`

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SoulMark.java#L38) **`icon()`**: 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SoulMark.java#L43) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SoulMark.java#L48) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SoulMark.java#L53) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.sprite.remove

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 105. [`Speed.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Speed.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 29행 / 타입 1개 / 필드 1개 / 메서드 0개.

### 타입·상속 선언

- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Speed.java#L24) `class Speed  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Speed.java#L26) `float DURATION` 초기식: `10f`

### 함수·메서드 역할과 내부 연결

- 검출 없음

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 106. [`Stamina.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Stamina.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 51행 / 타입 1개 / 필드 1개 / 메서드 3개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Stamina.java#L27) `class Stamina  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Stamina.java#L29) `float DURATION` 초기식: `100f`

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Stamina.java#L36) **`icon()`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Stamina.java#L41) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Stamina.java#L46) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 107. [`SuperNovaTracker.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 194행 / 타입 3개 / 필드 13개 / 메서드 5개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L42) `class SuperNovaTracker  extends Buff`
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L132) `class NovaBombImmune  extends FlavourBuff`
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L180) `class NovaVFX  extends Halo`

### 변수·상수 (단일 행 선언)

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L44) `int pos`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L45) `int depth` 초기식: `Dungeon.depth`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L46) `int branch` 초기식: `Dungeon.branch`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L48) `int turnsLeft` 초기식: `10`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L49) `boolean harmsAllies` 초기식: `true`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L51) `boolean[] fieldOfView`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L52) `NovaVFX halo`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L54) `int DIST` 초기식: `8`
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L153) `String POS` 초기식: `"pos"`
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L154) `String DEPTH` 초기식: `"depth"`
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L155) `String BRANCH` 초기식: `"branch"`
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L157) `String LEFT` 초기식: `"left"`
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L158) `String HARMS_ALLIES` 초기식: `"harms_allies"`

### 함수·메서드 역할과 내부 연결

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L57) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: spend, DungeonTilemap.raisedTileCenterToWorld, Dungeon.level.length, NovaVFX, halo.point, halo.hardlight, GameScene.effect, FloatingText.show, halo.radius
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L139) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: NovaVFX, DungeonTilemap.raisedTileCenterToWorld, halo.hardlight, halo.radius, halo.alpha, halo.point, GameScene.effect, super.fx
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L161) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L171) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getBoolean
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SuperNovaTracker.java#L183) **`update()`**: 시간·상태 갱신 / 참조 호출: Math.cos, scale.set, DungeonTilemap.raisedTileCenterToWorld, point, super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 108. [`SwarmIntelTracker.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 114행 / 타입 1개 / 필드 4개 / 메서드 8개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L31) `class SwarmIntelTracker  extends Buff`

### 변수·상수 (단일 행 선언)

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L33) `int alertRange` 초기식: `0`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L34) `float leftAtZero`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L96) `String ALERT_RANGE` 초기식: `"alert_range"`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L97) `String LEFT` 초기식: `"left"`

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L37) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.length, Math.max, m.swarmAlertRange, m.cooldown, target.cooldown, spend
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L64) **`icon()`**: 개별 처리 / 조건 분기
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L73) **`iconFadePercent()`**: 개별 처리
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L78) **`tintIcon(Image icon)`**: 개별 처리 / 조건 분기 / 참조 호출: icon.brightness, icon.resetColor
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L87) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L92) **`desc()`**: 개별 처리 / 참조 호출: Messages.get
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L101) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java#L108) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 109. [`Terror.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 75행 / 타입 1개 / 필드 4개 / 메서드 5개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java#L27) `class Terror  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java#L29) `int object` 초기식: `0`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java#L31) `String OBJECT` 초기식: `"object"`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java#L33) `float DURATION` 초기식: `20f`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java#L62) `boolean ignoreNextHit` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java#L41) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java#L47) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java#L53) **`icon()`**: 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java#L58) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java#L64) **`recover()`**: 개별 처리 / 조건 분기 / 참조 호출: spend, cooldown, detach

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 110. [`TimeStasis.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/TimeStasis.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 84행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/TimeStasis.java#L29) `class TimeStasis  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/TimeStasis.java#L37) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, target.next, Dungeon.observe
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/TimeStasis.java#L56) **`spend(float time)`**: 개별 처리 / 조건 분기 / 참조 호출: super.spend, Buff.affect, hunger.isStarving, hunger.affectHunger, cooldown
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/TimeStasis.java#L67) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: super.detach, Dungeon.observe
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/TimeStasis.java#L75) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.sprite.remove

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 111. [`ToxicImbue.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 133행 / 타입 1개 / 필드 3개 / 메서드 11개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L35) `class ToxicImbue  extends Buff`

### 변수·상수 (단일 행 선언)

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L42) `float DURATION` 초기식: `50f`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L44) `float left`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L46) `String LEFT` 초기식: `"left"`

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L49) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L56) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getFloat
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L61) **`set(float duration)`**: 상태 갱신
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L65) **`extend(float duration)`**: 개별 처리
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L70) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: GameScene.add, Blob.seed, spend, detach
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L94) **`icon()`**: 개별 처리
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L99) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L104) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L109) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L114) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, dispTurns
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ToxicImbue.java#L124) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, Buff.detach

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":18,"fields":47,"methods":98}

# Java 파일별 소스 구현 해설 112–127

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 112. [`Vertigo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vertigo.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 46행 / 타입 1개 / 필드 1개 / 메서드 2개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vertigo.java#L26) `class Vertigo  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vertigo.java#L28) `float DURATION` 초기식: `10f`

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vertigo.java#L36) **`icon()`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vertigo.java#L41) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 113. [`Vulnerable.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vulnerable.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 45행 / 타입 1개 / 필드 1개 / 메서드 2개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vulnerable.java#L26) `class Vulnerable  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vulnerable.java#L28) `float DURATION` 초기식: `20f`

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vulnerable.java#L36) **`icon()`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vulnerable.java#L41) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 114. [`WandEmpower.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 86행 / 타입 1개 / 필드 4개 / 메서드 8개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L29) `class WandEmpower  extends Buff`

### 변수·상수 (단일 행 선언)

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L60) `int dmgBoost`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L61) `int left`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L68) `String BOOST` 초기식: `"boost"`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L69) `String LEFT` 초기식: `"left"`

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L36) **`icon()`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L41) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L46) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L51) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L56) **`desc()`**: 개별 처리 / 참조 호출: Messages.get
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L63) **`set(int dmg, int shots)`**: 상태 갱신 / 참조 호출: Math.max
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L72) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java#L79) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 115. [`Weakness.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Weakness.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 45행 / 타입 1개 / 필드 1개 / 메서드 2개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Weakness.java#L26) `class Weakness  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Weakness.java#L28) `float DURATION` 초기식: `20f`

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Weakness.java#L36) **`icon()`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Weakness.java#L41) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 116. [`WellFed.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WellFed.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 116행 / 타입 1개 / 필드 1개 / 메서드 9개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WellFed.java#L34) `class WellFed  extends Buff`

### 변수·상수 (단일 행 선언)

- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WellFed.java#L102) `String LEFT` 초기식: `"left"`

### 함수·메서드 역할과 내부 연결

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WellFed.java#L44) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: detach, target.sprite.showStatusWithIcon, spend, SaltCube.hungerGainMultiplier
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WellFed.java#L66) **`reset()`**: 생성·초기화 / 조건 분기 / 참조 호출: Dungeon.isChallenged
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WellFed.java#L76) **`extend(float duration)`**: 개별 처리
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WellFed.java#L81) **`icon()`**: 개별 처리
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WellFed.java#L86) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WellFed.java#L91) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: SaltCube.hungerGainMultiplier, Integer.toString
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WellFed.java#L97) **`desc()`**: 개별 처리 / 참조 호출: SaltCube.hungerGainMultiplier, Messages.get
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WellFed.java#L105) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WellFed.java#L111) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 117. [`Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors` / 본문 1473행 / 타입 3개 / 필드 30개 / 메서드 57개.

### 타입·상속 선언

- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L166) `class Char  extends Actor`
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L184) `enum Alignment`
- [L1417](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1417) `enum Property`

### 변수·상수 (단일 행 선언)

- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L168) `int pos` 초기식: `0`
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L170) `CharSprite sprite`
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L172) `int HT`
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L173) `int HP`
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L175) `float baseSpeed` 초기식: `1`
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L176) `PathFinder.Path path`
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L178) `int paralysed` 초기식: `0`
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L179) `boolean rooted` 초기식: `false`
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L180) `boolean flying` 초기식: `false`
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L181) `int invisible` 초기식: `0`
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L189) `Alignment alignment`
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L191) `int viewDistance` 초기식: `8`
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L193) `boolean[] fieldOfView` 초기식: `null`
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L332) `String POS` 초기식: `"pos"`
- [L333](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L333) `String PREV_POS` 초기식: `"prev_pos"`
- [L334](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L334) `String TAG_HP` 초기식: `"HP"`
- [L335](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L335) `String TAG_HT` 초기식: `"HT"`
- [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L336) `String TAG_SHLD` 초기식: `"SHLD"`
- [L337](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L337) `String BUFFS` 초기식: `"buffs"`
- [L612](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L612) `int INFINITE_ACCURACY` 초기식: `1_000_000`
- [L613](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L613) `int INFINITE_EVASION` 초기식: `1_000_000`
- [L687](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L687) `int hitMissIcon` 초기식: `-1`
- [L791](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L791) `int cachedShield` 초기식: `0`
- [L792](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L792) `boolean needsShieldUpdate` 초기식: `true`
- [L808](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L808) `int cachedIncomingDOT` 초기식: `0`
- [L809](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L809) `boolean needsIncomingDOTUpdate` 초기식: `true`
- [L1140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1140) `boolean deathMarked` 초기식: `false`
- [L1297](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1297) `int previousPos` 초기식: `-1`
- [L1447](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1447) `HashSet<Class> resistances`
- [L1448](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1448) `HashSet<Class> immunities`

### 함수·메서드 역할과 내부 연결

- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L198) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.level.length, Dungeon.level.updateFieldOfView, properties, contains, throwItems
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L211) **`throwItems()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: level.heaps.get, heap.peek, candidates.add, candidates.isEmpty, Dungeon.level.drop, heap.pickUp, Random.element, sprite.drop
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L228) **`name()`**: 개별 처리 / 참조 호출: Messages.get
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L232) **`canInteract(Char c)`**: 조건 판정 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, hasProp, Dungeon.level.distance, Dungeon.hero.pointsInTalent
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L246) **`interact(Char c)`**: 개별 처리 / 조건 분기 / 참조 호출: properties, contains, c.properties, hasProp, Dungeon.hero.hasTalent, PathFinder.buildDistanceMap, BArray.or, ScrollOfTeleportation.appear, Dungeon.observe
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L312) **`moveSprite(int from, int to)`**: 개별 처리 / 조건 분기 / 참조 호출: sprite.isVisible, sprite.move, sprite.turnTo, sprite.place
- [L324](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L324) **`hitSound(float pitch)`**: 전투 관련 / 참조 호출: Sample.INSTANCE.play
- [L328](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L328) **`blockSound(float pitch)`**: 개별 처리
- [L340](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L340) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L352](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L352) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getCollection, attachTo
- [L368](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L368) **`attack(Char enemy)`**: 전투 관련 / 참조 호출: attack
- [L372](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L372) **`attack(Char enemy, float dmgMulti, float dmgBonus, float accMulti)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: enemy.isInvulnerable, getClass, enemy.sprite.showStatus, Messages.get, Sample.INSTANCE.play, Random.Float, hit, Math.round, enemy.drRoll
- [L615](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L615) **`hit(Char attacker, Char defender, boolean magic)`**: 전투 관련 / 참조 호출: hit
- [L619](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L619) **`hit(Char attacker, Char defender, float accMulti, boolean magic)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: attacker.attackSkill, defender.defenseSkill, interrupt, attacker.canSurpriseAttack, defender.buff, FloatingText.getMissReasonIcon, FloatingText.getHitReasonIcon, Random.Float, attacker.buff
- [L689](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L689) **`attackSkill(Char target)`**: 전투 관련
- [L693](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L693) **`defenseSkill(Char enemy)`**: 전투 관련
- [L697](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L697) **`defenseVerb()`**: 전투 관련 / 참조 호출: Messages.get
- [L701](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L701) **`drRoll()`**: 개별 처리 / 참조 호출: Random.NormalIntRange, Barkskin.currentLevel
- [L709](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L709) **`damageRoll()`**: 전투 관련
- [L716](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L716) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 반복 / 참조 호출: buffs, buff.onAttackProc
- [L723](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L723) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: buff, armor.absorb, enemy.id, Dungeon.hero.pointsInTalent, Random.NormalIntRange, Math.max, Dungeon.hero.hasTalent, TargetHealthIndicator.instance.target, Random.Int
- [L759](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L759) **`glyphLevel(Class<? extends Armor.Glyph> cls)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.buff, Dungeon.level.distance, buff, Dungeon.hero.glyphLevel
- [L770](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L770) **`speed()`**: 개별 처리 / 조건 분기 / 참조 호출: buff, Swiftness.speedBoost, glyphLevel, Flow.speedBoost, Bulk.speedBoost
- [L786](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L786) **`canSurpriseAttack()`**: 조건 판정
- [L794](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L794) **`shielding()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: buffs, s.shielding
- [L811](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L811) **`incomingDOT()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: buffs, Math.round, resist, b.getClass, totalIncomingDMG, Math.ceil, buff.damageTakenFactor
- [L830](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L830) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: isAlive, isInvulnerable, src.getClass, sprite.showStatus, Messages.get, buff, buffs, links.toArray, Actor.findById
- [L1095](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1095) **`destroy()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.remove, Actor.chars, toArray, ch.buff, id, detach
- [L1123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1123) **`die(Object src)`**: 개별 처리 / 조건 분기 / 참조 호출: buff, detachOnDeath, destroy, sprite.die, fall
- [L1142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1142) **`isAlive()`**: 조건 판정
- [L1146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1146) **`isActive()`**: 조건 판정 / 참조 호출: isAlive
- [L1151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1151) **`spendConstant(float time)`**: 개별 처리 / 조건 분기 / 참조 호출: buff, freeze.processTime, bubble.processTime, super.spendConstant
- [L1168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1168) **`spend(float time)`**: 개별 처리 / 조건 분기 / 참조 호출: buff, speedFactor, super.spend
- [L1184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1184) **`buffs()`**: 개별 처리
- [L1190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1190) **`buffs(Class<T> c)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: c.isInstance, filtered.add
- [L1202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1202) **`buff(Class<T> c)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: b.getClass
- [L1211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1211) **`isCharmedBy(Char ch)`**: 조건 판정 / 조건 분기·반복 / 참조 호출: ch.id
- [L1221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1221) **`add(Buff buff)`**: 상태 갱신 / 조건 분기·상태 선택 / 참조 호출: buff, buffs.add, Actor.chars, contains, Actor.add, sprite.showStatus, Messages.titleCase, buff.name
- [L1257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1257) **`remove(Buff buff)`**: 상태 갱신 / 참조 호출: buffs.remove, Actor.remove
- [L1265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1265) **`remove(Class<? extends Buff> buffClass)`**: 상태 갱신 / 반복 / 참조 호출: buffs, remove
- [L1272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1272) **`onRemove()`**: 이벤트·효과 실행 / 반복 / 참조 호출: buffs.toArray, buffs.size, buff.detach
- [L1278](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1278) **`updateSpriteState()`**: 시간·상태 갱신 / 반복 / 참조 호출: buff.fx
- [L1284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1284) **`stealth()`**: 개별 처리 / 참조 호출: Obfuscation.stealthBoost, glyphLevel
- [L1292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1292) **`move(int step)`**: 개별 처리 / 참조 호출: move
- [L1300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1300) **`move(int step, boolean travelling)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, buff, sprite.interruptMotion, Random.Int, properties, contains, Actor.findChar, sprite.move, Door.leave
- [L1333](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1333) **`distance(Char other)`**: 개별 처리 / 참조 호출: Dungeon.level.distance
- [L1337](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1337) **`modifyPassable(boolean[] passable)`**: 개별 처리
- [L1342](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1342) **`onMotionComplete()`**: 이벤트·효과 실행
- [L1348](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1348) **`onAttackComplete()`**: 이벤트·효과 실행 / 참조 호출: next
- [L1352](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1352) **`onOperateComplete()`**: 이벤트·효과 실행 / 참조 호출: next
- [L1360](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1360) **`resist(Class effect)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: properties, resists.addAll, p.resistances, buffs, b.resistances, c.isAssignableFrom, RingOfElements.resist
- [L1380](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1380) **`isImmune(Class effect)`**: 조건 판정 / 조건 분기·반복 / 참조 호출: properties, immunes.addAll, p.immunities, buffs, b.immunities, glyphLevel, immunes.add, c.isAssignableFrom
- [L1402](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1402) **`isInvulnerable(Class effect)`**: 조건 판정 / 참조 호출: buff
- [L1408](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1408) **`properties()`**: 개별 처리 / 조건 분기 / 참조 호출: buff, props.add
- [L1459](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1459) **`resistances()`**: 개별 처리
- [L1463](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1463) **`immunities()`**: 개별 처리
- [L1469](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L1469) **`hasProp(Char ch, Property p)`**: 조건 판정 / 참조 호출: ch.properties, contains

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 118. [`ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities` / 본문 121행 / 타입 1개 / 필드 1개 / 메서드 15개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L36) `class ArmorAbility  implements Bundlable`

### 변수·상수 (단일 행 선언)

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L38) `float baseChargeUse` 초기식: `35`

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L40) **`use(ClassArmor armor, Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: targetingPrompt, activate, GameScene.selectCell, CellSelector.Listener, onSelect, prompt
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L46) **`onSelect(Integer cell)`**: 이벤트·효과 실행 / 참조 호출: activate
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L51) **`prompt()`**: 개별 처리 / 참조 호출: targetingPrompt
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L59) **`targetingPrompt()`**: 개별 처리
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L63) **`useTargeting()`**: 이벤트·효과 실행 / 참조 호출: targetingPrompt
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L67) **`targetedPos(Char user, int dst)`**: 개별 처리 / 참조 호출: Ballistica
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L71) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: hero.hasTalent, hero.pointsInTalent
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L93) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L95) **`name()`**: 개별 처리 / 참조 호출: Messages.get
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L99) **`shortDesc()`**: 개별 처리 / 참조 호출: Messages.get
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L103) **`desc()`**: 개별 처리 / 참조 호출: Messages.get
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L107) **`icon()`**: 개별 처리
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L111) **`talents()`**: 개별 처리
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L114) **`storeInBundle(Bundle bundle)`**: 저장·복원
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java#L118) **`restoreFromBundle(Bundle bundle)`**: 저장·복원

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 119. [`AscendedForm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.cleric` / 본문 167행 / 타입 2개 / 필드 9개 / 메서드 13개.

### 타입·상속 선언

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L43) `class AscendedForm  extends ArmorAbility`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L74) `class AscendBuff  extends ShieldBuff`

### 변수·상수 (단일 행 선언)

- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L83) `float DURATION` 초기식: `10f`
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L106) `int left` 초기식: `10`
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L107) `int spellCasts` 초기식: `0`
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L108) `int flashCasts` 초기식: `0`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L109) `boolean divineInverventionCast` 초기식: `false`
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L142) `String LEFT` 초기식: `"left"`
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L143) `String SPELL_CASTS` 초기식: `"spell_casts"`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L144) `String FLASH_CASTS` 초기식: `"flash_casts"`
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L145) `String DIVINE_INTERVENTION_CAST` 초기식: `"divine_intervention_cast"`

### 함수·메서드 역할과 내부 연결

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L50) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 참조 호출: Buff.affect, reset, hero.sprite.operate, Sample.INSTANCE.play, Flare, color, show, chargeUse, armor.updateQuickslot
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L65) **`icon()`**: 개별 처리
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L70) **`talents()`**: 개별 처리
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L86) **`icon()`**: 개별 처리
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L91) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L96) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L101) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.sprite.remove
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L111) **`reset()`**: 생성·초기화 / 참조 호출: setShield
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L116) **`extend(int amt)`**: 개별 처리
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L121) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: detach, Actor.chars, ch.buff, spend
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L138) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, shielding
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L148) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java#L157) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getBoolean

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 120. [`PowerOfMany.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.cleric` / 본문 416행 / 타입 4개 / 필드 3개 / 메서드 31개.

### 타입·상속 선언

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L62) `class PowerOfMany  extends ArmorAbility`
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L201) `class PowerBuff  extends FlavourBuff`
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L244) `class LightAlly  extends DirectableAlly`
- [L355](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L355) `class LightAllySprite  extends MobSprite`

### 변수·상수 (단일 행 선언)

- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L203) `float DURATION` 초기식: `100f`
- [L337](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L337) `String HERO_CLS` 초기식: `"hero_cls"`
- [L338](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L338) `String DEF_SKILL` 초기식: `"def_skill"`

### 함수·메서드 역할과 내부 연결

- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L65) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: getPoweredAlly, super.chargeUse
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L73) **`targetingPrompt()`**: 개별 처리 / 조건 분기 / 참조 호출: getPoweredAlly, Dungeon.hero.buff, isEmpowered, Stasis.getStasisAlly, Messages.get
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L101) **`useTargeting()`**: 이벤트·효과 실행
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L106) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: getPoweredAlly, hero.buff, isEmpowered, Stasis.getStasisAlly, directTocell, GLog.w, Messages.get, chargeUse, Actor.findChar
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L183) **`icon()`**: 개별 처리
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L188) **`talents()`**: 개별 처리
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L192) **`getPoweredAlly()`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: Actor.chars, ch.buff
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L211) **`icon()`**: 개별 처리
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L216) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L221) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.sprite.remove
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L227) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: target.buff, spend, super.act
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L237) **`detach()`**: 개별 처리 / 참조 호출: super.detach, Dungeon.observe, GameScene.updateFog
- [L258](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L258) **`LightAlly()`**: 개별 처리 / 참조 호출: HeroClass.values, Random.Int
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L263) **`LightAlly(int heroLevel)`**: 개별 처리
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L269) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: buff, die, super.act, sprite.looping, sprite.idle
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L284) **`defendPos(int cell)`**: 개별 처리 / 참조 호출: GLog.i, Messages.get, super.defendPos
- [L290](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L290) **`followHero()`**: 개별 처리 / 참조 호출: GLog.i, Messages.get, super.followHero
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L296) **`targetChar(Char ch)`**: 개별 처리 / 참조 호출: GLog.i, Messages.get, super.targetChar
- [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L302) **`attackSkill(Char target)`**: 전투 관련
- [L307](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L307) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L312) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L317) **`speed()`**: 개별 처리 / 조건 분기 / 참조 호출: super.speed, Dungeon.level.distance
- [L331](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L331) **`sprite()`**: 개별 처리 / 참조 호출: super.sprite, setup
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L341) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L348](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L348) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getEnum, bundle.getInt
- [L357](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L357) **`LightAllySprite()`**: 개별 처리 / 참조 호출: setup, HeroClass.values, Random.Int
- [L363](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L363) **`setup(HeroClass cls)`**: 생성·초기화 / 참조 호출: texture, cls.spritesheet, TextureFilm, HeroSprite.tiers, Animation, idle.frames, run.frames, die.frames, attack.frames
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L385) **`link(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: super.link, setup
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L393) **`resetColor()`**: 생성·초기화 / 참조 호출: super.resetColor, alpha, tint
- [L401](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L401) **`die()`**: 개별 처리 / 참조 호출: super.die, emitter, start, Speck.factory
- [L408](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java#L408) **`draw()`**: 지형/화면 표현 / 조건 분기 / 참조 호출: alpha, super.draw

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 121. [`Trinity.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.cleric` / 본문 563행 / 타입 4개 / 필드 6개 / 메서드 21개.

### 타입·상속 선언

- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L80) `class Trinity  extends ArmorAbility`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L109) `class WndUseTrinity  extends WndTitledMessage`
- [L317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L317) `class WndItemtypeSelect  extends WndTitledMessage`
- [L435](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L435) `class WndItemConfirm  extends WndTitledMessage`

### 변수·상수 (단일 행 선언)

- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L86) `Bundlable bodyForm` 초기식: `null`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L87) `Bundlable mindForm` 초기식: `null`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L88) `Bundlable spiritForm` 초기식: `null`
- [L287](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L287) `String BODY` 초기식: `"body_form"`
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L288) `String MIND` 초기식: `"mind_form"`
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L289) `String SPIRIT` 초기식: `"spirit_form"`

### 함수·메서드 역할과 내부 연결

- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L91) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: GLog.w, Messages.get, GameScene.show, WndUseTrinity
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L102) **`targetedPos(Char user, int dst)`**: 개별 처리 / 조건 분기 / 참조 호출: targetingPos, super.targetedPos
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L111) **`WndUseTrinity(ClassArmor armor)`**: 개별 처리 / 조건 분기 / 참조 호출: HeroIcon, Messages.titleCase, Trinity.this.name, Messages.get, RedButton, name, trinityItemUseText, bodyForm.getClass, onClick
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L126) **`onClick()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.belongings.weapon, enchantment.getClass, equals, bodyForm.getClass, GLog.w, Messages.get, hide, Buff.prolong, BodyForm.duration
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L166) **`onClick()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.belongings.armor, glyph.getClass, equals, bodyForm.getClass, GLog.w, Messages.get, hide, Buff.prolong, BodyForm.duration
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L210) **`onClick()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hide, MindForm.targetSelector, mindEffect.setEffect, GameScene.selectCell, Sample.INSTANCE.play, Enchanting.show, hero.sprite.operate, Dungeon.quickslot.contains, QuickSlotButton.useTargeting
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L242) **`onClick()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.belongings.ring, getClass, equals, spiritForm.getClass, hero.belongings.misc, hero.belongings.artifact, GLog.w, Messages.get, hide
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L292) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L300) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, bundle.get
- [L308](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L308) **`icon()`**: 개별 처리
- [L313](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L313) **`talents()`**: 개별 처리
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L320) **`WndItemtypeSelect(HolyTome tome, ClericSpell spell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: HeroIcon, Messages.titleCase, spell.name, Messages.get, Catalog.ENCHANTMENTS.items, Statistics.itemTypesDiscovered.contains, discoveredClasses.add, Catalog.GLYPHS.items, Catalog.WANDS.items
- [L372](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L372) **`name()`**: 개별 처리 / 참조 호출: enchantment.name
- [L386](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L386) **`name()`**: 개별 처리 / 참조 호출: glyph.name
- [L408](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L408) **`onClick()`**: 이벤트·효과 실행 / 참조 호출: GameScene.show, WndItemConfirm
- [L437](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L437) **`WndItemConfirm(Window parentWnd, Item item, HolyTome tome, ClericSpell spell)`**: 개별 처리 / 조건 분기 / 참조 호출: ItemSprite, Messages.titleCase, getName, getText, Messages.get, RedButton, onClick, parentWnd.hide, WndItemConfirm.this.hide
- [L451](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L451) **`onClick()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: parentWnd.hide, WndItemConfirm.this.hide, spell.onSpellCast, hero.sprite.operate, Enchanting.show, Sample.INSTANCE.play
- [L478](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L478) **`getName(Item item)`**: 조회·탐색 / 조건 분기 / 참조 호출: enchantment.name, glyph.name, item.name
- [L487](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L487) **`getText(Item item)`**: 조회·탐색 / 조건 분기 / 참조 호출: enchantment.desc, trinityItemUseText, enchantment.getClass, glyph.desc, glyph.getClass, item.desc, item.getClass
- [L499](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L499) **`trinityItemUseText(Class<?> cls)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: trinityChargeUsePerEffect, Enchantment.class.isAssignableFrom, Glyph.class.isAssignableFrom, ench.equals, Messages.get, BodyForm.duration, Messages.decimalFormat, glyph.equals, MissileWeapon.class.isAssignableFrom
- [L533](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java#L533) **`trinityChargeUsePerEffect(Class<?> cls)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: hero.armorAbility.chargeUse, Enchantment.class.isAssignableFrom, Glyph.class.isAssignableFrom, ench.equals, glyph.equals, cls.equals, Artifact.class.isAssignableFrom

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 122. [`Challenge.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.duelist` / 본문 351행 / 타입 4개 / 필드 4개 / 메서드 18개.

### 타입·상속 선언

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L55) `class Challenge  extends ArmorAbility`
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L200) `class EliminationMatchTracker  extends FlavourBuff`
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L202) `class DuelParticipant  extends Buff`
- [L323](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L323) `class SpectatorFreeze  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L204) `float DURATION` 초기식: `10f`
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L207) `int takenDmg` 초기식: `0`
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L305) `String LEFT` 초기식: `"left"`
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L306) `String TAKEN_DMG` 초기식: `"taken_dmg"`

### 함수·메서드 역할과 내부 연결

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L62) **`icon()`**: 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L67) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L72) **`targetedPos(Char user, int dst)`**: 개별 처리
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L77) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: super.chargeUse, hero.buff, Math.pow, hero.pointsInTalent
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L87) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Actor.findChar, GLog.w, Messages.get, hero.buff, BArray.or, Actor.chars, PathFinder.buildDistanceMap, PathFinder.distance.clone, hero.hasTalent
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L196) **`talents()`**: 개별 처리
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L206) **`icon()`**: 개별 처리
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L210) **`icon()`**: 개별 처리
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L215) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L220) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L224) **`addDamage(int dmg)`**: 상태 갱신
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L229) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: detach, Actor.chars, ch.buff, Dungeon.level.distance, spend
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L254) **`detach()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.detach, target.isAlive, Sample.INSTANCE.play, Dungeon.hero.hasTalent, Dungeon.hero.buff, Math.round, Math.pow, Dungeon.hero.pointsInTalent, Math.min
- [L301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L301) **`desc()`**: 개별 처리 / 참조 호출: Messages.get
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L309) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L316](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L316) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L326) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.buff, target.sprite.remove
- [L338](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java#L338) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: super.detach, cooldown, Actor.delayChar

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 123. [`ElementalStrike.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.duelist` / 본문 682행 / 타입 4개 / 필드 3개 / 메서드 12개.

### 타입·상속 선언

- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L114) `class ElementalStrike  extends ArmorAbility`
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L294) `class DirectedPowerTracker  extends FlavourBuff`
- [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L298) `class ElementalStrikeLuckyTracker  extends Buff`
- [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L302) `class ElementalStrikeFurrowCounter  extends CounterBuff`

### 변수·상수 (단일 행 선언)

- [L295](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L295) `float enchBoost` 초기식: `0f`
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L300) `int storedKineticDamage` 초기식: `0`
- [L382](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L382) `int oldEnemyPos`

### 함수·메서드 역할과 내부 연결

- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L156) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L161) **`targetedPos(Char user, int dst)`**: 개별 처리
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L166) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: chargeUse, Item.updateQuickslot, Ballistica, hero.pointsInTalent, Math.min, ConeAOE, hero.belongings.weapon, enchantment.getClass, sprite.parent.recycle
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L207) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, hero.isCharmedBy, hero.canAttack, preAttackEffect, AttackIndicator.target, hero.attack, Sample.INSTANCE.play, perCellEffect, perCharEffect
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L246) **`preAttackEffect(ConeAOE cone, Hero hero, Weapon.Enchantment ench)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.chars, cone.cells.contains, hero.hasTalent, hero.pointsInTalent, Buff.affect, Dungeon.hero.pointsInTalent, hero.buff, damageBonus, Math.round
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L305) **`perCellEffect(ConeAOE cone, Weapon.Enchantment ench)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.chars, cone.cells.contains, Dungeon.hero.pointsInTalent, GameScene.add, Blob.seed, Math.round, Random.shuffle, Buff.affect, count
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L385) **`perCharEffect(ConeAOE cone, Hero hero, Char primaryTarget, Weapon.Enchantment ench)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.hero.pointsInTalent, Actor.chars, cone.cells.contains, affected.add, ch.damage, Math.round, Hero.heroDamageIntRange, hero.buff, detach
- [L444](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L444) **`compare(Char a, Char b)`**: 개별 처리 / 참조 호출: Dungeon.level.distance
- [L633](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L633) **`compare(Char a, Char b)`**: 개별 처리 / 참조 호출: Dungeon.level.distance
- [L655](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L655) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, Game.scene, hero.belongings.weapon
- [L672](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L672) **`icon()`**: 개별 처리
- [L677](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java#L677) **`talents()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 124. [`Feint.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.duelist` / 본문 281행 / 타입 4개 / 필드 0개 / 메서드 22개.

### 타입·상속 선언

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L56) `class Feint  extends ArmorAbility`
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L160) `class AfterImage  extends Mob`
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L248) `class FeintConfusion  extends FlavourBuff`
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L252) `class AfterImageSprite  extends MirrorSprite`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L63) **`icon()`**: 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L67) **`useTargeting()`**: 이벤트·효과 실행
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L72) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L77) **`targetedPos(Char user, int dst)`**: 개별 처리
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L82) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.adjacent, GLog.w, Messages.get, PixelScene.shake, Actor.findChar, hero.busy, Sample.INSTANCE.play, hero.sprite.jump, Callback
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L107) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Door.leave, Dungeon.level.occupyCell, Invisibility.dispel, hero.next
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L134) **`onComplete()`**: 이벤트·효과 실행 / 참조 호출: image.sprite.attack, Callback, call
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L137) **`call()`**: 개별 처리
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L156) **`talents()`**: 개별 처리
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L178) **`name()`**: 개별 처리
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L183) **`description()`**: 개별 처리
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L188) **`canInteract(Char c)`**: 조건 판정
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L193) **`act()`**: 시간·상태 갱신 / 참조 호출: destroy, sprite.die
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L199) **`syncToHero(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: cooldown, hero.cooldown, spendConstant
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L206) **`damage(int dmg, Object src)`**: 전투 관련
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L211) **`defenseSkill(Char enemy)`**: 전투 관련 / 조건 분기 / 참조 호출: clearEnemy, Buff.affect, enemy.sprite.showLost, Dungeon.hero.hasTalent, Buff.prolong, Dungeon.hero.pointsInTalent
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L233) **`add(Buff buff)`**: 상태 갱신
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L242) **`sprite()`**: 개별 처리 / 참조 호출: super.sprite, updateArmor
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L254) **`updateArmor()`**: 시간·상태 갱신 / 참조 호출: updateArmor
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L259) **`resetColor()`**: 생성·초기화 / 참조 호출: super.resetColor, alpha
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L265) **`die()`**: 개별 처리 / 조건 분기 / 참조 호출: parent.add, AlphaTweener, onComplete, AfterImageSprite.this.killAndErase
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java#L271) **`onComplete()`**: 이벤트·효과 실행 / 참조 호출: AfterImageSprite.this.killAndErase

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 125. [`NaturesPower.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.huntress` / 본문 99행 / 타입 2개 / 필드 2개 / 메서드 6개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java#L38) `class NaturesPower  extends ArmorAbility`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java#L70) `class naturesPowerTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java#L76) `float DURATION` 초기식: `8f`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java#L78) `int extensionsLeft` 초기식: `2`

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java#L45) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 참조 호출: Buff.prolong, hero.buff, hero.sprite.operate, Sample.INSTANCE.play, hero.sprite.emitter, burst, chargeUse, armor.updateQuickslot, Invisibility.dispel
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java#L61) **`icon()`**: 개별 처리
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java#L66) **`talents()`**: 개별 처리
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java#L80) **`extend(int turns)`**: 개별 처리 / 조건 분기 / 참조 호출: spend
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java#L88) **`icon()`**: 개별 처리
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java#L93) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 126. [`SpectralBlades.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpectralBlades.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.huntress` / 본문 168행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpectralBlades.java#L45) `class SpectralBlades  extends ArmorAbility`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpectralBlades.java#L52) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpectralBlades.java#L57) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Actor.findChar, GLog.w, Messages.get, Ballistica, findChar, hero.pointsInTalent, targets.add, hero.hasTalent, ConeAOE
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpectralBlades.java#L111) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: hero.pointsInTalent, hero.hasTalent, Buff.affect, hero.attack, callbacks.remove, callbacks.isEmpty, Invisibility.dispel, hero.spendAndNext, hero.attackDelay
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpectralBlades.java#L138) **`findChar(Ballistica path, Hero hero, int wallPenetration, HashSet<Char> existingTargets)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: Actor.findChar, existingTargets.contains
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpectralBlades.java#L159) **`icon()`**: 개별 처리
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpectralBlades.java#L164) **`talents()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 127. [`SpiritHawk.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.huntress` / 본문 334행 / 타입 3개 / 필드 4개 / 메서드 24개.

### 타입·상속 선언

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L55) `class SpiritHawk  extends ArmorAbility`
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L143) `class HawkAlly  extends DirectableAlly`
- [L295](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L295) `class HawkSprite  extends MobSprite`

### 변수·상수 (단일 행 선언)

- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L170) `int dodgesUsed` 초기식: `0`
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L171) `float timeRemaining` 초기식: `100f`
- [L277](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L277) `String DODGES_USED` 초기식: `"dodges_used"`
- [L278](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L278) `String TIME_REMAINING` 초기식: `"time_remaining"`

### 함수·메서드 역할과 내부 연결

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L58) **`targetingPrompt()`**: 개별 처리 / 조건 분기 / 참조 호출: getHawk, super.targetingPrompt, Messages.get
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L67) **`useTargeting()`**: 이벤트·효과 실행
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L76) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: getHawk, super.chargeUse
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L85) **`activate(ClassArmor armor, Hero hero, Integer target)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: getHawk, ally.directTocell, Actor.findChar, spawnPoints.add, spawnPoints.isEmpty, chargeUse, armor.updateQuickslot, HawkAlly, Random.element
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L125) **`icon()`**: 개별 처리
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L130) **`talents()`**: 개별 처리
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L134) **`getHawk()`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: Actor.chars
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L166) **`attackSkill(Char target)`**: 전투 관련
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L174) **`defenseSkill(Char enemy)`**: 전투 관련 / 조건 분기 / 참조 호출: Dungeon.hero.hasTalent, Dungeon.hero.pointsInTalent, super.defenseSkill
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L184) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L189) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 상태 선택 / 참조 호출: super.attackProc, Dungeon.hero.pointsInTalent, Buff.prolong
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L214) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: die, Dungeon.hero.interrupt, Dungeon.hero.pointsInTalent, super.act, Dungeon.level.updateFieldOfView, GameScene.updateFog, Math.ceil, speed
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L229) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L235) **`spend(float time)`**: 개별 처리 / 참조 호출: super.spend
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L241) **`destroy()`**: 개별 처리 / 참조 호출: super.destroy, Dungeon.observe, GameScene.updateFog
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L248) **`defendPos(int cell)`**: 개별 처리 / 참조 호출: GLog.i, Messages.get, super.defendPos
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L254) **`followHero()`**: 개별 처리 / 참조 호출: GLog.i, Messages.get, super.followHero
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L260) **`targetChar(Char ch)`**: 개별 처리 / 참조 호출: GLog.i, Messages.get, super.targetChar
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L266) **`description()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, Actor.chars, contains, Dungeon.hero.pointsInTalent
- [L281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L281) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L288) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getFloat
- [L297](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L297) **`HawkSprite()`**: 개별 처리 / 참조 호출: texture, TextureFilm, Animation, idle.frames, run.frames, attack.frames, die.frames, play
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L322) **`blood()`**: 개별 처리
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java#L327) **`die()`**: 개별 처리 / 참조 호출: super.die, emitter, start, Speck.factory

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":37,"fields":70,"methods":248}

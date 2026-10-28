# Java 파일별 소스 구현 해설 80–95

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 80. [`LostInventory.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/LostInventory.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 60행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/LostInventory.java#L28) `class LostInventory  extends Buff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/LostInventory.java#L35) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, belongings.lostInventory
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/LostInventory.java#L47) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: super.detach, belongings.lostInventory
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/LostInventory.java#L55) **`icon()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 81. [`MagicalSight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSight.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 75행 / 타입 1개 / 필드 2개 / 메서드 5개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSight.java#L30) `class MagicalSight  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSight.java#L32) `float DURATION` 초기식: `50f`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSight.java#L34) `int DISTANCE` 초기식: `12`

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSight.java#L41) **`icon()`**: 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSight.java#L46) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSight.java#L51) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSight.java#L56) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, Buff.detach
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSight.java#L65) **`detach()`**: 개별 처리 / 참조 호출: super.detach, Dungeon.observe, GameScene.updateFog

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 82. [`MagicalSleep.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSleep.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 105행 / 타입 1개 / 필드 1개 / 메서드 5개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSleep.java#L32) `class MagicalSleep  extends Buff`

### 변수·상수 (단일 행 선언)

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSleep.java#L34) `float STEP` 초기식: `1f`

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSleep.java#L37) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: target.isImmune, super.attachTo, GLog.i, Messages.get, detach
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSleep.java#L63) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: detach, Math.min, GLog.p, Messages.get, spend
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSleep.java#L81) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: super.detach
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSleep.java#L94) **`icon()`**: 개별 처리
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSleep.java#L99) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.remove

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 83. [`MagicImmune.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicImmune.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 86행 / 타입 1개 / 필드 1개 / 메서드 5개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicImmune.java#L30) `class MagicImmune  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicImmune.java#L32) `float DURATION` 초기식: `20f`

### 함수·메서드 역할과 내부 연결

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicImmune.java#L44) **`attachTo(Char target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.attachTo, target.buffs, b.getClass, isAssignableFrom, b.detach, updateHT
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicImmune.java#L64) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: super.detach, updateHT
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicImmune.java#L72) **`icon()`**: 개별 처리
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicImmune.java#L77) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicImmune.java#L82) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 84. [`MindVision.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MindVision.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 55행 / 타입 1개 / 필드 2개 / 메서드 3개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MindVision.java#L28) `class MindVision  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MindVision.java#L30) `float DURATION` 초기식: `20f`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MindVision.java#L32) `int distance` 초기식: `2`

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MindVision.java#L39) **`icon()`**: 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MindVision.java#L44) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MindVision.java#L49) **`detach()`**: 개별 처리 / 참조 호출: super.detach, Dungeon.observe, GameScene.updateFog

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 85. [`Momentum.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 248행 / 타입 1개 / 필드 7개 / 메서드 19개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L42) `class Momentum  extends Buff implements ActionIndicator.Action`

### 변수·상수 (단일 행 선언)

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L51) `int momentumStacks` 초기식: `0`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L52) `int freerunTurns` 초기식: `0`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L53) `int freerunCooldown` 초기식: `0`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L55) `boolean movedLastTurn` 초기식: `true`
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L186) `String STACKS` 초기식: `"stacks"`
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L187) `String FREERUN_TURNS` 초기식: `"freerun_turns"`
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L188) `String FREERUN_CD` 초기식: `"freerun_CD"`

### 함수·메서드 역할과 내부 연결

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L58) **`detach()`**: 개별 처리 / 참조 호출: super.detach, ActionIndicator.clearAction
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L64) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: freerunning, Dungeon.hero.pointsInTalent, Math.min, ActionIndicator.setAction, BuffIndicator.refreshHero, GameMath.gate, Math.round, ActionIndicator.clearAction, ActionIndicator.refresh
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L95) **`gainStack()`**: 개별 처리 / 조건 분기 / 참조 호출: freerunning, postpone, target.cooldown, target.speed, Math.min, ActionIndicator.setAction, BuffIndicator.refreshHero
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L105) **`freerunning()`**: 개별 처리
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L109) **`speedMultiplier()`**: 개별 처리 / 조건 분기 / 참조 호출: freerunning, Dungeon.hero.pointsInTalent
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L119) **`evasionBonus(int heroLvl, int excessArmorStr)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.pointsInTalent
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L128) **`icon()`**: 개별 처리 / 조건 분기
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L134) **`tintIcon(Image icon)`**: 개별 처리 / 조건 분기 / 참조 호출: icon.hardlight
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L143) **`iconFadePercent()`**: 개별 처리 / 조건 분기
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L154) **`iconTextDisplay()`**: 개별 처리 / 조건 분기 / 참조 호출: Integer.toString
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L165) **`name()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L176) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L191) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L199) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt, ActionIndicator.setAction
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L211) **`actionName()`**: 시간·상태 갱신 / 참조 호출: Messages.get
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L216) **`actionIcon()`**: 시간·상태 갱신
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L221) **`secondaryVisual()`**: 개별 처리 / 참조 호출: BitmapText, txt.text, Integer.toString, txt.hardlight, txt.measure
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L230) **`indicatorColor()`**: 개별 처리
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java#L235) **`doAction()`**: 개별 처리 / 참조 호출: Sample.INSTANCE.play, target.sprite.emitter, burst, Speck.factory, SpellSprite.show, BuffIndicator.refreshHero, ActionIndicator.clearAction

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 86. [`MonkEnergy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 684행 / 타입 12개 / 필드 5개 / 메서드 49개.

### 타입·상속 선언

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L60) `class MonkEnergy  extends Buff implements ActionIndicator.Action`
- [L286](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L286) `class MonkAbility`
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L320) `class UnarmedAbilityTracker  extends FlavourBuff`
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L322) `class FlurryEmpowerTracker  extends FlavourBuff`
- [L324](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L324) `class FlurryCooldownTracker  extends FlavourBuff`
- [L326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L326) `class Flurry  extends MonkAbility`
- [L417](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L417) `class Focus  extends MonkAbility`
- [L441](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L441) `class FocusBuff  extends Buff`
- [L462](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L462) `class Dash  extends MonkAbility`
- [L528](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L528) `class DragonKick  extends MonkAbility`
- [L621](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L621) `class Meditate  extends MonkAbility`
- [L675](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L675) `class MeditateResistance  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L66) `float energy` 초기식: `0`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L67) `int cooldown`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L69) `float MAX_COOLDOWN` 초기식: `5`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L128) `String ENERGY` 초기식: `"energy"`
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L129) `String COOLDOWN` 초기식: `"cooldown"`

### 함수·메서드 역할과 내부 연결

- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L72) **`icon()`**: 개별 처리
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L77) **`tintIcon(Image icon)`**: 개별 처리 / 조건 분기 / 참조 호출: icon.hardlight, icon.resetColor
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L86) **`iconFadePercent()`**: 개별 처리 / 참조 호출: GameMath.gate
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L91) **`iconTextDisplay()`**: 개별 처리 / 조건 분기 / 참조 호출: Integer.toString
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L100) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: ActionIndicator.setAction, BuffIndicator.refreshHero, spend
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L114) **`detach()`**: 개별 처리 / 참조 호출: super.detach, ActionIndicator.clearAction
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L120) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, energyCap
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L132) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L139) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getFloat, bundle.getInt, ActionIndicator.setAction
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L149) **`gainEnergy(Mob enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: Regeneration.regenOn, Char.hasProp, hero.hasTalent, hero.pointsInTalent, hero.belongings.armor, hero.belongings.weapon, hero.buff, target.buff, Math.min
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L212) **`energyCap()`**: 개별 처리 / 참조 호출: Math.max
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L216) **`abilityUsed(MonkAbility abil)`**: 개별 처리 / 조건 분기 / 참조 호출: abil.energyCost, Math.min, energyCap, hasTalent, pointsInTalent, target.buff, Buff.prolong, processCombinedEnergy, ActionIndicator.clearAction
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L239) **`abilitiesEmpowered(Hero hero)`**: 개별 처리 / 참조 호출: energyCap, hero.pointsInTalent
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L244) **`processCombinedEnergy(Talent.CombinedEnergyAbilityTracker tracker)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Math.min, energyCap, tracker.detach, ActionIndicator.setAction, BuffIndicator.refreshHero
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L254) **`actionName()`**: 시간·상태 갱신 / 참조 호출: Messages.get
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L259) **`actionIcon()`**: 시간·상태 갱신
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L264) **`secondaryVisual()`**: 개별 처리 / 참조 호출: BitmapText, txt.text, Integer.toString, txt.hardlight, txt.measure
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L273) **`indicatorColor()`**: 개별 처리 / 조건 분기 / 참조 호출: abilitiesEmpowered
- [L282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L282) **`doAction()`**: 개별 처리 / 참조 호출: GameScene.show, WndMonkAbilities
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L296) **`name()`**: 개별 처리 / 참조 호출: Messages.get
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L300) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.affect, abilitiesEmpowered, Messages.get
- [L308](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L308) **`energyCost()`**: 개별 처리
- [L310](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L310) **`usable(MonkEnergy buff)`**: 개별 처리 / 참조 호출: energyCost
- [L314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L314) **`targetingPrompt()`**: 개별 처리
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L318) **`doAbility(Hero hero, Integer target)`**: 개별 처리
- [L329](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L329) **`energyCost()`**: 개별 처리
- [L334](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L334) **`usable(MonkEnergy buff)`**: 개별 처리 / 참조 호출: super.usable, buff.target.buff
- [L339](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L339) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.affect, abilitiesEmpowered, Messages.get, Math.round, Dungeon.hero.STR
- [L351](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L351) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L356](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L356) **`doAbility(Hero hero, Integer target)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, hero.isCharmedBy, GLog.w, Messages.get, Buff.affect, abilitiesEmpowered, hero.canAttack, tracker.detach, hero.buff
- [L383](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L383) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: AttackIndicator.target, hero.attack, enemy.isAlive, hero.sprite.attack, Callback, call, Invisibility.dispel, hero.next, tracker.detach
- [L390](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L390) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: hero.attack, Invisibility.dispel, hero.next, tracker.detach, Buff.affect, abilityUsed, hero.buff, detach
- [L420](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L420) **`energyCost()`**: 개별 처리
- [L425](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L425) **`usable(MonkEnergy buff)`**: 개별 처리 / 참조 호출: super.usable, buff.target.buff
- [L430](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L430) **`doAbility(Hero hero, Integer target)`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.affect, abilitiesEmpowered, hero.next, hero.spendAndNext, abilityUsed
- [L449](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L449) **`icon()`**: 개별 처리
- [L454](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L454) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L465](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L465) **`energyCost()`**: 개별 처리
- [L470](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L470) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L475](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L475) **`doAbility(Hero hero, Integer target)`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.affect, abilitiesEmpowered, PixelScene.shake, GLog.w, Messages.get, Dungeon.level.distance, Actor.findChar, Ballistica, dash.collisionPos.equals
- [L514](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L514) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Door.leave, Dungeon.level.occupyCell, hero.next
- [L531](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L531) **`energyCost()`**: 개별 처리
- [L536](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L536) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.affect, abilitiesEmpowered, Messages.get, Dungeon.hero.STR
- [L547](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L547) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L552](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L552) **`doAbility(Hero hero, Integer target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.findChar, hero.isCharmedBy, GLog.w, Messages.get, Buff.affect, hero.canAttack, tracker.detach, hero.sprite.attack, Callback
- [L572](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L572) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: AttackIndicator.target, Buff.affect, abilitiesEmpowered, hero.attack, Sample.INSTANCE.play, Ballistica, trajectory.path.get, trajectory.path.size, WandOfBlastWave.throwChar
- [L624](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L624) **`energyCost()`**: 개별 처리
- [L629](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L629) **`doAbility(Hero hero, Integer target)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: hero.sprite.operate, GameScene.flash, Sample.INSTANCE.play, hero.buffs, b.detach, hero.spendConstant, Buff.affect, abilitiesEmpowered, Math.round
- [L662](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java#L662) **`act()`**: 시간·상태 갱신 / 참조 호출: Buff.affect, extend, Actor.remove

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 87. [`Ooze.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 143행 / 타입 1개 / 필드 5개 / 메서드 11개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L30) `class Ooze  extends Buff implements Buff.DOTbuff`

### 변수·상수 (단일 행 선언)

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L32) `float DURATION` 초기식: `20f`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L39) `float left`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L40) `boolean acted` 초기식: `false`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L42) `String LEFT` 초기식: `"left"`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L43) `String ACTED` 초기식: `"acted"`

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L46) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L53) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getFloat, bundle.getBoolean
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L60) **`icon()`**: 개별 처리
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L65) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L70) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L75) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, dispTurns
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L79) **`set(float left)`**: 상태 갱신 / 조건 분기
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L85) **`extend(float duration)`**: 개별 처리 / 조건 분기
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L91) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: detach, target.isAlive, Dungeon.scalingDepth, target.damage, Dungeon.fail, GLog.n, Messages.get, spend
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L126) **`detach()`**: 개별 처리 / 참조 호출: super.detach
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java#L132) **`totalIncomingDMG()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.scalingDepth, Math.ceil

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 88. [`Paralysis.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 122행 / 타입 2개 / 필드 3개 / 메서드 9개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L32) `class Paralysis  extends FlavourBuff`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L89) `class ParalysisResist  extends Buff`

### 변수·상수 (단일 행 선언)

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L34) `float DURATION` 초기식: `10f`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L95) `int damage`
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L107) `String DAMAGE` 초기식: `"damage"`

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L42) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L51) **`processDamage(int damage)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: target.buff, Buff.affect, Random.NormalIntRange, target.sprite.showStatus, Messages.get, detach
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L67) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: super.detach
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L74) **`icon()`**: 개별 처리
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L79) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L84) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.sprite.remove
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L98) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: target.buff, Math.ceil, detach, spend
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L110) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L116) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 89. [`PhysicalEmpower.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 91행 / 타입 1개 / 필드 4개 / 메서드 8개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L31) `class PhysicalEmpower  extends Buff`

### 변수·상수 (단일 행 선언)

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L63) `int dmgBoost`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L64) `int left`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L73) `String BOOST` 초기식: `"boost"`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L74) `String LEFT` 초기식: `"left"`

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L38) **`icon()`**: 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L43) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L48) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent, Math.max
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L54) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L59) **`desc()`**: 개별 처리 / 참조 호출: Messages.get
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L66) **`set(int dmg, int hits)`**: 상태 갱신 / 조건 분기
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L77) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java#L84) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 90. [`PinCushion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 105행 / 타입 1개 / 필드 1개 / 메서드 8개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java#L36) `class PinCushion  extends Buff`

### 변수·상수 (단일 행 선언)

- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java#L76) `String ITEMS` 초기식: `"items"`

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java#L40) **`stick(MissileWeapon projectile)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: items.size, projectile.isSimilar, items.get, projectile.merge, items.set, Dart, d.quantity, stick, items.add
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java#L57) **`grabOne()`**: 개별 처리 / 조건 분기 / 참조 호출: items.remove, items.isEmpty, detach
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java#L65) **`getStuckItems()`**: 조회·탐색
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java#L70) **`detach()`**: 개별 처리 / 반복 / 참조 호출: Dungeon.level.drop, sprite.drop, super.detach
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java#L79) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: bundle.put, super.storeInBundle
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java#L85) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: bundle.getCollection, super.restoreFromBundle
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java#L91) **`icon()`**: 개별 처리
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java#L96) **`desc()`**: 개별 처리 / 반복 / 참조 호출: Messages.get, i.title

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 91. [`Poison.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 146행 / 타입 1개 / 필드 2개 / 메서드 14개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L36) `class Poison  extends Buff implements Hero.Doom, Buff.DOTbuff`

### 변수·상수 (단일 행 선언)

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L38) `float left`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L40) `String LEFT` 초기식: `"left"`

### 함수·메서드 역할과 내부 연결

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L48) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L55) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getFloat
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L60) **`set(float duration)`**: 상태 갱신 / 조건 분기 / 참조 호출: Math.max
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L65) **`extend(float duration)`**: 개별 처리 / 조건 분기
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L70) **`delay(float turns)`**: 개별 처리 / 참조 호출: spend
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L75) **`icon()`**: 개별 처리
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L80) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L84) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L89) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, dispTurns
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L94) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, CellEmitter.center, burst
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L103) **`detach()`**: 개별 처리 / 참조 호출: super.detach
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L109) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: target.isAlive, target.damage, spend, detach
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L130) **`totalIncomingDMG()`**: 개별 처리 / 반복 / 참조 호출: Math.ceil
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L139) **`onDeath()`**: 이벤트·효과 실행 / 참조 호출: Badges.validateDeathFromPoison, Dungeon.fail, GLog.n, Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 92. [`Preparation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 337행 / 타입 2개 / 필드 5개 / 메서드 25개.

### 타입·상속 선언

- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L54) `class Preparation  extends Buff implements ActionIndicator.Action`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L62) `enum AttackLevel`

### 변수·상수 (단일 행 선언)

- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L68) `int turnsReq`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L69) `float baseDmgBonus`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L70) `int damageRolls`
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L132) `int turnsInvis` 초기식: `0`
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L218) `String TURNS` 초기식: `"turnsInvis"`

### 함수·메서드 역할과 내부 연결

- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L86) **`KOThreshold()`**: 개별 처리 / 참조 호출: ordinal, Dungeon.hero.pointsInTalent
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L98) **`blinkDistance()`**: 개별 처리 / 참조 호출: ordinal, Dungeon.hero.pointsInTalent
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L102) **`canKO(Char defender)`**: 조건 판정 / 조건 분기 / 참조 호출: defender.properties, contains, KOThreshold
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L111) **`damageRoll(Char attacker)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: attacker.damageRoll, Math.round
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L120) **`getLvl(int turnsInvis)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: Arrays.asList, values, Collections.reverse
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L135) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: AttackLevel.getLvl, blinkDistance, ActionIndicator.setAction, spend, detach
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L149) **`detach()`**: 개별 처리 / 참조 호출: super.detach, ActionIndicator.clearAction
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L154) **`attackLevel()`**: 전투 관련 / 참조 호출: AttackLevel.getLvl, ordinal
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L158) **`damageRoll(Char attacker)`**: 전투 관련 / 참조 호출: AttackLevel.getLvl, damageRoll
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L162) **`canKO(Char defender)`**: 조건 판정 / 참조 호출: defender.isInvulnerable, target.getClass, AttackLevel.getLvl, canKO
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L167) **`icon()`**: 개별 처리
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L172) **`tintIcon(Image icon)`**: 개별 처리 / 상태 선택 / 참조 호출: AttackLevel.getLvl, icon.hardlight
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L190) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, AttackLevel.getLvl, lvl.KOThreshold, lvl.blinkDistance, lvl.ordinal, AttackLevel.values
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L221) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, ActionIndicator.setAction
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L228) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L234) **`actionName()`**: 시간·상태 갱신 / 참조 호출: Messages.get
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L239) **`actionIcon()`**: 시간·상태 갱신
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L244) **`primaryVisual()`**: 개별 처리 / 참조 호출: HeroIcon, tintIcon
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L251) **`secondaryVisual()`**: 개별 처리 / 참조 호출: BitmapText, txt.text, Integer.toString, Math.min, txt.hardlight, txt.measure
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L260) **`indicatorColor()`**: 개별 처리
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L265) **`doAction()`**: 개별 처리 / 참조 호출: GameScene.selectCell
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L269) **`Listener()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: onSelect, Actor.findChar, Dungeon.hero.isCharmedBy, GLog.w, Messages.get, Dungeon.hero.canAttack, HeroAction.Attack, Dungeon.hero.next, AttackLevel.getLvl
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L272) **`onSelect(Integer cell)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Actor.findChar, Dungeon.hero.isCharmedBy, GLog.w, Messages.get, Dungeon.hero.canAttack, HeroAction.Attack, Dungeon.hero.next, AttackLevel.getLvl, PathFinder.buildDistanceMap
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L274) **`findChar(cell)`**: 조회·탐색
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java#L332) **`prompt()`**: 개별 처리 / 참조 호출: Messages.get, AttackLevel.getLvl, blinkDistance

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 93. [`PrismaticGuard.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 185행 / 타입 1개 / 필드 4개 / 메서드 13개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L38) `class PrismaticGuard  extends Buff`

### 변수·상수 (단일 행 선언)

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L44) `float HP`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L46) `float powerOfManyTurns` 초기식: `0`
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L168) `String HEALTH` 초기식: `"hp"`
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L169) `String POWER_TURNS` 초기식: `"power_turns"`

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L49) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: hero.visibleEnemies, hero.visibleEnemy, mob.isAlive, mob.isInvulnerable, hero.mindVisionEnemies.contains, Dungeon.level.distance, Actor.findChar, Dungeon.level.trueDistance, PrismaticImage
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L109) **`set(int HP)`**: 상태 갱신
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L114) **`set(PrismaticImage img)`**: 상태 갱신 / 조건 분기 / 참조 호출: img.buff, cooldown
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L123) **`maxHP()`**: 개별 처리 / 참조 호출: maxHP
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L127) **`maxHP(Hero hero)`**: 개별 처리 / 참조 호출: Math.floor
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L131) **`isEmpowered()`**: 조건 판정
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L136) **`icon()`**: 개별 처리
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L141) **`tintIcon(Image icon)`**: 개별 처리 / 조건 분기 / 참조 호출: isEmpowered, icon.hardlight
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L150) **`iconFadePercent()`**: 개별 처리 / 참조 호출: maxHP
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L155) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L160) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, maxHP, isEmpowered
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L172) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PrismaticGuard.java#L179) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getFloat

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 94. [`Recharging.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Recharging.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 59행 / 타입 1개 / 필드 1개 / 메서드 4개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Recharging.java#L27) `class Recharging  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Recharging.java#L29) `float DURATION` 초기식: `30f`

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Recharging.java#L36) **`icon()`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Recharging.java#L41) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Recharging.java#L46) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Recharging.java#L55) **`remainder()`**: 개별 처리 / 참조 호출: Math.min, this.cooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 95. [`Regeneration.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Regeneration.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.buffs` / 본문 135행 / 타입 1개 / 필드 3개 / 메서드 5개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Regeneration.java#L34) `class Regeneration  extends Buff`

### 변수·상수 (단일 행 선언)

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Regeneration.java#L42) `float partialRegen` 초기식: `0f`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Regeneration.java#L44) `float REGENERATION_DELAY` 초기식: `10`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Regeneration.java#L121) `String PARTIAL_REGEN` 초기식: `"partial_regen"`

### 함수·메서드 역할과 내부 연결

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Regeneration.java#L47) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: target.isAlive, ChaoticCenser.averageTurnsUntilGas, Buff.affect, regenOn, regencap, isStarving, target.buff, Dungeon.hero.buff, isCursed
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Regeneration.java#L109) **`regencap()`**: 개별 처리
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Regeneration.java#L113) **`regenOn()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.buff, lock.regenOn
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Regeneration.java#L124) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Regeneration.java#L130) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getFloat

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":29,"fields":46,"methods":186}

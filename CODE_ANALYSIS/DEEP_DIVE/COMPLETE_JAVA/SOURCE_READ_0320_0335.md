# Java 파일별 소스 구현 해설 320–335

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 320. [`WoolParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WoolParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 58행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WoolParticle.java#L30) `class WoolParticle  extends PixelParticle.Shrinking`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WoolParticle.java#L32) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WoolParticle.java#L34) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WoolParticle.java#L39) **`WoolParticle()`**: 개별 처리 / 참조 호출: color, ColorMath.random, acc.set
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WoolParticle.java#L47) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, Random.Float, speed.set

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 321. [`Pushing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 147행 / 타입 2개 / 필드 9개 / 메서드 6개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L35) `class Pushing  extends Actor`
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L100) `class Effect  extends Visual`

### 변수·상수 (단일 행 선언)

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L37) `CharSprite sprite`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L38) `int from`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L39) `int to`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L41) `Effect effect`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L42) `Char ch`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L44) `Callback callback`
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L102) `float DELAY` 초기식: `0.15f`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L104) `PointF end`
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L106) `float delay`

### 함수·메서드 역할과 내부 연결

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L50) **`Pushing(Char ch, int from, int to)`**: 개별 처리 / 조건 분기 / 참조 호출: Camera.main.panFollow
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L62) **`Pushing(Char ch, int from, int to, Callback callback)`**: 개별 처리
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L68) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Actor.remove, Effect, Actor.all, actor.cooldown
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L91) **`pushingExistsForChar(Char ch)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: all
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L108) **`Effect()`**: 개별 처리 / 조건 분기 / 참조 호출: point, sprite.worldToCamera, speed.set, acc.set, sprite.parent.add
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Pushing.java#L124) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, sprite.point, killAndErase, Actor.remove, callback.call, GameScene.sortMobSprites, next

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 322. [`Ripple.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Ripple.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 64행 / 타입 1개 / 필드 2개 / 메서드 3개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Ripple.java#L29) `class Ripple  extends Image`

### 변수·상수 (단일 행 선언)

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Ripple.java#L31) `float TIME_TO_FADE` 초기식: `0.5f`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Ripple.java#L33) `float time`

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Ripple.java#L35) **`Ripple()`**: 개별 처리 / 참조 호출: Effects.get
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Ripple.java#L39) **`reset(int p)`**: 생성·초기화 / 참조 호출: revive, Dungeon.level.width, origin.set, scale.set
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Ripple.java#L52) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, kill, scale.set, alpha

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 323. [`ShadowBox.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShadowBox.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 53행 / 타입 1개 / 필드 1개 / 메서드 3개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShadowBox.java#L28) `class ShadowBox  extends NinePatch`

### 변수·상수 (단일 행 선언)

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShadowBox.java#L30) `float SIZE` 초기식: `16`

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShadowBox.java#L32) **`ShadowBox()`**: 개별 처리 / 조건 분기 / 참조 호출: texture.filter, scale.set
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShadowBox.java#L43) **`size(float width, float height)`**: 개별 처리 / 참조 호출: super.size
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShadowBox.java#L47) **`boxRect(float x, float y, float width, float height)`**: 개별 처리 / 참조 호출: size

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 324. [`ShieldHalo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShieldHalo.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 81행 / 타입 1개 / 필드 2개 / 메서드 4개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShieldHalo.java#L30) `class ShieldHalo  extends Halo`

### 변수·상수 (단일 행 선언)

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShieldHalo.java#L32) `CharSprite target`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShieldHalo.java#L34) `float phase`

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShieldHalo.java#L36) **`ShieldHalo(CharSprite sprite)`**: 개별 처리 / 참조 호출: Math.sqrt, Math.pow, sprite.width, sprite.height
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShieldHalo.java#L50) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, killAndErase, scale.set, target.center, point
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShieldHalo.java#L70) **`draw()`**: 지형/화면 표현 / 참조 호출: Blending.setLightMode, super.draw, Blending.setNormalMode
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShieldHalo.java#L76) **`putOut()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 325. [`Speck.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 564행 / 타입 1개 / 필드 42개 / 메서드 8개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L35) `class Speck  extends Image`

### 변수·상수 (단일 행 선언)

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L37) `int HEALING` 초기식: `0`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L38) `int STAR` 초기식: `1`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L39) `int LIGHT` 초기식: `2`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L40) `int QUESTION` 초기식: `3`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L41) `int UP` 초기식: `4`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L42) `int SCREAM` 초기식: `5`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L43) `int BONE` 초기식: `6`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L44) `int WOOL` 초기식: `7`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L45) `int ROCK` 초기식: `8`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L46) `int NOTE` 초기식: `9`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L47) `int CHANGE` 초기식: `10`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L48) `int HEART` 초기식: `11`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L49) `int BUBBLE` 초기식: `12`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L50) `int STEAM` 초기식: `13`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L51) `int COIN` 초기식: `14`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L52) `int DOWN` 초기식: `15`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L54) `int DISCOVER` 초기식: `101`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L55) `int EVOKE` 초기식: `102`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L56) `int MASK` 초기식: `103`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L57) `int CROWN` 초기식: `104`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L58) `int RATTLE` 초기식: `105`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L59) `int JET` 초기식: `106`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L60) `int TOXIC` 초기식: `107`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L61) `int CORROSION` 초기식: `108`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L62) `int PARALYSIS` 초기식: `109`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L63) `int DUST` 초기식: `110`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L64) `int STENCH` 초기식: `111`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L65) `int FORGE` 초기식: `112`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L66) `int CONFUSION` 초기식: `113`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L67) `int RED_LIGHT` 초기식: `114`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L68) `int CALM` 초기식: `115`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L69) `int SMOKE` 초기식: `116`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L70) `int STORM` 초기식: `117`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L71) `int INFERNO` 초기식: `118`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L72) `int BLIZZARD` 초기식: `119`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L73) `int YELLOW_LIGHT` 초기식: `120`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L74) `int BLUE_LIGHT` 초기식: `121`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L76) `int SIZE` 초기식: `7`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L78) `int type`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L79) `float lifespan`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L80) `float left`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L82) `TextureFilm film`

### 함수·메서드 역할과 내부 연결

- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L86) **`Speck()`**: 개별 처리 / 조건 분기 / 참조 호출: texture, TextureFilm, origin.set
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L97) **`image(int type)`**: 개별 처리 / 참조 호출: reset, resetColor, scale.set, speed.set, acc.set
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L113) **`reset(int index, float x, float y, int type)`**: 생성·초기화 / 상태 선택 / 참조 호출: revive, frame, film.get, resetColor, scale.set, speed.set, acc.set, speed.polar, Random.Float
- [L414](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L414) **`update()`**: 시간·상태 갱신 / 조건 분기·상태 선택 / 참조 호출: super.update, kill, scale.set, Math.sqrt, Math.cos
- [L538](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L538) **`factory(final int type)`**: 개별 처리 / 참조 호출: factory
- [L542](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L542) **`factory(final int type, final boolean lightMode)`**: 개별 처리 / 조건 분기 / 참조 호출: factories.get, Emitter.Factory, emit, emitter.recycle, p.reset, lightMode, factories.put
- [L549](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L549) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, p.reset
- [L554](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java#L554) **`lightMode()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 326. [`SpellSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 156행 / 타입 2개 / 필드 17개 / 메서드 6개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L34) `class SpellSprite  extends Image`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L47) `enum Phase`

### 변수·상수 (단일 행 선언)

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L36) `int FOOD` 초기식: `0`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L37) `int MAP` 초기식: `1`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L38) `int CHARGE` 초기식: `2`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L39) `int BERSERK` 초기식: `3`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L40) `int ANKH` 초기식: `4`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L41) `int HASTE` 초기식: `5`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L42) `int VISION` 초기식: `6`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L43) `int PURITY` 초기식: `7`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L45) `int SIZE` 초기식: `16`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L51) `float FADE_IN_TIME` 초기식: `0.2f`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L52) `float STATIC_TIME` 초기식: `0.8f`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L53) `float FADE_OUT_TIME` 초기식: `0.4f`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L55) `TextureFilm film`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L57) `Char target`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L59) `Phase phase`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L60) `float duration`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L61) `float passed`

### 함수·메서드 역할과 내부 연결

- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L65) **`SpellSprite()`**: 개별 처리 / 조건 분기 / 참조 호출: TextureFilm
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L73) **`reset(int index)`**: 생성·초기화 / 참조 호출: frame, film.get, origin.set
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L84) **`update()`**: 시간·상태 갱신 / 조건 분기·상태 선택 / 참조 호출: super.update, target.sprite.center, alpha, scale.set, kill
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L128) **`kill()`**: 개별 처리 / 참조 호출: super.kill, all.remove
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L133) **`show(Char ch, int index)`**: 개별 처리 / 참조 호출: show
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java#L137) **`show(Char ch, int index, float r, float g, float b)`**: 개별 처리 / 조건 분기 / 참조 호출: all.get, old.kill, GameScene.spellSprite, sprite.reset, sprite.hardlight, sprite.revive, all.put

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 327. [`Splash.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 137행 / 타입 2개 / 필드 3개 / 메서드 6개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java#L34) `class Splash`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java#L121) `class SplashFactory  extends Emitter.Factory`

### 변수·상수 (단일 행 선언)

- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java#L123) `int color`
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java#L124) `float dir`
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java#L125) `float cone`

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java#L36) **`at(int cell, final int color, int n)`**: 개별 처리 / 참조 호출: at, DungeonTilemap.tileCenterToWorld
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java#L40) **`at(PointF p, final int color, int n)`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.emitter, emitter.pos, FACTORIES.containsKey, FACTORIES.put, SplashFactory, FACTORIES.get, emitter.burst
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java#L60) **`at(PointF p, final float dir, final float cone, final int color, int n)`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.emitter, emitter.pos, FACTORIES.containsKey, FACTORIES.put, SplashFactory, FACTORIES.get, emitter.burst
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java#L79) **`around(Visual v, final int color, int n)`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.emitter, emitter.pos, FACTORIES.containsKey, FACTORIES.put, SplashFactory, FACTORIES.get, emitter.burst
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java#L98) **`at(PointF p, final float dir, final float cone, final int color, int n, float interval)`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.emitter, emitter.pos, FACTORIES.containsKey, FACTORIES.put, SplashFactory, FACTORIES.get, emitter.start
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java#L128) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, p.reset, Random.Float, p.speed.polar, p.acc.set

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 328. [`Surprise.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 99행 / 타입 1개 / 필드 2개 / 메서드 8개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java#L32) `class Surprise  extends Image`

### 변수·상수 (단일 행 선언)

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java#L34) `float TIME_TO_FADE` 초기식: `1f`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java#L36) `float time`

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java#L38) **`Surprise()`**: 개별 처리 / 참조 호출: Effects.get, origin.set
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java#L43) **`reset(int p)`**: 생성·초기화 / 참조 호출: revive, Dungeon.level.width
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java#L52) **`reset(Visual v)`**: 생성·초기화 / 참조 호출: revive, point, v.center
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java#L61) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, kill, alpha, Math.sqrt
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java#L74) **`hit(Char ch)`**: 전투 관련 / 참조 호출: hit
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java#L78) **`hit(Char ch, float angle)`**: 전투 관련 / 조건 분기 / 참조 호출: sprite.parent.recycle, sprite.parent.bringToFront, s.reset
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java#L87) **`hit(int pos)`**: 전투 관련 / 참조 호출: hit
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java#L91) **`hit(int pos, float angle)`**: 전투 관련 / 참조 호출: parent.recycle, parent.bringToFront, s.reset

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 329. [`Swap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 129행 / 타입 2개 / 필드 8개 / 메서드 5개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L35) `class Swap  extends Actor`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L88) `class Effect  extends Visual`

### 변수·상수 (단일 행 선언)

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L37) `Char ch1`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L38) `Char ch2`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L40) `Effect eff1`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L41) `Effect eff2`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L43) `float delay`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L90) `CharSprite sprite`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L91) `PointF end`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L92) `float passed`

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L45) **`Swap(Char ch1, Char ch2)`**: 개별 처리 / 참조 호출: Dungeon.level.distance, Effect, Sample.INSTANCE.play
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L58) **`act()`**: 시간·상태 갱신
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L62) **`finish(Effect eff)`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.remove, next, Dungeon.level.occupyCell, Dungeon.observe, GameScene.updateFog
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L94) **`Effect(CharSprite sprite, int from, int to)`**: 개별 처리 / 참조 호출: point, sprite.worldToCamera, speed.set, acc.set, sprite.parent.add
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Swap.java#L111) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, sprite.point, killAndErase, finish

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 330. [`TargetedCell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 106행 / 타입 1개 / 필드 6개 / 메서드 5개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java#L33) `class TargetedCell  extends Image implements Bundlable`

### 변수·상수 (단일 행 선언)

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java#L35) `int pos`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java#L36) `float time`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java#L38) `float alpha`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java#L89) `String POS` 초기식: `"pos"`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java#L90) `String COLOR` 초기식: `"color"`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java#L91) `String TIME` 초기식: `"time"`

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java#L42) **`reset(int pos, float time)`**: 생성·초기화 / 참조 호출: copy, Icons.get, origin.set, point, DungeonTilemap.tileToWorld, hardlight, alpha, scale.set, synchronized
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java#L64) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Actor.now, Math.max, alpha, scale.set, Math.pow, synchronized, cells.remove, killAndErase
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java#L81) **`fixTime(float min)`**: 개별 처리 / 반복 / 참조 호출: synchronized, cells.valueList
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java#L94) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: bundle.put
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java#L100) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 331. [`TorchHalo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TorchHalo.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 74행 / 타입 1개 / 필드 2개 / 메서드 4개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TorchHalo.java#L29) `class TorchHalo  extends Halo`

### 변수·상수 (단일 행 선언)

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TorchHalo.java#L31) `CharSprite target`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TorchHalo.java#L33) `float phase` 초기식: `0`

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TorchHalo.java#L35) **`TorchHalo(CharSprite sprite)`**: 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TorchHalo.java#L42) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, killAndErase, scale.set, point, target.width, target.height
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TorchHalo.java#L64) **`draw()`**: 지형/화면 표현 / 참조 호출: Blending.setLightMode, super.draw, Blending.setNormalMode
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TorchHalo.java#L70) **`putOut()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 332. [`Transmuting.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 155행 / 타입 2개 / 필드 8개 / 메서드 5개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L33) `class Transmuting  extends Component`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L35) `enum Phase`

### 변수·상수 (단일 행 선언)

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L39) `float FADE_IN_TIME` 초기식: `0.2f`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L40) `float TRANSMUTING_TIME` 초기식: `1.4f`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L41) `float FADE_OUT_TIME` 초기식: `0.4f`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L43) `float ALPHA` 초기식: `0.6f`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L48) `Char target`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L50) `Phase phase`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L51) `float duration`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L52) `float passed`

### 함수·메서드 역할과 내부 연결

- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L54) **`Transmuting(Item oldItem, Item newItem)`**: 개별 처리 / 참조 호출: ItemSprite, oldSprite.originToCenter, add, newSprite.originToCenter, oldSprite.alpha, newSprite.alpha
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L70) **`Transmuting(Talent oldTalent, Talent newTalent)`**: 개별 처리 / 참조 호출: TalentIcon, oldSprite.originToCenter, add, newSprite.originToCenter, oldSprite.alpha, newSprite.alpha
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L87) **`update()`**: 시간·상태 갱신 / 조건 분기·상태 선택 / 참조 호출: super.update, target.sprite.center, oldSprite.width, oldSprite.height, newSprite.width, newSprite.height, oldSprite.alpha, oldSprite.scale.set, newSprite.alpha
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L132) **`show(Char ch, Item oldItem, Item newItem)`**: 개별 처리 / 조건 분기 / 참조 호출: Transmuting, sprite.parent.add
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Transmuting.java#L143) **`show(Char ch, Talent oldTalent, Talent newTalent)`**: 개별 처리 / 조건 분기 / 참조 호출: Transmuting, sprite.parent.add

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 333. [`Wound.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 99행 / 타입 1개 / 필드 2개 / 메서드 8개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java#L32) `class Wound  extends Image`

### 변수·상수 (단일 행 선언)

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java#L34) `float TIME_TO_FADE` 초기식: `1f`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java#L36) `float time`

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java#L38) **`Wound()`**: 개별 처리 / 참조 호출: Effects.get, hardlight, origin.set
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java#L44) **`reset(int p)`**: 생성·초기화 / 참조 호출: revive, Dungeon.level.width
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java#L53) **`reset(Visual v)`**: 생성·초기화 / 참조 호출: revive, point, v.center
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java#L62) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, kill, alpha, Math.sqrt
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java#L74) **`hit(Char ch)`**: 전투 관련 / 참조 호출: hit
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java#L78) **`hit(Char ch, float angle)`**: 전투 관련 / 조건 분기 / 참조 호출: sprite.parent.recycle, sprite.parent.bringToFront, w.reset
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java#L87) **`hit(int pos)`**: 전투 관련 / 참조 호출: hit
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java#L91) **`hit(int pos, float angle)`**: 전투 관련 / 참조 호출: parent.recycle, parent.bringToFront, w.reset

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 334. [`GamesInProgress.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon` / 본문 223행 / 타입 2개 / 필드 28개 / 메서드 12개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L36) `class GamesInProgress`
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L177) `class Info`

### 변수·상수 (단일 행 선언)

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L42) `int curSlot`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L44) `HeroClass selectedClass`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L45) `boolean randomizedClass` 초기식: `false`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L47) `String GAME_FOLDER` 초기식: `"game%d"`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L48) `String GAME_FILE` 초기식: `"game.dat"`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L49) `String DEPTH_FILE` 초기식: `"depth%d.dat"`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L50) `String DEPTH_BRANCH_FILE` 초기식: `"depth%d-branch%d.dat"`
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L178) `int slot`
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L180) `int depth`
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L181) `int version`
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L182) `int challenges`
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L184) `long seed`
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L185) `String customSeed`
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L186) `boolean daily`
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L187) `boolean dailyReplay`
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L188) `long lastPlayed`
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L190) `int level`
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L191) `int str`
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L192) `int strBonus`
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L193) `int exp`
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L194) `int hp`
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L195) `int ht`
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L196) `int shld`
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L197) `HeroClass heroClass`
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L198) `HeroSubClass subClass`
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L199) `int armorTier`
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L201) `int goldCollected`
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L202) `int maxDepth`

### 함수·메서드 역할과 내부 연결

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L52) **`gameExists(int slot)`**: 개별 처리 / 참조 호출: FileUtils.dirExists, gameFolder, FileUtils.fileLength, gameFile
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L57) **`gameFolder(int slot)`**: 개별 처리 / 참조 호출: Messages.format
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L61) **`gameFile(int slot)`**: 개별 처리 / 참조 호출: gameFolder
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L65) **`depthFile(int slot, int depth, int branch)`**: 개별 처리 / 조건 분기 / 참조 호출: gameFolder, Messages.format
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L73) **`firstEmpty()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: check
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L80) **`checkAll()`**: 조건 판정 / 조건 분기·반복·상태 선택 / 참조 호출: check, result.add, SPDSettings.gamesInProgressSort, Collections.sort
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L98) **`check(int slot)`**: 조건 판정 / 조건 분기·예외 처리 / 참조 호출: slotStates.containsKey, slotStates.get, gameExists, slotStates.put, FileUtils.bundleFromFile, gameFile, bundle.getInt, Info, Dungeon.preview
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L138) **`set(int slot)`**: 상태 갱신 / 참조 호출: Info, Dungeon.hero.STR, Dungeon.hero.shielding, Dungeon.hero.tier, slotStates.put
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L169) **`setUnknown(int slot)`**: 상태 갱신 / 참조 호출: slotStates.remove
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L173) **`delete(int slot)`**: 개별 처리 / 참조 호출: slotStates.put
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L207) **`compare(GamesInProgress.Info lhs, GamesInProgress.Info rhs)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.signum, lastPlayedComparator.compare
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L218) **`compare(GamesInProgress.Info lhs, GamesInProgress.Info rhs)`**: 개별 처리 / 참조 호출: Math.signum

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 335. [`Amulet.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 146행 / 타입 1개 / 필드 1개 / 메서드 10개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java#L40) `class Amulet  extends Item`

### 변수·상수 (단일 행 선언)

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java#L42) `String AC_END` 초기식: `"END"`

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java#L51) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, hero.buff, actions.clear, actions.add
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java#L62) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, showAmuletScene
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java#L72) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doPickUp, hero.spend, hero.cooldown, Actor.add, Actor, act, Actor.remove, showAmuletScene
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java#L87) **`act()`**: 시간·상태 갱신 / 참조 호출: Actor.remove, showAmuletScene
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java#L101) **`showAmuletScene(boolean showText)`**: 개별 처리 / 예외 처리 / 참조 호출: Game.switchScene, Game.SceneChangeCallback, beforeCreate, afterCreate, Badges.validateVictory, Badges.validateChampion, Challenges.activeChallenges, Dungeon.saveAll, Badges.saveGlobal
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java#L105) **`beforeCreate()`**: 개별 처리
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java#L110) **`afterCreate()`**: 개별 처리 / 예외 처리 / 참조 호출: Badges.validateVictory, Badges.validateChampion, Challenges.activeChallenges, Dungeon.saveAll, Badges.saveGlobal, ShatteredPixelDungeon.reportException
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java#L124) **`isIdentified()`**: 조건 판정
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java#L129) **`isUpgradable()`**: 조건 판정
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java#L134) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, Dungeon.hero.buff, Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":22,"fields":133,"methods":97}

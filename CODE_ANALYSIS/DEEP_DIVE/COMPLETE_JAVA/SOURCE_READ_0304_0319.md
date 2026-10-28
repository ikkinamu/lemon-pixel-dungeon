# Java 파일별 소스 구현 해설 304–319

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 304. [`FlameParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlameParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 68행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlameParticle.java#L28) `class FlameParticle  extends PixelParticle.Shrinking`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlameParticle.java#L30) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlameParticle.java#L32) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlameParticle.java#L36) **`lightMode()`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlameParticle.java#L41) **`FlameParticle()`**: 개별 처리 / 참조 호출: color, acc.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlameParticle.java#L50) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.set
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlameParticle.java#L63) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 305. [`FlowParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 96행 / 타입 2개 / 필드 1개 / 메서드 7개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java#L32) `class FlowParticle  extends PixelParticle`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java#L71) `class Flow  extends Emitter`

### 변수·상수 (단일 행 선언)

- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java#L73) `int pos`

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java#L34) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java#L36) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java#L41) **`FlowParticle()`**: 개별 처리 / 참조 호출: acc.set, Random.Float
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java#L49) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, size, speed.set
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java#L63) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, size
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java#L75) **`Flow(int pos)`**: 개별 처리 / 참조 호출: DungeonTilemap.tileToWorld, pos, pour
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java#L87) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 306. [`LeafParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/LeafParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 73행 / 타입 1개 / 필드 2개 / 메서드 6개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/LeafParticle.java#L31) `class LeafParticle  extends PixelParticle.Shrinking`

### 변수·상수 (단일 행 선언)

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/LeafParticle.java#L33) `int color1`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/LeafParticle.java#L34) `int color2`

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/LeafParticle.java#L37) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, p.color, ColorMath.random, p.reset
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/LeafParticle.java#L39) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, p.color, ColorMath.random, p.reset
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/LeafParticle.java#L46) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, p.color, ColorMath.random, p.reset
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/LeafParticle.java#L48) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, p.color, ColorMath.random, p.reset
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/LeafParticle.java#L55) **`LeafParticle()`**: 개별 처리 / 참조 호출: acc.set
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/LeafParticle.java#L62) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.set, Random.Float

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 307. [`PitfallParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PitfallParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 64행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PitfallParticle.java#L28) `class PitfallParticle  extends PixelParticle.Shrinking`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PitfallParticle.java#L30) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PitfallParticle.java#L32) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PitfallParticle.java#L37) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PitfallParticle.java#L39) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PitfallParticle.java#L44) **`PitfallParticle()`**: 개별 처리 / 참조 호출: color, Random.Float
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PitfallParticle.java#L52) **`reset(float x, float y, int size)`**: 생성·초기화 / 참조 호출: revive

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 308. [`PoisonParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PoisonParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 92행 / 타입 1개 / 필드 0개 / 메서드 10개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PoisonParticle.java#L30) `class PoisonParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PoisonParticle.java#L32) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetMissile, lightMode
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PoisonParticle.java#L34) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetMissile
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PoisonParticle.java#L38) **`lightMode()`**: 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PoisonParticle.java#L43) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetSplash, lightMode
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PoisonParticle.java#L45) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetSplash
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PoisonParticle.java#L49) **`lightMode()`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PoisonParticle.java#L54) **`PoisonParticle()`**: 개별 처리 / 참조 호출: acc.set
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PoisonParticle.java#L62) **`resetMissile(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.polar, Random.Float
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PoisonParticle.java#L73) **`resetSplash(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.polar, Random.Float
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PoisonParticle.java#L85) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, size, color, ColorMath.interpolate

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 309. [`PurpleParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PurpleParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 87행 / 타입 1개 / 필드 0개 / 메서드 9개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PurpleParticle.java#L31) `class PurpleParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PurpleParticle.java#L33) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PurpleParticle.java#L35) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PurpleParticle.java#L40) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetBurst, lightMode
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PurpleParticle.java#L42) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetBurst
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PurpleParticle.java#L46) **`lightMode()`**: 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PurpleParticle.java#L51) **`PurpleParticle()`**: 개별 처리
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PurpleParticle.java#L57) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.set, Random.Float
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PurpleParticle.java#L68) **`resetBurst(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.polar, Random.Float
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/PurpleParticle.java#L80) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, size, color, ColorMath.interpolate

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 310. [`RainbowParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/RainbowParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 79행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/RainbowParticle.java#L29) `class RainbowParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/RainbowParticle.java#L31) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetBurst, lightMode
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/RainbowParticle.java#L33) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetBurst
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/RainbowParticle.java#L37) **`lightMode()`**: 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/RainbowParticle.java#L43) **`RainbowParticle()`**: 개별 처리 / 참조 호출: color, Random.Int
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/RainbowParticle.java#L50) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.set, Random.Float
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/RainbowParticle.java#L61) **`resetBurst(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.polar, Random.Float
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/RainbowParticle.java#L73) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, size

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 311. [`SacrificialParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SacrificialParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 68행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SacrificialParticle.java#L28) `class SacrificialParticle  extends PixelParticle.Shrinking`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SacrificialParticle.java#L30) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SacrificialParticle.java#L32) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SacrificialParticle.java#L36) **`lightMode()`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SacrificialParticle.java#L41) **`SacrificialParticle()`**: 개별 처리 / 참조 호출: color, acc.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SacrificialParticle.java#L50) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.set
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SacrificialParticle.java#L63) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 312. [`ShadowParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 97행 / 타입 1개 / 필드 0개 / 메서드 10개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java#L31) `class ShadowParticle  extends PixelParticle.Shrinking`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java#L33) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java#L35) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java#L40) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetCurse
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java#L42) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetCurse
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java#L47) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetUp
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java#L49) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetUp
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java#L54) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.set, Random.Float
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java#L66) **`resetCurse(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.polar, Random.Float
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java#L77) **`resetUp(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.set, Random.Float
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java#L89) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, color, ColorMath.interpolate

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 313. [`ShaftParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShaftParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 70행 / 타입 1개 / 필드 1개 / 메서드 6개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShaftParticle.java#L29) `class ShaftParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShaftParticle.java#L49) `float offs`

### 함수·메서드 역할과 내부 연결

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShaftParticle.java#L31) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShaftParticle.java#L33) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShaftParticle.java#L37) **`lightMode()`**: 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShaftParticle.java#L42) **`ShaftParticle()`**: 개별 처리 / 참조 호출: speed.set
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShaftParticle.java#L51) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, Random.Float
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShaftParticle.java#L62) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 314. [`SmokeParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SmokeParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 84행 / 타입 1개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SmokeParticle.java#L30) `class SmokeParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SmokeParticle.java#L32) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SmokeParticle.java#L34) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SmokeParticle.java#L39) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetSpew
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SmokeParticle.java#L41) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetSpew
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SmokeParticle.java#L46) **`SmokeParticle()`**: 개별 처리 / 참조 호출: color, acc.set
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SmokeParticle.java#L54) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, Random.Float, speed.set
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SmokeParticle.java#L64) **`resetSpew(float x, float y)`**: 생성·초기화 / 참조 호출: revive, acc.set, Random.Float, speed.polar
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SmokeParticle.java#L77) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, size

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 315. [`SnowParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SnowParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 59행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SnowParticle.java#L29) `class SnowParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SnowParticle.java#L31) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SnowParticle.java#L33) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SnowParticle.java#L38) **`SnowParticle()`**: 개별 처리 / 참조 호출: speed.set, Random.Float
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SnowParticle.java#L44) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SnowParticle.java#L54) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 316. [`SparkParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 108행 / 타입 1개 / 필드 0개 / 메서드 12개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L31) `class SparkParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L33) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L35) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L39) **`lightMode()`**: 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L44) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetStatic, lightMode
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L46) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetStatic
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L50) **`lightMode()`**: 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L55) **`SparkParticle()`**: 개별 처리 / 참조 호출: size, acc.set
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L63) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, Random.Float, speed.polar
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L75) **`resetStatic(float x, float y)`**: 생성·초기화 / 참조 호출: reset, Random.Float, acc.set, speed.set
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L84) **`resetAttracting(float x, float y, Visual attracting)`**: 생성·초기화 / 참조 호출: reset, Random.Float, acc.set, speed.set, speed.normalize, scale
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L99) **`setMaxSize(float value)`**: 상태 갱신
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java#L104) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, size, Random.Float

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 317. [`SpectralWallParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SpectralWallParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 131행 / 타입 1개 / 필드 2개 / 메서드 6개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SpectralWallParticle.java#L31) `class SpectralWallParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SpectralWallParticle.java#L60) `int type` 초기식: `0`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SpectralWallParticle.java#L61) `float xScale` 초기식: `0, yScale = 0`

### 함수·메서드 역할과 내부 연결

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SpectralWallParticle.java#L33) **`Factory()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: emit, GameMath.gate, Random.Int, emitter.recycle, reset, lightMode
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SpectralWallParticle.java#L35) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: GameMath.gate, Random.Int, emitter.recycle, reset
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SpectralWallParticle.java#L55) **`lightMode()`**: 개별 처리
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SpectralWallParticle.java#L63) **`SpectralWallParticle()`**: 개별 처리
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SpectralWallParticle.java#L71) **`reset(float x, float y)`**: 생성·초기화 / 조건 분기·상태 선택 / 참조 호출: revive, GameMath.gate, Math.round, color, ColorMath.random, ColorMath.interpolate
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SpectralWallParticle.java#L125) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, scale.set

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 318. [`WebParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WebParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 65행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WebParticle.java#L29) `class WebParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WebParticle.java#L31) **`Factory()`**: 개별 처리 / 반복 / 참조 호출: emit, emitter.recycle, reset
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WebParticle.java#L33) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 반복 / 참조 호출: emitter.recycle, reset
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WebParticle.java#L40) **`WebParticle()`**: 개별 처리 / 참조 호출: color
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WebParticle.java#L47) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, Random.Float
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WebParticle.java#L58) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 319. [`WindParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 101행 / 타입 2개 / 필드 1개 / 메서드 9개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java#L32) `class WindParticle  extends PixelParticle`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java#L77) `class Wind  extends Emitter`

### 변수·상수 (단일 행 선언)

- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java#L79) `int pos`

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java#L34) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java#L36) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java#L41) **`Float(PointF.PI2)`**: 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java#L42) **`PointF().polar( angle, 5)`**: 개별 처리
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java#L45) **`WindParticle()`**: 개별 처리 / 참조 호출: Random.Float, scale.set
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java#L52) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, super.speed.set, super.speed.scale, Random.Float, PointF, polar
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java#L70) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java#L81) **`Wind(int pos)`**: 개별 처리 / 참조 호출: DungeonTilemap.tileToWorld, pos, pour
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java#L92) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":18,"fields":7,"methods":118}

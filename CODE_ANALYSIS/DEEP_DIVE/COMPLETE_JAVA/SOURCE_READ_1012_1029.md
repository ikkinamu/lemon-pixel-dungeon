# Java 소스 구현 분석 1012–1029

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1012. [`EarthGuardianSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EarthGuardianSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 57행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EarthGuardianSprite.java#L27) `public class EarthGuardianSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EarthGuardianSprite.java#L29) `public EarthGuardianSprite() {` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EarthGuardianSprite.java#L52) `public int blood() {` — 개별 처리

## 1013. [`ElementalSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 261행.

### 클래스/타입
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L39) `public abstract class ElementalSprite extends MobSprite {`
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L132) `public static class Fire extends ElementalSprite {`
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L156) `public static class NewbornFire extends ElementalSprite {`
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L180) `public static class Frost extends ElementalSprite {`
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L204) `public static class Shock extends ElementalSprite {`
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L234) `public static class Chaos extends ElementalSprite {`

### 변수·상수 후보
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L41) `protected int boltType;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L45) `private Emitter particles;`

### 메서드 및 코드 의존 단서
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L43) `protected abstract int texOffset();` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L46) `protected abstract Emitter createEmitter();` — 생성·초기화
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L48) `public ElementalSprite() {` — 개별 처리
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L75) `public void link( Char ch ) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L84) `public void update() {` — 행동·상태 갱신, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L93) `public void die() {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L101) `public void kill() {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L108) `public void zap( int cell ) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L117) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L125) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L139) `protected int texOffset() {` — 개별 처리
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L144) `protected Emitter createEmitter() {` — 생성·초기화
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L151) `public int blood() {` — 개별 처리
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L163) `protected int texOffset() {` — 개별 처리
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L168) `protected Emitter createEmitter() {` — 생성·초기화, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L175) `public int blood() {` — 개별 처리, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L187) `protected int texOffset() {` — 개별 처리, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L192) `protected Emitter createEmitter() {` — 생성·초기화, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L199) `public int blood() {` — 개별 처리, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L208) `public void zap( int cell ) {` — 개별 처리, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L217) `protected int texOffset() {` — 개별 처리
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L222) `protected Emitter createEmitter() {` — 생성·초기화
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L229) `public int blood() {` — 개별 처리
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L237) `public void zap(int cell) {` — 개별 처리
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L244) `protected int texOffset() {` — 개별 처리
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L249) `protected Emitter createEmitter() {` — 생성·초기화
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ElementalSprite.java#L256) `public int blood() {` — 개별 처리

## 1014. [`EyeSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 142행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L35) `public class EyeSprite extends MobSprite {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L37) `private int zapPos;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L39) `private Animation charging;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L40) `private Emitter chargeParticles;`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L42) `public EyeSprite() {` — 개별 처리
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L69) `public void link(Char ch) {` — 개별 처리, 인접 호출: INSTANCE.play
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L81) `public void update() {` — 행동·상태 갱신, 인접 호출: INSTANCE.play
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L90) `public void die() {` — 개별 처리, 인접 호출: INSTANCE.play, Actor.findChar, Beam.DeathRay, DungeonTilemap.raisedTileCenterToWorld
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L98) `public void kill() {` — 개별 처리, 인접 호출: INSTANCE.play, Actor.findChar, Beam.DeathRay, DungeonTilemap.raisedTileCenterToWorld
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L105) `public void charge( int pos ){` — 개별 처리, 인접 호출: INSTANCE.play, Actor.findChar, Beam.DeathRay, DungeonTilemap.raisedTileCenterToWorld
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L112) `public void play(Animation anim) {` — 개별 처리, 인접 호출: Actor.findChar, Beam.DeathRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L118) `public void zap( int pos ) {` — 개별 처리, 인접 호출: Actor.findChar, Beam.DeathRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/EyeSprite.java#L124) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행, 인접 호출: Actor.findChar, Beam.DeathRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play

## 1015. [`FetidRatSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FetidRatSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 85행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FetidRatSprite.java#L30) `public class FetidRatSprite extends MobSprite {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FetidRatSprite.java#L32) `private Emitter cloud;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FetidRatSprite.java#L34) `public FetidRatSprite() {` — 개별 처리, 인접 호출: Speck.factory
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FetidRatSprite.java#L57) `public void link( Char ch ) {` — 개별 처리, 인접 호출: Speck.factory
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FetidRatSprite.java#L67) `public void update() {` — 행동·상태 갱신
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FetidRatSprite.java#L77) `public void kill() {` — 개별 처리

## 1016. [`FistSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 308행.

### 클래스/타입
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L42) `public abstract class FistSprite extends MobSprite {`
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L149) `public static class Burning extends FistSprite {`
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L174) `public static class Soiled extends FistSprite {`
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L199) `public static class Rotting extends FistSprite {`
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L224) `public static class Rusted extends FistSprite {`
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L249) `public static class Bright extends FistSprite {`
- [L282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L282) `public static class Dark extends FistSprite {`

### 변수·상수 후보
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L44) `private static final float SLAM_TIME	= 0.33f;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L46) `protected int boltType;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L50) `private Emitter particles;`

### 메서드 및 코드 의존 단서
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L48) `protected abstract int texOffset();` — 개별 처리, 인접 호출: Math.round
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L51) `protected abstract Emitter createEmitter();` — 생성·초기화, 인접 호출: Math.round
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L53) `public FistSprite() {` — 개별 처리, 인접 호출: Math.round
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L81) `public void link( Char ch ) {` — 개별 처리
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L90) `public void update() {` — 행동·상태 갱신, 인접 호출: MagicMissile.boltFromChar
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L99) `public void die() {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play, PixelScene.shake
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L107) `public void kill() {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play, PixelScene.shake
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L115) `public void attack( int cell ) {` — 전투 관련, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play, PixelScene.shake
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L122) `public void zap( int cell ) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play, PixelScene.shake
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L132) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play, PixelScene.shake
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L140) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행, 인접 호출: PixelScene.shake
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L156) `protected int texOffset() {` — 개별 처리
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L161) `protected Emitter createEmitter() {` — 생성·초기화
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L168) `public int blood() {` — 개별 처리
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L181) `protected int texOffset() {` — 개별 처리, 인접 호출: Speck.factory
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L186) `protected Emitter createEmitter() {` — 생성·초기화, 인접 호출: Speck.factory
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L193) `public int blood() {` — 개별 처리, 인접 호출: Speck.factory
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L206) `protected int texOffset() {` — 개별 처리, 인접 호출: Speck.factory
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L211) `protected Emitter createEmitter() {` — 생성·초기화, 인접 호출: Speck.factory
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L218) `public int blood() {` — 개별 처리
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L231) `protected int texOffset() {` — 개별 처리, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L236) `protected Emitter createEmitter() {` — 생성·초기화, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L243) `public int blood() {` — 개별 처리, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L256) `protected int texOffset() {` — 개별 처리, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L261) `protected Emitter createEmitter() {` — 생성·초기화, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L268) `public void zap( int cell ) {` — 개별 처리, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L276](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L276) `public int blood() {` — 개별 처리
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L289) `protected int texOffset() {` — 개별 처리
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L294) `protected Emitter createEmitter() {` — 생성·초기화
- [L301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FistSprite.java#L301) `public int blood() {` — 개별 처리

## 1017. [`FungalCoreSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalCoreSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 98행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalCoreSprite.java#L30) `public class FungalCoreSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalCoreSprite.java#L32) `public FungalCoreSprite(){` — 개별 처리, 인접 호출: GameScene.updateMap
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalCoreSprite.java#L60) `public void update() {` — 행동·상태 갱신, 인접 호출: GameScene.updateMap
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalCoreSprite.java#L77) `public void die() {` — 개별 처리, 인접 호출: GameScene.updateMap
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalCoreSprite.java#L88) `public void turnTo(int from, int to) {` — 개별 처리
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalCoreSprite.java#L93) `public int blood() {` — 개별 처리

## 1018. [`FungalSentrySprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSentrySprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 100행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSentrySprite.java#L30) `public class FungalSentrySprite extends MobSprite {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSentrySprite.java#L32) `private int cellToAttack;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSentrySprite.java#L34) `public FungalSentrySprite(){` — 개별 처리, 인접 호출: MagicMissile.boltFromChar
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSentrySprite.java#L60) `public void attack( int cell ) {` — 전투 관련, 인접 호출: MagicMissile.boltFromChar
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSentrySprite.java#L74) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행, 인접 호출: MagicMissile.boltFromChar
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSentrySprite.java#L80) `public void call() {` — 개별 처리
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSentrySprite.java#L90) `public void turnTo(int from, int to) {` — 개별 처리
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSentrySprite.java#L95) `public int blood() {` — 개별 처리

## 1019. [`FungalSpinnerSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSpinnerSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 103행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSpinnerSprite.java#L33) `public class FungalSpinnerSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSpinnerSprite.java#L35) `public FungalSpinnerSprite() {` — 개별 처리, 인접 호출: MovieClip.Animation, MagicMissile.boltFromChar
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSpinnerSprite.java#L62) `public void link(Char ch) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSpinnerSprite.java#L73) `public void zap( int cell ) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSpinnerSprite.java#L83) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSpinnerSprite.java#L91) `public void onComplete( MovieClip.Animation anim ) {` — 이벤트·효과 실행
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/FungalSpinnerSprite.java#L99) `public int blood() {` — 개별 처리

## 1020. [`GhostSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhostSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 73행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhostSprite.java#L30) `public class GhostSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhostSprite.java#L32) `public GhostSprite() {` — 개별 처리, 인접 호출: Blending.setLightMode, Blending.setNormalMode, Speck.factory
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhostSprite.java#L55) `public void draw() {` — 개별 처리, 인접 호출: Blending.setLightMode, Blending.setNormalMode, Speck.factory
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhostSprite.java#L62) `public void die() {` — 개별 처리, 인접 호출: Speck.factory
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhostSprite.java#L69) `public int blood() {` — 개별 처리

## 1021. [`GhoulSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhoulSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 71행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhoulSprite.java#L27) `public class GhoulSprite extends MobSprite {`

### 변수·상수 후보
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhoulSprite.java#L29) `private Animation crumple;`

### 메서드 및 코드 의존 단서
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhoulSprite.java#L31) `public GhoulSprite() {` — 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhoulSprite.java#L56) `public void crumple(){` — 개별 처리
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhoulSprite.java#L63) `public void die() {` — 개별 처리

## 1022. [`GnollExileSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollExileSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 54행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollExileSprite.java#L27) `public class GnollExileSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollExileSprite.java#L29) `public GnollExileSprite() {` — 개별 처리

## 1023. [`GnollGeomancerSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 152행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L31) `public class GnollGeomancerSprite extends MobSprite {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L35) `private Emitter earthArmor;`

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L37) `public GnollGeomancerSprite() {` — 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L48) `public void link( Char ch ) {` — 개별 처리
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L60) `private void updateAnims(){` — 행동·상태 갱신
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L84) `public void setupArmor(){` — 생성·초기화
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L96) `public void loseArmor(){` — 개별 처리
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L104) `public void update() {` — 행동·상태 갱신
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L113) `public void die() {` — 개별 처리
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L122) `public void kill() {` — 개별 처리
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L131) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L139) `public void idle() {` — 개별 처리
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGeomancerSprite.java#L148) `public int blood() {` — 개별 처리

## 1024. [`GnollGuardSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGuardSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 114행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGuardSprite.java#L31) `public class GnollGuardSprite extends MobSprite {`

### 변수·상수 후보
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGuardSprite.java#L33) `private Emitter earthArmor;`

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGuardSprite.java#L35) `public GnollGuardSprite() {` — 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGuardSprite.java#L58) `public void link( Char ch ) {` — 개별 처리
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGuardSprite.java#L66) `public void setupArmor(){` — 생성·초기화
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGuardSprite.java#L78) `public void loseArmor(){` — 개별 처리
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGuardSprite.java#L86) `public void update() {` — 행동·상태 갱신
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGuardSprite.java#L95) `public void die() {` — 개별 처리
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollGuardSprite.java#L104) `public void kill() {` — 개별 처리

## 1025. [`GnollSapperSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollSapperSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 62행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollSapperSprite.java#L27) `public class GnollSapperSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollSapperSprite.java#L29) `public GnollSapperSprite() {` — 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollSapperSprite.java#L54) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행

## 1026. [`GnollSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 51행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollSprite.java#L27) `public class GnollSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollSprite.java#L29) `public GnollSprite() {` — 개별 처리

## 1027. [`GnollTricksterSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollTricksterSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 83행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollTricksterSprite.java#L31) `public class GnollTricksterSprite extends MobSprite {`

### 변수·상수 후보
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollTricksterSprite.java#L33) `private Animation cast;`

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollTricksterSprite.java#L35) `public GnollTricksterSprite() {` — 개별 처리, 인접 호출: MovieClip.Animation
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollTricksterSprite.java#L62) `public void attack( int cell ) {` — 전투 관련
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GnollTricksterSprite.java#L68) `public void call() {` — 개별 처리

## 1028. [`GolemSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 139행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L35) `public class GolemSprite extends MobSprite {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L37) `private Emitter teleParticles;`
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L125) `private boolean died = false;`

### 메서드 및 코드 의존 단서
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L39) `public GolemSprite() {` — 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L64) `public void link(Char ch) {` — 개별 처리
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L74) `public void update() {` — 행동·상태 갱신, 인접 호출: MagicMissile.boltFromChar
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L83) `public void kill() {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L91) `public void teleParticles(boolean value){` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L96) `public synchronized void play(Animation anim, boolean force) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L102) `public int blood() {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L106) `public void zap( int cell ) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L116) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GolemSprite.java#L128) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행

## 1029. [`GooSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 224행.

### 클래스/타입
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L40) `public class GooSprite extends MobSprite {`
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L171) `public static class GooParticle extends PixelParticle.Shrinking {`

### 변수·상수 후보
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L42) `private Animation pump;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L43) `private Animation pumpAttack;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L45) `private Emitter spray;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L47) `private int pumpUpEmitterDist = 0;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L48) `private int lastPumpUpPos = -1;`

### 메서드 및 코드 의존 단서
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L51) `public GooSprite() {` — 개별 처리
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L87) `public void link(Char ch) {` — 개별 처리, 인접 호출: INSTANCE.play, CellEmitter.get
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L93) `public void pumpUp( int warnDist ) {` — 개별 처리, 인접 호출: INSTANCE.play, CellEmitter.get
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L102) `public void updateEmitters( ){` — 행동·상태 갱신, 인접 호출: CellEmitter.get, INSTANCE.play
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L123) `public void clearEmitters(){` — 개별 처리, 인접 호출: INSTANCE.play
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L130) `public void triggerEmitters(){` — 이벤트·효과 실행, 인접 호출: INSTANCE.play
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L139) `public void pumpAttack() { play(pumpAttack); }` — 개별 처리
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L142) `public void play(Animation anim) {` — 개별 처리
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L151) `public int blood() {` — 개별 처리
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L155) `public void spray(boolean on){` — 개별 처리, 인접 호출: Random.Float
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L160) `public void update() {` — 행동·상태 갱신, 인접 호출: Random.Float
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L173) `public static final Emitter.Factory FACTORY = new Factory() {` — 개별 처리, 인접 호출: Random.Float
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L175) `public void emit( Emitter emitter, int index, float x, float y ) {` — 개별 처리, 인접 호출: Random.Float
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L180) `public GooParticle() {` — 개별 처리, 인접 호출: Random.Float
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L189) `public void reset( float x, float y ) {` — 개별 처리, 인접 호출: Random.Float
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L202) `public void update() {` — 행동·상태 갱신
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GooSprite.java#L210) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행


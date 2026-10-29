# Java 소스 구현 분석 1066–1083

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1066. [`SpawnerSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpawnerSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 87행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpawnerSprite.java#L30) `public class SpawnerSprite extends MobSprite {`

### 변수·상수 후보
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpawnerSprite.java#L56) `private float baseY = Float.NaN;`

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpawnerSprite.java#L32) `public SpawnerSprite() {` — 개별 처리, 인접 호출: Float.isNaN, Math.sin, Splash.around
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpawnerSprite.java#L59) `public void place(int cell) {` — 개별 처리, 인접 호출: Float.isNaN, Math.sin, Splash.around
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpawnerSprite.java#L65) `public void update() {` — 행동·상태 갱신, 인접 호출: Float.isNaN, Math.sin, Splash.around
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpawnerSprite.java#L75) `public void die() {` — 개별 처리, 인접 호출: Splash.around
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpawnerSprite.java#L81) `public void bloodBurstA(PointF from, int damage) {` — 개별 처리

## 1067. [`SpectralNecromancerSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 155행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L34) `public class SpectralNecromancerSprite extends MobSprite {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L36) `private Animation charging;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L37) `private Emitter summoningParticles;`

### 메서드 및 코드 의존 단서
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L39) `public SpectralNecromancerSprite(){` — 개별 처리
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L68) `public void link(Char ch) {` — 개별 처리, 인접 호출: INSTANCE.play
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L76) `public void update() {` — 행동·상태 갱신, 인접 호출: INSTANCE.play
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L84) `public void die() {` — 개별 처리, 인접 호출: INSTANCE.play
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L93) `public void kill() {` — 개별 처리, 인접 호출: INSTANCE.play, CellEmitter.get
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L101) `public void cancelSummoning(){` — 조회·판정, 인접 호출: INSTANCE.play, CellEmitter.get
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L108) `public void finishSummoning(){` — 개별 처리, 인접 호출: INSTANCE.play, CellEmitter.get
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L119) `public void charge(){` — 개별 처리, 인접 호출: CellEmitter.get, INSTANCE.play
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L124) `public void zap(int cell) {` — 개별 처리, 인접 호출: CellEmitter.get, INSTANCE.play
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpectralNecromancerSprite.java#L138) `public void onComplete(Animation anim) {` — 이벤트·효과 실행

## 1068. [`SpinnerSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpinnerSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 103행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpinnerSprite.java#L33) `public class SpinnerSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpinnerSprite.java#L35) `public SpinnerSprite() {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpinnerSprite.java#L62) `public void link(Char ch) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpinnerSprite.java#L73) `public void zap( int cell ) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpinnerSprite.java#L83) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpinnerSprite.java#L91) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SpinnerSprite.java#L99) `public int blood() {` — 개별 처리

## 1069. [`StatueSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/StatueSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 73행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/StatueSprite.java#L28) `public class StatueSprite extends MobSprite {`

### 변수·상수 후보
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/StatueSprite.java#L52) `private static int[] tierFrames = {0, 21, 32, 43, 54, 65};`

### 메서드 및 코드 의존 단서
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/StatueSprite.java#L30) `public StatueSprite() {` — 개별 처리, 인접 호출: GameMath.gate
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/StatueSprite.java#L54) `public void setArmor( int tier ){` — 개별 처리, 인접 호출: GameMath.gate
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/StatueSprite.java#L69) `public int blood() {` — 개별 처리

## 1070. [`SuccubusSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SuccubusSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 60행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SuccubusSprite.java#L29) `public class SuccubusSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SuccubusSprite.java#L31) `public SuccubusSprite() {` — 개별 처리, 인접 호출: Speck.factory
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SuccubusSprite.java#L54) `public void die() {` — 개별 처리, 인접 호출: Speck.factory

## 1071. [`SwarmSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SwarmSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 56행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SwarmSprite.java#L27) `public class SwarmSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SwarmSprite.java#L29) `public SwarmSprite() {` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SwarmSprite.java#L52) `public int blood() {` — 개별 처리

## 1072. [`TenguSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TenguSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 134행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TenguSprite.java#L31) `public class TenguSprite extends MobSprite {`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TenguSprite.java#L128) `public static class TenguShuriken extends Item {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TenguSprite.java#L33) `public TenguSprite() {` — 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TenguSprite.java#L59) `public void play(Animation anim) {` — 개별 처리, 인접 호출: GameScene.ripple
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TenguSprite.java#L61) `synchronized (this){` — 개별 처리, 인접 호출: GameScene.ripple
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TenguSprite.java#L70) `public void move( int from, int to ) {` — 개별 처리, 인접 호출: GameScene.ripple
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TenguSprite.java#L86) `public void update() {` — 행동·상태 갱신
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TenguSprite.java#L94) `public void attack( int cell ) {` — 전투 관련
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TenguSprite.java#L100) `public void call() {` — 개별 처리
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TenguSprite.java#L115) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TenguSprite.java#L117) `synchronized (this){` — 개별 처리

## 1073. [`ThiefSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ThiefSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 50행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ThiefSprite.java#L27) `public class ThiefSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ThiefSprite.java#L29) `public ThiefSprite() {` — 개별 처리

## 1074. [`TormentedSpiritSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TormentedSpiritSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 58행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TormentedSpiritSprite.java#L27) `public class TormentedSpiritSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TormentedSpiritSprite.java#L29) `public TormentedSpiritSprite() {` — 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/TormentedSpiritSprite.java#L54) `public int blood() {` — 개별 처리

## 1075. [`UndeadSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/UndeadSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 66행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/UndeadSprite.java#L29) `public class UndeadSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/UndeadSprite.java#L31) `public UndeadSprite() {` — 개별 처리, 인접 호출: Speck.factory
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/UndeadSprite.java#L54) `public void die() {` — 개별 처리, 인접 호출: Speck.factory
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/UndeadSprite.java#L62) `public int blood() {` — 개별 처리

## 1076. [`VaultBossElementalSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 274행.

### 클래스/타입
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L43) `public class VaultBossElementalSprite extends MobSprite {`

### 변수·상수 후보
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L45) `private Emitter particles;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L47) `private Emitter[] doorLockVfx;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L53) `private VaultBossElemental.ElementalForm form;`

### 메서드 및 코드 의존 단서
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L55) `public VaultBossElementalSprite() {` — 개별 처리, 인접 호출: ElementalForm.values, Random.Int
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L63) `public void setForm(VaultBossElemental.ElementalForm form){` — 개별 처리, 인접 호출: ElementalForm.values, Random.Int
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L69) `public void linkVisuals(Char ch) {` — 개별 처리, 인접 호출: ElementalForm.values, Random.Int
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L77) `public void updateForm(){` — 행동·상태 갱신, 인접 호출: ElementalForm.values, Random.Int
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L84) `private void updateAnimations(){` — 행동·상태 갱신, 인접 호출: ElementalForm.values, Random.Int
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L126) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L134) `public void zap(int cell) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L145) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L170) `private Emitter createEmitter() {` — 생성·초기화, 인접 호출: CellEmitter.get
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L189) `private Emitter[] createDoorEmitters(){` — 생성·초기화, 인접 호출: CellEmitter.get
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L217) `public void link( Char ch ) {` — 개별 처리
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L229) `public void update() {` — 행동·상태 갱신
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L238) `public void die() {` — 개별 처리
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L250) `public void kill() {` — 개별 처리
- [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultBossElementalSprite.java#L262) `public int blood() {` — 개별 처리

## 1077. [`VaultMirrorSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultMirrorSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 67행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultMirrorSprite.java#L28) `public class VaultMirrorSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultMirrorSprite.java#L30) `public VaultMirrorSprite () {` — 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultMirrorSprite.java#L56) `public void turnTo(int from, int to) {` — 개별 처리
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultMirrorSprite.java#L61) `public void link(Char ch) {` — 개별 처리

## 1078. [`VaultTokenDoorSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultTokenDoorSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 60행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultTokenDoorSprite.java#L28) `public class VaultTokenDoorSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultTokenDoorSprite.java#L30) `public VaultTokenDoorSprite () {` — 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/VaultTokenDoorSprite.java#L54) `public void link(Char ch) {` — 개별 처리

## 1079. [`WandmakerSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WandmakerSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 73행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WandmakerSprite.java#L31) `public class WandmakerSprite extends MobSprite {`

### 변수·상수 후보
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WandmakerSprite.java#L33) `private ShieldHalo shield;`

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WandmakerSprite.java#L35) `public WandmakerSprite() {` — 개별 처리, 인접 호출: INSTANCE.play
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WandmakerSprite.java#L55) `public void link( Char ch ) {` — 개별 처리, 인접 호출: INSTANCE.play
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WandmakerSprite.java#L61) `public void die() {` — 개별 처리, 인접 호출: INSTANCE.play

## 1080. [`WardSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 170행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L35) `public class WardSprite extends MobSprite {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L37) `private Animation tierIdles[] = new Animation[7];`
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L146) `private float baseY = Float.NaN;`

### 메서드 및 코드 의존 단서
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L39) `public WardSprite(){` — 개별 처리, 인접 호출: Actor.findChar, Beam.DeathRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L65) `public void zap( int pos ) {` — 개별 처리, 인접 호출: Actor.findChar, Beam.DeathRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play, Math.max
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L79) `public void turnTo(int from, int to) {` — 개별 처리, 인접 호출: Math.max
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L84) `public void die() {` — 개별 처리, 인접 호출: Math.max
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L91) `protected void onComplete() {` — 이벤트·효과 실행, 인접 호출: Math.max
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L99) `public void resetColor() {` — 개별 처리, 인접 호출: Math.max
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L109) `public void linkVisuals(Char ch ){` — 개별 처리
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L119) `public void updateTier(int tier){` — 행동·상태 갱신, 인접 호출: Float.isNaN, Math.sin
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L149) `public void place(int cell) {` — 개별 처리, 인접 호출: Float.isNaN, Math.sin
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L155) `public void update() {` — 행동·상태 갱신, 인접 호출: Float.isNaN, Math.sin
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WardSprite.java#L166) `public int blood() {` — 개별 처리

## 1081. [`WarlockSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WarlockSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 82행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WarlockSprite.java#L31) `public class WarlockSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WarlockSprite.java#L33) `public WarlockSprite() {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WarlockSprite.java#L57) `public void zap( int cell ) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WarlockSprite.java#L67) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WarlockSprite.java#L75) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행

## 1082. [`WraithSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WraithSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 56행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WraithSprite.java#L27) `public class WraithSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WraithSprite.java#L29) `public WraithSprite() {` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/WraithSprite.java#L52) `public int blood() {` — 개별 처리

## 1083. [`YogSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/YogSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 68행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/YogSprite.java#L29) `public class YogSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/YogSprite.java#L31) `public YogSprite() {` — 개별 처리, 인접 호출: Splash.at
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/YogSprite.java#L56) `public void link(Char ch) {` — 개별 처리, 인접 호출: Splash.at
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/YogSprite.java#L62) `public void die() {` — 개별 처리, 인접 호출: Splash.at


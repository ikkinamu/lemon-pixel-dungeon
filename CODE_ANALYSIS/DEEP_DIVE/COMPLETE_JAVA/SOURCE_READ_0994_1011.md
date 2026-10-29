# Java 소스 구현 분석 994–1011

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 994. [`AcidicSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/AcidicSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 58행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/AcidicSprite.java#L27) `public class AcidicSprite extends ScorpioSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/AcidicSprite.java#L29) `public AcidicSprite() {` — 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/AcidicSprite.java#L54) `public int blood() {` — 개별 처리

## 995. [`AlbinoSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/AlbinoSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 51행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/AlbinoSprite.java#L27) `public class AlbinoSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/AlbinoSprite.java#L29) `public AlbinoSprite() {` — 개별 처리

## 996. [`BanditSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BanditSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 50행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BanditSprite.java#L27) `public class BanditSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BanditSprite.java#L29) `public BanditSprite() {` — 개별 처리

## 997. [`BatSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BatSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 51행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BatSprite.java#L27) `public class BatSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BatSprite.java#L29) `public BatSprite() {` — 개별 처리

## 998. [`BeeSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BeeSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 56행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BeeSprite.java#L27) `public class BeeSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BeeSprite.java#L29) `public BeeSprite() {` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BeeSprite.java#L52) `public int blood() {` — 개별 처리

## 999. [`BlacksmithSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BlacksmithSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 89행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BlacksmithSprite.java#L33) `public class BlacksmithSprite extends MobSprite {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BlacksmithSprite.java#L35) `private Emitter emitter;`

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BlacksmithSprite.java#L37) `public BlacksmithSprite() {` — 개별 처리, 인접 호출: Speck.factory, INSTANCE.paused
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BlacksmithSprite.java#L57) `public void link( Char ch ) {` — 개별 처리, 인접 호출: Speck.factory, INSTANCE.paused, INSTANCE.play
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BlacksmithSprite.java#L67) `public void update() {` — 행동·상태 갱신, 인접 호출: Speck.factory, INSTANCE.paused, INSTANCE.play
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BlacksmithSprite.java#L76) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행, 인접 호출: Speck.factory, INSTANCE.paused, INSTANCE.play

## 1000. [`BruteSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BruteSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 51행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BruteSprite.java#L27) `public class BruteSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BruteSprite.java#L29) `public BruteSprite() {` — 개별 처리

## 1001. [`CausticSlimeSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CausticSlimeSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 54행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CausticSlimeSprite.java#L27) `public class CausticSlimeSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CausticSlimeSprite.java#L29) `public CausticSlimeSprite() {` — 개별 처리

## 1002. [`CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 893행.

### 클래스/타입
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L63) `public class CharSprite extends MovieClip implements Tweener.Listener, MovieClip.Listener {`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L88) `public enum State {`
- [L866](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L866) `private static class JumpTweener extends Tweener {`

### 변수·상수 후보
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L66) `public static final int DEFAULT		= 0xFFFFFF;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L67) `public static final int POSITIVE	= 0x00FF00;`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L68) `public static final int NEGATIVE	= 0xFF0000;`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L69) `public static final int WARNING		= 0xFF8800;`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L70) `public static final int NEUTRAL		= 0xFFFF00;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L72) `public static final float DEFAULT_MOVE_INTERVAL = 0.1f;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L73) `private static float moveInterval = DEFAULT_MOVE_INTERVAL;`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L74) `private static final float FLASH_INTERVAL	= 0.05f;`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L81) `protected boolean renderShadow  = false;`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L82) `protected float shadowWidth     = 1.2f;`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L83) `protected float shadowHeight    = 0.25f;`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L84) `protected float shadowOffset    = 0.25f;`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L86) `public boolean visibleOutOfFFOV = false;`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L92) `protected Animation idle;`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L93) `protected Animation run;`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L94) `protected Animation attack;`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L95) `protected Animation operate;`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L96) `protected Animation zap;`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L97) `protected Animation die;`
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L99) `protected Callback animCallback;`
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L101) `protected PosTweener motion;`
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L103) `protected Emitter burning;`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L104) `protected Emitter chilled;`
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L105) `protected Emitter marked;`
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L106) `protected Emitter levitation;`
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L107) `protected Emitter healing;`
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L108) `protected Emitter hearts;`
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L110) `protected IceBlock iceBlock;`
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L111) `protected DarkBlock darkBlock;`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L112) `protected GlowBlock glowBlock;`
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L113) `protected TorchHalo light;`
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L114) `protected ShieldHalo shield;`
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L115) `protected AlphaTweener invisible;`
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L116) `protected Flare aura;`
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L118) `protected EmoIcon emo;`
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L119) `protected CharHealthIndicator health;`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L121) `private Tweener jumpTweener;`
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L122) `private Callback jumpCallback;`
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L124) `protected float flashTime = 0;`
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L126) `protected boolean sleeping = false;`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L128) `public Char ch;`
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L131) `public volatile boolean isMoving = false;`
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L183) `final int csize = DungeonTilemap.SIZE;`
- [L378](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L378) `private int auraColor = 0;`
- [L379](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L379) `private int auraRays = 0;`
- [L766](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L766) `private float[] shadowMatrix = new float[16];`
- [L868](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L868) `public CharSprite visual;`
- [L870](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L870) `public PointF start;`
- [L871](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L871) `public PointF end;`
- [L873](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L873) `public float height;`

### 메서드 및 코드 의존 단서
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L133) `public CharSprite() {` — 개별 처리, 인접 호출: Random.Int
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L139) `public void play(Animation anim) {` — 개별 처리, 인접 호출: Random.Int
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L147) `public void link( Char ch ) {` — 개별 처리, 인접 호출: Random.Int, PixelScene.align
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L169) `public void destroy() {` — 개별 처리, 인접 호출: PixelScene.align, Messages.format, DungeonTilemap.worldToTile, FloatingText.show
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L177) `public void linkVisuals( Char ch ){` — 개별 처리, 인접 호출: PixelScene.align, Messages.format, DungeonTilemap.worldToTile, FloatingText.show
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L181) `public PointF worldToCamera( int cell ) {` — 개별 처리, 인접 호출: PixelScene.align, Messages.format, DungeonTilemap.worldToTile, FloatingText.show
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L191) `public void place( int cell ) {` — 개별 처리, 인접 호출: Messages.format, DungeonTilemap.worldToTile, FloatingText.show, GameScene.ripple
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L195) `public void showStatus( int color, String text, Object... args ) {` — 개별 처리, 인접 호출: Messages.format, DungeonTilemap.worldToTile, FloatingText.show, GameScene.ripple
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L199) `public void showStatusWithIcon( int color, String text, int icon, Object... args ) {` — 개별 처리, 인접 호출: Messages.format, DungeonTilemap.worldToTile, FloatingText.show, GameScene.ripple
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L215) `public void idle() {` — 개별 처리, 인접 호출: GameScene.ripple
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L219) `public void move( int from, int to ) {` — 개별 처리, 인접 호출: GameScene.ripple
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L236) `public static void setMoveInterval( float interval){` — 개별 처리
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L241) `public PointF destinationCenter(){` — 개별 처리
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L250) `public void interruptMotion() {` — 개별 처리
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L256) `public void attack( int cell ) {` — 전투 관련, 인접 호출: Math.max
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L260) `public synchronized void attack( int cell, Callback callback ) {` — 전투 관련, 인접 호출: Math.max
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L266) `public void operate( int cell ) {` — 개별 처리, 인접 호출: Math.max
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L270) `public synchronized void operate( int cell, Callback callback ) {` — 개별 처리, 인접 호출: Math.max
- [L276](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L276) `public void zap( int cell ) {` — 개별 처리, 인접 호출: Math.max
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L280) `public synchronized void zap( int cell, Callback callback ) {` — 개별 처리, 인접 호출: Math.max, GameScene.emitter
- [L286](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L286) `public void turnTo( int from, int to ) {` — 개별 처리, 인접 호출: Math.max, GameScene.emitter
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L296) `public void jump( int from, int to, Callback callback ) {` — 개별 처리, 인접 호출: Math.max, GameScene.emitter
- [L301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L301) `public void jump( int from, int to, float height, float duration,  Callback callback ) {` — 개별 처리, 인접 호출: GameScene.emitter, Splash.at
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L311) `public void die() {` — 개별 처리, 인접 호출: GameScene.emitter, Splash.at, Math.min, Math.sqrt, PointF.angle
- [L323](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L323) `public Emitter emitter() {` — 개별 처리, 인접 호출: GameScene.emitter, Splash.at, Math.min, Math.sqrt, PointF.angle
- [L329](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L329) `public Emitter centerEmitter() {` — 개별 처리, 인접 호출: GameScene.emitter, Splash.at, Math.min, Math.sqrt, PointF.angle
- [L335](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L335) `public Emitter bottomEmitter() {` — 개별 처리, 인접 호출: GameScene.emitter, Splash.at, Math.min, Math.sqrt, PointF.angle
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L341) `public void burst( final int color, int n ) {` — 개별 처리, 인접 호출: Splash.at, Math.min, Math.sqrt, PointF.angle
- [L347](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L347) `public void bloodBurstA( PointF from, int damage ) {` — 개별 처리, 인접 호출: Math.min, Math.sqrt, Splash.at, PointF.angle
- [L355](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L355) `public int blood() {` — 개별 처리, 인접 호출: INSTANCE.play
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L359) `public void flash() {` — 개별 처리, 인접 호출: INSTANCE.play, Speck.factory
- [L366](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L366) `public void add( State state ) {` — 개별 처리, 인접 호출: INSTANCE.play, Speck.factory
- [L371](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L371) `synchronized (State.class) {` — 개별 처리, 인접 호출: INSTANCE.play, Speck.factory
- [L382](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L382) `public void aura( int color, int nRays ){` — 개별 처리, 인접 호출: INSTANCE.play, Speck.factory, IceBlock.freeze, GameScene.effect
- [L388](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L388) `protected synchronized void processStateAddition( State state ) {` — 행동·상태 갱신, 인접 호출: INSTANCE.play, Speck.factory, IceBlock.freeze, GameScene.effect, DarkBlock.darken
- [L472](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L472) `public void remove( State state ) {` — 개별 처리
- [L477](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L477) `synchronized (State.class) {` — 개별 처리
- [L484](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L484) `public void clearAura(){` — 개별 처리
- [L488](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L488) `protected synchronized void processStateRemoval( State state ) {` — 행동·상태 갱신
- [L575](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L575) `public void update() {` — 행동·상태 갱신
- [L587](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L587) `synchronized (State.class) {` — 개별 처리
- [L642](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L642) `synchronized (EmoIcon.class) {` — 개별 처리, 인접 호출: EmoIcon.Sleep, EmoIcon.Alert
- [L650](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L650) `public void resetColor() {` — 개별 처리, 인접 호출: EmoIcon.Sleep, EmoIcon.Alert
- [L657](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L657) `public void showSleep() {` — 개별 처리, 인접 호출: EmoIcon.Sleep, EmoIcon.Alert
- [L658](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L658) `synchronized (EmoIcon.class) {` — 개별 처리, 인접 호출: EmoIcon.Sleep, EmoIcon.Alert
- [L670](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L670) `public void hideSleep() {` — 개별 처리, 인접 호출: EmoIcon.Alert, EmoIcon.Investigate
- [L671](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L671) `synchronized (EmoIcon.class) {` — 개별 처리, 인접 호출: EmoIcon.Alert, EmoIcon.Investigate
- [L679](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L679) `public void showAlert() {` — 개별 처리, 인접 호출: EmoIcon.Alert, EmoIcon.Investigate
- [L680](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L680) `synchronized (EmoIcon.class) {` — 개별 처리, 인접 호출: EmoIcon.Alert, EmoIcon.Investigate
- [L691](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L691) `public void hideAlert() {` — 개별 처리, 인접 호출: EmoIcon.Investigate, EmoIcon.Lost
- [L692](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L692) `synchronized (EmoIcon.class) {` — 개별 처리, 인접 호출: EmoIcon.Investigate, EmoIcon.Lost
- [L700](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L700) `public void showInvestigate() {` — 개별 처리, 인접 호출: EmoIcon.Investigate, EmoIcon.Lost
- [L701](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L701) `synchronized (EmoIcon.class) {` — 개별 처리, 인접 호출: EmoIcon.Investigate, EmoIcon.Lost
- [L712](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L712) `public void hideInvestigate() {` — 개별 처리, 인접 호출: EmoIcon.Lost
- [L713](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L713) `synchronized (EmoIcon.class) {` — 개별 처리, 인접 호출: EmoIcon.Lost, State.values
- [L721](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L721) `public void showLost() {` — 개별 처리, 인접 호출: EmoIcon.Lost, State.values
- [L722](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L722) `synchronized (EmoIcon.class) {` — 개별 처리, 인접 호출: EmoIcon.Lost, State.values
- [L733](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L733) `public void hideLost() {` — 개별 처리, 인접 호출: State.values, Matrix.copy, Matrix.translate, Matrix.scale
- [L734](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L734) `synchronized (EmoIcon.class) {` — 개별 처리, 인접 호출: State.values, Matrix.copy, Matrix.translate, Matrix.scale
- [L742](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L742) `public void hideEmo(){` — 개별 처리, 인접 호출: State.values, Matrix.copy, Matrix.translate, Matrix.scale
- [L743](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L743) `synchronized (EmoIcon.class) {` — 개별 처리, 인접 호출: State.values, Matrix.copy, Matrix.translate, Matrix.scale
- [L752](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L752) `public void kill() {` — 개별 처리, 인접 호출: State.values, Matrix.copy, Matrix.translate, Matrix.scale
- [L769](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L769) `protected void updateMatrix() {` — 행동·상태 갱신, 인접 호출: Matrix.copy, Matrix.translate, Matrix.scale
- [L779](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L779) `public void draw() {` — 개별 처리, 인접 호출: GameScene.ripple
- [L815](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L815) `public void onComplete( Tweener tweener ) {` — 이벤트·효과 실행, 인접 호출: GameScene.ripple, GameScene.sortMobSprites
- [L828](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L828) `synchronized (this) {` — 개별 처리, 인접 호출: GameScene.sortMobSprites
- [L843](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L843) `public synchronized void onComplete( Animation anim ) {` — 이벤트·효과 실행
- [L875](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L875) `public JumpTweener( CharSprite visual, PointF pos, float height, float time ) {` — 개별 처리, 인접 호출: PointF.inter
- [L886](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L886) `protected void updateValues( float progress ) {` — 행동·상태 갱신, 인접 호출: PointF.inter

## 1003. [`CrabSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrabSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 56행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrabSprite.java#L27) `public class CrabSprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrabSprite.java#L29) `public CrabSprite() {` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrabSprite.java#L52) `public int blood() {` — 개별 처리

## 1004. [`CrystalGuardianSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 117행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L30) `public abstract class CrystalGuardianSprite extends MobSprite {`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L83) `public static class Blue extends CrystalGuardianSprite {`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L94) `public static class Green extends CrystalGuardianSprite {`
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L105) `public static class Red extends CrystalGuardianSprite {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L32) `private Animation crumple;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L34) `public CrystalGuardianSprite() {` — 개별 처리, 인접 호출: MovieClip.Animation
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L63) `public void crumple(){` — 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L67) `public void endCrumple(){` — 개별 처리
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L74) `public void link(Char ch) {` — 개별 처리
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L81) `protected abstract int texOffset();` — 개별 처리
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L85) `protected int texOffset() {` — 개별 처리
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L89) `public int blood() {` — 개별 처리
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L96) `protected int texOffset() {` — 개별 처리
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L100) `public int blood() {` — 개별 처리
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L107) `protected int texOffset() {` — 개별 처리
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalGuardianSprite.java#L111) `public int blood() {` — 개별 처리

## 1005. [`CrystalSpireSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 160행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L33) `public abstract class CrystalSpireSprite extends MobSprite {`
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L126) `public static class Blue extends CrystalSpireSprite {`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L137) `public static class Green extends CrystalSpireSprite {`
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L148) `public static class Red extends CrystalSpireSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L35) `public CrystalSpireSprite(){` — 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L55) `public void updateIdle(){` — 행동·상태 갱신
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L79) `public void link(Char ch) {` — 개별 처리, 인접 호출: GameScene.updateMap, Splash.around
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L87) `public void update() {` — 행동·상태 갱신, 인접 호출: GameScene.updateMap, Splash.around
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L108) `public void die() {` — 개별 처리, 인접 호출: Splash.around, GameScene.updateMap
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L120) `public void turnTo(int from, int to) {` — 개별 처리
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L124) `protected abstract int texOffset();` — 개별 처리
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L128) `protected int texOffset() {` — 개별 처리
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L132) `public int blood() {` — 개별 처리
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L139) `protected int texOffset() {` — 개별 처리
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L143) `public int blood() {` — 개별 처리
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L150) `protected int texOffset() {` — 개별 처리
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalSpireSprite.java#L154) `public int blood() {` — 개별 처리

## 1006. [`CrystalWispSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 204행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L37) `public abstract class CrystalWispSprite extends MobSprite {`
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L170) `public static class Blue extends CrystalWispSprite {`
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L181) `public static class Green extends CrystalWispSprite {`
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L192) `public static class Red extends CrystalWispSprite {`

### 변수·상수 후보
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L39) `private TorchHalo light;`
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L131) `private float baseY = Float.NaN;`

### 메서드 및 코드 의존 단서
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L41) `public CrystalWispSprite() {` — 개별 처리, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L67) `public void zap( int cell ) {` — 개별 처리, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play, GameScene.effect
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L73) `public void onComplete() {` — 이벤트·효과 실행, 인접 호출: Beam.LightRay, DungeonTilemap.raisedTileCenterToWorld, INSTANCE.play, GameScene.effect
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L86) `public synchronized void attack(int cell) {` — 전투 관련, 인접 호출: GameScene.effect
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L90) `public void onComplete() {` — 이벤트·효과 실행, 인접 호출: GameScene.effect
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L97) `public void link(Char ch) {` — 개별 처리, 인접 호출: GameScene.effect
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L108) `public void die() {` — 개별 처리, 인접 호출: Float.isNaN, Math.abs, Math.sin
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L116) `public void kill() {` — 개별 처리, 인접 호출: Float.isNaN, Math.abs, Math.sin
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L124) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행, 인접 호출: Float.isNaN, Math.abs, Math.sin
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L134) `public void place(int cell) {` — 개별 처리, 인접 호출: Float.isNaN, Math.abs, Math.sin
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L140) `public PointF point(PointF p) {` — 개별 처리, 인접 호출: Float.isNaN, Math.abs, Math.sin
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L147) `public void update() {` — 행동·상태 갱신, 인접 호출: Float.isNaN, Math.abs, Math.sin
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L164) `public void turnTo(int from, int to) {` — 개별 처리
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L168) `protected abstract int texOffset();` — 개별 처리
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L172) `protected int texOffset() {` — 개별 처리
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L176) `public int blood() {` — 개별 처리
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L183) `protected int texOffset() {` — 개별 처리
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L187) `public int blood() {` — 개별 처리
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L194) `protected int texOffset() {` — 개별 처리
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CrystalWispSprite.java#L198) `public int blood() {` — 개별 처리

## 1007. [`DiscardedItemSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DiscardedItemSprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 51행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DiscardedItemSprite.java#L27) `public class DiscardedItemSprite extends ItemSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DiscardedItemSprite.java#L30) `public void drop() {` — 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DiscardedItemSprite.java#L40) `public void update() {` — 행동·상태 갱신

## 1008. [`DM100Sprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM100Sprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 133행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM100Sprite.java#L34) `public class DM100Sprite extends MobSprite {`
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM100Sprite.java#L124) `public static class Vault extends DM100Sprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM100Sprite.java#L36) `public DM100Sprite () {` — 개별 처리, 인접 호출: Actor.findChar
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM100Sprite.java#L63) `protected int texOffset() {` — 개별 처리, 인접 호출: Actor.findChar, INSTANCE.play, Speck.factory
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM100Sprite.java#L67) `public void zap( int pos ) {` — 개별 처리, 인접 호출: Actor.findChar, INSTANCE.play, Speck.factory
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM100Sprite.java#L85) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play, Speck.factory
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM100Sprite.java#L94) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play, Speck.factory
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM100Sprite.java#L106) `public void die() {` — 개별 처리, 인접 호출: Speck.factory
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM100Sprite.java#L112) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM100Sprite.java#L120) `public int blood() {` — 개별 처리
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM100Sprite.java#L127) `protected int texOffset() {` — 개별 처리

## 1009. [`DM200Sprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM200Sprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 119행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM200Sprite.java#L34) `public class DM200Sprite extends MobSprite {`
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM200Sprite.java#L110) `public static class Vault extends DM200Sprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM200Sprite.java#L36) `public DM200Sprite () {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM200Sprite.java#L63) `protected int texOffset(){` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play, GLog.w, Messages.get, Speck.factory
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM200Sprite.java#L67) `public void zap( int cell ) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play, GLog.w, Messages.get, Speck.factory
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM200Sprite.java#L77) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play, GLog.w, Messages.get, Speck.factory
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM200Sprite.java#L86) `public void place(int cell) {` — 개별 처리, 인접 호출: Speck.factory
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM200Sprite.java#L92) `public void die() {` — 개별 처리, 인접 호출: Speck.factory
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM200Sprite.java#L98) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM200Sprite.java#L106) `public int blood() {` — 개별 처리
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM200Sprite.java#L113) `protected int texOffset() {` — 개별 처리

## 1010. [`DM201Sprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM201Sprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 107행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM201Sprite.java#L34) `public class DM201Sprite extends MobSprite {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM201Sprite.java#L36) `public DM201Sprite () {` — 개별 처리, 인접 호출: Speck.factory, MagicMissile.boltFromChar
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM201Sprite.java#L63) `public void place(int cell) {` — 개별 처리, 인접 호출: Speck.factory, MagicMissile.boltFromChar, INSTANCE.play, GLog.w, Messages.get
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM201Sprite.java#L69) `public void die() {` — 개별 처리, 인접 호출: Speck.factory, MagicMissile.boltFromChar, INSTANCE.play, GLog.w, Messages.get
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM201Sprite.java#L74) `public void zap( int cell ) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play, GLog.w, Messages.get
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM201Sprite.java#L84) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play, GLog.w, Messages.get
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM201Sprite.java#L94) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM201Sprite.java#L102) `public int blood() {` — 개별 처리

## 1011. [`DM300Sprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.sprites`, 184행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L37) `public class DM300Sprite extends MobSprite {`

### 변수·상수 후보
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L39) `private Animation charge;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L40) `private Animation slam;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L42) `private Emitter superchargeSparks;`

### 메서드 및 코드 의존 단서
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L44) `public DM300Sprite() {` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L52) `public void updateChargeState( boolean enraged ){` — 행동·상태 갱신, 인접 호출: MagicMissile.boltFromChar
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L86) `public void zap( int cell ) {` — 개별 처리, 인접 호출: MagicMissile.boltFromChar, INSTANCE.play, PixelScene.shake
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L96) `public void call() {` — 개별 처리, 인접 호출: INSTANCE.play, PixelScene.shake
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L103) `public void charge(){` — 개별 처리, 인접 호출: INSTANCE.play, PixelScene.shake
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L107) `public void slam( int cell ){` — 개별 처리, 인접 호출: INSTANCE.play, PixelScene.shake
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L115) `public void onComplete( Animation anim ) {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L135) `public void place(int cell) {` — 개별 처리
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L141) `public void link(Char ch) {` — 개별 처리
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L155) `public void update() {` — 행동·상태 갱신
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L164) `public void die() {` — 개별 처리
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L172) `public void kill() {` — 개별 처리
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DM300Sprite.java#L180) `public int blood() {` — 개별 처리


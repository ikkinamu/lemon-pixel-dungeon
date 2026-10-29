# Java 소스 구현 분석 1102–1119

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1102. [`Banner.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 108행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java#L27) `public class Banner extends Image {`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java#L29) `private enum State {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java#L32) `private State state;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java#L34) `private float time;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java#L36) `private int color;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java#L37) `private float fadeTime;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java#L38) `private float showTime;`

### 메서드 및 코드 의존 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java#L40) `public Banner( Image sample ) {` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java#L46) `public Banner( Object tx ) {` — 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java#L51) `public void show( int color, float fadeTime, float showTime ) {` — 개별 처리
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java#L62) `public void show( int color, float fadeTime ) {` — 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java#L67) `public void update() {` — 행동·상태 갱신

## 1103. [`BossHealthBar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 297행.

### 클래스/타입
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L39) `public class BossHealthBar extends Component {`

### 변수·상수 후보
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L41) `private Image bar;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L43) `private Image shieldHP;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L44) `private Image hp;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L46) `private BitmapText hpText;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L48) `private Button bossInfo;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L49) `private BuffIndicator buffs;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L51) `private static Mob boss;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L53) `private Image skull;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L54) `private Emitter blood;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L56) `private static String asset = Assets.Interfaces.BOSSHP;`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L58) `private static BossHealthBar instance;`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L59) `private static boolean bleeding;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L61) `private boolean large;`

### 메서드 및 코드 의존 단서
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L63) `public BossHealthBar() {` — 개별 처리, 인접 호출: BuffIndicator.setBossInstance, SPDSettings.interfaceSize, Dot.hardlight, Dot.alpha, GameScene.show
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L70) `public synchronized void destroy() {` — 개별 처리, 인접 호출: BuffIndicator.setBossInstance, SPDSettings.interfaceSize, Dot.hardlight, Dot.alpha, GameScene.show
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L77) `protected void createChildren() {` — 생성·초기화, 인접 호출: SPDSettings.interfaceSize, Dot.hardlight, Dot.alpha, GameScene.show
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L103) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, BuffIndicator.setBossInstance
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L111) `protected String hoverText() {` — 개별 처리, 인접 호출: BuffIndicator.setBossInstance, PixelScene.align
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L142) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, Math.max, BuffIndicator.setBossInstance
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L178) `public void update() {` — 행동·상태 갱신, 인접 호출: BuffIndicator.setBossInstance, Math.min, Dot.width
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L233) `public static void assignBoss(Mob boss){` — 개별 처리, 인접 호출: ShatteredPixelDungeon.runOnRenderThread, BuffIndicator.setBossInstance
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L237) `public static void assignBoss(Mob boss, boolean forceSpriteRefresh){` — 개별 처리, 인접 호출: ShatteredPixelDungeon.runOnRenderThread, BuffIndicator.setBossInstance
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L243) `public void call() {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.runOnRenderThread, BuffIndicator.setBossInstance
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L259) `public void call() {` — 개별 처리, 인접 호출: BuffIndicator.setBossInstance
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L284) `public static boolean isAssigned(){` — 조회·판정
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L288) `public static void bleed(boolean value){` — 개별 처리
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java#L292) `public static boolean isBleeding(){` — 조회·판정

## 1104. [`BuffIcon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIcon.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 67행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIcon.java#L29) `public class BuffIcon extends Image {`

### 변수·상수 후보
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIcon.java#L31) `private static TextureFilm smallFilm;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIcon.java#L32) `private static final int SML_SIZE = 7;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIcon.java#L34) `private static TextureFilm largeFilm;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIcon.java#L35) `private static final int LRG_SIZE = 16;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIcon.java#L37) `private final boolean large;`

### 메서드 및 코드 의존 단서
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIcon.java#L39) `public BuffIcon(Buff buff, boolean large){` — 개별 처리
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIcon.java#L45) `public BuffIcon(int icon, boolean large){` — 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIcon.java#L51) `public void refresh(Buff buff){` — 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIcon.java#L56) `public void refresh(int icon){` — 개별 처리

## 1105. [`BuffIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 422행.

### 클래스/타입
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L46) `public class BuffIndicator extends Component {`
- [L315](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L315) `private static class BuffButton extends IconButton {`

### 변수·상수 후보
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L49) `public static final int NONE    = 127;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L53) `public static final int MIND_VISION = 0;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L54) `public static final int LEVITATION  = 1;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L55) `public static final int FIRE        = 2;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L56) `public static final int POISON      = 3;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L57) `public static final int PARALYSIS   = 4;`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L58) `public static final int HUNGER      = 5;`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L59) `public static final int STARVATION  = 6;`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L60) `public static final int TIME        = 7;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L61) `public static final int OOZE        = 8;`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L62) `public static final int AMOK        = 9;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L63) `public static final int TERROR      = 10;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L64) `public static final int ROOTS       = 11;`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L65) `public static final int INVISIBLE   = 12;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L66) `public static final int SHADOWS     = 13;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L67) `public static final int WEAKNESS    = 14;`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L68) `public static final int FROST       = 15;`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L69) `public static final int BLINDNESS   = 16;`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L70) `public static final int COMBO       = 17;`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L71) `public static final int FURY        = 18;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L72) `public static final int HERB_HEALING= 19;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L73) `public static final int ARMOR       = 20;`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L74) `public static final int HEART       = 21;`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L75) `public static final int LIGHT       = 22;`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L76) `public static final int CRIPPLE     = 23;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L77) `public static final int BARKSKIN    = 24;`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L78) `public static final int IMMUNITY    = 25;`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L79) `public static final int BLEEDING    = 26;`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L80) `public static final int MARK        = 27;`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L81) `public static final int DEFERRED    = 28;`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L82) `public static final int DROWSY      = 29;`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L83) `public static final int MAGIC_SLEEP = 30;`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L84) `public static final int THORNS      = 31;`
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L85) `public static final int FORESIGHT   = 32;`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L86) `public static final int VERTIGO     = 33;`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L87) `public static final int RECHARGING  = 34;`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L88) `public static final int LOCKED_FLOOR= 35;`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L89) `public static final int CORRUPT     = 36;`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L90) `public static final int BLESS       = 37;`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L91) `public static final int RAGE        = 38;`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L92) `public static final int SACRIFICE   = 39;`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L93) `public static final int BERSERK     = 40;`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L94) `public static final int HASTE       = 41;`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L95) `public static final int PREPARATION = 42;`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L96) `public static final int WELL_FED    = 43;`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L97) `public static final int HEALING     = 44;`
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L98) `public static final int WEAPON      = 45;`
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L99) `public static final int VULNERABLE  = 46;`
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L100) `public static final int HEX         = 47;`
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L101) `public static final int DEGRADE     = 48;`
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L102) `public static final int PINCUSHION  = 49;`
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L103) `public static final int UPGRADE     = 50;`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L104) `public static final int MOMENTUM    = 51;`
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L105) `public static final int ANKH        = 52;`
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L106) `public static final int NOINV       = 53;`
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L107) `public static final int TARGETED    = 54;`
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L108) `public static final int IMBUE       = 55;`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L109) `public static final int ENDURE      = 56;`
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L110) `public static final int INVERT_MARK = 57;`
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L111) `public static final int NATURE_POWER= 58;`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L112) `public static final int AMULET      = 59;`
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L113) `public static final int DUEL_CLEAVE = 60;`
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L114) `public static final int DUEL_GUARD  = 61;`
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L115) `public static final int DUEL_SPIN   = 62;`
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L116) `public static final int DUEL_EVASIVE= 63;`
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L117) `public static final int DUEL_DANCE  = 64;`
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L118) `public static final int DUEL_BRAWL  = 65;`
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L119) `public static final int DUEL_XBOW   = 66;`
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L120) `public static final int CHALLENGE   = 67;`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L121) `public static final int MONK_ENERGY = 68;`
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L122) `public static final int DUEL_COMBO  = 69;`
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L123) `public static final int DAZE        = 70;`
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L124) `public static final int DISGUISE    = 71;`
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L125) `public static final int WAND        = 72;`
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L126) `public static final int HOLY_WEAPON = 73;`
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L127) `public static final int HOLY_ARMOR  = 74;`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L128) `public static final int SPELL_FOOD  = 75;`
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L129) `public static final int LIGHT_SHIELD= 76;`
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L130) `public static final int HOLY_SIGHT  = 77;`
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L131) `public static final int GLYPH_RECALL= 78;`
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L132) `public static final int ASCEND      = 79;`
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L133) `public static final int PROT_AURA   = 80;`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L134) `public static final int ILLUMINATED = 81;`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L135) `public static final int TRINITY_FORM= 82;`
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L136) `public static final int MANY_POWER  = 83;`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L137) `public static final int SEAL_SHIELD = 84;`
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L138) `public static final int THROWN_WEP  = 85;`
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L140) `public static final int SIZE_SMALL  = 7;`
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L141) `public static final int SIZE_LARGE  = 16;`
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L143) `private static BuffIndicator heroInstance;`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L144) `private static BuffIndicator bossInstance;`
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L147) `private boolean needsRefresh;`
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L148) `private Char ch;`
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L150) `private boolean large = false;`
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L185) `private boolean buffsHidden = false;`
- [L317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L317) `private Buff buff;`
- [L319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L319) `private boolean large;`
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L320) `private int topOffset = 0;`

### 메서드 및 코드 의존 단서
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L157) `public BuffIndicator( Char ch, boolean large ) {` — 개별 처리
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L168) `public void destroy() {` — 개별 처리
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L177) `public synchronized void update() {` — 행동·상태 갱신
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L189) `protected void layout() {` — 개별 처리
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L209) `protected void updateValues( float progress ) {` — 행동·상태 갱신, 인접 호출: PixelScene.align
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L215) `protected void onComplete() {` — 이벤트·효과 실행, 인접 호출: PixelScene.align
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L311) `public boolean allBuffsVisible(){` — 개별 처리, 인접 호출: TextureCache.createSolid, GameMath.gate, Math.ceil, Math.floor
- [L325](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L325) `public BuffButton( Buff buff, boolean large ){` — 개별 처리, 인접 호출: TextureCache.createSolid, GameMath.gate, Math.ceil, Math.floor
- [L335](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L335) `protected void createChildren() {` — 생성·초기화, 인접 호출: TextureCache.createSolid, GameMath.gate, Math.ceil, Math.floor, PixelScene.align
- [L344](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L344) `public void updateIcon(){` — 행동·상태 갱신, 인접 호출: GameMath.gate, Math.ceil, Math.floor, PixelScene.align, GameScene.show
- [L370](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L370) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, GameScene.show, INSTANCE.play, Messages.titleCase
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L385) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.show, INSTANCE.play, Messages.titleCase
- [L390](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L390) `protected void onPointerDown() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, Messages.titleCase
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L396) `protected void onPointerUp() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase
- [L401](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L401) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase
- [L406](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L406) `public static void refreshHero() {` — 개별 처리
- [L412](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L412) `public static void refreshBoss(){` — 개별 처리
- [L418](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java#L418) `public static void setBossInstance(BuffIndicator boss){` — 개별 처리

## 1106. [`BusyIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BusyIndicator.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 43행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BusyIndicator.java#L27) `public class BusyIndicator extends Image {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BusyIndicator.java#L29) `public BusyIndicator() {` — 개별 처리, 인접 호출: BUSY.get
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BusyIndicator.java#L38) `public void update() {` — 행동·상태 갱신

## 1107. [`Button.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 231행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L37) `public class Button extends Component {`

### 변수·상수 후보
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L39) `public static float longClick = 0.5f;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L41) `protected PointerArea hotArea;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L42) `protected Tooltip hoverTip;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L45) `protected static Button pressedButton;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L46) `protected float pressTime;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L47) `protected boolean clickReady;`
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L145) `private Signal.Listener<KeyEvent> keyListener;`

### 메서드 및 코드 의존 단서
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L50) `protected void createChildren() {` — 생성·초기화, 인접 호출: KeyBindings.getFirstKeyForAction
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L53) `protected void onPointerDown( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getFirstKeyForAction
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L60) `protected void onPointerUp( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getFirstKeyForAction, KeyBindings.getKeyName
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L70) `protected void onClick( PointerEvent event ) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getFirstKeyForAction, KeyBindings.getKeyName
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L89) `protected void onHoverStart(PointerEvent event) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getFirstKeyForAction, KeyBindings.getKeyName, KeyEvent.addKeyListener, KeyBindings.getActionForKey
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L116) `protected void onHoverEnd(PointerEvent event) {` — 이벤트·효과 실행, 인접 호출: KeyEvent.addKeyListener, KeyBindings.getActionForKey
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L124) `public boolean onSignal ( KeyEvent event ) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getActionForKey
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L147) `public GameAction keyAction(){` — 개별 처리, 인접 호출: SPDSettings.vibration, Game.vibrate
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L152) `public GameAction secondaryTooltipAction(){` — 개별 처리, 인접 호출: SPDSettings.vibration, Game.vibrate
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L157) `public void update() {` — 행동·상태 갱신, 인접 호출: SPDSettings.vibration, Game.vibrate
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L177) `protected void onPointerDown() {}` — 이벤트·효과 실행
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L178) `protected void onPointerUp() {}` — 이벤트·효과 실행, 인접 호출: KeyEvent.removeKeyListener
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L179) `protected void onClick() {} //left click, default key type` — 이벤트·효과 실행, 인접 호출: KeyEvent.removeKeyListener
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L180) `protected void onRightClick() {}` — 이벤트·효과 실행, 인접 호출: KeyEvent.removeKeyListener
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L181) `protected void onMiddleClick() {}` — 이벤트·효과 실행, 인접 호출: KeyEvent.removeKeyListener
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L182) `protected boolean onLongClick() {` — 이벤트·효과 실행, 인접 호출: KeyEvent.removeKeyListener
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L186) `protected String hoverText() {` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L191) `private void alignTooltip( Tooltip tip ){` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L204) `public void killTooltip(){` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L212) `protected void layout() {` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L220) `public synchronized void destroy () {` — 개별 처리, 인접 호출: KeyEvent.removeKeyListener
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java#L226) `public void givePointerPriority(){` — 개별 처리

## 1108. [`ChangeButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeButton.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 68행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeButton.java#L33) `public class ChangeButton extends Component {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeButton.java#L35) `protected Image icon;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeButton.java#L36) `protected String title;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeButton.java#L37) `protected String[] messages;`

### 메서드 및 코드 의존 단서
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeButton.java#L39) `public ChangeButton(ChangeIcons icon, String title, String... message){` — 개별 처리, 인접 호출: Messages.titleCase, ChangesScene.showChangeInfo, PixelScene.align
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeButton.java#L43) `public ChangeButton( Image icon, String title, String... messages){` — 개별 처리, 인접 호출: Messages.titleCase, ChangesScene.showChangeInfo, PixelScene.align
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeButton.java#L55) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ChangesScene.showChangeInfo, PixelScene.align
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeButton.java#L60) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align

## 1109. [`ChangeIcons.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeIcons.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 389행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeIcons.java#L28) `public enum ChangeIcons {`

### 변수·상수 후보
- [L364](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeIcons.java#L364) `private static int texW = 128/16;`

### 메서드 및 코드 의존 단서
- [L376](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeIcons.java#L376) `public Image get(){` — 조회·판정
- [L380](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeIcons.java#L380) `public static Image get( ChangeIcons type ) {` — 조회·판정

## 1110. [`ChangeInfo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeInfo.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 155행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeInfo.java#L31) `public class ChangeInfo extends Component {`

### 변수·상수 후보
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeInfo.java#L33) `protected ColorBlock line;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeInfo.java#L35) `private RenderedTextBlock title;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeInfo.java#L36) `public boolean major;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeInfo.java#L38) `private RenderedTextBlock text;`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeInfo.java#L42) `public ChangeInfo( String title, boolean majorTitle, String text){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeInfo.java#L65) `public void hardlight( int color ){` — 개별 처리, 인접 호출: PixelScene.align
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeInfo.java#L72) `public void addButton( ChangeButton button ){` — 개별 처리, 인접 호출: PixelScene.align
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeInfo.java#L80) `public boolean onClick( float x, float y ){` — 이벤트·효과 실행, 인접 호출: PixelScene.align
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/ChangeInfo.java#L91) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align

## 1111. [`Pixel_Dungeon_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/Pixel_Dungeon_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 618행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/Pixel_Dungeon_Changes.java#L28) `public class Pixel_Dungeon_Changes {`
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/Pixel_Dungeon_Changes.java#L289) `"Ok, Pixel Dungeon 0.5.3 is released. There is one more class now, it’s a Huntress! This character class is unlockable, you need to slain DM-300 to un`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/Pixel_Dungeon_Changes.java#L31) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/Pixel_Dungeon_Changes.java#L35) `public static void add_PD_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리

## 1112. [`v0_1_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_1_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 115행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_1_X_Changes.java#L28) `public class v0_1_X_Changes {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_1_X_Changes.java#L30) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_1_X_Changes.java#L40) `public static void add_v0_1_1_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_1_X_Changes.java#L81) `public static void add_v0_1_0_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리

## 1113. [`v0_2_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_2_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 256행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_2_X_Changes.java#L30) `public class v0_2_X_Changes {`
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_2_X_Changes.java#L216) `"Artifacts came from realizing it would be very difficult to make some rings worth upgrading by just buffing them. Instead, I decided to put their mec`
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_2_X_Changes.java#L220) `"Giving the Cloak of Shadows to the Rogue was also my first attempt at a class rework. It was a much more simple change than later reworks, and I ende`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_2_X_Changes.java#L32) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_2_X_Changes.java#L49) `public static void add_v0_2_4_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_2_X_Changes.java#L90) `public static void add_v0_2_3_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_2_X_Changes.java#L131) `public static void add_v0_2_2_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_2_X_Changes.java#L177) `public static void add_v0_2_1_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_2_X_Changes.java#L204) `public static void add_v0_2_0_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get

## 1114. [`v0_3_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 339행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java#L30) `public class v0_3_X_Changes {`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java#L55) `"v0.3.5 introduced the second proper class rework, this time to the Warrior! I tried to shift the warrior's powers away from a raw stat increase into `
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java#L236) `"Still, v0.3.1 wasn't all bad. Traps in the earlygame were improved, and it also introduced some very important interface changes such as four quicksl`
- [L281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java#L281) `"v0.3.0 was Shattered's second major item category rework, and Shattered's first real class rework!\n" +`
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java#L283) `"This class rework also included changes to the Mage's subclasses. While other aspects of the Mage have changed a bunch since the rework, the core ide`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java#L32) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java#L46) `public static void add_v0_3_5_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java#L90) `public static void add_v0_3_4_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java#L132) `public static void add_v0_3_3_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java#L168) `public static void add_v0_3_2_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java#L223) `public static void add_v0_3_1_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_3_X_Changes.java#L271) `public static void add_v0_3_0_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get

## 1115. [`v0_4_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_4_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 242행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_4_X_Changes.java#L30) `public class v0_4_X_Changes {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_4_X_Changes.java#L32) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_4_X_Changes.java#L44) `public static void add_v0_4_3_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_4_X_Changes.java#L75) `public static void add_v0_4_2_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_4_X_Changes.java#L109) `public static void add_v0_4_1_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_4_X_Changes.java#L178) `public static void add_v0_4_0_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리

## 1116. [`v0_5_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_5_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 74행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_5_X_Changes.java#L30) `public class v0_5_X_Changes {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_5_X_Changes.java#L33) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_5_X_Changes.java#L37) `public static void add_v0_5_0_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get

## 1117. [`v0_6_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 879행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L31) `public class v0_6_X_Changes {`
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L164) `"Eventually I want to totally overhaul class armors. In the meantime though, two of the armors are disproportionately powerful with mind vision, and n`
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L200) `"The interface for starting and loading a game has been completely overhauled!\n" +`
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L341) `"Huntress adjusted due to ranged weapon changes (note that this is not a full class rework):\n\n" +`
- [L353](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L353) `"_-_ Alchemy interface now features a recipes button to show you what you can create."));`
- [L562](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L562) `"_-_ Added a new interface and graphics for alchemy.\n" +`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L33) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L42) `public static void add_v0_6_5_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L169) `public static void add_v0_6_4_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L313](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L313) `public static void add_v0_6_3_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L462](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L462) `public static void add_v0_6_2_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L649](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L649) `public static void add_v0_6_1_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L822](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_6_X_Changes.java#L822) `public static void add_v0_6_0_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리

## 1118. [`v0_7_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_7_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 903행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_7_X_Changes.java#L31) `public class v0_7_X_Changes {`
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_7_X_Changes.java#L202) `"_-_ Overhauled main menu interface to allow for more expandability.\n" +`
- [L594](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_7_X_Changes.java#L594) `"The Huntress has received a class overhaul!\n\n" +`
- [L837](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_7_X_Changes.java#L837) `"_-_ 'Faith is my armor' deleting class armors\n" +`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_7_X_Changes.java#L33) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_7_X_Changes.java#L42) `public static void add_v0_7_5_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_7_X_Changes.java#L159) `public static void add_v0_7_4_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_7_X_Changes.java#L289) `public static void add_v0_7_3_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L421](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_7_X_Changes.java#L421) `public static void add_v0_7_2_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L576](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_7_X_Changes.java#L576) `public static void add_v0_7_1_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L710](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_7_X_Changes.java#L710) `public static void add_v0_7_0_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get

## 1119. [`v0_8_X_Changes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_8_X_Changes.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui.changelist`, 685행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_8_X_Changes.java#L31) `public class v0_8_X_Changes {`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_8_X_Changes.java#L80) `"_-_ The supporter interface now has its own dedicated scene and improved visuals\n\n" +`
- [L452](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_8_X_Changes.java#L452) `"These changes also heavily influenced item and class balance. Offense and defense became more fairly balanced, as many enemies gained mechanics that `
- [L529](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_8_X_Changes.java#L529) `"While I intend to make larger changes in a future update, I've decided to do some targeted improvements to class armors now to make the abilities mor`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_8_X_Changes.java#L33) `public static void addAllChanges( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_8_X_Changes.java#L39) `public static void add_v0_8_2_Changes( ArrayList<ChangeInfo> changeInfos ) {` — 개별 처리, 인접 호출: Messages.get
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_8_X_Changes.java#L225) `public static void add_v0_8_1_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get
- [L436](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/changelist/v0_8_X_Changes.java#L436) `public static void add_v0_8_0_Changes( ArrayList<ChangeInfo> changeInfos ){` — 개별 처리, 인접 호출: Messages.get


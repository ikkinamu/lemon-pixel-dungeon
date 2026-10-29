# Java 소스 구현 분석 1264–1281

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1264. [`PointerEvent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java)

패키지 `com.watabou.input`, 198행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L33) `public class PointerEvent {`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L35) `public enum Type {`

### 변수·상수 후보
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L43) `public static final int NONE = -1;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L44) `public static final int LEFT = Input.Buttons.LEFT;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L45) `public static final int RIGHT = Input.Buttons.RIGHT;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L46) `public static final int MIDDLE = Input.Buttons.MIDDLE;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L50) `public PointF start;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L51) `public PointF current;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L52) `public int id;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L53) `public Type type;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L54) `public int button;`
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L142) `public static boolean clearKeyboardThisPress = true;`

### 메서드 및 코드 의존 단서
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L57) `public PointerEvent( int x, int y, int id, Type type){` — 개별 처리, 인접 호출: Cursor.isCursorCaptured
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L61) `public PointerEvent( int x, int y, int id, Type type, int button){` — 개별 처리, 인접 호출: Cursor.isCursorCaptured
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L73) `public void update( PointerEvent other ){` — 행동·상태 갱신
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L77) `public void update( int x, int y ){` — 행동·상태 갱신
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L81) `public PointerEvent up() {` — 개별 처리
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L86) `public PointerEvent cancel() {` — 조회·판정
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L91) `public PointerEvent handle(){` — 개별 처리
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L102) `public static void addPointerListener( Signal.Listener<PointerEvent> listener ){` — 개별 처리
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L106) `public static void removePointerListener( Signal.Listener<PointerEvent> listener ){` — 개별 처리
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L110) `public static void clearListeners(){` — 개별 처리
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L118) `private static PointF lastHoverPos = new PointF();` — 개별 처리
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L120) `public static PointF currentHoverPos(){` — 개별 처리
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L128) `public static void setHoverPos(PointF pos){` — 개별 처리
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L132) `public static synchronized void addPointerEvent( PointerEvent event ){` — 개별 처리
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L136) `public static synchronized void addIfExisting( PointerEvent event ){` — 개별 처리
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java#L144) `public static synchronized void processPointerEvents(){` — 행동·상태 갱신

## 1265. [`ScrollEvent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ScrollEvent.java)

패키지 `com.watabou.input`, 76행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ScrollEvent.java#L29) `public class ScrollEvent {`

### 변수·상수 후보
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ScrollEvent.java#L31) `public PointF pos;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ScrollEvent.java#L32) `public float amount;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ScrollEvent.java#L34) `public ScrollEvent(PointF mousePos, float amount){` — 개별 처리
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ScrollEvent.java#L45) `public static void addScrollListener( Signal.Listener<ScrollEvent> listener ){` — 개별 처리
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ScrollEvent.java#L49) `public static void removeScrollListener( Signal.Listener<ScrollEvent> listener ){` — 개별 처리
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ScrollEvent.java#L53) `public static void clearListeners(){` — 개별 처리
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ScrollEvent.java#L60) `public static synchronized void addScrollEvent( ScrollEvent event ){` — 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ScrollEvent.java#L64) `public static synchronized void processScrollEvents(){` — 행동·상태 갱신

## 1266. [`Music.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java)

패키지 `com.watabou.noosa.audio`, 331행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L34) `public enum Music {`

### 변수·상수 후보
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L38) `private com.badlogic.gdx.audio.Music player;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L40) `private String lastPlayed;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L41) `private boolean looping;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L43) `private boolean enabled = true;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L44) `private float volume = 1f;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L46) `private float fadeTime = -1f;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L47) `private float fadeTotal = -1f;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L48) `private Callback onFadeOut = null;`
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L244) `private boolean paused = false;`

### 메서드 및 코드 의존 단서
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L56) `public synchronized void play( String assetName, boolean looping ) {` — 개별 처리, 인접 호출: DeviceCompat.isiOS
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L86) `public synchronized void playTracks( String[] tracks, float[] chances, boolean shuffle){` — 개별 처리, 인접 호출: DeviceCompat.isiOS
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L158) `public synchronized void fadeOut(float duration, Callback onComplete){` — 개별 처리, 인접 호출: Music.OnCompletionListener
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L169) `public synchronized void update(){` — 행동·상태 갱신, 인접 호출: Music.OnCompletionListener, Random.Float, Collections.shuffle
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L186) `private com.badlogic.gdx.audio.Music.OnCompletionListener trackLooper = new com.badlogic.gdx.audio.Music.OnCompletionListener() {` — 개별 처리, 인접 호출: Random.Float, Collections.shuffle
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L188) `public void onCompletion(com.badlogic.gdx.audio.Music music) {` — 이벤트·효과 실행, 인접 호출: Random.Float, Collections.shuffle
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L196) `private synchronized void playNextTrack(com.badlogic.gdx.audio.Music music){` — 개별 처리, 인접 호출: Random.Float, Collections.shuffle, Game.reportException
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L219) `private synchronized void play(String track, com.badlogic.gdx.audio.Music.OnCompletionListener listener){` — 개별 처리, 인접 호출: Game.reportException
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L238) `public synchronized void end() {` — 개별 처리
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L246) `public synchronized boolean paused(){` — 개별 처리
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L250) `public synchronized void pause() {` — 개별 처리
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L257) `public synchronized void resume() {` — 개별 처리
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L265) `public synchronized void stop() {` — 개별 처리, 인접 호출: Math.max
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L272) `public synchronized void reset() {` — 개별 처리, 인접 호출: Math.max
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L283) `private com.badlogic.gdx.audio.Music createPlayer(String asset){` — 생성·초기화, 인접 호출: Math.max
- [L293](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L293) `public synchronized void volume( float value ) {` — 개별 처리, 인접 호출: Math.max
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L300) `private synchronized float volumeWithFade(){` — 개별 처리, 인접 호출: Math.max
- [L308](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L308) `public synchronized boolean isPlaying() {` — 조회·판정
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L312) `public synchronized void enable( boolean value ) {` — 개별 처리
- [L326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java#L326) `public synchronized boolean isEnabled() {` — 조회·판정

## 1267. [`Sample.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java)

패키지 `com.watabou.noosa.audio`, 188행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L32) `public enum Sample {`
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L118) `private class DelayedSoundEffect{`

### 변수·상수 후보
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L38) `private boolean enabled = true;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L39) `private float globalVolume = 1f;`

### 메서드 및 코드 의존 단서
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L41) `public synchronized void reset() {` — 개별 처리, 인접 호출: Game.reportException
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L52) `public synchronized void pause() {` — 개별 처리, 인접 호출: Game.reportException
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L58) `public synchronized void resume() {` — 개별 처리, 인접 호출: Game.reportException
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L64) `public synchronized void load( final String asset){` — 저장·복원, 인접 호출: Game.reportException
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L79) `public void load( final String[] assets ) {` — 저장·복원, 인접 호출: Math.max
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L80) `synchronized (loadingQueue) {` — 개별 처리, 인접 호출: Math.max
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L89) `public synchronized void unload( Object src ) {` — 개별 처리, 인접 호출: Math.max
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L96) `public long play( Object id ) {` — 개별 처리, 인접 호출: Math.max
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L100) `public long play( Object id, float volume ) {` — 개별 처리, 인접 호출: Math.max
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L104) `public long play( Object id, float volume, float pitch ) {` — 개별 처리, 인접 호출: Math.max
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L108) `public synchronized long play( Object id, float leftVolume, float rightVolume, float pitch ) {` — 개별 처리, 인접 호출: Math.max
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L129) `public void playDelayed( Object id, float delay ){` — 개별 처리
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L133) `public void playDelayed( Object id, float delay, float volume ) {` — 개별 처리
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L137) `public void playDelayed( Object id, float delay, float volume, float pitch ) {` — 개별 처리
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L141) `public void playDelayed( Object id, float delay, float leftVolume, float rightVolume, float pitch ) {` — 개별 처리
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L152) `synchronized (delayedSFX) {` — 개별 처리
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L157) `public void update(){` — 행동·상태 갱신
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L158) `synchronized (loadingQueue) {` — 개별 처리
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L164) `synchronized (delayedSFX) {` — 개별 처리
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L176) `public void enable( boolean value ) {` — 개별 처리
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L180) `public void volume( float value ) {` — 개별 처리
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java#L184) `public boolean isEnabled() {` — 조회·판정

## 1268. [`BitmapText.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java)

패키지 `com.watabou.noosa`, 368행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L34) `public class BitmapText extends Visual {`
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L219) `public static class Font extends TextureFilm {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L36) `protected String text;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L37) `protected Font font;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L39) `protected float[] vertices = new float[16];`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L40) `protected FloatBuffer quads;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L41) `protected Vertexbuffer buffer;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L43) `public int realLength;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L45) `protected boolean dirty = true;`
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L224) `public SmartTexture texture;`
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L226) `public float tracking = 0;`
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L227) `public float baseLine;`
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L229) `public float lineHeight;`

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L47) `public BitmapText() {` — 개별 처리, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale, Matrix.rotate, NoosaScript.get
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L51) `public BitmapText( Font font ) {` — 개별 처리, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale, Matrix.rotate, NoosaScript.get
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L55) `public BitmapText( String text, Font font ) {` — 개별 처리, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale, Matrix.rotate, NoosaScript.get
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L63) `protected void updateMatrix() {` — 행동·상태 갱신, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale, Matrix.rotate, NoosaScript.get
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L72) `public void draw() {` — 개별 처리, 인접 호출: NoosaScript.get, Quad.createSet
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L100) `public void destroy() {` — 개별 처리, 인접 호출: Quad.createSet
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L106) `protected synchronized void updateVertices() {` — 행동·상태 갱신, 인접 호출: Quad.createSet
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L169) `public synchronized void measure() {` — 개별 처리
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L196) `public float baseLine() {` — 개별 처리
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L200) `public Font font() {` — 개별 처리
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L204) `public synchronized void font( Font value ) {` — 개별 처리
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L208) `public String text() {` — 개별 처리
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L212) `public synchronized void text( String str ) {` — 개별 처리
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L231) `protected Font( SmartTexture tx ) {` — 개별 처리
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L237) `public Font( SmartTexture tx, int width, String chars ) {` — 개별 처리
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L241) `public Font( SmartTexture tx, int width, int height, String chars ) {` — 개별 처리
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L268) `protected void splitBy( Pixmap bitmap, int height, int color, String chars ) {` — 개별 처리
- [L339](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L339) `private boolean colorNotMatch(Pixmap pixmap, int x, int y, int color) {` — 개별 처리
- [L347](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L347) `public static Font colorMarked( SmartTexture tex, int color, String chars ) {` — 개별 처리
- [L353](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L353) `public static Font colorMarked( SmartTexture tex, int height, int color, String chars ) {` — 개별 처리
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java#L359) `public RectF get( char ch ) {` — 조회·판정

## 1269. [`Camera.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java)

패키지 `com.watabou.noosa`, 322행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L31) `public class Camera extends Gizmo {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L35) `protected static float invW2;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L36) `protected static float invH2;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L38) `public static Camera main;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L40) `public boolean fullScreen;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L42) `public float zoom;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L44) `public int x;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L45) `public int y;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L46) `public int width;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L47) `public int height;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L52) `public float[] matrix;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L54) `public PointF edgeScroll;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L55) `public PointF scroll;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L56) `public PointF centerOffset;`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L58) `private float shakeMagX		= 10f;`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L59) `private float shakeMagY		= 10f;`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L60) `private float shakeTime		= 0f;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L61) `private float shakeDuration	= 1f;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L63) `protected float shakeX;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L64) `protected float shakeY;`

### 메서드 및 코드 의존 단서
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L66) `public static Camera reset() {` — 개별 처리, 인접 호출: Math.ceil
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L70) `public static synchronized Camera reset( Camera newCamera ) {` — 개별 처리, 인접 호출: Math.ceil
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L84) `public static synchronized Camera add( Camera camera ) {` — 개별 처리, 인접 호출: Math.ceil
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L89) `public static synchronized Camera remove( Camera camera ) {` — 개별 처리, 인접 호출: Math.ceil, Matrix.setIdentity
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L94) `public static synchronized void updateAll() {` — 행동·상태 갱신, 인접 호출: Math.ceil, Matrix.setIdentity
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L104) `public static Camera createFullscreen( float zoom ) {` — 생성·초기화, 인접 호출: Math.ceil, Matrix.setIdentity
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L115) `public Camera( int x, int y, int width, int height, float zoom ) {` — 개별 처리, 인접 호출: Matrix.setIdentity
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L135) `public void destroy() {` — 개별 처리
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L139) `public synchronized void zoom( float value ) {` — 개별 처리
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L145) `public synchronized void zoom( float value, float fx, float fy ) {` — 개별 처리
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L157) `public synchronized void resize( int width, int height ) {` — 개별 처리
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L175) `public synchronized void update() {` — 행동·상태 갱신, 인접 호출: Math.min, Random.Float
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L228) `public PointF center() {` — 개별 처리
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L232) `public boolean hitTest( float x, float y ) {` — 전투 관련
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L236) `public synchronized void shift( PointF point ){` — 개별 처리
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L241) `public synchronized void setCenterOffset( float x, float y ){` — 개별 처리
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L251) `public synchronized void snapTo(float x, float y ) {` — 개별 처리
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L257) `public void snapTo(PointF point ) {` — 개별 처리
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L261) `public synchronized void panTo( PointF dst, float intensity ){` — 개별 처리, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale
- [L267](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L267) `public synchronized void panFollow(Visual target, float intensity ){` — 개별 처리, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L272) `public synchronized Visual followTarget(){` — 개별 처리, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale
- [L276](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L276) `public synchronized void setFollowDeadzone( float deadzone ){` — 개별 처리, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L280) `public PointF screenToCamera( int x, int y ) {` — 개별 처리, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale
- [L286](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L286) `public Point cameraToScreen( float x, float y ) {` — 개별 처리, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L292) `public float screenWidth() {` — 개별 처리, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L296) `public float screenHeight() {` — 개별 처리, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L300) `protected void updateMatrix() {` — 행동·상태 갱신, 인접 호출: Matrix.setIdentity, Matrix.translate, Matrix.scale
- [L317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java#L317) `public synchronized void shake( float magnitude, float duration ) {` — 개별 처리

## 1270. [`ColorBlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ColorBlock.java)

패키지 `com.watabou.noosa`, 49행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ColorBlock.java#L26) `public class ColorBlock extends Image implements Resizable {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ColorBlock.java#L28) `public ColorBlock( float width, float height, int color ) {` — 개별 처리, 인접 호출: TextureCache.createSolid
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ColorBlock.java#L35) `public void size( float width, float height ) {` — 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ColorBlock.java#L40) `public float width() {` — 개별 처리
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ColorBlock.java#L45) `public float height() {` — 개별 처리

## 1271. [`Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)

패키지 `com.watabou.noosa`, 327행.

### 클래스/타입
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L45) `public class Game implements ApplicationListener {`
- [L321](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L321) `public interface SceneChangeCallback{`

### 변수·상수 후보
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L47) `public static Game instance;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L50) `public static int width;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L51) `public static int height;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L54) `public static float density = 1;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L56) `public static String version;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L57) `public static int versionCode;`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L60) `protected Scene scene;`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L62) `protected Scene requestedScene;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L64) `protected boolean requestedReset = true;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L66) `protected SceneChangeCallback onChange;`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L68) `protected static Class<? extends Scene> sceneClass;`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L70) `public static float timeScale = 1f;`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L71) `public static float elapsed = 0f;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L72) `public static float timeTotal = 0f;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L73) `public static long realTime = 0;`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L75) `public static InputHandler inputHandler;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L77) `public static PlatformSupport platform;`
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L119) `private GLVersion versionContextRef;`
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L147) `private boolean justResumed = true;`

### 메서드 및 코드 의존 단서
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L79) `public Game(Class<? extends Scene> c, PlatformSupport platform) {` — 개별 처리, 인접 호출: DeviceCompat.isDesktop, ControllerHandler.controllersSupported, Controllers.addListener, Blending.useDefault, TextureCache.reload, Vertexbuffer.reload
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L87) `public void create() {` — 생성·초기화, 인접 호출: DeviceCompat.isDesktop, ControllerHandler.controllersSupported, Controllers.addListener, Blending.useDefault, TextureCache.reload, Vertexbuffer.reload
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L122) `public void resize(int width, int height) {` — 개별 처리, 인접 호출: Blending.useDefault, TextureCache.reload, Vertexbuffer.reload, DeviceCompat.isAndroid, NoosaScript.get, NoosaScriptNoLighting.get
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L150) `public void render() {` — 개별 처리, 인접 호출: DeviceCompat.isAndroid, NoosaScript.get, NoosaScriptNoLighting.get, Script.reset
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L174) `public void pause() {` — 개별 처리, 인접 호출: Script.reset, INSTANCE.reset
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L183) `public void resume() {` — 개별 처리, 인접 호출: INSTANCE.reset
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L187) `public void finish(){` — 개별 처리, 인접 호출: INSTANCE.reset
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L192) `public void destroy(){` — 개별 처리, 인접 호출: INSTANCE.reset, Reflection.newInstance
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L204) `public void dispose() {` — 개별 처리, 인접 호출: Reflection.newInstance
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L208) `public static void resetScene() {` — 개별 처리, 인접 호출: Reflection.newInstance, Camera.reset
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L212) `public static void switchScene(Class<? extends Scene> c) {` — 개별 처리, 인접 호출: Reflection.newInstance, Camera.reset
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L216) `public static void switchScene(Class<? extends Scene> c, SceneChangeCallback callback) {` — 개별 처리, 인접 호출: Reflection.newInstance, Camera.reset, Vertexbuffer.clear
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L222) `public static Scene scene() {` — 개별 처리, 인접 호출: Reflection.newInstance, Camera.reset, Vertexbuffer.clear
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L226) `public static boolean switchingScene() {` — 개별 처리, 인접 호출: Reflection.newInstance, Camera.reset, Vertexbuffer.clear
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L230) `protected void step() {` — 개별 처리, 인접 호출: Reflection.newInstance, Camera.reset, Vertexbuffer.clear, Math.min
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L245) `protected void draw() {` — 개별 처리, 인접 호출: Camera.reset, Vertexbuffer.clear, Math.min, TimeUtils.millis, INSTANCE.update, Camera.updateAll
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L249) `protected void switchScene() {` — 개별 처리, 인접 호출: Camera.reset, Vertexbuffer.clear, Math.min, TimeUtils.millis, INSTANCE.update, Camera.updateAll
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L269) `protected void update() {` — 행동·상태 갱신, 인접 호출: Math.min, TimeUtils.millis, INSTANCE.update, Camera.updateAll
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L285) `public static void reportException( Throwable tr ) {` — 개별 처리
- [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L298) `protected void logException( Throwable tr ){` — 개별 처리
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L306) `public static void runOnRenderThread(Callback c){` — 개별 처리
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L309) `public void run() {` — 개별 처리
- [L315](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java#L315) `public static void vibrate( int milliseconds ) {` — 개별 처리

## 1272. [`Gizmo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java)

패키지 `com.watabou.noosa`, 102행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L24) `public class Gizmo {`

### 변수·상수 후보
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L26) `public boolean exists;`
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L27) `public boolean alive;`
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L28) `public boolean active;`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L29) `public boolean visible;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L31) `public Group parent;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L33) `public Camera camera;`

### 메서드 및 코드 의존 단서
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L35) `public Gizmo() {` — 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L42) `public void destroy() {` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L46) `public void update() {` — 행동·상태 갱신
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L49) `public void draw() {` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L52) `public void kill() {` — 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L58) `public void revive() {` — 개별 처리
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L63) `public Camera camera() {` — 개별 처리
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L73) `public boolean isVisible() {` — 조회·판정
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L81) `public boolean isActive() {` — 조회·판정
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L89) `public void killAndErase() {` — 개별 처리
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java#L96) `public void remove() {` — 개별 처리

## 1273. [`Group.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java)

패키지 `com.watabou.noosa`, 326행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L31) `public class Group extends Gizmo {`

### 변수·상수 후보
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L33) `protected ArrayList<Gizmo> members;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L37) `public int length;`

### 메서드 및 코드 의존 단서
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L39) `public Group() {` — 개별 처리
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L45) `public synchronized void destroy() {` — 개별 처리
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L62) `public synchronized void update() {` — 행동·상태 갱신
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L72) `public synchronized void draw() {` — 개별 처리
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L82) `public synchronized void kill() {` — 개별 처리
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L95) `public synchronized int indexOf( Gizmo g ) {` — 개별 처리
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L99) `public synchronized Gizmo add( Gizmo g ) {` — 개별 처리
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L124) `public synchronized Gizmo addToFront( Gizmo g){` — 개별 처리
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L154) `public synchronized Gizmo addToBack( Gizmo g ) {` — 개별 처리, 인접 호출: Reflection.newInstance
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L177) `public synchronized Gizmo recycle( Class<? extends Gizmo> c ) {` — 개별 처리, 인접 호출: Reflection.newInstance
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L201) `public synchronized Gizmo erase( Gizmo g ) {` — 개별 처리
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L214) `public synchronized Gizmo remove( Gizmo g ) {` — 개별 처리
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L224) `public synchronized Gizmo replace( Gizmo oldOne, Gizmo newOne ) {` — 개별 처리
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L236) `public synchronized Gizmo getFirstAvailable( Class<? extends Gizmo> c ) {` — 조회·판정, 인접 호출: Random.Int
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L248) `public synchronized int countLiving() {` — 개별 처리, 인접 호출: Random.Int
- [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L262) `public synchronized int countDead() {` — 개별 처리, 인접 호출: Random.Int
- [L276](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L276) `public synchronized Gizmo random() {` — 개별 처리, 인접 호출: Random.Int, Collections.sort
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L284) `public synchronized void clear() {` — 개별 처리, 인접 호출: Collections.sort
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L296) `public synchronized Gizmo bringToFront( Gizmo g ) {` — 개별 처리, 인접 호출: Collections.sort
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L306) `public synchronized Gizmo sendToBack( Gizmo g ) {` — 개별 처리, 인접 호출: Collections.sort
- [L316](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java#L316) `public synchronized void sort(Comparator c){` — 개별 처리, 인접 호출: Collections.sort

## 1274. [`Halo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Halo.java)

패키지 `com.watabou.noosa`, 81행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Halo.java#L27) `public class Halo extends Image {`

### 변수·상수 후보
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Halo.java#L29) `private static final Object CACHE_KEY = Halo.class;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Halo.java#L31) `protected static final int RADIUS	= 128;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Halo.java#L33) `protected float radius = RADIUS;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Halo.java#L34) `protected float brightness = 1;`

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Halo.java#L36) `public Halo() {` — 개별 처리, 인접 호출: TextureCache.contains, TextureCache.create
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Halo.java#L56) `public Halo( float radius, int color, float brightness ) {` — 개별 처리
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Halo.java#L65) `public Halo point( float x, float y ) {` — 개별 처리
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Halo.java#L72) `public void alpha( float value) {` — 개별 처리
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Halo.java#L77) `public void radius(float value ) {` — 개별 처리

## 1275. [`Image.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java)

패키지 `com.watabou.noosa`, 198행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L33) `public class Image extends Visual {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L35) `public SmartTexture texture;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L36) `protected RectF frame;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L38) `public boolean flipHorizontal;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L39) `public boolean flipVertical;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L41) `protected float[] vertices;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L42) `protected FloatBuffer verticesBuffer;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L43) `protected Vertexbuffer buffer;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L45) `protected boolean dirty;`

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L47) `public Image() {` — 개별 처리, 인접 호출: Quad.create, TextureCache.get
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L54) `public Image( Image src ) {` — 개별 처리, 인접 호출: TextureCache.get
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L59) `public Image( Object tx ) {` — 개별 처리, 인접 호출: TextureCache.get
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L64) `public Image( Object tx, int left, int top, int width, int height ) {` — 개별 처리, 인접 호출: TextureCache.get
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L69) `public void texture( Object tx ) {` — 개별 처리, 인접 호출: TextureCache.get
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L74) `public void frame( RectF frame ) {` — 개별 처리
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L84) `public void frame( int left, int top, int width, int height ) {` — 개별 처리
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L88) `public RectF frame() {` — 개별 처리
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L92) `public void copy( Image other ) {` — 개별 처리
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L108) `protected void updateFrame() {` — 행동·상태 갱신
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L137) `protected void updateVertices() {` — 행동·상태 갱신
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L155) `public void draw() {` — 개별 처리, 인접 호출: NoosaScript.get
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L187) `protected NoosaScript script(){` — 개별 처리, 인접 호출: NoosaScript.get
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java#L192) `public void destroy() {` — 개별 처리

## 1276. [`MovieClip.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java)

패키지 `com.watabou.noosa`, 147행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L26) `public class MovieClip extends Image {`
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L114) `public static class Animation {`
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L143) `public interface Listener {`

### 변수·상수 후보
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L28) `protected Animation curAnim;`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L29) `protected int curFrame;`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L30) `protected float frameTimer;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L31) `protected boolean finished;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L33) `public boolean paused = false;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L35) `public Listener listener;`
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L116) `public float delay;`
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L117) `public RectF[] frames;`
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L118) `public boolean looped;`

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L37) `public MovieClip() {` — 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L41) `public MovieClip( Object tx ) {` — 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L46) `public void update() {` — 행동·상태 갱신
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L53) `public boolean looping(){` — 개별 처리
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L57) `protected synchronized void updateAnimation() {` — 행동·상태 갱신
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L93) `public void play( Animation anim ) {` — 개별 처리
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L97) `public synchronized void play( Animation anim, boolean force ) {` — 개별 처리, 인접 호출: Math.round
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L120) `public Animation( int fps, boolean looped ) {` — 개별 처리, 인접 호출: Math.round
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L125) `public Animation frames( RectF... frames ) {` — 개별 처리, 인접 호출: Math.round
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L130) `public Animation frames( TextureFilm film, Object... frames ) {` — 개별 처리, 인접 호출: Math.round
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java#L138) `public Animation clone() {` — 개별 처리, 인접 호출: Math.round

## 1277. [`NinePatch.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java)

패키지 `com.watabou.noosa`, 238행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L33) `public class NinePatch extends Visual {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L35) `public SmartTexture texture;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L37) `protected float[] vertices;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L38) `protected FloatBuffer quads;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L39) `protected Vertexbuffer buffer;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L41) `protected RectF outterF;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L42) `protected RectF innerF;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L44) `protected int marginLeft;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L45) `protected int marginRight;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L46) `protected int marginTop;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L47) `protected int marginBottom;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L49) `protected float nWidth;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L50) `protected float nHeight;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L52) `protected boolean flipHorizontal;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L53) `protected boolean flipVertical;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L55) `protected boolean dirty;`

### 메서드 및 코드 의존 단서
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L57) `public NinePatch( Object tx, int margin ) {` — 개별 처리, 인접 호출: TextureCache.get, Quad.createSet
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L61) `public NinePatch( Object tx, int left, int top, int right, int bottom ) {` — 개별 처리, 인접 호출: TextureCache.get, Quad.createSet
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L65) `public NinePatch( Object tx, int x, int y, int w, int h, int margin ) {` — 개별 처리, 인접 호출: TextureCache.get, Quad.createSet
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L69) `public NinePatch( Object tx, int x, int y, int w, int h, int left, int top, int right, int bottom ) {` — 개별 처리, 인접 호출: TextureCache.get, Quad.createSet, Quad.fill
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L93) `protected void updateVertices() {` — 행동·상태 갱신, 인접 호출: Quad.fill
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L143) `public int marginLeft() {` — 개별 처리
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L147) `public int marginRight() {` — 개별 처리
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L151) `public int marginTop() {` — 개별 처리
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L155) `public int marginBottom() {` — 개별 처리
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L159) `public int marginHor() {` — 개별 처리
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L163) `public int marginVer() {` — 개별 처리
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L167) `public float innerWidth() {` — 개별 처리
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L171) `public float innerHeight() {` — 개별 처리
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L175) `public float innerRight() {` — 개별 처리, 인접 호출: NoosaScript.get
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L179) `public float innerBottom() {` — 개별 처리, 인접 호출: NoosaScript.get
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L183) `public void flipHorizontal(boolean value) {` — 개별 처리, 인접 호출: NoosaScript.get
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L190) `public void flipVertical(boolean value) {` — 개별 처리, 인접 호출: NoosaScript.get
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L197) `public void size( float width, float height ) {` — 개별 처리, 인접 호출: NoosaScript.get
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L204) `public void draw() {` — 개별 처리, 인접 호출: NoosaScript.get
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java#L232) `public void destroy() {` — 개별 처리

## 1278. [`NoosaScript.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java)

패키지 `com.watabou.noosa`, 222행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L36) `public class NoosaScript extends Script {`

### 변수·상수 후보
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L38) `public Uniform uCamera;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L39) `public Uniform uModel;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L40) `public Uniform uTex;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L41) `public Uniform uColorM;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L42) `public Uniform uColorA;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L43) `public Attribute aXY;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L44) `public Attribute aUV;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L46) `private Camera lastCamera;`

### 메서드 및 코드 의존 단서
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L48) `public NoosaScript() {` — 개별 처리, 인접 호출: Quad.setupIndices, Quad.bindIndices, Quad.releaseIndices
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L67) `public void use() {` — 이벤트·효과 실행, 인접 호출: Quad.releaseIndices, Quad.bindIndices
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L76) `public void drawElements( FloatBuffer vertices, ShortBuffer indices, int size ) {` — 개별 처리, 인접 호출: Quad.releaseIndices, Quad.bindIndices
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L89) `public void drawQuad( FloatBuffer vertices ) {` — 개별 처리
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L100) `public void drawQuad( Vertexbuffer buffer ) {` — 개별 처리
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L114) `public void drawQuadSet( FloatBuffer vertices, int size ) {` — 개별 처리
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L129) `public void drawQuadSet( Vertexbuffer buffer, int length, int offset ){` — 개별 처리, 인접 호출: DeviceCompat.getRealPixelScaleX, DeviceCompat.getRealPixelScaleY
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L147) `public void lighting( float rm, float gm, float bm, float am, float ra, float ga, float ba, float aa ) {` — 개별 처리, 인접 호출: DeviceCompat.getRealPixelScaleX, DeviceCompat.getRealPixelScaleY, Math.round, Script.use
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L152) `public void resetCamera() {` — 개별 처리, 인접 호출: DeviceCompat.getRealPixelScaleX, DeviceCompat.getRealPixelScaleY, Math.round, Script.use
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L156) `public void camera( Camera camera ) {` — 개별 처리, 인접 호출: DeviceCompat.getRealPixelScaleX, DeviceCompat.getRealPixelScaleY, Math.round, Script.use
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L184) `public static NoosaScript get() {` — 조회·판정, 인접 호출: Script.use
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java#L189) `protected String shader() {` — 개별 처리

## 1279. [`NoosaScriptNoLighting.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScriptNoLighting.java)

패키지 `com.watabou.noosa`, 74행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScriptNoLighting.java#L31) `public class NoosaScriptNoLighting extends NoosaScript {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScriptNoLighting.java#L34) `public void lighting(float rm, float gm, float bm, float am, float ra, float ga, float ba, float aa) {` — 개별 처리, 인접 호출: Script.use
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScriptNoLighting.java#L38) `public static NoosaScriptNoLighting get(){` — 조회·판정, 인접 호출: Script.use
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScriptNoLighting.java#L43) `protected String shader() {` — 개별 처리

## 1280. [`BitmaskEmitter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/BitmaskEmitter.java)

패키지 `com.watabou.noosa.particles`, 64행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/BitmaskEmitter.java#L29) `public class BitmaskEmitter extends Emitter {`

### 변수·상수 후보
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/BitmaskEmitter.java#L33) `private SmartTexture map;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/BitmaskEmitter.java#L34) `private int mapW;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/BitmaskEmitter.java#L35) `private int mapH;`

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/BitmaskEmitter.java#L37) `public BitmaskEmitter( Image target ) {` — 개별 처리, 인접 호출: Random.Float
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/BitmaskEmitter.java#L48) `protected void emit( int index ) {` — 개별 처리, 인접 호출: Random.Float

## 1281. [`Emitter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java)

패키지 `com.watabou.noosa.particles`, 193행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L31) `public class Emitter extends Group {`
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L184) `abstract public static class Factory {`

### 변수·상수 후보
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L33) `protected boolean lightMode = false;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L35) `public float x;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L36) `public float y;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L37) `public float width;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L38) `public float height;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L40) `protected Visual target;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L41) `public boolean fillTarget = true;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L43) `protected float interval;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L44) `protected int quantity;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L46) `public boolean on = false;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L48) `private boolean started = false;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L49) `public boolean autoKill = true;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L51) `protected int count;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L52) `protected float time;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L54) `protected Factory factory;`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L109) `public static boolean freezeEmitters = false;`

### 메서드 및 코드 의존 단서
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L56) `public void pos( float x, float y ) {` — 개별 처리, 인접 호출: Random.Float
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L60) `public void pos( PointF p ) {` — 개별 처리, 인접 호출: Random.Float
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L64) `public void pos( float x, float y, float width, float height ) {` — 개별 처리, 인접 호출: Random.Float
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L73) `public void pos( Visual target ) {` — 개별 처리, 인접 호출: Random.Float
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L77) `public void pos( Visual target, float x, float y, float width, float height ) {` — 개별 처리, 인접 호출: Random.Float
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L82) `public void burst( Factory factory, int quantity ) {` — 개별 처리, 인접 호출: Random.Float
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L86) `public void pour( Factory factory, float interval ) {` — 개별 처리, 인접 호출: Random.Float
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L90) `public void start( Factory factory, float interval, int quantity ) {` — 개별 처리, 인접 호출: Random.Float
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L95) `public void startDelayed( Factory factory, float interval, int quantity, float delay ) {` — 개별 처리
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L111) `protected boolean isFrozen(){` — 조회·판정, 인접 호출: Random.Float
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L116) `public void update() {` — 행동·상태 갱신, 인접 호출: Random.Float
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L140) `public void revive() {` — 개별 처리, 인접 호출: Random.Float, Blending.setLightMode, Blending.setNormalMode
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L149) `protected void emit( int index ) {` — 개별 처리, 인접 호출: Random.Float, Blending.setLightMode, Blending.setNormalMode
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L174) `public void draw() {` — 개별 처리, 인접 호출: Blending.setLightMode, Blending.setNormalMode
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L186) `abstract public void emit( Emitter emitter, int index, float x, float y );` — 개별 처리
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java#L188) `public boolean lightMode() {` — 개별 처리


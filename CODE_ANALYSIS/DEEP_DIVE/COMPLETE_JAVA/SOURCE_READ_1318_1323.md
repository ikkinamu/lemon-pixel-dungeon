# Java 소스 구현 분석 1318–1323

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1318. [`Random.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java)

패키지 `com.watabou.utils`, 297행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L32) `public class Random {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L37) `private static ArrayDeque<java.util.Random> generators;`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L42) `public static synchronized void resetGenerators(){` — 개별 처리, 인접 호출: Game.reportException
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L47) `public static synchronized void pushGenerator(){` — 개별 처리, 인접 호출: Game.reportException
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L51) `public static synchronized void pushGenerator( long seed ){` — 개별 처리, 인접 호출: Game.reportException
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L57) `private static synchronized long scrambleSeed( long seed ){` — 개별 처리, 인접 호출: Game.reportException
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L68) `public static synchronized void popGenerator(){` — 개별 처리, 인접 호출: Game.reportException
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L77) `public static synchronized float Float() {` — 개별 처리
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L81) `public static synchronized float Float( boolean useGeneratorStack ) {` — 개별 처리
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L87) `public static float Float( float max ) {` — 개별 처리
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L92) `public static float Float( float min, float max ) {` — 개별 처리
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L97) `public static float NormalFloat( float min, float max ) {` — 개별 처리
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L102) `public static synchronized int Int() {` — 개별 처리, 인접 호출: Math.abs
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L108) `public static synchronized int Int( boolean useGeneratorStack ) {` — 개별 처리, 인접 호출: Math.abs
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L114) `public static synchronized int Int( int max ) {` — 개별 처리, 인접 호출: Math.abs
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L120) `public static synchronized int Int( int max, boolean useGeneratorStack ) {` — 개별 처리, 인접 호출: Math.abs
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L127) `public static int Int( int min, int max ) {` — 개별 처리, 인접 호출: Math.abs
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L132) `public static int IntRange( int min, int max ) {` — 개별 처리, 인접 호출: Math.abs
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L138) `public static int NormalIntRange( int min, int max ) {` — 개별 처리, 인접 호출: Math.abs, Math.max
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L144) `public static int InvNormalIntRange( int min, int max ){` — 개별 처리, 인접 호출: Math.abs, Math.max
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L154) `public static synchronized long Long() {` — 개별 처리, 인접 호출: Math.max
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L160) `public static synchronized long Long( boolean useGeneratorStack ) {` — 개별 처리, 인접 호출: Math.max
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L166) `public static long Long( long max ) {` — 개별 처리, 인접 호출: Math.max
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L175) `public static int chances( float[] chances ) {` — 개별 처리, 인접 호출: Math.max
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L202) `public static <K> K chances( HashMap<K,Float> chances ) {` — 개별 처리
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L231) `public static int index( Collection<?> collection ) {` — 개별 처리, 인접 호출: Collections.shuffle
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L236) `public static<T> T oneOf(T... array ) {` — 이벤트·효과 실행, 인접 호출: Collections.shuffle
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L240) `public static<T> T element( T[] array ) {` — 개별 처리, 인접 호출: Collections.shuffle
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L244) `public static<T> T element( T[] array, int max ) {` — 개별 처리, 인접 호출: Collections.shuffle
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L249) `public static<T> T element( Collection<? extends T> collection ) {` — 개별 처리, 인접 호출: Collections.shuffle
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L256) `public synchronized static<T> void shuffle( List<?extends T> list){` — 개별 처리, 인접 호출: Collections.shuffle
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L260) `public static void shuffle( int[] array ) {` — 개별 처리
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L271) `public static<T> void shuffle( T[] array ) {` — 개별 처리
- [L282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L282) `public static<U,V> void shuffle( U[] u, V[]v ) {` — 개별 처리

## 1319. [`Rect.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java)

패키지 `com.watabou.utils`, 164행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L26) `public class Rect {`

### 변수·상수 후보
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L28) `public int left;`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L29) `public int top;`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L30) `public int right;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L31) `public int bottom;`

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L33) `public Rect() {` — 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L37) `public Rect( Rect rect ) {` — 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L41) `public Rect( int left, int top, int right, int bottom ) {` — 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L48) `public int width() {` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L52) `public int height() {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L56) `public int square() {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L60) `public Rect set( int left, int top, int right, int bottom ) {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L68) `public Rect set( Rect rect ) {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L72) `public Rect setPos( int x, int y ) {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L76) `public Rect shift( int x, int y ) {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L80) `public Rect resize( int w, int h ){` — 개별 처리, 인접 호출: Math.max, Math.min
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L84) `public boolean isEmpty() {` — 조회·판정, 인접 호출: Math.max, Math.min
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L88) `public Rect setEmpty() {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L93) `public Rect intersect( Rect other ) {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L102) `public Rect union( Rect other ){` — 개별 처리, 인접 호출: Math.min, Math.max, Random.Int
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L111) `public Rect union( int x, int y ) {` — 개별 처리, 인접 호출: Random.Int
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L129) `public Rect union( Point p ) {` — 개별 처리, 인접 호출: Random.Int
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L133) `public boolean inside( Point p ) {` — 개별 처리, 인접 호출: Random.Int
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L137) `public Point center() {` — 개별 처리, 인접 호출: Random.Int
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L143) `public Rect shrink( int d ) {` — 개별 처리
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L147) `public Rect shrink() {` — 개별 처리
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L151) `public Rect scale( int d ){` — 개별 처리
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java#L155) `public ArrayList<Point> getPoints() {` — 조회·판정

## 1320. [`RectF.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java)

패키지 `com.watabou.utils`, 152행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L24) `public class RectF {`

### 변수·상수 후보
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L26) `public float left;`
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L27) `public float top;`
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L28) `public float right;`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L29) `public float bottom;`

### 메서드 및 코드 의존 단서
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L31) `public RectF() {` — 개별 처리
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L35) `public RectF( RectF rect ) {` — 개별 처리
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L39) `public RectF( Rect rect ) {` — 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L43) `public RectF( float left, float top, float right, float bottom ) {` — 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L50) `public float width() {` — 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L54) `public float height() {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L58) `public float square() {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L62) `public RectF set( float left, float top, float right, float bottom ) {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L70) `public RectF set( Rect rect ) {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L74) `public RectF setPos( float x, float y ) {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L78) `public RectF shift( float x, float y ) {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L82) `public RectF resize( float w, float h ){` — 개별 처리, 인접 호출: Math.max, Math.min
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L86) `public boolean isEmpty() {` — 조회·판정, 인접 호출: Math.max, Math.min
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L90) `public RectF setEmpty() {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L95) `public RectF intersect( RectF other ) {` — 개별 처리, 인접 호출: Math.max, Math.min
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L104) `public RectF union( RectF other ){` — 개별 처리, 인접 호출: Math.min, Math.max
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L113) `public RectF union( float x, float y ) {` — 개별 처리
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L131) `public RectF union( Point p ) {` — 개별 처리
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L135) `public boolean inside( Point p ) {` — 개별 처리
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L139) `public RectF shrink( float d ) {` — 개별 처리
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L143) `public RectF shrink() {` — 개별 처리
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java#L147) `public RectF scale( float d ){` — 개별 처리

## 1321. [`Reflection.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Reflection.java)

패키지 `com.watabou.utils`, 65행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Reflection.java#L28) `public class Reflection {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Reflection.java#L30) `public static boolean isMemberClass( Class cls ){` — 조회·판정, 인접 호출: ClassReflection.isMemberClass, ClassReflection.isStaticClass, ClassReflection.newInstance, Game.reportException, ClassReflection.forName
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Reflection.java#L34) `public static boolean isStatic( Class cls ){` — 조회·판정, 인접 호출: ClassReflection.isStaticClass, ClassReflection.newInstance, Game.reportException, ClassReflection.forName
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Reflection.java#L38) `public static <T> T newInstance( Class<T> cls ){` — 개별 처리, 인접 호출: ClassReflection.newInstance, Game.reportException, ClassReflection.forName
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Reflection.java#L47) `public static <T> T newInstanceUnhandled( Class<T> cls ) throws Exception {` — 개별 처리, 인접 호출: ClassReflection.newInstance, ClassReflection.forName, Game.reportException
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Reflection.java#L51) `public static Class forName( String name ){` — 개별 처리, 인접 호출: ClassReflection.forName, Game.reportException
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Reflection.java#L60) `public static Class forNameUnhandled( String name ) throws Exception {` — 개별 처리, 인접 호출: ClassReflection.forName

## 1322. [`Signal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java)

패키지 `com.watabou.utils`, 88행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java#L26) `public class Signal<T> {`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java#L83) `public interface Listener<T> {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java#L30) `private boolean stackMode;`

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java#L32) `public Signal() {` — 개별 처리
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java#L36) `public Signal( boolean stackMode ) {` — 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java#L40) `public synchronized void add( Listener<T> listener ) {` — 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java#L50) `public synchronized void remove( Listener<T> listener ) {` — 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java#L54) `public synchronized void removeAll() {` — 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java#L58) `public synchronized void replace( Listener<T> listener ) {` — 개별 처리
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java#L63) `public synchronized int numListeners() {` — 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java#L67) `public synchronized void dispatch( T t ) {` — 개별 처리

## 1323. [`SparseArray.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/SparseArray.java)

패키지 `com.watabou.utils`, 54행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/SparseArray.java#L29) `public class SparseArray<T> extends IntMap<T> {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/SparseArray.java#L32) `public synchronized T put(int key, T value) {` — 개별 처리, 인접 호출: Arrays.asList
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/SparseArray.java#L37) `public synchronized T get(int key, T defaultValue) {` — 조회·판정, 인접 호출: Arrays.asList
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/SparseArray.java#L42) `public synchronized T remove(int key) {` — 개별 처리, 인접 호출: Arrays.asList
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/SparseArray.java#L46) `public synchronized int[] keyArray() {` — 개별 처리, 인접 호출: Arrays.asList
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/SparseArray.java#L50) `public synchronized List<T> valueList() {` — 개별 처리, 인접 호출: Arrays.asList


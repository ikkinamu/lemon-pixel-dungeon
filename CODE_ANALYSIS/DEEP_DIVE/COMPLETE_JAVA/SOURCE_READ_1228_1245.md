# Java 소스 구현 분석 1228–1245

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1228. [`DesktopPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.desktop`, 177행.

### 클래스/타입
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L40) `public class DesktopPlatformSupport extends PlatformSupport {`

### 변수·상수 후보
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L44) `protected static Point[] previousSizes = null;`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L60) `private static boolean first = true;`
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L110) `private static FreeTypeFontGenerator basicFontGenerator;`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L112) `private static FreeTypeFontGenerator asianFontGenerator;`

### 메서드 및 코드 의존 단서
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L47) `public void updateDisplaySize() {` — 행동·상태 갱신, 인접 호출: SPDSettings.windowResolution, SPDSettings.fullscreen, SPDSettings.fulLScreenMonitor
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L63) `public void updateSystemUI() {` — 행동·상태 갱신, 인접 호출: SPDSettings.fullscreen, SPDSettings.fulLScreenMonitor, SPDSettings.windowResolution, ControllerHandler.vibrationSupported
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L66) `public void run () {` — 개별 처리, 인접 호출: SPDSettings.fullscreen, SPDSettings.fulLScreenMonitor, SPDSettings.windowResolution, ControllerHandler.vibrationSupported
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L97) `public boolean connectedToUnmeteredNetwork() {` — 개별 처리, 인접 호출: ControllerHandler.vibrationSupported, Pattern.compile
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L102) `public boolean supportsVibration() {` — 개별 처리, 인접 호출: ControllerHandler.vibrationSupported, Pattern.compile
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L115) `public void setupFontGenerators(int pageSize, boolean systemfont) {` — 생성·초기화, 인접 호출: Pattern.compile
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L144) `protected FreeTypeFontGenerator getGeneratorForString( String input ){` — 조회·판정, 인접 호출: Pattern.compile
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java#L169) `public String[] splitforTextBlock(String text, boolean multiline) {` — 개별 처리

## 1229. [`DesktopWindowListener.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopWindowListener.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.desktop`, 58행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopWindowListener.java#L29) `public class DesktopWindowListener implements Lwjgl3WindowListener {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopWindowListener.java#L32) `public void created ( Lwjgl3Window lwjgl3Window ) { }` — 생성·초기화, 인접 호출: SPDSettings.windowMaximized, SPDSettings.windowResolution, SPDSettings.playMusicInBackground, INSTANCE.pause, INSTANCE.resume
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopWindowListener.java#L35) `public void maximized ( boolean b ) {` — 개별 처리, 인접 호출: SPDSettings.windowMaximized, SPDSettings.windowResolution, SPDSettings.playMusicInBackground, INSTANCE.pause, INSTANCE.resume
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopWindowListener.java#L43) `public void iconified ( boolean b ) { }` — 개별 처리, 인접 호출: SPDSettings.playMusicInBackground, INSTANCE.pause, INSTANCE.resume
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopWindowListener.java#L44) `public void focusLost () {` — 개별 처리, 인접 호출: SPDSettings.playMusicInBackground, INSTANCE.pause, INSTANCE.resume
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopWindowListener.java#L49) `public void focusGained () {` — 개별 처리, 인접 호출: SPDSettings.playMusicInBackground, INSTANCE.resume
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopWindowListener.java#L54) `public boolean closeRequested () { return true; }` — 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopWindowListener.java#L55) `public void filesDropped ( String[] strings ) { }` — 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopWindowListener.java#L56) `public void refreshRequested () { }` — 개별 처리

## 1230. [`IOSLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ios`, 221행.

### 클래스/타입
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java#L54) `public class IOSLauncher extends IOSApplication.Delegate {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java#L56) `protected IOSApplication createApplication() {` — 생성·초기화, 인접 호출: NSException.registerDefaultJavaUncaughtExceptionHandler, NSBundle.getMainBundle, Integer.parseInt, UpdateImpl.supportsUpdates, UpdateImpl.getUpdateService, NewsImpl.supportsNews, NewsImpl.getNewsService
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java#L193) `protected IOSInput createInput() {` — 생성·초기화, 인접 호출: ShatteredPixelDungeon.seamlessResetScene, UIApplication.main
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java#L197) `public void setOnscreenKeyboardVisible(boolean visible, OnscreenKeyboardType type) {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.seamlessResetScene, UIApplication.main
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java#L210) `public void didChangStatusBarOrientation(UIApplication application, UIInterfaceOrientation oldStatusBarOrientation) {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.seamlessResetScene, UIApplication.main
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java#L215) `public static void main(String[] argv) {` — 개별 처리, 인접 호출: UIApplication.main

## 1231. [`IOSPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ios`, 260행.

### 클래스/타입
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L47) `public class IOSPlatformSupport extends PlatformSupport {`

### 변수·상수 후보
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L193) `private static FreeTypeFontGenerator basicFontGenerator;`
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L195) `private static FreeTypeFontGenerator asianFontGenerator;`

### 메서드 및 코드 의존 단서
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L50) `public void updateDisplaySize() {` — 행동·상태 갱신, 인접 호출: UIApplication.getSharedApplication, HWMachine.getMachineString
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L55) `public boolean supportsFullScreen() {` — 개별 처리, 인접 호출: HWMachine.getMachineString
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L61) `public RectF getDisplayCutout() {` — 조회·판정, 인접 호출: HWMachine.getMachineString, SPDSettings.fullscreen
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L93) `public RectF getSafeInsets(int level) {` — 조회·판정, 인접 호출: SPDSettings.fullscreen, UIApplication.getSharedApplication
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L133) `public void updateSystemUI() {` — 행동·상태 갱신, 인접 호출: ControllerHandler.vibrationSupported, HWMachine.getMachineString, ControllerHandler.isControllerConnected, ControllerHandler.vibrate, AudioServices.playSystemSound
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L138) `public boolean connectedToUnmeteredNetwork() {` — 개별 처리, 인접 호출: ControllerHandler.vibrationSupported, HWMachine.getMachineString, ControllerHandler.isControllerConnected, ControllerHandler.vibrate, AudioServices.playSystemSound, OALSimpleAudio.sharedInstance
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L144) `public boolean supportsVibration() {` — 개별 처리, 인접 호출: ControllerHandler.vibrationSupported, HWMachine.getMachineString, ControllerHandler.isControllerConnected, ControllerHandler.vibrate, AudioServices.playSystemSound, OALSimpleAudio.sharedInstance
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L167) `public void vibrate(int millis ){` — 개별 처리, 인접 호출: ControllerHandler.isControllerConnected, ControllerHandler.vibrate, AudioServices.playSystemSound, OALSimpleAudio.sharedInstance
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L180) `public void setHonorSilentSwitch( boolean value ) {` — 개별 처리, 인접 호출: OALSimpleAudio.sharedInstance, Pattern.compile
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L184) `public void setOnscreenKeyboardVisible(boolean value, boolean multiline){` — 개별 처리, 인접 호출: Pattern.compile
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L198) `public void setupFontGenerators(int pageSize, boolean systemfont) {` — 생성·초기화, 인접 호출: Pattern.compile
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L227) `protected FreeTypeFontGenerator getGeneratorForString( String input ){` — 조회·판정, 인접 호출: Pattern.compile
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java#L252) `public String[] splitforTextBlock(String text, boolean multiline) {` — 개별 처리

## 1232. [`DebugNews.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/debugNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/DebugNews.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.services.news`, 75행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/debugNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/DebugNews.java#L29) `public class DebugNews extends NewsService {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/debugNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/DebugNews.java#L32) `public void checkForArticles(boolean useMetered, boolean forceHTTPS, NewsResultCallback callback) {` — 개별 처리

## 1233. [`NewsImpl.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/debugNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsImpl.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.services.news`, 37행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/debugNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsImpl.java#L24) `public class NewsImpl {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/debugNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsImpl.java#L26) `private static NewsService newsChecker = new DebugNews();` — 개별 처리
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/debugNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsImpl.java#L28) `public static NewsService getNewsService(){` — 조회·판정
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/debugNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsImpl.java#L32) `public static boolean supportsNews(){` — 개별 처리

## 1234. [`NewsImpl.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsImpl.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.services.news`, 36행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsImpl.java#L24) `public class NewsImpl {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsImpl.java#L26) `private static NewsService newsChecker = new ShatteredNews();` — 개별 처리
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsImpl.java#L28) `public static NewsService getNewsService(){` — 조회·판정
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsImpl.java#L32) `public static boolean supportsNews(){` — 개별 처리

## 1235. [`ShatteredNews.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/ShatteredNews.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.services.news`, 114행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/ShatteredNews.java#L37) `public class ShatteredNews extends NewsService {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/ShatteredNews.java#L40) `public void checkForArticles(boolean useMetered, boolean preferHTTPS, NewsResultCallback callback) {` — 개별 처리, 인접 호출: Net.HttpRequest, Net.HttpResponseListener, Game.reportException, URL.replace, Pattern.compile
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/ShatteredNews.java#L56) `public void handleHttpResponse(Net.HttpResponse httpResponse) {` — 개별 처리, 인접 호출: Game.reportException, URL.replace, Pattern.compile, Integer.parseInt
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/ShatteredNews.java#L102) `public void failed(Throwable t) {` — 개별 처리
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/ShatteredNews.java#L107) `public void cancelled() {` — 조회·판정

## 1236. [`NewsArticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsArticle.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.services.news`, 38행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsArticle.java#L26) `public class NewsArticle {`

### 변수·상수 후보
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsArticle.java#L28) `public String title;`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsArticle.java#L29) `public Date date;`
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsArticle.java#L30) `public String summary;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsArticle.java#L32) `public String URL;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsArticle.java#L36) `public String icon;`

### 메서드 및 코드 의존 단서
- 없음

## 1237. [`NewsService.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsService.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.services.news`, 36행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsService.java#L26) `public abstract class NewsService {`
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsService.java#L28) `public static abstract class NewsResultCallback {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsService.java#L29) `public abstract void onArticlesFound(ArrayList<NewsArticle> articles);` — 이벤트·효과 실행
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsService.java#L30) `public abstract void onConnectionFailed();` — 이벤트·효과 실행
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsService.java#L33) `public abstract void checkForArticles(boolean useMetered, boolean forceHTTPS, NewsResultCallback callback);` — 개별 처리

## 1238. [`AvailableUpdateData.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/AvailableUpdateData.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.services.updates`, 34행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/AvailableUpdateData.java#L24) `public class AvailableUpdateData {`

### 변수·상수 후보
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/AvailableUpdateData.java#L26) `public String versionName;`
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/AvailableUpdateData.java#L27) `public int versionCode;`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/AvailableUpdateData.java#L29) `public String desc;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/AvailableUpdateData.java#L31) `public String URL;`

### 메서드 및 코드 의존 단서
- 없음

## 1239. [`UpdateService.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.services.updates`, 56행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L26) `public abstract class UpdateService {`
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L28) `public static abstract class UpdateResultCallback {`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L44) `public static abstract class ReviewResultCallback {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L29) `public abstract void onUpdateAvailable( AvailableUpdateData update );` — 이벤트·효과 실행
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L30) `public abstract void onNoUpdateFound();` — 이벤트·효과 실행
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L31) `public abstract void onConnectionFailed();` — 이벤트·효과 실행
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L35) `public abstract boolean supportsUpdatePrompts();` — 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L38) `public abstract boolean supportsBetaChannel();` — 개별 처리
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L40) `public abstract void checkForUpdate( boolean useMetered, boolean includeBetas, UpdateResultCallback callback );` — 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L42) `public abstract void initializeUpdate( AvailableUpdateData update );` — 생성·초기화
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L45) `public abstract void onComplete();` — 이벤트·효과 실행
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L49) `public abstract boolean supportsReviews();` — 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L51) `public abstract void initializeReview( ReviewResultCallback callback );` — 생성·초기화
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java#L53) `public abstract void openReviewURI();` — 개별 처리

## 1240. [`DebugUpdates.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/DebugUpdates.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.services.updates`, 78행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/DebugUpdates.java#L27) `public class DebugUpdates extends UpdateService {`

### 변수·상수 후보
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/DebugUpdates.java#L29) `private static AvailableUpdateData debugUpdateInfo;`

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/DebugUpdates.java#L32) `public boolean supportsUpdatePrompts() {` — 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/DebugUpdates.java#L37) `public boolean supportsBetaChannel() {` — 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/DebugUpdates.java#L42) `public void checkForUpdate(boolean useMetered, boolean includeBetas, UpdateResultCallback callback) {` — 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/DebugUpdates.java#L58) `public void initializeUpdate(AvailableUpdateData update) {` — 생성·초기화
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/DebugUpdates.java#L63) `public boolean supportsReviews() {` — 개별 처리
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/DebugUpdates.java#L68) `public void initializeReview(ReviewResultCallback callback) {` — 생성·초기화
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/DebugUpdates.java#L74) `public void openReviewURI() {` — 개별 처리

## 1241. [`UpdateImpl.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateImpl.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.services.updates`, 39행.

### 클래스/타입
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateImpl.java#L26) `public class UpdateImpl {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateImpl.java#L28) `private static UpdateService updateChecker = new DebugUpdates();` — 개별 처리
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateImpl.java#L30) `public static UpdateService getUpdateService(){` — 조회·판정
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/debugUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateImpl.java#L34) `public static boolean supportsUpdates(){` — 개별 처리

## 1242. [`GitHubUpdates.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.services.updates`, 170행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L36) `public class GitHubUpdates extends UpdateService {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L38) `private static Pattern descPattern = Pattern.compile("(.*?)(\r\n|\n|\r)(\r\n|\n|\r)---", Pattern.DOTALL + Pattern.MULTILINE);` — 개별 처리, 인접 호출: Pattern.compile, Net.HttpRequest, Net.HttpResponseListener, Bundle.read, Integer.parseInt
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L39) `private static Pattern versionCodePattern = Pattern.compile("internal version number: ([0-9]*)", Pattern.CASE_INSENSITIVE);` — 개별 처리, 인접 호출: Pattern.compile, Net.HttpRequest, Net.HttpResponseListener, Bundle.read, Integer.parseInt
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L41) `private static Pattern minAndroidPattern = Pattern.compile("Android .*\\(API ([0-9]*)\\)\\+ Devices", Pattern.CASE_INSENSITIVE);` — 개별 처리, 인접 호출: Pattern.compile, Net.HttpRequest, Net.HttpResponseListener, Bundle.read, Integer.parseInt
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L42) `private static Pattern minIOSPattern = Pattern.compile("iOS ([0-9]*)\\+ Devices", Pattern.CASE_INSENSITIVE);` — 개별 처리, 인접 호출: Net.HttpRequest, Net.HttpResponseListener, Bundle.read, Integer.parseInt
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L45) `public boolean supportsUpdatePrompts() {` — 개별 처리, 인접 호출: Net.HttpRequest, Net.HttpResponseListener, Bundle.read, Integer.parseInt, DeviceCompat.isAndroid
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L50) `public boolean supportsBetaChannel() {` — 개별 처리, 인접 호출: Net.HttpRequest, Net.HttpResponseListener, Bundle.read, Integer.parseInt, DeviceCompat.isAndroid, DeviceCompat.getPlatformVersion, DeviceCompat.isiOS
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L55) `public void checkForUpdate(boolean useMetered, boolean includeBetas, UpdateResultCallback callback) {` — 개별 처리, 인접 호출: Net.HttpRequest, Net.HttpResponseListener, Bundle.read, Integer.parseInt, DeviceCompat.isAndroid, DeviceCompat.getPlatformVersion, DeviceCompat.isiOS
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L68) `public void handleHttpResponse(Net.HttpResponse httpResponse) {` — 개별 처리, 인접 호출: Bundle.read, Integer.parseInt, DeviceCompat.isAndroid, DeviceCompat.getPlatformVersion, DeviceCompat.isiOS
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L129) `public void failed(Throwable t) {` — 개별 처리, 인접 호출: Game.reportException
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L142) `public void cancelled() {` — 조회·판정
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L150) `public void initializeUpdate(AvailableUpdateData update) {` — 생성·초기화
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L155) `public boolean supportsReviews() {` — 개별 처리
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L160) `public void initializeReview(ReviewResultCallback callback) {` — 생성·초기화
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java#L166) `public void openReviewURI() {` — 개별 처리

## 1243. [`UpdateImpl.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateImpl.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.services.updates`, 37행.

### 클래스/타입
- [L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateImpl.java#L24) `public class UpdateImpl {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateImpl.java#L26) `private static UpdateService updateChecker = new GitHubUpdates();` — 개별 처리
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateImpl.java#L28) `public static UpdateService getUpdateService(){` — 조회·판정
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateImpl.java#L32) `public static boolean supportsUpdates(){` — 개별 처리

## 1244. [`Script.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glscripts/Script.java)

패키지 `com.watabou.glscripts`, 83행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glscripts/Script.java#L30) `public class Script extends Program {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glscripts/Script.java#L35) `private static Script curScript = null;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glscripts/Script.java#L36) `private static Class<? extends Script> curScriptClass = null;`

### 메서드 및 코드 의존 단서
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glscripts/Script.java#L39) `public synchronized static<T extends Script> T use( Class<T> c ) {` — 이벤트·효과 실행, 인접 호출: Reflection.newInstance, Shader.createCompiled
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glscripts/Script.java#L58) `public synchronized static void unuse(){` — 개별 처리, 인접 호출: Shader.createCompiled
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glscripts/Script.java#L63) `public synchronized static void reset() {` — 개별 처리, 인접 호출: Shader.createCompiled
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glscripts/Script.java#L73) `public void compile( String src ) {` — 개별 처리, 인접 호출: Shader.createCompiled

## 1245. [`Atlas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java)

패키지 `com.watabou.gltextures`, 100행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L28) `public class Atlas {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L30) `public SmartTexture tx;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L32) `protected HashMap<Object,RectF> namedFrames;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L34) `protected float uvLeft;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L35) `protected float uvTop;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L36) `protected float uvWidth;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L37) `protected float uvHeight;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L38) `protected int cols;`

### 메서드 및 코드 의존 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L40) `public Atlas( SmartTexture tx ) {` — 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L48) `public void add( Object key, int left, int top, int right, int bottom ) {` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L52) `public void add( Object key, RectF rect ) {` — 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L56) `public void grid( int width ) {` — 개별 처리
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L60) `public void grid( int width, int height ) {` — 개별 처리
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L64) `public void grid( int left, int top, int width, int height, int cols ) {` — 개별 처리
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L72) `public RectF get( int index ) {` — 조회·판정
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L80) `public RectF get( Object key ) {` — 조회·판정
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L84) `public float width( RectF rect ) {` — 개별 처리
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L88) `public float height( RectF rect ) {` — 개별 처리
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/Atlas.java#L92) `public static RectF uvRect( SmartTexture tx, int left, int top, int right, int bottom ) {` — 개별 처리


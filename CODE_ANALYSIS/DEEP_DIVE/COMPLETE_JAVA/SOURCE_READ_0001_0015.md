# Java 소스 본문별 메서드 해설 — 1–15

실제 Java 소스 기준 커밋: `bd3a990254e4249458816f4879e93ab87275555b`. **이름만 추정한 파일 분류와 달리 소스 본문을 직접 읽었다.** 아래 정적 패턴 추출은 모든 메서드의 정확한 의미/실행 순서를 보장하지 않으며, 호출 구문은 실행된 호출이 아니다. 복잡한 다중 행 선언 및 익명 내부 클래스는 일부 누락될 수 있다.

## 1. [`AndroidBackupHandler.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidBackupHandler.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.android`; **본문:** 79행; **클래스·내부 타입:** 1개; **필드 후보:** 0개; **메서드 후보:** 4개.

### 타입 및 상속 선언
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidBackupHandler.java#L38) `class AndroidBackupHandler  extends BackupAgent`

### 필드·상수
- 단일 행 필드 패턴 없음

### 메서드·기능 연결
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidBackupHandler.java#L42) **`onBackup(ParcelFileDescriptor oldState, BackupDataOutput data, ParcelFileDescriptor newState)`**: 이벤트·효과 실행
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidBackupHandler.java#L43) **`onRestore(BackupDataInput data, int appVersionCode, ParcelFileDescriptor newState)`**: 이벤트·효과 실행
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidBackupHandler.java#L47) **`onFullBackup(FullBackupDataOutput data)`**: 이벤트·효과 실행; 조건 분기; 본문 호출 표현 fullBackupFile, File, getFilesDir, getParent, getFile
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidBackupHandler.java#L70) **`getFile(File base, String name)`**: 조회·탐색; 조건 분기; 본문 호출 표현 File, file.exists, file.isDirectory

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 2. [`AndroidLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.android`; **본문:** 205행; **클래스·내부 타입:** 1개; **필드 후보:** 2개; **메서드 후보:** 8개.

### 타입 및 상속 선언
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java#L54) `class AndroidLauncher  extends AndroidApplication`

### 필드·상수
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java#L56) `AndroidApplication instance`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java#L58) `AndroidPlatformSupport support`

### 메서드·기능 연결
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java#L62) **`onCreate(Bundle savedInstanceState)`**: 이벤트·효과 실행; 조건 분기/예외 처리; 본문 호출 표현 super.onCreate, GdxNativesLoader.load, FreeType.initFreeType, Intent, startActivity, finish, getPackageManager, getPackageInfo, getPackageName
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java#L142) **`run()`**: 개별 기능; 본문 호출 표현 getOnBackInvokedDispatcher, registerOnBackInvokedCallback, OnBackInvokedCallback, onBackInvoked, KeyEvent.addKeyEvent, KeyEvent
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java#L145) **`onBackInvoked()`**: 이벤트·효과 실행; 본문 호출 표현 KeyEvent.addKeyEvent, KeyEvent
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java#L175) **`createAudio(Context context, AndroidApplicationConfiguration config)`**: 생성·초기화; 본문 호출 표현 AsynchronousAndroidAudio
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java#L180) **`onResume()`**: 이벤트·효과 실행; 조건 분기; 본문 호출 표현 finishAndRemoveTask, super.onResume
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java#L190) **`onBackPressed()`**: 이벤트·효과 실행
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java#L195) **`onWindowFocusChanged(boolean hasFocus)`**: 이벤트·효과 실행; 본문 호출 표현 super.onWindowFocusChanged, support.updateSystemUI
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java#L201) **`onMultiWindowModeChanged(boolean isInMultiWindowMode)`**: 이벤트·효과 실행; 본문 호출 표현 super.onMultiWindowModeChanged, support.updateSystemUI

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 3. [`AndroidMissingNativesHandler.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidMissingNativesHandler.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.android`; **본문:** 97행; **클래스·내부 타입:** 1개; **필드 후보:** 1개; **메서드 후보:** 1개.

### 타입 및 상속 선언
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidMissingNativesHandler.java#L33) `class AndroidMissingNativesHandler  extends Activity`

### 필드·상수
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidMissingNativesHandler.java#L35) `Throwable error`

### 메서드·기능 연결
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidMissingNativesHandler.java#L39) **`onCreate(Bundle savedInstanceState)`**: 이벤트·효과 실행; 조건 분기/반복/예외 처리; 본문 호출 표현 super.onCreate, getPackageManager, getPackageInfo, getPackageName, getInstallSourceInfo, getInstallingPackageName, getInstallerPackageName, TextView, developer

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 4. [`AndroidPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.android`; **본문:** 356행; **클래스·내부 타입:** 1개; **필드 후보:** 5개; **메서드 후보:** 13개.

### 타입 및 상속 선언
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L48) `class AndroidPlatformSupport  extends PlatformSupport`

### 필드·상수
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L201) `FreeTypeFontGenerator basicFontGenerator`
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L203) `FreeTypeFontGenerator KRFontGenerator`
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L205) `FreeTypeFontGenerator ZHFontGenerator`
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L207) `FreeTypeFontGenerator JPFontGenerator`
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L210) `boolean koreanAndroid6OTF` — 초기식: `false`

### 메서드·기능 연결
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L50) **`updateDisplaySize()`**: 시뮬레이션·주기 갱신; 본문 호출 표현 AndroidLauncher.instance.setRequestedOrientation, SPDSettings.landscape, ShatteredPixelDungeon.seamlessResetScene
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L58) **`supportsFullScreen()`**: 개별 기능; 조건 분기; 본문 호출 표현 AndroidLauncher.instance.getApplicationWindow, getDecorView, getRootWindowInsets, insets.getStableInsetBottom, insets.getStableInsetRight, insets.getStableInsetLeft
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L70) **`getDisplayCutout()`**: 조회·탐색; 조건 분기/반복; 본문 호출 표현 RectF, AndroidLauncher.instance.getApplicationWindow, getDecorView, getRootWindowInsets, getDisplayCutout, cutout.getBoundingRects, Math.abs, r.height, r.width
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L99) **`getSafeInsets(int level)`**: 조회·탐색; 조건 분기/반복; 본문 호출 표현 RectF, AndroidLauncher.instance.isInMultiWindowMode, AndroidLauncher.instance.getApplicationWindow, getDecorView, getRootWindowInsets, supportsFullScreen, SPDSettings.fullscreen, Math.max, rootInsets.getStableInsetLeft
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L156) **`updateSystemUI()`**: 시뮬레이션·주기 갱신; 조건 분기; 본문 호출 표현 AndroidLauncher.instance.runOnUiThread, Runnable, run, AndroidLauncher.instance.isInMultiWindowMode, AndroidLauncher.instance.getWindow, setFlags, supportsFullScreen, SPDSettings.fullscreen, getDecorView
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L160) **`run()`**: 개별 기능; 조건 분기; 본문 호출 표현 AndroidLauncher.instance.isInMultiWindowMode, AndroidLauncher.instance.getWindow, setFlags, supportsFullScreen, SPDSettings.fullscreen, getDecorView, setSystemUiVisibility
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L188) **`connectedToUnmeteredNetwork()`**: 개별 기능; 본문 호출 표현 AndroidLauncher.instance.getSystemService, isActiveNetworkMetered
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L194) **`supportsVibration()`**: 개별 기능
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L213) **`setupFontGenerators(int pageSize, boolean systemfont)`**: 생성·초기화; 조건 분기/분기 선택; 본문 호출 표현 resetGenerators, Gdx.files.absolute, exists, FreeTypeFontGenerator, Gdx.files.internal, SPDSettings.language
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L304) **`matcher("")`**: 개별 기능
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L306) **`matcher("")`**: 개별 기능
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L309) **`getGeneratorForString(String input)`**: 조회·탐색; 조건 분기; 본문 호출 표현 KRMatcher.reset, find, ZHMatcher.reset, JPMatcher.reset
- [L345](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java#L345) **`splitforTextBlock(String text, boolean multiline)`**: 개별 기능; 조건 분기; 본문 호출 표현 getGeneratorForString, android6KRSplitter.split, regularsplitterMultiline.split, regularsplitter.split

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 5. [`Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.actors`; **본문:** 403행; **클래스·내부 타입:** 1개; **필드 후보:** 17개; **메서드 후보:** 35개.

### 타입 및 상속 선언
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L37) `class Actor  implements Bundlable`

### 필드·상수
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L39) `float TICK` — 초기식: `1f`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L41) `float time`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L43) `int id` — 초기식: `0`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L48) `int VFX_PRIO` — 초기식: `100`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L49) `int HERO_PRIO` — 초기식: `0`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L50) `int BLOB_PRIO` — 초기식: `-10`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L51) `int MOB_PRIO` — 초기식: `-20`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L52) `int BUFF_PRIO` — 초기식: `-30`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L53) `int DEFAULT` — 초기식: `-100`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L56) `int actPriority` — 초기식: `DEFAULT`
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L120) `String TIME` — 초기식: `"time"`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L121) `String ID` — 초기식: `"id"`
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L154) `Actor current`
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L157) `int nextID` — 초기식: `1`
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L159) `float now` — 초기식: `0`
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L220) `String NEXTID` — 초기식: `"nextid"`
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L248) `boolean keepActorThreadAlive` — 초기식: `true`

### 메서드·기능 연결
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L58) **`act()`**: 시뮬레이션·주기 갱신
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L61) **`spendConstant(float time)`**: 개별 기능; 조건 분기; 본문 호출 표현 Math.abs, Math.round
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L71) **`spend(float time)`**: 개별 기능; 본문 호출 표현 spendConstant
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L75) **`spendToWhole()`**: 개별 기능; 본문 호출 표현 Math.ceil
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L79) **`postpone(float time)`**: 개별 기능; 조건 분기; 본문 호출 표현 Math.abs, Math.round
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L90) **`cooldown()`**: 개별 기능
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L94) **`clearTime()`**: 상태 조작; 조건 분기/반복; 본문 호출 표현 spendConstant, Actor.now, buffs, b.spendConstant
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L103) **`timeToNow()`**: 개별 기능
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L108) **`fixTime(float decrement)`**: 개별 기능
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L112) **`diactivate()`**: 개별 기능
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L116) **`onAdd()`**: 이벤트·효과 실행
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L118) **`onRemove()`**: 이벤트·효과 실행
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L124) **`storeInBundle(Bundle bundle)`**: 저장·복원; 본문 호출 표현 bundle.put
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L130) **`restoreFromBundle(Bundle bundle)`**: 저장·복원; 조건 분기; 본문 호출 표현 bundle.getFloat, bundle.getInt, Actor.findById
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L140) **`id()`**: 개별 기능; 조건 분기
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L161) **`now()`**: 개별 기능
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L165) **`clear()`**: 상태 조작; 본문 호출 표현 all.clear, chars.clear, ids.clear
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L175) **`fixTime()`**: 개별 기능; 조건 분기/반복; 본문 호출 표현 all.isEmpty, a.fixTime, TargetedCell.fixTime, all.contains
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L200) **`init()`**: 생성·초기화; 반복; 본문 호출 표현 add, mob.restoreEnemy, level.blobs.values
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L222) **`storeNextID(Bundle bundle)`**: 저장·복원; 본문 호출 표현 bundle.put
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L226) **`restoreNextID(Bundle bundle)`**: 저장·복원; 본문 호출 표현 bundle.getInt
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L230) **`resetNextID()`**: 생성·초기화
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L240) **`processing()`**: 시뮬레이션·주기 갱신
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L244) **`curActorPriority()`**: 개별 기능
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L250) **`process()`**: 시뮬레이션·주기 갱신; 조건 분기/반복/예외 처리; 본문 호출 표현 Game.switchingScene, synchronized, sprite.wait, Thread.interrupted, acting.act, Dungeon.hero.isAlive, Thread.currentThread, notify, wait
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L311) **`currentThread())`**: 개별 기능; 조건 분기/예외 처리; 본문 호출 표현 Thread.interrupted, Thread.currentThread, notify, wait
- [L334](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L334) **`add(Actor actor)`**: 상태 조작; 본문 호출 표현 add
- [L338](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L338) **`addDelayed(Actor actor, float delay)`**: 상태 조작; 본문 호출 표현 add, Math.max
- [L342](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L342) **`add(Actor actor, float time)`**: 상태 조작; 조건 분기/반복; 본문 호출 표현 all.contains, ids.put, actor.id, all.add, actor.onAdd, chars.add, ch.buffs, add
- [L363](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L363) **`remove(Actor actor)`**: 상태 조작; 조건 분기; 본문 호출 표현 all.remove, chars.remove, actor.onRemove, ids.remove
- [L378](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L378) **`delayChar(Char ch, float time)`**: 개별 기능; 반복; 본문 호출 표현 ch.spendConstant, ch.buffs, b.spendConstant
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L385) **`findChar(int pos)`**: 조회·탐색; 조건 분기/반복
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L393) **`findById(int id)`**: 조회·탐색; 본문 호출 표현 ids.get
- [L397](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L397) **`all()`**: 개별 기능
- [L401](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L401) **`chars()`**: 개별 기능

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 6. [`Alchemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Alchemy.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.actors.blobs`; **본문:** 64행; **클래스·내부 타입:** 1개; **필드 후보:** 1개; **메서드 후보:** 3개.

### 타입 및 상속 선언
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Alchemy.java#L29) `class Alchemy  extends Blob`

### 필드·상수
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Alchemy.java#L35) `int pos`

### 메서드·기능 연결
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Alchemy.java#L38) **`landmark()`**: 개별 기능
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Alchemy.java#L43) **`evolve()`**: 시뮬레이션·주기 갱신; 조건 분기/반복; 본문 호출 표현 Dungeon.level.width, Dungeon.level.insideMap
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Alchemy.java#L58) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행; 본문 호출 표현 super.use, emitter.start, Speck.factory

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 7. [`Blizzard.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blizzard.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.actors.blobs`; **본문:** 77행; **클래스·내부 타입:** 1개; **필드 후보:** 0개; **메서드 후보:** 3개.

### 타입 및 상속 선언
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blizzard.java#L29) `class Blizzard  extends Blob`

### 필드·상수
- 단일 행 필드 패턴 없음

### 메서드·기능 연결
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blizzard.java#L32) **`evolve()`**: 시뮬레이션·주기 갱신; 조건 분기/반복; 본문 호출 표현 super.evolve, level.blobs.get, Dungeon.level.width, fire.clear, freeze.clear, inf.clear, Freezing.freeze
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blizzard.java#L65) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행; 본문 호출 표현 super.use, emitter.pour, Speck.factory
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blizzard.java#L71) **`tileDesc()`**: 개별 기능; 본문 호출 표현 Messages.get

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 8. [`Blob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.actors.blobs`; **본문:** 284행; **클래스·내부 타입:** 1개; **필드 후보:** 8개; **메서드 후보:** 18개.

### 타입 및 상속 선언
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L35) `class Blob  extends Actor`

### 필드·상수
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L41) `int volume` — 초기식: `0`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L43) `int[] cur`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L44) `int[] off`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L46) `BlobEmitter emitter`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L50) `boolean alwaysVisible` — 초기식: `false`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L52) `String CUR` — 초기식: `"cur"`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L53) `String START` — 초기식: `"start"`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L54) `String LENGTH` — 초기식: `"length"`

### 메서드·기능 연결
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L48) **`Rect()`**: 개별 기능
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L57) **`storeInBundle(Bundle bundle)`**: 저장·복원; 조건 분기/반복; 본문 호출 표현 super.storeInBundle, Dungeon.level.length, bundle.put, trim
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L82) **`trim(int start, int end)`**: 개별 기능; 본문 호출 표현 System.arraycopy
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L90) **`restoreFromBundle(Bundle bundle)`**: 저장·복원; 조건 분기/반복; 본문 호출 표현 super.restoreFromBundle, bundle.contains, bundle.getInt, bundle.getIntArray
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L112) **`act()`**: 시뮬레이션·주기 갱신; 조건 분기/반복; 본문 호출 표현 spend, area.isEmpty, setupArea, evolve, Dungeon.level.updateCellFlags, cellsToFlagUpdate.clear, area.setEmpty, System.arraycopy
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L144) **`setupArea()`**: 생성·초기화; 조건 분기/반복; 본문 호출 표현 area.union, Dungeon.level.width
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L152) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L156) **`evolve()`**: 시뮬레이션·주기 갱신; 조건 분기/반복; 본문 호출 표현 Dungeon.level.width, Dungeon.level.insideMap
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L209) **`seed(Level level, int cell, int amount)`**: 개별 기능; 조건 분기; 본문 호출 표현 level.length, area.union, level.width
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L219) **`clear(int cell)`**: 상태 조작; 조건 분기
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L225) **`fullyClear()`**: 개별 기능; 본문 호출 표현 area.setEmpty, Dungeon.level.length
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L232) **`onBuildFlagMaps(Level l)`**: 이벤트·효과 실행
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L236) **`onUpdateCellFlags(Level l, int cell)`**: 이벤트·효과 실행
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L242) **`landmark()`**: 개별 기능
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L246) **`tileDesc()`**: 개별 기능
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L250) **`seed(int cell, int amount, Class<T> type)`**: 개별 기능; 본문 호출 표현 seed
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L255) **`seed(int cell, int amount, Class<T> type, Level level)`**: 개별 기능; 조건 분기; 본문 호출 표현 level.blobs.get, Reflection.newInstance, Actor.curActorPriority, gas.spend, level.blobs.put, gas.seed
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L275) **`volumeAt(int cell, Class<? extends Blob> type)`**: 개별 기능; 조건 분기; 본문 호출 표현 level.blobs.get

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 9. [`ConfusionGas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ConfusionGas.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.actors.blobs`; **본문:** 65행; **클래스·내부 타입:** 1개; **필드 후보:** 0개; **메서드 후보:** 3개.

### 타입 및 상속 선언
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ConfusionGas.java#L33) `class ConfusionGas  extends Blob`

### 필드·상수
- 단일 행 필드 패턴 없음

### 메서드·기능 연결
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ConfusionGas.java#L36) **`evolve()`**: 시뮬레이션·주기 갱신; 조건 분기/반복; 본문 호출 표현 super.evolve, Dungeon.level.width, Actor.findChar, ch.isImmune, this.getClass, Buff.prolong
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ConfusionGas.java#L55) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행; 본문 호출 표현 super.use, emitter.pour, Speck.factory
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ConfusionGas.java#L62) **`tileDesc()`**: 개별 기능; 본문 호출 표현 Messages.get

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 10. [`CorrosiveGas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.actors.blobs`; **본문:** 106행; **클래스·내부 타입:** 1개; **필드 후보:** 4개; **메서드 후보:** 7개.

### 타입 및 상속 선언
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java#L34) `class CorrosiveGas  extends Blob`

### 필드·상수
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java#L37) `int strength` — 초기식: `0`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java#L40) `Class source`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java#L77) `String STRENGTH` — 초기식: `"strength"`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java#L78) `String SOURCE` — 초기식: `"source"`

### 메서드·기능 연결
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java#L43) **`evolve()`**: 시뮬레이션·주기 갱신; 조건 분기/반복; 본문 호출 표현 super.evolve, Dungeon.level.width, Actor.findChar, ch.isImmune, this.getClass, Buff.affect, set
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java#L65) **`setStrength(int str)`**: 상태 조작; 본문 호출 표현 setStrength
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java#L69) **`setStrength(int str, Class source)`**: 상태 조작; 조건 분기
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java#L81) **`restoreFromBundle(Bundle bundle)`**: 저장·복원; 본문 호출 표현 super.restoreFromBundle, bundle.getInt, bundle.getClass
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java#L88) **`storeInBundle(Bundle bundle)`**: 저장·복원; 본문 호출 표현 super.storeInBundle, bundle.put
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java#L95) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행; 본문 호출 표현 super.use, emitter.pour, Speck.factory
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/CorrosiveGas.java#L102) **`tileDesc()`**: 개별 기능; 본문 호출 표현 Messages.get

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 11. [`Electricity.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.actors.blobs`; **본문:** 130행; **클래스·내부 타입:** 1개; **필드 후보:** 1개; **메서드 후보:** 4개.

### 타입 및 상속 선언
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java#L40) `class Electricity  extends Blob`

### 필드·상수
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java#L47) `boolean[] water`

### 메서드·기능 연결
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java#L50) **`evolve()`**: 시뮬레이션·주기 갱신; 조건 분기/반복; 본문 호출 표현 Dungeon.level.width, spreadFromCell, Actor.findChar, ch.isImmune, this.getClass, ch.buff, Buff.prolong, ch.damage, Math.round
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java#L105) **`spreadFromCell(int cell, int power)`**: 개별 기능; 조건 분기/반복; 본문 호출 표현 area.union, Dungeon.level.width, Math.max, spreadFromCell
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java#L119) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행; 본문 호출 표현 super.use, emitter.start
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java#L125) **`tileDesc()`**: 개별 기능; 본문 호출 표현 Messages.get

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 12. [`Fire.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.actors.blobs`; **본문:** 127행; **클래스·내부 타입:** 1개; **필드 후보:** 0개; **메서드 후보:** 4개.

### 타입 및 상속 선언
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java#L36) `class Fire  extends Blob`

### 필드·상수
- 단일 행 필드 패턴 없음

### 메서드·기능 연결
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java#L39) **`evolve()`**: 시뮬레이션·주기 갱신; 조건 분기/반복; 본문 호출 표현 level.blobs.get, Dungeon.level.width, freeze.clear, burn, Dungeon.level.destroy, GameScene.updateMap, area.union, Dungeon.observe
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java#L99) **`burn(int pos)`**: 개별 기능; 조건 분기; 본문 호출 표현 Actor.findChar, ch.isImmune, Buff.affect, reignite, level.heaps.get, heap.burn, level.plants.get, plant.wither
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java#L117) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행; 본문 호출 표현 super.use, emitter.pour
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java#L123) **`tileDesc()`**: 개별 기능; 본문 호출 표현 Messages.get

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 13. [`Foliage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Foliage.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.actors.blobs`; **본문:** 106행; **클래스·내부 타입:** 1개; **필드 후보:** 0개; **메서드 후보:** 4개.

### 타입 및 상속 선언
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Foliage.java#L37) `class Foliage  extends Blob`

### 필드·상수
- 단일 행 필드 패턴 없음

### 메서드·기능 연결
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Foliage.java#L40) **`landmark()`**: 개별 기능
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Foliage.java#L45) **`evolve()`**: 시뮬레이션·주기 갱신; 조건 분기/반복; 본문 호출 표현 level.blobs.get, Dungeon.level.width, Level.set, GameScene.updateMap, hero.isAlive, Buff.affect, s.prolong
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Foliage.java#L96) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행; 본문 호출 표현 super.use, emitter.start
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Foliage.java#L102) **`tileDesc()`**: 개별 기능; 본문 호출 표현 Messages.get

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 14. [`Freezing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.actors.blobs`; **본문:** 142행; **클래스·내부 타입:** 1개; **필드 후보:** 0개; **메서드 후보:** 5개.

### 타입 및 상속 선언
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java#L37) `class Freezing  extends Blob`

### 필드·상수
- 단일 행 필드 패턴 없음

### 메서드·기능 연결
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java#L40) **`evolve()`**: 시뮬레이션·주기 갱신; 조건 분기/반복; 본문 호출 표현 level.blobs.get, Dungeon.level.width, fire.clear, Freezing.freeze
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java#L68) **`freeze(int cell)`**: 개별 기능; 조건 분기; 본문 호출 표현 Actor.findChar, ch.isImmune, ch.buff, Buff.affect, chill.cooldown, ch.resist, Math.min, level.heaps.get, heap.freeze
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java#L97) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행; 본문 호출 표현 super.use, emitter.start
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java#L103) **`tileDesc()`**: 개별 기능; 본문 호출 표현 Messages.get
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java#L108) **`affect(int cell)`**: 개별 기능; 조건 분기; 본문 호출 표현 Actor.findChar, Buff.prolong, level.blobs.get, fire.clear, eternalFire.clear, level.heaps.get, heap.freeze, CellEmitter.get, start

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 15. [`GooWarn.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/GooWarn.java)

**패키지:** `com.shatteredpixel.shatteredpixeldungeon.actors.blobs`; **본문:** 86행; **클래스·내부 타입:** 1개; **필드 후보:** 1개; **메서드 후보:** 4개.

### 타입 및 상속 선언
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/GooWarn.java#L30) `class GooWarn  extends Blob`

### 필드·상수
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/GooWarn.java#L40) `int pos`

### 메서드·기능 연결
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/GooWarn.java#L43) **`evolve()`**: 시뮬레이션·주기 갱신; 조건 분기/반복; 본문 호출 표현 Dungeon.level.width
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/GooWarn.java#L61) **`seed(Level level, int cell, int amount)`**: 개별 기능; 조건 분기; 본문 호출 표현 level.length, area.union, level.width
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/GooWarn.java#L75) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행; 본문 호출 표현 super.use, emitter.pour
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/GooWarn.java#L81) **`tileDesc()`**: 개별 기능; 본문 호출 표현 Messages.get

**의미 해설:** 위 메서드 분류는 이름·본문 코드 패턴에 의존하는 **정적 분석 후보**이며, 참조 객체의 실제 타입과 조건부 실행은 코드 전체/테스트 확인이 필요함.

## 검사 범위

접근 성공 15개 / 실패 0개, 타입 후보 15, 필드 후보 40, 메서드 후보 116. 이 문서는 **자동 추출 결과**이며 모든 호출의 의미를 사람이 검증했다는 주장은 하지 않는다.

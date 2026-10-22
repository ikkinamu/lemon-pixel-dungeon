# 플랫폼 실행·빌드·뉴스·업데이트

## 1. 빌드 기준 값
분석 대상 [build.gradle](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/build.gradle)의 확인된 속성:
- appName = Shattered Pixel Dungeon
- appPackageName = com.shatteredpixel.shatteredpixeldungeon
- appVersionName = 4.0.2, appVersionCode = 922
- appJavaCompatibility = JavaVersion.VERSION_11
- appAndroidCompileSDK = 36, appAndroidTargetSDK = 36, appAndroidMinSDK = 21
- gdxVersion = 1.14.0, gdxControllersVersion = 2.2.4, robovmVersion = 2.3.24

**주의:** Gradle의 Java 11 소스 호환 설정과 데스크톱 패키징용 Java 런타임 버전 17 지정은 서로 다른 설정이다. 실제 지원 대상의 정확한 전체 범위는 빌드/실행 테스트로 별도 확인해야 한다.

## 2. 진입점
| 플랫폼 | 확인된 코드와 역할 |
|---|---|
| Desktop | [desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java:35-90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java#L35-L90): main(), JVM 환경 검증, OS 환경/창 설정, libGDX LWJGL3 앱 |
| Android | [android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java:54-62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java#L54-L62): AndroidApplication 기반 onCreate |
| iOS | [ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java:54-56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java#L54-L56): IOSApplication.Delegate 및 iOS 앱 구성 |

플랫폼별 Display, safe area, 글꼴, 진동, 네트워크 관련 동작은 PlatformSupport 구현에 위임:
- [desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java)
- [android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java)
- [ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java) (파일 경로 확인; 상세 메서드 미분석)

## 3. 패키징
- [desktop/build.gradle](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/build.gradle): mainClass=DesktopLauncher, core 및 desktop 자산 복사, debug/release/jpackage 관련 작업.
- [android/build.gradle](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/build.gradle): core 의존성, Android 네이티브 자산, debug/release별 서비스 구현 선택, release의 R8 설정.
- [ios/build.gradle](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/build.gradle): RoboVM, iOS용 앱 properties 작성, core 및 서비스 종속성, iOS 그래픽 백엔드 버전 별도 지정.
- iOS build.gradle에는 **일부 기기에서 최신 백엔드 충돌을 피하기 위해 MetalANGLE 1.13.1을 사용**한다는 주석이 있다. 이 주석만으로 실제 현재 하드웨어 호환성이 검증되었다고 보아서는 안 된다.

## 4. 서비스 의존성 주입
[services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsService.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsService.java)는 checkForArticles()와 응답 콜백의 추상 인터페이스.
[services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateService.java)는 업데이트 확인·다운로드/리뷰 진입 인터페이스.
- [services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/ShatteredNews.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/ShatteredNews.java): 뉴스 HTTP 요청 구현.
- [services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java): GitHub 기반 버전 확인 구현.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/Updates.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/Updates.java): UI/공통 로직에서 이용하는 정적 서비스 경유 계층.

News.service와 Updates.service는 플랫폼 런처가 지원되는 실제 구현을 주입하는 구조. 'services가 인터넷 없는 환경에서 프로그램 전체의 실행을 막는다'는 결론은 이 파일만으로 성립하지 않는다.

## 5. 라이선스·포크 구분
저장소 API에서 fork=true, 원본 상위 저장소는 00-Evan/shattered-pixel-dungeon으로 확인됨.
현재 포크가 원본과 어떤 기능적 차이를 갖는지는 비교(diff)를 별도로 수행하지 않았으므로 **Lemon 고유 기능이 있다고 추측하지 않는다**.

## 6. 빌드 검증의 한계
- 이 문서 작성은 GitHub API를 통한 정적 분석이며 Gradle 컴파일·기기 실행·테스트를 수행하지 않음.
- 추후 검증 지점: Gradle wrapper, Android SDK / JDK / iOS toolchain, 의존성 다운로드, 실행 환경의 네이티브 라이브러리.

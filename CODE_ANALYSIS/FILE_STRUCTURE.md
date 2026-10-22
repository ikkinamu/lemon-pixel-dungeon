# 파일 및 모듈 구조

## Gradle 모듈 (settings.gradle에서 확인)
```text
/
├── SPD-classes/             # 공통 기반 클래스 모듈
├── core/                    # 게임 공통 로직
├── android/                 # Android 플랫폼 모듈
├── ios/                     # iOS 플랫폼 모듈
├── desktop/                 # 데스크톱 플랫폼 모듈
├── services/                # 서비스 모듈
│   ├── updates/
│   │   ├── debugUpdates/
│   │   └── githubUpdates/
│   └── news/
│       ├── debugNews/
│       └── shatteredNews/
├── docs/                    # 기존 개발 안내 문서
├── settings.gradle
├── build.gradle
└── CODE_ANALYSIS/           # 추가된 분석 문서
```

위 트리는 `settings.gradle`의 선언과 확인된 경로를 요약한 것이며, 전체 파일 트리의 완전한 열거가 아닙니다.

## 대표 Java 파일
| 경로 (core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ 기준) | 역할 |
|---|---|
| ShatteredPixelDungeon.java | 게임 인스턴스 초기화, 오디오 설정, 장면 전환, 화면 크기 및 시스템 UI |
| Dungeon.java | 던전 진행 상태와 한정 드롭 관리 등 |
| SPDSettings.java | 설정 키와 설정 값의 읽기/쓰기 |
| actors/Actor.java | 액터의 시간·우선순위·식별자 및 저장/복원 기반 |
| scenes/GameScene.java | 게임 장면과 여러 UI/월드 구성 요소를 연결 |

데스크톱 진입점: `desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java`.

## 빌드 설정에서 확인한 내용
루트 `build.gradle`에는 `appVersionName = '4.0.2'`, `appVersionCode = 922`, Java 11 호환성, libGDX 1.14.0이 지정되어 있습니다. 이 값들은 분석 당시 읽은 파일의 값입니다.

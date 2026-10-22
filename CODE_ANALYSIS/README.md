# Lemon Pixel Dungeon 코드 분석 안내

대상: `ikkinamu/lemon-pixel-dungeon`, 기본 브랜치 `master`.
이 폴더는 실행되지 않는 설명용 Markdown 문서만 포함합니다. 기존 소스 코드와 빌드 설정을 수정하지 않습니다.

## 범위와 정확도
이 문서는 저장소의 `README.md`, `settings.gradle`, `build.gradle`, `core/build.gradle` 및 주요 Java 소스 파일을 직접 읽어 작성한 **1차 분석**입니다. 모든 소스 파일과 모든 변수/메서드를 전수 조사한 문서는 아닙니다. 확인된 사실과 추후 확인이 필요한 사항을 구분합니다.

- [파일 구조](FILE_STRUCTURE.md)
- [변수 및 상수](VARIABLES.md)
- [함수 및 메서드](FUNCTIONS.md)
- [클래스](CLASSES.md)
- [실행 흐름](EXECUTION_FLOW.md)
- [의존 관계](DEPENDENCIES.md)

## 분석한 대표 소스
- `settings.gradle`, `build.gradle`, `core/build.gradle`
- `core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java`
- `core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`
- `core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java`
- `core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`
- `core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`
- `desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java`

이 문서의 설명은 읽은 소스 범위와 시점에 한정됩니다. 실행 테스트는 수행하지 않았습니다.

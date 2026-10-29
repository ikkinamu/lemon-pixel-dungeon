# 분석 문서 시작점

## 전체 Java 소스 원문 분석 (신규)

[25_FULL_SOURCE_ANALYSIS.md](25_FULL_SOURCE_ANALYSIS.md)에서 정적 분석 완료 범위와 확인되지 않은 의미를 구분한다. [COMPLETE_JAVA/00_README.md](COMPLETE_JAVA/00_README.md)에는 전체 1,323개 Java의 본문 기반 분석 문서 79개가 연결된다. 기존 시스템별 해설은 그보다 직접 확인한 실행 경로를 우선 제공한다.


저장소: [ikkinamu/lemon-pixel-dungeon](https://github.com/ikkinamu/lemon-pixel-dungeon)  
소스 분석 기준: bd3a990254e4249458816f4879e93ab87275555b  
코드 수정: 없음. 이 폴더에 설명 Markdown만 추가.

## 분석의 층위
**전체 트리 인벤토리**는 모든 파일명을 수집한 결과이고 **심층 해설**은 주요 클래스의 실제 코드 독해이며 **선언 색인**은 대표 Java 파일에서 정규식으로 추출한 필드/메서드 후보 목록이다. 세 가지의 정확성 범위를 혼동하지 않기를 권장한다.

## 추천 읽기 순서
1. [10_ARCHITECTURE.md](10_ARCHITECTURE.md): 전체 구조와 모듈
2. [11_TURNS_ACTORS_COMBAT.md](11_TURNS_ACTORS_COMBAT.md): 시간·AI·전투
3. [12_LEVEL_WORLD_GENERATION.md](12_LEVEL_WORLD_GENERATION.md): 절차 생성과 맵
4. [13_ITEMS_EQUIPMENT_LOOT.md](13_ITEMS_EQUIPMENT_LOOT.md): 아이템·드롭
5. [14_SAVE_RESTORE_SEED.md](14_SAVE_RESTORE_SEED.md): 저장·시드
6. [15_SCENES_UI_INPUT_THREADS.md](15_SCENES_UI_INPUT_THREADS.md): 화면·입력·스레드
7. [16_PLATFORM_BUILD_SERVICES.md](16_PLATFORM_BUILD_SERVICES.md): 빌드·플랫폼·서비스
8. [17_ASSETS_LOCALIZATION.md](17_ASSETS_LOCALIZATION.md): 그래픽·메시지·글꼴
9. [18_PROGRESS_STATS_META.md](18_PROGRESS_STATS_META.md): 성장·도전·기록
10. [19_AMBIGUITY_AND_INTERPRETATION.md](19_AMBIGUITY_AND_INTERPRETATION.md): 자주 헷갈리는 개념
11. [20_GLOSSARY.md](20_GLOSSARY.md): 용어집
12. [21_COVERAGE_LIMITS_NEXT_STEPS.md](21_COVERAGE_LIMITS_NEXT_STEPS.md): 검증 범위/잔여 작업
13. [22_ADDENDUM_MECHANICS.md](22_ADDENDUM_MECHANICS.md): 특수 물리·환경·지형

## 완전 파일 목록 및 패키지 지도
- [00_SCOPE_AND_COUNTS.md](00_SCOPE_AND_COUNTS.md): 전체 파일 수·분포
- [01_JAVA_INDEX_ACTORS.md](01_JAVA_INDEX_ACTORS.md)
- [02_JAVA_INDEX_ITEMS.md](02_JAVA_INDEX_ITEMS.md)
- [03_JAVA_INDEX_LEVELS.md](03_JAVA_INDEX_LEVELS.md)
- [04_JAVA_INDEX_PRESENTATION.md](04_JAVA_INDEX_PRESENTATION.md)
- [05_JAVA_INDEX_OTHER.md](05_JAVA_INDEX_OTHER.md)
- [06_JAVA_INDEX_PLATFORM.md](06_JAVA_INDEX_PLATFORM.md)
- [07_PACKAGE_MAP.md](07_PACKAGE_MAP.md): 모든 Java 소스 디렉터리 및 파일 수

## 대표 클래스의 선언 색인
- [선언 색인 폴더](DECLARATIONS/)에 엔진/액터/아이템/맵/UI/특수 시스템/플랫폼/서비스 영역별 8개 파일.
- 한 줄 단위 자동 수집이므로 AST/타입 분석의 완전한 결과로 해석하지 말 것.

## 신뢰도
- 소스 링크는 분석 당시 커밋에 고정되어 재현 가능.
- '직접 확인'과 '해석', '아직 미검증'을 구분.
- Gradle 빌드·실제 플레이·버전 호환 자동 테스트는 수행하지 않았음.

# 내부 코드·파일 연결관계 문서 안내

**종합 설명:** [23_CODE_FILE_RELATIONSHIPS.md](../23_CODE_FILE_RELATIONSHIPS.md)  
**분석 원본 코드:** `bd3a990254e4249458816f4879e93ab87275555b`. 모든 링크/통계는 정적 코드 분석 기준이며 기존 프로젝트의 실행 코드를 수정하지 않는다.

## 문서 구분

| 문서 | 연결 방향 | 관계 유형 |
|---|---|---|
| [01_CORE_STATE.md](01_CORE_STATE.md) | 전역 상태/설정 파일 → 가져오는 내부 Java 파일 | IMPORT |
| [02_ACTORS_AI.md](02_ACTORS_AI.md) | 액터·영웅·AI·버프 → 내부 Java 파일 | IMPORT |
| [03_LEVELS_GENERATION.md](03_LEVELS_GENERATION.md) | 층·방·생성 관련 파일 → 내부 Java 파일 | IMPORT |
| [04_ITEMS_LOOT.md](04_ITEMS_LOOT.md) | 아이템·드롭 관련 파일 → 내부 Java 파일 | IMPORT |
| [05_SCENES_UI.md](05_SCENES_UI.md) | 장면·UI → 내부 Java 파일 | IMPORT |
| [06_PLATFORM_ENGINE_SERVICES.md](06_PLATFORM_ENGINE_SERVICES.md) | 엔진·플랫폼·서비스 → 내부 Java 파일 | IMPORT |
| [07_MODULE_DEPENDENCIES.md](07_MODULE_DEPENDENCIES.md) | Gradle 모듈·리소스 | MODULE/ASSET |
| [08_REVERSE_REFERENCE_INDEX.md](08_REVERSE_REFERENCE_INDEX.md) | 내부 파일 ← 표본 내 해당 파일을 import하는 Java 파일 | REVERSE |
| [09_CALL_CHAINS.md](09_CALL_CHAINS.md) | 실제 호출/상태 전달을 추적한 흐름 | CALL/DATA/ASYNC |
| [10_INHERITANCE_COMPOSITION.md](10_INHERITANCE_COMPOSITION.md) | 클래스 상속·인터페이스·객체 보유 | INHERIT/COMPOSITION |

### 자료 신뢰성
- 전체 Git Tree를 수집한 1,323개 Java 파일 **경로**와 개별 소스 본문을 읽은 98개 Java 파일 **연결 표본**은 다르다.
- 표본 내 실제 import 관계: 2,608개(출발과 대상 중복 제거), 대상 파일 759개.
- 상위 저장소 기능이 포크와 동일하다고 추정하지 않고, 지정된 포크의 코드만 직접 열람했다.
- 전체 파일의 실제 호출 그래프·컴파일러 기반 타입 결합 결과는 아님.

### 빠른 탐색
- *내 파일이 의존하는 파일*: 01~06.
- *내 파일을 참조하는 파일*: 08. **98개 출발 파일에 제한된 통계**.
- *특정 기능이 여러 파일을 거치는 과정*: 09.
- *클래스가 무엇을 상속하거나 구현하는지*: 10.
- *Android/Desktop/iOS가 어떤 모듈을 조합하는지*: 07.

변수 이름 및 범위 오해는 [19_AMBIGUITY_AND_INTERPRETATION.md](../19_AMBIGUITY_AND_INTERPRETATION.md)와 함께 확인한다.

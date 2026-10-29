# 실제 소스 구현 분석 — 목차 및 범위

**전체 1,323개 Java 파일의 본문 기반 정적 색인**은 [../COMPLETE_JAVA/00_README.md](../COMPLETE_JAVA/00_README.md)에서 확인할 수 있다. 아래의 134개 파일 수는 이 `IMPLEMENTATION/` 하위 문서에서 별도로 자세히 검토한 고유 파일 수이며, 저장소 전체 본문 열람 수를 뜻하지 않는다.


원본 코드 스냅샷: `d6f487f29ae86d0da317e088e5ad81d52378bc5b`. 이 폴더의 문서들은 소스 파일 내용을 직접 불러와 **메서드 후보, 필드, 클래스 선언, 인접 호출 관계**를 정리한 것이다. 파일명만으로 분류한 전수 역할 목록은 별도의 [ALL_FILE_ROLES](../ALL_FILE_ROLES/)에 있고, 두 자료의 신뢰도를 혼동하면 안 된다.

## 구현 분석 문서

| 문서 | 주요 내용 | 실제 읽은 파일 수 |
|---|---|---:|
| [01_LARGE_SYSTEMS.md](01_LARGE_SYSTEMS.md) | 대형 보스·복잡한 게임 시스템 | 13 |
| [02_MONSTER_CLASSES.md](02_MONSTER_CLASSES.md) | 일반 몬스터 종류와 AI | 16 |
| [03_ITEMS_CONSUMABLES.md](03_ITEMS_CONSUMABLES.md) | 물약·주문서·장비·유물 | 16 |
| [04_LEVEL_VARIANTS.md](04_LEVEL_VARIANTS.md) | 지역별 층 생성·방·함정 | 15 |
| [05_UI_WINDOWS_EVENTS.md](05_UI_WINDOWS_EVENTS.md) | 장면·창·UI 입력 | 15 |
| [06_ENGINE_FRAMEWORK.md](06_ENGINE_FRAMEWORK.md) | Noosa 프레임워크·저장·경로 탐색 | 15 |
| [07_CORE_GAMEPLAY.md](07_CORE_GAMEPLAY.md) | 전역 상태·턴·전투·저장 | 16 |
| [08_BUFF_BLOBS_PLANTS.md](08_BUFF_BLOBS_PLANTS.md) | 상태 효과·환경 효과·식물 | 16 |
| [09_MECHANICS_WORLD_RENDER.md](09_MECHANICS_WORLD_RENDER.md) | 지형·탄도·시각화 | 13 |

문서별 읽기 횟수 합계 135건, 중복 파일 제거 후 **134개 고유 Java 파일**. **전체 Java 파일 1323개 중 약 10.1%**에 해당한다.

## 검증 상태 구분

1. **소스 본문 열람:** 해당 .java를 실제로 불러와 클래스/필드/메서드의 선언과 표현을 확인했음. 그러나 단순 정규식 기반 분석이므로 완전 AST나 모든 분기 검증과 동일하지 않다.
2. **파일 경로/명칭 분류:** 전체 Java 1323개의 이름과 디렉터리로 예상 역할을 분류했지만 해당 파일의 본문을 확인하지 않았을 수 있다.
3. **실행 시 기능 검증:** 이 분석 작업에서는 하지 않았음. Gradle 빌드, 동작·성능·재현성·세이브 호환성은 보증하지 않음.
4. **구현 해석:** 각 문서의 기능 열은 함수 선언명과 인접 코드에서 해석한 단서다. 정적 코드에서 직접 확인되지 않은 인과관계를 단정하지 않는다.

모든 1,323개 소스 파일의 호출 그래프 및 메서드별 의미가 검증된 것은 아니다. 정확한 전체 분석이라고 주장하려면 모든 본문/타입 바인딩/메서드 내부를 후속으로 분석해야 한다.

## 사용 방법

1. [전체 상태 목록](00_VERIFICATION_STATUS.md)에서 파일을 찾고 **본문 열람 여부**를 확인.
2. **열람됨**이면 해당 구현 분석 문서에서 메서드 줄 번호로 이동.
3. **경로만 수집**이면 ALL_FILE_ROLES의 역할은 어디까지나 **추정**임.
4. 실제 호출자/피호출 관계는 [RELATIONSHIPS](../RELATIONSHIPS/)에서 정적 import / 수동 호출 추적을 구별해 참고.

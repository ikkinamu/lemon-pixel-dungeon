# 주요 변수·상수

**범위:** 아래는 실제로 확인한 일부 선언의 목록이며, 프로젝트 전체 변수 목록이 아닙니다.

| 클래스 | 이름 | 선언형 | 의미 |
|---|---|---|---|
| ShatteredPixelDungeon | v1_2_3 | public static final int | 구버전 랭킹 점수 방식 호환용 버전 코드(628) |
| ShatteredPixelDungeon | v3_1_1 | public static final int | 오래된 세이브 호환성 기준 코드(850) |
| ShatteredPixelDungeon | v4_0_0 | public static final int | 버전 코드 기준(911) |
| Actor | TICK | public static final float | 액터 기본 시간 단위(1f) |
| Actor | time | private float | 개별 액터의 시간 |
| Actor | id | private int | 개별 액터 식별자 |
| Actor | actPriority | protected int | 시간이 같을 때의 행동 우선순위 |
| Actor | VFX_PRIO | protected static final int | 시각 효과 우선순위(100) |
| Actor | HERO_PRIO | protected static final int | 영웅 기준 우선순위(0) |
| Actor | BLOB_PRIO | protected static final int | 환경 효과 우선순위(-10) |
| Actor | MOB_PRIO | protected static final int | 몬스터 우선순위(-20) |
| Actor | BUFF_PRIO | protected static final int | 버프 우선순위(-30) |
| Actor | all | private static HashSet<Actor> | 액터 집합 |
| Actor | chars | private static HashSet<Char> | 캐릭터 집합 |
| Actor | current | private static volatile Actor | 현재 액터 참조 |
| Actor | ids | private static SparseArray<Actor> | ID 기반 액터 조회 구조 |
| Actor | nextID | private static int | 다음 ID 값(초깃값 1) |
| Actor | now | private static float | 액터 스케줄 기준 현재 시간 |
| GameScene | scene | static GameScene | 게임 장면 참조 |
| SPDSettings | KEY_FULLSCREEN | public static final String | 전체 화면 설정 키(`fullscreen`) |
| SPDSettings | KEY_LANDSCAPE | public static final String | 화면 방향 설정 키(`force_landscape`) |
| SPDSettings | KEY_ZOOM | public static final String | 확대 설정 키(`zoom`) |
| SPDSettings | KEY_BRIGHTNESS | public static final String | 밝기 설정 키(`brightness`) |
| SPDSettings | KEY_GRID | public static final String | 시각 격자 설정 키(`visual_grid`) |
| Dungeon.LimitedDrops | count | public int | 한정 드롭 항목별 발생 횟수 |

참고: `Actor.TIME`, `Actor.ID`는 Bundle 저장/복원에 사용하는 문자열 키입니다. `Dungeon.LimitedDrops`의 열거 항목은 한정 드롭의 종류를 정의합니다.

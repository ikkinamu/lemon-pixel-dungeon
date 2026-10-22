# 주요 함수·메서드

**범위:** 직접 읽은 대표 소스의 일부 메서드입니다. 전체 함수 목록은 아닙니다.

| 클래스 | 메서드 | 확인된 동작 |
|---|---|---|
| DesktopLauncher | main(String[] args) | 데스크톱 실행 시작, JVM 상태 검증, 플랫폼 환경 설정, 서비스 초기화와 창 구성 |
| ShatteredPixelDungeon | ShatteredPixelDungeon(PlatformSupport) | 초기 장면 지정 및 구버전 클래스 별칭 등록 |
| ShatteredPixelDungeon | create() | 부모 초기화, 시스템 UI 갱신, 입력 바인딩 및 음악/효과음 설정 |
| ShatteredPixelDungeon | finish() | iOS에서는 종료 대신 타이틀 장면으로 이동 |
| ShatteredPixelDungeon | switchNoFade(...) | 페이드 없이 장면 전환 |
| ShatteredPixelDungeon | seamlessResetScene(...) | 장면의 창 상태를 보존하며 장면을 다시 구성하도록 요청 |
| ShatteredPixelDungeon | resize(int,int) | 0 크기 무시, 화면 크기 변경 처리 |
| ShatteredPixelDungeon | destroy() | 부모 정리 후 게임 액터 스레드 종료 |
| ShatteredPixelDungeon | updateDisplaySize() | 플랫폼의 디스플레이 크기 갱신 위임 |
| SPDSettings | fullscreen(boolean) | 설정 저장 및 시스템 UI 갱신 |
| SPDSettings | fullscreen() | 전체 화면 설정 값 읽기 |
| SPDSettings | brightness(int) | 밝기 저장 및 안개 표현 갱신 요청 |
| SPDSettings | visualGrid(int) | 격자 설정 저장 및 맵 갱신 요청 |
| SPDSettings | interfaceSize() | 화면 크기/밀도에 따른 UI 모드 선택 |
| Actor | act() | 하위 액터가 구현해야 하는 추상 행동 메서드 |
| Actor | spendConstant(float) | 액터 시간 증가 및 부동소수 오차 보정 |
| Actor | spend(float) | 기본 구현에서 spendConstant 호출 |
| Actor | postpone(float) | 특정 시각 이후로 액터 행동 시간 지연 |
| Actor | cooldown() | 현재 시간과 액터 시간의 차이 반환 |
| Actor | storeInBundle(Bundle) | 액터 시간과 ID 직렬화 |
| Actor | restoreFromBundle(Bundle) | 저장된 시간/ID 복원 및 ID 충돌 처리 |
| Actor | id() | 액터 식별자 반환 또는 새로 발급 |
| Dungeon.LimitedDrops | dropped() | 해당 드롭이 이미 발생했는지 검사 |
| Dungeon.LimitedDrops | drop() | 해당 항목의 발생 상태를 1로 표시 |
| Dungeon.LimitedDrops | reset() | 모든 한정 드롭 카운트 초기화 |

일부 메서드는 내부 호출이 더 복잡합니다. 상세한 전체 호출 그래프는 추가 분석이 필요합니다.

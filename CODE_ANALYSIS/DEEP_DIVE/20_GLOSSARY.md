# 프로젝트 용어·변수 풀이

## 게임 상태/구성
- **core**: Android/iOS/Desktop에서 공유하는 게임 로직 코드.
- **SPD-classes**: Game, Scene, Rendering, Bundle, Random, PathFinder 등을 담는 기반 코드 모듈.
- **platform**: OS 화면·입력·글꼴·진동·네트워크 기능을 접속하는 코드.
- **scene**: 게임 화면 단위. GameScene, TitleScene, InterlevelScene 등이 있음.
- **sprite**: 엔티티의 시각적 표현.
- **tilemap**: 맵 타일의 시각적 배치/렌더링.
- **level**: 하나의 던전 층(지형 + 아이템 + 몬스터 등).
- **depth**: 기본 던전의 층 깊이.
- **branch**: 같은 depth에서 다른 층으로 가는 분기 경로.
- **transition**: 다른 층으로의 이동 지점/목적지 정보.
- **feeling**: 층의 특수 생성 성향.
- **FOV**: Field Of View. 시야 판정.
- **LOS**: Line Of Sight. 시선의 통과 여부(코드에 losBlocking 등이 있음).

## 행동/전투
- **Actor**: 일정 시간에 행동하는 시뮬레이션 개체.
- **Char**: 체력, 위치, 공격, 방어, 시야 등을 갖춘 Actor.
- **Hero**: 플레이어 캐릭터.
- **Mob**: 몬스터/AI 행동 주체 기반.
- **Buff**: 캐릭터에 붙는 상태 효과 개체.
- **TICK**: 기본 시간 단위(Actor.TICK=1f).
- **actPriority**: 시간이 같을 때 행동 처리 우선순위.
- **cooldown()**: 이 액터 time과 now 사이의 차이.
- **HT**: 최대 체력에 해당하는 값; HP와 구분.
- **STR**: 영웅의 힘(Strength) 관련 값.
- **EXP**: 적이 제공하는 경험치 등의 문맥에서 사용; 같은 약어라도 클래스별 용도를 확인해야 함.

## 아이템/저장
- **Bag**: 소지품을 수용하는 객체.
- **Heap**: 바닥에 놓인 아이템 더미.
- **stackable**: 동일 아이템 중첩 허용 여부.
- **upgrade**: 아이템 강화 처리.
- **glyph/enchantment**: 방어구/무기에 결합하는 특수 효과 구성.
- **augment**: 무기/방어구의 성능 보정 종류.
- **Bundlable**: Bundle 직렬화/역직렬화 계약.
- **Bundle**: 여러 타입의 데이터를 이름-값 방식으로 직렬화하는 래퍼.
- **seed**: 난수 생성 재현을 위한 시작 상태.
- **drop deck**: 가중치/소진 상태를 관리하는 드롭 추첨 구조.

## 표기 해석 원칙
이 설명은 일반적인 게임 프로그래밍 용어와 소스에서 확인한 구조를 함께 제시한다. 예를 들어 speed, cooldown, turn은 메서드마다 실제 정의가 달라질 수 있으므로 구현과 호출 지점을 참조해야 한다.

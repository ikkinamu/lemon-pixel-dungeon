# 대표 클래스 및 상속 관계

| 클래스 | 확인된 선언 | 역할 |
|---|---|---|
| ShatteredPixelDungeon | extends Game | 공통 게임 라이프사이클과 장면 전환을 확장 |
| SPDSettings | extends GameSettings | 게임 설정 저장/조회 API |
| Actor | abstract class, implements Bundlable | 행동 주체의 시간·ID·직렬화 기반 |
| GameScene | extends PixelScene | 플레이 장면 구성 |
| Dungeon | class | 던전 진행 상태 관련 중심 클래스 |
| Dungeon.LimitedDrops | enum | 제한된 드롭의 종류와 발생 횟수 관리 |
| DesktopLauncher | class | 데스크톱 프로그램 시작점 |

## 관찰한 연결
- `ShatteredPixelDungeon`은 `com.watabou.noosa.Game`을 상속합니다.
- `GameScene`은 `PixelScene`을 상속합니다.
- `SPDSettings`는 `com.watabou.utils.GameSettings`를 상속합니다.
- `Actor`는 `Bundlable`을 구현하며 `act()`를 추상 메서드로 선언합니다.

## 추가 조사 대상
`Hero`, `Mob`, `Item`, `Level`, `Buff` 등은 다른 소스에서 참조되는 것이 확인되지만, 이 문서에서는 선언과 전체 상속 트리를 전수 검증하지 않았습니다. 따라서 상속 관계를 임의로 완성하지 않습니다.

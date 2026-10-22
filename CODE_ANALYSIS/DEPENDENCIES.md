# 의존 관계 및 데이터 흐름

## Gradle 모듈
`settings.gradle`에 `SPD-classes`, `core`, `android`, `ios`, `desktop`, `services` 및 뉴스/업데이트 하위 모듈이 등록되어 있습니다.

`core/build.gradle`에서 직접 확인한 의존성:
```text
core
  ├─ api project(':SPD-classes')
  └─ implementation project(':services')
```
다른 플랫폼 모듈의 세부 의존성은 이 문서에서 검증하지 않았습니다.

## 코드에서 확인된 호출
```text
DesktopLauncher
  ├─ DesktopLaunchValidator
  ├─ SPDSettings
  ├─ ShatteredPixelDungeon
  ├─ Updates / UpdateImpl
  └─ News / NewsImpl

ShatteredPixelDungeon
  ├─ Game (상속)
  ├─ SPDAction (입력 바인딩)
  ├─ SPDSettings (음악/효과음 설정)
  ├─ Music / Sample (오디오)
  ├─ PixelScene / TitleScene / WelcomeScene
  └─ GameScene.endActorThread() (종료 정리)

SPDSettings
  ├─ GameSettings (상속)
  ├─ ShatteredPixelDungeon.updateSystemUI()
  └─ GameScene.updateFog() / updateMap()

Actor
  ├─ Bundlable (직렬화 계약)
  ├─ Bundle (저장/복원)
  └─ Buff / Char (시간 보정 관련 참조)
```

위 관계는 직접 확인한 import, 선언 및 메서드 호출을 중심으로 작성했습니다. 단순 import만으로 실제 런타임 호출이 발생한다고 단정하지 않았습니다.

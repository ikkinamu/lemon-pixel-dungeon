# 실행 흐름 (확인된 범위)

## 데스크톱 실행 경로
```text
DesktopLauncher.main(args)
  ├─ DesktopLaunchValidator.verifyValidJVMState(args)
  ├─ OS/아키텍처 환경 처리
  ├─ 예외 처리기 설정
  ├─ 버전 정보 초기화
  ├─ 지원되는 업데이트/뉴스 서비스 연결
  └─ Lwjgl3ApplicationConfiguration 구성
       └─ (후속 실행 연결의 상세는 추가 확인 필요)
```

## 공통 게임 초기화
```text
ShatteredPixelDungeon(PlatformSupport)
  └─ Game 생성자 호출: WelcomeScene 또는 기존 sceneClass

ShatteredPixelDungeon.create()
  ├─ super.create()
  ├─ updateSystemUI()
  ├─ SPDAction.loadBindings()
  ├─ Music.INSTANCE.enable / volume
  ├─ Sample.INSTANCE.enable / volume
  └─ Sample.INSTANCE.load(Assets.Sounds.all)
```

## 장면 관리
- `switchNoFade(...)`는 `PixelScene.noFade = true` 설정 후 장면을 바꿉니다.
- `seamlessResetScene(...)`는 현재 장면이 `PixelScene`일 때 창 상태를 저장하고 장면 전환을 수행합니다.
- 재정의된 `switchScene()`은 장면 전환 후 창 상태를 복원합니다.
- `resize(...)`는 크기 변화 시 창 상태 보존을 처리하고 디스플레이 크기 갱신을 호출합니다.

이 문서는 **정적 코드 독해** 결과입니다. 게임을 실행하여 모든 런타임 경로를 검증한 것은 아닙니다.

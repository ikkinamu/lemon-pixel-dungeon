# 저장·복원·버전 호환·난수

## 1. 저장은 전역 게임과 층을 분리
소스: [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java:620-750](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L620-L750), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java:765-867](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L765-L867).
- saveGame(slot): hero, depth, branch, gold, energy, challenges, seed, 퀘스트, 통계, 생성 이력, 소모품 외형 정보 등 **게임 전체 상태**를 Bundle로 직렬화하고 game.dat에 기록.
- saveLevel(slot): 현재 Level 객체를 별도 Bundle에 넣어 depth 파일에 기록.
- saveAll(): Actor.fixTime()·탐색 정보 갱신·전체 게임 저장·현재 층 저장·진행 슬롯 상태 갱신을 순서대로 호출.
- loadGame(slot): 게임 공통 정보 복원.
- loadLevel(slot): depth/branch에 맞는 층 저장 파일을 읽어 Level 복원.
- deleteGame(slot,...): 진행 슬롯 및 관련 층 데이터 정리.

**중요:** saveGame()은 IOException을 내부에서 포착하고 슬롯을 Unknown 처리한다. 이것을 saveAll()이 항상 예외를 전파한다는 뜻으로 읽으면 안 된다. saveLevel()의 예외 처리 경로와 구별해야 한다.

## 2. 파일 경로
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java:38-67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L38-L67):
- game%d/ 디렉터리
- game.dat: 게임 전체 저장 데이터
- depth%d.dat: branch=0의 층
- depth%d-branch%d.dat: branch가 0이 아닌 층

Info, curSlot, selectedClass는 메뉴에서 진행 기록을 조회·정렬하는 데 쓰이며, 파일 경로 함수의 %d는 슬롯/층 숫자 자리표시자이다.

## 3. Bundle
[SPD-classes/src/main/java/com/watabou/utils/Bundle.java:46-166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java#L46-L166):
- 내부 JSON 기반 데이터 래퍼이며 getInt/getFloat/getString/getBundle/get(Bundlable) 등의 API를 제공.
- Bundlable을 구현하는 Actor/Level/Item 등은 storeInBundle()/restoreFromBundle() 계약 사용.
- 클래스 이름 별칭이 존재하여 이름이 바뀐 객체의 역직렬화 호환성을 처리할 수 있음.
- 코드에서 gzip 압축 관련 처리가 확인되지만 **모든 저장 파일이 사람이 바로 읽을 수 있는 JSON 텍스트라는 뜻은 아니다**.

## 4. 버전
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java:39-57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java#L39-L57):
- v1_2_3, v3_1_1, v3_2_1, v3_2_5, v3_3_0, v4_0_0 등은 하위 호환성 판단에 쓰이는 **정수 버전 코드 기준**.
- v3_1_1보다 오래된 세이브 무시 규칙이 주석과 GamesInProgress.check()에 확인됨([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java:98-125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java#L98-L125)).
- 버전명 '4.0.2'와 코드 922는 분석 당시 루트 build.gradle에서 확인. 매번 현재 출시 버전이라고 단정하지 말 것.

## 5. seed의 정확한 의미
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java:215-250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L215-L250), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java:414-431](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L414-L431):
- daily면 날짜 기반 코드를 사용자 시드 범위 바깥으로 옮기는 분기.
- 사용자 지정 문자열이면 DungeonSeed.convertFromText() 사용.
- 그 외에는 DungeonSeed.randomSeed() 사용.
- seedForDepth(depth,branch)는 run seed를 난수 생성기에 설정하고 depth + 30*branch만큼 난수를 소비한 뒤 값을 하나 더 얻어 층 seed로 사용.
- Level.create()는 이 층 seed를 pushGenerator 하고 맵/아이템/몬스터 생성을 처리한 뒤 popGenerator.
- Random 자체에 난수 생성기 스택이 존재([SPD-classes/src/main/java/com/watabou/utils/Random.java:32-77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java#L32-L77)).

**주의:** seedForDepth()의 '30*branch'는 소스 주석상 depth가 1~30이라는 가정에 의존한다. branch와 depth 범위를 임의 확장하면 설계 가정에 부딪힐 수 있다. 또한 **동일 seed=항상 동일 최종 플레이 기록**은 성립하지 않는다. 진행 중 선택과 생성 호출 순서에 따라 상태가 바뀜.

## 6. 생성 이력 인코딩
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java:292-298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L292-L298): generatedLevels에는 depth + 1000*branch 인코딩을 사용. 소스에는 depth 범위 가정이 명시됨. 이 정수는 레벨 객체나 파일 경로 자체가 아니라 **생성 여부 추적 키**다.

## 7. 조심해야 할 변경 지점 (분석용)
- 클래스·필드 이름을 바꾸면 Bundle과 호환성·별칭에 영향이 있을 수 있음.
- level/branch/seed나 RNG 덱 로직 변경은 새 게임 뿐 아니라 이어하기 및 재현성에도 영향이 있을 수 있음.
- 저장 스키마 또는 파일 경로를 바꿀 땐 별도 버전 마이그레이션 설계가 필요할 수 있음.

여기서는 분석만 수행했으며 어떤 저장 포맷도 변경하지 않았다.

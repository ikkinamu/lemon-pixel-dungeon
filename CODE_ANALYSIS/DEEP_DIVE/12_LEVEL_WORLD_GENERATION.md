# 던전 층·방·지형·생성 파이프라인

## 1. Dungeon에서 층 선택
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java:292-405](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L292-L405)의 Dungeon.newLevel()에서 현재 depth와 branch에 따라 Level 클래스를 고른다.

**기본 경로 branch=0**
| 층 | 클래스 |
|---|---|
| 1–4 | SewerLevel |
| 5 | SewerBossLevel |
| 6–9 | PrisonLevel |
| 10 | PrisonBossLevel |
| 11–14 | CavesLevel |
| 15 | CavesBossLevel |
| 16–19 | CityLevel |
| 20 | CityBossLevel |
| 21–24 | HallsLevel |
| 25 | HallsBossLevel |
| 26 | LastLevel |
| 기타 | DeadEndLevel |

**별도 경로 branch=1**
- 11–14: MiningLevel
- 16–19: VaultLevel
- 그 외: DeadEndLevel

이는 코드의 분기표이며 플레이어의 보편적인 방문 순서나 각 층의 실제 접근 가능성을 설명한 표는 아니다.

## 2. Level 모델과 배열
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java:145-216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java#L145-L216):
- width, height, length: 타일 공간의 치수·길이.
- map (int[]): 타일별 지형 코드.
- visited/mapped/discoverable (boolean[]): 탐험·지도·발견 관련 상태.
- heroFOV (boolean[]): 영웅의 시야 판정용 배열.
- passable/losBlocking/flamable/secret/solid/avoid/water/pit/openSpace: 지형의 성질을 캐시한 불리언 배열.
- mobs (HashSet<Mob>), heaps (SparseArray<Heap>), blobs (HashMap<Class<? extends Blob>,Blob>), plants/traps (SparseArray): 층의 엔티티.
- transitions (ArrayList<LevelTransition>): 층 이동 지점.
- feeling: 층 성향; locked: 보스층 잠금 여부 등의 상태.

**주의:** passable는 해당 타일의 통과 가능 성질을 표현하지만 특정 순간 실제 이동이 항상 가능하다는 뜻은 아니다. 캐릭터 점유, 버프, 능력, 문 등의 추가 조건을 확인해야 함. heroFOV의 true는 시야 조건에 대한 판단이지 탐험 완료 여부와 동일하지 않음.

## 3. Level.create()의 주요 순서
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java:218-326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java#L218-L326):
1. Dungeon.seedCurDepth()로 난수 생성기 스택을 설정.
2. 층에 필요한 음식/힘의 물약/강화의 주문서 및 기타 한정 드롭을 결정.
3. 층 feeling(예: CHASM, WATER, GRASS, DARK, LARGE, TRAPS, SECRETS 등)을 선택할 수 있음.
4. mobs/heaps/blobs/plants/traps/타일 관련 컨테이너 초기화.
5. build()가 성공할 때까지 반복.
6. buildFlagMaps()·cleanWalls() 적용.
7. createMobs()·createItems() 호출.
8. 난수 생성기를 pop.

## 4. RegularLevel의 방 배치
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java:105-192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java#L105-L192):
~~~
initRooms(): 입구/출구 + 일반 방 + 상점 + 특수 방 + 비밀 방
 -> Random.shuffle(initRooms)
 -> builder.build(...)
 -> painter().paint(level, rooms)
 -> Level.create()의 후속 createMobs()/createItems()
~~~
RegularLevel.builder()의 기본 후보: LoopBuilder 또는 FigureEightBuilder. 그러나 하위 층 클래스가 builder()나 painter()를 재정의할 수 있으므로 **모든 층이 무조건 동일한 빌더를 사용한다고 일반화하면 안 됨**.

Room은 Rect와 Graph.Node, Bundlable에 연결되고, neigbours(기하학적 이웃), connected(통로로 연결됨)를 구별함([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java:37-43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L37-L43), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java:165-282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java#L165-L282)).
- 이름 철자 neigbours는 실제 코드의 식별자를 따른 것이며 여기서 임의로 수정하지 않음.
- canConnect()는 지점·방향·입출구 직접 연결 제한 등을 검사.
- Painter는 지형 셀 채우기/직선/타원/다이아몬드 등의 묘화 유틸리티 제공([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/Painter.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/Painter.java)).

## 5. 전환 지점과 탐색
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java:32-116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java#L32-L116): type, destDepth, destBranch, destType, centerCell로 목적지를 보관.
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java:464-514](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L464-L514): switchLevel()은 유효 위치 보정, PathFinder.setMapSize, 영웅 위치 지정, Actor.init, 적 위치 충돌 회피, 시야 갱신 및 저장을 연결.

## 6. 다른 층 객체
- Trap: 위치/가시성/활성화 상태, trigger()/activate()/disarm()([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java)).
- Blob: 가스/불/전기 등 영역 효과를 구현하는 하위 클래스가 actors/blobs에 위치(개별 효과는 하위 클래스 별도 확인 필요).
- 여러 rooms/secret, rooms/special, painters, builders 하위 클래스가 존재함. 전체 파일명 목록은 03_JAVA_INDEX_LEVELS.md.

## 생성의 핵심 함정
**생성 결과는 seed 하나로만 설명할 수 없다.** 게임 생성 상태, 생성 순서, 호출별 난수 스택, 드롭 덱 및 저장 복원 여부가 영향을 준다. 확정적 재현을 주장하려면 같은 버전·설정·초기 상태 및 실제 호출 경로를 통제해 비교해야 한다.

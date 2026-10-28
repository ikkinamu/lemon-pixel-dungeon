# Java 파일별 소스 구현 해설 272–287

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 272. [`Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon` / 본문 273행 / 타입 1개 / 필드 9개 / 메서드 4개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L41) `class Bones`

### 변수·상수 (단일 행 선언)

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L43) `String BONES_FILE` 초기식: `"bones.dat"`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L45) `String LEVEL` 초기식: `"level"`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L46) `String BRANCH` 초기식: `"branch"`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L47) `String ITEM` 초기식: `"item"`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L48) `String HERO_CLASS` 초기식: `"hero_class"`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L50) `int depth` 초기식: `-1`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L51) `int branch` 초기식: `-1`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L53) `Item item`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L54) `HeroClass heroClass`

### 함수·메서드 역할과 내부 연결

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L56) **`leave()`**: 개별 처리 / 조건 분기·예외 처리 / 참조 호출: Math.max, pickItem, Bundle, bundle.put, FileUtils.bundleToFile, ShatteredPixelDungeon.reportException
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L86) **`pickItem(Hero hero)`**: 개별 처리 / 조건 분기·반복·상태 선택 / 참조 호출: Dungeon.customSeedText.isEmpty, Random.Int, belongings.secondWep.trueLevel, item.trueLevel, Dungeon.quickslot.randomNonePlaceholder, pickItem, belongings.backpack.iterator, iterator.hasNext, iterator.next
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L154) **`get()`**: 조회·탐색 / 조건 분기·예외 처리 / 참조 호출: FileUtils.bundleFromFile, bundle.getInt, bundle.contains, bundle.get, bundle.getEnum, get, lootAtCurLevel, Bundle, emptyBones.put
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java#L260) **`lootAtCurLevel()`**: 개별 처리 / 조건 분기

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 273. [`Challenges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon` / 본문 81행 / 타입 1개 / 필드 11개 / 메서드 3개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L27) `class Challenges`

### 변수·상수 (단일 행 선언)

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L30) `int NO_FOOD` 초기식: `1`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L31) `int NO_ARMOR` 초기식: `2`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L32) `int NO_HEALING` 초기식: `4`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L33) `int NO_HERBALISM` 초기식: `8`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L34) `int SWARM_INTELLIGENCE` 초기식: `16`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L35) `int DARKNESS` 초기식: `32`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L36) `int NO_SCROLLS` 초기식: `64`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L37) `int CHAMPION_ENEMIES` 초기식: `128`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L38) `int STRONGER_BOSSES` 초기식: `256`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L40) `int MAX_VALUE` 초기식: `511`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L41) `int MAX_CHALS` 초기식: `9`

### 함수·메서드 역할과 내부 연결

- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L59) **`activeChallenges()`**: 시간·상태 갱신 / 참조 호출: activeChallenges
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L63) **`activeChallenges(int mask)`**: 시간·상태 갱신 / 조건 분기·반복
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L71) **`isItemBlocked(Item item)`**: 조건 판정 / 조건 분기 / 참조 호출: Dungeon.isChallenged

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 274. [`Chrome.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Chrome.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon` / 본문 86행 / 타입 2개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Chrome.java#L26) `class Chrome`
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Chrome.java#L28) `enum Type`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Chrome.java#L47) **`get(Type type)`**: 조회·탐색 / 상태 선택 / 참조 호출: NinePatch

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 275. [`Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon` / 본문 1097행 / 타입 2개 / 필드 41개 / 메서드 47개.

### 타입·상속 선언

- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L100) `class Dungeon`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L104) `enum LimitedDrops`

### 변수·상수 (단일 행 선언)

- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L147) `int count` 초기식: `0`
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L182) `int challenges`
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L183) `float mobsToChampion`
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L185) `Hero hero`
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L186) `Level level`
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L190) `int depth`
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L194) `int branch`
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L199) `int gold`
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L200) `int energy`
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L202) `HashSet<Integer> chapters`
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L204) `SparseArray<ArrayList<Item>> droppedItems`
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L207) `int initialVersion`
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L208) `int version`
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L210) `boolean daily`
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L211) `boolean dailyReplay`
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L212) `String customSeedText` 초기식: `""`
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L213) `long seed`
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L214) `long lastPlayed`
- [L601](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L601) `String INIT_VER` 초기식: `"init_ver"`
- [L602](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L602) `String VERSION` 초기식: `"version"`
- [L603](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L603) `String SEED` 초기식: `"seed"`
- [L604](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L604) `String CUSTOM_SEED` 초기식: `"custom_seed"`
- [L605](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L605) `String DAILY` 초기식: `"daily"`
- [L606](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L606) `String DAILY_REPLAY` 초기식: `"daily_replay"`
- [L607](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L607) `String LAST_PLAYED` 초기식: `"last_played"`
- [L608](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L608) `String CHALLENGES` 초기식: `"challenges"`
- [L609](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L609) `String MOBS_TO_CHAMPION` 초기식: `"mobs_to_champion"`
- [L610](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L610) `String HERO` 초기식: `"hero"`
- [L611](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L611) `String DEPTH` 초기식: `"depth"`
- [L612](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L612) `String BRANCH` 초기식: `"branch"`
- [L613](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L613) `String GENERATED_LEVELS` 초기식: `"generated_levels"`
- [L614](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L614) `String GOLD` 초기식: `"gold"`
- [L615](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L615) `String ENERGY` 초기식: `"energy"`
- [L616](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L616) `String DROPPED` 초기식: `"dropped%d"`
- [L617](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L617) `String PORTED` 초기식: `"ported%d"`
- [L618](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L618) `String LEVEL` 초기식: `"level"`
- [L619](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L619) `String LIMDROPS` 초기식: `"limited_drops"`
- [L620](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L620) `String CHAPTERS` 초기식: `"chapters"`
- [L621](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L621) `String QUESTS` 초기식: `"quests"`
- [L622](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L622) `String BADGES` 초기식: `"badges"`
- [L1025](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L1025) `boolean[] passable`

### 함수·메서드 역할과 내부 연결

- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L150) **`dropped()`**: 개별 처리
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L153) **`drop()`**: 개별 처리
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L157) **`reset()`**: 생성·초기화 / 반복 / 참조 호출: values
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L163) **`store(Bundle bundle)`**: 저장·복원 / 반복 / 참조 호출: values, bundle.put, lim.name
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L169) **`restore(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: values, bundle.contains, lim.name, bundle.getInt
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L188) **`QuickSlot()`**: 개별 처리
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L217) **`initSeed()`**: 생성·초기화 / 조건 분기 / 참조 호출: SPDSettings.lastDaily, SimpleDateFormat, format.setTimeZone, TimeZone.getTimeZone, format.format, Date, SPDSettings.customSeed, isEmpty, DungeonSeed.convertFromText
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L233) **`init()`**: 생성·초기화 / 참조 호출: SPDSettings.challenges, Actor.clear, Actor.resetNextID, Random.pushGenerator, Scroll.initLabels, Potion.initColors, Ring.initGems, SpecialRoom.initForRun, SecretRoom.initForRun
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L289) **`isChallenged(int mask)`**: 조건 판정
- [L293](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L293) **`levelHasBeenGenerated(int depth, int branch)`**: 개별 처리 / 참조 호출: generatedLevels.contains
- [L297](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L297) **`newLevel()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Actor.clear, SewerLevel, SewerBossLevel, PrisonLevel, PrisonBossLevel, CavesLevel, CavesBossLevel, CityLevel, CityBossLevel
- [L406](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L406) **`resetLevel()`**: 생성·초기화 / 참조 호출: Actor.clear, level.reset, switchLevel, level.entrance
- [L414](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L414) **`seedCurDepth()`**: 개별 처리 / 참조 호출: seedForDepth
- [L418](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L418) **`seedForDepth(int depth, int branch)`**: 개별 처리 / 반복 / 참조 호출: Random.pushGenerator, Random.Long, Random.popGenerator
- [L433](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L433) **`shopOnLevel()`**: 개별 처리
- [L437](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L437) **`bossLevel()`**: 개별 처리 / 참조 호출: bossLevel
- [L441](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L441) **`bossLevel(int depth)`**: 개별 처리
- [L447](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L447) **`scalingDepth()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.buff
- [L455](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L455) **`interfloorTeleportAllowed()`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.getItem
- [L464](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L464) **`switchLevel(final Level level, int pos)`**: 개별 처리 / 조건 분기·반복·예외 처리 / 참조 호출: level.getTransition, t.cell, level.length, level.invalidHeroPos, cell, PathFinder.setMapSize, level.width, level.height, hero.buff
- [L520](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L520) **`dropToChasm(Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.droppedItems.get, Dungeon.droppedItems.put, dropped.add
- [L529](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L529) **`posNeeded()`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int
- [L545](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L545) **`souNeeded()`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int
- [L556](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L556) **`asNeeded()`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int
- [L566](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L566) **`enchStoneNeeded()`**: 개별 처리 / 조건 분기 / 참조 호출: LimitedDrops.ENCH_STONE.dropped, Random.Int
- [L579](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L579) **`intStoneNeeded()`**: 개별 처리 / 참조 호출: LimitedDrops.INT_STONE.dropped, Random.Int
- [L584](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L584) **`trinketCataNeeded()`**: 개별 처리 / 참조 호출: LimitedDrops.TRINKET_CATA.dropped, Random.Int
- [L589](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L589) **`labRoomNeeded()`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int
- [L624](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L624) **`saveGame(int save)`**: 저장·복원 / 반복·예외 처리 / 참조 호출: Bundle, bundle.put, droppedItems.keyArray, Messages.format, droppedItems.get, quickslot.storePlaceholders, LimitedDrops.store, chapters.size, Quest.storeInBundle
- [L699](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L699) **`saveLevel(int save)`**: 저장·복원 / 참조 호출: Bundle, bundle.put, FileUtils.bundleToFile, GamesInProgress.depthFile
- [L706](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L706) **`saveAll()`**: 저장·복원 / 조건 분기 / 참조 호출: hero.isAlive, Actor.fixTime, updateLevelExplored, saveGame, saveLevel, GamesInProgress.set
- [L719](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L719) **`loadGame(int save)`**: 저장·복원 / 참조 호출: loadGame
- [L723](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L723) **`loadGame(int save, boolean fullLoad)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: FileUtils.bundleFromFile, GamesInProgress.gameFile, bundle.getInt, bundle.contains, bundle.getLong, DungeonSeed.randomSeed, bundle.getString, bundle.getBoolean, Actor.clear
- [L826](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L826) **`loadLevel(int save)`**: 저장·복원 / 조건 분기 / 참조 호출: Actor.clear, FileUtils.bundleFromFile, GamesInProgress.depthFile, bundle.get, IOException
- [L842](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L842) **`deleteGame(int save, boolean deleteLevels)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: GamesInProgress.gameFolder, FileUtils.filesInDir, file.contains, FileUtils.deleteFile, FileUtils.overwriteFile, GamesInProgress.gameFile, GamesInProgress.delete
- [L858](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L858) **`preview(GamesInProgress.Info info, Bundle bundle)`**: 개별 처리 / 참조 호출: bundle.getInt, bundle.getLong, bundle.getString, bundle.getBoolean, Hero.preview, bundle.getBundle, Statistics.preview
- [L872](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L872) **`fail(Object cause)`**: 개별 처리 / 조건 분기 / 참조 호출: updateLevelExplored, Rankings.INSTANCE.submit
- [L880](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L880) **`win(Object cause)`**: 개별 처리 / 참조 호출: updateLevelExplored, hero.belongings.identify, Rankings.INSTANCE.submit
- [L890](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L890) **`updateLevelExplored()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.bossLevel, Statistics.floorsExplored.put, level.levelExplorePercent
- [L897](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L897) **`observe()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, Dungeon.hero.pointsInTalent, Dungeon.hero.buff, observe
- [L908](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L908) **`observe(int dist)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: level.updateFieldOfView, level.width, Math.max, Math.min, level.height, BArray.or, GameScene.updateFog, hero.buff, level.mobs.toArray
- [L1027](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L1027) **`setupPassable()`**: 생성·초기화 / 조건 분기 / 참조 호출: Dungeon.level.length, BArray.setFalse
- [L1034](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L1034) **`findPassable(Char ch, boolean[] pass, boolean[] vis, boolean chars)`**: 조회·탐색 / 참조 호출: findPassable
- [L1038](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L1038) **`findPassable(Char ch, boolean[] pass, boolean[] vis, boolean chars, boolean considerLarge)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: setupPassable, ch.buff, BArray.or, System.arraycopy, Dungeon.level.length, Char.hasProp, BArray.and, ch.modifyPassable, Actor.chars
- [L1063](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L1063) **`findPath(Char ch, int to, boolean[] pass, boolean[] vis, boolean chars)`**: 조회·탐색 / 참조 호출: PathFinder.find, findPassable
- [L1069](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L1069) **`findStep(Char ch, int to, boolean[] pass, boolean[] visible, boolean chars)`**: 조회·탐색 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, Actor.findChar, PathFinder.getStep, findPassable
- [L1079](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L1079) **`flee(Char ch, int from, boolean[] pass, boolean[] visible, boolean chars)`**: 개별 처리 / 반복 / 참조 호출: findPassable, ch.buff, PathFinder.getStepBack, Actor.findChar

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 276. [`BadgeBanner.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 219행 / 타입 2개 / 필드 9개 / 메서드 9개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L38) `class BadgeBanner  extends Image`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L40) `enum State`

### 변수·상수 (단일 행 선언)

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L43) `State state`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L45) `float DEFAULT_SCALE` 초기식: `3`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L46) `int SIZE` 초기식: `16`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L48) `float FADE_IN_TIME` 초기식: `0.25f`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L49) `float STATIC_TIME` 초기식: `1f`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L50) `float FADE_OUT_TIME` 초기식: `1.75f`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L52) `int index`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L53) `float time`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L55) `TextureFilm atlas`

### 함수·메서드 역할과 내부 연결

- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L59) **`BadgeBanner(int index)`**: 개별 처리 / 조건 분기 / 참조 호출: TextureFilm, setup
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L70) **`setup(int index)`**: 생성·초기화 / 참조 호출: frame, atlas.get, origin.set, alpha, scale.set, Sample.INSTANCE.play
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L86) **`update()`**: 시간·상태 갱신 / 조건 분기·상태 선택 / 참조 호출: super.update, scale.set, alpha, highlight, killAndErase
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L128) **`kill()`**: 개별 처리 / 참조 호출: showing.remove, super.kill
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L134) **`destroy()`**: 개별 처리 / 참조 호출: showing.remove, super.destroy
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L148) **`highlight(Image image, int index)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: PointF, highlightPositions.containsKey, highlightPositions.get, TextureCache.get, tx.getPixel, highlightPositions.put, Point, p.offset, image.point
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L200) **`show(int image)`**: 개별 처리 / 참조 호출: BadgeBanner, showing.add
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L206) **`isShowingBadges()`**: 조건 판정 / 참조 호출: showing.isEmpty
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java#L210) **`image(int index)`**: 개별 처리 / 조건 분기 / 참조 호출: Image, TextureFilm, image.frame, atlas.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 277. [`BannerSprites.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BannerSprites.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 63행 / 타입 2개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BannerSprites.java#L27) `class BannerSprites`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BannerSprites.java#L29) `enum Type`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BannerSprites.java#L38) **`get(Type type)`**: 조회·탐색 / 상태 선택 / 참조 호출: Image, icon.frame, icon.texture.uvRect

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 278. [`Beam.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 100행 / 타입 5개 / 필드 3개 / 메서드 7개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L31) `class Beam  extends Image`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L55) `class DeathRay  extends Beam`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L61) `class LightRay  extends Beam`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L67) `class SunRay  extends Beam`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L74) `class HealthRay  extends Beam`

### 변수·상수 (단일 행 선언)

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L33) `double A` 초기식: `180 / Math.PI`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L35) `float duration`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L37) `float timeLeft`

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L39) **`Beam(PointF s, PointF e, Effects.Type asset, float duration)`**: 개별 처리 / 참조 호출: Effects.get, origin.set, Math.atan2, Math.sqrt
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L56) **`DeathRay(PointF s, PointF e)`**: 개별 처리
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L62) **`LightRay(PointF s, PointF e)`**: 개별 처리
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L68) **`SunRay(PointF s, PointF e)`**: 개별 처리 / 참조 호출: tint
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L75) **`HealthRay(PointF s, PointF e)`**: 개별 처리
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L81) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, alpha, scale.set, killAndErase
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Beam.java#L94) **`draw()`**: 지형/화면 표현 / 참조 호출: Blending.setLightMode, super.draw, Blending.setNormalMode

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 279. [`BlobEmitter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BlobEmitter.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 75행 / 타입 1개 / 필드 1개 / 메서드 3개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BlobEmitter.java#L31) `class BlobEmitter  extends Emitter`

### 변수·상수 (단일 행 선언)

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BlobEmitter.java#L33) `Blob blob`

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BlobEmitter.java#L35) **`BlobEmitter(Blob blob)`**: 개별 처리 / 참조 호출: blob.use
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BlobEmitter.java#L43) **`RectF(0, 0, 1, 1)`**: 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BlobEmitter.java#L46) **`emit(int index)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: blob.area.isEmpty, blob.setupArea, Dungeon.level.width, Dungeon.level.length, Random.Float, factory.emit

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 280. [`CellEmitter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CellEmitter.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 71행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CellEmitter.java#L29) `class CellEmitter`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CellEmitter.java#L31) **`floor(int cell)`**: 개별 처리 / 참조 호출: DungeonTilemap.tileToWorld, GameScene.floorEmitter, emitter.pos
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CellEmitter.java#L41) **`get(int cell)`**: 조회·탐색 / 참조 호출: DungeonTilemap.tileToWorld, GameScene.emitter, emitter.pos
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CellEmitter.java#L51) **`center(int cell)`**: 개별 처리 / 참조 호출: DungeonTilemap.tileToWorld, GameScene.emitter, emitter.pos
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CellEmitter.java#L61) **`bottom(int cell)`**: 개별 처리 / 참조 호출: DungeonTilemap.tileToWorld, GameScene.emitter, emitter.pos

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 281. [`Chains.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 104행 / 타입 1개 / 필드 9개 / 메서드 3개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L31) `class Chains  extends Group`

### 변수·상수 (단일 행 선언)

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L33) `double A` 초기식: `180 / Math.PI`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L35) `float spent` 초기식: `0f`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L36) `float duration`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L38) `Callback callback`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L40) `Image[] chains`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L41) `int numChains`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L42) `float distance`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L43) `float rotation` 초기식: `0`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L45) `PointF from, to`

### 함수·메서드 역할과 내부 연결

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L47) **`Chains(int from, int to, Effects.Type type, Callback callback)`**: 개별 처리 / 참조 호출: DungeonTilemap.tileCenterToWorld
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L54) **`Chains(PointF from, PointF to, Effects.Type type, Callback callback)`**: 개별 처리 / 반복 / 참조 호출: Math.hypot, Math.atan2, Math.round, Image, Effects.get, origin.set, width, height, add
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Chains.java#L83) **`update()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: killAndErase, callback.call, center, PointF

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 282. [`CheckedCell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CheckedCell.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 70행 / 타입 1개 / 필드 2개 / 메서드 3개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CheckedCell.java#L30) `class CheckedCell  extends Image`

### 변수·상수 (단일 행 선언)

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CheckedCell.java#L32) `float alpha`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CheckedCell.java#L33) `float delay`

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CheckedCell.java#L35) **`CheckedCell()`**: 개별 처리 / 참조 호출: TextureCache.createSolid
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CheckedCell.java#L39) **`reset(int pos, int visSource)`**: 생성·초기화 / 조건 분기 / 참조 호출: revive, origin.set, point, DungeonTilemap.tileToWorld, offset, scale.set, Dungeon.level.trueDistance, Math.pow, alpha
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CheckedCell.java#L59) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: alpha, scale.set, kill

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 283. [`CircleArc.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 200행 / 타입 1개 / 필드 11개 / 메서드 9개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L39) `class CircleArc  extends Visual`

### 변수·상수 (단일 행 선언)

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L41) `float duration` 초기식: `0`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L42) `float lifespan`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L45) `float sweep`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L46) `boolean dirty`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L48) `boolean lightMode` 초기식: `true`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L50) `SmartTexture texture`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L52) `float[] vertices`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L53) `FloatBuffer verticesBuffer`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L54) `ShortBuffer indices`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L56) `int nTris`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L57) `float rad`

### 함수·메서드 역할과 내부 연결

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L60) **`CircleArc(int triangles, float radius)`**: 개별 처리 / 참조 호출: TextureCache.createSolid, allocateDirect, order, ByteOrder.nativeOrder, asFloatBuffer, asShortBuffer, updateTriangles
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L84) **`color(int color, boolean lightMode)`**: 개별 처리 / 참조 호출: hardlight
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L91) **`show(Visual visual, float duration)`**: 개별 처리 / 참조 호출: point, visual.center, visual.parent.addToBack
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L100) **`show(Group parent, PointF pos, float duration)`**: 개별 처리 / 참조 호출: point, parent.add
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L109) **`setSweep(float sweep)`**: 상태 갱신 / 조건 분기
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L116) **`getSweep()`**: 조회·탐색
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L120) **`updateTriangles()`**: 시간·상태 갱신 / 반복 / 참조 호출: position, verticesBuffer.put, Math.cos, Math.sin, indices.put
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L160) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, killAndErase
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java#L175) **`draw()`**: 지형/화면 표현 / 조건 분기 / 참조 호출: super.draw, updateTriangles, Blending.setLightMode, NoosaScript.get, texture.bind, script.uModel.valueM4, script.lighting, script.camera, script.drawElements

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 284. [`DarkBlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/DarkBlock.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 62행 / 타입 1개 / 필드 1개 / 메서드 4개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/DarkBlock.java#L27) `class DarkBlock  extends Gizmo`

### 변수·상수 (단일 행 선언)

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/DarkBlock.java#L29) `CharSprite target`

### 함수·메서드 역할과 내부 연결

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/DarkBlock.java#L31) **`DarkBlock(CharSprite target)`**: 개별 처리
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/DarkBlock.java#L38) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, target.brightness
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/DarkBlock.java#L45) **`lighten()`**: 개별 처리 / 참조 호출: target.resetColor, killAndErase
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/DarkBlock.java#L52) **`darken(CharSprite sprite)`**: 개별 처리 / 조건 분기 / 참조 호출: DarkBlock, sprite.parent.add

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 285. [`Degradation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 158행 / 타입 2개 / 필드 2개 / 메서드 9개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L30) `class Degradation  extends Group`
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L120) `class Speck  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L122) `int COLOR` 초기식: `0xFF4422`
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L123) `int SIZE` 초기식: `3`

### 함수·메서드 역할과 내부 연결

- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L81) **`weapon(PointF p)`**: 개별 처리 / 참조 호출: Degradation
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L85) **`armor(PointF p)`**: 개별 처리 / 참조 호출: Degradation
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L89) **`ring(PointF p)`**: 개별 처리 / 참조 호출: Degradation
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L93) **`wand(PointF p)`**: 개별 처리 / 참조 호출: Degradation
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L97) **`Degradation(PointF p, int[] matrix)`**: 개별 처리 / 반복 / 참조 호출: add, Speck
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L106) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, countLiving, killAndErase
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L114) **`draw()`**: 지형/화면 표현 / 참조 호출: Blending.setLightMode, super.draw, Blending.setNormalMode
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L125) **`Speck(float x0, float y0, int mx, int my)`**: 개별 처리 / 참조 호출: color, PointF, polar, Random.Float, speed.set, acc.set
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Degradation.java#L149) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, Math.abs, size

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 286. [`Effects.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Effects.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 75행 / 타입 2개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Effects.java#L27) `class Effects`
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Effects.java#L29) `enum Type`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Effects.java#L41) **`get(Type type)`**: 조회·탐색 / 상태 선택 / 참조 호출: Image, icon.frame, icon.texture.uvRect

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 287. [`EmoIcon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 174행 / 타입 5개 / 필드 4개 / 메서드 11개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L33) `class EmoIcon  extends Image`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L78) `class Sleep  extends EmoIcon`
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L102) `class Alert  extends EmoIcon`
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L126) `class Investigate  extends EmoIcon`
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L150) `class Lost  extends EmoIcon`

### 변수·상수 (단일 행 선언)

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L35) `float maxSize` 초기식: `2`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L36) `float timeScale` 초기식: `1`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L38) `boolean growing` 초기식: `true`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L40) `CharSprite owner`

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L42) **`EmoIcon(CharSprite owner)`**: 개별 처리 / 참조 호출: GameScene.add
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L50) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, scale.set, Math.min, Math.max, centerPoint, PixelScene.align, owner.width
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L74) **`centerPoint()`**: 개별 처리 / 참조 호출: PointF, width, height
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L80) **`Sleep(CharSprite owner)`**: 개별 처리 / 참조 호출: copy, Icons.get, scale.set, Random.Float
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L96) **`centerPoint()`**: 개별 처리 / 참조 호출: PointF, width, height
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L104) **`Alert(CharSprite owner)`**: 개별 처리 / 참조 호출: copy, Icons.get, scale.set, Random.Float
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L120) **`centerPoint()`**: 개별 처리 / 참조 호출: PointF, width, height
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L128) **`Investigate(CharSprite owner)`**: 개별 처리 / 참조 호출: copy, Icons.get, scale.set, Random.Float
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L144) **`centerPoint()`**: 개별 처리 / 참조 호출: PointF, width, height
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L152) **`Lost(CharSprite owner)`**: 개별 처리 / 참조 호출: copy, Icons.get, scale.set, Random.Float
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java#L167) **`centerPoint()`**: 개별 처리 / 참조 호출: PointF, width, height

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":30,"fields":103,"methods":119}

# Java 파일별 소스 구현 해설 240–255

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 240. [`VaultDM100.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultDM100.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.quest.vault` / 본문 54행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultDM100.java#L29) `class VaultDM100  extends DM100`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultDM100.java#L44) **`attackSkill(Char target)`**: 전투 관련
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultDM100.java#L49) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 241. [`VaultDM200.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultDM200.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.quest.vault` / 본문 59행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultDM200.java#L30) `class VaultDM200  extends DM200`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultDM200.java#L45) **`attackSkill(Char target)`**: 전투 관련
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultDM200.java#L50) **`lootChance()`**: 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultDM200.java#L55) **`createLoot()`**: 생성·초기화 / 참조 호출: DwarfToken

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 242. [`VaultElemental.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultElemental.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.quest.vault` / 본문 86행 / 타입 4개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultElemental.java#L28) `class VaultElemental  extends Elemental`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultElemental.java#L41) `class Fire  extends FireElemental`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultElemental.java#L56) `class Frost  extends FrostElemental`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultElemental.java#L71) `class Shock  extends ShockElemental`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultElemental.java#L30) **`random()`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Float

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 243. [`VaultGhoul.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultGhoul.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.quest.vault` / 본문 62행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultGhoul.java#L31) `class VaultGhoul  extends Ghoul`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultGhoul.java#L46) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.distance, beckon, super.act

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 244. [`VaultGolem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultGolem.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.quest.vault` / 본문 53행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultGolem.java#L29) `class VaultGolem  extends Golem`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultGolem.java#L43) **`lootChance()`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultGolem.java#L48) **`createLoot()`**: 생성·초기화 / 참조 호출: DwarfToken

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 245. [`VaultRat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultRat.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.quest.vault` / 본문 55행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultRat.java#L32) `class VaultRat  extends Rat`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultRat.java#L46) **`attackSkill(Char target)`**: 전투 관련
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultRat.java#L51) **`description()`**: 개별 처리 / 참조 호출: Messages.get, super.description

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 246. [`VaultShaman.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultShaman.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.quest.vault` / 본문 108행 / 타입 1개 / 필드 1개 / 메서드 8개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultShaman.java#L36) `class VaultShaman  extends Shaman`

### 변수·상수 (단일 행 선언)

- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultShaman.java#L94) `String TYPE` 초기식: `"type"`

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultShaman.java#L51) **`attackSkill(Char target)`**: 전투 관련
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultShaman.java#L56) **`lootChance()`**: 개별 처리
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultShaman.java#L61) **`createLoot()`**: 생성·초기화 / 참조 호출: DwarfToken
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultShaman.java#L68) **`debuff(Char enemy)`**: 개별 처리 / 상태 선택 / 참조 호출: Buff.prolong
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultShaman.java#L83) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultShaman.java#L89) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultShaman.java#L97) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultShaman.java#L103) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 247. [`VaultSkeleton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultSkeleton.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.quest.vault` / 본문 65행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultSkeleton.java#L30) `class VaultSkeleton  extends Skeleton`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultSkeleton.java#L45) **`attackSkill(Char target)`**: 전투 관련
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultSkeleton.java#L50) **`lootChance()`**: 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultSkeleton.java#L55) **`createLoot()`**: 생성·초기화 / 참조 호출: DwarfToken
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultSkeleton.java#L60) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 248. [`Rat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 83행 / 타입 1개 / 필드 1개 / 메서드 6개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L31) `class Rat  extends Mob`

### 변수·상수 (단일 행 선언)

- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L69) `String RAT_ALLY` 초기식: `"rat_ally"`

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L43) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.act
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L55) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L60) **`attackSkill(Char target)`**: 전투 관련
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L65) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L72) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L78) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 249. [`RipperDemon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 294행 / 타입 2개 / 필드 7개 / 메서드 11개.

### 타입·상속 선언

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L46) `class RipperDemon  extends Mob`
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L138) `class Hunting  extends Mob.Hunting`

### 변수·상수 (단일 행 선언)

- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L91) `String LAST_ENEMY_POS` 초기식: `"last_enemy_pos"`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L92) `String LEAP_POS` 초기식: `"leap_pos"`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L93) `String LEAP_CD` 초기식: `"leap_cd"`
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L111) `int lastEnemyPos` 초기식: `-1`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L135) `int leapPos` 초기식: `-1`
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L136) `float leapCooldown` 초기식: `0`
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L156) `int endPos`

### 함수·메서드 역할과 내부 연결

- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L67) **`spawningWeight()`**: 개별 처리
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L72) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L77) **`attackSkill(Char target)`**: 전투 관련
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L82) **`attackDelay()`**: 전투 관련 / 참조 호출: super.attackDelay
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L87) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L96) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L104) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getFloat
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L114) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.act
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L141) **`act(boolean enemyInFOV, boolean justAlerted)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Random.NormalIntRange, Ballistica, Actor.findChar, Dungeon.level.trueDistance, sprite.jump, Callback, call, hit, Buff.affect
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L155) **`findChar(leapPos)`**: 조회·탐색
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RipperDemon.java#L192) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: hit, Buff.affect, set, damageRoll, leapVictim.sprite.flash, Sample.INSTANCE.play, leapVictim.sprite.showStatus, leapVictim.defenseVerb, Actor.add

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 250. [`RotHeart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 141행 / 타입 1개 / 필드 0개 / 메서드 11개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java#L37) `class RotHeart  extends Mob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java#L55) **`act()`**: 시간·상태 갱신 / 참조 호출: super.act
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java#L61) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: destroy, sprite.die, super.damage
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java#L72) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기·반복 / 참조 호출: GameScene.add, Blob.seed, super.defenseProc
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java#L87) **`beckon(int cell)`**: 개별 처리
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java#L92) **`getCloser(int target)`**: 조회·탐색
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java#L97) **`destroy()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.destroy, level.mobs.toArray, level.mobs.size, mob.die
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java#L109) **`die(Object cause)`**: 개별 처리 / 참조 호출: super.die, Dungeon.level.drop, Rotberry.Seed, sprite.drop
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java#L117) **`reset()`**: 생성·초기화
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java#L122) **`damageRoll()`**: 전투 관련
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java#L127) **`attackSkill(Char target)`**: 전투 관련
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotHeart.java#L132) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 251. [`RotLasher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 134행 / 타입 2개 / 필드 0개 / 메서드 11개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L37) `class RotLasher  extends Mob`
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L125) `class Waiting  extends Mob.Wandering`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L58) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, sprite.showStatusWithIcon, Integer.toString, Math.min, super.act
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L67) **`damage(int dmg, Object src)`**: 전투 관련 / 조건 분기 / 참조 호출: destroy, sprite.die, super.damage
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L77) **`attack(Char enemy, float dmgMulti, float dmgBonus, float accMulti)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attack
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L85) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 참조 호출: super.attackProc, Buff.affect
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L92) **`reset()`**: 생성·초기화
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L97) **`getCloser(int target)`**: 조회·탐색
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L102) **`getFurther(int target)`**: 조회·탐색
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L107) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L112) **`attackSkill(Char target)`**: 전투 관련
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L117) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/RotLasher.java#L128) **`noticeEnemy()`**: 개별 처리 / 참조 호출: spend, super.noticeEnemy

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 252. [`Scorpio.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Scorpio.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 118행 / 타입 1개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Scorpio.java#L39) `class Scorpio  extends Mob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Scorpio.java#L58) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Scorpio.java#L63) **`attackSkill(Char target)`**: 전투 관련
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Scorpio.java#L68) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Scorpio.java#L73) **`canAttack(Char enemy)`**: 조건 판정 / 참조 호출: Dungeon.level.adjacent, super.canAttack, Ballistica
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Scorpio.java#L79) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, Random.Int, Buff.prolong
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Scorpio.java#L89) **`getCloser(int target)`**: 조회·탐색 / 조건 분기 / 참조 호출: getFurther, super.getCloser
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Scorpio.java#L98) **`aggro(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.length, super.aggro
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Scorpio.java#L108) **`createLoot()`**: 생성·초기화 / 반복 / 참조 호출: Random.oneOf, Reflection.newInstance

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 253. [`Senior.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Senior.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 51행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Senior.java#L28) `class Senior  extends Monk`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Senior.java#L38) **`move(int step, boolean travelling)`**: 개별 처리 / 조건 분기 / 참조 호출: super.move
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Senior.java#L46) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 254. [`Shaman.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 195행 / 타입 5개 / 필드 0개 / 메서드 15개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L44) `class Shaman  extends Mob`
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L111) `class EarthenBolt`
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L151) `class RedShaman  extends Shaman`
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L162) `class BlueShaman  extends Shaman`
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L173) `class PurpleShaman  extends Shaman`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L58) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L63) **`attackSkill(Char target)`**: 전투 관련
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L68) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L73) **`canAttack(Char enemy)`**: 조건 판정 / 참조 호출: super.canAttack, Ballistica
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L79) **`lootChance()`**: 개별 처리 / 참조 호출: super.lootChance, Math.pow
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L86) **`createLoot()`**: 생성·초기화 / 참조 호출: super.createLoot
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L91) **`doAttack(Char enemy)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, Ballistica, super.doAttack, sprite.zap, zap
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L113) **`zap()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: spend, Invisibility.dispel, hit, Random.Int, debuff, Sample.INSTANCE.play, Random.NormalIntRange, Math.round, AscensionChallenge.statModifier
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L139) **`debuff(Char enemy)`**: 개별 처리
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L141) **`onZapComplete()`**: 이벤트·효과 실행 / 참조 호출: zap, next
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L147) **`description()`**: 개별 처리 / 참조 호출: super.description, Messages.get
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L157) **`debuff(Char enemy)`**: 개별 처리 / 참조 호출: Buff.prolong
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L168) **`debuff(Char enemy)`**: 개별 처리 / 참조 호출: Buff.prolong
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L179) **`debuff(Char enemy)`**: 개별 처리 / 참조 호출: Buff.prolong
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Shaman.java#L184) **`random()`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Float

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 255. [`Skeleton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Skeleton.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 167행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Skeleton.java#L47) `class Skeleton  extends Mob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Skeleton.java#L66) **`damageRoll()`**: 전투 관련 / 참조 호출: Random.NormalIntRange
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Skeleton.java#L71) **`die(Object cause)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.die, findChar, ch.isAlive, Math.round, Random.NormalIntRange, AscensionChallenge.statModifier, ch.buff, rockArmor.absorb, armor.absorb
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Skeleton.java#L144) **`lootChance()`**: 개별 처리 / 참조 호출: super.lootChance, Math.pow
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Skeleton.java#L151) **`createLoot()`**: 생성·초기화 / 참조 호출: super.createLoot
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Skeleton.java#L157) **`attackSkill(Char target)`**: 전투 관련
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Skeleton.java#L162) **`drRoll()`**: 개별 처리 / 참조 호출: super.drRoll, Random.NormalIntRange

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":25,"fields":9,"methods":93}

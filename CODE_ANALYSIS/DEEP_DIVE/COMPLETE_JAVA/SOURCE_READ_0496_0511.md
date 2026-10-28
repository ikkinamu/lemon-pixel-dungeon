# Java 파일별 소스 구현 해설 496–511

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 496. [`BrokenHilt.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/BrokenHilt.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.remains` / 본문 42행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/BrokenHilt.java#L31) `class BrokenHilt  extends RemainsItem`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/BrokenHilt.java#L38) **`doEffect(Hero hero)`**: 개별 처리 / 참조 호출: Buff.affect, set, Math.max, Sample.INSTANCE.play

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 497. [`BrokenStaff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/BrokenStaff.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.remains` / 본문 44행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/BrokenStaff.java#L30) `class BrokenStaff  extends RemainsItem`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/BrokenStaff.java#L37) **`doEffect(Hero hero)`**: 개별 처리 / 참조 호출: hero.belongings.charge, ScrollOfRecharging.charge, Sample.INSTANCE.play

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 498. [`CloakScrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/CloakScrap.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.remains` / 본문 44행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/CloakScrap.java#L31) `class CloakScrap  extends RemainsItem`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/CloakScrap.java#L38) **`doEffect(Hero hero)`**: 개별 처리 / 참조 호출: ArtifactRecharge.chargeArtifacts, ScrollOfRecharging.charge, Sample.INSTANCE.play

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 499. [`RemainsItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/RemainsItem.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.remains` / 본문 99행 / 타입 1개 / 필드 1개 / 메서드 7개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/RemainsItem.java#L32) `class RemainsItem  extends Item`

### 변수·상수 (단일 행 선언)

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/RemainsItem.java#L40) `String AC_USE` 초기식: `"USE"`

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/RemainsItem.java#L43) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/RemainsItem.java#L50) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, hero.sprite.operate, Catalog.countUse, getClass, doEffect, hero.spendAndNext, detach
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/RemainsItem.java#L64) **`doEffect(Hero hero)`**: 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/RemainsItem.java#L67) **`isIdentified()`**: 조건 판정
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/RemainsItem.java#L72) **`isUpgradable()`**: 조건 판정
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/RemainsItem.java#L77) **`value()`**: 개별 처리
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/RemainsItem.java#L81) **`get(HeroClass cls)`**: 조회·탐색 / 상태 선택 / 참조 호출: SealShard, BrokenStaff, CloakScrap, BowFragment, BrokenHilt, TornPage

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 500. [`SealShard.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/SealShard.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.remains` / 본문 47행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/SealShard.java#L33) `class SealShard  extends RemainsItem`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/SealShard.java#L40) **`doEffect(Hero hero)`**: 개별 처리 / 참조 호출: Buff.affect, incShield, Math.round, hero.sprite.showStatusWithIcon, Integer.toString, Sample.INSTANCE.play

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 501. [`TornPage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/TornPage.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.remains` / 본문 46행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/TornPage.java#L31) `class TornPage  extends RemainsItem`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/TornPage.java#L38) **`doEffect(Hero hero)`**: 개별 처리 / 참조 호출: Math.round, Math.min, hero.sprite.showStatusWithIcon, Integer.toString, Sample.INSTANCE.play

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 502. [`Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 460행 / 타입 2개 / 필드 7개 / 메서드 44개.

### 타입·상속 선언

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L50) `class Ring  extends KindofMisc`
- [L430](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L430) `class RingBuff  extends Buff`

### 변수·상수 (단일 행 선언)

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L52) `Buff buff`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L53) `Class<? extends RingBuff> buffClass`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L72) `ItemStatusHandler<Ring> handler`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L74) `String gem`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L77) `float levelsToID` 초기식: `1`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L109) `boolean anonymous` 초기식: `false`
- [L315](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L315) `String LEVELS_TO_ID` 초기식: `"levels_to_ID"`

### 함수·메서드 역할과 내부 연결

- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L80) **`initGems()`**: 생성·초기화
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L84) **`clearGems()`**: 상태 갱신
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L88) **`save(Bundle bundle)`**: 저장·복원 / 참조 호출: handler.save
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L92) **`saveSelectively(Bundle bundle, ArrayList<Item> items)`**: 저장·복원 / 참조 호출: handler.saveSelectively
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L97) **`restore(Bundle bundle)`**: 저장·복원
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L101) **`Ring()`**: 개별 처리 / 참조 호출: reset
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L110) **`anonymize()`**: 개별 처리 / 조건 분기 / 참조 호출: isKnown
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L115) **`reset()`**: 생성·초기화 / 조건 분기 / 참조 호출: super.reset, handler.contains, handler.image, handler.label
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L127) **`activate(Char ch)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: buff.detach, buff, buff.attachTo
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L137) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doUnequip, buff.detach
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L154) **`isKnown()`**: 조건 판정 / 참조 호출: handler.isKnown
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L158) **`setKnown()`**: 상태 갱신 / 조건 분기 / 참조 호출: isKnown, handler.know, Dungeon.hero.isAlive, Catalog.setSeen, getClass, Statistics.itemTypesDiscovered.add
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L172) **`name()`**: 개별 처리 / 참조 호출: isKnown, super.name, Messages.get
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L177) **`desc()`**: 개별 처리 / 참조 호출: isKnown, super.desc, Messages.get
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L182) **`info()`**: 개별 처리 / 조건 분기 / 참조 호출: handler.isKnown, desc, super.info, isEquipped, Messages.get, isIdentified, isKnown, statsInfo
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L211) **`statsInfo()`**: 개별 처리
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L215) **`upgradeStat1(int level)`**: 개별 처리
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L219) **`upgradeStat2(int level)`**: 개별 처리
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L223) **`upgradeStat3(int level)`**: 개별 처리
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L228) **`upgrade()`**: 개별 처리 / 조건 분기 / 참조 호출: super.upgrade, Random.Int
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L239) **`isIdentified()`**: 조건 판정 / 참조 호출: super.isIdentified, isKnown
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L244) **`identify(boolean byHero)`**: 개별 처리 / 참조 호출: setKnown, super.identify
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L250) **`setIDReady()`**: 상태 갱신
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L254) **`readyToIdentify()`**: 개별 처리 / 참조 호출: isIdentified
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L259) **`random()`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Int, level, Random.Float
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L280) **`getKnown()`**: 조회·탐색 / 참조 호출: handler.known
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L284) **`getUnknown()`**: 조회·탐색 / 참조 호출: handler.unknown
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L288) **`allKnown()`**: 개별 처리 / 참조 호출: handler.known, size
- [L293](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L293) **`value()`**: 개별 처리 / 조건 분기 / 참조 호출: level
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L311) **`buff()`**: 개별 처리
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L318) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L324](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L324) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getFloat
- [L329](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L329) **`onHeroGainExp(float levelPercent, Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: isIdentified, isEquipped, Talent.itemIDSpeedFactor, ShardOfOblivion.passiveIDDisabled, GLog.p, Messages.get, name, setIDReady, identify
- [L349](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L349) **`buffedLvl()`**: 개별 처리 / 조건 분기 / 참조 호출: super.buffedLvl, Dungeon.hero.buff
- [L357](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L357) **`getBonus(Char target, Class<?extends RingBuff> type)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: target.buff, target.buffs, buff.level, spiritForm.ring, soloBonus
- [L373](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L373) **`getBuffedBonus(Char target, Class<?extends RingBuff> type)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: target.buff, target.buffs, buff.buffedLvl, ring, soloBuffedBonus
- [L389](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L389) **`soloBonus()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Ring.this.level
- [L398](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L398) **`soloBuffedBonus()`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Ring.this.buffedLvl
- [L407](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L407) **`combinedBonus(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.ring, getClass, soloBonus, hero.belongings.misc
- [L419](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L419) **`combinedBuffedBonus(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.ring, getClass, soloBuffedBonus, hero.belongings.misc
- [L433](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L433) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, cooldown, target.cooldown, spend
- [L445](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L445) **`act()`**: 시간·상태 갱신 / 참조 호출: spend
- [L450](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L450) **`level()`**: 개별 처리 / 참조 호출: Ring.this.soloBonus
- [L454](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java#L454) **`buffedLvl()`**: 개별 처리 / 참조 호출: Ring.this.soloBuffedBonus

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 503. [`RingOfAccuracy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfAccuracy.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 67행 / 타입 2개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfAccuracy.java#L29) `class RingOfAccuracy  extends Ring`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfAccuracy.java#L64) `class Accuracy  extends RingBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfAccuracy.java#L36) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, Math.pow, soloBuffedBonus, isEquipped, combinedBuffedBonus
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfAccuracy.java#L50) **`upgradeStat1(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Messages.decimalFormat, Math.pow
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfAccuracy.java#L56) **`buff()`**: 개별 처리 / 참조 호출: Accuracy
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfAccuracy.java#L60) **`accuracyMultiplier(Char target)`**: 개별 처리 / 참조 호출: Math.pow, getBuffedBonus

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 504. [`RingOfArcana.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfArcana.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 68행 / 타입 2개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfArcana.java#L29) `class RingOfArcana  extends Ring`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfArcana.java#L64) `class Arcana  extends RingBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfArcana.java#L36) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, Math.pow, soloBuffedBonus, isEquipped, combinedBuffedBonus
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfArcana.java#L50) **`upgradeStat1(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Messages.decimalFormat, Math.pow
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfArcana.java#L56) **`buff()`**: 개별 처리 / 참조 호출: Arcana
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfArcana.java#L60) **`enchantPowerMultiplier(Char target)`**: 개별 처리 / 참조 호출: Math.pow, getBuffedBonus

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 505. [`RingOfElements.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfElements.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 104행 / 타입 2개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfElements.java#L41) `class RingOfElements  extends Ring`
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfElements.java#L100) `class Resistance  extends RingBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfElements.java#L48) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, Math.pow, soloBuffedBonus, isEquipped, combinedBuffedBonus
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfElements.java#L62) **`upgradeStat1(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Messages.decimalFormat, Math.pow
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfElements.java#L68) **`buff()`**: 개별 처리 / 참조 호출: Resistance
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfElements.java#L88) **`resist(Char target, Class effect)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: getBuffedBonus, c.isAssignableFrom, Math.pow

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 506. [`RingOfEnergy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEnergy.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 91행 / 타입 2개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEnergy.java#L32) `class RingOfEnergy  extends Ring`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEnergy.java#L88) `class Energy  extends RingBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEnergy.java#L39) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, Math.pow, soloBuffedBonus, isEquipped, combinedBuffedBonus
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEnergy.java#L54) **`upgradeStat1(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Messages.decimalFormat, Math.pow
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEnergy.java#L60) **`buff()`**: 개별 처리 / 참조 호출: Energy
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEnergy.java#L64) **`wandChargeMultiplier(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.pow, getBuffedBonus, hasTalent, pointsInTalent
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEnergy.java#L74) **`artifactChargeMultiplier(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.pow, getBuffedBonus, hasTalent, pointsInTalent
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEnergy.java#L84) **`armorChargeMultiplier(Char target)`**: 개별 처리 / 참조 호출: Math.pow, getBuffedBonus

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 507. [`RingOfEvasion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEvasion.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 67행 / 타입 2개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEvasion.java#L29) `class RingOfEvasion  extends Ring`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEvasion.java#L64) `class Evasion  extends RingBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEvasion.java#L36) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, Math.pow, soloBuffedBonus, isEquipped, combinedBuffedBonus
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEvasion.java#L50) **`upgradeStat1(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Messages.decimalFormat, Math.pow
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEvasion.java#L56) **`buff()`**: 개별 처리 / 참조 호출: Evasion
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEvasion.java#L60) **`evasionMultiplier(Char target)`**: 개별 처리 / 참조 호출: Math.pow, getBuffedBonus

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 508. [`RingOfForce.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 361행 / 타입 3개 / 필드 5개 / 메서드 25개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L42) `class RingOfForce  extends Ring`
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L170) `class Force  extends RingBuff`
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L305) `class BrawlersStance  extends Buff`

### 변수·상수 (단일 행 선언)

- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L175) `String AC_ABILITY` 초기식: `"ABILITY"`
- [L313](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L313) `boolean active` 초기식: `true`
- [L314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L314) `int minTurnsLeft`
- [L342](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L342) `String ACTIVE` 초기식: `"active"`
- [L343](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L343) `String MIN_TURNS_LEFT` 초기식: `"min_turns_left"`

### 함수·메서드 역할과 내부 연결

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L50) **`buff()`**: 개별 처리 / 참조 호출: Force
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L54) **`armedDamageBonus(Char ch)`**: 개별 처리 / 참조 호출: getBuffedBonus
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L59) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doUnequip, hero.buff
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L73) **`tier(int str)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L82) **`damageRoll(Hero hero)`**: 전투 관련 / 조건 분기 / 참조 호출: hero.buff, ring, getBuffedBonus, tier, hero.STR, Hero.heroDamageIntRange, min, max, Math.round
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L110) **`min(int lvl, float tier)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, Math.round
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L120) **`max(int lvl, float tier)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.max, Math.round
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L130) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: tier, Dungeon.hero.STR, isIdentified, soloBuffedBonus, Messages.get, min, max, isEquipped, combinedBuffedBonus
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L146) **`upgradeStat1(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, tier, Dungeon.hero.STR, min, max
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L153) **`upgradeStat2(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Integer.toString
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L159) **`upgradeStat3(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, tier, Dungeon.hero.STR, Math.round, min, max
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L178) **`activate(Char ch)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.activate, Buff.affect
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L186) **`defaultAction()`**: 개별 처리 / 조건 분기 / 참조 호출: super.defaultAction
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L195) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, actions.add
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L204) **`actionName(String action, Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: action.equals, Messages.upperCase, Messages.get, super.actionName
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L213) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: action.equals, isEquipped, GLog.w, Messages.get, hero.buff, reset, BuffIndicator.refreshHero, AttackIndicator.updateState, hero.sprite.operate
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L238) **`info()`**: 개별 처리 / 조건 분기 / 참조 호출: super.info, isIdentified, isEquipped, getBuffedBonus, soloBuffedBonus, tier, Dungeon.hero.STR, Math.round, Messages.get
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L257) **`fightingUnarmed(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.attackingWeapon, hero.buff, AttackIndicator.updateState
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L279) **`unarmedGetsWeaponEnchantment(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.attackingWeapon, hero.buff
- [L293](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L293) **`unarmedGetsWeaponAugment(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.attackingWeapon, hero.buff
- [L316](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L316) **`reset()`**: 생성·초기화 / 조건 분기 / 참조 호출: target.sprite.showStatus, Messages.titleCase, name
- [L326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L326) **`icon()`**: 개별 처리
- [L331](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L331) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: detach, spend
- [L346](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L346) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L353](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java#L353) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getBoolean, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 509. [`RingOfFuror.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfFuror.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 67행 / 타입 2개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfFuror.java#L29) `class RingOfFuror  extends Ring`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfFuror.java#L64) `class Furor  extends RingBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfFuror.java#L36) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, Math.pow, soloBuffedBonus, isEquipped, combinedBuffedBonus
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfFuror.java#L50) **`upgradeStat1(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Messages.decimalFormat, Math.pow
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfFuror.java#L56) **`buff()`**: 개별 처리 / 참조 호출: Furor
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfFuror.java#L60) **`attackSpeedMultiplier(Char target)`**: 전투 관련 / 참조 호출: Math.pow, getBuffedBonus

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 510. [`RingOfHaste.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 67행 / 타입 2개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java#L29) `class RingOfHaste  extends Ring`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java#L64) `class Haste  extends RingBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java#L36) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, Messages.decimalFormat, Math.pow, soloBuffedBonus, isEquipped, combinedBuffedBonus
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java#L50) **`upgradeStat1(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Messages.decimalFormat, Math.pow
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java#L56) **`buff()`**: 개별 처리 / 참조 호출: Haste
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java#L60) **`speedMultiplier(Char target)`**: 개별 처리 / 참조 호출: Math.pow, getBuffedBonus

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 511. [`RingOfMight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.rings` / 본문 122행 / 타입 2개 / 필드 0개 / 메서드 11개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L32) `class RingOfMight  extends Ring`
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L118) `class Might  extends RingBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L40) **`doEquip(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doEquip, hero.updateHT
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L50) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doUnequip, hero.updateHT
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L60) **`upgrade()`**: 개별 처리 / 참조 호출: super.upgrade, updateTargetHT
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L67) **`level(int value)`**: 개별 처리 / 참조 호출: super.level, updateTargetHT
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L73) **`updateTargetHT()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: updateHT
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L79) **`statsInfo()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, soloBonus, Messages.decimalFormat, Math.pow, soloBuffedBonus, isEquipped, combinedBuffedBonus, getBonus
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L94) **`upgradeStat1(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Integer.toString
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L100) **`upgradeStat2(int level)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, Messages.decimalFormat, Math.pow
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L106) **`buff()`**: 개별 처리 / 참조 호출: Might
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L110) **`strengthBonus(Char target)`**: 개별 처리 / 참조 호출: getBonus
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java#L114) **`HTMultiplier(Char target)`**: 개별 처리 / 참조 호출: Math.pow, getBuffedBonus

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":27,"fields":13,"methods":122}

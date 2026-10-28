# Java 파일별 소스 구현 해설 528–543

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 528. [`InventoryScroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 149행 / 타입 2개 / 필드 2개 / 메서드 14개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L34) `class InventoryScroll  extends Scroll`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L56) `class WndConfirmCancel  extends WndOptions`

### 변수·상수 (단일 행 선언)

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L36) `boolean identifiedByUse` 초기식: `false`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L89) `Class<?extends Bag> preferredBag` 초기식: `null`

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L39) **`doRead()`**: 개별 처리 / 조건 분기 / 참조 호출: isKnown, identify, detach, GameScene.selectItem
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L52) **`confirmCancelation()`**: 개별 처리 / 참조 호출: GameScene.show, WndConfirmCancel
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L58) **`WndConfirmCancel()`**: 개별 처리 / 참조 호출: ItemSprite, Messages.titleCase, name, Messages.get
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L66) **`onSelect(int index)`**: 이벤트·효과 실행 / 상태 선택 / 참조 호출: curUser.spendAndNext, GameScene.selectItem
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L77) **`onBackPressed()`**: 이벤트·효과 실행
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L79) **`getItemSelector()`**: 조회·탐색
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L85) **`inventoryTitle()`**: 개별 처리 / 참조 호출: Messages.get
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L91) **`usableOnItem(Item item)`**: 개별 처리
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L95) **`onItemSelected(Item item)`**: 이벤트·효과 실행
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L97) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, inventoryTitle, preferredBag, itemSelectable, usableOnItem, onSelect, detach, onItemSelected, readAnimation
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L100) **`textPrompt()`**: 개별 처리 / 참조 호출: inventoryTitle
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L105) **`preferredBag()`**: 개별 처리
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L110) **`itemSelectable(Item item)`**: 개별 처리 / 참조 호출: usableOnItem
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java#L115) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: detach, onItemSelected, readAnimation, Sample.INSTANCE.play, confirmCancelation, curUser.spendAndNext

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 529. [`Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 374행 / 타입 3개 / 필드 7개 / 메서드 32개.

### 타입·상속 선언

- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L67) `class Scroll  extends Item`
- [L287](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L287) `class PlaceHolder  extends Scroll`
- [L308](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L308) `class ScrollToStone  extends Recipe`

### 변수·상수 (단일 행 선언)

- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L69) `String AC_READ` 초기식: `"READ"`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L71) `float TIME_TO_READ` 초기식: `1f`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L90) `ItemStatusHandler<Scroll> handler`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L92) `String rune`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L95) `float talentFactor` 초기식: `1`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L97) `float talentChance` 초기식: `1`
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L146) `boolean anonymous` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L105) **`initLabels()`**: 생성·초기화
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L109) **`clearLabels()`**: 상태 갱신
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L113) **`save(Bundle bundle)`**: 저장·복원 / 참조 호출: handler.save
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L117) **`saveSelectively(Bundle bundle, ArrayList<Item> items)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: classes.contains, ExoticScroll.exoToReg.get, i.getClass, classes.add, handler.saveClassesSelectively
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L134) **`restore(Bundle bundle)`**: 저장·복원
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L138) **`Scroll()`**: 개별 처리 / 참조 호출: reset
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L147) **`anonymize()`**: 개별 처리 / 조건 분기 / 참조 호출: isKnown
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L154) **`reset()`**: 생성·초기화 / 조건 분기 / 참조 호출: super.reset, handler.contains, handler.image, handler.label
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L166) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L173) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, hero.buff, GLog.w, Messages.get, isCursed, GLog.n, doRead
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L194) **`doRead()`**: 개별 처리
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L196) **`readAnimation()`**: 개별 처리 / 조건 분기 / 참조 호출: Invisibility.dispel, curUser.spend, curUser.busy, read, Catalog.countUse, getClass, Random.Float, Talent.onScrollUsed
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L211) **`isKnown()`**: 조건 판정 / 참조 호출: handler.isKnown
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L215) **`setKnown()`**: 상태 갱신 / 조건 분기 / 참조 호출: isKnown, handler.know, updateQuickslot, Dungeon.hero.isAlive, Catalog.setSeen, getClass, Statistics.itemTypesDiscovered.add
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L230) **`identify(boolean byHero)`**: 개별 처리 / 조건 분기 / 참조 호출: super.identify, isKnown, setKnown
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L240) **`name()`**: 개별 처리 / 참조 호출: isKnown, super.name, Messages.get
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L245) **`info()`**: 개별 처리 / 참조 호출: handler.isKnown, desc, super.info
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L251) **`desc()`**: 개별 처리 / 참조 호출: isKnown, super.desc, Messages.get
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L256) **`isUpgradable()`**: 조건 판정
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L261) **`isIdentified()`**: 조건 판정 / 참조 호출: isKnown
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L265) **`getKnown()`**: 조회·탐색 / 참조 호출: handler.known
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L269) **`getUnknown()`**: 조회·탐색 / 참조 호출: handler.unknown
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L273) **`allKnown()`**: 개별 처리 / 참조 호출: handler.known, size
- [L278](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L278) **`value()`**: 개별 처리
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L283) **`energyVal()`**: 개별 처리
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L294) **`isSimilar(Item item)`**: 조건 판정 / 참조 호출: ExoticScroll.regToExo.containsKey, item.getClass, ExoticScroll.regToExo.containsValue
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L300) **`doRead()`**: 개별 처리
- [L303](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L303) **`info()`**: 개별 처리
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L327) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기 / 참조 호출: ingredients.size, ingredients.get, stones.containsKey, getClass
- [L338](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L338) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L343](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L343) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기 / 참조 호출: testIngredients, ingredients.get, s.quantity, ShatteredPixelDungeon.scene, s.isIdentified, showIdentify, s.identify, Reflection.newInstance, stones.get
- [L361](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java#L361) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기 / 참조 호출: testIngredients, ingredients.get, s.isKnown, Runestone.PlaceHolder, quantity, Reflection.newInstance, stones.get, s.getClass

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 530. [`ScrollOfIdentify.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 88행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java#L36) `class ScrollOfIdentify  extends InventoryScroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java#L45) **`usableOnItem(Item item)`**: 개별 처리 / 참조 호출: item.isIdentified
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java#L50) **`onItemSelected(Item item)`**: 이벤트·효과 실행 / 참조 호출: sprite.parent.add, Identification, curUser.sprite.center, offset, IDItem
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java#L57) **`IDItem(Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: ShardOfOblivion.passiveIDDisabled, setIDReady, GLog.p, Messages.get, item.name, item.identify, GLog.i, item.title, Badges.validateItemLevelAquired
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java#L84) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 531. [`ScrollOfLullaby.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfLullaby.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 68행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfLullaby.java#L35) `class ScrollOfLullaby  extends Scroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfLullaby.java#L42) **`doRead()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: detach, curUser.sprite.centerEmitter, start, Speck.factory, Sample.INSTANCE.play, level.mobs.toArray, Buff.affect, mob.sprite.centerEmitter, GLog.i
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfLullaby.java#L64) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 532. [`ScrollOfMagicMapping.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMagicMapping.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 97행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMagicMapping.java#L36) `class ScrollOfMagicMapping  extends Scroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMagicMapping.java#L43) **`doRead()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: detach, Dungeon.level.length, Dungeon.level.discover, GameScene.discoverTile, discover, GameScene.updateFog, GLog.i, Messages.get, Sample.INSTANCE.play
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMagicMapping.java#L89) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMagicMapping.java#L93) **`discover(int cell)`**: 개별 처리 / 참조 호출: CellEmitter.get, start, Speck.factory

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 533. [`ScrollOfMirrorImage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMirrorImage.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 100행 / 타입 1개 / 필드 1개 / 메서드 4개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMirrorImage.java#L39) `class ScrollOfMirrorImage  extends Scroll`

### 변수·상수 (단일 행 선언)

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMirrorImage.java#L45) `int NIMAGES` 초기식: `2`

### 함수·메서드 역할과 내부 연결

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMirrorImage.java#L48) **`doRead()`**: 개별 처리 / 조건 분기 / 참조 호출: detach, spawnImages, GLog.i, Messages.get, identify, Sample.INSTANCE.play, readAnimation
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMirrorImage.java#L62) **`spawnImages(Hero hero, int nImages)`**: 개별 처리 / 참조 호출: spawnImages
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMirrorImage.java#L67) **`spawnImages(Hero hero, int pos, int nImages)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.findChar, respawnPoints.add, respawnPoints.size, Random.index, MirrorImage, mob.duplicate, GameScene.add, ScrollOfTeleportation.appear, respawnPoints.get
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMirrorImage.java#L96) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 534. [`ScrollOfRage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRage.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 67행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRage.java#L36) `class ScrollOfRage  extends Scroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRage.java#L43) **`doRead()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: detach, level.mobs.toArray, mob.beckon, Buff.prolong, GLog.w, Messages.get, identify, curUser.sprite.centerEmitter, start
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRage.java#L63) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 535. [`ScrollOfRecharging.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRecharging.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 71행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRecharging.java#L36) `class ScrollOfRecharging  extends Scroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRecharging.java#L43) **`doRead()`**: 개별 처리 / 참조 호출: detach, Buff.affect, charge, Sample.INSTANCE.play, GLog.i, Messages.get, SpellSprite.show, identify, readAnimation
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRecharging.java#L59) **`charge(Char user)`**: 개별 처리 / 조건 분기 / 참조 호출: user.sprite.centerEmitter, e.burst
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRecharging.java#L67) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 536. [`ScrollOfRemoveCurse.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRemoveCurse.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 165행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRemoveCurse.java#L45) `class ScrollOfRemoveCurse  extends InventoryScroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRemoveCurse.java#L53) **`doRead()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Actor.findChar, identify, Sample.INSTANCE.play, readAnimation, Flare, show, curUser.buff, Degrade.detach, detach
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRemoveCurse.java#L81) **`usableOnItem(Item item)`**: 개별 처리 / 참조 호출: uncursable
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRemoveCurse.java#L85) **`uncursable(Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: item.isEquipped, Dungeon.hero.buff, item.isIdentified, hasCurseEnchant, hasCurseGlyph
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRemoveCurse.java#L100) **`onItemSelected(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Flare, show, uncurse, curUser.buff, Degrade.detach, GLog.p, Messages.get, GLog.i
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRemoveCurse.java#L117) **`uncurse(Hero hero, Item... items)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: w.hasCurseEnchant, w.enchant, a.hasCurseGlyph, a.inscribe, updateLevel, hero.sprite.emitter, start, hero.updateHT, updateQuickslot
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRemoveCurse.java#L161) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 537. [`ScrollOfRetribution.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRetribution.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 89행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRetribution.java#L38) `class ScrollOfRetribution  extends Scroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRetribution.java#L45) **`doRead()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: detach, GameScene.flash, Math.min, Sample.INSTANCE.play, GLog.i, Messages.get, level.mobs.toArray, targets.add, mob.damage
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRetribution.java#L85) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 538. [`ScrollOfTeleportation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 340행 / 타입 1개 / 필드 0개 / 메서드 9개.

### 타입·상속 선언

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L53) `class ScrollOfTeleportation  extends Scroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L60) **`doRead()`**: 개별 처리 / 조건 분기 / 참조 호출: detach, Sample.INSTANCE.play, teleportPreferringUnseen, readAnimation, identify
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L72) **`teleportToLocation(Char ch, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: PathFinder.buildDistanceMap, BArray.or, Actor.findChar, GLog.w, Messages.get, appear, Dungeon.level.occupyCell, Buff.detach, Dungeon.observe
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L94) **`teleportChar(Char ch)`**: 개별 처리 / 참조 호출: teleportChar
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L98) **`teleportChar(Char ch, Class source)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: teleportInNonRegularLevel, Char.hasProp, ch.isImmune, GLog.w, Messages.get, Dungeon.level.randomRespawnCell, appear, Dungeon.level.occupyCell, Buff.detach
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L142) **`teleportPreferringUnseen(Hero hero)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: teleportInNonRegularLevel, level.rooms, r.getPoints, level.pointToCell, r.charPlaceablePoints, Actor.findChar, candidates.add, candidates.isEmpty, teleportChar
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L221) **`teleportInNonRegularLevel(Char ch, boolean preferNotSeen)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Char.hasProp, GLog.w, Messages.get, BArray.and, PathFinder.buildDistanceMap, Dungeon.level.length, Actor.findChar, notSeenValid.add, visibleValid.add
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L284) **`appear(Char ch, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: ch.sprite.interruptMotion, Sample.INSTANCE.play, CellEmitter.get, start, Speck.factory, ch.move, ch.sprite.place, ch.sprite.alpha, sprite.parent.add
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L318) **`appearVFX(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: Sample.INSTANCE.play, Dungeon.level.occupyCell, ch.sprite.alpha, sprite.parent.add, AlphaTweener, ch.sprite.emitter, start, Speck.factory
- [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java#L336) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 539. [`ScrollOfTerror.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTerror.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 82행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTerror.java#L36) `class ScrollOfTerror  extends Scroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTerror.java#L43) **`doRead()`**: 개별 처리 / 조건 분기·반복·상태 선택 / 참조 호출: detach, Flare, color, show, Sample.INSTANCE.play, level.mobs.toArray, Buff.affect, curUser.id, mob.buff
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTerror.java#L78) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 540. [`ScrollOfTransmutation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 405행 / 타입 1개 / 필드 0개 / 메서드 16개.

### 타입·상속 선언

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L60) `class ScrollOfTransmutation  extends InventoryScroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L71) **`usableOnItem(Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: item.getClass, item.quantity
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L100) **`onItemSelected(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: changeItem, GLog.n, Messages.get, curItem.collect, Dungeon.quickslot.getSlot, item.isEquipped, doUnequip, result.collect, Dungeon.level.drop
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L157) **`changeItem(Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: changeStaff, changeTippedDart, changeWeapon, changeScroll, changePotion, changeRing, changeWand, changeSeed, changeStone
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L203) **`changeStaff(MagesStaff staff)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: staff.wandClass, Generator.randomUsingDefaults, Challenges.isItemBlocked, n.getClass, n.level, n.identify, staff.imbueWand
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L222) **`changeTippedDart(TippedDart dart)`**: 개별 처리 / 반복 / 참조 호출: TippedDart.randomTipped, n.getClass, dart.getClass
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L231) **`changeWeapon(Weapon w)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Generator.randomUsingDefaults, Challenges.isItemBlocked, n.getClass, w.getClass, n.level, n.quantity, w.quantity, w.trueLevel, n.upgrade
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L273) **`changeRing(Ring r)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Generator.randomUsingDefaults, Challenges.isItemBlocked, n.getClass, r.getClass, n.level, r.level, n.upgrade, n.degrade
- [L295](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L295) **`changeArtifact(Artifact a)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Generator.randomArtifact, Challenges.isItemBlocked, n.getClass, a.getClass, ghostWeapon, Dungeon.level.drop, ghostArmor, n.transferUpgrade, a.visiblyUpgraded
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L322) **`changeTrinket(Trinket t)`**: 개별 처리 / 반복 / 참조 호출: Generator.random, Challenges.isItemBlocked, n.getClass, t.getClass, n.level, t.trueLevel
- [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L336) **`changeWand(Wand w)`**: 개별 처리 / 반복 / 참조 호출: Generator.randomUsingDefaults, Challenges.isItemBlocked, n.getClass, w.getClass, n.level, w.trueLevel, n.upgrade, n.updateLevel
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L359) **`changeSeed(Plant.Seed s)`**: 개별 처리 / 반복 / 참조 호출: Generator.randomUsingDefaults, n.getClass, s.getClass
- [L369](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L369) **`changeStone(Runestone r)`**: 개별 처리 / 반복 / 참조 호출: Generator.randomUsingDefaults, n.getClass, r.getClass
- [L379](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L379) **`changeScroll(Scroll s)`**: 개별 처리 / 조건 분기 / 참조 호출: Reflection.newInstance, ExoticScroll.exoToReg.get, s.getClass, ExoticScroll.regToExo.get
- [L387](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L387) **`changePotion(Potion p)`**: 개별 처리 / 조건 분기 / 참조 호출: Reflection.newInstance, ExoticPotion.exoToReg.get, p.getClass, ExoticPotion.regToExo.get
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L396) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value
- [L401](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java#L401) **`energyVal()`**: 개별 처리 / 참조 호출: isKnown, super.energyVal

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 541. [`ScrollOfUpgrade.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.scrolls` / 본문 174행 / 타입 1개 / 필드 0개 / 메서드 10개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L45) `class ScrollOfUpgrade  extends InventoryScroll`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L57) **`usableOnItem(Item item)`**: 개별 처리 / 참조 호출: item.isUpgradable
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L62) **`onItemSelected(Item item)`**: 이벤트·효과 실행 / 참조 호출: GameScene.show, WndUpgrade
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L68) **`reShowSelector(boolean force)`**: 개별 처리 / 참조 호출: GameScene.selectItem
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L74) **`getSelector(boolean force)`**: 조회·탐색
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L80) **`upgradeItem(Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: upgrade, Degrade.detach, w.hasCurseEnchant, w.hasGoodEnchant, w.upgrade, removeCurse, weakenCurse, GLog.w, Messages.get
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L149) **`upgrade(Hero hero)`**: 개별 처리 / 참조 호출: hero.sprite.emitter, start, Speck.factory
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L153) **`weakenCurse(Hero hero)`**: 개별 처리 / 참조 호출: GLog.p, Messages.get, hero.sprite.emitter, start
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L158) **`removeCurse(Hero hero)`**: 상태 갱신 / 참조 호출: GLog.p, Messages.get, hero.sprite.emitter, start, Badges.validateClericUnlock
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L165) **`value()`**: 개별 처리 / 참조 호출: isKnown, super.value
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java#L170) **`energyVal()`**: 개별 처리 / 참조 호출: isKnown, super.energyVal

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 542. [`Alchemize.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 307행 / 타입 3개 / 필드 5개 / 메서드 21개.

### 타입·상속 선언

- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L54) `class Alchemize  extends Spell`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L80) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe`
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L141) `class WndAlchemizeItem  extends WndInfoItem`

### 변수·상수 (단일 행 선언)

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L62) `WndBag parentWnd`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L82) `int OUT_QUANTITY` 초기식: `8`
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L143) `float GAP` 초기식: `2`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L144) `int BTN_HEIGHT` 초기식: `18`
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L146) `WndBag owner`

### 함수·메서드 역할과 내부 연결

- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L65) **`onCast(Hero hero)`**: 이벤트·효과 실행 / 참조 호출: GameScene.selectItem
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L70) **`value()`**: 개별 처리
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L76) **`energyVal()`**: 개별 처리
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L85) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기 / 참조 호출: ingredients.size, ingredients.get
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L100) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L105) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: ingredients.get, quantity, sampleOutput
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L112) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: Alchemize, quantity
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L117) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, Messages.get, itemSelectable, Shopkeeper.canSell, item.energyVal, onSelect, GameScene.selectItem, GameScene.show, WndAlchemizeItem
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L119) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L124) **`itemSelectable(Item item)`**: 개별 처리 / 참조 호출: Shopkeeper.canSell, item.energyVal
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L130) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: GameScene.selectItem, GameScene.show, WndAlchemizeItem
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L148) **`WndAlchemizeItem(Item item, WndBag owner)`**: 개별 처리 / 조건 분기 / 참조 호출: Shopkeeper.canSell, item.quantity, item.isUpgradable, PixelScene.renderTextBlock, Messages.get, warn.hardlight, warn.maxWidth, warn.setPos, add
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L169) **`onClick()`**: 이벤트·효과 실행 / 참조 호출: WndTradeItem.sell, hide, consumeAlchemize
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L186) **`onClick()`**: 이벤트·효과 실행 / 참조 호출: WndTradeItem.sellOne, hide, consumeAlchemize
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L197) **`onClick()`**: 이벤트·효과 실행 / 참조 호출: WndTradeItem.sell, hide, consumeAlchemize
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L217) **`onClick()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: GameScene.show, WndOptions, ItemSprite, Messages.titleCase, item.name, Messages.get, onSelect, WndEnergizeItem.energizeAll, hide
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L225) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: WndEnergizeItem.energizeAll
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L232) **`hide()`**: 개별 처리 / 참조 호출: super.hide, WndAlchemizeItem.this.hide
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L255) **`onClick()`**: 이벤트·효과 실행 / 참조 호출: WndEnergizeItem.energizeOne, hide, consumeAlchemize
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L266) **`onClick()`**: 이벤트·효과 실행 / 참조 호출: WndEnergizeItem.energizeAll, hide, consumeAlchemize
- [L285](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Alchemize.java#L285) **`consumeAlchemize()`**: 개별 처리 / 조건 분기 / 참조 호출: Sample.INSTANCE.play, curItem.quantity, curItem.detachAll, owner.hide, curItem.detach, GameScene.selectItem, Catalog.countUse, getClass, Random.Float

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 543. [`BeaconOfReturning.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.spells` / 본문 327행 / 타입 3개 / 필드 13개 / 메서드 15개.

### 타입·상속 선언

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L53) `class BeaconOfReturning  extends Spell`
- [L278](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L278) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe.SimpleRecipe`
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L294) `class BeaconTracker  extends Buff`

### 변수·상수 (단일 행 선언)

- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L64) `int returnDepth` 초기식: `-1`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L65) `int returnBranch` 초기식: `0`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L66) `int returnPos`
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L246) `String DEPTH` 초기식: `"depth"`
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L247) `String BRANCH` 초기식: `"branch"`
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L248) `String POS` 초기식: `"pos"`
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L280) `int OUT_QUANTITY` 초기식: `5`
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L300) `int returnDepth` 초기식: `-1`
- [L301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L301) `int returnBranch` 초기식: `0`
- [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L302) `int returnPos`
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L304) `String DEPTH` 초기식: `"depth"`
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L305) `String BRANCH` 초기식: `"branch"`
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L306) `String POS` 초기식: `"pos"`

### 함수·메서드 역할과 내부 연결

- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L69) **`onCast(final Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.buff, setBeacon, GameScene.show, WndOptions, ItemSprite, Messages.titleCase, name, Messages.get, onSelect
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L82) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: setBeacon, returnBeacon
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L98) **`onThrow(int cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.belongings.getItem, getClass, Notes.remove, super.onThrow
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L109) **`doDrop(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: Notes.remove, super.doDrop
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L117) **`setBeacon(Hero hero)`**: 상태 갱신 / 조건 분기 / 참조 호출: Notes.remove, hero.buff, Buff.affect, Notes.add, hero.spend, hero.busy, GLog.i, Messages.get, hero.sprite.operate
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L143) **`returnBeacon(Hero hero)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: hero.buff, BeaconTracker, Actor.findChar, Char.hasProp, candidates.add, Random.shuffle, candidates.isEmpty, candidates.get, Actor.add
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L226) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, Dungeon.hero.buff, Messages.get
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L239) **`Glowing(0xFFFFFF)`**: 개별 처리
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L242) **`glowing()`**: 개별 처리
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L251) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L261) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L269) **`value()`**: 개별 처리
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L274) **`energyVal()`**: 개별 처리
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L309) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/BeaconOfReturning.java#L319) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":23,"fields":28,"methods":145}

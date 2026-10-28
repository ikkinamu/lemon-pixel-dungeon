# Java 파일별 소스 구현 해설 560–575

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 560. [`StoneOfBlast.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlast.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 39행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlast.java#L27) `class StoneOfBlast  extends Runestone`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlast.java#L34) **`activate(int cell)`**: 시간·상태 갱신 / 참조 호출: Bomb.ConjuredBomb, explode

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 561. [`StoneOfBlink.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlink.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 58행 / 타입 1개 / 필드 1개 / 메서드 3개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlink.java#L30) `class StoneOfBlink  extends Runestone`

### 변수·상수 (단일 행 선언)

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlink.java#L36) `Ballistica throwPath`

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlink.java#L39) **`throwPos(Hero user, int dst)`**: 개별 처리 / 참조 호출: Ballistica
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlink.java#L45) **`onThrow(int cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Actor.findChar, throwPath.path.get, super.onThrow
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlink.java#L54) **`activate(int cell)`**: 시간·상태 갱신 / 참조 호출: ScrollOfTeleportation.teleportToLocation

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 562. [`StoneOfClairvoyance.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfClairvoyance.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 92행 / 타입 1개 / 필드 1개 / 메서드 1개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfClairvoyance.java#L34) `class StoneOfClairvoyance  extends Runestone`

### 변수·상수 (단일 행 선언)

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfClairvoyance.java#L36) `int DIST` 초기식: `20`

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfClairvoyance.java#L43) **`activate(final int cell)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Dungeon.level.cellToPoint, Math.max, Math.min, Dungeon.level.height, Math.abs, Dungeon.level.width, GameScene.checkedCell, Dungeon.level.discover, GameScene.discoverTile

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 563. [`StoneOfDeepSleep.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfDeepSleep.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 60행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfDeepSleep.java#L34) `class StoneOfDeepSleep  extends Runestone`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfDeepSleep.java#L41) **`activate(int cell)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Actor.findChar, Buff.affect, c.sprite.centerEmitter, start, Speck.factory, Sample.INSTANCE.play

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 564. [`StoneOfDetectMagic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfDetectMagic.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 96행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfDetectMagic.java#L37) `class StoneOfDetectMagic  extends InventoryStone`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfDetectMagic.java#L45) **`usableOnItem(Item item)`**: 개별 처리 / 참조 호출: item.isIdentified
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfDetectMagic.java#L51) **`onItemSelected(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: useAnimation, hasCurseEnchant, hasCurseGlyph, item.trueLevel, hasGoodEnchant, hasGoodGlyph, GLog.i, Messages.get, GLog.h

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 565. [`StoneOfEnchantment.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfEnchantment.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 93행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfEnchantment.java#L37) `class StoneOfEnchantment  extends InventoryStone`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfEnchantment.java#L47) **`usableOnItem(Item item)`**: 개별 처리 / 참조 호출: ScrollOfEnchantment.enchantable
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfEnchantment.java#L52) **`onItemSelected(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: curItem.detach, Catalog.countUse, getClass, Talent.onRunestoneUsed, enchant, inscribe, curUser.sprite.emitter, start, Speck.factory
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfEnchantment.java#L83) **`value()`**: 개별 처리
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfEnchantment.java#L88) **`energyVal()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 566. [`StoneOfFear.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfFear.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 56행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfFear.java#L35) `class StoneOfFear  extends Runestone`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfFear.java#L42) **`activate(int cell)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Actor.findChar, Buff.affect, curUser.id, Flare, color, show, DungeonTilemap.tileCenterToWorld, Sample.INSTANCE.play

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 567. [`StoneOfFlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfFlock.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 75행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfFlock.java#L38) `class StoneOfFlock  extends Runestone`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfFlock.java#L45) **`activate(int cell)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: PathFinder.buildDistanceMap, BArray.not, spawnPoints.add, Dungeon.level.insideMap, Actor.findChar, Sheep, sheep.initialize, GameScene.add, Dungeon.level.occupyCell

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 568. [`StoneOfIntuition.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 226행 / 타입 3개 / 필드 3개 / 메서드 7개.

### 타입·상속 선언

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L52) `class StoneOfIntuition  extends InventoryStone`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L90) `class IntuitionUseTracker  extends Buff`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L94) `class WndGuess  extends Window`

### 변수·상수 (단일 행 선언)

- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L92) `Class curGuess` 초기식: `null`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L96) `int WIDTH` 초기식: `120`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L97) `int BTN_SIZE` 초기식: `20`

### 함수·메서드 역할과 내부 연결

- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L59) **`usableOnItem(Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: isKnown
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L71) **`onItemSelected(Item item)`**: 이벤트·효과 실행 / 참조 호출: GameScene.show, WndGuess
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L78) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, Dungeon.hero.buff, Messages.get
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L99) **`WndGuess(final Item item)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: IconTitle, titlebar.icon, ItemSprite, titlebar.label, Messages.titleCase, item.name, titlebar.setRect, add, PixelScene.renderTextBlock
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L113) **`RedButton("")`**: 개별 처리 / 조건 분기 / 참조 호출: onClick, super.onClick, useAnimation, item.getClass, setKnown, Item.updateQuickslot, item.identify, GLog.p, Messages.get
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L115) **`onClick()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onClick, useAnimation, item.getClass, setKnown, Item.updateQuickslot, item.identify, GLog.p, Messages.get, sprite.parent.add
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java#L195) **`onClick()`**: 이벤트·효과 실행 / 참조 호출: guess.text, Messages.titleCase, Messages.get, guess.enable, super.onClick

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 569. [`StoneOfShock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfShock.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.stones` / 본문 79행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfShock.java#L41) `class StoneOfShock  extends Runestone`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfShock.java#L48) **`activate(int cell)`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Sample.INSTANCE.play, PathFinder.buildDistanceMap, BArray.not, Actor.findChar, arcs.add, Lightning.Arc, n.sprite.center, Buff.prolong, CellEmitter.center

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 570. [`Stylus.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 143행 / 타입 1개 / 필드 2개 / 메서드 11개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L41) `class Stylus  extends Item`

### 변수·상수 (단일 행 선언)

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L43) `float TIME_TO_INSCRIBE` 초기식: `2`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L45) `String AC_INSCRIBE` 초기식: `"INSCRIBE"`

### 함수·메서드 역할과 내부 연결

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L58) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L65) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, GameScene.selectItem
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L78) **`isUpgradable()`**: 조건 판정
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L83) **`isIdentified()`**: 조건 판정
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L87) **`inscribe(Armor armor)`**: 개별 처리 / 조건 분기 / 참조 호출: GLog.w, Messages.get, armor.hasCurseGlyph, detach, Catalog.countUse, getClass, armor.inscribe, curUser.sprite.operate, curUser.sprite.centerEmitter
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L114) **`value()`**: 개별 처리
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L118) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, Messages.get, preferredBag, itemSelectable, onSelect, Stylus.this.inscribe
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L121) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L126) **`preferredBag()`**: 개별 처리
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L131) **`itemSelectable(Item item)`**: 개별 처리
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java#L136) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Stylus.this.inscribe

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 571. [`TengusMask.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/TengusMask.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 119행 / 타입 1개 / 필드 1개 / 메서드 6개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/TengusMask.java#L44) `class TengusMask  extends Item`

### 변수·상수 (단일 행 선언)

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/TengusMask.java#L46) `String AC_WEAR` 초기식: `"WEAR"`

### 함수·메서드 역할과 내부 연결

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/TengusMask.java#L58) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/TengusMask.java#L65) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, GameScene.show, WndChooseSubclass
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/TengusMask.java#L79) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 참조 호출: Badges.validateMastery, super.doPickUp
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/TengusMask.java#L85) **`isUpgradable()`**: 조건 판정
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/TengusMask.java#L90) **`isIdentified()`**: 조건 판정
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/TengusMask.java#L94) **`choose(HeroSubClass way)`**: 개별 처리 / 조건 분기 / 참조 호출: detach, Catalog.countUse, getClass, curUser.spend, curUser.busy, Talent.initSubclassTalents, Buff.affect, curUser.sprite.operate, Sample.INSTANCE.play

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 572. [`Torch.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Torch.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 97행 / 타입 1개 / 필드 2개 / 메서드 5개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Torch.java#L36) `class Torch  extends Item`

### 변수·상수 (단일 행 선언)

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Torch.java#L38) `String AC_LIGHT` 초기식: `"LIGHT"`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Torch.java#L40) `float TIME_TO_LIGHT` 초기식: `1`

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Torch.java#L51) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Torch.java#L58) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, hero.spend, hero.busy, hero.sprite.operate, detach, Catalog.countUse, getClass, Buff.affect
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Torch.java#L82) **`isUpgradable()`**: 조건 판정
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Torch.java#L87) **`isIdentified()`**: 조건 판정
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Torch.java#L92) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 573. [`ChaoticCenser.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 344행 / 타입 3개 / 필드 14개 / 메서드 12개.

### 타입·상속 선언

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L56) `class ChaoticCenser  extends Trinket`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L89) `class CenserGasTracker  extends Buff`
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L234) `class GasSpewer  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L91) `int left` 초기식: `Integer.MAX_VALUE`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L92) `int safeAreaDelay` 초기식: `100`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L134) `String LEFT` 초기식: `"left"`
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L236) `int targetCell`
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L238) `int depth`
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L239) `int branch`
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L241) `Class<?extends Blob> gasType`
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L242) `int gasQuantity`
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L273) `String CELL` 초기식: `"cell"`
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L274) `String DEPTH` 초기식: `"depth"`
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L275) `String BRANCH` 초기식: `"branch"`
- [L276](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L276) `String GAS_TYPE` 초기식: `"gas_type"`
- [L277](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L277) `String GAS_QUANTITY` 초기식: `"gas_quantity"`
- [L300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L300) `float[][] GAS_CAT_CHANCES` 초기식: `new float[4][3]`

### 함수·메서드 역할과 내부 연결

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L63) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L69) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, averageTurnsUntilGas, buffedLvl
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L77) **`averageTurnsUntilGas()`**: 개별 처리 / 참조 호출: averageTurnsUntilGas, trinketLevel
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L81) **`averageTurnsUntilGas(int level)`**: 개별 처리 / 조건 분기
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L95) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: averageTurnsUntilGas, spend, Random.NormalIntRange, Random.IntRange, TargetHealthIndicator.instance.isVisible, TargetHealthIndicator.instance.target, target.isActive, produceGas, Sample.INSTANCE.play
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L137) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L143) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, bundle.getInt
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L151) **`produceGas(Char target)`**: 개별 처리 / 조건 분기·반복·상태 선택 / 참조 호출: trinketLevel, Random.chances, Random.element, COMMON_GASSES.keySet, Regeneration.regenOn, COMMON_GASSES.get, UNCOMMON_GASSES.keySet, UNCOMMON_GASSES.get, RARE_GASSES.keySet
- [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L244) **`set(int targetCell, Class<?extends Blob> gasType, int gasQuantity)`**: 상태 갱신
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L255) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: GameScene.add, Blob.seed, level.blobs.get, setStrength, Dungeon.scalingDepth, MagicMissile.boltFromChar, MISSILE_VFX.get, Sample.INSTANCE.play, detach
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L280) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L290](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java#L290) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt, bundle.getClass

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 574. [`CrackedSpyglass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/CrackedSpyglass.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 65행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/CrackedSpyglass.java#L27) `class CrackedSpyglass  extends Trinket`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/CrackedSpyglass.java#L34) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/CrackedSpyglass.java#L40) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, buffedLvl, Messages.get, Messages.decimalFormat, extraLootChance
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/CrackedSpyglass.java#L52) **`extraLootChance()`**: 개별 처리 / 참조 호출: extraLootChance, trinketLevel
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/CrackedSpyglass.java#L56) **`extraLootChance(int level)`**: 개별 처리 / 조건 분기

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 575. [`DimensionalSundial.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/DimensionalSundial.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.trinkets` / 본문 100행 / 타입 1개 / 필드 1개 / 메서드 7개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/DimensionalSundial.java#L31) `class DimensionalSundial  extends Trinket`

### 변수·상수 (단일 행 선언)

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/DimensionalSundial.java#L57) `boolean sundialWarned` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/DimensionalSundial.java#L38) **`upgradeEnergyCost()`**: 개별 처리 / 참조 호출: level
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/DimensionalSundial.java#L44) **`statsDesc()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.get, enemySpawnMultiplierDaytime, buffedLvl, enemySpawnMultiplierNighttime
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/DimensionalSundial.java#L59) **`spawnMultiplierAtCurrentTime()`**: 개별 처리 / 조건 분기 / 참조 호출: trinketLevel, GregorianCalendar.getInstance, cal.get, GLog.w, Messages.get, enemySpawnMultiplierNighttime, enemySpawnMultiplierDaytime
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/DimensionalSundial.java#L76) **`enemySpawnMultiplierDaytime()`**: 개별 처리 / 참조 호출: enemySpawnMultiplierDaytime, trinketLevel
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/DimensionalSundial.java#L80) **`enemySpawnMultiplierDaytime(int level)`**: 개별 처리 / 조건 분기
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/DimensionalSundial.java#L88) **`enemySpawnMultiplierNighttime()`**: 개별 처리 / 참조 호출: enemySpawnMultiplierNighttime, trinketLevel
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/DimensionalSundial.java#L92) **`enemySpawnMultiplierNighttime(int level)`**: 개별 처리 / 조건 분기

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":20,"fields":25,"methods":67}

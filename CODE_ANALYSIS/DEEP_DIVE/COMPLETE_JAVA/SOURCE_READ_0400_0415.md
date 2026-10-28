# Java 파일별 소스 구현 해설 400–415

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 400. [`RegrowthBomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/RegrowthBomb.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bombs` / 본문 124행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/RegrowthBomb.java#L44) `class RegrowthBomb  extends Bomb`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/RegrowthBomb.java#L51) **`explodesDestructively()`**: 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/RegrowthBomb.java#L56) **`explosionRange()`**: 개별 처리
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/RegrowthBomb.java#L61) **`explode(int cell)`**: 개별 처리 / 조건 분기·반복·상태 선택 / 참조 호출: super.explode, Splash.at, PathFinder.buildDistanceMap, BArray.not, explosionRange, Actor.findChar, PotionOfHealing.cure, PotionOfHealing.heal, level.plants.get
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/RegrowthBomb.java#L119) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 401. [`ShrapnelBomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ShrapnelBomb.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bombs` / 본문 91행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ShrapnelBomb.java#L36) `class ShrapnelBomb  extends Bomb`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ShrapnelBomb.java#L43) **`explodesDestructively()`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ShrapnelBomb.java#L48) **`explosionRange()`**: 개별 처리
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ShrapnelBomb.java#L53) **`explode(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.explode, Dungeon.level.length, Dungeon.level.cellToPoint, ShadowCaster.castShadow, Dungeon.level.width, explosionRange, CellEmitter.center, burst, Actor.findChar
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/ShrapnelBomb.java#L86) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 402. [`SmokeBomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/SmokeBomb.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bombs` / 본문 69행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/SmokeBomb.java#L32) `class SmokeBomb  extends Bomb`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/SmokeBomb.java#L39) **`explosionRange()`**: 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/SmokeBomb.java#L44) **`explode(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.explode, PathFinder.buildDistanceMap, BArray.not, explosionRange, GameScene.add, Blob.seed
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/SmokeBomb.java#L64) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 403. [`WoollyBomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/WoollyBomb.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.bombs` / 본문 85행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/WoollyBomb.java#L38) `class WoollyBomb  extends Bomb`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/WoollyBomb.java#L45) **`explosionRange()`**: 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/WoollyBomb.java#L50) **`explode(int cell)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: super.explode, PathFinder.buildDistanceMap, BArray.not, explosionRange, spawnPoints.add, Dungeon.level.insideMap, Actor.findChar, Sheep, sheep.initialize
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/WoollyBomb.java#L80) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 404. [`BrokenSeal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 408행 / 타입 2개 / 필드 12개 / 메서드 33개.

### 타입·상속 선언

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L53) `class BrokenSeal  extends Item`
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L246) `class WarriorShield  extends ShieldBuff`

### 변수·상수 (단일 행 선언)

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L55) `String AC_AFFIX` 초기식: `"AFFIX"`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L58) `String AC_INFO` 초기식: `"INFO_WINDOW"`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L70) `Armor.Glyph glyph`
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L232) `String GLYPH` 초기식: `"glyph"`
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L255) `Armor armor`
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L257) `int cooldown` 초기식: `0`
- [L258](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L258) `float turnsSinceEnemies` 초기식: `0`
- [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L259) `int initialShield` 초기식: `0`
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L261) `int COOLDOWN_START` 초기식: `150`
- [L380](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L380) `String COOLDOWN` 초기식: `"cooldown"`
- [L381](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L381) `String TURNS_SINCE_ENEMIES` 초기식: `"turns_since_enemies"`
- [L382](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L382) `String INITIAL_SHIELD` 초기식: `"initial_shield"`

### 함수·메서드 역할과 내부 연결

- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L72) **`canTransferGlyph()`**: 조건 판정 / 조건 분기 / 참조 호출: Dungeon.hero.pointsInTalent, Arrays.asList, contains, glyph.getClass
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L87) **`getGlyph()`**: 조회·탐색
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L91) **`setGlyph(Armor.Glyph glyph)`**: 상태 갱신
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L95) **`maxShield(int armTier, int armLvl)`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L101) **`glowing()`**: 개별 처리 / 참조 호출: glyph.glowing
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L106) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L113) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, GameScene.selectItem, GameScene.show, WndUseItem
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L126) **`affixToArmor(Armor armor, Item outgoing)`**: 개별 처리 / 조건 분기 / 참조 호출: GLog.w, Messages.get, getGlyph, curse, canTransferGlyph, armor.glyph.getClass, getClass, GameScene.show, WndOptions
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L144) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: detach, detachSeal, setGlyph, GLog.p, Messages.get, hero.sprite.operate, Sample.INSTANCE.play, armor.affixSeal
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L163) **`hide()`**: 개별 처리 / 참조 호출: super.hide, Dungeon.hero.next
- [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L186) **`name()`**: 개별 처리 / 참조 호출: glyph.name, super.name
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L191) **`info()`**: 개별 처리 / 조건 분기 / 참조 호출: super.info, Messages.get, glyph.name, glyph.desc
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L202) **`isUpgradable()`**: 조건 판정 / 참조 호출: level
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L206) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, Messages.get, preferredBag, itemSelectable, onSelect, seal.affixToArmor
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L209) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L214) **`preferredBag()`**: 개별 처리
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L219) **`itemSelectable(Item item)`**: 개별 처리
- [L224](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L224) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: seal.affixToArmor
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L235) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L241) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.get
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L264) **`icon()`**: 개별 처리 / 조건 분기 / 참조 호출: coolingDown, shielding
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L273) **`tintIcon(Image icon)`**: 개별 처리 / 조건 분기 / 참조 호출: icon.resetColor, coolingDown, shielding, icon.brightness, icon.invert
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L283) **`iconFadePercent()`**: 개별 처리 / 조건 분기 / 참조 호출: shielding, GameMath.gate, coolingDown
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L296) **`iconTextDisplay()`**: 개별 처리 / 조건 분기 / 참조 호출: shielding, Integer.toString, coolingDown
- [L307](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L307) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: shielding, Messages.get
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L318) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Regeneration.regenOn, shielding, Dungeon.hero.visibleEnemies, Dungeon.hero.buff, HoldFast.buffDecayFactor, Math.max, decShield, maxShield, detach
- [L347](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L347) **`activate()`**: 시간·상태 갱신 / 참조 호출: incShield, maxShield, Math.max
- [L354](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L354) **`coolingDown()`**: 개별 처리
- [L358](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L358) **`reduceCooldown(float percentage)`**: 개별 처리 / 참조 호출: Math.round, Math.max
- [L363](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L363) **`setArmor(Armor arm)`**: 상태 갱신
- [L367](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L367) **`maxShield()`**: 개별 처리 / 조건 분기 / 참조 호출: hasTalent, pointsInTalent, armor.isEquipped, armor.checkSeal, maxShield, armor.level
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L385) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java#L393) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, bundle.getInt, bundle.getFloat, shielding

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 405. [`Dewdrop.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Dewdrop.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 158행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Dewdrop.java#L43) `class Dewdrop  extends Item`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Dewdrop.java#L53) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.belongings.getItem, Catalog.setSeen, getClass, Statistics.itemTypesDiscovered.add, flask.isFull, flask.collectDew, GameScene.pickUp, consumeDew, Catalog.countUse
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Dewdrop.java#L82) **`consumeDew(int quantity, Hero hero, boolean force)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, Math.min, hero.hasTalent, VialOfBlood.delayBurstHealing, VialOfBlood.totalHealMultiplier, hero.pointsInTalent, hero.buff, shielding, Buff.affect
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Dewdrop.java#L131) **`isUpgradable()`**: 조건 판정
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Dewdrop.java#L136) **`isIdentified()`**: 조건 판정
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Dewdrop.java#L143) **`merge(Item other)`**: 개별 처리 / 조건 분기 / 참조 호출: isSimilar
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Dewdrop.java#L152) **`quantity(int value)`**: 개별 처리 / 참조 호출: Math.min

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 406. [`EnergyCrystal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EnergyCrystal.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 87행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EnergyCrystal.java#L36) `class EnergyCrystal  extends Item`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EnergyCrystal.java#L43) **`EnergyCrystal()`**: 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EnergyCrystal.java#L47) **`EnergyCrystal(int value)`**: 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EnergyCrystal.java#L52) **`actions(Hero hero)`**: 시간·상태 갱신
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EnergyCrystal.java#L57) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 참조 호출: Catalog.setSeen, getClass, Statistics.itemTypesDiscovered.add, GameScene.pickUp, hero.sprite.showStatusWithIcon, Integer.toString, hero.spendAndNext, pickupDelay, Sample.INSTANCE.play
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EnergyCrystal.java#L77) **`isUpgradable()`**: 조건 판정
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EnergyCrystal.java#L82) **`isIdentified()`**: 조건 판정

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 407. [`EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items` / 본문 162행 / 타입 1개 / 필드 3개 / 메서드 11개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L39) `class EquipableItem  extends Item`

### 변수·상수 (단일 행 선언)

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L41) `String AC_EQUIP` 초기식: `"EQUIP"`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L42) `String AC_UNEQUIP` 초기식: `"UNEQUIP"`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L67) `int slotOfUnequipped` 초기식: `-1`

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L49) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add, isEquipped
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L56) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doPickUp, isIdentified, Document.ADVENTURERS_GUIDE.isPageRead, GameScene.flashForDocument
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L70) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, Dungeon.quickslot.getSlot, doEquip, Dungeon.quickslot.setSlot, updateQuickslot, defaultAction, doUnequip
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L95) **`doDrop(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: isEquipped, doUnequip, super.doDrop
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L102) **`cast(final Hero user, int dst)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: isEquipped, this.doUnequip, super.cast
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L113) **`equipCursed(Hero hero)`**: 개별 처리 / 참조 호출: hero.sprite.emitter, burst, Sample.INSTANCE.play
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L118) **`timeToEquip(Hero hero)`**: 개별 처리
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L122) **`doEquip(Hero hero)`**: 개별 처리
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L124) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff, hero.belongings.lostInventory, keptThroughLostInventory, GLog.w, Messages.get, hero.spendAndNext, timeToEquip, hero.spend, Dungeon.quickslot.getSlot
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L155) **`doUnequip(Hero hero, boolean collect)`**: 개별 처리 / 참조 호출: doUnequip
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java#L159) **`activate(Char ch)`**: 시간·상태 갱신

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 408. [`Berry.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Berry.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.food` / 본문 73행 / 타입 2개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Berry.java#L33) `class Berry  extends Food`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Berry.java#L71) `class SeedCounter  extends CounterBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Berry.java#L43) **`eatingTime()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.hasTalent
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Berry.java#L57) **`satisfy(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: super.satisfy, Buff.count, counter.count, Dungeon.level.drop, Generator.randomUsingDefaults, sprite.drop, counter.detach
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Berry.java#L67) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 409. [`Blandfruit.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.food` / 본문 312행 / 타입 3개 / 필드 3개 / 메서드 17개.

### 타입·상속 선언

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L56) `class Blandfruit  extends Food`
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L239) `class CookFruit  extends Recipe`
- [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L298) `class Chunks  extends Food`

### 변수·상수 (단일 행 선언)

- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L58) `Potion potionAttrib` 초기식: `null`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L59) `ItemSprite.Glowing potionGlow` 초기식: `null`
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L189) `String POTIONATTRIB` 초기식: `"potionattrib"`

### 함수·메서드 역할과 내부 연결

- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L72) **`isSimilar(Item item)`**: 조건 판정 / 조건 분기 / 참조 호출: super.isSimilar, potionAttrib.isSimilar
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L86) **`defaultAction()`**: 개별 처리 / 조건 분기 / 참조 호출: potionAttrib.defaultAction, equals
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L97) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: action.equals, GameScene.show, WndUseItem, GLog.w, Messages.get, super.execute, potionAttrib.apply
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L123) **`name()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, super.name
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L140) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, Messages.get
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L158) **`value()`**: 개별 처리
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L162) **`cook(Seed seed)`**: 개별 처리 / 참조 호출: imbuePotion, Reflection.newInstance, SeedToPotion.types.get, seed.getClass
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L166) **`imbuePotion(Potion potion)`**: 개별 처리 / 조건 분기 / 참조 호출: potionAttrib.anonymize, ItemSprite.Glowing
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L192) **`onThrow(int cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onThrow, Catalog.countUse, getClass, potionAttrib.shatter, Dungeon.level.drop, Chunks, sprite.drop
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L213) **`reset()`**: 생성·초기화 / 조건 분기 / 참조 호출: super.reset, imbuePotion
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L221) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L227) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, imbuePotion, bundle.get
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L235) **`glowing()`**: 개별 처리
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L243) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기 / 참조 호출: ingredients.size, ingredients.get, ingredients.set, fruit.quantity, seed.quantity
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L275) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L280](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L280) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기 / 참조 호출: testIngredients, ingredients.get, quantity, Blandfruit, cook
- [L291](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Blandfruit.java#L291) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기 / 참조 호출: testIngredients, Blandfruit, cook, ingredients.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 410. [`ChargrilledMeat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/ChargrilledMeat.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.food` / 본문 45행 / 타입 1개 / 필드 0개 / 메서드 2개.

### 타입·상속 선언

- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/ChargrilledMeat.java#L27) `class ChargrilledMeat  extends Food`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/ChargrilledMeat.java#L35) **`value()`**: 개별 처리
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/ChargrilledMeat.java#L39) **`cook(int quantity)`**: 개별 처리 / 참조 호출: ChargrilledMeat

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 411. [`Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.food` / 본문 144행 / 타입 1개 / 필드 3개 / 메서드 8개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java#L45) `class Food  extends Item`

### 변수·상수 (단일 행 선언)

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java#L47) `float TIME_TO_EAT` 초기식: `3f`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java#L49) `String AC_EAT` 초기식: `"EAT"`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java#L51) `float energy` 초기식: `Hunger.HUNGRY`

### 함수·메서드 역할과 내부 연결

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java#L63) **`actions(Hero hero)`**: 시간·상태 갱신 / 참조 호출: super.actions, actions.add
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java#L70) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, detach, Catalog.countUse, getClass, satisfy, GLog.i, Messages.get, hero.sprite.operate
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java#L97) **`eatSFX()`**: 개별 처리 / 참조 호출: Sample.INSTANCE.play
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java#L101) **`eatingTime()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.hasTalent
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java#L114) **`satisfy(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.isChallenged, hero.buff, buff.isCursed, GLog.n, Messages.get, Buff.affect, satisfy
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java#L130) **`isUpgradable()`**: 조건 판정
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java#L135) **`isIdentified()`**: 조건 판정
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java#L140) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 412. [`FrozenCarpaccio.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/FrozenCarpaccio.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.food` / 본문 82행 / 타입 1개 / 필드 0개 / 메서드 4개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/FrozenCarpaccio.java#L37) `class FrozenCarpaccio  extends Food`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/FrozenCarpaccio.java#L45) **`satisfy(Hero hero)`**: 개별 처리 / 참조 호출: super.satisfy, effect
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/FrozenCarpaccio.java#L50) **`value()`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/FrozenCarpaccio.java#L54) **`effect(Hero hero)`**: 개별 처리 / 상태 선택 / 참조 호출: Random.Int, GLog.i, Messages.get, Buff.affect, Barkskin.conditionallyAppend, PotionOfHealing.cure, Math.min, hero.sprite.showStatusWithIcon, Integer.toString
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/FrozenCarpaccio.java#L76) **`cook(MysteryMeat ingredient)`**: 개별 처리 / 참조 호출: FrozenCarpaccio, ingredient.quantity

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 413. [`MeatPie.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MeatPie.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.food` / 본문 99행 / 타입 2개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MeatPie.java#L33) `class MeatPie  extends Food`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MeatPie.java#L51) `class Recipe  extends com.shatteredpixel.shatteredpixeldungeon.items.Recipe`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MeatPie.java#L41) **`satisfy(Hero hero)`**: 개별 처리 / 참조 호출: super.satisfy, Buff.affect, reset
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MeatPie.java#L47) **`value()`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MeatPie.java#L54) **`testIngredients(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: ingredient.quantity, ingredient.getClass
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MeatPie.java#L78) **`cost(ArrayList<Item> ingredients)`**: 개별 처리
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MeatPie.java#L83) **`brew(ArrayList<Item> ingredients)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: testIngredients, ingredient.quantity, sampleOutput
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MeatPie.java#L94) **`sampleOutput(ArrayList<Item> ingredients)`**: 개별 처리 / 참조 호출: MeatPie

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 414. [`MysteryMeat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MysteryMeat.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.food` / 본문 93행 / 타입 2개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MysteryMeat.java#L37) `class MysteryMeat  extends Food`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MysteryMeat.java#L75) `class PlaceHolder  extends MysteryMeat`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MysteryMeat.java#L45) **`satisfy(Hero hero)`**: 개별 처리 / 참조 호출: super.satisfy, effect
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MysteryMeat.java#L50) **`value()`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MysteryMeat.java#L54) **`effect(Hero hero)`**: 개별 처리 / 상태 선택 / 참조 호출: Random.Int, GLog.w, Messages.get, Buff.affect, reignite, Buff.prolong, set
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MysteryMeat.java#L82) **`isSimilar(Item item)`**: 조건 판정
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MysteryMeat.java#L88) **`info()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 415. [`Pasty.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Pasty.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.food` / 본문 244행 / 타입 2개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Pasty.java#L45) `class Pasty  extends Food`
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Pasty.java#L231) `class FishLeftover  extends Food`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Pasty.java#L56) **`reset()`**: 생성·초기화 / 상태 선택 / 참조 호출: super.reset, Holiday.getCurrentHoliday
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Pasty.java#L93) **`eatSFX()`**: 개별 처리 / 상태 선택 / 참조 호출: Holiday.getCurrentHoliday, Sample.INSTANCE.play, super.eatSFX
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Pasty.java#L104) **`satisfy(Hero hero)`**: 개별 처리 / 조건 분기·반복·상태 선택 / 참조 호출: Holiday.getCurrentHoliday, super.satisfy, FishLeftover, left.collect, Dungeon.level.drop, sprite.drop, Sample.INSTANCE.play, ArtifactRecharge.chargeArtifacts, ScrollOfRecharging.charge
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Pasty.java#L175) **`name()`**: 개별 처리 / 상태 선택 / 참조 호출: Holiday.getCurrentHoliday, super.name, Messages.get
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Pasty.java#L201) **`desc()`**: 개별 처리 / 상태 선택 / 참조 호출: Holiday.getCurrentHoliday, super.desc, Messages.get
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Pasty.java#L227) **`value()`**: 개별 처리
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Pasty.java#L239) **`value()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":23,"fields":21,"methods":122}

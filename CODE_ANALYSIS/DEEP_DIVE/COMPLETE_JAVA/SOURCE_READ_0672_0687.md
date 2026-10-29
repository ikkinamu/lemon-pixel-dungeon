# Java 파일별 실제 소스 정적 분석 672–687

코드 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 본문에서 타입·변수·함수와 참조 호출을 추출했다. 기능 설명은 **함수명 및 제한된 본문 구문에 근거한 정적 추론**이며, 전수 AST/실행 검증이 아니다. 여러 줄 메서드·익명 클래스·동적 디스패치·깊은 함수의 누락/오탐 가능성이 있다.

## 672. [`ChillingDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/ChillingDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 51행 / 타입 1개 · 선언 변수 0개 · 메서드 1개.

### 타입·상속
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/ChillingDart.java#L30) `class ChillingDart extends TippedDart`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/ChillingDart.java#L37) **`proc(Char attacker, Char defender, int damage)`** — 개별 처리; 조건; 호출 후보: proc, Buff.prolong, super.proc

## 673. [`CleansingDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/CleansingDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 91행 / 타입 1개 · 선언 변수 0개 · 메서드 3개.

### 타입·상속
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/CleansingDart.java#L35) `class CleansingDart extends TippedDart`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/CleansingDart.java#L42) **`damageRoll(Char owner)`** — 전투 계산; 조건·반복; 호출 후보: damageRoll, attackTarget, super.damageRoll, proc, PotionOfCleansing.cleanse, defender.buffs, b.detach, defender.isAlive
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/CleansingDart.java#L52) **`proc(Char attacker, final Char defender, int damage)`** — 개별 처리; 조건·반복; 호출 후보: proc, PotionOfCleansing.cleanse, defender.buffs, b.detach, defender.isAlive, defender.die, super.proc, FlavourBuff
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/CleansingDart.java#L76) **`act()`** — 시간·상태 갱신; 조건; 호출 후보: act, beckon, Dungeon.level.randomDestination, defender.sprite.showLost, super.act, attachTo, super.proc

## 674. [`Dart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 368행 / 타입 1개 · 선언 변수 6개 · 메서드 27개.

### 타입·상속
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L48) `class Dart extends MissileWeapon`

### 변수·상수 후보
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L66) `String AC_TIP` = ` "TIP"`
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L117) `Crossbow bow`
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L182) `boolean processingChargedShot` = ` false`
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L183) `int chargedShotPos`
- [L291](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L291) `int singleSeedDarts`
- [L293](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L293) `String[] options`

### 메서드 역할·호출 표현
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L69) **`actions(Hero hero)`** — 시간·상태 갱신; 조건; 호출 후보: actions, super.actions, actions.add, execute, super.execute, action.equals, GameScene.selectItem, min
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L76) **`execute(Hero hero, String action)`** — 이벤트·효과; 조건; 호출 후보: execute, super.execute, action.equals, GameScene.selectItem, min, Dungeon.hero.buff, bow.dartMin, bow.buffedLvl
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L84) **`min(int lvl)`** — 개별 처리; 조건; 호출 후보: min, Dungeon.hero.buff, bow.dartMin, bow.buffedLvl, max, bow.dartMax, updateCrossbow, hero.belongings.weapon
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L101) **`max(int lvl)`** — 개별 처리; 조건; 호출 후보: max, Dungeon.hero.buff, bow.dartMax, bow.buffedLvl, updateCrossbow, hero.belongings.weapon, hero.belongings.secondWep, crossbowHasEnchant
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L119) **`updateCrossbow()`** — 시간·상태 갱신; 조건·반복; 호출 후보: updateCrossbow, hero.belongings.weapon, hero.belongings.secondWep, crossbowHasEnchant, owner.buff, hasEnchant, bow.hasEnchant, super.hasEnchant
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L132) **`crossbowHasEnchant( Char owner )`** — 개별 처리; 조건·반복; 호출 후보: crossbowHasEnchant, owner.buff, hasEnchant, bow.hasEnchant, super.hasEnchant, accuracyFactor, super.accuracyFactor, proc
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L137) **`hasEnchant(Class<? extends Enchantment> type, Char owner)`** — 조건 판정; 조건·반복; 호출 후보: hasEnchant, bow.hasEnchant, super.hasEnchant, accuracyFactor, owner.buff, super.accuracyFactor, proc, bow.proc
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L146) **`accuracyFactor(Char owner, Char target)`** — 개별 처리; 조건·반복; 호출 후보: accuracyFactor, owner.buff, super.accuracyFactor, proc, bow.proc, super.proc, processChargedShot, throwPos
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L156) **`proc(Char attacker, Char defender, int damage)`** — 개별 처리; 조건·반복; 호출 후보: proc, bow.proc, super.proc, processChargedShot, throwPos, updateCrossbow, super.throwPos, onThrow
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L169) **`throwPos(Hero user, int dst)`** — 개별 처리; 조건·반복; 호출 후보: throwPos, updateCrossbow, super.throwPos, onThrow, super.onThrow, processChargedShot, Dungeon.hero.buff, PathFinder.buildDistanceMap
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L175) **`onThrow(int cell)`** — 이벤트·효과; 조건·반복; 호출 후보: onThrow, updateCrossbow, super.onThrow, processChargedShot, Dungeon.hero.buff, PathFinder.buildDistanceMap, PathFinder.distance.clone, Actor.chars
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L184) **`processChargedShot( Char target, int dmg )`** — 시간·상태 갱신; 조건·반복; 호출 후보: processChargedShot, Dungeon.hero.buff, PathFinder.buildDistanceMap, PathFinder.distance.clone, Actor.chars, Actor.add, Actor, act
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L196) **`act()`** — 시간·상태 갱신; 조건; 호출 후보: act, ch.isAlive, bow.onAbilityKill, Actor.remove, proc, decrementDurability, super.decrementDurability, Dungeon.hero.buff
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L214) **`decrementDurability()`** — 개별 처리; 조건; 호출 후보: decrementDurability, super.decrementDurability, Dungeon.hero.buff, detach, throwSound, updateCrossbow, Sample.INSTANCE.play, Random.Float
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L222) **`throwSound()`** — 개별 처리; 조건; 호출 후보: throwSound, updateCrossbow, Sample.INSTANCE.play, Random.Float, super.throwSound, info, bow.isIdentified, Crossbow
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L232) **`info()`** — 개별 처리; 조건; 호출 후보: info, updateCrossbow, bow.isIdentified, Crossbow, super.info, isUpgradable, isIdentified, defaultQuantity
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L247) **`isUpgradable()`** — 조건 판정; 조건; 호출 후보: isUpgradable, isIdentified, defaultQuantity, value, Math.round, super.value, WndBag.ItemSelector, textPrompt
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L252) **`isIdentified()`** — 조건 판정; 조건; 호출 후보: isIdentified, defaultQuantity, value, Math.round, super.value, WndBag.ItemSelector, textPrompt, Messages.get
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L257) **`defaultQuantity()`** — 개별 처리; 조건; 호출 후보: defaultQuantity, value, Math.round, super.value, WndBag.ItemSelector, textPrompt, Messages.get, preferredBag
- [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L262) **`value()`** — 개별 처리; 조건; 호출 후보: value, Math.round, super.value, WndBag.ItemSelector, textPrompt, Messages.get, preferredBag, itemSelectable
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L266) **`ItemSelector()`** — 개별 처리; 조건; 호출 후보: WndBag.ItemSelector, textPrompt, Messages.get, preferredBag, itemSelectable, onSelect, Math.min, curItem.quantity
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L269) **`textPrompt()`** — 개별 처리; 조건; 호출 후보: textPrompt, Messages.get, preferredBag, itemSelectable, onSelect, Math.min, curItem.quantity, item.quantity
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L274) **`preferredBag()`** — 개별 처리; 조건; 호출 후보: preferredBag, itemSelectable, onSelect, Math.min, curItem.quantity, item.quantity, Messages.get, TippedDart.getTipped
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L279) **`itemSelectable(Item item)`** — 개별 처리; 조건; 호출 후보: itemSelectable, onSelect, Math.min, curItem.quantity, item.quantity, Messages.get, TippedDart.getTipped, GameScene.show
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L284) **`onSelect(final Item item)`** — 이벤트·효과; 조건; 호출 후보: onSelect, Math.min, curItem.quantity, item.quantity, Messages.get, TippedDart.getTipped, GameScene.show, WndOptions
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L288) **`min(curItem.quantity(), item.quantity()*2)`** — 개별 처리; 조건; 호출 후보: Math.min, curItem.quantity, item.quantity, Messages.get, TippedDart.getTipped, GameScene.show, WndOptions, ItemSprite
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java#L322) **`onSelect(int index)`** — 이벤트·효과; 조건; 호출 후보: onSelect, super.onSelect, item.quantity, item.detachAll, curItem.quantity, curItem.detachAll, TippedDart.getTipped, newDart.collect

## 675. [`DisplacingDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/DisplacingDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 111행 / 타입 1개 · 선언 변수 0개 · 메서드 1개.

### 타입·상속
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/DisplacingDart.java#L37) `class DisplacingDart extends TippedDart`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/DisplacingDart.java#L44) **`proc(Char attacker, Char defender, int damage)`** — 개별 처리; 조건·반복; 호출 후보: proc, super.proc, defender.properties, contains, PathFinder.buildDistanceMap, BArray.or, Dungeon.level.length, Char.hasProp

## 676. [`HealingDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/HealingDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 69행 / 타입 1개 · 선언 변수 0개 · 메서드 2개.

### 타입·상속
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/HealingDart.java#L31) `class HealingDart extends TippedDart`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/HealingDart.java#L39) **`damageRoll(Char owner)`** — 전투 계산; 조건; 호출 후보: damageRoll, attackTarget, super.damageRoll, proc, super.proc, PotionOfHealing.cure, Buff.affect, setHeal
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/HealingDart.java#L49) **`proc(Char attacker, Char defender, int damage)`** — 개별 처리; 조건; 호출 후보: proc, super.proc, PotionOfHealing.cure, Buff.affect, setHeal

## 677. [`HolyDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/HolyDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 76행 / 타입 1개 · 선언 변수 0개 · 메서드 2개.

### 타입·상속
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/HolyDart.java#L35) `class HolyDart extends TippedDart`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/HolyDart.java#L42) **`damageRoll(Char owner)`** — 전투 계산; 조건; 호출 후보: damageRoll, attackTarget, super.damageRoll, proc, super.proc, Buff.affect, Math.round, Char.hasProp
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/HolyDart.java#L52) **`proc(Char attacker, Char defender, int damage)`** — 개별 처리; 조건; 호출 후보: proc, super.proc, Buff.affect, Math.round, Char.hasProp, defender.sprite.emitter, start, buffedLvl

## 678. [`IncendiaryDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/IncendiaryDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 66행 / 타입 1개 · 선언 변수 0개 · 메서드 2개.

### 타입·상속
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/IncendiaryDart.java#L34) `class IncendiaryDart extends TippedDart`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/IncendiaryDart.java#L41) **`onThrow( int cell )`** — 이벤트·효과; 조건; 호출 후보: onThrow, Actor.findChar, GameScene.add, Blob.seed, decrementDurability, super.onThrow, Dungeon.level.drop, Dart
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/IncendiaryDart.java#L57) **`proc( Char attacker, Char defender, int damage )`** — 개별 처리; 조건; 호출 후보: proc, Buff.affect, reignite, super.proc

## 679. [`ParalyticDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/ParalyticDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 45행 / 타입 1개 · 선언 변수 0개 · 메서드 1개.

### 타입·상속
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/ParalyticDart.java#L29) `class ParalyticDart extends TippedDart`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/ParalyticDart.java#L36) **`proc( Char attacker, Char defender, int damage )`** — 개별 처리; 조건; 호출 후보: proc, Buff.prolong, super.proc

## 680. [`PoisonDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/PoisonDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 47행 / 타입 1개 · 선언 변수 0개 · 메서드 1개.

### 타입·상속
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/PoisonDart.java#L30) `class PoisonDart extends TippedDart`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/PoisonDart.java#L37) **`proc(Char attacker, Char defender, int damage)`** — 개별 처리; 조건; 호출 후보: proc, Buff.affect, set, Dungeon.scalingDepth, super.proc

## 681. [`RotDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/RotDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 58행 / 타입 1개 · 선언 변수 0개 · 메서드 2개.

### 타입·상속
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/RotDart.java#L31) `class RotDart extends TippedDart`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/RotDart.java#L38) **`proc(Char attacker, Char defender, int damage)`** — 개별 처리; 조건; 호출 후보: proc, defender.properties, contains, Buff.affect, set, Dungeon.scalingDepth, super.proc, durabilityPerUse
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/RotDart.java#L54) **`durabilityPerUse(int level)`** — 개별 처리; 호출 후보: durabilityPerUse

## 682. [`ShockingDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/ShockingDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 63행 / 타입 1개 · 선언 변수 0개 · 메서드 1개.

### 타입·상속
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/ShockingDart.java#L37) `class ShockingDart extends TippedDart`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/ShockingDart.java#L44) **`proc(Char attacker, Char defender, int damage)`** — 개별 처리; 조건; 호출 후보: proc, defender.damage, Random.NormalIntRange, Dungeon.scalingDepth, Electricity, arcs.add, Lightning.Arc, PointF

## 683. [`TippedDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.darts` / 본문 254행 / 타입 1개 · 선언 변수 3개 · 메서드 9개.

### 타입·상속
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L58) `class TippedDart extends Dart`

### 변수·상수 후보
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L66) `String AC_CLEAN` = ` "CLEAN"`
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L150) `int lostDarts` = ` 0`
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L165) `int targetPos` = ` -1`

### 메서드 역할·호출 표현
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L69) **`actions(Hero hero)`** — 시간·상태 갱신; 조건; 호출 후보: actions, super.actions, actions.remove, actions.add, execute, super.execute, action.equals, quantity
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L77) **`execute(final Hero hero, String action)`** — 이벤트·효과; 조건; 호출 후보: execute, super.execute, action.equals, quantity, Messages.get, GameScene.show, WndOptions, ItemSprite
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L100) **`onSelect(int index)`** — 이벤트·효과; 조건; 호출 후보: onSelect, detachAll, Dart, quantity, collect, hero.spend, hero.busy, hero.sprite.operate
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L128) **`rangedHit(Char enemy, int cell)`** — 개별 처리; 조건·반복; 호출 후보: rangedHit, super.rangedHit, Dart, d.quantity, Catalog.countUse, getClass, enemy.isAlive, Buff.affect
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L153) **`merge(Item other)`** — 개별 처리; 조건·반복; 호출 후보: merge, quantity, other.quantity, super.merge, durabilityPerUse, super.durabilityPerUse, Dungeon.hero.pointsInTalent, Actor.chars
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L172) **`durabilityPerUse(int level)`** — 개별 처리; 조건·반복; 호출 후보: durabilityPerUse, super.durabilityPerUse, Dungeon.hero.pointsInTalent, Actor.chars, l.inRange, Math.max, l.seedPreservation, Math.round
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L218) **`value()`** — 개별 처리; 반복; 호출 후보: value, Math.round, types.put, getTipped, Reflection.newInstance, types.get, s.getClass, quantity
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L239) **`getTipped( Plant.Seed s, int quantity )`** — 조회·탐색; 반복; 호출 후보: getTipped, Reflection.newInstance, types.get, s.getClass, quantity, randomTipped, Generator.randomUsingDefaults, types.containsKey
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java#L243) **`randomTipped( int quantity )`** — 개별 처리; 반복; 호출 후보: randomTipped, Generator.randomUsingDefaults, types.containsKey, s.getClass, getTipped

## 684. [`FishingSpear.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/FishingSpear.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles` / 본문 47행 / 타입 1개 · 선언 변수 0개 · 메서드 1개.

### 타입·상속
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/FishingSpear.java#L29) `class FishingSpear extends MissileWeapon`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/FishingSpear.java#L40) **`proc(Char attacker, Char defender, int damage)`** — 개별 처리; 조건; 호출 후보: proc, Math.max, super.proc

## 685. [`ForceCube.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ForceCube.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles` / 본문 143행 / 타입 1개 · 선언 변수 0개 · 메서드 6개.

### 타입·상속
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ForceCube.java#L43) `class ForceCube extends MissileWeapon`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ForceCube.java#L55) **`max(int lvl)`** — 개별 처리; 조건·반복; 호출 후보: max, hitSound, castDelay, Actor.findChar, delayFactor, super.castDelay, onThrow, super.onThrow
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ForceCube.java#L61) **`hitSound(float pitch)`** — 전투 계산; 조건·반복; 호출 후보: hitSound, castDelay, Actor.findChar, delayFactor, super.castDelay, onThrow, super.onThrow, rangedHit
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ForceCube.java#L66) **`castDelay(Char user, int cell)`** — 이벤트·효과; 조건·반복; 호출 후보: castDelay, Actor.findChar, delayFactor, super.castDelay, onThrow, super.onThrow, rangedHit, Dungeon.level.pressCell
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ForceCube.java#L76) **`onThrow(int cell)`** — 이벤트·효과; 조건·반복; 호출 후보: onThrow, Actor.findChar, super.onThrow, rangedHit, Dungeon.level.pressCell, targets.add, level.traps.get, Collections.sort
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ForceCube.java#L105) **`compare(Char a, Char b)`** — 개별 처리; 조건·반복; 호출 후보: compare, Float.compare, Dungeon.level.trueDistance, curUser.shoot, target.isAlive, Badges.validateDeathFromFriendlyMagic, Dungeon.fail, GLog.n
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ForceCube.java#L128) **`act()`** — 시간·상태 갱신; 조건; 호출 후보: act, Dungeon.hero.buff, primaryTarget.isActive, primaryTarget.id, Actor.remove, WandOfBlastWave.BlastWave.blast, Sample.INSTANCE.play

## 686. [`HeavyBoomerang.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles` / 본문 196행 / 타입 2개 · 선언 변수 12개 · 메서드 14개.

### 타입·상속
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L36) `class HeavyBoomerang extends MissileWeapon`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L84) `class CircleBack extends Buff`

### 변수·상수 후보
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L90) `HeavyBoomerang boomerang`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L91) `int thrownPos`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L92) `int returnPos`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L93) `int returnDepth`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L94) `int returnBranch`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L96) `int left`
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L126) `Char target` = ` this.target`
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L168) `String BOOMERANG` = ` "boomerang"`
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L169) `String THROWN_POS` = ` "thrown_pos"`
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L170) `String RETURN_POS` = ` "return_pos"`
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L171) `String RETURN_DEPTH` = ` "return_depth"`
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L172) `String RETURN_BRANCH` = ` "return_branch"`

### 메서드 역할·호출 표현
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L49) **`max(int lvl)`** — 개별 처리; 조건; 호출 후보: max, adjacentAccFactor, super.adjacentAccFactor, pickupDelay, super.pickupDelay, rangedHit, decrementDurability, Buff.append
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L57) **`adjacentAccFactor(Char owner, Char target)`** — 개별 처리; 조건; 호출 후보: adjacentAccFactor, super.adjacentAccFactor, pickupDelay, super.pickupDelay, rangedHit, decrementDurability, Buff.append, setup
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L65) **`pickupDelay()`** — 개별 처리; 조건; 호출 후보: pickupDelay, super.pickupDelay, rangedHit, decrementDurability, Buff.append, setup, rangedMiss, returnPos
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L71) **`rangedHit(Char enemy, int cell)`** — 개별 처리; 조건; 호출 후보: rangedHit, decrementDurability, Buff.append, setup, rangedMiss, returnPos, cancel, detach
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L79) **`rangedMiss(int cell)`** — 개별 처리; 조건; 호출 후보: rangedMiss, Buff.append, setup, returnPos, cancel, detach, activeDepth, act
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L98) **`setup( HeavyBoomerang boomerang, int thrownPos, int returnPos, int returnDepth, int returnBranch)`** — 생성·초기화; 조건; 호출 후보: setup, returnPos, cancel, detach, activeDepth, act, Actor.findChar, sprite.parent.recycle
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L107) **`returnPos()`** — 개별 처리; 조건; 호출 후보: returnPos, cancel, detach, activeDepth, act, Actor.findChar, sprite.parent.recycle, visual.reset
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L111) **`cancel()`** — 조건 판정; 조건; 호출 후보: cancel, detach, activeDepth, act, Actor.findChar, sprite.parent.recycle, visual.reset, Callback
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L116) **`activeDepth()`** — 시간·상태 갱신; 조건; 호출 후보: activeDepth, act, Actor.findChar, sprite.parent.recycle, visual.reset, Callback, call, detach
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L121) **`act()`** — 시간·상태 갱신; 조건; 호출 후보: act, Actor.findChar, sprite.parent.recycle, visual.reset, Callback, call, detach, boomerang.doPickUp
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L125) **`findChar(returnPos)`** — 조회·탐색; 조건; 호출 후보: Actor.findChar, sprite.parent.recycle, visual.reset, Callback, call, detach, boomerang.doPickUp, Dungeon.level.drop
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L133) **`call()`** — 개별 처리; 조건; 호출 후보: call, detach, boomerang.doPickUp, Dungeon.level.drop, sprite.drop, shoot, boomerang.decrementDurability, CircleBack.this.next
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L175) **`storeInBundle(Bundle bundle)`** — 저장·복원; 호출 후보: storeInBundle, super.storeInBundle, bundle.put, restoreFromBundle, super.restoreFromBundle, bundle.get, bundle.getInt, bundle.contains
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java#L185) **`restoreFromBundle(Bundle bundle)`** — 저장·복원; 호출 후보: restoreFromBundle, super.restoreFromBundle, bundle.get, bundle.getInt, bundle.contains

## 687. [`Javelin.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Javelin.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles` / 본문 38행 / 타입 1개 · 선언 변수 0개 · 메서드 0개.

### 타입·상속
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Javelin.java#L27) `class Javelin extends MissileWeapon`

### 변수·상수 후보
- 탐지 없음

### 메서드 역할·호출 표현
- 탐지 없음


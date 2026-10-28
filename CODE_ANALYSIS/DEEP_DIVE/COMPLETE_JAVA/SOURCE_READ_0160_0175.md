# Java 파일별 소스 구현 해설 160–175

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 160. [`LayOnHands.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LayOnHands.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 140행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LayOnHands.java#L41) `class LayOnHands  extends TargetedClericSpell`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LayOnHands.java#L43) **`LayOnHands()`**: 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LayOnHands.java#L46) **`icon()`**: 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LayOnHands.java#L51) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, Dungeon.hero.pointsInTalent, chargeUse
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LayOnHands.java#L56) **`targetingFlags()`**: 개별 처리
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LayOnHands.java#L61) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LayOnHands.java#L66) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Dungeon.level.distance, GLog.w, Messages.get, Actor.findChar, Sample.INSTANCE.play, affectChar, hero.sprite.operate, hero.next, hero.sprite.zap
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LayOnHands.java#L107) **`affectChar(Hero hero, Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.pointsInTalent, Buff.affect, Math.min, barrier.shielding, Math.max, incShield, ch.sprite.showStatusWithIcon, Integer.toString, barrier.incShield

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 161. [`LifeLinkSpell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 122행 / 타입 2개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java#L42) `class LifeLinkSpell  extends ClericSpell`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java#L104) `class LifeLinkSpellBuff  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java#L44) **`LifeLinkSpell()`**: 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java#L47) **`icon()`**: 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java#L52) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, Dungeon.hero.pointsInTalent, chargeUse
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java#L57) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent, PowerOfMany.getPoweredAlly, Stasis.getStasisAlly
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java#L64) **`chargeUse(Hero hero)`**: 개별 처리
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java#L69) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Math.round, Dungeon.hero.pointsInTalent, PowerOfMany.getPoweredAlly, hero.sprite.zap, sprite.parent.add, Beam.HealthRay, hero.sprite.center, ally.sprite.center, Sample.INSTANCE.play
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java#L111) **`icon()`**: 개별 처리
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java#L116) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.round, Dungeon.hero.pointsInTalent, Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 162. [`MindForm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 177행 / 타입 2개 / 필드 1개 / 메서드 16개.

### 타입·상속 선언

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L47) `class MindForm  extends ClericSpell`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L86) `class targetSelector  extends CellSelector.Listener`

### 변수·상수 (단일 행 선언)

- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L88) `Bundlable effect`

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L49) **`MindForm()`**: 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L52) **`icon()`**: 개별 처리
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L57) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, itemLevel, chargeUse
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L62) **`chargeUse(Hero hero)`**: 개별 처리
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L67) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L71) **`effectLevel()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L76) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 참조 호출: GameScene.show, Trinity.WndItemtypeSelect
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L82) **`itemLevel()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L90) **`setEffect(Bundlable effect)`**: 상태 갱신
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L94) **`wand()`**: 개별 처리 / 조건 분기 / 참조 호출: level, effectLevel, identify
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L104) **`thrown()`**: 개별 처리 / 조건 분기 / 참조 호출: level, effectLevel, repair, identify
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L116) **`onSelect(Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: wand, wand.tryToZap, Ballistica, wand.collisionProperties, GLog.i, Messages.get, hero.sprite.zap, Actor.findChar, QuickSlotButton.target
- [L124](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L124) **`Ballistica(Dungeon.hero.pos, target, wand.collisionProperties(target))`**: 개별 처리
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L141) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: wand.onZap, Random.Float, WondrousResin.extraCurseEffectChance, CursedWand.cursedZap, Ballistica, Callback, call, hero.belongings.armor, Trinity.trinityChargeUsePerEffect
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L149) **`call()`**: 개별 처리
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MindForm.java#L167) **`prompt()`**: 개별 처리 / 조건 분기 / 참조 호출: wand, Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 163. [`MnemonicPrayer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MnemonicPrayer.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 198행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MnemonicPrayer.java#L66) `class MnemonicPrayer  extends TargetedClericSpell`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MnemonicPrayer.java#L68) **`MnemonicPrayer()`**: 개별 처리
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MnemonicPrayer.java#L71) **`icon()`**: 개별 처리
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MnemonicPrayer.java#L76) **`targetingFlags()`**: 개별 처리
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MnemonicPrayer.java#L81) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MnemonicPrayer.java#L87) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Actor.findChar, GLog.w, Messages.get, QuickSlotButton.target, hero.pointsInTalent, affectChar, PowerOfMany.getPoweredAlly, ally.buff, hero.sprite.operate
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MnemonicPrayer.java#L125) **`affectChar(Char ch, float extension)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Sample.INSTANCE.play, ch.sprite.emitter, start, Speck.factory, ch.buffs, b.icon, Buff.affect, b.getClass, delay
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/MnemonicPrayer.java#L193) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, Dungeon.hero.pointsInTalent, chargeUse

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 164. [`Radiance.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Radiance.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 91행 / 타입 1개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Radiance.java#L39) `class Radiance  extends ClericSpell`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Radiance.java#L41) **`Radiance()`**: 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Radiance.java#L44) **`icon()`**: 개별 처리
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Radiance.java#L49) **`chargeUse(Hero hero)`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Radiance.java#L54) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Radiance.java#L59) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: GameScene.flash, Sample.INSTANCE.play, Buff.prolong, Dungeon.isChallenged, level.mobs.toArray, mob.buff, mob.damage, Buff.affect, mob.isActive

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 165. [`RecallInscription.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 177행 / 타입 2개 / 필드 2개 / 메서드 12개.

### 타입·상속 선언

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L48) `class RecallInscription  extends ClericSpell`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L137) `class UsedItemTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L143) `Class<?extends Item> item`
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L161) `String ITEM` 초기식: `"item"`

### 함수·메서드 역할과 내부 연결

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L50) **`RecallInscription()`**: 개별 처리
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L53) **`icon()`**: 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L58) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, Dungeon.hero.pointsInTalent, chargeUse
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L63) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.buff, Reflection.newInstance, item.setCurrent, hero.sprite.operate, Enchanting.show, anonymize, doRead, directActivate, ShatteredPixelDungeon.runOnRenderThread
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L89) **`call()`**: 개별 처리 / 참조 호출: item.doThrow
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L104) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff, ExoticScroll.class.isAssignableFrom, Scroll.class.isAssignableFrom, Runestone.class.isAssignableFrom
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L131) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent, hero.buff
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L146) **`icon()`**: 개별 처리
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L151) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent, Math.max, visualcooldown
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L157) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, Messages.titleCase, Reflection.newInstance, name, dispTurns
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L164) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java#L170) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getClass

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 166. [`ShieldOfLight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 147행 / 타입 2개 / 필드 3개 / 메서드 10개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L45) `class ShieldOfLight  extends TargetedClericSpell`
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L110) `class ShieldOfLightTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L112) `int object` 초기식: `0`
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L114) `float DURATION` 초기식: `5`
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L130) `String OBJECT` 초기식: `"object"`

### 함수·메서드 역할과 내부 연결

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L47) **`ShieldOfLight()`**: 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L50) **`icon()`**: 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L55) **`targetingFlags()`**: 개별 처리
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L60) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L65) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Actor.findChar, GLog.w, Messages.get, QuickSlotButton.target, Sample.INSTANCE.play, hero.sprite.operate, Buff.prolong, ch.id, Buff.affect
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L104) **`desc()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent, Messages.get, chargeUse
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L121) **`icon()`**: 개별 처리
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L126) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L133) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java#L139) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 167. [`Smite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 133행 / 타입 2개 / 필드 0개 / 메서드 9개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java#L44) `class Smite  extends TargetedClericSpell`
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java#L130) `class SmiteTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java#L46) **`Smite()`**: 개별 처리
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java#L49) **`icon()`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java#L54) **`targetingFlags()`**: 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java#L59) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, chargeUse
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java#L66) **`chargeUse(Hero hero)`**: 개별 처리
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java#L71) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java#L76) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Actor.findChar, GLog.w, Messages.get, Buff.affect, hero.isCharmedBy, hero.canAttack, tracker.detach, hero.sprite.attack, Callback
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java#L97) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: AttackIndicator.target, hero.belongings.attackingWeapon, STRReq, hero.STR, hero.attack, Sample.INSTANCE.play, enemy.sprite.burst, tracker.detach, Invisibility.dispel
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java#L120) **`bonusDmg(Hero attacker, Char defender)`**: 개별 처리 / 조건 분기 / 참조 호출: Char.hasProp, Hero.heroDamageIntRange

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 168. [`SpiritForm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 259행 / 타입 2개 / 필드 3개 / 메서드 19개.

### 타입·상속 선언

- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L70) `class SpiritForm  extends ClericSpell`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L109) `class SpiritFormBuff  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L115) `float DURATION` 초기식: `20f`
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L117) `Bundlable effect`
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L178) `String EFFECT` 초기식: `"effect"`

### 함수·메서드 역할과 내부 연결

- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L72) **`SpiritForm()`**: 개별 처리
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L75) **`icon()`**: 개별 처리
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L80) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, ringLevel, artifactLevel, chargeUse
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L85) **`chargeUse(Hero hero)`**: 개별 처리
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L90) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L95) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 참조 호출: GameScene.show, Trinity.WndItemtypeSelect
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L101) **`ringLevel()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L105) **`artifactLevel()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L120) **`icon()`**: 개별 처리
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L125) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L130) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L134) **`setEffect(Bundlable effect)`**: 상태 갱신 / 조건 분기 / 참조 호출: level, ringLevel, Dungeon.hero.updateHT
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L143) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: super.detach, Dungeon.hero.updateHT
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L150) **`ring()`**: 개별 처리 / 조건 분기 / 참조 호출: level, ringLevel
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L158) **`artifact()`**: 개별 처리 / 조건 분기 / 참조 호출: visiblyUpgraded, artifactLevel, transferUpgrade
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L169) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: ring, Messages.get, Messages.titleCase, name, dispTurns, artifact, super.desc
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L181) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L187) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.get
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java#L194) **`applyActiveArtifactEffect(ClassArmor armor, Artifact effect)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Talent.onArtifactUsed, AlchemyScene.assignToolkit, Game.switchScene, Actor.findChar, spawnPoints.add, spawnPoints.isEmpty, Wraith.spawnAt, Random.element, artifactLevel

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 169. [`Stasis.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 198행 / 타입 2개 / 필드 1개 / 메서드 13개.

### 타입·상속 선언

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L51) `class Stasis  extends ClericSpell`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L128) `class StasisBuff  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L182) `String ALLY` 초기식: `"ally"`

### 함수·메서드 역할과 내부 연결

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L53) **`Stasis()`**: 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L56) **`icon()`**: 개별 처리
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L61) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, Dungeon.hero.pointsInTalent, chargeUse
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L66) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent, PowerOfMany.getPoweredAlly, hero.buff
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L73) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L81) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: onSpellCast, hero.buff, hero.sprite.operate, act, PowerOfMany.getPoweredAlly, hero.sprite.zap, MagicMissile.boltFromChar, ally.buffs, Actor.remove
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L121) **`getStasisAlly()`**: 조회·탐색 / 조건 분기 / 참조 호출: Dungeon.hero.buff
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L135) **`icon()`**: 개별 처리
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L140) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent, Math.max, visualcooldown
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L146) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, Messages.titleCase, stasisAlly.name, dispTurns
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L151) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Actor.findChar, spawnPoints.add, spawnPoints.isEmpty, Random.Int, Random.element, GameScene.add, clearDefensingPos, stasisAlly.buff, Buff.prolong
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L185) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java#L191) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 170. [`Sunray.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Sunray.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 140행 / 타입 3개 / 필드 0개 / 메서드 5개.

### 타입·상속 선언

- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Sunray.java#L47) `class Sunray  extends TargetedClericSpell`
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Sunray.java#L136) `class SunRayUsedTracker  extends Buff`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Sunray.java#L137) `class SunRayRecentlyBlindedTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Sunray.java#L49) **`Sunray()`**: 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Sunray.java#L52) **`icon()`**: 개별 처리
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Sunray.java#L57) **`desc()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent, Messages.get, chargeUse
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Sunray.java#L65) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Sunray.java#L70) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Ballistica, targetingFlags, Actor.findChar, GLog.i, Messages.get, QuickSlotButton.target, hero.busy, Sample.INSTANCE.play, hero.sprite.zap

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 171. [`TargetedClericSpell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/TargetedClericSpell.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 60행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/TargetedClericSpell.java#L31) `class TargetedClericSpell  extends ClericSpell`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/TargetedClericSpell.java#L34) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 참조 호출: GameScene.selectCell, CellSelector.Listener, onSelect, onTargetSelected, prompt, targetingPrompt
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/TargetedClericSpell.java#L37) **`onSelect(Integer cell)`**: 이벤트·효과 실행 / 참조 호출: onTargetSelected
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/TargetedClericSpell.java#L42) **`prompt()`**: 개별 처리 / 참조 호출: targetingPrompt
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/TargetedClericSpell.java#L49) **`targetingFlags()`**: 개별 처리
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/TargetedClericSpell.java#L53) **`targetingPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/TargetedClericSpell.java#L57) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 172. [`WallOfLight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 321행 / 타입 2개 / 필드 0개 / 메서드 17개.

### 타입·상속 선언

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L46) `class WallOfLight  extends TargetedClericSpell`
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L243) `class LightWall  extends Blob`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L48) **`WallOfLight()`**: 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L51) **`icon()`**: 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L56) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, Dungeon.hero.pointsInTalent, chargeUse
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L61) **`targetingFlags()`**: 개별 처리
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L66) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: level.blobs.get
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L75) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L80) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: level.blobs.get, fullyClear, GLog.i, Messages.get, super.onCast
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L91) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행 / 조건 분기·반복·상태 선택 / 참조 호출: GLog.w, Messages.get, Dungeon.level.trueDistance, Dungeon.hero.pointsInTalent, level.blobs.get, fullyClear
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L231) **`placeWall(int pos, int knockbackDIR)`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.add, Blob.seed, Actor.findChar, WandOfBlastWave.throwChar, Ballistica, Buff.affect, ch.cooldown
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L250) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: l.width, cellsToFlagUpdate.add
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L270) **`seed(Level level, int cell, int amount)`**: 개별 처리 / 참조 호출: super.seed, level.updateCellFlags
- [L276](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L276) **`clear(int cell)`**: 상태 갱신 / 조건 분기 / 참조 호출: super.clear, Dungeon.level.updateCellFlags
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L283) **`fullyClear()`**: 개별 처리 / 참조 호출: super.fullyClear, Dungeon.level.buildFlagMaps
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L289) **`onBuildFlagMaps(Level l)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: l.length, onUpdateCellFlags
- [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L298) **`onUpdateCellFlags(Level l, int cell)`**: 이벤트·효과 실행 / 조건 분기
- [L308](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L308) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour
- [L314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/WallOfLight.java#L314) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 173. [`Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero` / 본문 1223행 / 타입 33개 / 필드 22개 / 메서드 85개.

### 타입·상속 선언

- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L96) `enum Talent`
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L205) `class ImprovisedProjectileCooldown  extends FlavourBuff`
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L210) `class LethalMomentumTracker  extends FlavourBuff`
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L211) `class StrikingWaveTracker  extends FlavourBuff`
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L212) `class WandPreservationCounter  extends CounterBuff`
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L213) `class EmpoweredStrikeTracker  extends FlavourBuff`
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L217) `class ProtectiveShadowsTracker  extends Buff`
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L254) `class BountyHunterTracker  extends FlavourBuff`
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L255) `class RejuvenatingStepsCooldown  extends FlavourBuff`
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L260) `class RejuvenatingStepsFurrow  extends CounterBuff`
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L261) `class SeerShotCooldown  extends FlavourBuff`
- [L266](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L266) `class SpiritBladesTracker  extends FlavourBuff`
- [L267](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L267) `class PatientStrikeTracker  extends Buff`
- [L293](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L293) `class AggressiveBarrierCooldown  extends FlavourBuff`
- [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L298) `class LiquidAgilEVATracker  extends FlavourBuff`
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L304) `class LiquidAgilACCTracker  extends FlavourBuff`
- [L324](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L324) `class LethalHasteCooldown  extends FlavourBuff`
- [L329](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L329) `class SwiftEquipCooldown  extends FlavourBuff`
- [L354](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L354) `class DeadlyFollowupTracker  extends FlavourBuff`
- [L372](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L372) `class PreciseAssaultTracker  extends FlavourBuff`
- [L378](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L378) `class VariedChargeTracker  extends Buff`
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L393) `class CombinedLethalityAbilityTracker  extends FlavourBuff`
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L396) `class CombinedEnergyAbilityTracker  extends FlavourBuff`
- [L415](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L415) `class CounterAbilityTacker  extends FlavourBuff`
- [L416](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L416) `class SatiatedSpellsTracker  extends Buff`
- [L423](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L423) `class SearingLightCooldown  extends FlavourBuff`
- [L584](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L584) `class CachedRationsDropped  extends CounterBuff`
- [L585](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L585) `class NatureBerriesDropped  extends CounterBuff`
- [L679](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L679) `class WarriorFoodImmunity  extends FlavourBuff`
- [L928](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L928) `class ProvokedAngerTracker  extends FlavourBuff`
- [L934](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L934) `class LingeringMagicTracker  extends FlavourBuff`
- [L940](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L940) `class SuckerPunchTracker  extends Buff`
- [L941](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L941) `class FollowupStrikeTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L215) `boolean delayedDetach` 초기식: `false`
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L241) `String BARRIER_INC` 초기식: `"barrier_inc"`
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L268) `int pos`
- [L281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L281) `String POS` 초기식: `"pos"`
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L305) `int uses`
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L312) `String USES` 초기식: `"uses"`
- [L330](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L330) `boolean secondUse`
- [L342](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L342) `String SECOND_USE` 초기식: `"second_use"`
- [L355](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L355) `int object`
- [L360](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L360) `String OBJECT` 초기식: `"object"`
- [L379](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L379) `Class weapon`
- [L381](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L381) `String WEAPON` 초기식: `"weapon"`
- [L394](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L394) `MeleeWeapon weapon`
- [L397](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L397) `boolean monkAbilused` 초기식: `false`
- [L398](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L398) `boolean wepAbilUsed` 초기식: `false`
- [L400](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L400) `String MONK_ABIL_USED` 초기식: `"monk_abil_used"`
- [L401](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L401) `String WEP_ABIL_USED` 초기식: `"wep_abil_used"`
- [L436](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L436) `int[] tierLevelThresholds` 초기식: `new int[]{0, 2, 7, 13, 21, 31}`
- [L942](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L942) `int object`
- [L947](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L947) `String OBJECT` 초기식: `"object"`
- [L960](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L960) `int MAX_TALENT_TIERS` 초기식: `4`
- [L1143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L1143) `String TALENT_TIER` 초기식: `"talents_tier_"`

### 함수·메서드 역할과 내부 연결

- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L206) **`icon()`**: 개별 처리
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L207) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L208) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L221) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: hasTalent, Buff.affect, barrier.shielding, pointsInTalent, barrier.incShield, detach, spend
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L243) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L249) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getFloat
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L256) **`icon()`**: 개별 처리
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L257) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L258](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L258) **`iconFadePercent()`**: 개별 처리 / 참조 호출: GameMath.gate, visualcooldown, Dungeon.hero.pointsInTalent
- [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L262) **`icon()`**: 개별 처리 / 참조 호출: target.buff
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L263) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L264) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L270) **`icon()`**: 개별 처리
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L271) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L273) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: detach, spend
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L283) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L288) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L294) **`icon()`**: 개별 처리
- [L295](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L295) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L296) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L308](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L308) **`icon()`**: 개별 처리
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L309) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L310](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L310) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L314) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L319) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L325](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L325) **`icon()`**: 개별 처리
- [L326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L326) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L327) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L331](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L331) **`hasSecondUse()`**: 조건 판정
- [L335](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L335) **`icon()`**: 개별 처리
- [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L336) **`tintIcon(Image icon)`**: 개별 처리 / 조건 분기 / 참조 호출: hasSecondUse, icon.hardlight
- [L340](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L340) **`iconFadePercent()`**: 개별 처리 / 참조 호출: GameMath.gate, visualcooldown
- [L344](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L344) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L349](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L349) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getBoolean
- [L357](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L357) **`icon()`**: 개별 처리
- [L358](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L358) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L359) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L362](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L362) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L367](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L367) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L374](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L374) **`icon()`**: 개별 처리
- [L375](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L375) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L376](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L376) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L383](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L383) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L388](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L388) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getClass
- [L403](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L403) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L409](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L409) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getBoolean
- [L418](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L418) **`icon()`**: 개별 처리
- [L425](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L425) **`icon()`**: 개별 처리
- [L428](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L428) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L429](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L429) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L447](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L447) **`icon()`**: 개별 처리 / 조건 분기·상태 선택
- [L472](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L472) **`maxPoints()`**: 개별 처리
- [L476](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L476) **`title()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, name
- [L483](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L483) **`desc()`**: 개별 처리 / 참조 호출: desc
- [L487](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L487) **`desc(boolean metamorphed)`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, name, metaDesc.equals
- [L497](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L497) **`onTalentUpgraded(Hero hero, Talent talent)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Buff.affect, hero.pointsInTalent, hero.belongings.armor, ShardOfOblivion.passiveIDDisabled, belongings.armor.identify, belongings.ring.identify, belongings.misc.identify, setKnown, belongings.ring.setKnown
- [L587](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L587) **`onFoodEaten(Hero hero, float foodVal, Item foodSource)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.hasTalent, hero.pointsInTalent, Math.min, hero.sprite.showStatusWithIcon, Integer.toString, hero.cooldown, Buff.affect, set, ScrollOfRecharging.charge
- [L683](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L683) **`itemIDSpeedFactor(Hero hero, Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.pointsInTalent
- [L711](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L711) **`onPotionUsed(Hero hero, int cell, float factor)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: hero.hasTalent, Math.round, hero.pointsInTalent, hero.sprite.showStatusWithIcon, Integer.toString, Buff.affect, setShield, grassCells.add, Random.shuffle
- [L762](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L762) **`onScrollUsed(Hero hero, int pos, float factor, Class<?extends Item> cls)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.hasTalent, Buff.affect, reset, hero.pointsInTalent, Sample.INSTANCE.play, Scroll.class.isAssignableFrom, Buff.prolong, Random.Int, Reflection.newInstance
- [L785](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L785) **`onRunestoneUsed(Hero hero, int pos, Class<?extends Item> cls)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.hasTalent, Runestone.class.isAssignableFrom, Buff.prolong, hero.pointsInTalent, cls.equals, hero.buff, Random.Int, Reflection.newInstance, collect
- [L804](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L804) **`onArtifactUsed(Hero hero)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: hero.hasTalent, Buff.prolong, hero.pointsInTalent, Dungeon.hero.hasTalent, Dungeon.hero.cooldown, Random.Int, Dungeon.hero.pointsInTalent, Dungeon.hero.buffs, b.detach
- [L832](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L832) **`onItemEquipped(Hero hero, Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.pointsInTalent, hero.hasTalent, setKnown, ShardOfOblivion.passiveIDDisabled, setIDReady, item.identify
- [L862](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L862) **`onItemCollected(Hero hero, Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.pointsInTalent, setKnown
- [L868](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L868) **`onAttackProc(Hero hero, Char enemy, int dmg)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: hero.hasTalent, hero.buff, hero.pointsInTalent, detach, Random.IntRange, surprisedBy, enemy.buff, Buff.affect, enemy.isAlive
- [L930](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L930) **`icon()`**: 개별 처리
- [L931](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L931) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L932](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L932) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L936](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L936) **`icon()`**: 개별 처리
- [L937](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L937) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L938](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L938) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L944](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L944) **`icon()`**: 개별 처리
- [L945](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L945) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L946](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L946) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L949](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L949) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L954](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L954) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L962](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L962) **`initClassTalents(Hero hero)`**: 생성·초기화 / 참조 호출: initClassTalents
- [L966](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L966) **`initClassTalents(HeroClass cls, ArrayList<LinkedHashMap<Talent, Integer>> talents)`**: 생성·초기화 / 참조 호출: initClassTalents
- [L970](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L970) **`initClassTalents(HeroClass cls, ArrayList<LinkedHashMap<Talent, Integer>> talents, LinkedHashMap<Talent, Talent> replacements)`**: 생성·초기화 / 조건 분기·반복·상태 선택 / 참조 호출: talents.size, talents.add, Collections.addAll, replacements.containsKey, replacements.get, talents.get, put, tierTalents.clear
- [L1068](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L1068) **`initSubclassTalents(Hero hero)`**: 생성·초기화 / 참조 호출: initSubclassTalents
- [L1072](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L1072) **`initSubclassTalents(HeroSubClass cls, ArrayList<LinkedHashMap<Talent, Integer>> talents)`**: 생성·초기화 / 조건 분기·반복·상태 선택 / 참조 호출: talents.size, talents.add, Collections.addAll, talents.get, put, tierTalents.clear
- [L1127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L1127) **`initArmorTalents(Hero hero)`**: 생성·초기화 / 참조 호출: initArmorTalents
- [L1131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L1131) **`initArmorTalents(ArmorAbility abil, ArrayList<LinkedHashMap<Talent, Integer>> talents)`**: 생성·초기화 / 조건 분기·반복 / 참조 호출: talents.size, talents.add, abil.talents, talents.get, put
- [L1145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L1145) **`storeTalentsInBundle(Bundle bundle, Hero hero)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: hero.talents.get, Bundle, tier.keySet, tier.get, tierBundle.put, talent.name, tierBundle.contains, tier.put, Math.min
- [L1178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java#L1178) **`restoreTalentsFromBundle(Bundle bundle, Hero hero)`**: 저장·복원 / 조건 분기·반복·예외 처리 / 참조 호출: bundle.contains, bundle.getBundle, replacements.getKeys, replacements.getString, renamedTalents.containsKey, renamedTalents.get, removedTalents.contains, hero.metamorphedTalents.put, Talent.valueOf

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 174. [`Acidic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Acidic.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 61행 / 타입 1개 / 필드 0개 / 메서드 3개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Acidic.java#L32) `class Acidic  extends Scorpio`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Acidic.java#L43) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 참조 호출: Buff.affect, set, super.attackProc
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Acidic.java#L49) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: Dungeon.level.adjacent, Buff.affect, set, super.defenseProc
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Acidic.java#L57) **`createLoot()`**: 생성·초기화 / 참조 호출: PotionOfExperience

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 175. [`Albino.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Albino.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.mobs` / 본문 53행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Albino.java#L31) `class Albino  extends Rat`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Albino.java#L44) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, Random.Int, Buff.affect, set, Random.NormalFloat

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":58,"fields":32,"methods":223}

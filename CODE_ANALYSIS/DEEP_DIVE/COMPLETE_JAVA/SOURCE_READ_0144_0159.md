# Java 파일별 소스 구현 해설 144–159

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 144. [`BeamingRay.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 224행 / 타입 2개 / 필드 3개 / 메서드 10개.

### 타입·상속 선언

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L51) `class BeamingRay  extends TargetedClericSpell`
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L187) `class BeamingRayBoost  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L193) `int object` 초기식: `0`
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L195) `float DURATION` 초기식: `10f`
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L197) `String OBJECT` 초기식: `"object"`

### 함수·메서드 역할과 내부 연결

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L53) **`BeamingRay()`**: 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L56) **`icon()`**: 개별 처리
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L61) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, Dungeon.hero.pointsInTalent, chargeUse
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L66) **`targetingFlags()`**: 개별 처리
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L71) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent, PowerOfMany.getPoweredAlly, Stasis.getStasisAlly
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L78) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: PowerOfMany.getPoweredAlly, Dungeon.level.insideMap, GLog.w, Messages.get, Actor.findChar, Dungeon.level.trueDistance, Stasis.getStasisAlly, hero.pointsInTalent, Char.hasProp
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L200) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L206) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L212) **`icon()`**: 개별 처리
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java#L217) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 145. [`BlessSpell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BlessSpell.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 137행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BlessSpell.java#L44) `class BlessSpell  extends TargetedClericSpell`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BlessSpell.java#L46) **`BlessSpell()`**: 개별 처리
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BlessSpell.java#L49) **`icon()`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BlessSpell.java#L54) **`targetingFlags()`**: 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BlessSpell.java#L59) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BlessSpell.java#L64) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Actor.findChar, GLog.w, Messages.get, Sample.INSTANCE.play, affectChar, hero.busy, hero.sprite.operate, hero.spend, hero.sprite.zap
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BlessSpell.java#L100) **`affectChar(Hero hero, Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: Flare, color, show, Buff.prolong, hero.pointsInTalent, Buff.affect, setShield, ch.sprite.showStatusWithIcon, Integer.toString
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BlessSpell.java#L131) **`desc()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent, Messages.get, chargeUse

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 146. [`BodyForm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 142행 / 타입 2개 / 필드 2개 / 메서드 16개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L40) `class BodyForm  extends ClericSpell`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L75) `class BodyFormBuff  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L81) `Bundlable effect`
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L126) `String EFFECT` 초기식: `"effect"`

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L42) **`BodyForm()`**: 개별 처리
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L45) **`icon()`**: 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L50) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, duration, chargeUse
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L55) **`chargeUse(Hero hero)`**: 개별 처리
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L60) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L65) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 참조 호출: GameScene.show, Trinity.WndItemtypeSelect
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L71) **`duration()`**: 개별 처리 / 참조 호출: Math.round, Dungeon.hero.pointsInTalent
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L84) **`icon()`**: 개별 처리
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L89) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L94) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, duration, visualcooldown
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L98) **`setEffect(Bundlable effect)`**: 상태 갱신
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L102) **`enchant()`**: 개별 처리 / 조건 분기
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L109) **`glyph()`**: 개별 처리 / 조건 분기
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L117) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: enchant, Messages.get, Messages.titleCase, name, dispTurns, glyph, super.desc
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L129) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java#L135) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 147. [`Cleanse.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Cleanse.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 116행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Cleanse.java#L44) `class Cleanse  extends ClericSpell`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Cleanse.java#L46) **`Cleanse()`**: 개별 처리
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Cleanse.java#L49) **`icon()`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Cleanse.java#L54) **`chargeUse(Hero hero)`**: 개별 처리
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Cleanse.java#L58) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.pointsInTalent, Messages.get, chargeUse
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Cleanse.java#L66) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Cleanse.java#L71) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: affected.add, level.mobs.toArray, PowerOfMany.getPoweredAlly, ally.buff, affected.contains, ch.buffs, b.detach, hero.pointsInTalent, Buff.prolong

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 148. [`ClericSpell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 241행 / 타입 1개 / 필드 0개 / 메서드 12개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L40) `class ClericSpell`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L42) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L44) **`chargeUse(Hero hero)`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L48) **`canCast(Hero hero)`**: 조건 판정
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L52) **`name()`**: 개별 처리 / 참조 호출: Messages.get
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L56) **`shortDesc()`**: 개별 처리 / 참조 호출: Messages.get, chargeUse
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L60) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, chargeUse
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L64) **`usesTargeting()`**: 이벤트·효과 실행
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L68) **`targetingFlags()`**: 개별 처리
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L72) **`icon()`**: 개별 처리
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L76) **`onSpellCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Invisibility.dispel, hero.hasTalent, hero.buff, hero.pointsInTalent, Buff.affect, setShield, PowerOfMany.getPoweredAlly, ally.buff, detach
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L104) **`getSpellList(Hero cleric, int tier)`**: 조회·탐색 / 조건 분기 / 참조 호출: spells.add, cleric.hasTalent
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java#L209) **`getAllSpells()`**: 조회·탐색 / 참조 호출: spells.add

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 149. [`DivineIntervention.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineIntervention.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 126행 / 타입 2개 / 필드 0개 / 메서드 9개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineIntervention.java#L40) `class DivineIntervention  extends ClericSpell`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineIntervention.java#L94) `class DivineShield  extends ShieldBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineIntervention.java#L42) **`DivineIntervention()`**: 개별 처리
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineIntervention.java#L45) **`icon()`**: 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineIntervention.java#L50) **`chargeUse(Hero hero)`**: 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineIntervention.java#L55) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent, hero.buff
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineIntervention.java#L63) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Sample.INSTANCE.play, hero.sprite.operate, Actor.chars, Buff.affect, setShield, hero.pointsInTalent, Flare, color, show
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineIntervention.java#L88) **`desc()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent, Messages.get, chargeUse
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineIntervention.java#L101) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Dungeon.hero.buff, detach, spend
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineIntervention.java#L112) **`shielding()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.buff, super.shielding
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineIntervention.java#L120) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.sprite.remove

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 150. [`DivineSense.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 110행 / 타입 2개 / 필드 1개 / 메서드 9개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java#L40) `class DivineSense  extends ClericSpell`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java#L83) `class DivineSenseTracker  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java#L85) `float DURATION` 초기식: `50f`

### 함수·메서드 역할과 내부 연결

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java#L42) **`DivineSense()`**: 개별 처리
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java#L45) **`icon()`**: 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java#L50) **`chargeUse(Hero hero)`**: 개별 처리
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java#L55) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java#L60) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Buff.prolong, Dungeon.observe, Sample.INSTANCE.play, SpellSprite.show, hero.sprite.operate, hero.next, PowerOfMany.getPoweredAlly, ally.buff, onSpellCast
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java#L79) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, Dungeon.hero.pointsInTalent, chargeUse
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java#L92) **`icon()`**: 개별 처리
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java#L97) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java#L102) **`detach()`**: 개별 처리 / 참조 호출: super.detach, Dungeon.observe, GameScene.updateFog

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 151. [`Flash.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Flash.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 85행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Flash.java#L34) `class Flash  extends TargetedClericSpell`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Flash.java#L36) **`Flash()`**: 개별 처리
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Flash.java#L39) **`icon()`**: 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Flash.java#L44) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Flash.java#L53) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent, hero.buff
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Flash.java#L60) **`targetingFlags()`**: 개별 처리
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Flash.java#L65) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Dungeon.level.distance, hero.pointsInTalent, GLog.w, Messages.get, ScrollOfTeleportation.teleportToLocation, hero.spendAndNext, onSpellCast, hero.buff

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 152. [`GuidingLight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 182행 / 타입 4개 / 필드 0개 / 메서드 13개.

### 타입·상속 선언

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L49) `class GuidingLight  extends TargetedClericSpell`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L128) `class GuidingLightPriestCooldown  extends FlavourBuff`
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L149) `class Illuminated  extends Buff`
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L180) `class WasIlluminatedTracker  extends Buff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L51) **`GuidingLight()`**: 개별 처리
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L54) **`icon()`**: 개별 처리
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L59) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Ballistica, targetingFlags, Actor.findChar, GLog.i, Messages.get, QuickSlotButton.target, hero.busy, Sample.INSTANCE.play, hero.sprite.zap
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L82) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Actor.findChar, ch.damage, Hero.heroDamageIntRange, Sample.INSTANCE.play, Random.Float, ch.sprite.burst, ch.isAlive, Buff.affect, Dungeon.level.pressCell
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L111) **`chargeUse(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: hero.buff
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L120) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, chargeUse
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L131) **`icon()`**: 개별 처리
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L136) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.brightness
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L140) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L143) **`detach()`**: 개별 처리 / 참조 호출: super.detach, ActionIndicator.refresh
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L156) **`icon()`**: 개별 처리
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L161) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.sprite.remove
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java#L167) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 153. [`HallowedGround.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 271행 / 타입 3개 / 필드 0개 / 메서드 12개.

### 타입·상속 선언

- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L60) `class HallowedGround  extends TargetedClericSpell`
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L166) `class HallowedTerrain  extends Blob`
- [L268](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L268) `class HallowedFurrowTracker  extends CounterBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L62) **`HallowedGround()`**: 개별 처리
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L65) **`icon()`**: 개별 처리
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L70) **`chargeUse(Hero hero)`**: 개별 처리
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L75) **`targetingFlags()`**: 개별 처리
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L80) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L85) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: GLog.w, Messages.get, PathFinder.buildDistanceMap, BArray.not, hero.pointsInTalent, Dungeon.level.length, Level.set, GameScene.updateMap, CellEmitter.get
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L138) **`affectChar(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.min, ch.shielding, Buff.affect, incShield, ch.sprite.showStatusWithIcon, Integer.toString, Math.max
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L161) **`desc()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent, Messages.get, chargeUse
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L169) **`evolve()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: level.blobs.get, Dungeon.hero.pointsInTalent, Dungeon.level.width, level.plants.get, Random.Int, Regeneration.regenOn, Dungeon.hero.buff, count, Level.set
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L242) **`affectChar(Char ch)`**: 개별 처리 / 조건 분기 / 참조 호출: Buff.affect, incShield, ch.sprite.showStatusWithIcon, ch.buff, Buff.prolong
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L257) **`use(BlobEmitter emitter)`**: 이벤트·효과 실행 / 참조 호출: super.use, emitter.pour
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java#L263) **`tileDesc()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 154. [`HolyIntuition.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyIntuition.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 87행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyIntuition.java#L38) `class HolyIntuition  extends InventoryClericSpell`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyIntuition.java#L40) **`HolyIntuition()`**: 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyIntuition.java#L43) **`icon()`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyIntuition.java#L48) **`usableOnItem(Item item)`**: 개별 처리 / 참조 호출: item.isIdentified
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyIntuition.java#L53) **`chargeUse(Hero hero)`**: 개별 처리 / 참조 호출: hero.pointsInTalent
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyIntuition.java#L58) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyIntuition.java#L63) **`onItemSelected(HolyTome tome, Hero hero, Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: GLog.w, Messages.get, GLog.i, hero.spend, hero.busy, hero.sprite.operate, sprite.parent.add, Identification, hero.sprite.center

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 155. [`HolyLance.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 192행 / 타입 3개 / 필드 0개 / 메서드 14개.

### 타입·상속 선언

- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L52) `class HolyLance  extends TargetedClericSpell`
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L156) `class HolyLanceVFX  extends Item`
- [L177](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L177) `class LanceCooldown  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L54) **`HolyLance()`**: 개별 처리
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L57) **`icon()`**: 개별 처리
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L62) **`desc()`**: 개별 처리 / 참조 호출: Dungeon.hero.pointsInTalent, Math.round, Messages.get, chargeUse
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L69) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent, hero.buff
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L76) **`chargeUse(Hero hero)`**: 개별 처리
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L81) **`targetingFlags()`**: 개별 처리
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L86) **`onTargetSelected(HolyTome tome, Hero hero, Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Ballistica, targetingFlags, Actor.findChar, GLog.i, Messages.get, QuickSlotButton.target, hero.sprite.zap, hero.busy, Sample.INSTANCE.play
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L117) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.pointsInTalent, Math.round, Char.hasProp, enemy.damage, Hero.heroDamageIntRange, Sample.INSTANCE.play, Random.Float, enemy.isActive, Buff.affect
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L144) **`call()`**: 개별 처리 / 참조 호출: Splash.at, Dungeon.level.pressCell, hero.spendAndNext, onSpellCast, FlavourBuff.affect
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L163) **`glowing()`**: 개별 처리 / 참조 호출: ItemSprite.Glowing
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L168) **`emitter()`**: 개별 처리 / 참조 호출: Emitter, emitter.pos, emitter.pour
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L180) **`icon()`**: 개별 처리
- [L185](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L185) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.hardlight
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyLance.java#L189) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 156. [`HolyWard.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 113행 / 타입 2개 / 필드 1개 / 메서드 9개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java#L38) `class HolyWard  extends ClericSpell`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java#L70) `class HolyArmBuff  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java#L72) `float DURATION` 초기식: `50f`

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java#L40) **`HolyWard()`**: 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java#L43) **`icon()`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java#L48) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Buff.affect, Item.updateQuickslot, Sample.INSTANCE.play, hero.sprite.operate, hero.belongings.armor, Enchanting.show, onSpellCast
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java#L62) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, chargeUse
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java#L79) **`icon()`**: 개별 처리
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java#L84) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java#L89) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, dispTurns
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java#L98) **`detach()`**: 개별 처리 / 참조 호출: super.detach, Item.updateQuickslot
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java#L103) **`extend(float extension)`**: 개별 처리 / 조건 분기 / 참조 호출: cooldown, spend, postpone

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 157. [`HolyWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 118행 / 타입 2개 / 필드 1개 / 메서드 10개.

### 타입·상속 선언

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L38) `class HolyWeapon  extends ClericSpell`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L75) `class HolyWepBuff  extends FlavourBuff`

### 변수·상수 (단일 행 선언)

- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L77) `float DURATION` 초기식: `50f`

### 함수·메서드 역할과 내부 연결

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L40) **`HolyWeapon()`**: 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L43) **`icon()`**: 개별 처리
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L48) **`chargeUse(Hero hero)`**: 개별 처리
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L53) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Buff.affect, Item.updateQuickslot, Sample.INSTANCE.play, hero.sprite.operate, hero.belongings.weapon, Enchanting.show, onSpellCast
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L67) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, chargeUse
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L84) **`icon()`**: 개별 처리
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L89) **`iconFadePercent()`**: 개별 처리 / 참조 호출: Math.max, visualcooldown
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L94) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, dispTurns
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L103) **`detach()`**: 개별 처리 / 참조 호출: super.detach, Item.updateQuickslot
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java#L108) **`extend(float extension)`**: 개별 처리 / 조건 분기 / 참조 호출: cooldown, spend, postpone

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 158. [`InventoryClericSpell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/InventoryClericSpell.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 75행 / 타입 1개 / 필드 0개 / 메서드 9개.

### 타입·상속 선언

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/InventoryClericSpell.java#L32) `class InventoryClericSpell  extends ClericSpell`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/InventoryClericSpell.java#L35) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 참조 호출: GameScene.selectItem, WndBag.ItemSelector, textPrompt, inventoryPrompt, preferredBag, InventoryClericSpell.this.preferredBag, itemSelectable, usableOnItem, onSelect
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/InventoryClericSpell.java#L39) **`textPrompt()`**: 개별 처리 / 참조 호출: inventoryPrompt
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/InventoryClericSpell.java#L44) **`preferredBag()`**: 개별 처리 / 참조 호출: InventoryClericSpell.this.preferredBag
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/InventoryClericSpell.java#L49) **`itemSelectable(Item item)`**: 개별 처리 / 참조 호출: usableOnItem
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/InventoryClericSpell.java#L54) **`onSelect(Item item)`**: 이벤트·효과 실행 / 참조 호출: onItemSelected
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/InventoryClericSpell.java#L60) **`inventoryPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/InventoryClericSpell.java#L64) **`preferredBag()`**: 개별 처리
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/InventoryClericSpell.java#L68) **`usableOnItem(Item item)`**: 개별 처리
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/InventoryClericSpell.java#L72) **`onItemSelected(HolyTome tome, Hero hero, Item item)`**: 이벤트·효과 실행

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 159. [`Judgement.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Judgement.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells` / 본문 105행 / 타입 1개 / 필드 0개 / 메서드 7개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Judgement.java#L41) `class Judgement  extends ClericSpell`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Judgement.java#L43) **`Judgement()`**: 개별 처리
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Judgement.java#L46) **`icon()`**: 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Judgement.java#L51) **`chargeUse(Hero hero)`**: 개별 처리
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Judgement.java#L56) **`canCast(Hero hero)`**: 조건 판정 / 참조 호출: super.canCast, hero.hasTalent, hero.buff
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Judgement.java#L63) **`onCast(HolyTome tome, Hero hero)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: hero.sprite.attack, Callback, call, GameScene.flash, Sample.INSTANCE.play, hero.pointsInTalent, Math.round, hero.buff, Actor.chars
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Judgement.java#L67) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: GameScene.flash, Sample.INSTANCE.play, hero.pointsInTalent, Math.round, hero.buff, Actor.chars, ch.damage, Hero.heroDamageIntRange, Buff.affect
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Judgement.java#L95) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.hero.pointsInTalent, Dungeon.hero.buff, Math.round, Messages.get, chargeUse

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":29,"fields":8,"methods":155}

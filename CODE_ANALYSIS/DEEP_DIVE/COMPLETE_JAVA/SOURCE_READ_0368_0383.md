# Java 파일별 소스 구현 해설 368–383

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 368. [`PlateArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/PlateArmor.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor` / 본문 37행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/PlateArmor.java#L26) `class PlateArmor  extends Armor`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/PlateArmor.java#L32) **`PlateArmor()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 369. [`RogueArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/RogueArmor.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor` / 본문 32행 / 타입 1개 / 필드 0개 / 메서드 0개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/RogueArmor.java#L26) `class RogueArmor  extends ClassArmor`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- 검출 없음

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 370. [`ScaleArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ScaleArmor.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor` / 본문 37행 / 타입 1개 / 필드 0개 / 메서드 1개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ScaleArmor.java#L26) `class ScaleArmor  extends Armor`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ScaleArmor.java#L32) **`ScaleArmor()`**: 개별 처리

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 371. [`WarriorArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/WarriorArmor.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.armor` / 본문 32행 / 타입 1개 / 필드 0개 / 메서드 0개.

### 타입·상속 선언

- [L26](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/WarriorArmor.java#L26) `class WarriorArmor  extends ClassArmor`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- 검출 없음

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 372. [`AlchemistsToolkit.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 263행 / 타입 2개 / 필드 4개 / 메서드 17개.

### 타입·상속 선언

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L45) `class AlchemistsToolkit  extends Artifact`
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L220) `class kitEnergy  extends ArtifactBuff`

### 변수·상수 (단일 행 선언)

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L57) `String AC_BREW` 초기식: `"BREW"`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L58) `String AC_ENERGIZE` 초기식: `"ENERGIZE"`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L60) `float warmUpDelay`
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L206) `String WARM_UP` 초기식: `"warm_up"`

### 함수·메서드 역할과 내부 연결

- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L63) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, hero.buff, actions.add, level
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L75) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, hero.buff, action.equals, isEquipped, GLog.i, Messages.get, GLog.w, AlchemyScene.assignToolkit, Game.switchScene
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L96) **`min(levelCap - level(), Dungeon.energy/6)`**: 개별 처리
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L110) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.onSelect, Sample.INSTANCE.play, Sample.INSTANCE.playDelayed, hero.sprite.operate, upgrade, Catalog.countUse, Catalog.countUses
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L132) **`hasIcon(int index)`**: 조건 판정
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L137) **`getIcon(int index)`**: 조회·탐색 / 참조 호출: ItemSprite
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L148) **`status()`**: 개별 처리 / 조건 분기 / 참조 호출: isEquipped, Messages.format, Math.max, super.status
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L157) **`passiveBuff()`**: 개별 처리 / 참조 호출: kitEnergy
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L162) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, updateQuickslot
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L172) **`availableEnergy()`**: 개별 처리
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L176) **`consumeEnergy(int amount)`**: 개별 처리 / 참조 호출: Math.max, Talent.onArtifactUsed
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L184) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, isEquipped
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L197) **`doEquip(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doEquip
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L209) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L215) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getFloat
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L223) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: level, target.buff, Math.pow, updateQuickslot, spend
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java#L241) **`gainCharge(float levelPortion)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, level, RingOfEnergy.artifactChargeMultiplier, updateQuickslot

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 373. [`Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 302행 / 타입 2개 / 필드 11개 / 메서드 23개.

### 타입·상속 선언

- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L41) `class Artifact  extends KindofMisc`
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L253) `class ArtifactBuff  extends Buff`

### 변수·상수 (단일 행 선언)

- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L43) `Buff passiveBuff`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L44) `Buff activeBuff`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L49) `int exp` 초기식: `0`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L51) `int levelCap` 초기식: `0`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L54) `int charge` 초기식: `0`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L57) `float partialCharge` 초기식: `0`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L59) `int chargeCap` 초기식: `0`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L62) `int cooldown` 초기식: `0`
- [L281](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L281) `String EXP` 초기식: `"exp"`
- [L282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L282) `String CHARGE` 초기식: `"charge"`
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L283) `String PARTIALCHARGE` 초기식: `"partialcharge"`

### 함수·메서드 역할과 내부 연결

- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L65) **`doEquip(final Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: belongings.artifact.getClass, this.getClass, belongings.misc.getClass, GLog.w, Messages.get, super.doEquip, identify
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L90) **`activate(Char ch)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: passiveBuff.detach, passiveBuff, passiveBuff.attachTo
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L100) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doUnequip, passiveBuff.detach
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L118) **`isUpgradable()`**: 조건 판정
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L123) **`visiblyUpgraded()`**: 개별 처리 / 참조 호출: Math.round, level
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L128) **`buffedVisiblyUpgraded()`**: 개별 처리 / 참조 호출: visiblyUpgraded
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L133) **`buffedLvl()`**: 개별 처리 / 참조 호출: level
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L139) **`transferUpgrade(int transferLvl)`**: 개별 처리 / 참조 호출: upgrade, Math.round
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L143) **`resetForTrinity(int visibleLevel)`**: 생성·초기화 / 참조 호출: level, Math.round
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L150) **`artifactProc(Char target, int artifLevel, int chargesUsed)`**: 개별 처리 / 조건 분기 / 참조 호출: target.buff, detach, target.damage, Dungeon.hero.hasTalent, Dungeon.hero.buff, Buff.affect, Random.Int, Dungeon.hero.pointsInTalent, Buff.prolong
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L175) **`info()`**: 개별 처리 / 조건 분기 / 참조 호출: isEquipped, super.info, Messages.get, isIdentified
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L189) **`status()`**: 개별 처리 / 조건 분기 / 참조 호출: isIdentified, Messages.format
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L218) **`random()`**: 개별 처리 / 조건 분기 / 참조 호출: Random.Float
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L229) **`value()`**: 개별 처리 / 조건 분기 / 참조 호출: level, visiblyUpgraded
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L243) **`passiveBuff()`**: 개별 처리
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L247) **`activeBuff()`**: 시간·상태 갱신
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L249) **`charge(Hero target, float amount)`**: 개별 처리
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L256) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, cooldown, target.cooldown, spend
- [L267](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L267) **`itemLevel()`**: 개별 처리 / 참조 호출: level
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L271) **`isCursed()`**: 조건 판정 / 참조 호출: target.buff
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L275) **`charge(Hero target, float amount)`**: 개별 처리 / 참조 호출: Artifact.this.charge
- [L286](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L286) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java#L294) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt, Math.min, bundle.getFloat

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 374. [`CapeOfThorns.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 149행 / 타입 2개 / 필드 0개 / 메서드 8개.

### 타입·상속 선언

- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java#L34) `class CapeOfThorns  extends Artifact`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java#L78) `class Thorns  extends ArtifactBuff`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java#L49) **`passiveBuff()`**: 개별 처리 / 참조 호출: Thorns
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java#L54) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기 / 참조 호출: Math.round, updateQuickslot, target.buff, proc
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java#L65) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, isEquipped
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java#L81) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: GLog.w, Messages.get, updateQuickslot, spend
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java#L93) **`proc(int damage, Char attacker, Char defender)`**: 개별 처리 / 조건 분기 / 참조 호출: level, GLog.p, Messages.get, Random.NormalIntRange, Dungeon.level.adjacent, attacker.damage, upgrade, Catalog.countUse, updateQuickslot
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java#L126) **`desc()`**: 개별 처리 / 참조 호출: Messages.get, dispTurns
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java#L131) **`icon()`**: 개별 처리 / 조건 분기
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java#L139) **`detach()`**: 개별 처리 / 참조 호출: super.detach

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 375. [`ChaliceOfBlood.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 239행 / 타입 2개 / 필드 1개 / 메서드 11개.

### 타입·상속 선언

- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L51) `class ChaliceOfBlood  extends Artifact`
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L234) `class chaliceRegen  extends ArtifactBuff`

### 변수·상수 (단일 행 선언)

- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L59) `String AC_PRICK` 초기식: `"PRICK"`

### 함수·메서드 역할과 내부 연결

- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L62) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, level, hero.isInvulnerable, getClass, hero.buff, actions.add
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L74) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, action.equals, minPrickDmg, maxPrickDmg, hero.shielding, Math.pow, GameScene.show, WndOptions, ItemSprite
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L108) **`onSelect(int index)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: prick
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L119) **`minPrickDmg()`**: 개별 처리 / 참조 호출: Math.ceil, level
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L123) **`maxPrickDmg()`**: 개별 처리 / 참조 호출: Math.floor, level
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L127) **`prick(Hero hero)`**: 개별 처리 / 조건 분기 / 참조 호출: Random.NormalIntRange, minPrickDmg, maxPrickDmg, hero.buff, armor.absorb, rockArmor.absorb, hero.drRoll, hero.sprite.operate, hero.busy
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L171) **`upgrade()`**: 개별 처리 / 조건 분기 / 참조 호출: level, super.upgrade
- [L180](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L180) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, level
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L187) **`passiveBuff()`**: 개별 처리 / 참조 호출: chaliceRegen
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L192) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기 / 참조 호출: target.buff, target.isStarving, level, Random.Float, Math.min, target.sprite.showStatusWithIcon, Integer.toString
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java#L216) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, isEquipped, Messages.get, level

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 376. [`CloakOfShadows.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 402행 / 타입 3개 / 필드 5개 / 메서드 27개.

### 타입·상속 선언

- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L50) `class CloakOfShadows  extends Artifact`
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L230) `class cloakRecharge  extends ArtifactBuff`
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L270) `class cloakStealth  extends ArtifactBuff`

### 변수·상수 (단일 행 선언)

- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L68) `String AC_STEALTH` 초기식: `"STEALTH"`
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L207) `String STEALTHED` 초기식: `"stealthed"`
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L208) `String BUFF` 초기식: `"buff"`
- [L384](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L384) `String TURNSTOCOST` 초기식: `"turnsToCost"`
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L385) `String BARRIER_INC` 초기식: `"barrier_inc"`

### 함수·메서드 역할과 내부 연결

- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L71) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, hero.hasTalent, hero.buff, actions.add
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L83) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, hero.buff, action.equals, isEquipped, hero.hasTalent, GLog.i, Messages.get, hero.spend, hero.busy
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L117) **`activate(Char ch)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.activate, activeBuff.attachTo
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L125) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doUnequip, hero.hasTalent, activeBuff.detach, activate
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L142) **`collect(Bag container)`**: 개별 처리 / 조건 분기 / 참조 호출: super.collect, hasTalent, activate
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L156) **`onDetach()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: passiveBuff.detach, isEquipped, activeBuff.detach
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L168) **`passiveBuff()`**: 개별 처리 / 참조 호출: cloakRecharge
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L173) **`activeBuff()`**: 시간·상태 갱신 / 참조 호출: cloakStealth
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L178) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, isEquipped, target.pointsInTalent, updateQuickslot
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L196) **`directCharge(int amount)`**: 개별 처리 / 참조 호출: Math.min, updateQuickslot
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L202) **`upgrade()`**: 개별 처리 / 참조 호출: Math.min, super.upgrade
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L211) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L217) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.contains, cloakStealth, activeBuff.restoreFromBundle, bundle.getBundle
- [L226](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L226) **`value()`**: 개별 처리
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L232) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: target.buff, Regeneration.regenOn, level, RingOfEnergy.artifactChargeMultiplier, isEquipped, Dungeon.hero.pointsInTalent, updateQuickslot, spend
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L279) **`icon()`**: 개별 처리
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L284) **`tintIcon(Image icon)`**: 개별 처리 / 참조 호출: icon.brightness
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L289) **`iconFadePercent()`**: 개별 처리
- [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L294) **`iconTextDisplay()`**: 개별 처리 / 참조 호출: Integer.toString
- [L299](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L299) **`desc()`**: 개별 처리 / 참조 호출: Messages.get
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L304) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, Buff.affect, hasTalent
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L320) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: detach, GLog.w, Messages.get, interrupt, level, Math.round, Math.pow, upgrade, Catalog.countUse
- [L360](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L360) **`dispel()`**: 개별 처리 / 조건 분기 / 참조 호출: updateQuickslot, detach
- [L369](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L369) **`fx(boolean on)`**: 개별 처리 / 조건 분기 / 참조 호출: target.sprite.add, target.sprite.remove
- [L375](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L375) **`detach()`**: 개별 처리 / 조건 분기 / 참조 호출: updateQuickslot, super.detach
- [L388](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L388) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L395](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java#L395) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 377. [`DriedRose.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 1058행 / 타입 6개 / 필드 23개 / 메서드 64개.

### 타입·상속 선언

- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L86) `class DriedRose  extends Artifact`
- [L398](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L398) `class roseRecharge  extends ArtifactBuff`
- [L491](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L491) `class Petal  extends Item`
- [L542](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L542) `class GhostHero  extends DirectableAlly`
- [L630](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L630) `class NoRoseDamage`
- [L879](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L879) `class WndGhostHero  extends Window`

### 변수·상수 (단일 행 선언)

- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L99) `boolean talkedTo` 초기식: `false`
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L100) `boolean firstSummon` 초기식: `false`
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L102) `GhostHero ghost` 초기식: `null`
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L103) `int ghostID` 초기식: `0`
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L105) `MeleeWeapon weapon` 초기식: `null`
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L106) `Armor armor` 초기식: `null`
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L108) `int droppedPetals` 초기식: `0`
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L110) `String AC_SUMMON` 초기식: `"SUMMON"`
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L111) `String AC_DIRECT` 초기식: `"DIRECT"`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L112) `String AC_OUTFIT` 초기식: `"OUTFIT"`
- [L364](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L364) `String TALKEDTO` 초기식: `"talkedto"`
- [L365](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L365) `String FIRSTSUMMON` 초기식: `"firstsummon"`
- [L366](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L366) `String GHOSTID` 초기식: `"ghostID"`
- [L367](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L367) `String PETALS` 초기식: `"petals"`
- [L369](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L369) `String WEAPON` 초기식: `"weapon"`
- [L370](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L370) `String ARMOR` 초기식: `"armor"`
- [L555](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L555) `DriedRose rose` 초기식: `null`
- [L881](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L881) `int BTN_SIZE` 초기식: `32`
- [L882](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L882) `float GAP` 초기식: `2`
- [L883](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L883) `float BTN_GAP` 초기식: `12`
- [L884](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L884) `int WIDTH` 초기식: `116`
- [L886](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L886) `ItemButton btnWeapon`
- [L887](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L887) `ItemButton btnArmor`

### 함수·메서드 역할과 내부 연결

- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L115) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, Ghost.Quest.completed, isEquipped, hero.buff, actions.add, isIdentified
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L139) **`defaultAction()`**: 개별 처리 / 조건 분기
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L148) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: super.execute, action.equals, hero.buff, Ghost.Quest.completed, GameScene.show, WndUseItem, GLog.i, Messages.get, isEquipped
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L221) **`findGhost()`**: 조회·탐색 / 조건 분기 / 참조 호출: Actor.findById, Stasis.getStasisAlly, ghost.id
- [L235](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L235) **`ghostStrength()`**: 개별 처리 / 참조 호출: level
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L240) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Ghost.Quest.completed, ShatteredPixelDungeon.scene, Messages.get, super.desc, isEquipped, level, Messages.titleCase, weapon.title, armor.title
- [L278](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L278) **`value()`**: 개별 처리 / 조건 분기 / 참조 호출: super.value
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L289) **`status()`**: 개별 처리 / 조건 분기·예외 처리 / 참조 호출: findGhost, ShatteredPixelDungeon.reportException, super.status
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L306) **`passiveBuff()`**: 개별 처리 / 참조 호출: roseRecharge
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L311) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, GLog.p, Messages.get, updateQuickslot, Math.round, level, Math.min, ghost.sprite.showStatusWithIcon, Integer.toString
- [L339](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L339) **`upgrade()`**: 개별 처리 / 조건 분기 / 참조 호출: level, Math.max, ghost.updateRose, Math.min, super.upgrade
- [L356](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L356) **`ghostWeapon()`**: 개별 처리
- [L360](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L360) **`ghostArmor()`**: 개별 처리
- [L373](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L373) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L386](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L386) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getBoolean, bundle.getInt, bundle.contains, bundle.get
- [L401](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L401) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: spend, findGhost, ghost.isAlive, target.buff, Regeneration.regenOn, RingOfEnergy.artifactChargeMultiplier, updateQuickslot, GLog.p, Messages.get
- [L473](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L473) **`Listener()`**: 개별 처리 / 조건 분기 / 참조 호출: onSelect, Sample.INSTANCE.play, ghost.directTocell, prompt, Messages.get
- [L476](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L476) **`onSelect(Integer cell)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: Sample.INSTANCE.play, ghost.directTocell
- [L486](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L486) **`prompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L501](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L501) **`doPickUp(Hero hero, int pos)`**: 개별 처리 / 조건 분기 / 참조 호출: Catalog.setSeen, getClass, Statistics.itemTypesDiscovered.add, hero.belongings.getItem, GLog.w, Messages.get, rose.level, GLog.i, hero.spendAndNext
- [L531](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L531) **`isUpgradable()`**: 조건 판정
- [L536](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L536) **`isIdentified()`**: 조건 판정
- [L557](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L557) **`GhostHero()`**: 개별 처리
- [L561](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L561) **`GhostHero(DriedRose rose)`**: 개별 처리 / 참조 호출: updateRose
- [L569](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L569) **`defendPos(int cell)`**: 개별 처리 / 참조 호출: yell, Messages.get, Random.IntRange, super.defendPos
- [L575](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L575) **`followHero()`**: 개별 처리 / 참조 호출: yell, Messages.get, Random.IntRange, super.followHero
- [L581](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L581) **`targetChar(Char ch)`**: 개별 처리 / 참조 호출: yell, Messages.get, Random.IntRange, super.targetChar
- [L586](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L586) **`updateRose()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: hero.belongings.getItem, id, rose.level
- [L601](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L601) **`weapon()`**: 개별 처리 / 조건 분기
- [L606](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L606) **`clearWeapon()`**: 상태 갱신 / 조건 분기
- [L610](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L610) **`armor()`**: 개별 처리 / 조건 분기
- [L616](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L616) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: updateRose, rose.isEquipped, Dungeon.hero.buff, damage, NoRoseDamage, isAlive, super.act
- [L633](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L633) **`attackSkill(Char target)`**: 전투 관련 / 조건 분기 / 참조 호출: weapon, accuracyFactor
- [L646](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L646) **`attackDelay()`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackDelay, weapon, delayFactor
- [L655](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L655) **`canAttack(Char enemy)`**: 조건 판정 / 참조 호출: super.canAttack, weapon, canReach
- [L660](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L660) **`damageRoll()`**: 전투 관련 / 조건 분기 / 참조 호출: weapon, damageRoll, rose.ghostStrength, STRReq, Random.NormalIntRange
- [L679](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L679) **`attackProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: super.attackProc, weapon, proc, enemy.isAlive, Dungeon.fail, GLog.n, Messages.capitalize, Messages.get, name
- [L694](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L694) **`defenseProc(Char enemy, int damage)`**: 전투 관련 / 조건 분기 / 참조 호출: armor, proc, super.defenseProc
- [L702](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L702) **`damage(int dmg, Object src)`**: 전투 관련 / 참조 호출: super.damage, Item.updateQuickslot
- [L710](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L710) **`speed()`**: 개별 처리 / 조건 분기 / 참조 호출: super.speed, Dungeon.level.distance
- [L724](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L724) **`defenseSkill(Char enemy)`**: 전투 관련 / 조건 분기 / 참조 호출: super.defenseSkill, armor, Math.round, evasionFactor
- [L735](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L735) **`drRoll()`**: 개별 처리 / 조건 분기 / 참조 호출: super.drRoll, armor, Random.NormalIntRange, DRMin, DRMax, weapon, defenseFactor
- [L747](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L747) **`glyphLevel(Class<? extends Armor.Glyph> cls)`**: 개별 처리 / 조건 분기 / 참조 호출: armor, hasGlyph, Math.max, super.glyphLevel, buffedLvl
- [L756](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L756) **`interact(Char c)`**: 개별 처리 / 조건 분기 / 참조 호출: updateRose, Game.runOnRenderThread, Callback, call, GameScene.show, WndQuest, Messages.get, super.interact
- [L762](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L762) **`call()`**: 개별 처리 / 참조 호출: GameScene.show, WndQuest, Messages.get
- [L773](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L773) **`die(Object cause)`**: 개별 처리 / 참조 호출: sayDefeated, super.die
- [L779](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L779) **`destroy()`**: 개별 처리 / 조건 분기 / 참조 호출: updateRose, super.destroy
- [L791](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L791) **`sayAppeared()`**: 개별 처리 / 조건 분기·상태 선택 / 참조 호출: Dungeon.hero.buff, yell, Messages.get, Random.IntRange, ShatteredPixelDungeon.scene, Sample.INSTANCE.play
- [L826](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L826) **`sayBoss()`**: 개별 처리 / 상태 선택 / 참조 호출: yell, Messages.get, Random.IntRange, Sample.INSTANCE.play
- [L849](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L849) **`sayDefeated()`**: 개별 처리 / 조건 분기 / 참조 호출: BossHealthBar.isAssigned, yell, Messages.get, Random.IntRange, Sample.INSTANCE.play
- [L858](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L858) **`sayHeroKilled()`**: 개별 처리 / 참조 호출: yell, Messages.get, Random.IntRange, GLog.newLine, Sample.INSTANCE.play
- [L864](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L864) **`sayAnhk()`**: 개별 처리 / 참조 호출: yell, Messages.get, Random.IntRange, Sample.INSTANCE.play
- [L905](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L905) **`onClick()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: item, WndBag.Placeholder, rose.weapon.doPickUp, Dungeon.level.drop, GameScene.selectItem, WndBag.ItemSelector, textPrompt, Messages.get, preferredBag
- [L916](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L916) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L921](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L921) **`preferredBag()`**: 개별 처리
- [L926](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L926) **`itemSelectable(Item item)`**: 개별 처리
- [L931](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L931) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: GLog.w, Messages.get, hide, STRReq, rose.ghostStrength, item.isEquipped, doUnequip, item.detach, item
- [L962](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L962) **`onLongClick()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: item, name, GameScene.show, WndInfoItem
- [L980](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L980) **`onClick()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: item, WndBag.Placeholder, rose.armor.doPickUp, Dungeon.level.drop, GameScene.selectItem, WndBag.ItemSelector, textPrompt, Messages.get, preferredBag
- [L991](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L991) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L996](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L996) **`preferredBag()`**: 개별 처리
- [L1001](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L1001) **`itemSelectable(Item item)`**: 개별 처리
- [L1006](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L1006) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: checkSeal, GLog.w, Messages.get, hide, STRReq, rose.ghostStrength, item.isEquipped, doUnequip, item.detach
- [L1037](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java#L1037) **`onLongClick()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: item, name, GameScene.show, WndInfoItem

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 378. [`EtherealChains.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 365행 / 타입 2개 / 필드 3개 / 메서드 19개.

### 타입·상속 선언

- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L57) `class EtherealChains  extends Artifact`
- [L315](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L315) `class chainsRecharge  extends ArtifactBuff`

### 변수·상수 (단일 행 선언)

- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L59) `String AC_CAST` 초기식: `"CAST"`
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L178) `int pulledPos` 초기식: `bestPos`
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L246) `int newHeroPos` 초기식: `chain.collisionPos`

### 함수·메서드 역할과 내부 연결

- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L74) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, hero.buff, actions.add
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L82) **`targetingPos(Hero user, int dst)`**: 개별 처리
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L87) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, hero.buff, action.equals, isEquipped, GLog.i, Messages.get, GLog.w, GameScene.selectCell
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L118) **`resetForTrinity(int visibleLevel)`**: 생성·초기화 / 참조 호출: super.resetForTrinity, level
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L123) **`Listener()`**: 개별 처리 / 조건 분기 / 참조 호출: onSelect, PathFinder.buildDistanceMap, BArray.or, GLog.w, Messages.get, Ballistica, Actor.findChar, chainEnemy, chainLocation
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L126) **`onSelect(Integer target)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: PathFinder.buildDistanceMap, BArray.or, GLog.w, Messages.get, Ballistica, Actor.findChar, chainEnemy, chainLocation
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L136) **`Ballistica(curUser.pos, target, Ballistica.STOP_TARGET)`**: 개별 처리
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L149) **`prompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L155) **`chainEnemy(Ballistica chain, final Hero hero, final Char enemy)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: enemy.properties, contains, GLog.w, Messages.get, chain.subPath, Actor.findChar, Char.hasProp, GLog.i, Dungeon.level.distance
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L193) **`call()`**: 개별 처리 / 참조 호출: Actor.add, Pushing, Callback, call, Invisibility.dispel, Talent.onArtifactUsed, updateQuickslot, Dungeon.level.occupyCell, Dungeon.observe
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L195) **`call()`**: 개별 처리 / 참조 호출: Invisibility.dispel, Talent.onArtifactUsed, updateQuickslot, Dungeon.level.occupyCell, Dungeon.observe, GameScene.updateFog, hero.spendAndNext, artifactProc, visiblyUpgraded
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L217) **`chainLocation(Ballistica chain, final Hero hero)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: PixelScene.shake, GLog.w, Messages.get, GLog.i, Dungeon.level.distance, hero.busy, throwSound, Sample.INSTANCE.play, sprite.parent.add
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L261) **`call()`**: 개별 처리 / 참조 호출: Actor.add, Pushing, Callback, call, Invisibility.dispel, Talent.onArtifactUsed, updateQuickslot, Dungeon.level.occupyCell, hero.spendAndNext
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L263) **`call()`**: 개별 처리 / 참조 호출: Invisibility.dispel, Talent.onArtifactUsed, updateQuickslot, Dungeon.level.occupyCell, hero.spendAndNext, Dungeon.observe, GameScene.updateFog
- [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L283) **`passiveBuff()`**: 개별 처리 / 참조 호출: chainsRecharge
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L288) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, level, updateQuickslot
- [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L302) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, isEquipped, Messages.get
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L318) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: level, target.buff, Regeneration.regenOn, RingOfEnergy.artifactChargeMultiplier, Random.Int, Buff.prolong, updateQuickslot, spend
- [L344](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java#L344) **`gainExp(float levelPortion)`**: 개별 처리 / 조건 분기 / 참조 호출: target.buff, Math.round, level, GLog.p, Messages.get, Catalog.countUses, upgrade

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 379. [`HolyTome.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 375행 / 타입 2개 / 필드 4개 / 메서드 22개.

### 타입·상속 선언

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L49) `class HolyTome  extends Artifact`
- [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L269) `class TomeRecharge  extends ArtifactBuff implements ActionIndicator.Action`

### 변수·상수 (단일 행 선언)

- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L67) `String AC_CAST` 초기식: `"CAST"`
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L101) `ClericSpell targetingSpell` 초기식: `null`
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L230) `ClericSpell quickSpell` 초기식: `null`
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L246) `String QUICK_CLS` 초기식: `"quick_cls"`

### 함수·메서드 역할과 내부 연결

- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L70) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, hero.hasTalent, hero.buff, actions.add
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L81) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, hero.buff, action.equals, isEquipped, hero.hasTalent, GLog.i, Messages.get, GameScene.show, WndClericSpells
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L104) **`targetingPos(Hero user, int dst)`**: 개별 처리 / 조건 분기 / 참조 호출: targetingSpell.targetingFlags, super.targetingPos, Ballistica
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L113) **`doUnequip(Hero hero, boolean collect, boolean single)`**: 개별 처리 / 조건 분기 / 참조 호출: super.doUnequip, hero.hasTalent, activate
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L125) **`collect(Bag container)`**: 개별 처리 / 조건 분기 / 참조 호출: super.collect, hasTalent, activate
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L139) **`onDetach()`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: passiveBuff.detach
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L146) **`canCast(Hero hero, ClericSpell spell)`**: 조건 판정 / 참조 호출: isEquipped, Dungeon.hero.hasTalent, hero.belongings.contains, hero.buff, spell.chargeUse, spell.canCast
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L153) **`spendCharge(float chargesSpent)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: level, Math.round, Math.pow, upgrade, Catalog.countUse, GLog.p, Messages.get, updateQuickslot
- [L184](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L184) **`directCharge(float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: updateQuickslot
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L201) **`upgrade()`**: 개별 처리 / 참조 호출: Math.min, super.upgrade
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L207) **`passiveBuff()`**: 개별 처리 / 참조 호출: TomeRecharge
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L212) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, isEquipped, target.pointsInTalent, updateQuickslot
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L232) **`setQuickSpell(ClericSpell spell)`**: 상태 갱신 / 조건 분기 / 참조 호출: ActionIndicator.clearAction, ActionIndicator.setAction
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L249) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put, quickSpell.getClass
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L257) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: super.restoreFromBundle, bundle.contains, bundle.getClass, ClericSpell.getAllSpells, spell.getClass
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L272) **`attachTo(Char target)`**: 개별 처리 / 조건 분기 / 참조 호출: super.attachTo, ActionIndicator.setAction
- [L282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L282) **`detach()`**: 개별 처리 / 참조 호출: super.detach, ActionIndicator.clearAction
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L288) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: target.buff, Regeneration.regenOn, level, RingOfEnergy.artifactChargeMultiplier, isEquipped, Dungeon.hero.pointsInTalent, updateQuickslot, spend
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L322) **`actionName()`**: 시간·상태 갱신 / 참조 호출: quickSpell.name
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L327) **`actionIcon()`**: 시간·상태 갱신 / 참조 호출: quickSpell.icon
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L332) **`indicatorColor()`**: 개별 처리 / 조건 분기 / 참조 호출: quickSpell.chargeUse
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java#L341) **`doAction()`**: 개별 처리 / 조건 분기 / 참조 호출: GLog.w, Messages.get, canCast, Dungeon.quickslot.getItem, QuickSlotButton.autoAim, GameScene.handleCell, quickSpell.onCast, quickSpell.targetingFlags, Dungeon.quickslot.contains

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 380. [`HornOfPlenty.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 350행 / 타입 2개 / 필드 5개 / 메서드 17개.

### 타입·상속 선언

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L55) `class HornOfPlenty  extends Artifact`
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L273) `class hornRecharge  extends ArtifactBuff`

### 변수·상수 (단일 행 선언)

- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L70) `int storedFoodEnergy` 초기식: `0`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L72) `String AC_SNACK` 초기식: `"SNACK"`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L73) `String AC_EAT` 초기식: `"EAT"`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L74) `String AC_STORE` 초기식: `"STORE"`
- [L254](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L254) `String STORED` 초기식: `"stored"`

### 함수·메서드 역할과 내부 연결

- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L77) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, hero.buff, isEquipped, actions.add, level
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L91) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, hero.buff, action.equals, isEquipped, GLog.i, Messages.get, Dungeon.isChallenged, Buff.affect, Math.max
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L127) **`doEatEffect(Hero hero, int chargesToUse)`**: 개별 처리 / 조건 분기 / 참조 호출: Dungeon.isChallenged, Buff.affect, satisfy, Talent.onArtifactUsed, hero.sprite.operate, hero.busy, SpellSprite.show, Sample.INSTANCE.play, GLog.i
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L170) **`passiveBuff()`**: 개별 처리 / 참조 호출: hornRecharge
- [L175](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L175) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, GLog.p, Messages.get, updateQuickslot
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L198) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, isEquipped, level, Messages.get
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L214) **`level(int value)`**: 개별 처리 / 참조 호출: super.level, level
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L221) **`upgrade()`**: 개별 처리 / 참조 호출: super.upgrade, level
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L227) **`gainFoodValue(Food food)`**: 개별 처리 / 조건 분기 / 참조 호출: level, Math.min, upgrade, Catalog.countUse, GLog.p, Messages.get, GLog.i
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L257) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L263) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L275) **`gainCharge(float levelPortion)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, level, RingOfEnergy.artifactChargeMultiplier, updateQuickslot, GLog.p, Messages.get
- [L314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L314) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, Messages.get, preferredBag, itemSelectable, onSelect, GLog.w, hero.sprite.operate, hero.busy, hero.spend
- [L317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L317) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L322) **`preferredBag()`**: 개별 처리
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L327) **`itemSelectable(Item item)`**: 개별 처리
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java#L332) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: GLog.w, Messages.get, hero.sprite.operate, hero.busy, hero.spend, gainFoodValue, item.detach

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 381. [`LloydsBeacon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 338행 / 타입 2개 / 필드 8개 / 메서드 17개.

### 타입·상속 선언

- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L53) `class LloydsBeacon  extends Artifact`
- [L316](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L316) `class beaconRecharge  extends ArtifactBuff`

### 변수·상수 (단일 행 선언)

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L55) `float TIME_TO_USE` 초기식: `1`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L57) `String AC_ZAP` 초기식: `"ZAP"`
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L58) `String AC_SET` 초기식: `"SET"`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L59) `String AC_RETURN` 초기식: `"RETURN"`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L61) `int returnDepth` 초기식: `-1`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L62) `int returnPos`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L76) `String DEPTH` 초기식: `"depth"`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L77) `String POS` 초기식: `"pos"`

### 함수·메서드 역할과 내부 연결

- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L80) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 조건 분기 / 참조 호출: super.storeInBundle, bundle.put
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L89) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.restoreFromBundle, bundle.getInt
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L96) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, actions.add
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L107) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: super.execute, Dungeon.bossLevel, Dungeon.interfloorTeleportAllowed, hero.spend, GLog.w, Messages.get, Actor.findChar, isEquipped, GLog.i
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L190) **`Listener()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: onSelect, Invisibility.dispel, Dungeon.scalingDepth, updateQuickslot, Actor.findChar, ScrollOfTeleportation.teleportChar, curUser.spendAndNext, Ballistica, Sample.INSTANCE.play
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L193) **`onSelect(Integer target)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Invisibility.dispel, Dungeon.scalingDepth, updateQuickslot, Actor.findChar, ScrollOfTeleportation.teleportChar, curUser.spendAndNext, Ballistica, Sample.INSTANCE.play, curUser.sprite.zap
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L205) **`Ballistica(curUser.pos, target, Ballistica.MAGIC_BOLT)`**: 개별 처리
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L206) **`findChar(bolt.collisionPos)`**: 조회·탐색
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L222) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Dungeon.level.randomRespawnCell, Dungeon.bossLevel, GLog.w, Messages.get, ch.properties, contains, ch.sprite.place, curUser.spendAndNext
- [L265](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L265) **`prompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L271) **`passiveBuff()`**: 개별 처리 / 참조 호출: beaconRecharge
- [L276](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L276) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: updateQuickslot
- [L293](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L293) **`upgrade()`**: 개별 처리 / 조건 분기 / 참조 호출: level, GLog.p, Messages.get, super.upgrade
- [L301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L301) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, Messages.get
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L309) **`Glowing(0xFFFFFF)`**: 개별 처리
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L312) **`glowing()`**: 개별 처리
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/LloydsBeacon.java#L318) **`act()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: Regeneration.regenOn, updateQuickslot, spend

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 382. [`MasterThievesArmband.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 341행 / 타입 3개 / 필드 1개 / 메서드 17개.

### 타입·상속 선언

- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L55) `class MasterThievesArmband  extends Artifact`
- [L211](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L211) `class StolenTracker  extends CounterBuff`
- [L261](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L261) `class Thievery  extends ArtifactBuff`

### 변수·상수 (단일 행 선언)

- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L69) `String AC_STEAL` 초기식: `"STEAL"`

### 함수·메서드 역할과 내부 연결

- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L72) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, isEquipped, hero.buff, actions.add
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L84) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, hero.buff, action.equals, isEquipped, GLog.i, Messages.get, GLog.w, GameScene.selectCell
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L113) **`Listener()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: onSelect, Dungeon.level.adjacent, Actor.findChar, GLog.w, Messages.get, curUser.busy, curUser.sprite.attack, Callback, call
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L116) **`onSelect(Integer target)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Dungeon.level.adjacent, Actor.findChar, GLog.w, Messages.get, curUser.busy, curUser.sprite.attack, Callback, call, Sample.INSTANCE.play
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L133) **`call()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: Sample.INSTANCE.play, surprisedBy, level, Invisibility.dispel, Surprise.hit, lootChance, ch.buff, GLog.w, Messages.get
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L205) **`prompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L213) **`setItemStolen(boolean stolen)`**: 상태 갱신 / 조건 분기 / 참조 호출: countUp
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L214) **`itemWasStolen()`**: 개별 처리 / 참조 호출: count
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L218) **`passiveBuff()`**: 개별 처리 / 참조 호출: Thievery
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L223) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, GLog.p, Messages.get, updateQuickslot
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L241) **`upgrade()`**: 개별 처리 / 참조 호출: level, super.upgrade
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L247) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: super.desc, isEquipped, Messages.get
- [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L264) **`act()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: Random.Int, updateQuickslot, spend
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L274) **`gainCharge(float levelPortion)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, level, RingOfEnergy.artifactChargeMultiplier, updateQuickslot, GLog.p, Messages.get
- [L299](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L299) **`steal(Item item)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: chargesToUse, stealChance, Random.Float, GLog.i, Messages.get, item.name, Talent.onArtifactUsed, Math.round, level
- [L321](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L321) **`stealChance(Item item)`**: 개별 처리 / 참조 호출: chargesToUse, level, Math.min, item.value
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java#L327) **`chargesToUse(Item item)`**: 개별 처리 / 반복 / 참조 호출: item.value, level

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 383. [`SandalsOfNature.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.items.artifacts` / 본문 375행 / 타입 2개 / 필드 5개 / 메서드 21개.

### 타입·상속 선언

- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L70) `class SandalsOfNature  extends Artifact`
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L271) `class Naturalism  extends ArtifactBuff`

### 변수·상수 (단일 행 선언)

- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L83) `String AC_FEED` 초기식: `"FEED"`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L84) `String AC_ROOT` 초기식: `"ROOT"`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L87) `Class curSeedEffect` 초기식: `null`
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L245) `String SEEDS` 초기식: `"seeds"`
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L246) `String CUR_SEED_EFFECT` 초기식: `"cur_seed_effect"`

### 함수·메서드 역할과 내부 연결

- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L122) **`actions(Hero hero)`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.actions, hero.buff, isEquipped, actions.add, seedChargeReqs.get
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L140) **`execute(Hero hero, String action)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: super.execute, hero.buff, action.equals, GameScene.selectItem, isEquipped, GLog.i, Messages.get, seedChargeReqs.get, GameScene.selectCell
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L161) **`passiveBuff()`**: 개별 처리 / 참조 호출: Naturalism
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L166) **`charge(Hero target, float amount)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, updateQuickslot
- [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L183) **`glowing()`**: 개별 처리 / 조건 분기 / 참조 호출: ItemSprite.Glowing, seedColors.get
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L191) **`name()`**: 개별 처리 / 조건 분기 / 참조 호출: level, super.name, Messages.get
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L197) **`desc()`**: 개별 처리 / 조건 분기 / 참조 호출: Messages.get, level, isEquipped, Messages.titleCase, seedChargeReqs.get, seeds.isEmpty, seeds.size
- [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L225) **`upgrade()`**: 개별 처리 / 조건 분기 / 참조 호출: level, super.upgrade
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L233) **`canUseSeed(Item item)`**: 조건 판정 / 참조 호출: seeds.contains, item.getClass, level
- [L240](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L240) **`resetForTrinity(int visibleLevel)`**: 생성·초기화 / 참조 호출: super.reset
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L249) **`storeInBundle(Bundle bundle)`**: 저장·복원 / 참조 호출: super.storeInBundle, bundle.put, seeds.toArray
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L256) **`restoreFromBundle(Bundle bundle)`**: 저장·복원 / 조건 분기·반복 / 참조 호출: super.restoreFromBundle, seeds.clear, bundle.contains, bundle.getClassArray, seeds.add, bundle.getClass, level
- [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L272) **`charge()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: target.buff, level, RingOfEnergy.artifactChargeMultiplier, Math.max, Math.min, updateQuickslot
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L289) **`ItemSelector()`**: 개별 처리 / 조건 분기 / 참조 호출: textPrompt, Messages.get, preferredBag, itemSelectable, canUseSeed, onSelect, level, seeds.add, item.getClass
- [L292](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L292) **`textPrompt()`**: 개별 처리 / 참조 호출: Messages.get
- [L297](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L297) **`preferredBag()`**: 개별 처리
- [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L302) **`itemSelectable(Item item)`**: 개별 처리 / 참조 호출: canUseSeed
- [L307](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L307) **`onSelect(Item item)`**: 이벤트·효과 실행 / 조건 분기 / 참조 호출: level, seeds.add, item.getClass, hero.sprite.operate, Sample.INSTANCE.play, hero.busy, hero.spend, seeds.size, seeds.clear
- [L333](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L333) **`Listener()`**: 개별 처리 / 조건 분기·반복 / 참조 호출: onSelect, Dungeon.level.distance, GLog.w, Messages.get, Ballistica, aim.subPath, CellEmitter.get, burst, Splash.at
- [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L336) **`onSelect(Integer cell)`**: 이벤트·효과 실행 / 조건 분기·반복 / 참조 호출: Dungeon.level.distance, GLog.w, Messages.get, Ballistica, aim.subPath, CellEmitter.get, burst, Splash.at, DungeonTilemap.tileCenterToWorld
- [L369](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java#L369) **`prompt()`**: 개별 처리 / 참조 호출: Messages.get

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":34,"fields":70,"methods":265}

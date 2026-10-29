# 상태 효과·환경 영역 효과·식물 처리 상세

**기준 코드:** `d6f487f29ae86d0da317e088e5ad81d52378bc5b`. 실제 파일을 열어 상태 필드·메서드·인접 호출을 확인했다. Buff(캐릭터 부착 상태), Blob(격자 공간 효과), Plant(환경 오브젝트)를 구분해야 한다. '효과 이름=무조건 같은 피해량'이라는 추정은 하지 않는다. 실제 효과는 지속시간, 면역, 대상, 난수 및 하위 재정의가 관여한다.

## [`actors/buffs/Burning.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java)

**타입:** `public class Burning extends Buff implements Hero.Doom, Buff.DOTbuff {` · 270줄.

**상태 필드:** [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L54) `private static final float DURATION = 8f;`; [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L56) `private float left;`; [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L61) `private static final String LEFT	= "left";`; [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L62) `private static final String ACTED	= "acted";`; [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L63) `private static final String BURN	= "burnIncrement";`; [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L64) `private static final String NEXT_DMG= "next_dmg";`.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L72) | `public void storeInBundle( Bundle bundle ) {` | 상태 저장·복원 / 주변 코드: `Buff.detach` |
| [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L81) | `public void restoreFromBundle( Bundle bundle ) {` | 상태 저장·복원 / 주변 코드: `Buff.detach`, `Random.NormalIntRange`, `Dungeon.scalingDepth` |
| [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L90) | `public boolean attachTo(Char target) {` | 상태 효과의 적용·제거·연장 / 주변 코드: `Buff.detach`, `Random.NormalIntRange`, `Dungeon.scalingDepth` |
| [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L97) | `public boolean act() {` | 주기적 상태 효과/트리거 처리 / 주변 코드: `Random.NormalIntRange`, `Dungeon.scalingDepth`, `Buff.detach`, `Random.Int` |
| [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L189) | `public void detach() {` | 상태 효과의 적용·제거·연장 / 주변 코드: `Glyph.genericProcChanceMultiplier`, `Math.round`, `Random.Float`, `Buff.affect`, `Math.min` |
| [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L194) | `public void reignite( Char ch ) {` | 원문 상세 확인 / 주변 코드: `Glyph.genericProcChanceMultiplier`, `Math.round`, `Random.Float`, `Buff.affect`, `Math.min` |
| [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L198) | `public void reignite( Char ch, float duration ) {` | 원문 상세 확인 / 주변 코드: `Glyph.genericProcChanceMultiplier`, `Math.round`, `Random.Float`, `Buff.affect`, `Math.min` |
| [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L221) | `public void extend( float duration ) {` | 원문 상세 확인 / 주변 코드: `Math.max`, `Integer.toString`, `Messages.get` |
| [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L227) | `public int icon() {` | 시각·문구 표현 / 주변 코드: `Math.max`, `Integer.toString`, `Messages.get`, `Badges.validateDeathFromFire`, `Dungeon.fail`, `GLog.n` |
| [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L232) | `public float iconFadePercent() {` | 시각·문구 표현 / 주변 코드: `Math.max`, `Integer.toString`, `Messages.get`, `Badges.validateDeathFromFire`, `Dungeon.fail`, `GLog.n` |
| [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L237) | `public String iconTextDisplay() {` | 조건·값 조회 / 주변 코드: `Integer.toString`, `Messages.get`, `Badges.validateDeathFromFire`, `Dungeon.fail`, `GLog.n`, `Random.NormalIntRange` |
| [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L242) | `public void fx(boolean on) {` | 시각·문구 표현 / 주변 코드: `Messages.get`, `Badges.validateDeathFromFire`, `Dungeon.fail`, `GLog.n`, `Random.NormalIntRange`, `Dungeon.scalingDepth` |
| [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L248) | `public String desc() {` | 시각·문구 표현 / 주변 코드: `Messages.get`, `Badges.validateDeathFromFire`, `Dungeon.fail`, `GLog.n`, `Random.NormalIntRange`, `Dungeon.scalingDepth` |
| [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L253) | `public void onDeath() {` | 원문 상세 확인 / 주변 코드: `Badges.validateDeathFromFire`, `Dungeon.fail`, `GLog.n`, `Messages.get`, `Random.NormalIntRange`, `Dungeon.scalingDepth` |
| [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java#L262) | `public int totalIncomingDMG() {` | 원문 상세 확인 / 주변 코드: `Random.NormalIntRange`, `Dungeon.scalingDepth`, `Math.round`, `Math.ceil` |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/buffs/Poison.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java)

**타입:** `public class Poison extends Buff implements Hero.Doom, Buff.DOTbuff {` · 146줄.

**상태 필드:** [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L38) `protected float left;`; [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L40) `private static final String LEFT	= "left";`.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L48) | `public void storeInBundle( Bundle bundle ) {` | 상태 저장·복원 / 주변 코드: `Math.max` |
| [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L55) | `public void restoreFromBundle( Bundle bundle ) {` | 상태 저장·복원 / 주변 코드: `Math.max`, `Integer.toString` |
| [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L60) | `public void set( float duration ) {` | 원문 상세 확인 / 주변 코드: `Math.max`, `Integer.toString`, `Messages.get` |
| [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L65) | `public void extend( float duration ) {` | 원문 상세 확인 / 주변 코드: `Integer.toString`, `Messages.get`, `CellEmitter.center` |
| [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L70) | `public void delay( float turns ){` | 원문 상세 확인 / 주변 코드: `Integer.toString`, `Messages.get`, `CellEmitter.center` |
| [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L75) | `public int icon() {` | 시각·문구 표현 / 주변 코드: `Integer.toString`, `Messages.get`, `CellEmitter.center` |
| [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L80) | `public void tintIcon(Image icon) {` | 원문 상세 확인 / 주변 코드: `Integer.toString`, `Messages.get`, `CellEmitter.center` |
| [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L84) | `public String iconTextDisplay(){` | 조건·값 조회 / 주변 코드: `Integer.toString`, `Messages.get`, `CellEmitter.center` |
| [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L89) | `public String desc() {` | 시각·문구 표현 / 주변 코드: `Messages.get`, `CellEmitter.center` |
| [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L94) | `public boolean attachTo(Char target) {` | 상태 효과의 적용·제거·연장 / 주변 코드: `CellEmitter.center` |
| [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L103) | `public void detach() {` | 상태 효과의 적용·제거·연장 / 주변 코드: `Math.ceil` |
| [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L109) | `public boolean act() {` | 주기적 상태 효과/트리거 처리 / 주변 코드: `Math.ceil`, `Badges.validateDeathFromPoison` |
| [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L130) | `public int totalIncomingDMG() {` | 원문 상세 확인 / 주변 코드: `Math.ceil`, `Badges.validateDeathFromPoison`, `Dungeon.fail`, `GLog.n`, `Messages.get` |
| [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java#L139) | `public void onDeath() {` | 원문 상세 확인 / 주변 코드: `Badges.validateDeathFromPoison`, `Dungeon.fail`, `GLog.n`, `Messages.get` |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/buffs/Corruption.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java)

**타입:** `public class Corruption extends AllyBuff implements Buff.DOTbuff {` · 106줄.

**상태 필드:** [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java#L37) `private float partialDamage = 0f;`; [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java#L92) `public static final String PARTIAL_DAMAGE = "partial_damage";`.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java#L40) | `public static void corruptionHeal(Char target){` | 원문 상세 확인 / 주변 코드: `Integer.toString` |
| [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java#L52) | `public boolean attachTo(Char target) {` | 상태 효과의 적용·제거·연장 |
| [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java#L61) | `public boolean act() {` | 주기적 상태 효과/트리거 처리 |
| [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java#L77) | `public void fx(boolean on) {` | 시각·문구 표현 |
| [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java#L83) | `public int icon() {` | 시각·문구 표현 |
| [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java#L88) | `public int totalIncomingDMG() {` | 원문 상세 확인 |
| [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java#L95) | `public void storeInBundle(Bundle bundle) {` | 상태 저장·복원 |
| [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java#L101) | `public void restoreFromBundle(Bundle bundle) {` | 상태 저장·복원 |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/buffs/Haste.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Haste.java)

**타입:** `public class Haste extends FlavourBuff {` · 51줄.

**상태 필드:** [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Haste.java#L33) `public static final float DURATION	= 20f;`.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Haste.java#L36) | `public int icon() {` | 시각·문구 표현 / 주변 코드: `Math.max` |
| [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Haste.java#L41) | `public void tintIcon(Image icon) {` | 원문 상세 확인 / 주변 코드: `Math.max` |
| [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Haste.java#L46) | `public float iconFadePercent() {` | 시각·문구 표현 / 주변 코드: `Math.max` |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/buffs/Paralysis.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java)

**타입:** `public class Paralysis extends FlavourBuff {`; `public static class ParalysisResist extends Buff {` · 122줄.

**상태 필드:** [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L34) `public static final float DURATION	= 10f;`; [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L95) `private int damage;`; [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L107) `private static final String DAMAGE = "damage";`.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L42) | `public boolean attachTo( Char target ) {` | 상태 효과의 적용·제거·연장 / 주변 코드: `Buff.affect`, `Random.NormalIntRange`, `Messages.get` |
| [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L51) | `public void processDamage( int damage ){` | 피해·발동 효과 / 주변 코드: `Buff.affect`, `Random.NormalIntRange`, `Messages.get`, `Math.max` |
| [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L67) | `public void detach() {` | 상태 효과의 적용·제거·연장 / 주변 코드: `Math.max` |
| [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L74) | `public int icon() {` | 시각·문구 표현 / 주변 코드: `Math.max`, `Math.ceil` |
| [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L79) | `public float iconFadePercent() {` | 시각·문구 표현 / 주변 코드: `Math.max`, `Math.ceil` |
| [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L84) | `public void fx(boolean on) {` | 시각·문구 표현 / 주변 코드: `Math.ceil` |
| [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L98) | `public boolean act() {` | 주기적 상태 효과/트리거 처리 / 주변 코드: `Math.ceil` |
| [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L110) | `public void storeInBundle(Bundle bundle) {` | 상태 저장·복원 |
| [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java#L116) | `public void restoreFromBundle(Bundle bundle) {` | 상태 저장·복원 |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/buffs/Roots.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java)

**타입:** `public class Roots extends FlavourBuff {` · 62줄.

**상태 필드:** [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java#L29) `public static final float DURATION = 5f;`.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java#L37) | `public boolean attachTo( Char target ) {` | 상태 효과의 적용·제거·연장 / 주변 코드: `Math.max` |
| [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java#L47) | `public void detach() {` | 상태 효과의 적용·제거·연장 / 주변 코드: `Math.max` |
| [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java#L53) | `public int icon() {` | 시각·문구 표현 / 주변 코드: `Math.max` |
| [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java#L58) | `public float iconFadePercent() {` | 시각·문구 표현 / 주변 코드: `Math.max` |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/buffs/Slow.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java)

**타입:** `public class Slow extends FlavourBuff {` · 52줄.

**상태 필드:** [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java#L34) `public static final float DURATION = 10f;`.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java#L37) | `public int icon() {` | 시각·문구 표현 / 주변 코드: `Math.max` |
| [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java#L42) | `public void tintIcon(Image icon) {` | 원문 상세 확인 / 주변 코드: `Math.max` |
| [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java#L47) | `public float iconFadePercent() {` | 시각·문구 표현 / 주변 코드: `Math.max` |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/buffs/Invisibility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invisibility.java)

**타입:** `public class Invisibility extends FlavourBuff {` · 122줄.

**상태 필드:** [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invisibility.java#L38) `public static final float DURATION	= 20f;`.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invisibility.java#L46) | `public boolean attachTo( Char target ) {` | 상태 효과의 적용·제거·연장 / 주변 코드: `Buff.affect`, `Math.max` |
| [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invisibility.java#L62) | `public void detach() {` | 상태 효과의 적용·제거·연장 / 주변 코드: `Math.max` |
| [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invisibility.java#L69) | `public int icon() {` | 시각·문구 표현 / 주변 코드: `Math.max` |
| [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invisibility.java#L74) | `public float iconFadePercent() {` | 시각·문구 표현 / 주변 코드: `Math.max` |
| [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invisibility.java#L79) | `public void fx(boolean on) {` | 시각·문구 표현 |
| [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invisibility.java#L84) | `public static void dispel() {` | 조건·값 조회 |
| [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invisibility.java#L90) | `public static void dispel(Char ch){` | 조건·값 조회 |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/buffs/Barrier.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java)

**타입:** `public class Barrier extends ShieldBuff {` · 113줄.

**상태 필드:** [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java#L99) `private static final String PARTIAL_LOST_SHIELD = "partial_lost_shield";`.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java#L40) | `public void incShield(int amt) {` | 원문 상세 확인 / 주변 코드: `Math.min`, `HoldFast.buffDecayFactor` |
| [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java#L46) | `public void setShield(int shield) {` | 원문 상세 확인 / 주변 코드: `Math.min`, `HoldFast.buffDecayFactor` |
| [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java#L52) | `public boolean act() {` | 주기적 상태 효과/트리거 처리 / 주변 코드: `Math.min`, `HoldFast.buffDecayFactor` |
| [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java#L71) | `public void fx(boolean on) {` | 시각·문구 표현 / 주변 코드: `Integer.toString`, `Messages.get` |
| [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java#L80) | `public int icon() {` | 시각·문구 표현 / 주변 코드: `Integer.toString`, `Messages.get` |
| [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java#L85) | `public void tintIcon(Image icon) {` | 원문 상세 확인 / 주변 코드: `Integer.toString`, `Messages.get` |
| [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java#L90) | `public String iconTextDisplay() {` | 조건·값 조회 / 주변 코드: `Integer.toString`, `Messages.get` |
| [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java#L95) | `public String desc() {` | 시각·문구 표현 / 주변 코드: `Messages.get` |
| [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java#L102) | `public void storeInBundle(Bundle bundle) {` | 상태 저장·복원 |
| [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java#L108) | `public void restoreFromBundle(Bundle bundle) {` | 상태 저장·복원 |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/buffs/Bless.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Bless.java)

**타입:** `public class Bless extends FlavourBuff {` · 46줄.

**상태 필드:** [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Bless.java#L28) `public static final float DURATION	= 30f;`.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Bless.java#L36) | `public int icon() {` | 시각·문구 표현 / 주변 코드: `Math.max` |
| [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Bless.java#L41) | `public float iconFadePercent() {` | 시각·문구 표현 / 주변 코드: `Math.max` |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/blobs/Fire.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java)

**타입:** `public class Fire extends Blob {` · 127줄.

**상태 필드:** 한 줄 필드 선언 발견되지 않음.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java#L39) | `protected void evolve() {` | 주기적 상태 효과/트리거 처리 / 주변 코드: `GameScene.updateMap` |
| [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java#L99) | `public static void burn( int pos ) {` | 원문 상세 확인 / 주변 코드: `Actor.findChar`, `Buff.affect`, `Messages.get` |
| [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java#L117) | `public void use( BlobEmitter emitter ) {` | 원문 상세 확인 / 주변 코드: `Messages.get` |
| [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java#L123) | `public String tileDesc() {` | 원문 상세 확인 / 주변 코드: `Messages.get` |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/blobs/ToxicGas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java)

**타입:** `public class ToxicGas extends Blob implements Hero.Doom {` · 79줄.

**상태 필드:** 한 줄 필드 선언 발견되지 않음.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java#L37) | `protected void evolve() {` | 주기적 상태 효과/트리거 처리 / 주변 코드: `Dungeon.scalingDepth`, `Actor.findChar`, `Speck.factory`, `Messages.get` |
| [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java#L59) | `public void use( BlobEmitter emitter ) {` | 원문 상세 확인 / 주변 코드: `Speck.factory`, `Messages.get`, `Badges.validateDeathFromGas`, `Dungeon.fail`, `GLog.n` |
| [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java#L66) | `public String tileDesc() {` | 원문 상세 확인 / 주변 코드: `Messages.get`, `Badges.validateDeathFromGas`, `Dungeon.fail`, `GLog.n` |
| [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java#L71) | `public void onDeath() {` | 원문 상세 확인 / 주변 코드: `Badges.validateDeathFromGas`, `Dungeon.fail`, `GLog.n`, `Messages.get` |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/blobs/Freezing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java)

**타입:** `public class Freezing extends Blob {` · 142줄.

**상태 필드:** 한 줄 필드 선언 발견되지 않음.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java#L40) | `protected void evolve() {` | 주기적 상태 효과/트리거 처리 / 주변 코드: `Freezing.freeze`, `Actor.findChar` |
| [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java#L68) | `public static void freeze( int cell ){` | 원문 상세 확인 / 주변 코드: `Actor.findChar`, `Buff.affect`, `Math.min` |
| [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java#L97) | `public void use( BlobEmitter emitter ) {` | 원문 상세 확인 / 주변 코드: `Messages.get`, `Actor.findChar`, `Buff.prolong` |
| [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java#L103) | `public String tileDesc() {` | 원문 상세 확인 / 주변 코드: `Messages.get`, `Actor.findChar`, `Buff.prolong` |
| [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Freezing.java#L108) | `public static boolean affect( int cell ) {` | 상태 효과의 적용·제거·연장 / 주변 코드: `Actor.findChar`, `Buff.prolong`, `CellEmitter.get` |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`actors/blobs/Electricity.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java)

**타입:** `public class Electricity extends Blob {` · 130줄.

**상태 필드:** [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java#L47) `private boolean[] water;`.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java#L50) | `protected void evolve() {` | 주기적 상태 효과/트리거 처리 / 주변 코드: `Actor.findChar`, `Buff.prolong`, `Math.round`, `Random.Float`, `Dungeon.scalingDepth`, `Dungeon.fail` |
| [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java#L105) | `private void spreadFromCell( int cell, int power ){` | 영역 생성·정리 / 주변 코드: `Math.max`, `Messages.get` |
| [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java#L119) | `public void use( BlobEmitter emitter ) {` | 원문 상세 확인 / 주변 코드: `Messages.get` |
| [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java#L125) | `public String tileDesc() {` | 원문 상세 확인 / 주변 코드: `Messages.get` |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`plants/Firebloom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Firebloom.java)

**타입:** `public class Firebloom extends Plant {`; `public static class Seed extends Plant.Seed {` · 72줄.

**상태 필드:** 한 줄 필드 선언 발견되지 않음.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Firebloom.java#L47) | `public void activate( Char ch ) {` | 주기적 상태 효과/트리거 처리 / 주변 코드: `Buff.affect`, `Buff.prolong`, `GameScene.add`, `Blob.seed`, `CellEmitter.get` |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.

## [`plants/Sungrass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java)

**타입:** `public class Sungrass extends Plant {`; `public static class Seed extends Plant.Seed {`; `public static class Health extends Buff {` · 172줄.

**상태 필드:** [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L74) `private static final float STEP = 1f;`; [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L76) `private int pos;`; [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L77) `private float partialHeal;`; [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L78) `private int level;`; [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L150) `private static final String POS	= "pos";`; [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L151) `private static final String PARTIAL = "partial_heal";`; [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L152) `private static final String LEVEL = "level";`.

| 함수 위치 | 함수 | 기능 해석·참조 |
|---|---|---|
| [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L47) | `public void activate( Char ch ) {` | 주기적 상태 효과/트리거 처리 / 주변 코드: `Buff.affect`, `CellEmitter.get` |
| [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L86) | `public boolean act() {` | 주기적 상태 효과/트리거 처리 / 주변 코드: `Integer.toString` |
| [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L123) | `public void boost( int amount ){` | 원문 상세 확인 / 주변 코드: `Math.max`, `Integer.toString`, `Messages.get` |
| [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L131) | `public int icon() {` | 시각·문구 표현 / 주변 코드: `Math.max`, `Integer.toString`, `Messages.get` |
| [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L136) | `public float iconFadePercent() {` | 시각·문구 표현 / 주변 코드: `Math.max`, `Integer.toString`, `Messages.get` |
| [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L141) | `public String iconTextDisplay() {` | 조건·값 조회 / 주변 코드: `Integer.toString`, `Messages.get` |
| [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L146) | `public String desc() {` | 시각·문구 표현 / 주변 코드: `Messages.get` |
| [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L155) | `public void storeInBundle( Bundle bundle ) {` | 상태 저장·복원 |
| [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java#L163) | `public void restoreFromBundle( Bundle bundle ) {` | 상태 저장·복원 |

**해석 주의:** 상태 지속시간은 `Actor` 스케줄과 `Buff` 자체 시간 모델을 함께 확인하고, 환경 효과는 `Blob.cur` 배열의 셀별 양과 `evolve()` 호출을 구분해야 한다. 실제 게임 내 효과는 개별 `Char`/면역·도전 설정의 영향을 받음.


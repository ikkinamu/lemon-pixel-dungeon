# 몬스터 개별 AI·행동·전투 구현 색인

**분석 소스:** `d6f487f29ae86d0da317e088e5ad81d52378bc5b` 기준 Java 본문. **함수 이름과 인접 소스에서 해석한 정적 설명**이며, 전투 시뮬레이션으로 모든 패턴을 검증한 자료는 아님. 각 라인을 클릭해 원본과 대조할 수 있다.

## [`actors/mobs/Albino.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Albino.java)

**타입:** `public class Albino extends Rat {`. **본문:** 53줄. **탐지 메서드:** 1개.

**상태 필드/상수:** 일치 선언 없음.

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Albino.java#L44) | `public int attackProc( Char enemy, int damage ) {` | 행동·공격 처리 / 인접 본문: 난수, 상태효과, 부모 메서드 / 호출 패턴: `Random.Int`, `Buff.affect`, `Random.NormalFloat` |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/Bat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Bat.java)

**타입:** `public class Bat extends Mob {`. **본문:** 97줄. **탐지 메서드:** 7개.

**상태 필드/상수:** 일치 선언 없음.

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Bat.java#L52) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Math.min`, `Integer.toString` |
| [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Bat.java#L57) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Math.min`, `Integer.toString` |
| [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Bat.java#L62) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Math.min`, `Integer.toString` |
| [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Bat.java#L67) | `public void die(Object cause) {` | 사망·제거·후처리 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Math.min`, `Integer.toString` |
| [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Bat.java#L73) | `public int attackProc( Char enemy, int damage ) {` | 행동·공격 처리 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Math.min`, `Integer.toString` |
| [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Bat.java#L86) | `public float lootChance(){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드 |
| [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Bat.java#L91) | `public Item createLoot(){` | 생성·드롭 처리 / 인접 본문: 던전 상태, 부모 메서드 |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)

**타입:** `public class Brute extends Mob {`, `public static class BruteRage extends ShieldBuff {`. **본문:** 171줄. **탐지 메서드:** 12개.

**상태 필드/상수:** [protected boolean hasRaged = false;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L55); [private BruteRage rage;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L84); [private static final String HAS_RAGED = "has_raged";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L114).

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L58) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L65) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L70) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 부모 메서드, 반복 / 호출 패턴: `Random.NormalIntRange` |
| [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L75) | `public void die(Object cause) {` | 사망·제거·후처리 / 인접 본문: 상태효과, 부모 메서드, 반복 / 호출 패턴: `Buff.affect` |
| [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L87) | `public boolean isAlive() {` | 조건/값 조회 / 인접 본문: 던전 상태, 상태효과, 부모 메서드, 반복 / 호출 패턴: `Buff.affect`, `Integer.toString`, `SpellSprite.show` |
| [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L103) | `protected void triggerEnrage(){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 상태효과, 부모 메서드 / 호출 패턴: `Buff.affect`, `Integer.toString`, `SpellSprite.show` |
| [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L117) | `public void storeInBundle(Bundle bundle) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드 / 호출 패턴: `Math.round`, `AscensionChallenge.statModifier` |
| [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L123) | `public void restoreFromBundle(Bundle bundle) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드 / 호출 패턴: `Math.round`, `AscensionChallenge.statModifier` |
| [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L135) | `public boolean act() {` | 행동·공격 처리 / 인접 본문: 부모 메서드 / 호출 패턴: `Math.round`, `AscensionChallenge.statModifier` |
| [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L154) | `public void detach() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 부모 메서드 / 호출 패턴: `Messages.get` |
| [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L160) | `public int icon () {` | 표현 및 텍스트 / 호출 패턴: `Messages.get` |
| [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java#L165) | `public String desc () {` | 표현 및 텍스트 / 호출 패턴: `Messages.get` |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/Crab.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Crab.java)

**타입:** `public class Crab extends Mob {`. **본문:** 60줄. **탐지 메서드:** 3개.

**상태 필드/상수:** 일치 선언 없음.

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Crab.java#L46) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Crab.java#L51) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Crab.java#L56) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/DM100.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM100.java)

**타입:** `public class DM100 extends Mob {`, `public static class LightningBolt{}`. **본문:** 131줄. **탐지 메서드:** 5개.

**상태 필드/상수:** [private static final float TIME_TO_ZAP	= 1f;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM100.java#L42).

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM100.java#L61) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM100.java#L66) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM100.java#L71) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Invisibility.dispel`, `Math.round`, `AscensionChallenge.statModifier` |
| [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM100.java#L76) | `protected boolean canAttack( Char enemy ) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Invisibility.dispel`, `Random.NormalIntRange`, `Math.round`, `AscensionChallenge.statModifier` |
| [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM100.java#L85) | `protected boolean doAttack( Char enemy ) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Invisibility.dispel`, `Random.NormalIntRange`, `Math.round`, `AscensionChallenge.statModifier`, `PixelScene.shake`, `Badges.validateDeathFromEnemyMagic` |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/DM200.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java)

**타입:** `public class DM200 extends Mob {`, `private class Hunting extends Mob.Hunting{`. **본문:** 189줄. **탐지 메서드:** 12개.

**상태 필드/상수:** [private int ventCooldown = 0;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L90); [private static final String VENT_COOLDOWN = "vent_cooldown";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L92).

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L59) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Math.pow`, `Generator.randomWeapon`, `Generator.randomArmor` |
| [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L64) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Math.pow`, `Generator.randomWeapon`, `Generator.randomArmor` |
| [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L69) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Math.pow`, `Generator.randomWeapon`, `Generator.randomArmor` |
| [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L74) | `public float lootChance(){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Math.pow`, `Generator.randomWeapon`, `Generator.randomArmor` |
| [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L80) | `public Item createLoot() {` | 생성·드롭 처리 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Generator.randomWeapon`, `Generator.randomArmor` |
| [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L95) | `public void storeInBundle(Bundle bundle) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드, 반복, UI 갱신 / 호출 패턴: `GameScene.add`, `Blob.seed` |
| [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L101) | `public void restoreFromBundle(Bundle bundle) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드, 반복, UI 갱신 / 호출 패턴: `GameScene.add`, `Blob.seed` |
| [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L107) | `protected boolean act() {` | 행동·공격 처리 / 인접 본문: 던전 상태, 부모 메서드, 반복, UI 갱신 / 호출 패턴: `GameScene.add`, `Blob.seed`, `PathFinder.buildDistanceMap`, `BArray.not` |
| [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L112) | `public void onZapComplete(){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 반복, UI 갱신 / 호출 패턴: `GameScene.add`, `Blob.seed`, `PathFinder.buildDistanceMap`, `BArray.not` |
| [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L117) | `private void zap( ){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드, 반복, UI 갱신 / 호출 패턴: `GameScene.add`, `Blob.seed`, `PathFinder.buildDistanceMap`, `BArray.not` |
| [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L130) | `protected boolean canVent(int target){` | 조건/값 조회 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `PathFinder.buildDistanceMap`, `BArray.not`, `Random.Int` |
| [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DM200.java#L143) | `public boolean act(boolean enemyInFOV, boolean justAlerted) {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.Int` |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/Gnoll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Gnoll.java)

**타입:** `public class Gnoll extends Mob {`. **본문:** 59줄. **탐지 메서드:** 3개.

**상태 필드/상수:** 일치 선언 없음.

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Gnoll.java#L45) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Gnoll.java#L50) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Gnoll.java#L55) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/GnollTrickster.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java)

**타입:** `public class GnollTrickster extends Gnoll {`, `protected class Wandering extends Mob.Wandering{`. **본문:** 177줄. **탐지 메서드:** 10개.

**상태 필드/상수:** [private int combo = 0;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L63); [private static final String COMBO = "combo";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L162).

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L66) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드, UI 갱신 / 호출 패턴: `Random.Int`, `GameScene.add`, `Blob.seed` |
| [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L71) | `protected boolean canAttack( Char enemy ) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 상태효과, 부모 메서드, UI 갱신 / 호출 패턴: `Random.Int`, `GameScene.add`, `Blob.seed`, `Buff.affect` |
| [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L77) | `public int attackProc( Char enemy, int damage ) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 상태효과, 부모 메서드, UI 갱신 / 호출 패턴: `Random.Int`, `GameScene.add`, `Blob.seed`, `Buff.affect` |
| [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L107) | `protected boolean getCloser( int target ) {` | 조건/값 조회 / 인접 본문: 던전 상태, 부모 메서드 |
| [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L117) | `public void aggro(Char ch) {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Quest.process` |
| [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L127) | `public Item createLoot() {` | 생성·드롭 처리 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Quest.process`, `PathFinder.buildDistanceMap` |
| [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L141) | `public void die( Object cause ) {` | 사망·제거·후처리 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Quest.process`, `PathFinder.buildDistanceMap` |
| [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L149) | `protected int randomDestination() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `PathFinder.buildDistanceMap` |
| [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L165) | `public void storeInBundle( Bundle bundle ) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드 |
| [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java#L171) | `public void restoreFromBundle( Bundle bundle ) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드 |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/Goo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java)

**타입:** `public class Goo extends Mob {`. **본문:** 351줄. **탐지 메서드:** 17개.

**상태 필드/상수:** [private int pumpedUp = 0;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L64); [private int healInc = 1;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L65); [private final String PUMPEDUP = "pumpedup";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L326); [private final String HEALINC = "healinc";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L327).

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L68) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L84) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L92) | `public int defenseSkill(Char enemy) {` | 전투 수치 계산 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Dungeon.isChallenged`, `Integer.toString` |
| [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L97) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Dungeon.isChallenged`, `Integer.toString`, `BossHealthBar.bleed` |
| [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L102) | `public boolean act() {` | 행동·공격 처리 / 인접 본문: 던전 상태 / 호출 패턴: `Dungeon.isChallenged`, `Integer.toString`, `BossHealthBar.bleed`, `Math.min` |
| [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L142) | `protected boolean canAttack( Char enemy ) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 상태효과, 부모 메서드 / 호출 패턴: `Random.Int`, `Buff.affect`, `PixelScene.shake` |
| [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L155) | `public int attackProc( Char enemy, int damage ) {` | 행동·공격 처리 / 인접 본문: 난수, 상태효과, 부모 메서드 / 호출 패턴: `Random.Int`, `Buff.affect`, `PixelScene.shake` |
| [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L170) | `public void updateSpriteState() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.Int` |
| [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L179) | `protected boolean doAttack( Char enemy ) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태 / 호출 패턴: `Random.Int`, `Invisibility.dispel` |
| [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L231) | `public boolean attack( Char enemy, float dmgMulti, float dmgBonus, float accMulti ) {` | 행동·공격 처리 / 인접 본문: 던전 상태, 부모 메서드 |
| [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L244) | `protected boolean getCloser( int target ) {` | 조건/값 조회 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `BossHealthBar.isAssigned`, `BossHealthBar.assignBoss`, `BossHealthBar.bleed`, `Messages.get` |
| [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L253) | `protected boolean getFurther(int target) {` | 조건/값 조회 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `BossHealthBar.isAssigned`, `BossHealthBar.assignBoss`, `BossHealthBar.bleed`, `Messages.get`, `Dungeon.isChallenged` |
| [L262](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L262) | `public void damage(int dmg, Object src) {` | 행동·공격 처리 / 인접 본문: 던전 상태, 부모 메서드, UI 갱신 / 호출 패턴: `BossHealthBar.isAssigned`, `BossHealthBar.assignBoss`, `BossHealthBar.bleed`, `Messages.get`, `Dungeon.isChallenged`, `GameScene.bossSlain` |
| [L283](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L283) | `public void die( Object cause ) {` | 사망·제거·후처리 / 인접 본문: 난수, 던전 상태, 부모 메서드, 반복, UI 갱신 / 호출 패턴: `GameScene.bossSlain`, `Random.chances`, `Random.Int`, `Badges.validateBossSlain`, `Badges.validateBossChallengeCompleted`, `Messages.get` |
| [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L312) | `public void notice() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드, 반복 / 호출 패턴: `BossHealthBar.isAssigned`, `BossHealthBar.assignBoss`, `Messages.get`, `Actor.chars` |
| [L330](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L330) | `public void storeInBundle( Bundle bundle ) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드 / 호출 패턴: `BossHealthBar.assignBoss`, `BossHealthBar.bleed` |
| [L339](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Goo.java#L339) | `public void restoreFromBundle( Bundle bundle ) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드 / 호출 패턴: `BossHealthBar.assignBoss`, `BossHealthBar.bleed` |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/Guard.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java)

**타입:** `public class Guard extends Mob {`, `private class Hunting extends Mob.Hunting{`. **본문:** 193줄. **탐지 메서드:** 12개.

**상태 필드/상수:** [private boolean chainsUsed = false;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L46); [private final String CHAINSUSED = "chainsused";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L160).

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L66) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 반복 / 호출 패턴: `Random.NormalIntRange`, `Actor.findChar`, `Char.hasProp` |
| [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L70) | `private boolean chain(int target){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 반복 / 호출 패턴: `Actor.findChar`, `Char.hasProp`, `Messages.get` |
| [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L105) | `public void call() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, UI 갱신 / 호출 패턴: `Actor.add`, `Cripple.prolong`, `Dungeon.observe`, `GameScene.updateFog` |
| [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L107) | `public void call() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, UI 갱신 / 호출 패턴: `Cripple.prolong`, `Dungeon.observe`, `GameScene.updateFog` |
| [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L123) | `private void pullEnemy( Char enemy, int pullPos ){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 난수, 던전 상태, 부모 메서드, UI 갱신 / 호출 패턴: `Cripple.prolong`, `Dungeon.observe`, `GameScene.updateFog`, `Random.NormalIntRange`, `Math.pow` |
| [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L138) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Math.pow` |
| [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L143) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Math.pow` |
| [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L148) | `public float lootChance() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Math.pow` |
| [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L155) | `public Item createLoot() {` | 생성·드롭 처리 / 인접 본문: 던전 상태, 부모 메서드 |
| [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L163) | `public void storeInBundle(Bundle bundle) {` | 직렬화 및 복원 / 인접 본문: 던전 상태, 부모 메서드 |
| [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L169) | `public void restoreFromBundle(Bundle bundle) {` | 직렬화 및 복원 / 인접 본문: 던전 상태, 부모 메서드 |
| [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java#L176) | `public boolean act( boolean enemyInFOV, boolean justAlerted ) {` | 행동·공격 처리 / 인접 본문: 던전 상태, 부모 메서드 |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/Mimic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java)

**타입:** `public class Mimic extends Mob {`. **본문:** 362줄. **탐지 메서드:** 28개.

**상태 필드/상수:** [private int level;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L53); [public ArrayList<Item> items;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L67); [private boolean stealthy = false;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L69); [private static final String LEVEL	= "level";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L71); [private static final String ITEMS	= "items";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L72); [private static final String STEALTHY= "stealthy";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L73).

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L76) | `public void storeInBundle( Bundle bundle ) {` | 직렬화 및 복원 / 인접 본문: 상태효과, 부모 메서드 |
| [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L85) | `public void restoreFromBundle( Bundle bundle ) {` | 직렬화 및 복원 / 인접 본문: 상태효과, 부모 메서드 / 호출 패턴: `Messages.get` |
| [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L99) | `public boolean add(Buff buff) {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 상태효과, 부모 메서드 / 호출 패턴: `Messages.get`, `MimicTooth.stealthyMimics` |
| [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L112) | `public String name() {` | 표현 및 텍스트 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Messages.get`, `MimicTooth.stealthyMimics`, `GLog.w`, `CellEmitter.get`, `Speck.factory`, `INSTANCE.play` |
| [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L121) | `public String description() {` | 표현 및 텍스트 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `MimicTooth.stealthyMimics`, `Messages.get`, `GLog.w`, `CellEmitter.get`, `Speck.factory`, `INSTANCE.play` |
| [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L134) | `protected boolean act() {` | 행동·공격 처리 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `GLog.w`, `Messages.get`, `CellEmitter.get`, `Speck.factory`, `INSTANCE.play` |
| [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L148) | `public CharSprite sprite() {` | 표현 및 텍스트 / 인접 본문: 던전 상태, 부모 메서드 |
| [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L155) | `public boolean interact(Char c) {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드 |
| [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L176) | `public void onAttackComplete() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드 |
| [L186](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L186) | `public int defenseProc(Char enemy, int damage) {` | 전투 수치 계산 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Actor.chars` |
| [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L195) | `public void damage(int dmg, Object src) {` | 행동·공격 처리 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Actor.chars`, `GLog.w`, `Messages.get`, `CellEmitter.get`, `Speck.factory`, `INSTANCE.play` |
| [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L204) | `public void die(Object cause) {` | 사망·제거·후처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Actor.chars`, `GLog.w`, `Messages.get`, `CellEmitter.get`, `Speck.factory`, `INSTANCE.play` |
| [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L212) | `public void stopHiding(){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Actor.chars`, `GLog.w`, `Messages.get`, `CellEmitter.get`, `Speck.factory`, `INSTANCE.play` |
| [L225](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L225) | `public boolean stealthy(){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L230) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L239) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L244](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L244) | `public void beckon( int cell ) {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 부모 메서드 |
| [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L251) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 던전 상태, 부모 메서드, 반복 |
| [L259](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L259) | `public void setLevel( int level ){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드, 반복 |
| [L264](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L264) | `public void adjustStats( int level ) {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드, 반복 |
| [L272](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L272) | `public void rollToDropLoot(){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드, 반복 |
| [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L284) | `public float spawningWeight() {` | 생성·드롭 처리 |
| [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L289) | `public boolean reset() {` | 구현 상세는 연결된 메서드 본문 참조 / 호출 패턴: `Arrays.asList` |
| [L294](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L294) | `public static Mimic spawnAt( int pos, Item... items){` | 생성·드롭 처리 / 인접 본문: 던전 상태 / 호출 패턴: `Arrays.asList`, `Dungeon.scalingDepth` |
| [L298](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L298) | `public static Mimic spawnAt( int pos, Class mimicType, Item... items){` | 생성·드롭 처리 / 인접 본문: 던전 상태 / 호출 패턴: `Arrays.asList`, `Dungeon.scalingDepth`, `MimicTooth.stealthyMimics` |
| [L302](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L302) | `public static Mimic spawnAt( int pos, boolean useDecks, Item... items){` | 생성·드롭 처리 / 인접 본문: 던전 상태 / 호출 패턴: `Arrays.asList`, `Dungeon.scalingDepth`, `MimicTooth.stealthyMimics` |
| [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L306) | `public static Mimic spawnAt( int pos, Class mimicType, boolean useDecks, Item... items){` | 생성·드롭 처리 / 인접 본문: 난수, 던전 상태, 조건 분기 / 호출 패턴: `Arrays.asList`, `Dungeon.scalingDepth`, `MimicTooth.stealthyMimics`, `Random.Int` |
| [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java#L332) | `protected void generatePrize( boolean useDecks ){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 난수, 조건 분기, 반복 / 호출 패턴: `Random.Int`, `Generator.randomMissile`, `Generator.randomArmor`, `Generator.randomWeapon`, `Generator.random`, `Generator.randomUsingDefaults` |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/Monk.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java)

**타입:** `public class Monk extends Mob {`, `public static class Focus extends Buff {`. **본문:** 161줄. **탐지 메서드:** 14개.

**상태 필드/상수:** [protected float focusCooldown = 0;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L81); [private static String FOCUS_COOLDOWN = "focus_cooldown";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L129).

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L55) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Quest.oldProcess` |
| [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L60) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 난수, 상태효과, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Quest.oldProcess`, `Buff.affect` |
| [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L65) | `public float attackDelay() {` | 행동·공격 처리 / 인접 본문: 난수, 상태효과, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Quest.oldProcess`, `Buff.affect` |
| [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L70) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 상태효과, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Quest.oldProcess`, `Buff.affect` |
| [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L75) | `public void rollToDropLoot() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 상태효과, 부모 메서드 / 호출 패턴: `Quest.oldProcess`, `Buff.affect` |
| [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L84) | `protected boolean act() {` | 행동·공격 처리 / 인접 본문: 상태효과, 부모 메서드 / 호출 패턴: `Buff.affect` |
| [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L93) | `protected void spend( float time ) {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `INSTANCE.play`, `Random.Float` |
| [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L99) | `public void move( int step, boolean travelling) {` | 추적·이동·대상 선택 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `INSTANCE.play`, `Random.Float`, `Random.NormalFloat`, `Messages.get` |
| [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L107) | `public int defenseSkill( Char enemy ) {` | 전투 수치 계산 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `INSTANCE.play`, `Random.Float`, `Random.NormalFloat`, `Messages.get` |
| [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L115) | `public String defenseVerb() {` | 전투 수치 계산 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `INSTANCE.play`, `Random.Float`, `Random.NormalFloat`, `Messages.get` |
| [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L132) | `public void storeInBundle( Bundle bundle ) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드 |
| [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L138) | `public void restoreFromBundle( Bundle bundle ) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드 |
| [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L151) | `public int icon() {` | 표현 및 텍스트 |
| [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java#L156) | `public void tintIcon(Image icon) {` | 구현 상세는 연결된 메서드 본문 참조 |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/Necromancer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java)

**타입:** `public class Necromancer extends Mob {`, `public static class SummoningBlockDamage{}`, `private class Hunting extends Mob.Hunting{`, `public static class NecroSkeleton extends Skeleton {`, `public static class NecroSkeletonSprite extends SkeletonSprite{`. **본문:** 444줄. **탐지 메서드:** 15개.

**상태 필드/상수:** [public boolean summoning = false;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L69); [public int summoningPos = -1;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L70); [protected boolean firstSummon = true;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L72); [private NecroSkeleton mySkeleton;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L74); [private int storedSkeletonID = -1;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L75); [private static final String SUMMONING = "summoning";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L134); [private static final String FIRST_SUMMON = "first_summon";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L135); [private static final String SUMMONING_POS = "summoning_pos";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L136); [private static final String MY_SKELETON = "my_skeleton";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L137).

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L78) | `protected boolean act() {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L87) | `public void aggro(Char ch) {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Actor.findById` |
| [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L97) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Actor.findById` |
| [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L102) | `public float lootChance() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Actor.findById` |
| [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L107) | `public Item createLoot(){` | 생성·드롭 처리 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Actor.findById` |
| [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L113) | `public void die(Object cause) {` | 사망·제거·후처리 / 인접 본문: 부모 메서드 / 호출 패턴: `Actor.findById` |
| [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L130) | `protected boolean canAttack(Char enemy) {` | 행동·공격 처리 / 인접 본문: 부모 메서드 |
| [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L140) | `public void storeInBundle(Bundle bundle) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드 |
| [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L155) | `public void restoreFromBundle(Bundle bundle) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드 / 호출 패턴: `Beam.HealthRay`, `INSTANCE.play`, `Math.min`, `Integer.toString` |
| [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L167) | `public void onZapComplete(){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 상태효과 / 호출 패턴: `Beam.HealthRay`, `INSTANCE.play`, `Math.min`, `Integer.toString`, `Buff.affect` |
| [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L199) | `public void summonMinion(){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 반복 / 호출 패턴: `Actor.findChar`, `Char.hasProp`, `Actor.add` |
| [L269](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L269) | `public boolean act(boolean enemyInFOV, boolean justAlerted) {` | 행동·공격 처리 / 인접 본문: 던전 상태 / 호출 패턴: `Actor.findById` |
| [L424](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L424) | `public float spawningWeight() {` | 생성·드롭 처리 / 인접 본문: 부모 메서드 |
| [L430](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L430) | `public NecroSkeletonSprite(){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 부모 메서드 |
| [L436](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java#L436) | `public void resetColor() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 부모 메서드 |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/Piranha.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java)

**타입:** `public class Piranha extends Mob {`, `private class Sleeping extends Mob.Sleeping{`, `private class Wandering extends Mob.Wandering{`, `private class Hunting extends Mob.Hunting{`. **본문:** 215줄. **탐지 메서드:** 16개.

**상태 필드/상수:** 일치 선언 없음.

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L62) | `public Piranha() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Speck.factory`, `Random.NormalIntRange` |
| [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L70) | `protected boolean act() {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Speck.factory`, `Random.NormalIntRange` |
| [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L84) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L89) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L94) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange`, `Badges.validatePiranhasKilled` |
| [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L99) | `public boolean surprisedBy(Char enemy, boolean attacking) {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Badges.validatePiranhasKilled` |
| [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L110) | `public void dieOnLand(){` | 사망·제거·후처리 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Badges.validatePiranhasKilled`, `Dungeon.findStep`, `BArray.and` |
| [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L115) | `public void die( Object cause ) {` | 사망·제거·후처리 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `Badges.validatePiranhasKilled`, `Dungeon.findStep`, `BArray.and` |
| [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L123) | `public float spawningWeight() {` | 생성·드롭 처리 / 인접 본문: 던전 상태 / 호출 패턴: `Dungeon.findStep`, `BArray.and`, `Dungeon.flee` |
| [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L128) | `public boolean reset() {` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 던전 상태 / 호출 패턴: `Dungeon.findStep`, `BArray.and`, `Dungeon.flee` |
| [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L133) | `protected boolean getCloser( int target ) {` | 조건/값 조회 / 인접 본문: 던전 상태, 반복 / 호출 패턴: `Dungeon.findStep`, `BArray.and`, `Dungeon.flee` |
| [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L149) | `protected boolean getFurther( int target ) {` | 조건/값 조회 / 인접 본문: 던전 상태, 부모 메서드, 반복 / 호출 패턴: `Dungeon.flee`, `BArray.and`, `PathFinder.buildDistanceMap` |
| [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L171) | `public boolean act(boolean enemyInFOV, boolean justAlerted) {` | 행동·공격 처리 / 인접 본문: 던전 상태, 부모 메서드 / 호출 패턴: `PathFinder.buildDistanceMap` |
| [L183](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L183) | `public boolean act(boolean enemyInFOV, boolean justAlerted) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `PathFinder.buildDistanceMap`, `RatSkull.exoticChanceMultiplier`, `Random.Float` |
| [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L196) | `public boolean act(boolean enemyInFOV, boolean justAlerted) {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `PathFinder.buildDistanceMap`, `RatSkull.exoticChanceMultiplier`, `Random.Float` |
| [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java#L206) | `public static Piranha random(){` | 구현 상세는 연결된 메서드 본문 참조 / 인접 본문: 난수 / 호출 패턴: `RatSkull.exoticChanceMultiplier`, `Random.Float` |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/Rat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java)

**타입:** `public class Rat extends Mob {`. **본문:** 83줄. **탐지 메서드:** 6개.

**상태 필드/상수:** [private static final String RAT_ALLY = "rat_ally";](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L69).

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L43) | `protected boolean act() {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L55) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L60) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L65) | `public int drRoll() {` | 전투 수치 계산 / 인접 본문: 난수, 부모 메서드 / 호출 패턴: `Random.NormalIntRange` |
| [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L72) | `public void storeInBundle(Bundle bundle) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드 |
| [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Rat.java#L78) | `public void restoreFromBundle(Bundle bundle) {` | 직렬화 및 복원 / 인접 본문: 부모 메서드 |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.

## [`actors/mobs/Snake.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java)

**타입:** `public class Snake extends Mob {`. **본문:** 73줄. **탐지 메서드:** 3개.

**상태 필드/상수:** [private static int dodges = 0;](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java#L58).

| 위치 | 메서드 | 역할·분기/연동 근거 |
|---|---|---|
| [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java#L49) | `public int damageRoll() {` | 행동·공격 처리 / 인접 본문: 난수, 던전 상태, 부모 메서드, UI 갱신 / 호출 패턴: `Random.NormalIntRange`, `ADVENTURERS_GUIDE.isPageRead`, `Badges.isUnlocked`, `GameScene.flashForDocument` |
| [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java#L54) | `public int attackSkill( Char target ) {` | 행동·공격 처리 / 인접 본문: 던전 상태, 부모 메서드, UI 갱신 / 호출 패턴: `ADVENTURERS_GUIDE.isPageRead`, `Badges.isUnlocked`, `GameScene.flashForDocument` |
| [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/d6f487f29ae86d0da317e088e5ad81d52378bc5b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java#L61) | `public String defenseVerb() {` | 전투 수치 계산 / 인접 본문: 던전 상태, 부모 메서드, UI 갱신 / 호출 패턴: `ADVENTURERS_GUIDE.isPageRead`, `Badges.isUnlocked`, `GameScene.flashForDocument` |

**해석 주의:** `Mob`에 공통으로 정의된 상태기계가 하위 클래스에서 재정의될 수 있고, 상단 30줄의 호출 패턴은 인접 영역의 정적 힌트다. 실제 공격 순서·명중·버프 중첩은 `Mob`, `Char`, `Buff` 및 하위 AI를 함께 확인해야 한다.


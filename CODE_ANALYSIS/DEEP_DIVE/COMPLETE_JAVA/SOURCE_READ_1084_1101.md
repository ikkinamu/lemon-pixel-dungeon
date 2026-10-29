# Java 소스 구현 분석 1084–1101

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1084. [`Statistics.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon`, 277행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L30) `public class Statistics {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L32) `public static int goldCollected;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L33) `public static int deepestFloor;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L34) `public static int highestAscent;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L35) `public static int enemiesSlain;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L36) `public static int foodEaten;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L37) `public static int itemsCrafted;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L38) `public static int piranhasKilled;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L39) `public static int hazardAssistedKills;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L40) `public static int ankhsUsed;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L46) `public static int progressScore;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L47) `public static int heldItemValue;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L48) `public static int treasureScore;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L50) `public static int exploreScore;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L51) `public static int[] bossScores = new int[5];`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L52) `public static int totalBossScore;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L53) `public static int[] questScores = new int[5];`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L54) `public static int totalQuestScore;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L55) `public static float winMultiplier;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L56) `public static float chalMultiplier;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L57) `public static int totalScore;`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L60) `public static int upgradesUsed;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L61) `public static int sneakAttacks;`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L62) `public static int thrownAttacks;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L64) `public static int spawnersAlive;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L66) `public static float duration;`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L68) `public static boolean qualifiedForNoKilling = false;`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L69) `public static boolean completedWithNoKilling = false;`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L70) `public static boolean qualifiedForBossRemainsBadge = false;`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L71) `public static boolean qualifiedForBossChallengeBadge = false;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L72) `public static boolean qualifiedForRandomVictoryBadge = false;`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L74) `public static boolean vaultInjureWarned = false;`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L76) `public static boolean amuletObtained = false;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L77) `public static boolean gameWon = false;`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L78) `public static boolean ascended = false;`
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L127) `private static final String GOLD		= "score";`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L128) `private static final String DEEPEST		= "maxDepth";`
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L129) `private static final String HIGHEST		= "maxAscent";`
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L130) `private static final String SLAIN		= "enemiesSlain";`
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L131) `private static final String FOOD		= "foodEaten";`
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L132) `private static final String ALCHEMY		= "potionsCooked";`
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L133) `private static final String PIRANHAS	= "priranhas";`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L134) `private static final String HAZARD_ASSISTS	= "hazard_assists";`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L135) `private static final String ANKHS		= "ankhsUsed";`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L137) `private static final String PROG_SCORE	    = "prog_score";`
- [L138](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L138) `private static final String ITEM_VAL	    = "item_val";`
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L139) `private static final String TRES_SCORE      = "tres_score";`
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L140) `private static final String FLR_EXPL        = "flr_expl_";`
- [L141](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L141) `private static final String EXPL_SCORE      = "expl_score";`
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L142) `private static final String BOSS_SCORES		= "boss_scores";`
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L143) `private static final String TOT_BOSS		= "tot_boss";`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L144) `private static final String QUEST_SCORES	= "quest_scores";`
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L145) `private static final String TOT_QUEST		= "tot_quest";`
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L146) `private static final String WIN_MULT		= "win_mult";`
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L147) `private static final String CHAL_MULT		= "chal_mult";`
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L148) `private static final String TOTAL_SCORE		= "total_score";`
- [L150](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L150) `private static final String UPGRADES	= "upgradesUsed";`
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L151) `private static final String SNEAKS		= "sneakAttacks";`
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L152) `private static final String THROWN		= "thrownAssists";`
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L154) `private static final String ITEM_TYPES_DISCOVERED    = "item_types_discovered";`
- [L156](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L156) `private static final String SPAWNERS	= "spawnersAlive";`
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L158) `private static final String DURATION	= "duration";`
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L160) `private static final String NO_KILLING_QUALIFIED	= "qualifiedForNoKilling";`
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L161) `private static final String BOSS_REMAINS_QUALIFIED	= "qualifiedForBossRemainsBadge";`
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L162) `private static final String BOSS_CHALLENGE_QUALIFIED= "qualifiedForBossChallengeBadge";`
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L163) `private static final String RANDOM_VICTORY_QUALIFIED= "qualifiedForRandomVictory";`
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L165) `private static final String AMULET          = "amuletObtained";`
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L166) `private static final String WON		        = "won";`
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L167) `private static final String ASCENDED		= "ascended";`

### 메서드 및 코드 의존 단서
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L80) `public static void reset() {` — 개별 처리
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L169) `public static void storeInBundle( Bundle bundle ) {` — 저장·복원
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L216) `public static void restoreFromBundle( Bundle bundle ) {` — 저장·복원, 인접 호출: Arrays.asList
- [L271](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L271) `public static void preview( GamesInProgress.Info info, Bundle bundle ){` — 개별 처리

## 1085. [`Carpet.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.tiles.custom`, 144행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L35) `public class Carpet extends CustomTilemap {`

### 변수·상수 후보
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L43) `public static final int SKIP = -1;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L45) `public static final int CITY_STATUE = 80;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L46) `public static final int CITY_PEDESTAL = 81;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L47) `public static final int CITY_ENTRANCE = 82;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L48) `public static final int CITY_STATUE_TR = 83;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L49) `public static final int CITY_STATUE_BR = 84;`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L50) `public static final int CITY_STATUE_TL = 85;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L51) `public static final int CITY_STATUE_BL = 86;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L52) `public static final int CITY_PEDESTAL_TR = 87;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L53) `public static final int CITY_PEDESTAL_TL = 88;`
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L118) `public static final String OVERRIDES_KEYS = "overrides_keys";`
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L119) `public static final String OVERRIDES_VALUES = "overrides_values";`

### 메서드 및 코드 의존 단서
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L56) `public void overrideTile(int x, int y, int override){` — 개별 처리
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L61) `public void overrideTile(Level level, int x, int y, int override){` — 개별 처리
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L68) `public void overrideTile(int tile, Level level, int override){` — 개별 처리, 인접 호출: Messages.get
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L75) `public Tilemap create() {` — 생성·초기화, 인접 호출: Messages.get
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L101) `public String name(int tileX, int tileY) {` — 개별 처리, 인접 호출: Messages.get
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L110) `public String desc(int tileX, int tileY) {` — 개별 처리, 인접 호출: Messages.get
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L122) `public void storeInBundle(Bundle bundle) {` — 저장·복원
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/custom/Carpet.java#L134) `public void restoreFromBundle(Bundle bundle) {` — 저장·복원

## 1086. [`CustomTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.tiles`, 175행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L33) `public abstract class CustomTilemap implements Bundlable {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L35) `protected static final int SIZE = DungeonTilemap.SIZE;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L40) `protected Object texture;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L41) `protected Tilemap vis = null;`
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L151) `private static final String TILE_X  = "tileX";`
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L152) `private static final String TILE_Y  = "tileY";`
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L154) `private static final String TILE_W  = "tileW";`
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L155) `private static final String TILE_H  = "tileH";`

### 메서드 및 코드 의존 단서
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L43) `public void pos(int pos) {` — 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L47) `public void pos(int pos, Level level) {` — 개별 처리
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L51) `public void pos(int tileX, int tileY){` — 개별 처리, 인접 호출: NoosaScript.get
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L56) `public void setRect(int topLeft, int bottomRight){` — 개별 처리, 인접 호출: NoosaScript.get
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L64) `public void setRect(int tileX, int tileY, int tileW, int tileH){` — 개별 처리, 인접 호출: NoosaScript.get
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L73) `protected int[] mapSimpleImage(int txX, int txY, int texW){` — 개별 처리, 인접 호출: NoosaScript.get
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L89) `public Tilemap create(){` — 생성·초기화, 인접 호출: NoosaScript.get
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L93) `protected NoosaScript script() {` — 개별 처리, 인접 호출: NoosaScript.get
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L99) `public synchronized void updateMap() {` — 행동·상태 갱신
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L105) `public synchronized void updateMapCell(int cell) {` — 행동·상태 갱신
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L121) `protected boolean updateCell(int cell, int[] data){` — 행동·상태 갱신
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L125) `protected void updateAll(int[] data){` — 행동·상태 갱신
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L130) `public boolean allowWater(int tileX, int tileY){` — 개별 처리
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L135) `public Image image(int tileX, int tileY){` — 개별 처리
- [L143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L143) `public String name(int tileX, int tileY){` — 개별 처리
- [L147](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L147) `public String desc(int tileX, int tileY){` — 개별 처리
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L158) `public void restoreFromBundle(Bundle bundle) {` — 저장·복원
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java#L167) `public void storeInBundle(Bundle bundle) {` — 저장·복원

## 1087. [`DungeonTerrainTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTerrainTilemap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.tiles`, 130행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTerrainTilemap.java#L30) `public class DungeonTerrainTilemap extends DungeonTilemap {`

### 변수·상수 후보
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTerrainTilemap.java#L32) `static DungeonTerrainTilemap instance;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTerrainTilemap.java#L34) `public DungeonTerrainTilemap(){` — 개별 처리, 인접 호출: DungeonTileSheet.getVisualWithAlts, DungeonTileSheet.stitchWaterTile, DungeonTileSheet.stitchChasmTile, DungeonTileSheet.doorTile, DungeonTileSheet.getRaisedDoorTile, DungeonTileSheet.wallStitcheable, DungeonTileSheet.getRaisedWallTile
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTerrainTilemap.java#L43) `protected int getTileVisual(int pos, int tile, boolean flat) {` — 조회·판정, 인접 호출: DungeonTileSheet.getVisualWithAlts, DungeonTileSheet.stitchWaterTile, DungeonTileSheet.stitchChasmTile, DungeonTileSheet.doorTile, DungeonTileSheet.getRaisedDoorTile, DungeonTileSheet.wallStitcheable, DungeonTileSheet.getRaisedWallTile
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTerrainTilemap.java#L119) `public static Image tile(int pos, int tile ) {` — 개별 처리
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTerrainTilemap.java#L126) `protected boolean needsRender(int pos) {` — 개별 처리

## 1088. [`DungeonTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.tiles`, 179행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L34) `public abstract class DungeonTilemap extends Tilemap {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L36) `public static final int SIZE = 16;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L38) `protected int[] map;`

### 메서드 및 코드 의존 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L40) `public DungeonTilemap(String tex) {` — 개별 처리
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L47) `public void map(int[] data, int cols) {` — 개별 처리, 인접 호출: GameMath.gate
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L53) `public synchronized void updateMap() {` — 행동·상태 갱신, 인접 호출: GameMath.gate
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L60) `public synchronized void updateMapCell(int cell) {` — 행동·상태 갱신, 인접 호출: GameMath.gate
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L76) `protected abstract int getTileVisual(int pos, int tile, boolean flat);` — 조회·판정, 인접 호출: GameMath.gate, DungeonTileSheet.wallStitcheable
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L78) `public int screenToTile(int x, int y ){` — 개별 처리, 인접 호출: GameMath.gate, DungeonTileSheet.wallStitcheable
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L82) `public int screenToTile(int x, int y, boolean wallAssist ) {` — 개별 처리, 인접 호출: GameMath.gate, DungeonTileSheet.wallStitcheable
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L111) `private boolean isWallAssistable(int cell){` — 조회·판정, 인접 호출: DungeonTileSheet.wallStitcheable
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L130) `public boolean overlapsPoint( float x, float y ) {` — 개별 처리
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L134) `public void discover( int pos, int oldValue ) {` — 개별 처리
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L139) `final Image tile = new Image( texture );` — 개별 처리
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L146) `protected void onComplete() {` — 이벤트·효과 실행
- [L153](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L153) `public static PointF tileToWorld( int pos ) {` — 개별 처리
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L157) `public static PointF tileCenterToWorld( int pos ) {` — 개별 처리
- [L163](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L163) `public static PointF raisedTileCenterToWorld( int pos ) {` — 개별 처리
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L169) `public static int worldToTile( float x, float y, int width){` — 개별 처리
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java#L174) `public boolean overlapsScreenPoint( int x, int y ) {` — 개별 처리

## 1089. [`DungeonTileSheet.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.tiles`, 557행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L34) `public class DungeonTileSheet {`
- [L492](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L492) `private static class tileAlt {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L36) `private static final int WIDTH = 16;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L44) `public static final int NULL_TILE       = -1;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L53) `public static final int FLOOR           = GROUND +0;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L54) `public static final int FLOOR_DECO      = GROUND +1;`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L55) `public static final int GRASS           = GROUND +2;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L56) `public static final int EMBERS          = GROUND +3;`
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L57) `public static final int FLOOR_SP        = GROUND +4;`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L59) `public static final int MINE_FLOOR_DECO_HEAVY   = GROUND +5;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L61) `public static final int FLOOR_ALT_1     = GROUND +6;`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L62) `public static final int FLOOR_DECO_ALT  = GROUND +7;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L63) `public static final int GRASS_ALT       = GROUND +8;`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L64) `public static final int EMBERS_ALT      = GROUND +9;`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L65) `public static final int FLOOR_SP_ALT    = GROUND +10;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L67) `public static final int MINE_FLOOR_DECO_HEAVY_ALT   = GROUND +11;`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L69) `public static final int FLOOR_ALT_2     = GROUND +12;`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L71) `public static final int ENTRANCE        = GROUND +16;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L72) `public static final int EXIT            = GROUND +17;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L73) `public static final int WELL            = GROUND +18;`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L74) `public static final int EMPTY_WELL      = GROUND +19;`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L75) `public static final int PEDESTAL        = GROUND +20;`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L77) `public static final int ENTRANCE_SP     = GROUND +22;`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L81) `public static final int CHASM_FLOOR     = CHASM+1;`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L82) `public static final int CHASM_FLOOR_SP  = CHASM+2;`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L83) `public static final int CHASM_WALL      = CHASM+3;`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L84) `public static final int CHASM_WATER     = CHASM+4;`
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L188) `public static final int FLAT_WALL           = FLAT_WALLS+0;`
- [L189](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L189) `public static final int FLAT_WALL_DECO      = FLAT_WALLS+1;`
- [L190](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L190) `public static final int FLAT_BOOKSHELF      = FLAT_WALLS+2;`
- [L192](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L192) `public static final int FLAT_WALL_ALT       = FLAT_WALLS+4;`
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L193) `public static final int FLAT_WALL_DECO_ALT  = FLAT_WALLS+5;`
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L194) `public static final int FLAT_BOOKSHELF_ALT  = FLAT_WALLS+6;`
- [L196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L196) `public static final int FLAT_DOOR           = FLAT_WALLS+8;`
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L197) `public static final int FLAT_DOOR_OPEN      = FLAT_WALLS+9;`
- [L198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L198) `public static final int FLAT_DOOR_LOCKED    = FLAT_WALLS+10;`
- [L199](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L199) `public static final int FLAT_DOOR_CRYSTAL   = FLAT_WALLS+11;`
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L200) `public static final int UNLOCKED_EXIT       = FLAT_WALLS+12;`
- [L201](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L201) `public static final int LOCKED_EXIT         = FLAT_WALLS+13;`
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L204) `public static final int FLAT_ALCHEMY_POT    = FLAT_OTHER+0;`
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L205) `public static final int FLAT_BARRICADE      = FLAT_OTHER+1;`
- [L206](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L206) `public static final int FLAT_HIGH_GRASS     = FLAT_OTHER+2;`
- [L207](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L207) `public static final int FLAT_FURROWED_GRASS = FLAT_OTHER+3;`
- [L209](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L209) `public static final int FLAT_HIGH_GRASS_ALT = FLAT_OTHER+5;`
- [L210](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L210) `public static final int FLAT_FURROWED_ALT   = FLAT_OTHER+6;`
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L212) `public static final int FLAT_STATUE         = FLAT_OTHER+8;`
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L213) `public static final int FLAT_STATUE_SP      = FLAT_OTHER+9;`
- [L214](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L214) `public static final int FLAT_REGION_DECO    = FLAT_OTHER+10;`
- [L215](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L215) `public static final int FLAT_REGION_DECO_ALT= FLAT_OTHER+11;`
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L217) `public static final int FLAT_MINE_CRYSTAL         = FLAT_OTHER+12;`
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L218) `public static final int FLAT_MINE_CRYSTAL_ALT     = FLAT_OTHER+13;`
- [L219](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L219) `public static final int FLAT_MINE_CRYSTAL_ALT_2   = FLAT_OTHER+14;`
- [L220](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L220) `public static final int FLAT_MINE_BOULDER         = FLAT_OTHER+12;`
- [L221](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L221) `public static final int FLAT_MINE_BOULDER_ALT     = FLAT_OTHER+13;`
- [L222](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L222) `public static final int FLAT_MINE_BOULDER_ALT_2   = FLAT_OTHER+14;`
- [L230](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L230) `public static final int RAISED_WALL                 = RAISED_WALLS+0;`
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L231) `public static final int RAISED_WALL_DECO            = RAISED_WALLS+4;`
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L233) `public static final int RAISED_WALL_DOOR            = RAISED_WALLS+8;`
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L234) `public static final int RAISED_WALL_BOOKSHELF       = RAISED_WALLS+12;`
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L236) `public static final int RAISED_WALL_ALT             = RAISED_WALLS+16;`
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L237) `public static final int RAISED_WALL_DECO_ALT        = RAISED_WALLS+20;`
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L238) `public static final int RAISED_WALL_BOOKSHELF_ALT   = RAISED_WALLS+28;`
- [L274](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L274) `public static final int RAISED_DOOR             = RAISED_DOORS+0;`
- [L275](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L275) `public static final int RAISED_DOOR_OPEN        = RAISED_DOORS+1;`
- [L276](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L276) `public static final int RAISED_DOOR_LOCKED      = RAISED_DOORS+2;`
- [L277](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L277) `public static final int RAISED_DOOR_CRYSTAL     = RAISED_DOORS+3;`
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L279) `public static final int RAISED_DOOR_SIDEWAYS    = RAISED_DOORS+4;`
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L304) `public static final int RAISED_ALCHEMY_POT      = RAISED_OTHER+0;`
- [L305](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L305) `public static final int RAISED_BARRICADE        = RAISED_OTHER+1;`
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L306) `public static final int RAISED_HIGH_GRASS       = RAISED_OTHER+2;`
- [L307](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L307) `public static final int RAISED_FURROWED_GRASS   = RAISED_OTHER+3;`
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L309) `public static final int RAISED_HIGH_GRASS_ALT   = RAISED_OTHER+5;`
- [L310](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L310) `public static final int RAISED_FURROWED_ALT     = RAISED_OTHER+6;`
- [L312](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L312) `public static final int RAISED_STATUE           = RAISED_OTHER+8;`
- [L313](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L313) `public static final int RAISED_STATUE_SP        = RAISED_OTHER+9;`
- [L314](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L314) `public static final int RAISED_REGION_DECO      = RAISED_OTHER+10;`
- [L315](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L315) `public static final int RAISED_REGION_DECO_ALT  = RAISED_OTHER+11;`
- [L318](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L318) `public static final int RAISED_MINE_CRYSTAL_BLUE_2  = RAISED_OTHER+13;`
- [L319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L319) `public static final int RAISED_MINE_CRYSTAL_GREEN_1 = RAISED_OTHER+14;`
- [L320](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L320) `public static final int RAISED_MINE_CRYSTAL_GREEN_2 = RAISED_OTHER+15;`
- [L321](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L321) `public static final int RAISED_MINE_CRYSTAL_RED_1   = RAISED_OTHER+16;`
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L322) `public static final int RAISED_MINE_CRYSTAL_RED_2   = RAISED_OTHER+17;`
- [L324](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L324) `public static final int RAISED_MINE_BOULDER     = RAISED_OTHER+12;`
- [L325](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L325) `public static final int RAISED_MINE_BOULDER_ALT = RAISED_OTHER+13;`
- [L326](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L326) `public static final int RAISED_MINE_BOULDER_ALT_2=RAISED_OTHER+14;`
- [L335](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L335) `private static final int WALL_INTERNAL              = WALLS_INTERNAL+0;`
- [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L336) `private static final int WALL_INTERNAL_DECO         = WALLS_INTERNAL+16;`
- [L337](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L337) `private static final int WALL_INTERNAL_WOODEN       = WALLS_INTERNAL+32;`
- [L356](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L356) `public static final int WALL_OVERHANG                   = WALLS_OVERHANG+0;`
- [L357](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L357) `public static final int WALL_OVERHANG_DECO              = WALLS_OVERHANG+4;`
- [L358](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L358) `public static final int WALL_OVERHANG_WOODEN            = WALLS_OVERHANG+8;`
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L359) `public static final int DOOR_SIDEWAYS_OVERHANG          = WALLS_OVERHANG+16;`
- [L360](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L360) `public static final int DOOR_SIDEWAYS_OVERHANG_CLOSED   = WALLS_OVERHANG+20;`
- [L361](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L361) `public static final int DOOR_SIDEWAYS_OVERHANG_LOCKED   = WALLS_OVERHANG+24;`
- [L362](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L362) `public static final int DOOR_SIDEWAYS_OVERHANG_CRYSTAL  = WALLS_OVERHANG+28;`
- [L384](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L384) `public static final int DOOR_OVERHANG_OPEN          = DOOR_OVERHANG+1;`
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L385) `public static final int DOOR_OVERHANG_CRYSTAL       = DOOR_OVERHANG+2;`
- [L386](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L386) `public static final int DOOR_SIDEWAYS               = DOOR_OVERHANG+3;`
- [L387](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L387) `public static final int DOOR_SIDEWAYS_LOCKED        = DOOR_OVERHANG+4;`
- [L388](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L388) `public static final int DOOR_SIDEWAYS_CRYSTAL       = DOOR_OVERHANG+5;`
- [L390](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L390) `public static final int EXIT_UNDERHANG              = DOOR_OVERHANG+6;`
- [L394](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L394) `public static final int ALCHEMY_POT_OVERHANG        = OTHER_OVERHANG+0;`
- [L395](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L395) `public static final int BARRICADE_OVERHANG          = OTHER_OVERHANG+1;`
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L396) `public static final int HIGH_GRASS_OVERHANG         = OTHER_OVERHANG+2;`
- [L397](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L397) `public static final int FURROWED_OVERHANG           = OTHER_OVERHANG+3;`
- [L399](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L399) `public static final int HIGH_GRASS_OVERHANG_ALT     = OTHER_OVERHANG+5;`
- [L400](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L400) `public static final int FURROWED_OVERHANG_ALT       = OTHER_OVERHANG+6;`
- [L402](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L402) `public static final int STATUE_OVERHANG             = OTHER_OVERHANG+8;`
- [L403](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L403) `public static final int STATUE_SP_OVERHANG          = OTHER_OVERHANG+9;`
- [L404](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L404) `public static final int REGION_DECO_OVERHANG        = OTHER_OVERHANG+10;`
- [L405](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L405) `public static final int REGION_DECO_ALT_OVERHANG    = OTHER_OVERHANG+11;`
- [L407](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L407) `public static final int MINE_CRYSTAL_OVERHANG_BLUE  = OTHER_OVERHANG+12;`
- [L408](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L408) `public static final int MINE_CRYSTAL_OVERHANG_GREEN = OTHER_OVERHANG+13;`
- [L409](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L409) `public static final int MINE_CRYSTAL_OVERHANG_RED   = OTHER_OVERHANG+14;`
- [L410](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L410) `public static final int MINE_BOULDER_OVERHANG       = OTHER_OVERHANG+12;`
- [L411](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L411) `public static final int MINE_BOULDER_OVERHANG_ALT   = OTHER_OVERHANG+13;`
- [L412](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L412) `public static final int MINE_BOULDER_OVERHANG_ALT_2 = OTHER_OVERHANG+14;`
- [L478](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L478) `public static byte[] tileVariance;`

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L38) `private static int xy(int x, int y){` — 개별 처리
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L52) `private static final int GROUND         =                               xy(1, 1);   //24 slots` — 개별 처리
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L79) `public static final int CHASM           =                               xy(9, 2);   //8 slots` — 개별 처리
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L129) `public static int stitchChasmTile(int above){` — 개별 처리, 인접 호출: Arrays.asList
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L145) `public static final int WATER =                                         xy(1, 3);   //16 slots` — 개별 처리, 인접 호출: Arrays.asList
- [L159](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L159) `public static boolean waterStitcheable(int tile){` — 개별 처리
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L169) `public static int stitchWaterTile(int top, int right, int bottom, int left){` — 개별 처리
- [L178](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L178) `public static boolean floorTile(int tile){` — 개별 처리
- [L187](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L187) `private static final int FLAT_WALLS         =                           xy(1, 4);   //16 slots` — 개별 처리
- [L203](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L203) `public static final int FLAT_OTHER          =                           xy(1, 5);   //16 slots` — 개별 처리
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L228) `private static final int RAISED_WALLS               =                   xy(1, 6);   //32 slots` — 개별 처리
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L249) `public static boolean wallStitcheable(int tile){` — 개별 처리
- [L256](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L256) `public static int getRaisedWallTile(int tile, int pos, int right, int below, int left){` — 조회·판정
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L273) `private static final int RAISED_DOORS           =                       xy(1, 8);  //8 slots` — 개별 처리
- [L282](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L282) `public static int getRaisedDoorTile(int tile, int below){` — 조회·판정
- [L296](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L296) `public static boolean doorTile(int tile){` — 개별 처리
- [L303](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L303) `private static final int RAISED_OTHER           =                       xy(9, 8);  //24 slots` — 개별 처리
- [L334](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L334) `public static final int WALLS_INTERNAL              =                   xy(1, 10);  //48 slots` — 개별 처리
- [L339](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L339) `public static int stitchInternalWallTile(int tile, int right, int rightBelow, int below, int leftBelow, int left){` — 개별 처리
- [L355](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L355) `private static final int WALLS_OVERHANG             =                   xy(1, 13);  //32 slots` — 개별 처리
- [L365](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L365) `public static int stitchWallOverhangTile(int tile, int rightBelow, int below, int leftBelow){` — 개별 처리
- [L383](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L383) `public static final int DOOR_OVERHANG               =                   xy(1, 15);  //8 slots` — 개별 처리
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L393) `private static final int OTHER_OVERHANG             =                   xy(9, 15);  //24 slots` — 개별 처리
- [L480](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L480) `public static void setupVariance(int size, long seed){` — 생성·초기화, 인접 호출: Random.pushGenerator, Random.Int, Random.popGenerator
- [L495](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L495) `public tileAlt(float[] chances, int... alts){` — 개별 처리, 인접 호출: Quest.Type
- [L526](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L526) `public static void updateAltVariants(){` — 행동·상태 갱신, 인접 호출: Quest.Type
- [L544](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java#L544) `public static int getVisualWithAlts(int visual, int pos){` — 조회·판정

## 1090. [`DungeonWallsTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonWallsTilemap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.tiles`, 133행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonWallsTilemap.java#L29) `public class DungeonWallsTilemap extends DungeonTilemap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonWallsTilemap.java#L33) `public DungeonWallsTilemap(){` — 개별 처리, 인접 호출: DungeonTileSheet.wallStitcheable, DungeonTileSheet.stitchInternalWallTile
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonWallsTilemap.java#L40) `protected int getTileVisual(int pos, int tile, boolean flat){` — 조회·판정, 인접 호출: DungeonTileSheet.wallStitcheable, DungeonTileSheet.stitchInternalWallTile, DungeonTileSheet.stitchWallOverhangTile
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonWallsTilemap.java#L123) `public boolean overlapsPoint( float x, float y ) {` — 개별 처리
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonWallsTilemap.java#L128) `public boolean overlapsScreenPoint( int x, int y ) {` — 개별 처리

## 1091. [`FogOfWar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.tiles`, 339행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L35) `public class FogOfWar extends Image {`

### 변수·상수 후보
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L60) `private static final int VISIBLE    =   0;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L61) `private static final int VISITED    =   1;`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L62) `private static final int MAPPED     =   2;`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L63) `private static final int INVISIBLE  =   3;`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L65) `private int mapWidth;`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L66) `private int mapHeight;`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L67) `private int mapLength;`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L69) `private int pWidth;`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L70) `private int pHeight;`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L72) `private int width2;`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L73) `private int height2;`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L75) `private volatile ArrayList<Rect> toUpdate;`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L76) `private volatile ArrayList<Rect> updating;`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L79) `private static final int PIX_PER_TILE = 2;`
- [L167](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L167) `private boolean[] visible;`
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L168) `private boolean[] visited;`
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L169) `private boolean[] mapped;`
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L170) `private int brightness;`

### 메서드 및 코드 의존 단서
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L88) `public FogOfWar( int mapWidth, int mapHeight ) {` — 개별 처리, 인접 호출: TextureCache.create
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L128) `public synchronized void updateFog(){` — 행동·상태 갱신, 인접 호출: Math.max, Math.min
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L133) `public synchronized void updateFog(Rect update){` — 행동·상태 갱신, 인접 호출: Math.max, Math.min, SPDSettings.brightness
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L144) `public synchronized void updateFog( int cell, int radius ){` — 행동·상태 갱신, 인접 호출: Math.max, Math.min, SPDSettings.brightness
- [L158](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L158) `public synchronized void updateFogArea(int x, int y, int w, int h){` — 행동·상태 갱신, 인접 호출: SPDSettings.brightness
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L162) `private synchronized void moveToUpdating(){` — 개별 처리, 인접 호출: SPDSettings.brightness
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L172) `private void updateTexture( boolean[] visible, boolean[] visited, boolean[] mapped ) {` — 행동·상태 갱신, 인접 호출: SPDSettings.brightness
- [L284](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L284) `private boolean wall(int cell) {` — 개별 처리, 인접 호출: DungeonTileSheet.wallStitcheable, NoosaScriptNoLighting.get
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L288) `private int getCellFog( int cell ){` — 조회·판정, 인접 호출: NoosaScriptNoLighting.get
- [L301](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L301) `private void fillLeft( Pixmap fog, int x, int y, int color){` — 개별 처리, 인접 호출: NoosaScriptNoLighting.get, TextureCache.remove
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L306) `private void fillRight( Pixmap fog, int x, int y, int color){` — 개별 처리, 인접 호출: NoosaScriptNoLighting.get, TextureCache.remove
- [L311](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L311) `private void fillCell( Pixmap fog, int x, int y, int color){` — 개별 처리, 인접 호출: NoosaScriptNoLighting.get, TextureCache.remove
- [L317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L317) `protected NoosaScript script() {` — 개별 처리, 인접 호출: NoosaScriptNoLighting.get, TextureCache.remove
- [L322](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L322) `public void draw() {` — 개별 처리, 인접 호출: TextureCache.remove
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java#L332) `public void destroy() {` — 개별 처리, 인접 호출: TextureCache.remove

## 1092. [`GridTileMap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/GridTileMap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.tiles`, 65행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/GridTileMap.java#L29) `public class GridTileMap extends DungeonTilemap {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/GridTileMap.java#L37) `private int gridSetting = -1;`

### 메서드 및 코드 의존 단서
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/GridTileMap.java#L31) `public GridTileMap() {` — 개별 처리, 인접 호출: SPDSettings.visualGrid, DungeonTileSheet.floorTile, DungeonTileSheet.doorTile, DungeonTileSheet.wallStitcheable
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/GridTileMap.java#L40) `public synchronized void updateMap() {` — 행동·상태 갱신, 인접 호출: SPDSettings.visualGrid, DungeonTileSheet.floorTile, DungeonTileSheet.doorTile, DungeonTileSheet.wallStitcheable
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/GridTileMap.java#L46) `protected int getTileVisual(int pos, int tile, boolean flat) {` — 조회·판정, 인접 호출: DungeonTileSheet.floorTile, DungeonTileSheet.doorTile, DungeonTileSheet.wallStitcheable

## 1093. [`RaisedTerrainTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/RaisedTerrainTilemap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.tiles`, 69행.

### 클래스/타입
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/RaisedTerrainTilemap.java#L30) `public class RaisedTerrainTilemap extends DungeonTilemap {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/RaisedTerrainTilemap.java#L32) `public RaisedTerrainTilemap() {` — 개별 처리, 인접 호출: DungeonTileSheet.getVisualWithAlts
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/RaisedTerrainTilemap.java#L41) `protected int getTileVisual(int pos, int tile, boolean flat) {` — 조회·판정, 인접 호출: DungeonTileSheet.getVisualWithAlts

## 1094. [`TerrainFeaturesTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.tiles`, 191행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java#L36) `public class TerrainFeaturesTilemap extends DungeonTilemap {`

### 변수·상수 후보
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java#L38) `private static TerrainFeaturesTilemap instance;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java#L40) `private SparseArray<Plant> plants;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java#L41) `private SparseArray<Trap> traps;`

### 메서드 및 코드 의존 단서
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java#L43) `public TerrainFeaturesTilemap(SparseArray<Plant> plants, SparseArray<Trap> traps) {` — 개별 처리, 인접 호출: Math.min, DungeonTileSheet.getVisualWithAlts
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java#L56) `protected int getTileVisual(int pos, int tile, boolean flat){` — 조회·판정, 인접 호출: Math.min, DungeonTileSheet.getVisualWithAlts
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java#L140) `public static Image getTrapVisual( Trap trap ){` — 조회·판정, 인접 호출: DungeonTilemap.tileToWorld
- [L151](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java#L151) `public static Image getPlantVisual( Plant plant ){` — 조회·판정, 인접 호출: DungeonTilemap.tileToWorld
- [L162](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java#L162) `public static Image tile(int pos, int tile ) {` — 개별 처리, 인접 호출: DungeonTilemap.tileToWorld
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java#L171) `public void growPlant( final int pos ){` — 개별 처리, 인접 호출: DungeonTilemap.tileToWorld
- [L172](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java#L172) `final Image plant = tile( pos, map[pos] );` — 개별 처리, 인접 호출: DungeonTilemap.tileToWorld
- [L182](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java#L182) `protected void onComplete() {` — 이벤트·효과 실행

## 1095. [`WallBlockingTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.tiles`, 241행.

### 클래스/타입
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L33) `public class WallBlockingTilemap extends Tilemap {`

### 변수·상수 후보
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L35) `public static final int SIZE = 16;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L37) `private static final int CLEARED        = -2;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L38) `private static final int BLOCK_NONE     = -1;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L39) `private static final int BLOCK_RIGHT    = 0;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L40) `private static final int BLOCK_LEFT     = 1;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L41) `private static final int BLOCK_ALL      = 2;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L42) `private static final int BLOCK_BELOW    = 3;`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L65) `private int curr;`

### 메서드 및 코드 의존 단서
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L44) `public WallBlockingTilemap() {` — 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L50) `public synchronized void updateMap() {` — 행동·상태 갱신
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L68) `public synchronized void updateMapCell(int cell) {` — 행동·상태 갱신
- [L194](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L194) `private boolean fogHidden(int cell){` — 개별 처리, 인접 호출: DungeonTileSheet.wallStitcheable, DungeonTileSheet.doorTile, Math.max, Math.min
- [L204](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L204) `private boolean wall(int cell) {` — 개별 처리, 인접 호출: DungeonTileSheet.wallStitcheable, DungeonTileSheet.doorTile, Math.max, Math.min
- [L208](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L208) `private boolean shelf(int cell) {` — 개별 처리, 인접 호출: DungeonTileSheet.doorTile, Math.max, Math.min
- [L212](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L212) `private boolean door(int cell) {` — 개별 처리, 인접 호출: DungeonTileSheet.doorTile, Math.max, Math.min
- [L216](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L216) `public synchronized void updateArea(int cell, int radius){` — 행동·상태 갱신, 인접 호출: Math.max, Math.min
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java#L229) `public synchronized void updateArea(int x, int y, int w, int h) {` — 행동·상태 갱신

## 1096. [`WallOcclusionTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.tiles`, 134행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L28) `public class WallOcclusionTilemap extends DungeonTilemap {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L30) `public static final int SIZE = 16;`
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L33) `private static final int CLEARED        = 0;`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L34) `private static final int EMPTY          = 0;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L35) `private static final int DOOR_VERT      = 6;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L36) `private static final int DOOR_HORIZ     = 7;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L39) `private static final int WALL_ABOVE     = 40;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L40) `private static final int WALL_LEFT_BELOW= 1;`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L41) `private static final int WALL_LEFT      = 2;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L42) `private static final int WALL_LEFT_ABOVE= 3;`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L44) `private static final int WALL_RIGHT_BELOW= 8;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L45) `private static final int WALL_RIGHT     = 16;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L46) `private static final int WALL_RIGHT_ABOVE= 24;`

### 메서드 및 코드 의존 단서
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L49) `public WallOcclusionTilemap() {` — 개별 처리, 인접 호출: DungeonTileSheet.doorTile, DungeonTileSheet.wallStitcheable
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L54) `protected int getTileVisual( int pos, int tile, boolean flat ){` — 조회·판정, 인접 호출: DungeonTileSheet.doorTile, DungeonTileSheet.wallStitcheable
- [L126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L126) `private boolean wall(int cell) {` — 개별 처리, 인접 호출: DungeonTileSheet.wallStitcheable, DungeonTileSheet.doorTile
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java#L130) `private boolean door(int cell) {` — 개별 처리, 인접 호출: DungeonTileSheet.doorTile

## 1097. [`ActionIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 206행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L32) `public class ActionIndicator extends Tag {`
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L181) `public interface Action {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L37) `public static Action action;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L38) `public static ActionIndicator instance;`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L83) `private boolean needsRefresh = false;`

### 메서드 및 코드 의존 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L40) `public ActionIndicator() {` — 개별 처리, 인접 호출: PixelScene.align
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L50) `public GameAction keyAction() {` — 개별 처리, 인접 호출: PixelScene.align
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L55) `public void destroy() {` — 개별 처리, 인접 호출: PixelScene.align
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L61) `protected synchronized void layout() {` — 개별 처리, 인접 호출: PixelScene.align
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L86) `public void update() {` — 행동·상태 갱신
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L89) `synchronized (ActionIndicator.class) {` — 개별 처리
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L137) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L145) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L154) `public static void setAction(Action action){` — 개별 처리
- [L155](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L155) `synchronized (ActionIndicator.class) {` — 개별 처리
- [L161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L161) `public static void clearAction(){` — 개별 처리
- [L165](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L165) `public static void clearAction(Action action){` — 개별 처리
- [L166](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L166) `synchronized (ActionIndicator.class) {` — 개별 처리
- [L173](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L173) `public static void refresh(){` — 개별 처리
- [L174](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java#L174) `synchronized (ActionIndicator.class) {` — 개별 처리

## 1098. [`Archs.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 112행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L34) `public class Archs extends Component {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L36) `private static final float SCROLL_SPEED	= 20f;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L38) `private SkinnedBlock arcsBg;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L39) `private SkinnedBlock arcsFg;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L40) `private Image darkness;`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L42) `private static float offsB = 0;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L43) `private static float offsF = 0;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L45) `public boolean reversed = false;`

### 메서드 및 코드 의존 단서
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L48) `protected void createChildren() {` — 생성·초기화, 인접 호출: NoosaScriptNoLighting.get, Blending.disable, Blending.enable, TextureCache.createGradient
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L51) `protected NoosaScript script() {` — 개별 처리, 인접 호출: NoosaScriptNoLighting.get, Blending.disable, Blending.enable, TextureCache.createGradient
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L56) `public void draw() {` — 개별 처리, 인접 호출: Blending.disable, Blending.enable, NoosaScriptNoLighting.get, TextureCache.createGradient
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L69) `protected NoosaScript script() {` — 개별 처리, 인접 호출: NoosaScriptNoLighting.get, TextureCache.createGradient
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L83) `protected void layout() {` — 개별 처리
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Archs.java#L96) `public void update() {` — 행동·상태 갱신

## 1099. [`AttackIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 209행.

### 클래스/타입
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L40) `public class AttackIndicator extends Tag {`

### 변수·상수 후보
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L42) `private static final float ENABLED	= 1.0f;`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L43) `private static final float DISABLED	= 0.3f;`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L45) `private static float delay;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L47) `private static AttackIndicator instance;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L49) `private CharSprite sprite = null;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L51) `private Mob lastTarget;`
- [L168](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L168) `private boolean enabled = true;`

### 메서드 및 코드 의존 단서
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L54) `public AttackIndicator() {` — 개별 처리, 인접 호출: PixelScene.align
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L57) `synchronized (this) {` — 개별 처리, 인접 호출: PixelScene.align
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L68) `public GameAction keyAction() {` — 개별 처리, 인접 호출: PixelScene.align
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L73) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.align
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L78) `protected synchronized void layout() {` — 개별 처리, 인접 호출: PixelScene.align
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L90) `public synchronized void update() {` — 행동·상태 갱신, 인접 호출: Random.element
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L114) `private synchronized void checkEnemies() {` — 개별 처리, 인접 호출: Random.element, Reflection.newInstance
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L145) `private synchronized void updateImage() {` — 행동·상태 갱신, 인접 호출: Reflection.newInstance, PixelScene.align, Math.max
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L169) `private synchronized void enable( boolean value ) {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, QuickSlotButton.target
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L176) `private synchronized void visible( boolean value ) {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, QuickSlotButton.target
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L181) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.titleCase, Messages.get, QuickSlotButton.target
- [L191](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L191) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.titleCase, Messages.get, QuickSlotButton.target
- [L195](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L195) `public static void target(Char target ) {` — 개별 처리, 인접 호출: QuickSlotButton.target
- [L197](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L197) `synchronized (instance) {` — 개별 처리, 인접 호출: QuickSlotButton.target
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java#L205) `public static void updateState() {` — 행동·상태 갱신

## 1100. [`BadgesGrid.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 151행.

### 클래스/타입
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java#L37) `public class BadgesGrid extends Component {`
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java#L100) `private static class BadgeButton extends Button {`

### 변수·상수 후보
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java#L102) `private Badges.Badge badge;`
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java#L103) `private boolean unlocked;`
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java#L105) `private Image icon;`

### 메서드 및 코드 의존 단서
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java#L41) `public BadgesGrid( boolean global ){` — 개별 처리, 인접 호출: Badges.filterReplacedBadges, Badge.values, Badges.isUnlocked, Badges.filterBadgesWithoutPrerequisites, Math.sqrt, Math.round, Math.ceil
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java#L77) `protected void layout() {` — 개별 처리, 인접 호출: Math.sqrt, Math.round, Math.ceil, PixelScene.align, BadgeBanner.image
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java#L107) `public BadgeButton( Badges.Badge badge, boolean unlocked ) {` — 개별 처리, 인접 호출: BadgeBanner.image, Random.Float, BadgeBanner.highlight, INSTANCE.play, Game.scene
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java#L123) `protected void layout() {` — 개별 처리, 인접 호출: Random.Float, BadgeBanner.highlight, INSTANCE.play, Game.scene
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java#L131) `public void update() {` — 행동·상태 갱신, 인접 호출: Random.Float, BadgeBanner.highlight, INSTANCE.play, Game.scene
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java#L140) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, Game.scene
- [L146](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesGrid.java#L146) `protected String hoverText() {` — 개별 처리

## 1101. [`BadgesList.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.ui`, 131행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L36) `public class BadgesList extends ScrollPane {`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L81) `private class ListItem extends Component {`

### 변수·상수 후보
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L83) `private static final float HEIGHT	= 18;`
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L85) `private Badges.Badge badge;`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L87) `private Image icon;`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L88) `private RenderedTextBlock label;`

### 메서드 및 코드 의존 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L40) `public BadgesList( boolean global ) {` — 개별 처리, 인접 호출: Badges.filterReplacedBadges
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L56) `protected void layout() {` — 개별 처리, 인접 호출: BadgeBanner.image
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L72) `public void onClick( float x, float y ) {` — 이벤트·효과 실행, 인접 호출: BadgeBanner.image, PixelScene.renderTextBlock, PixelScene.align
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L90) `public ListItem( Badges.Badge badge ) {` — 개별 처리, 인접 호출: BadgeBanner.image, PixelScene.renderTextBlock, PixelScene.align, INSTANCE.play, Game.scene
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L99) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.renderTextBlock, PixelScene.align, INSTANCE.play, Game.scene
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L108) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, INSTANCE.play, Game.scene
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BadgesList.java#L120) `public boolean onClick( float x, float y ) {` — 이벤트·효과 실행, 인접 호출: INSTANCE.play, Game.scene


# Java 소스 구현 분석 1192–1209

원본 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 실제 원문에서 클래스·변수·메서드·참조 표현을 추출하였다. 기능 분류는 **메서드명과 인접 코드에 기반한 정적 추론**이며, Java AST·런타임 전체 분기 검증이 아니다.

## 1192. [`WndInfoArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoArmorAbility.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 58행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoArmorAbility.java#L36) `public class WndInfoArmorAbility extends WndTitledMessage {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoArmorAbility.java#L38) `public WndInfoArmorAbility(HeroClass cls, ArmorAbility ability){` — 개별 처리, 인접 호출: Messages.titleCase, Talent.initArmorTalents, TalentsPane.TalentTierPane, Messages.get
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoArmorAbility.java#L54) `protected float targetHeight() {` — 개별 처리

## 1193. [`WndInfoBuff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoBuff.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 58행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoBuff.java#L32) `public class WndInfoBuff extends Window {`

### 변수·상수 후보
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoBuff.java#L34) `private static final float GAP	= 2;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoBuff.java#L36) `private static final int WIDTH = 120;`

### 메서드 및 코드 의존 단서
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoBuff.java#L38) `public WndInfoBuff(Buff buff){` — 개별 처리, 인접 호출: Messages.titleCase, PixelScene.renderTextBlock

## 1194. [`WndInfoCell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoCell.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 192행.

### 클래스/타입
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoCell.java#L36) `public class WndInfoCell extends Window {`

### 변수·상수 후보
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoCell.java#L38) `private static final float GAP	= 2;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoCell.java#L40) `private static final int WIDTH = 120;`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoCell.java#L42) `public static Image cellImage( int cell ){` — 개별 처리, 인접 호출: DungeonTerrainTilemap.tile
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoCell.java#L86) `public static String cellName( int cell ){` — 개별 처리
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoCell.java#L121) `public WndInfoCell( int cell ) {` — 개별 처리

## 1195. [`WndInfoItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 132행.

### 클래스/타입
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java#L31) `public class WndInfoItem extends Window {`

### 변수·상수 후보
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java#L33) `private static final float GAP	= 2;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java#L35) `private static final int WIDTH_MIN = 120;`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java#L36) `private static final int WIDTH_MAX = 220;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java#L39) `private static WndInfoItem INSTANCE;`

### 메서드 및 코드 의존 단서
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java#L41) `public WndInfoItem( Heap heap ) {` — 개별 처리, 인접 호출: INSTANCE.hide, PixelScene.renderTextBlock
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java#L59) `public WndInfoItem( Item item ) {` — 개별 처리, 인접 호출: INSTANCE.hide, PixelScene.renderTextBlock
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java#L71) `public void hide() {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.landscape
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java#L78) `private void fillFields(Heap heap ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.landscape
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java#L88) `private void fillFields( Item item ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.landscape
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java#L105) `private void layoutFields(IconTitle title, RenderedTextBlock info){` — 개별 처리, 인접 호출: PixelScene.landscape

## 1196. [`WndInfoMob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 94행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java#L34) `public class WndInfoMob extends WndTitledMessage {`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java#L42) `private static class MobTitle extends Component {`

### 변수·상수 후보
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java#L44) `private static final int GAP	= 2;`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java#L46) `private CharSprite image;`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java#L47) `private RenderedTextBlock name;`
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java#L48) `private HealthBar health;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java#L49) `private BuffIndicator buffs;`

### 메서드 및 코드 의존 단서
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java#L36) `public WndInfoMob( Mob mob ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, Char.hasProp, Math.max
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java#L51) `public MobTitle( Mob mob ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.titleCase, Char.hasProp, Math.max
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java#L69) `protected void layout() {` — 개별 처리, 인접 호출: Math.max

## 1197. [`WndInfoPlant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoPlant.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 38행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoPlant.java#L29) `public class WndInfoPlant extends WndTitledMessage {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoPlant.java#L31) `public WndInfoPlant( Plant plant ) {` — 개별 처리, 인접 호출: TerrainFeaturesTilemap.tile, Messages.titleCase

## 1198. [`WndInfoSubclass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoSubclass.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 58행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoSubclass.java#L35) `public class WndInfoSubclass extends WndTitledMessage {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoSubclass.java#L37) `public WndInfoSubclass(HeroClass cls, HeroSubClass subCls){` — 개별 처리, 인접 호출: Messages.titleCase, Talent.initClassTalents, Talent.initSubclassTalents, TalentsPane.TalentTierPane, Messages.get
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoSubclass.java#L53) `protected float targetHeight() {` — 개별 처리

## 1199. [`WndInfoTalent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTalent.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 103행.

### 클래스/타입
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTalent.java#L35) `public class WndInfoTalent extends Window {`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTalent.java#L92) `public static abstract class TalentButtonCallback implements Callback {`

### 변수·상수 후보
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTalent.java#L37) `private static final float GAP	= 2;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTalent.java#L39) `private static final int WIDTH_MIN = 120;`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTalent.java#L40) `private static final int WIDTH_MAX = 220;`

### 메서드 및 코드 의존 단서
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTalent.java#L42) `public WndInfoTalent(Talent talent, int points, TalentButtonCallback buttonCallback){` — 개별 처리, 인접 호출: Messages.titleCase, PixelScene.renderTextBlock, PixelScene.landscape, Icons.get
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTalent.java#L78) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Icons.get
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTalent.java#L94) `public abstract String prompt();` — 개별 처리
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTalent.java#L96) `public boolean metamorphDesc(){` — 개별 처리

## 1200. [`WndInfoTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTrap.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 40행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTrap.java#L29) `public class WndInfoTrap extends WndTitledMessage {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTrap.java#L31) `public WndInfoTrap(Trap trap) {` — 개별 처리, 인접 호출: TerrainFeaturesTilemap.tile, Messages.titleCase

## 1201. [`WndJournal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 1157행.

### 클래스/타입
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L88) `public class WndJournal extends WndTabbed {`
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L236) `public static class GuideTab extends Component {`
- [L287](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L287) `public static class AlchemyTab extends Component {`
- [L474](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L474) `private static class NotesTab extends Component {`
- [L568](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L568) `public static class CatalogTab extends Component{`
- [L1071](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1071) `public static class BadgesTab extends Component {`

### 변수·상수 후보
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L90) `public static final int WIDTH_P     = 126;`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L91) `public static final int HEIGHT_P    = 180;`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L93) `public static final int WIDTH_L     = 216;`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L94) `public static final int HEIGHT_L    = 130;`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L96) `private static final int ITEM_HEIGHT	= 18;`
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L98) `private GuideTab guideTab;`
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L99) `private AlchemyTab alchemyTab;`
- [L100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L100) `private NotesTab notesTab;`
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L101) `private CatalogTab catalogTab;`
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L102) `private BadgesTab badgesTab;`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L104) `public static int last_index = 0;`
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L106) `private static WndJournal INSTANCE = null;`
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L238) `private ScrollingListPane list;`
- [L289](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L289) `private RedButton[] pageButtons;`
- [L290](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L290) `private static final int NUM_BUTTONS = 9;`
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L304) `public static int currentPageIdx   = 0;`
- [L306](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L306) `private IconTitle title;`
- [L307](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L307) `private RenderedTextBlock body;`
- [L309](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L309) `private ScrollPane list;`
- [L316](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L316) `final int idx = i;`
- [L476](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L476) `private ScrollingGridPane grid;`
- [L477](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L477) `private CustomNoteButton custom;`
- [L570](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L570) `private RedButton[] itemButtons;`
- [L571](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L571) `private static final int NUM_BUTTONS = 4;`
- [L573](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L573) `public static int currentItemIdx   = 0;`
- [L574](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L574) `private static float[] scrollPositions = new float[NUM_BUTTONS];`
- [L577](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L577) `private static final int EQUIP_IDX = 0;`
- [L578](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L578) `private static final int CONSUM_IDX = 1;`
- [L579](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L579) `private static final int BESTIARY_IDX = 2;`
- [L580](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L580) `private static final int LORE_IDX = 3;`
- [L582](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L582) `private ScrollingGridPane grid;`
- [L588](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L588) `final int idx = i;`
- [L1073](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1073) `private RedButton btnLocal;`
- [L1074](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1074) `private RedButton btnGlobal;`
- [L1076](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1076) `private RenderedTextBlock title;`
- [L1078](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1078) `private Component badgesLocal;`
- [L1079](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1079) `private Component badgesGlobal;`
- [L1081](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1081) `public static boolean global = false;`

### 메서드 및 코드 의존 단서
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L108) `public WndJournal(){` — 개별 처리, 인접 호출: INSTANCE.hide, PixelScene.landscape, JOURNAL.get
- [L145](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L145) `protected void select( boolean value ) {` — 개별 처리, 인접 호출: Messages.get, ALCHEMY.get, CATALOG.get
- [L152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L152) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, ALCHEMY.get, CATALOG.get, BADGES.get
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L157) `protected void select( boolean value ) {` — 개별 처리, 인접 호출: Messages.get, ALCHEMY.get, CATALOG.get, BADGES.get
- [L164](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L164) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, ALCHEMY.get, CATALOG.get, BADGES.get
- [L169](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L169) `protected void select( boolean value ) {` — 개별 처리, 인접 호출: Messages.get, CATALOG.get, BADGES.get
- [L176](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L176) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, CATALOG.get, BADGES.get, KeyBindings.getActionForKey
- [L181](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L181) `protected void select( boolean value ) {` — 개별 처리, 인접 호출: Messages.get, BADGES.get, KeyBindings.getActionForKey
- [L188](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L188) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, BADGES.get, KeyBindings.getActionForKey
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L193) `protected void select( boolean value ) {` — 개별 처리, 인접 호출: Messages.get, KeyBindings.getActionForKey
- [L200](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L200) `protected String hoverText() {` — 개별 처리, 인접 호출: Messages.get, KeyBindings.getActionForKey
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L218) `public boolean onSignal(KeyEvent event) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getActionForKey, ADVENTURERS_GUIDE.title, ADVENTURERS_GUIDE.pageNames, ADVENTURERS_GUIDE.isPageFound, ScrollingListPane.ListItem, ADVENTURERS_GUIDE.pageSprite, Messages.titleCase
- [L228](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L228) `public void offset(int xOffset, int yOffset) {` — 개별 처리, 인접 호출: ADVENTURERS_GUIDE.title, ADVENTURERS_GUIDE.pageNames, ADVENTURERS_GUIDE.isPageFound, ScrollingListPane.ListItem, ADVENTURERS_GUIDE.pageSprite, Messages.titleCase, ADVENTURERS_GUIDE.pageTitle
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L241) `protected void createChildren() {` — 생성·초기화, 인접 호출: ADVENTURERS_GUIDE.title, ADVENTURERS_GUIDE.pageNames, ADVENTURERS_GUIDE.isPageFound, ScrollingListPane.ListItem, ADVENTURERS_GUIDE.pageSprite, Messages.titleCase, ADVENTURERS_GUIDE.pageTitle
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L247) `protected void layout() {` — 개별 처리, 인접 호출: ADVENTURERS_GUIDE.title, ADVENTURERS_GUIDE.pageNames, ADVENTURERS_GUIDE.isPageFound, ScrollingListPane.ListItem, ADVENTURERS_GUIDE.pageSprite, Messages.titleCase, ADVENTURERS_GUIDE.pageTitle
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L252) `public void updateList(){` — 행동·상태 갱신, 인접 호출: ADVENTURERS_GUIDE.title, ADVENTURERS_GUIDE.pageNames, ADVENTURERS_GUIDE.isPageFound, ScrollingListPane.ListItem, ADVENTURERS_GUIDE.pageSprite, Messages.titleCase, ADVENTURERS_GUIDE.pageTitle
- [L263](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L263) `public boolean onClick(float x, float y) {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, ADVENTURERS_GUIDE.pageSprite, ADVENTURERS_GUIDE.pageTitle, ADVENTURERS_GUIDE.pageBody, ADVENTURERS_GUIDE.readPage
- [L313](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L313) `protected void createChildren() {` — 생성·초기화, 인접 호출: ALCHEMY_GUIDE.isPageFound, PixelScene.renderTextBlock, PixelScene.align
- [L319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L319) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ALCHEMY_GUIDE.isPageFound, PixelScene.renderTextBlock, PixelScene.align
- [L344](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L344) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, ALCHEMY_GUIDE.isPageFound
- [L376](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L376) `public void updateList() {` — 행동·상태 갱신, 인접 호출: ALCHEMY_GUIDE.isPageFound, ALCHEMY_GUIDE.pageTitle, ALCHEMY_GUIDE.pageBody, ALCHEMY_GUIDE.readPage, QuickRecipe.getRecipes
- [L480](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L480) `protected void createChildren() {` — 생성·초기화, 인접 호출: Messages.get, Notes.getRecords, Notes.customRecordLimit, ScrollingGridPane.GridItem, GameScene.show, CustomNoteButton.CustomNoteWindow
- [L486](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L486) `protected void layout() {` — 개별 처리, 인접 호출: Messages.get, Notes.getRecords, Notes.customRecordLimit, ScrollingGridPane.GridItem, GameScene.show, CustomNoteButton.CustomNoteWindow
- [L491](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L491) `private void updateList(){` — 행동·상태 갱신, 인접 호출: Messages.get, Notes.getRecords, Notes.customRecordLimit, ScrollingGridPane.GridItem, GameScene.show, CustomNoteButton.CustomNoteWindow
- [L505](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L505) `public boolean onClick(float x, float y) {` — 이벤트·효과 실행, 인접 호출: GameScene.show, CustomNoteButton.CustomNoteWindow, Notes.getRecords, Messages.get, ScrollingGridPane.GridItem, Messages.titleCase
- [L537](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L537) `public boolean onClick(float x, float y) {` — 이벤트·효과 실행, 인접 호출: GameScene.show, Messages.titleCase
- [L585](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L585) `protected void createChildren() {` — 생성·초기화, 인접 호출: PixelScene.align
- [L591](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L591) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: PixelScene.align
- [L605](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L605) `public synchronized void update() {` — 행동·상태 갱신, 인접 호출: PixelScene.align
- [L614](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L614) `protected void layout() {` — 개별 처리, 인접 호출: PixelScene.align, Messages.get, Messages.titleCase
- [L633](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L633) `public void updateList() {` — 행동·상태 갱신, 인접 호출: Messages.get, Messages.titleCase
- [L746](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L746) `private static void addGridItems( ScrollingGridPane grid, Collection<Class<?>> classes) {` — 개별 처리, 인접 호출: Catalog.isSeen, Reflection.newInstance, Messages.get, Messages.titleCase, Catalog.useCount
- [L852](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L852) `public boolean onClick(float x, float y) {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, GameScene.show, Bestiary.isSeen, Reflection.newInstance
- [L877](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L877) `private static void addGridEntities(ScrollingGridPane grid, Collection<Class<?>> classes) {` — 개별 처리, 인접 호출: Bestiary.isSeen, Reflection.newInstance, Messages.titleCase, Bestiary.encounterCount, Messages.get
- [L986](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L986) `public boolean onClick(float x, float y) {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, GameScene.show, ScrollingGridPane.GridItem
- [L1014](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1014) `private static void addGridDocuments( ScrollingGridPane grid, Document doc ){` — 개별 처리, 인접 호출: ScrollingGridPane.GridItem, ShatteredPixelDungeon.scene, GameScene.show, Messages.get, Integer.toString
- [L1028](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1028) `public boolean onClick(float x, float y) {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, GameScene.show, Messages.get, Integer.toString
- [L1084](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1084) `protected void createChildren() {` — 생성·초기화, 인접 호출: Messages.get, BADGES.get, Badges.filterReplacedBadges, PixelScene.renderTextBlock
- [L1089](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1089) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: BADGES.get, Messages.get, Badges.filterReplacedBadges, PixelScene.renderTextBlock
- [L1100](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1100) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: BADGES.get, Badges.filterReplacedBadges, PixelScene.renderTextBlock, Messages.get
- [L1126](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1126) `protected void layout() {` — 개별 처리
- [L1142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java#L1142) `private void updateList(){` — 행동·상태 갱신

## 1202. [`WndJournalItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournalItem.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 46행.

### 클래스/타입
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournalItem.java#L29) `public class WndJournalItem extends WndTitledMessage {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournalItem.java#L31) `public WndJournalItem(Image icon, String title, String message ) {` — 개별 처리
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournalItem.java#L36) `protected void onClick( PointerEvent event ) {` — 이벤트·효과 실행

## 1203. [`WndKeyBindings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 558행.

### 클래스/타입
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L45) `public class WndKeyBindings extends Window {`
- [L227](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L227) `private class BindingItem extends Component {`
- [L381](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L381) `private class WndChangeBinding extends Window {`

### 변수·상수 후보
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L47) `private static final int WIDTH = 135;`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L49) `private static final int BTN_HEIGHT = 16;`
- [L51](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L51) `private static final int COL1_CENTER = WIDTH/5;`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L52) `private static final int COL2_CENTER = 5*WIDTH/10;`
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L53) `private static final int COL3_CENTER = 7*WIDTH/10;`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L54) `private static final int COL4_CENTER = 9*WIDTH/10;`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L56) `private Component bindingsList;`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L59) `private LinkedHashMap<Integer, GameAction> changedBindings;`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L61) `private static boolean controller = false;`
- [L229](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L229) `private static final int HEIGHT = 13;`
- [L231](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L231) `private static final int CHANGED = TITLE_COLOR;`
- [L232](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L232) `private static final int DEFAULT = 0xFFFFFF;`
- [L233](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L233) `private static final int UNBOUND = 0x888888;`
- [L234](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L234) `private static final int UNBOUND_CHANGED = 0x888822;`
- [L236](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L236) `private GameAction gameAction;`
- [L237](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L237) `private int key1;`
- [L238](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L238) `private int key2;`
- [L239](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L239) `private int key3;`
- [L241](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L241) `private int origKey1;`
- [L242](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L242) `private int origKey2;`
- [L243](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L243) `private int origKey3;`
- [L245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L245) `private RenderedTextBlock actionName;`
- [L246](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L246) `private RenderedTextBlock key1Name;`
- [L247](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L247) `private RenderedTextBlock key2Name;`
- [L248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L248) `private RenderedTextBlock key3Name;`
- [L250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L250) `private ColorBlock sep1;`
- [L251](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L251) `private ColorBlock sep2;`
- [L252](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L252) `private ColorBlock sep3;`
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L253) `private ColorBlock sep4;`
- [L383](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L383) `private int curKeyCode;`
- [L384](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L384) `private int otherBoundKey1;`
- [L385](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L385) `private int otherBoundKey2;`
- [L386](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L386) `private int changedKeyCode = -1;`
- [L388](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L388) `private BindingItem changedAction;`
- [L389](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L389) `private RenderedTextBlock changedKey;`
- [L390](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L390) `private RenderedTextBlock warnErr;`
- [L392](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L392) `private RedButton btnUnbind;`
- [L393](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L393) `private RedButton btnConfirm;`
- [L394](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L394) `private RedButton btnCancel;`

### 메서드 및 코드 의존 단서
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L63) `public WndKeyBindings(Boolean controller) {` — 개별 처리, 인접 호출: KeyBindings.getAllControllerBindings, KeyBindings.getAllBindings, PixelScene.renderTextBlock, Messages.get
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L111) `public void onClick(float x, float y) {` — 이벤트·효과 실행, 인접 호출: PixelScene.renderTextBlock, Messages.get, SPDAction.getControllerDefaults, SPDAction.getDefaults, GameAction.allActions
- [L171](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L171) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: SPDAction.getControllerDefaults, SPDAction.getDefaults, Messages.get, KeyBindings.setAllControllerBindings, KeyBindings.setAllBindings, SPDAction.saveBindings
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L193) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: KeyBindings.setAllControllerBindings, KeyBindings.setAllBindings, SPDAction.saveBindings, Messages.get
- [L205](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L205) `protected void onClick() {` — 이벤트·효과 실행
- [L217](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L217) `public void offset(int xOffset, int yOffset) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.get
- [L223](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L223) `public void onBackPressed() {` — 이벤트·효과 실행, 인접 호출: PixelScene.renderTextBlock, Messages.get, KeyBindings.getControllerKeysForAction, KeyBindings.getKeyboardKeysForAction
- [L255](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L255) `public BindingItem( GameAction action ){` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.get, KeyBindings.getControllerKeysForAction, KeyBindings.getKeyboardKeysForAction, KeyBindings.getKeyName
- [L297](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L297) `public void updateBindings(int first, int second, int third){` — 행동·상태 갱신, 인접 호출: KeyBindings.getKeyName
- [L327](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L327) `protected void layout() {` — 개별 처리, 인접 호출: ShatteredPixelDungeon.scene
- [L357](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L357) `private boolean onClick( float x, float y ){` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L396) `public WndChangeBinding(GameAction action, BindingItem listItem, int keyAssigning, int curKeyCode, int otherBoundKey1, int otherBoundKe` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, Messages.get, KeyBindings.getKeyName, ShatteredPixelDungeon.scene
- [L431](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L431) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: ShatteredPixelDungeon.scene, Messages.get
- [L444](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L444) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Messages.get
- [L489](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L489) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getActionForKey, PointerEvent.currentHoverPos, ControllerHandler.icControllerKey, KeyEvent.isKeyboardKey, Messages.get, KeyBindings.getKeyName
- [L502](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L502) `public boolean onSignal(KeyEvent event) {` — 이벤트·효과 실행, 인접 호출: KeyBindings.getActionForKey, PointerEvent.currentHoverPos, ControllerHandler.icControllerKey, KeyEvent.isKeyboardKey, Messages.get, KeyBindings.getKeyName
- [L551](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java#L551) `public void destroy() {` — 개별 처리

## 1204. [`WndList.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndList.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 63행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndList.java#L28) `public class WndList extends Window {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndList.java#L30) `private static final int WIDTH	= 120;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndList.java#L31) `private static final int MARGIN	= 4;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndList.java#L32) `private static final int GAP	= 4;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndList.java#L34) `public WndList( String[] items ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock

## 1205. [`WndMessage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMessage.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 57행.

### 클래스/타입
- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMessage.java#L28) `public class WndMessage extends Window {`

### 변수·상수 후보
- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMessage.java#L30) `private static final int WIDTH_MIN = 120;`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMessage.java#L31) `private static final int WIDTH_MAX = 220;`
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMessage.java#L32) `private static final int MARGIN = 4;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMessage.java#L34) `public WndMessage( String text ) {` — 개별 처리, 인접 호출: PixelScene.renderTextBlock, PixelScene.landscape

## 1206. [`WndMonkAbilities.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMonkAbilities.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 99행.

### 클래스/타입
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMonkAbilities.java#L34) `public class WndMonkAbilities extends Window {`

### 변수·상수 후보
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMonkAbilities.java#L36) `private static final int WIDTH_P = 120;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMonkAbilities.java#L37) `private static final int WIDTH_L = 180;`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMonkAbilities.java#L39) `private static final int MARGIN  = 2;`

### 메서드 및 코드 의존 단서
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMonkAbilities.java#L41) `public WndMonkAbilities( MonkEnergy energyBuff ){` — 개별 처리, 인접 호출: PixelScene.landscape, PixelScene.renderTextBlock, Messages.titleCase, Messages.get, GameScene.selectCell, CellSelector.Listener
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMonkAbilities.java#L59) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: GameScene.selectCell, CellSelector.Listener
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMonkAbilities.java#L85) `private CellSelector.Listener listener = new CellSelector.Listener() {` — 개별 처리
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMonkAbilities.java#L88) `public void onSelect(Integer cell) {` — 이벤트·효과 실행
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMonkAbilities.java#L93) `public String prompt() {` — 개별 처리

## 1207. [`WndOptions.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 141행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L32) `public class WndOptions extends Window {`

### 변수·상수 후보
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L34) `protected static final int WIDTH_P = 120;`
- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L35) `protected static final int WIDTH_L = 144;`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L37) `protected static final int MARGIN 		= 2;`
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L38) `protected static final int BUTTON_HEIGHT	= 18;`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L87) `final int index = i;`

### 메서드 및 코드 의존 단서
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L40) `public WndOptions(Image icon, String title, String message, String... options) {` — 개별 처리, 인접 호출: PixelScene.landscape, PixelScene.renderTextBlock
- [L57](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L57) `public WndOptions( String title, String message, String... options ) {` — 개별 처리, 인접 호출: PixelScene.landscape, PixelScene.renderTextBlock
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L76) `protected void layoutBody(float pos, String message, String... options){` — 개별 처리, 인접 호출: PixelScene.landscape, PixelScene.renderTextBlock, Icons.get
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L90) `protected void onClick() {` — 이벤트·효과 실행, 인접 호출: Icons.get
- [L105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L105) `protected void onClick() {` — 이벤트·효과 실행
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L121) `protected boolean enabled( int index ){` — 개별 처리
- [L125](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L125) `protected void onSelect( int index ) {}` — 이벤트·효과 실행
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L127) `protected boolean hasInfo( int index ) {` — 조회·판정
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L131) `protected void onInfo( int index ) {}` — 이벤트·효과 실행
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L133) `protected boolean hasIcon( int index ) {` — 조회·판정
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java#L137) `protected Image getIcon( int index ) {` — 조회·판정

## 1208. [`WndOptionsCondensed.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptionsCondensed.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 164행.

### 클래스/타입
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptionsCondensed.java#L32) `public class WndOptionsCondensed extends WndOptions {`

### 변수·상수 후보
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptionsCondensed.java#L56) `final int index = i;`

### 메서드 및 코드 의존 단서
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptionsCondensed.java#L34) `public WndOptionsCondensed(Image icon, String title, String message, String... options) {` — 개별 처리, 인접 호출: PixelScene.landscape, PixelScene.renderTextBlock
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptionsCondensed.java#L38) `public WndOptionsCondensed( String title, String message, String... options ) {` — 개별 처리, 인접 호출: PixelScene.landscape, PixelScene.renderTextBlock
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptionsCondensed.java#L43) `protected void layoutBody(float pos, String message, String... options) {` — 개별 처리, 인접 호출: PixelScene.landscape, PixelScene.renderTextBlock
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptionsCondensed.java#L59) `protected void onClick() {` — 이벤트·효과 실행
- [L160](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptionsCondensed.java#L160) `protected boolean hasInfo(int index) {` — 조회·판정

## 1209. [`WndQuest.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuest.java)

패키지 `com.shatteredpixel.shatteredpixeldungeon.windows`, 33행.

### 클래스/타입
- [L27](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuest.java#L27) `public class WndQuest extends WndTitledMessage {`

### 변수·상수 후보
- 없음

### 메서드 및 코드 의존 단서
- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuest.java#L29) `public WndQuest( NPC questgiver, String text ) {` — 개별 처리, 인접 호출: Messages.titleCase


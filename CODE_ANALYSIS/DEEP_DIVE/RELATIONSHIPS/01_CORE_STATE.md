# 파일 연결 관계 — 공통 게임 상태 및 설정

기준 코드 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 아래 **확정된 import 연결**은 Java 소스의 import 문을 같은 저장소 내 `.java` 경로로 실제 대응시킨 정적 컴파일 의존이다. import는 실제 실행 시 메서드 호출의 증거가 아니다. Java 기본 라이브러리 및 외부 모듈의 import는 별도로 개수 표시. 정적 import의 소속 클래스도 역추적한다. 같은 패키지 참조나 완전한 한정 이름은 미포함될 수 있다.

## [`ShatteredPixelDungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `ShatteredPixelDungeon` extends `Game `
- import: 전체 9개, 저장소 내부로 경로 확인 0개, 외부/표준 0개, 내부 이름이지만 경로 미확인 9개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.shatteredpixel.shatteredpixeldungeon.scenes.GameScene`, `com.shatteredpixel.shatteredpixeldungeon.scenes.PixelScene`, `com.shatteredpixel.shatteredpixeldungeon.scenes.TitleScene`, `com.shatteredpixel.shatteredpixeldungeon.scenes.WelcomeScene`, `com.watabou.noosa.Game`, `com.watabou.noosa.audio.Music`, `com.watabou.noosa.audio.Sample`, `com.watabou.utils.DeviceCompat`, `com.watabou.utils.PlatformSupport`

## [`Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `Dungeon`; `LimitedDrops`
- import: 전체 74개, 저장소 내부로 경로 확인 0개, 외부/표준 8개, 내부 이름이지만 경로 미확인 66개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.shatteredpixel.shatteredpixeldungeon.actors.Actor`, `com.shatteredpixel.shatteredpixeldungeon.actors.Char`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.Amok`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.AscensionChallenge`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.Awareness`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.Dread`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.Light`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.MagicalSight`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.MindVision`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.RevealedArea`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.Terror`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.Hero`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.Talent`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.cleric.PowerOfMany`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.huntress.SpiritHawk`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells.DivineSense`, `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.Mimic`, `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.Mob`, `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs.Blacksmith`, `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs.Ghost`, `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs.Imp`, `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.npcs.Wandmaker`, `com.shatteredpixel.shatteredpixeldungeon.items.Amulet`, `com.shatteredpixel.shatteredpixeldungeon.items.Generator`, `com.shatteredpixel.shatteredpixeldungeon.items.Heap`, `com.shatteredpixel.shatteredpixeldungeon.items.Item`, `com.shatteredpixel.shatteredpixeldungeon.items.artifacts.TalismanOfForesight`, `com.shatteredpixel.shatteredpixeldungeon.items.potions.Potion`, `com.shatteredpixel.shatteredpixeldungeon.items.rings.Ring`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.Scroll`, `com.shatteredpixel.shatteredpixeldungeon.items.wands.WandOfRegrowth`, `com.shatteredpixel.shatteredpixeldungeon.items.wands.WandOfWarding`, `com.shatteredpixel.shatteredpixeldungeon.journal.Notes`, `com.shatteredpixel.shatteredpixeldungeon.levels.CavesBossLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.CavesLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.CityBossLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.CityLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.DeadEndLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.HallsBossLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.HallsLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.LastLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.Level`, `com.shatteredpixel.shatteredpixeldungeon.levels.MiningLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.PrisonBossLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.PrisonLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.RegularLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.SewerBossLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.SewerLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.VaultLevel`, `com.shatteredpixel.shatteredpixeldungeon.levels.features.LevelTransition`, `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.secret.SecretRoom`, `com.shatteredpixel.shatteredpixeldungeon.levels.rooms.special.SpecialRoom`, `com.shatteredpixel.shatteredpixeldungeon.messages.Messages`, `com.shatteredpixel.shatteredpixeldungeon.scenes.GameScene`, `com.shatteredpixel.shatteredpixeldungeon.ui.QuickSlotButton`, `com.shatteredpixel.shatteredpixeldungeon.ui.Toolbar`, `com.shatteredpixel.shatteredpixeldungeon.utils.DungeonSeed`, `com.shatteredpixel.shatteredpixeldungeon.windows.WndResurrect`, `com.watabou.noosa.Game`, `com.watabou.utils.BArray`, `com.watabou.utils.Bundlable`, `com.watabou.utils.Bundle`, `com.watabou.utils.FileUtils`, `com.watabou.utils.PathFinder`, `com.watabou.utils.Random`, `com.watabou.utils.SparseArray`

## [`GamesInProgress.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `GamesInProgress`; `Info`
- import: 전체 10개, 저장소 내부로 경로 확인 0개, 외부/표준 5개, 내부 이름이지만 경로 미확인 5개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.shatteredpixel.shatteredpixeldungeon.actors.hero.HeroClass`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.HeroSubClass`, `com.shatteredpixel.shatteredpixeldungeon.messages.Messages`, `com.watabou.utils.Bundle`, `com.watabou.utils.FileUtils`

## [`Statistics.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `Statistics`
- import: 전체 4개, 저장소 내부로 경로 확인 0개, 외부/표준 2개, 내부 이름이지만 경로 미확인 2개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.watabou.utils.Bundle`, `com.watabou.utils.SparseArray`

## [`Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `Rankings`; `Record` implements `Bundlable `
- import: 전체 36개, 저장소 내부로 경로 확인 0개, 외부/표준 12개, 내부 이름이지만 경로 미확인 24개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.shatteredpixel.shatteredpixeldungeon.actors.Actor`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.Buff`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.Belongings`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.Hero`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.HeroClass`, `com.shatteredpixel.shatteredpixeldungeon.items.Generator`, `com.shatteredpixel.shatteredpixeldungeon.items.Item`, `com.shatteredpixel.shatteredpixeldungeon.items.bags.Bag`, `com.shatteredpixel.shatteredpixeldungeon.items.potions.Potion`, `com.shatteredpixel.shatteredpixeldungeon.items.quest.CorpseDust`, `com.shatteredpixel.shatteredpixeldungeon.items.quest.EscapeCrystal`, `com.shatteredpixel.shatteredpixeldungeon.items.rings.Ring`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.Scroll`, `com.shatteredpixel.shatteredpixeldungeon.items.trinkets.Trinket`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee.MeleeWeapon`, `com.shatteredpixel.shatteredpixeldungeon.journal.Notes`, `com.shatteredpixel.shatteredpixeldungeon.messages.Messages`, `com.shatteredpixel.shatteredpixeldungeon.ui.QuickSlotButton`, `com.shatteredpixel.shatteredpixeldungeon.ui.Toolbar`, `com.shatteredpixel.shatteredpixeldungeon.utils.DungeonSeed`, `com.watabou.noosa.Game`, `com.watabou.utils.Bundlable`, `com.watabou.utils.Bundle`, `com.watabou.utils.FileUtils`

## [`SPDSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `SPDSettings` extends `GameSettings `
- import: 전체 10개, 저장소 내부로 경로 확인 0개, 외부/표준 1개, 내부 이름이지만 경로 미확인 9개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.shatteredpixel.shatteredpixeldungeon.messages.Languages`, `com.shatteredpixel.shatteredpixeldungeon.scenes.GameScene`, `com.shatteredpixel.shatteredpixeldungeon.scenes.PixelScene`, `com.watabou.noosa.Game`, `com.watabou.noosa.audio.Music`, `com.watabou.noosa.audio.Sample`, `com.watabou.utils.DeviceCompat`, `com.watabou.utils.GameSettings`, `com.watabou.utils.Point`

## [`SPDAction.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `SPDAction` extends `GameAction `
- import: 전체 9개, 저장소 내부로 경로 확인 0개, 외부/표준 3개, 내부 이름이지만 경로 미확인 6개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.watabou.input.ControllerHandler`, `com.watabou.input.GameAction`, `com.watabou.input.KeyBindings`, `com.watabou.input.KeyEvent`, `com.watabou.utils.Bundle`, `com.watabou.utils.FileUtils`

## [`Assets.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `Assets`; `Effects`; `Environment`; `Fonts`; `Interfaces`; `Messages`; `Music`; `Sounds`
- import: 전체 0개, 저장소 내부로 경로 확인 0개, 외부/표준 0개

**내부 import:** 발견되지 않음

## [`Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `Badges`; `BadgeType`; `Badge`
- import: 전체 32개, 저장소 내부로 경로 확인 0개, 외부/표준 9개, 내부 이름이지만 경로 미확인 23개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.AscensionChallenge`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.HeroClass`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.HeroSubClass`, `com.shatteredpixel.shatteredpixeldungeon.items.Item`, `com.shatteredpixel.shatteredpixeldungeon.items.artifacts.Artifact`, `com.shatteredpixel.shatteredpixeldungeon.items.bags.MagicalHolster`, `com.shatteredpixel.shatteredpixeldungeon.items.bags.PotionBandolier`, `com.shatteredpixel.shatteredpixeldungeon.items.bags.ScrollHolder`, `com.shatteredpixel.shatteredpixeldungeon.items.bags.VelvetPouch`, `com.shatteredpixel.shatteredpixeldungeon.items.potions.Potion`, `com.shatteredpixel.shatteredpixeldungeon.items.quest.Pickaxe`, `com.shatteredpixel.shatteredpixeldungeon.items.remains.RemainsItem`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.Scroll`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.curses.Explosive`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee.MeleeWeapon`, `com.shatteredpixel.shatteredpixeldungeon.journal.Bestiary`, `com.shatteredpixel.shatteredpixeldungeon.journal.Catalog`, `com.shatteredpixel.shatteredpixeldungeon.journal.Document`, `com.shatteredpixel.shatteredpixeldungeon.messages.Messages`, `com.shatteredpixel.shatteredpixeldungeon.scenes.PixelScene`, `com.shatteredpixel.shatteredpixeldungeon.utils.GLog`, `com.watabou.utils.Bundle`, `com.watabou.utils.FileUtils`

## [`Challenges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `Challenges`
- import: 전체 2개, 저장소 내부로 경로 확인 0개, 외부/표준 0개, 내부 이름이지만 경로 미확인 2개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.shatteredpixel.shatteredpixeldungeon.items.Dewdrop`, `com.shatteredpixel.shatteredpixeldungeon.items.Item`

## [`Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `Bones`
- import: 전체 15개, 저장소 내부로 경로 확인 0개, 외부/표준 3개, 내부 이름이지만 경로 미확인 12개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.shatteredpixel.shatteredpixeldungeon.actors.hero.Hero`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.HeroClass`, `com.shatteredpixel.shatteredpixeldungeon.items.Generator`, `com.shatteredpixel.shatteredpixeldungeon.items.Gold`, `com.shatteredpixel.shatteredpixeldungeon.items.Item`, `com.shatteredpixel.shatteredpixeldungeon.items.artifacts.Artifact`, `com.shatteredpixel.shatteredpixeldungeon.items.remains.RemainsItem`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.MissileWeapon`, `com.watabou.utils.Bundle`, `com.watabou.utils.FileUtils`, `com.watabou.utils.Random`, `com.watabou.utils.Reflection`

## [`Chrome.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Chrome.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `Chrome`; `Type`
- import: 전체 1개, 저장소 내부로 경로 확인 0개, 외부/표준 0개, 내부 이름이지만 경로 미확인 1개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.watabou.noosa.NinePatch`

## [`QuickSlot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon`
- 주요 선언: `QuickSlot`
- import: 전체 6개, 저장소 내부로 경로 확인 0개, 외부/표준 2개, 내부 이름이지만 경로 미확인 4개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.shatteredpixel.shatteredpixeldungeon.items.Item`, `com.watabou.utils.Bundlable`, `com.watabou.utils.Bundle`, `com.watabou.utils.Random`

## [`actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero`
- 주요 선언: `HeroClass`
- import: 전체 60개, 저장소 내부로 경로 확인 0개, 외부/표준 0개, 내부 이름이지만 경로 미확인 60개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.shatteredpixel.shatteredpixeldungeon.Assets`, `com.shatteredpixel.shatteredpixeldungeon.Badges`, `com.shatteredpixel.shatteredpixeldungeon.Challenges`, `com.shatteredpixel.shatteredpixeldungeon.Dungeon`, `com.shatteredpixel.shatteredpixeldungeon.QuickSlot`, `com.shatteredpixel.shatteredpixeldungeon.SPDSettings`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.ArmorAbility`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.cleric.AscendedForm`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.cleric.PowerOfMany`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.cleric.Trinity`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.duelist.Challenge`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.duelist.ElementalStrike`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.duelist.Feint`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.huntress.NaturesPower`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.huntress.SpectralBlades`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.huntress.SpiritHawk`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.mage.ElementalBlast`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.mage.WarpBeacon`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.mage.WildMagic`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.rogue.DeathMark`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.rogue.ShadowClone`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.rogue.SmokeBomb`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.warrior.Endure`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.warrior.HeroicLeap`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.warrior.Shockwave`, `com.shatteredpixel.shatteredpixeldungeon.items.BrokenSeal`, `com.shatteredpixel.shatteredpixeldungeon.items.Item`, `com.shatteredpixel.shatteredpixeldungeon.items.Waterskin`, `com.shatteredpixel.shatteredpixeldungeon.items.armor.ClothArmor`, `com.shatteredpixel.shatteredpixeldungeon.items.artifacts.CloakOfShadows`, `com.shatteredpixel.shatteredpixeldungeon.items.artifacts.HolyTome`, `com.shatteredpixel.shatteredpixeldungeon.items.bags.VelvetPouch`, `com.shatteredpixel.shatteredpixeldungeon.items.food.Food`, `com.shatteredpixel.shatteredpixeldungeon.items.potions.PotionOfHealing`, `com.shatteredpixel.shatteredpixeldungeon.items.potions.PotionOfInvisibility`, `com.shatteredpixel.shatteredpixeldungeon.items.potions.PotionOfLiquidFlame`, `com.shatteredpixel.shatteredpixeldungeon.items.potions.PotionOfMindVision`, `com.shatteredpixel.shatteredpixeldungeon.items.potions.PotionOfPurity`, `com.shatteredpixel.shatteredpixeldungeon.items.potions.PotionOfStrength`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.ScrollOfIdentify`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.ScrollOfLullaby`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.ScrollOfMagicMapping`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.ScrollOfMirrorImage`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.ScrollOfRage`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.ScrollOfRemoveCurse`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.ScrollOfUpgrade`, `com.shatteredpixel.shatteredpixeldungeon.items.wands.WandOfMagicMissile`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.SpiritBow`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee.Cudgel`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee.Dagger`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee.Gloves`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee.MagesStaff`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee.Rapier`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee.WornShortsword`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.ThrowingKnife`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.ThrowingSpike`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.ThrowingStone`, `com.shatteredpixel.shatteredpixeldungeon.journal.Catalog`, `com.shatteredpixel.shatteredpixeldungeon.messages.Messages`, `com.watabou.utils.DeviceCompat`

## [`actors/hero/HeroSubClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero`
- 주요 선언: `HeroSubClass`
- import: 전체 6개, 저장소 내부로 경로 확인 0개, 외부/표준 0개, 내부 이름이지만 경로 미확인 6개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.shatteredpixel.shatteredpixeldungeon.Dungeon`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee.MagesStaff`, `com.shatteredpixel.shatteredpixeldungeon.messages.Messages`, `com.shatteredpixel.shatteredpixeldungeon.scenes.GameScene`, `com.shatteredpixel.shatteredpixeldungeon.ui.HeroIcon`, `com.watabou.noosa.Game`

## [`actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)

- 패키지: `com.shatteredpixel.shatteredpixeldungeon.actors.hero`
- 주요 선언: `Talent`; `ImprovisedProjectileCooldown` extends `FlavourBuff`; `LethalMomentumTracker` extends `FlavourBuff`; `StrikingWaveTracker` extends `FlavourBuff`; `WandPreservationCounter` extends `CounterBuff`; `EmpoweredStrikeTracker` extends `FlavourBuff`; `ProtectiveShadowsTracker` extends `Buff `; `BountyHunterTracker` extends `FlavourBuff`
- import: 전체 70개, 저장소 내부로 경로 확인 0개, 외부/표준 5개, 내부 이름이지만 경로 미확인 65개

**내부 import:** 발견되지 않음

**해결되지 않은 내부 import:** `com.shatteredpixel.shatteredpixeldungeon.Assets`, `com.shatteredpixel.shatteredpixeldungeon.Dungeon`, `com.shatteredpixel.shatteredpixeldungeon.GamesInProgress`, `com.shatteredpixel.shatteredpixeldungeon.ShatteredPixelDungeon`, `com.shatteredpixel.shatteredpixeldungeon.actors.Actor`, `com.shatteredpixel.shatteredpixeldungeon.actors.Char`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.ArtifactRecharge`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.Barrier`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.Buff`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.CounterBuff`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.EnhancedRings`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.FlavourBuff`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.Haste`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.Invisibility`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.LostInventory`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.PhysicalEmpower`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.Recharging`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.RevealedArea`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.Roots`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.ScrollEmpower`, `com.shatteredpixel.shatteredpixeldungeon.actors.buffs.WandEmpower`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.ArmorAbility`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.abilities.Ratmogrify`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells.DivineSense`, `com.shatteredpixel.shatteredpixeldungeon.actors.hero.spells.RecallInscription`, `com.shatteredpixel.shatteredpixeldungeon.actors.mobs.Mob`, `com.shatteredpixel.shatteredpixeldungeon.effects.CellEmitter`, `com.shatteredpixel.shatteredpixeldungeon.effects.Flare`, `com.shatteredpixel.shatteredpixeldungeon.effects.FloatingText`, `com.shatteredpixel.shatteredpixeldungeon.effects.SpellSprite`, `com.shatteredpixel.shatteredpixeldungeon.effects.particles.LeafParticle`, `com.shatteredpixel.shatteredpixeldungeon.items.BrokenSeal`, `com.shatteredpixel.shatteredpixeldungeon.items.Item`, `com.shatteredpixel.shatteredpixeldungeon.items.armor.Armor`, `com.shatteredpixel.shatteredpixeldungeon.items.armor.ClothArmor`, `com.shatteredpixel.shatteredpixeldungeon.items.artifacts.CloakOfShadows`, `com.shatteredpixel.shatteredpixeldungeon.items.artifacts.HolyTome`, `com.shatteredpixel.shatteredpixeldungeon.items.artifacts.HornOfPlenty`, `com.shatteredpixel.shatteredpixeldungeon.items.rings.Ring`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.Scroll`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.ScrollOfRecharging`, `com.shatteredpixel.shatteredpixeldungeon.items.scrolls.ScrollOfUpgrade`, `com.shatteredpixel.shatteredpixeldungeon.items.stones.Runestone`, `com.shatteredpixel.shatteredpixeldungeon.items.stones.StoneOfIntuition`, `com.shatteredpixel.shatteredpixeldungeon.items.trinkets.ShardOfOblivion`, `com.shatteredpixel.shatteredpixeldungeon.items.wands.Wand`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.SpiritBow`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.Weapon`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee.Gloves`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.melee.MeleeWeapon`, `com.shatteredpixel.shatteredpixeldungeon.items.weapon.missiles.MissileWeapon`, `com.shatteredpixel.shatteredpixeldungeon.levels.Level`, `com.shatteredpixel.shatteredpixeldungeon.levels.Terrain`, `com.shatteredpixel.shatteredpixeldungeon.messages.Messages`, `com.shatteredpixel.shatteredpixeldungeon.scenes.GameScene`, `com.shatteredpixel.shatteredpixeldungeon.sprites.CharSprite`, `com.shatteredpixel.shatteredpixeldungeon.ui.BuffIndicator`, `com.shatteredpixel.shatteredpixeldungeon.utils.GLog`, `com.watabou.noosa.Image`, `com.watabou.noosa.audio.Sample`, `com.watabou.utils.Bundle`, `com.watabou.utils.GameMath`, `com.watabou.utils.PathFinder`, `com.watabou.utils.Random`, `com.watabou.utils.Reflection`


## 통계와 해석
- 실제 본문을 읽은 파일: 16/16
- 이 파일들에서 확인된 내부 import-파일 관계 합계: 0개 (파일별 유일 대상 기준)
- 미해결 내부 import 표현 수: 294
- 이 표는 출발 파일 집합에 관한 **정방향 연결**이다. 해당 클래스를 누가 참조하는지 전수 조사한 역방향 그래프가 아니다.
- 동적 클래스 로딩, 상속 기반 호출, 동일 패키지 참조 및 런타임 객체 관계는 별도 근거가 필요하다.

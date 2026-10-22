# 역방향 import 관계 색인 — 이 파일을 누가 참조하나?

원본 코드 커밋 `bd3a990254e4249458816f4879e93ab87275555b`. 관계 데이터는 같은 폴더의 01~06 정방향 관계 문서에서 추출했다. **기준은 문서화한 93개 출발 소스 파일**이며, 프로젝트 전체 Java 1323개가 아니다. 따라서 숫자는 전수 실제 이용량이 아니라 **표본 내 정적 import 발생 파일 수**다. 이 목록에 없더라도 다른 파일이 참조할 수 있다. import는 실제 메서드 호출 증거가 아니다.

- 서로 다른 참조 출발 Java 파일: **93개**
- 정적 import 타깃 Java 파일: **759개**
- 중복 없는 출발→대상 파일 연결: **2608개**

## 표본 내 피참조 수 상위 30개

| 순위 | 참조된 파일 | 이 파일을 import하는 출발 파일 수 |
|---:|---|---:|
| 1 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java) | 57 |
| 2 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java) | 52 |
| 3 | [`SPD-classes/src/main/java/com/watabou/utils/Bundle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java) | 42 |
| 4 | [`SPD-classes/src/main/java/com/watabou/utils/Random.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java) | 39 |
| 5 | [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java) | 38 |
| 6 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java) | 34 |
| 7 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java) | 33 |
| 8 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java) | 33 |
| 9 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java) | 33 |
| 10 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java) | 28 |
| 11 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java) | 24 |
| 12 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java) | 23 |
| 13 | [`SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java) | 23 |
| 14 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java) | 22 |
| 15 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java) | 21 |
| 16 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java) | 21 |
| 17 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java) | 20 |
| 18 | [`SPD-classes/src/main/java/com/watabou/utils/PointF.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java) | 20 |
| 19 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java) | 18 |
| 20 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java) | 18 |
| 21 | [`SPD-classes/src/main/java/com/watabou/noosa/Image.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java) | 18 |
| 22 | [`SPD-classes/src/main/java/com/watabou/utils/Bundlable.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundlable.java) | 16 |
| 23 | [`SPD-classes/src/main/java/com/watabou/utils/Point.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java) | 16 |
| 24 | [`SPD-classes/src/main/java/com/watabou/utils/Reflection.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Reflection.java) | 16 |
| 25 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ItemSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ItemSprite.java) | 15 |
| 26 | [`SPD-classes/src/main/java/com/watabou/utils/GameMath.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameMath.java) | 15 |
| 27 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ItemSpriteSheet.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ItemSpriteSheet.java) | 14 |
| 28 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java) | 13 |
| 29 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Catalog.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Catalog.java) | 13 |
| 30 | [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java) | 13 |

## 전체 타깃별 역방향 연결

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java) — 57개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Messages.java) — 52개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)

### [`SPD-classes/src/main/java/com/watabou/utils/Bundle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java) — 42개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java)

### [`SPD-classes/src/main/java/com/watabou/utils/Random.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java) — 39개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/LoopBuilder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/LoopBuilder.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/SewerPainter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/SewerPainter.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java) — 38개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/utils/Bundle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundle.java)
- [`SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java)
- [`SPD-classes/src/main/java/com/watabou/utils/Random.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Random.java)
- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java)
- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java)
- [`services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/ShatteredNews.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/ShatteredNews.java)
- [`services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java) — 34개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java) — 33개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Assets.java) — 33개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java) — 33개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java) — 28개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java) — 24개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java) — 23개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Sample.java) — 23개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/GLog.java) — 22개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java) — 21개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java) — 21개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java) — 20개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`SPD-classes/src/main/java/com/watabou/utils/PointF.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PointF.java) — 20개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/LoopBuilder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/LoopBuilder.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java) — 18개 출발 파일

- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java)
- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java) — 18개 출발 파일

- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java)
- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/Image.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Image.java) — 18개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`SPD-classes/src/main/java/com/watabou/utils/Bundlable.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Bundlable.java) — 16개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)

### [`SPD-classes/src/main/java/com/watabou/utils/Point.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Point.java) — 16개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/Painter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/Painter.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java)

### [`SPD-classes/src/main/java/com/watabou/utils/Reflection.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Reflection.java) — 16개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ItemSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ItemSprite.java) — 15개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`SPD-classes/src/main/java/com/watabou/utils/GameMath.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameMath.java) — 15개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ItemSpriteSheet.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ItemSpriteSheet.java) — 14개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java) — 13개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Catalog.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Catalog.java) — 13개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java) — 13개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/Painter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/Painter.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/SewerPainter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/SewerPainter.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java) — 12개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/LoopBuilder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/LoopBuilder.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/Painter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/Painter.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/SewerPainter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/SewerPainter.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/audio/Music.java) — 12개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/Camera.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Camera.java) — 12개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`SPD-classes/src/main/java/com/watabou/utils/Callback.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Callback.java) — 12개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java) — 11개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java) — 11개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java) — 11개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java) — 11개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Notes.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Notes.java) — 11개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java) — 11개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java) — 11개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)

### [`SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ControllerHandler.java) — 11개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)
- [`SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java)

### [`SPD-classes/src/main/java/com/watabou/utils/PathFinder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PathFinder.java) — 11개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java) — 10개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java) — 10개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Document.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Document.java) — 10개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java) — 10개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/SewerPainter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/SewerPainter.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Icons.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Icons.java) — 10개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)

### [`SPD-classes/src/main/java/com/watabou/utils/FileUtils.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/FileUtils.java) — 10개 출발 파일

- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/GamesInProgress.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java)

### [`SPD-classes/src/main/java/com/watabou/utils/RectF.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/RectF.java) — 10개 출발 파일

- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AscensionChallenge.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AscensionChallenge.java) — 9개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java) — 9개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ShardOfOblivion.java) — 9개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java) — 9개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java) — 9개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndOptions.java) — 9개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)

### [`SPD-classes/src/main/java/com/watabou/input/GameAction.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/GameAction.java) — 9개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Scene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/Emitter.java) — 9개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)

### [`SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/DeviceCompat.java) — 9개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/GitHubUpdates.java)

### [`SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/PlatformSupport.java) — 9개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)
- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidPlatformSupport.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopPlatformSupport.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSPlatformSupport.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicImmune.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicImmune.java) — 8개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Chrome.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Chrome.java) — 8개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java) — 8개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java) — 8개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java) — 8개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java) — 8개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/Painter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/Painter.java) — 8개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java) — 8개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java) — 8개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`SPD-classes/src/main/java/com/watabou/input/KeyBindings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyBindings.java) — 8개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Scene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`SPD-classes/src/main/java/com/watabou/input/KeyEvent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/KeyEvent.java) — 8개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Scene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java)
- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDAction.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`SPD-classes/src/main/java/com/watabou/utils/BArray.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/BArray.java) — 8개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/LostInventory.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/LostInventory.java) — 7개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Speck.java) — 7개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java) — 7개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java) — 7개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java) — 7개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java) — 7개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StyledButton.java) — 7개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Window.java) — 7개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)

### [`SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/gltextures/TextureCache.java) — 7개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)

### [`SPD-classes/src/main/java/com/watabou/glwrap/Blending.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Blending.java) — 7개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)

### [`SPD-classes/src/main/java/com/watabou/input/PointerEvent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/PointerEvent.java) — 7개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/Group.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Group.java) — 7개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CellEmitter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CellEmitter.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TalismanOfForesight.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/MagicalHolster.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/MagicalHolster.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/Chasm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/Chasm.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RenderedTextBlock.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndKeyBindings.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NinePatch.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Chrome.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Chrome.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Component.java) — 6개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Blindness.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Blindness.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invisibility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invisibility.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/PowerOfMany.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mimic.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ShadowParticle.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/SpellSprite.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Splash.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClothArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClothArmor.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/DriedRose.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/TimekeepersHourglass.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/BrokenSeal.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Pickaxe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/Pickaxe.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ParchmentScrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ParchmentScrap.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrinketCatalyst.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MagesStaff.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/Dart.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/SpiritBow.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/SpiritBow.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Bestiary.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Bestiary.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Journal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Journal.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GatewayTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GatewayTrap.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GeyserTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GeyserTrap.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/SummoningTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/SummoningTrap.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Swiftthistle.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/HeroSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/HeroSprite.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BuffIndicator.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/IconButton.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TitleBackground.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMessage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndMessage.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/BitmapText.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/PointerArea.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Tweener.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`SPD-classes/src/main/java/com/watabou/utils/Rect.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Rect.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/LevelTransition.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/Painter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/Painter.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java)

### [`SPD-classes/src/main/java/com/watabou/utils/Signal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Signal.java) — 5개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Scene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)

### [`SPD-classes/src/main/java/com/watabou/utils/SparseArray.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/SparseArray.java) — 5개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barrier.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Hunger.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Hunger.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MindVision.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MindVision.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Momentum.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MonkEnergy.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Recharging.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Recharging.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Regeneration.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Regeneration.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/RevealedArea.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/ShadowClone.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/DivineSense.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/GuidingLight.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CloakOfShadows.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HolyTome.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/HornOfPlenty.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SkeletonKey.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/VelvetPouch.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/VelvetPouch.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindOfWeapon.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfForce.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRecharging.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRecharging.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfUpgrade.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfIntuition.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfRegrowth.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FrostTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FrostTrap.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PitfallTrap.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/messages/Languages.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/News.java) — 4개 출발 파일

- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/Updates.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/Updates.java) — 4개 출발 파일

- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ExitButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ExitButton.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndJournal.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/ColorBlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ColorBlock.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/particles/PixelParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/particles/PixelParticle.java) — 4개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SacrificialFire.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Amok.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Amok.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ArtifactRecharge.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ArtifactRecharge.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Awareness.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Awareness.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Berserk.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Berserk.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Burning.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Charm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Charm.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Dread.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Dread.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/GreaterHaste.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/GreaterHaste.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Ooze.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Terror.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/AscendedForm.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Challenge.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/ElementalStrike.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpiritHawk.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Endure.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BodyForm.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWeapon.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Blacksmith.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Imp.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BannerSprites.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BannerSprites.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TargetedCell.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClassArmor.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Viscosity.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Viscosity.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/AlchemistsToolkit.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/MasterThievesArmband.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/PotionBandolier.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/PotionBandolier.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/ScrollHolder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/ScrollHolder.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bombs/Bomb.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/ItemStatusHandler.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/Guidebook.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/Guidebook.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindofMisc.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/KindofMisc.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/ExoticPotion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/ExoticPotion.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHealing.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfStrength.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfStrength.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/EscapeCrystal.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Recipe.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfArcana.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfArcana.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfFuror.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfFuror.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfWealth.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ExoticScroll.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfChallenge.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMagicMapping.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMagicMapping.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRemoveCurse.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRemoveCurse.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Belongings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTeleportation.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/Runestone.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAggression.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAggression.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfEnchantment.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfEnchantment.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/DimensionalSundial.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/DimensionalSundial.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLivingEarth.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfWarding.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Explosive.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Crystal.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gloves.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gloves.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Scimitar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Scimitar.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WornShortsword.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WornShortsword.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/secret/SecretRoom.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SpecialRoom.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/BlazingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/BlazingTrap.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/BurningTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/BurningTrap.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ChillingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ChillingTrap.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ConfusionTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ConfusionTrap.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/CorrosionTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/CorrosionTrap.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DisintegrationTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DisintegrationTrap.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GuardianTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GuardianTrap.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/RockfallTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/RockfallTrap.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/StormTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/StormTrap.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WarpingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WarpingTrap.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/VaultLevel.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ShadowCaster.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ShadowCaster.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Earthroot.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/QuickSlot.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ActionIndicator.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/AttackIndicator.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/HeroIcon.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroSubClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/ArmorAbility.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RedButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RedButton.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/DungeonSeed.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/DungeonSeed.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHero.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoItem.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndResurrect.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUseItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUseItem.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsImpl.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/news/shatteredNews/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/news/NewsImpl.java) — 3개 출발 파일

- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java)

### [`services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateImpl.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/updates/githubUpdates/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/UpdateImpl.java) — 3개 출발 파일

- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java)
- [`desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/desktop/src/main/java/com/shatteredpixel/shatteredpixeldungeon/desktop/DesktopLauncher.java)
- [`ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/ios/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ios/IOSLauncher.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Gizmo.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScript.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/SkinnedBlock.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/tweeners/AlphaTweener.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/AlphaTweener.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/Visual.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Visual.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)

### [`SPD-classes/src/main/java/com/watabou/utils/ColorMath.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/ColorMath.java) — 3개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Fire.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Adrenaline.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Adrenaline.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AllyBuff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AllyBuff.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barkskin.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Barkskin.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Bless.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Bless.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corruption.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Degrade.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Degrade.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/EnhancedRings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/EnhancedRings.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/FlavourBuff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/FlavourBuff.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Haste.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Haste.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/HoldFast.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/HoldFast.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invulnerability.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Invulnerability.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSight.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Paralysis.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PhysicalEmpower.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/PinCushion.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Preparation.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ScrollEmpower.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ShieldBuff.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Sleep.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Sleep.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SnipersMark.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SoulMark.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SoulMark.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vertigo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vertigo.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/duelist/Feint.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/NaturesPower.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WildMagic.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/DeathMark.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/AuraOfProtection.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HolyWard.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/LifeLinkSpell.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Smite.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/Stasis.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollGeomancer.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/MirrorImage.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/PrismaticImage.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Wandmaker.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BlobEmitter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BlobEmitter.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/EmoIcon.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Fireball.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Fireball.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ElmoParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ElmoParticle.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlameParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlameParticle.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/LeafParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/LeafParticle.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/WindParticle.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Ripple.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Ripple.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Amulet.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Ankh.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Bulk.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Bulk.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/AntiMagic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/AntiMagic.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Brimstone.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Brimstone.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Flow.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Flow.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Obfuscation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Obfuscation.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Potential.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Potential.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Stone.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Stone.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Swiftness.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Swiftness.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/LeatherArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/LeatherArmor.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/MailArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/MailArmor.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/PlateArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/PlateArmor.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ScaleArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ScaleArmor.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/EtherealChains.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/UnstableSpellbook.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Dewdrop.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Dewdrop.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Food.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MysteryMeat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/MysteryMeat.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Gold.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Gold.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/DocumentPage.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/CrystalKey.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/CrystalKey.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/GoldenKey.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/GoldenKey.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/Key.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/Brew.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/Brew.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfCleansing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfCleansing.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfExperience.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfExperience.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfInvisibility.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfInvisibility.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLiquidFlame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLiquidFlame.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfMindVision.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfMindVision.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfPurity.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfPurity.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/RemainsItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/remains/RemainsItem.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Bones.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfAccuracy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfAccuracy.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfElements.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfElements.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEnergy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEnergy.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEvasion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfEvasion.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfHaste.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfMight.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfSharpshooting.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfSharpshooting.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfTenacity.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/RingOfTenacity.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfIdentify.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfLullaby.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfLullaby.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMirrorImage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfMirrorImage.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRage.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRetribution.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfRetribution.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfAugmentation.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlast.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlast.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlink.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfBlink.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfClairvoyance.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfClairvoyance.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfDeepSleep.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfDeepSleep.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfDetectMagic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfDetectMagic.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfFear.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfFear.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfFlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfFlock.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfShock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/stones/StoneOfShock.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Torch.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Torch.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/CrackedSpyglass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/CrackedSpyglass.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ExoticCrystals.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ExoticCrystals.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/EyeOfNewt.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/EyeOfNewt.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/FerretTuft.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/FerretTuft.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MimicTooth.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MimicTooth.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/MossyClump.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ThirteenLeafClover.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ThirteenLeafClover.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/TrapMechanism.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/Trinket.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/WondrousResin.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/WondrousResin.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfBlastWave.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFireblast.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfFrost.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfLightning.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfMagicMissile.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Waterskin.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/QuickSlotButton.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blazing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blazing.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Grim.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Grim.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Kinetic.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Lucky.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Projecting.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Projecting.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Shocking.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Shocking.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vorpal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vorpal.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Crossbow.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Cudgel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Cudgel.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dagger.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Flail.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Quarterstaff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Quarterstaff.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Rapier.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RoundShield.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RunicBlade.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/RunicBlade.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sai.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sickle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sickle.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/TippedDart.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/HeavyBoomerang.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ThrowingKnife.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ThrowingKnife.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ThrowingSpike.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ThrowingSpike.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ThrowingStone.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ThrowingStone.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/Door.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/Door.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/MiningLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/MiningLevel.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/AlarmTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/AlarmTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/CursingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/CursingTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DisarmingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DisarmingTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DistortionTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/DistortionTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FlashingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FlashingTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FlockTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/FlockTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrimTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrimTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrippingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GrippingTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/OozeTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/OozeTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PoisonDartTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/PoisonDartTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ShockingTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ShockingTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/TeleportationTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/TeleportationTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ToxicTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ToxicTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WeakeningTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WeakeningTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WornDartTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/WornDartTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Blindweed.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Blindweed.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Fadeleaf.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Fadeleaf.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Firebloom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Firebloom.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Icecap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Icecap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Mageroyal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Mageroyal.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Rotberry.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Rotberry.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sorrowmoss.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sorrowmoss.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Starflower.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Starflower.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Stormvine.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Stormvine.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Sungrass.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ShatteredPixelDungeon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ImpSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/ImpSprite.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/CustomTilemap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTerrainTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTerrainTilemap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTileSheet.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/TerrainFeaturesTilemap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Button.java) — 2개 출발 파일

- [`android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/android/src/main/java/com/shatteredpixel/shatteredpixeldungeon/android/AndroidLauncher.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CharHealthIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CharHealthIndicator.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/GameLog.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventoryPane.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RightClickMenu.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TargetHealthIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/TargetHealthIndicator.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/IconTitle.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/JournalScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndError.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndError.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoTrap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/Trap.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuickBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuickBag.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toolbar.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTitledMessage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTitledMessage.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndVictoryCongrats.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndVictoryCongrats.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)

### [`SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Vertexbuffer.java) — 2개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/NoosaScriptNoLighting.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/NoosaScriptNoLighting.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Tilemap.java) — 2개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)
- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Electricity.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SmokeScreen.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/SmokeScreen.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/StormCloud.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/StormCloud.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/ToxicGas.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Web.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WellWater.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/WellWater.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/AdrenalineSurge.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ArcaneArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ArcaneArmor.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Bleeding.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Bleeding.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Chill.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Chill.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Combo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Combo.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corrosion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Corrosion.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/CounterBuff.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/CounterBuff.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Cripple.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Cripple.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Daze.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Daze.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Doom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Doom.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Drowsy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Drowsy.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/FireImbue.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/FireImbue.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Foresight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Foresight.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Frost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Frost.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/FrostImbue.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/FrostImbue.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Fury.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Fury.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/HeroDisguise.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/HeroDisguise.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Hex.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Hex.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Levitation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Levitation.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/LifeLink.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/LifeLink.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Light.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Light.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/LockedFloor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/LockedFloor.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSleep.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/MagicalSleep.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Poison.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Roots.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Shadows.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Slow.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Speed.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Speed.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Stamina.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Stamina.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/SwarmIntelTracker.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/TimeStasis.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/TimeStasis.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vulnerable.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Vulnerable.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/WandEmpower.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Weakness.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Weakness.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/cleric/Trinity.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpectralBlades.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/huntress/SpectralBlades.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/ElementalBlast.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/ElementalBlast.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/mage/WarpBeacon.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/Ratmogrify.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/rogue/SmokeBomb.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/HeroicLeap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/HeroicLeap.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Shockwave.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/abilities/warrior/Shockwave.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/BeamingRay.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ClericSpell.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/HallowedGround.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/RecallInscription.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/ShieldOfLight.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/spells/SpiritForm.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Bat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Bat.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Crab.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Crab.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/CrystalSpire.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/CrystalSpire.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DemonSpawner.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DemonSpawner.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/DwarfKing.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/EbonyMimic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/EbonyMimic.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Elemental.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FetidRat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/FetidRat.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Ghoul.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GnollTrickster.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GoldenMimic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GoldenMimic.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GreatCrab.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/GreatCrab.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Guard.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/MobSpawner.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/MobSpawner.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Monk.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Necromancer.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/DirectableAlly.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Sheep.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Shopkeeper.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Piranha.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/quest/vault/VaultBossElemental.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Statue.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Tengu.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Thief.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/ChampionEnemy.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Wraith.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/YogFist.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/BadgeBanner.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CheckedCell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CheckedCell.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/CircleArc.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/StatusPane.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/DarkBlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/DarkBlock.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/GlowBlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/GlowBlock.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/IceBlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/IceBlock.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/FlowParticle.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SacrificialParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SacrificialParticle.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SnowParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SnowParticle.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/SparkParticle.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShadowBox.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShadowBox.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShieldHalo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/ShieldHalo.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Surprise.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TorchHalo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/TorchHalo.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Wound.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClericArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/ClericArmor.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/AntiEntropy.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/AntiEntropy.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Corrosion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Corrosion.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Displacement.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Displacement.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Metabolism.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Metabolism.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Multiplicity.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Multiplicity.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Overgrowth.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Overgrowth.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Stench.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/curses/Stench.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/DuelistArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/DuelistArmor.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Affection.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Affection.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Camouflage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Camouflage.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Entanglement.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Entanglement.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Repulsion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Repulsion.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Thorns.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/glyphs/Thorns.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/HuntressArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/HuntressArmor.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/MageArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/MageArmor.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/RogueArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/RogueArmor.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/WarriorArmor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/WarriorArmor.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/CapeOfThorns.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/ChaliceOfBlood.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/SandalsOfNature.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EnergyCrystal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EnergyCrystal.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/ChargrilledMeat.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/ChargrilledMeat.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/FrozenCarpaccio.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/FrozenCarpaccio.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Pasty.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/Pasty.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/SupplyRation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/food/SupplyRation.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Honeypot.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/GuidePage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/GuidePage.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/journal/RegionLorePage.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/IronKey.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/IronKey.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/WornKey.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/keys/WornKey.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LiquidMetal.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LostBackpack.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/LostBackpack.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/InterlevelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/AquaBrew.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/brews/AquaBrew.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/elixirs/Elixir.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/elixirs/Elixir.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/elixirs/ElixirOfHoneyedHealing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/elixirs/ElixirOfHoneyedHealing.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/elixirs/ElixirOfMight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/elixirs/ElixirOfMight.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfCorrosiveGas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfCorrosiveGas.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfDivineInspiration.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfDivineInspiration.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfShroudingFog.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfShroudingFog.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfSnapFreeze.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfSnapFreeze.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfStormClouds.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/exotic/PotionOfStormClouds.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfFrost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfFrost.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHaste.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfHaste.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLevitation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfLevitation.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfParalyticGas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfParalyticGas.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfToxicGas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/PotionOfToxicGas.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/CorpseDust.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DarkGold.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DarkGold.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DwarfToken.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/quest/DwarfToken.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfAntiMagic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfAntiMagic.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfPsionicBlast.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/exotic/ScrollOfPsionicBlast.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/InventoryScroll.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTerror.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTerror.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/ScrollOfTransmutation.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Spell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/spells/Spell.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Stylus.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/ChaoticCenser.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/PetrifiedSeed.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/PetrifiedSeed.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/RatSkull.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/RatSkull.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/SaltCube.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/SaltCube.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/VialOfBlood.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/trinkets/VialOfBlood.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorrosion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorrosion.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfCorruption.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfDisintegration.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfPrismaticLight.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/WandOfTransfusion.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Annoying.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Annoying.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Dazzling.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Dazzling.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Displacing.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Displacing.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Friendly.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Friendly.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Polarized.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Polarized.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Pressurized.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Pressurized.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Sacrificial.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Sacrificial.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wayward.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wondrous.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/curses/Wondrous.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blocking.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blooming.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Blooming.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Chilling.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Chilling.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Corrupting.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Corrupting.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Elastic.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Elastic.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Eldritch.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Eldritch.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Unstable.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Unstable.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vampiric.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Vampiric.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Venomous.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/enchantments/Venomous.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/AssassinsBlade.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/AssassinsBlade.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/BattleAxe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/BattleAxe.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dirk.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Dirk.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gauntlet.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Gauntlet.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Glaive.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Glaive.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greataxe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greataxe.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatshield.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatshield.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatsword.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Greatsword.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/HandAxe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/HandAxe.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Katana.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Katana.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Longsword.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Longsword.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Mace.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Mace.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Shortsword.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Shortsword.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Spear.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Spear.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Sword.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarHammer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarHammer.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarScythe.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/WarScythe.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Whip.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/Whip.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Bolas.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Bolas.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/ShockingDart.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/darts/ShockingDart.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/FishingSpear.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/FishingSpear.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ForceCube.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ForceCube.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Javelin.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Javelin.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Kunai.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Kunai.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Shuriken.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Shuriken.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ThrowingClub.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ThrowingClub.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ThrowingHammer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ThrowingHammer.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ThrowingSpear.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/ThrowingSpear.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Tomahawk.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Tomahawk.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Trident.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/Trident.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/Builder.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/FigureEightBuilder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/FigureEightBuilder.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/LoopBuilder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/LoopBuilder.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesBossLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesBossLevel.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityBossLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityBossLevel.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/DeadEndLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/DeadEndLevel.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/HighGrass.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/features/HighGrass.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Level.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsBossLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsBossLevel.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/LastLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/LastLevel.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/CavesPainter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/CavesPainter.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/CityPainter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/CityPainter.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CityLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/HallsPainter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/HallsPainter.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/PrisonPainter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/PrisonPainter.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/SewerPainter.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/painters/SewerPainter.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonBossLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonBossLevel.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/ConnectionRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/connection/ConnectionRoom.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/LoopBuilder.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/builders/LoopBuilder.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/DemonSpawnerRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/DemonSpawnerRoom.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/HallsLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/MagicalFireRoom.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/PitRoom.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SacrificeRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/SacrificeRoom.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/ShopRoom.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/StatueRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/StatueRoom.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/WeakFloorRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/special/WeakFloorRoom.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/entrance/EntranceRoom.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ExitRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/exit/ExitRoom.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerBossLevel.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ExplosiveTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/ExplosiveTrap.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/RegularLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GnollRockfallTrap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/traps/GnollRockfallTrap.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/RankingsScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/RankingsScene.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/SurfaceScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/SurfaceScene.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BlacksmithSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BlacksmithSprite.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/CavesLevel.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BruteSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/BruteSprite.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Brute.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DiscardedItemSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/DiscardedItemSprite.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhostSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/GhostSprite.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/MissileSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/MissileSprite.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/MobSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/MobSprite.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SnakeSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/SnakeSprite.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Snake.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonWallsTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonWallsTilemap.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/FogOfWar.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/GridTileMap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/GridTileMap.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/RaisedTerrainTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/RaisedTerrainTilemap.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallBlockingTilemap.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/WallOcclusionTilemap.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Banner.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/BossHealthBar.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CheckBox.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/CheckBox.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/InventorySlot.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndBag.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ItemSlot.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/LootIndicator.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/MenuPane.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/OptionSlider.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/RadialMenu.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ResumeIndicator.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/ResumeIndicator.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tag.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Toast.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/ui/Tooltip.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/Holiday.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/utils/Holiday.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndChallenges.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndEnergizeItem.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/AlchemyScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndGame.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHardNotification.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHardNotification.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/WelcomeScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndHeroInfo.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoCell.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoCell.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoMob.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoPlant.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndInfoPlant.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuest.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndQuest.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSadGhost.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/npcs/Ghost.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndSettings.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTextInput.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/HeroSelectScene.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndTradeItem.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/windows/WndUpgrade.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/GameScene.java)

### [`services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/AvailableUpdateData.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/services/src/main/java/com/shatteredpixel/shatteredpixeldungeon/services/updates/AvailableUpdateData.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/TitleScene.java)

### [`SPD-classes/src/main/java/com/watabou/glscripts/Script.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glscripts/Script.java) — 1개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)

### [`SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/glwrap/Matrix.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`SPD-classes/src/main/java/com/watabou/input/InputHandler.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/InputHandler.java) — 1개 출발 파일

- [`SPD-classes/src/main/java/com/watabou/noosa/Game.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Game.java)

### [`SPD-classes/src/main/java/com/watabou/input/ScrollEvent.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/input/ScrollEvent.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/Halo.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Halo.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/PrisonLevel.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/MovieClip.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/Scene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/Scene.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/ScrollArea.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ScrollArea.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/CellSelector.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/TextureFilm.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/tiles/DungeonTilemap.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/tweeners/Delayer.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/Delayer.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/tweeners/PosTweener.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/tweeners/PosTweener.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java)

### [`SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/noosa/ui/Cursor.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/scenes/PixelScene.java)

### [`SPD-classes/src/main/java/com/watabou/utils/GameSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/GameSettings.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/SPDSettings.java)

### [`SPD-classes/src/main/java/com/watabou/utils/Graph.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/SPD-classes/src/main/java/com/watabou/utils/Graph.java) — 1개 출발 파일

- [`core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/Room.java)

## 해석 주의
- 목록의 모든 관계는 **명시적 Java import→실제 파일 경로**이다.
- 의존성이 많은 파일이 실제 런타임 병목인 것은 아니다.
- import가 없는 같은 패키지 참조, 리플렉션, 상속에 따른 동적 디스패치, FQCN 참조는 빠질 수 있다.
- 표본 편향: 게임 공통 핵심 코드 위주이므로 정확한 전역 centrality 값이 아니다.

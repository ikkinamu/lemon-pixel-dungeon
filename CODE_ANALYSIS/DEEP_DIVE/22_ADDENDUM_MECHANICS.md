# 추가 구현 해설: 투사체·환경 효과·스프라이트·방 생성

## 물리 투사체 / 광역 범위
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/Ballistica.java#L31): 맵상 시작점과 목표점 및 충돌 옵션으로 경로를 계산하는 자료 구조. path, sourcePos, collisionPos와 STOP_TARGET/STOP_CHARS/STOP_SOLID 플래그가 존재한다.
- PROJECTILE = STOP_TARGET | STOP_CHARS | STOP_SOLID
- MAGIC_BOLT = STOP_CHARS | STOP_SOLID
- WONT_STOP = 0
여기서 OR 결합은 비트 플래그 표현이며, 이름에 따라 항상 해당 충돌에만 멈춘다는 추론은 다른 사용자가 매개변수를 추가할 수 있으므로 실제 callsite를 확인해야 한다.

[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/mechanics/ConeAOE.java#L34): Ballistica를 바탕으로 coreRay, outerRays, rays, cells를 계산한다. 화면 파티클이 아니라 실제 영향 대상 셀 집합을 계산하는 기하적 용도.

## 공간 효과
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/blobs/Blob.java#L35): Blob extends Actor, volume, cur, off, area 필드와 evolve(), seed(), clear() 제공. 환경의 공간 효과를 액터 시간 체계로 처리한다.
소스에 존재하는 Blob은 Git 객체의 데이터 블롭이나 단순 이미지와 다른 개념임.

## 논리 상태와 애니메이션
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/sprites/CharSprite.java#L63): CharSprite extends MovieClip, move(), attack(), zap(), link(Char), idle() 등 외형 애니메이션. 시뮬레이션의 피해 판정은 Char/Mob/Hero 계층과 별도로 이뤄짐.
소스 CharSprite.move() 호출이 정확히 언제 논리 pos 변경과 일치하는지는 발신 호출의 순서를 분석해야 한다.

## 지형 번호
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java L24](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/Terrain.java#L24)는 CHASM, EMPTY, GRASS, WALL, DOOR 등의 정수 지형 ID를 선언. 이 숫자들은 Level.map의 값과 연계되며 타일 이미지를 직접 가리키는 픽셀 좌표가 아님.

## 일반 방과 기본 층
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/rooms/standard/StandardRoom.java#L34): StandardRoom extends Room, 크기 분류 SizeCategory, 방 크기·가중치·생성 후보 관리.
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/levels/SewerLevel.java#L63): SewerLevel extends RegularLevel, 해당 지역 음악, trapClasses/chances, painter, 스프라이트/지형 동작을 특화.
**중요:** RegularLevel의 기본 생성 로직과 지역별 재정의가 결합하므로 '모든 층이 같은 속성'이라고 가정하지 않음.

## 소지품과 식물
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/bags/Bag.java#L38): Bag extends Item, Iterable<Item> 구현. capacity()/canHold()/collect()/iterator()를 제공하며 중첩 Bag 처리도 연결.
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/plants/Plant.java#L53): Plant implements Bundlable, trigger(), activate(Char), wither()를 정의하고 Seed extends Item을 내부 클래스로 가짐. 바닥 Plant와 인벤토리 Seed는 서로 역할이 다름.

## 해석의 한계
각 클래스의 모든 하위 구현을 비교한 것은 아님. 대표 소스에서 확인한 선언·메서드 및 상속을 근거로 설명했고, 외부에서 실제 어떤 옵션으로 호출하는지는 별도 검증이 필요하다.

# 아이템·장비·소모품·드롭 생성

## 1. Item이 다루는 공통 사항
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java:61-105](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L61-L105):
- quantity / stackable: 수량과 중첩 가능 여부.
- level / levelKnown: 강화 단계 관련 내부 값과 플레이어에게 알려졌는지 여부.
- cursed / cursedKnown: 저주 상태와 식별 여부.
- image / icon: 화면 표현·랜덤 이미지 식별.
- defaultAction / usesTargeting: 기본 사용 동작과 대상 선택 필요 여부.
- doPickUp / doDrop / doThrow / collect / split / duplicate / detach / upgrade 등.

**아이템 level과 던전 depth는 별개**다. 또한 buffedLvl()은 보정된 장비 수준과 관련된 API이므로 저장된 내부 level 필드와 항상 같다고 보면 안 됨.

### 수집 흐름
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java:198-245](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Item.java#L198-L245):
1. Bag과 중첩 가능성을 확인.
2. 내부 Bag이 해당 아이템을 넣을 수 있으면 우선 재귀적으로 시도.
3. 컨테이너 용량 확인.
4. 스택 가능하고 유사한 아이템이 있으면 합침.
5. 퀵슬롯/발견 기록/특성 연동이 이어질 수 있음.

Heap은 맵 바닥 위 여러 Item을 담는 **아이템 더미** 모델이며 type, pos, items, seen, hidden, haunted 등 저장([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java:60-82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Heap.java#L60-L82)). 캐릭터 소지품 Bag과 동일한 구조가 아님.

## 2. 장비 계층
| 구분 | 실제 선언 / 확인된 특징 |
|---|---|
| EquipableItem | Item 상속. 장착/해제 및 장착 시간 |
| Weapon | KindOfWeapon 상속. ACC(명중 계수), DLY(지연 계수), RCH(사거리 관련) |
| MeleeWeapon | Weapon 상속. 티어/근접 공격·결투가 능력/충전 |
| MissileWeapon | Weapon 상속. 사거리·내구도·발사 처리 |
| Armor | EquipableItem 상속. 방어/회피 계수, Glyph, Seal |
| Wand | Item 상속. curCharges, maxCharges, 충전 및 발사 |
| Ring | KindofMisc 상속. RingBuff, 식별된 보석 |
| Artifact | KindofMisc 상속. 능동·수동 효과와 충전 |
| Potion | Item 상속. 마시기/던지기/적용/식별 |
| Scroll | Item 상속. 읽기/식별/룬 표식 |

출처: [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/EquipableItem.java), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/melee/MeleeWeapon.java), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/missiles/MissileWeapon.java), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/armor/Armor.java), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/wands/Wand.java), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/rings/Ring.java), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/artifacts/Artifact.java), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/potions/Potion.java), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/scrolls/Scroll.java).

**중요:** Weapon은 EquipableItem을 바로 상속하지 않는다. 코드를 읽지 않고 '모든 장비는 EquipableItem의 직접 자식'으로 적으면 실제 상속과 어긋난다. Weapon 상위 KindOfWeapon의 자세한 구현은 별도 검증 대상.

## 3. 공격력과 속도의 보정
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java:90-121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/weapon/Weapon.java#L90-L121):
- ACC=1f 기본 명중 계수
- DLY=1f 기본 행동 지연 계수 (값이 클수록 무조건 빠르다는 뜻이 아님)
- RCH=1 기본 사거리 계수 (설명상 근접 타격 적용)
- Augment.SPEED/DAMAGE/NONE은 피해량/딜레이 계수 쌍을 정의.
- 피해량의 최종 계산은 무기 + Char.attack + 방어자 + 버프 등 여러 지점을 함께 살펴야 함.

## 4. Generator: 단순 무작위 추첨기가 아님
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java:219-300](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L219-L300), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java:620-750](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/items/Generator.java#L620-L750).
- Category가 아이템 분류·확률 테이블을 유지.
- fullReset(): 덱 종류 및 분류별 난수·확률을 다시 설정.
- random(): 큰 분류 덱에서 추첨하고 소모량을 줄임. 덱이 소진되면 새 덱을 사용.
- random(Category): 분류별 별도 분기(장비/무기/투척/유물 등) 및 확률 변화를 처리.
- randomUsingDefaults(...): 덱 효과를 일부 우회하는 생성 경로.
- undoDrop(...): 특정 아이템의 드롭 확률 변화 일부를 되돌림. 소스 주석도 **덱의 이전 순서를 보존하지 않는다**고 명시.

'랜덤'의 의미를 독립 균등분포로 단정하면 안 된다. 분류별 가중치, 덱 소진, 미리 생성한 난수 seed, 유물 예외 등 복합적인 체계를 가짐.

## 5. 식별과 표현
Potion/Scroll/Ring은 알려진 종류, 익명 표현/색상/룬/보석 등을 다룬다. 게임 내에서 '외형으로 나타난 종류'와 '정체가 식별된 종류'를 구분해 봐야 한다. 새 아이템을 설계할 때 ItemStatusHandler 등 식별·저장 연동이 있는지 추가 확인 필요.

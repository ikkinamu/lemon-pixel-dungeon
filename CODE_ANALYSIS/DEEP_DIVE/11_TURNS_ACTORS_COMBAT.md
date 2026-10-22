# 시간·턴·행동·전투·AI

## 1. Actor의 실제 스케줄 방식
소스: [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java:37-161](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L37-L161), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java:250-344](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L250-L344).

**확인한 필드**
| 필드 | 의미 |
|---|---|
| time (float) | 개별 Actor가 다음 행동을 처리할 시간 |
| now (static float) | 처리 기준의 현재 시간 |
| all (HashSet<Actor>) | 등록된 액터의 집합 |
| chars (HashSet<Char>) | 등록된 캐릭터 집합 |
| current (volatile Actor) | 처리 중인 액터 |
| actPriority | 동일 시간에 어느 액터를 먼저 처리할지 구분 |
| id/nextID/ids | 액터 식별과 복원에 사용 |
| TICK=1f | 기본 행동 시간 단위 |

**Actor.process()**
1. 모든 등록 액터를 훑어 가장 작은 time을 찾음.
2. time이 같으면 actPriority가 큰 액터를 우선.
3. now를 해당 액터의 time으로 지정.
4. 움직이는 캐릭터 스프라이트가 있으면 대기할 수 있음.
5. 그 액터의 act() 호출.
6. 반환값·인터럽트·영웅 생존 여부에 따라 연속 처리하거나 스레드가 대기.
7. 게임 장면에서 스레드를 깨우면 다음 구간을 처리.

**주의:** HashSet 순회 순서에 의존하는 것처럼 보일 수 있으므로, 정확히 동시간·동우선순위인 두 액터의 안정적인 순서를 이 메서드만으로 보장하지 않는다. 반환값 boolean을 단순히 '행동 성공'으로 번역하면 틀릴 수 있다. 이 문맥에서는 **처리 반복/일시 중단에 참여하는 값**이다.

우선순위(Actor.java 선언): VFX_PRIO=100, HERO_PRIO=0, BLOB_PRIO=-10, MOB_PRIO=-20, BUFF_PRIO=-30, DEFAULT=-100. 개별 액터가 더 세부 우선순위를 설정할 수 있다.

**Actor.fixTime():** 모든 액터의 누적 시간을 정수 단위로 평행 이동해 큰 시간값을 줄이고 Statistics.duration을 갱신한다. 게임 시간 전부를 0으로 초기화하는 메서드가 아니다([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java:175-196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L175-L196)).

## 2. 캐릭터 계층
- **Char extends Actor:** 위치 pos, HP/HT, 속도, 시야, 상태 효과, 공격·방어의 공통 기반([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java:166-198](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L166-L198)).
- **Hero extends Char:** 클래스/서브클래스, 특성, 소지품, 플레이어 행동 요청, 시야/입력 준비([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java:197-248](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L197-L248)).
- **Mob extends Char:** 개별 적/동료를 포함할 수 있는 몬스터 기반, 적 대상 선택 및 상태 AI([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java:111-143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L111-L143)).
- **Buff extends Actor:** Char에 붙여 효과를 제공하며 target/attachTo/detach/act를 가짐([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java:34-94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/buffs/Buff.java#L34-L94)).

### HP와 HT
Char의 HT는 현재 HP와 별도인 체력 상한 개념으로 사용된다. 예: Mob.onAdd()는 승천 효과 적용 시 기존 HP/HT 비율을 보존하며 새 HT를 계산([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java:144-152](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L144-L152)). 변수명 HT를 '치유량'으로 해석하지 말 것.

## 3. 영웅 행동의 전달
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java): Move, PickUp, OpenChest, Buy, Interact, Unlock, LvlTransition, Mine, Alchemy, Attack 등의 행동 객체를 정의.
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java:829-948](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L829-L948): Hero.act()는 curAction의 실제 타입에 따라 actMove / actInteract / actPickUp / actAttack 등을 분기해 호출한다.
- curAction=null이면 휴식(resting) 또는 입력 대기 상태로 이동.
- ready는 **플레이어 입력 가능/행동 대기 상태** 맥락의 플래그. '엔진 로딩 준비 완료'와 다름.
- busy()/spendAndNext()는 행동 중 표시와 시간 소비 및 액터 스케줄의 다음 진행을 연결.
- fieldOfView가 Dungeon.level.heroFOV를 가리키므로 시야 데이터를 영웅 객체 안의 독립 복제본으로 가정하면 안 됨.

## 4. 적 AI의 상태 객체
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java:111-143](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L111-L143), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java:1215-1250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L1215-L1250).
- AiState는 act(enemyInFOV, justAlerted) 메서드를 가진 인터페이스.
- SLEEPING, HUNTING, INVESTIGATING, WANDERING, FLEEING, PASSIVE가 각각 **상태 객체 참조**.
- state는 현재 상태 객체; 단순한 enum 숫자가 아니다.
- Mob.act()는 마비, 도주 효과, 대상 탐지, 현재 state.act(...), 집단 경고 처리 등을 연결([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java:263-317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/mobs/Mob.java#L263-L317)).
- enemySeen과 enemyInFOV는 같은 뜻이 아니다. 전자는 저장된 상황 인식 상태이고 후자는 현재 시야·생존·투명 여부를 조건으로 계산.

## 5. 타격·피해 판정
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java:368-454](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L368-L454), [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java:615-685](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Char.java#L615-L685).
- Char.hit()는 attackSkill과 defenseSkill로 명중 확률 관련 굴림을 처리. 여러 버프/디버프/승천 보정을 거친 뒤 acuRoll >= defRoll 비교.
- 특정 조건에서는 무한 명중/무한 회피에 해당하는 특례가 우선한다.
- Char.attack()은 먼저 명중/무적을 확인하고, 기본 피해량·특성·버프·장비·방어 관련 처리를 이어 나간다.
- **유의:** damageRoll()을 호출한다는 사실만으로 화면에 보이는 최종 피해가 결정되는 것이 아니다. 전투 결과에 영향을 주는 전체 보정과 부수 효과를 추적해야 함.

## 용어 모호성 해설
- **turn**: '영웅이 버튼을 누른 한 번'과 '시뮬레이션이 흐르는 시간'은 일대일 대응하지 않을 수 있다.
- **priority**: 점수가 높을수록 먼저 처리되는 **동시간 우선순위**이지, 모든 액터의 전체 행동속도가 아니다.
- **speed**: Char의 이동/행동 시간에 영향을 주지만, Actor.actPriority와 다른 개념.
- **buff**: 이름만으로 이로운 효과라 판단 금지. Buff.buffType에는 POSITIVE, NEGATIVE, NEUTRAL이 있음.

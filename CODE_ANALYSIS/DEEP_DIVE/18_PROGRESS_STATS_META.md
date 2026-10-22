# 영웅 성장·도전·통계·기록·일지

## 1. 클래스와 성장
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroClass.java): HeroClass enum, initHero()와 클래스별 초기화 메서드, 선택 가능 클래스·문구·스프라이트 참조.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java:197-250](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Hero.java#L197-L250): heroClass, subClass, armorAbility, talents, belongings, STR, HP/HT 등.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/Talent.java): 재능 enum과 효과 추적용 Buff 하위 타입·티어 규칙 등이 함께 정의됨.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/hero/HeroAction.java): 이동·공격·상호작용 등의 행동 요청 데이터.

**해설:** HeroClass는 플레이어의 '직업 선택 종류'를 나타내는 enum이고, Hero는 실제 플레이 중 상태를 가진 객체다. HeroSubClass도 따로 존재하므로 현재 클래스와 서브클래스를 혼동하지 말 것.

## 2. 도전
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java:27-81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Challenges.java#L27-L81):
- NO_FOOD=1, NO_ARMOR=2, NO_HEALING=4, NO_HERBALISM=8
- SWARM_INTELLIGENCE=16, DARKNESS=32, NO_SCROLLS=64
- CHAMPION_ENEMIES=128, STRONGER_BOSSES=256
- MAX_VALUE=511, MAX_CHALS=9
Dungeon.challenges에 비트 마스크로 조합되어 Dungeon.isChallenged(mask)에서 비트 AND를 사용([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java:289-291](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Dungeon.java#L289-L291)).

**해설:** 511은 9개의 플래그 값이 모두 켜졌을 때의 비트 마스크 최댓값을 나타내며, '511가지 난이도 단계'라고 해석할 수 없다.

## 3. 통계
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java:30-90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Statistics.java#L30-L90):
goldCollected, deepestFloor, enemiesSlain, foodEaten, itemsCrafted, ankhsUsed 등 다양한 지표와 탐험/보스/퀘스트 점수를 유지. reset(), storeInBundle(), restoreFromBundle(), preview()가 확인됨.
Statistics.duration은 액터 시간 보정과도 연결([core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java:175-196](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/actors/Actor.java#L175-L196)).

## 4. 랭킹
[core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java:62-83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Rankings.java#L62-L83):
Rankings enum, Record 데이터, submit(), calculateScore(), saveGameData(), loadGameData(), save()/load() 및 정렬 로직. records, latestDaily, dailyScoreHistory 등 보관.
**중요:** 랭킹의 점수 계산과 Statistics 개별 지표는 같은 것이 아님. 점수는 여러 조건과 기록을 조합할 수 있고, 최종 점수는 calculateScore() 구현을 참조해야 함.

## 5. 업적과 일지
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/Badges.java): 업적 조건별 validate*(), 로컬·글로벌 업적 저장, 버전 간 이름 호환.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Journal.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Journal.java): journal.dat 저장과 불러오기.
- [core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Notes.java](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/journal/Notes.java): 랜드마크/열쇠/사용자 메모 등을 담는 Record 계층 및 Bundle 저장.
- 해당 UI는 scenes/JournalScene, windows/Wnd* 등에서 표시함.

**기록 데이터의 범위:** 개별 플레이 저장(game.dat), 전역 기록(rankings.dat, badges.dat, journal.dat 등)은 보관 목적과 갱신 경로가 다르다. '게임 데이터'를 모두 하나의 파일이라고 설명하면 부정확함.

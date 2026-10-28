# Java 파일별 소스 구현 해설 288–303

실제 소스 기준 `bd3a990254e4249458816f4879e93ab87275555b`. 타입·필드·메서드·내부 호출을 정적 추출하였다. 메서드의 역할 설명은 식별자·본문 패턴을 이용한 **분석 후보**이므로 모두 의미 검증된 설명이 아니다. 복잡한 Java 문법·긴 메서드(미리보기 80행)·익명 클래스는 누락/오탐될 수 있다.

## 288. [`Enchanting.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 116행 / 타입 2개 / 필드 9개 / 메서드 3개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L29) `class Enchanting  extends ItemSprite`
- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L31) `enum Phase`

### 변수·상수 (단일 행 선언)

- [L35](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L35) `float FADE_IN_TIME` 초기식: `0.2f`
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L36) `float STATIC_TIME` 초기식: `1.0f`
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L37) `float FADE_OUT_TIME` 초기식: `0.4f`
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L39) `float ALPHA` 초기식: `0.6f`
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L41) `int color`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L43) `Char target`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L45) `Phase phase`
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L46) `float duration`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L47) `float passed`

### 함수·메서드 역할과 내부 연결

- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L49) **`Enchanting(Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: item.image, item.glowing
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L65) **`update()`**: 시간·상태 갱신 / 조건 분기·상태 선택 / 참조 호출: super.update, target.sprite.center, width, height, alpha, scale.set, tint, kill
- [L106](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Enchanting.java#L106) **`show(Char ch, Item item)`**: 개별 처리 / 조건 분기 / 참조 호출: Enchanting, sprite.parent.add

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 289. [`Fireball.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Fireball.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 62행 / 타입 1개 / 필드 1개 / 메서드 2개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Fireball.java#L28) `class Fireball  extends MovieClip`

### 변수·상수 (단일 행 선언)

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Fireball.java#L30) `boolean second` 초기식: `false`

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Fireball.java#L32) **`Fireball()`**: 개별 처리
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Fireball.java#L37) **`Fireball(boolean second)`**: 개별 처리 / 조건 분기 / 참조 호출: PixelScene.landscape, texture, TextureFilm, MovieClip.Animation, anim.frames, play, frame

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 290. [`Flare.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 185행 / 타입 1개 / 필드 7개 / 메서드 7개.

### 타입·상속 선언

- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L40) `class Flare  extends Visual`

### 변수·상수 (단일 행 선언)

- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L42) `float duration` 초기식: `0`
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L43) `float lifespan`
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L45) `boolean lightMode` 초기식: `true`
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L47) `SmartTexture texture`
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L49) `FloatBuffer vertices`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L50) `ShortBuffer indices`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L52) `int nRays`

### 함수·메서드 역할과 내부 연결

- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L54) **`Flare(int nRays, float radius)`**: 개별 처리 / 반복 / 참조 호출: TextureCache.createGradient, allocateDirect, order, ByteOrder.nativeOrder, asFloatBuffer, asShortBuffer, vertices.put, Math.cos, Math.sin
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L107) **`color(int color, boolean lightMode)`**: 개별 처리 / 참조 호출: hardlight
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L114) **`show(Visual visual, float duration)`**: 개별 처리 / 조건 분기 / 참조 호출: point, destinationCenter, visual.center, visual.parent.addToBack, scale.set
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L128) **`show(Group parent, PointF pos, float duration)`**: 개별 처리 / 조건 분기 / 참조 호출: point, parent.add, scale.set
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L139) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, scale.set, alpha, killAndErase
- [L157](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L157) **`draw()`**: 지형/화면 표현 / 조건 분기 / 참조 호출: super.draw, Blending.setLightMode, drawRays, Blending.setNormalMode
- [L170](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Flare.java#L170) **`drawRays()`**: 지형/화면 표현 / 참조 호출: NoosaScript.get, texture.bind, script.uModel.valueM4, script.lighting, script.camera, script.drawElements

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 291. [`FloatingText.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 512행 / 타입 1개 / 필드 55개 / 메서드 17개.

### 타입·상속 선언

- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L68) `class FloatingText  extends RenderedTextBlock`

### 변수·상수 (단일 행 선언)

- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L70) `float LIFESPAN` 초기식: `1f`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L71) `float DISTANCE` 초기식: `DungeonTilemap.SIZE`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L73) `int ICON_WIDTH` 초기식: `7`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L74) `int ICON_HEIGHT` 초기식: `8`
- [L77](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L77) `int NO_ICON` 초기식: `-1`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L80) `int PHYS_DMG` 초기식: `0`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L81) `int PHYS_DMG_NO_BLOCK` 초기식: `1`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L82) `int MAGIC_DMG` 초기식: `2`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L83) `int PICK_DMG` 초기식: `3`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L86) `int HUNGER` 초기식: `5`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L87) `int BURNING` 초기식: `6`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L88) `int SHOCKING` 초기식: `7`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L89) `int FROST` 초기식: `8`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L90) `int WATER` 초기식: `9`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L91) `int BLEEDING` 초기식: `10`
- [L92](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L92) `int TOXIC` 초기식: `11`
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L93) `int CORROSION` 초기식: `12`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L94) `int POISON` 초기식: `13`
- [L95](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L95) `int OOZE` 초기식: `14`
- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L96) `int DEFERRED` 초기식: `15`
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L97) `int CORRUPTION` 초기식: `16`
- [L98](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L98) `int AMULET` 초기식: `17`
- [L101](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L101) `int HEALING` 초기식: `18`
- [L102](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L102) `int SHIELDING` 초기식: `19`
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L103) `int EXPERIENCE` 초기식: `20`
- [L104](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L104) `int STRENGTH` 초기식: `21`
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L107) `int GOLD` 초기식: `23`
- [L108](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L108) `int ENERGY` 초기식: `24`
- [L111](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L111) `int HIT_WEP` 초기식: `36`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L112) `int HIT_ARM` 초기식: `37`
- [L113](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L113) `int HIT_BLS` 초기식: `38`
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L114) `int HIT_HEX` 초기식: `39`
- [L115](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L115) `int HIT_DAZE` 초기식: `40`
- [L116](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L116) `int HIT_ACC` 초기식: `41`
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L117) `int HIT_EVA` 초기식: `42`
- [L118](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L118) `int HIT_LIQ` 초기식: `43`
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L119) `int HIT_DANCE` 초기식: `44`
- [L120](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L120) `int HIT_SUPR` 초기식: `45`
- [L121](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L121) `int HIT_PRES` 초기식: `46`
- [L122](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L122) `int HIT_MOMEN` 초기식: `47`
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L127) `int MISS_WEP` 초기식: `72`
- [L128](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L128) `int MISS_ARM` 초기식: `73`
- [L129](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L129) `int MISS_BLS` 초기식: `74`
- [L130](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L130) `int MISS_HEX` 초기식: `75`
- [L131](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L131) `int MISS_DAZE` 초기식: `76`
- [L132](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L132) `int MISS_ACC` 초기식: `77`
- [L133](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L133) `int MISS_EVA` 초기식: `78`
- [L134](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L134) `int MISS_LIQ` 초기식: `79`
- [L135](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L135) `int MISS_DEF` 초기식: `80`
- [L136](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L136) `int MISS_TUFT` 초기식: `81`
- [L137](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L137) `int MISS_RUN` 초기식: `82`
- [L139](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L139) `Image icon`
- [L140](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L140) `boolean iconLeft`
- [L142](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L142) `float timeLeft`
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L144) `int key` 초기식: `-1`

### 함수·메서드 역할과 내부 연결

- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L75) **`TextureFilm(Assets.Effects.TEXT_ICONS, ICON_WIDTH, ICON_HEIGHT)`**: 개별 처리
- [L148](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L148) **`FloatingText()`**: 개별 처리 / 참조 호출: setHightlighting
- [L154](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L154) **`update()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: super.update, kill, alpha, icon.alpha
- [L179](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L179) **`layout()`**: 지형/화면 표현 / 조건 분기 / 참조 호출: super.layout, left, width, icon.width, PixelScene.align, top
- [L193](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L193) **`width()`**: 개별 처리 / 조건 분기 / 참조 호출: super.width, icon.width
- [L202](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L202) **`kill()`**: 개별 처리 / 조건 분기 / 참조 호출: synchronized, stacks.get, remove, super.kill
- [L213](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L213) **`destroy()`**: 개별 처리 / 참조 호출: kill, super.destroy
- [L218](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L218) **`reset(float x, float y, String text, int color, int iconIdx, boolean left)`**: 생성·초기화 / 조건 분기 / 참조 호출: revive, zoom, text, hardlight, Image, icon.frame, iconFilm.get, add, align
- [L249](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L249) **`show(float x, float y, String text, int color)`**: 개별 처리 / 참조 호출: show
- [L253](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L253) **`show(float x, float y, int key, String text, int color)`**: 개별 처리 / 참조 호출: show
- [L257](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L257) **`show(float x, float y, int key, String text, int color, int iconIdx, boolean left)`**: 개별 처리 / 조건 분기 / 참조 호출: Game.runOnRenderThread, Callback, call, GameScene.status, txt.reset, push
- [L260](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L260) **`call()`**: 개별 처리 / 조건 분기 / 참조 호출: GameScene.status, txt.reset, push
- [L270](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L270) **`push(FloatingText txt, int key)`**: 개별 처리 / 조건 분기·반복 / 참조 호출: synchronized, stacks.get, stacks.put, stack.size, stack.get, above.bottom, below.top, above.setPos, above.left
- [L313](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L313) **`getHitReasonIcon(Char attacker, float accRoll, Char defender, float defRoll)`**: 조회·탐색 / 조건 분기 / 참조 호출: defender.buff, surprisedBy, attacker.buff, belongings.attackingWeapon, hero.belongings.weapon, weapon, belongings.armor, hero.belongings.armor, armor
- [L409](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L409) **`compare(Integer a, Integer b)`**: 개별 처리 / 참조 호출: hitReasons.get, Math.signum
- [L429](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L429) **`getMissReasonIcon(Char attacker, float accRoll, Char defender, float defRoll)`**: 조회·탐색 / 조건 분기·반복 / 참조 호출: defender.buff, belongings.attackingWeapon, hero.belongings.weapon, weapon, belongings.armor, hero.belongings.armor, armor, evasionAndAccuracyFactor, Dungeon.hero.hasTalent
- [L492](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/FloatingText.java#L492) **`compare(Integer a, Integer b)`**: 개별 처리 / 참조 호출: missReasons.get, Math.signum

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 292. [`GlowBlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/GlowBlock.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 65행 / 타입 1개 / 필드 1개 / 메서드 4개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/GlowBlock.java#L28) `class GlowBlock  extends Gizmo`

### 변수·상수 (단일 행 선언)

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/GlowBlock.java#L30) `CharSprite target`

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/GlowBlock.java#L32) **`GlowBlock(CharSprite target)`**: 개별 처리
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/GlowBlock.java#L39) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, target.tint, Math.cos
- [L47](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/GlowBlock.java#L47) **`darken()`**: 개별 처리 / 참조 호출: target.resetColor, killAndErase
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/GlowBlock.java#L54) **`lighten(CharSprite sprite)`**: 개별 처리 / 조건 분기 / 참조 호출: GlowBlock, sprite.parent.add

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 293. [`IceBlock.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/IceBlock.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 74행 / 타입 1개 / 필드 2개 / 메서드 4개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/IceBlock.java#L30) `class IceBlock  extends Gizmo`

### 변수·상수 (단일 행 선언)

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/IceBlock.java#L32) `float phase`
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/IceBlock.java#L34) `CharSprite target`

### 함수·메서드 역할과 내부 연결

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/IceBlock.java#L36) **`IceBlock(CharSprite target)`**: 개별 처리
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/IceBlock.java#L44) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, target.tint
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/IceBlock.java#L54) **`melt()`**: 개별 처리 / 조건 분기 / 참조 호출: target.resetColor, killAndErase, Splash.at, target.center, Sample.INSTANCE.play
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/IceBlock.java#L65) **`freeze(CharSprite sprite)`**: 개별 처리 / 조건 분기 / 참조 호출: IceBlock, sprite.parent.add

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 294. [`Identification.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Identification.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 106행 / 타입 2개 / 필드 2개 / 메서드 5개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Identification.java#L30) `class Identification  extends Group`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Identification.java#L68) `class Speck  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Identification.java#L70) `int COLOR` 초기식: `0x4488CC`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Identification.java#L71) `int SIZE` 초기식: `3`

### 함수·메서드 역할과 내부 연결

- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Identification.java#L45) **`Identification(PointF p)`**: 개별 처리 / 반복 / 참조 호출: add, Speck
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Identification.java#L54) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, countLiving, killAndErase
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Identification.java#L62) **`draw()`**: 지형/화면 표현 / 참조 호출: Blending.setLightMode, super.draw, Blending.setNormalMode
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Identification.java#L73) **`Speck(float x0, float y0, int mx, int my)`**: 개별 처리 / 참조 호출: color, PointF, polar, Random.Float, speed.set, acc.set
- [L97](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Identification.java#L97) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, Math.abs, size

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 295. [`Lightning.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 167행 / 타입 2개 / 필드 7개 / 메서드 13개.

### 타입·상속 선언

- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L36) `class Lightning  extends Group`
- [L107](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L107) `class Arc  extends Group`

### 변수·상수 (단일 행 선언)

- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L38) `float DURATION` 초기식: `0.3f`
- [L40](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L40) `float life`
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L42) `List<Arc> arcs`
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L44) `Callback callback`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L75) `double A` 초기식: `180 / Math.PI`
- [L109](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L109) `Image arc1, arc2`
- [L112](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L112) `PointF start, end`

### 함수·메서드 역할과 내부 연결

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L46) **`Lightning(int from, int to, Callback callback)`**: 개별 처리 / 참조 호출: Arrays.asList, Arc
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L50) **`Lightning(PointF from, int to, Callback callback)`**: 개별 처리 / 참조 호출: Arrays.asList, Arc
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L54) **`Lightning(int from, PointF to, Callback callback)`**: 개별 처리 / 참조 호출: Arrays.asList, Arc
- [L58](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L58) **`Lightning(PointF from, PointF to, Callback callback)`**: 개별 처리 / 참조 호출: Arrays.asList, Arc
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L62) **`Lightning(List<Arc> arcs, Callback callback)`**: 개별 처리 / 반복 / 참조 호출: add
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L78) **`update()`**: 시간·상태 갱신 / 조건 분기·반복 / 참조 호출: killAndErase, callback.call, arc.alpha, super.update
- [L99](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L99) **`draw()`**: 지형/화면 표현 / 참조 호출: Blending.setLightMode, super.draw, Blending.setNormalMode
- [L114](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L114) **`Arc(int from, int to)`**: 개별 처리 / 참조 호출: DungeonTilemap.tileCenterToWorld
- [L119](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L119) **`Arc(PointF from, int to)`**: 개별 처리 / 참조 호출: DungeonTilemap.tileCenterToWorld
- [L123](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L123) **`Arc(int from, PointF to)`**: 개별 처리 / 참조 호출: DungeonTilemap.tileCenterToWorld
- [L127](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L127) **`Arc(PointF from, PointF to)`**: 개별 처리 / 참조 호출: Image, Effects.get, arc1.origin.set, arc1.height, add, arc2.origin.set, arc2.height, update
- [L144](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L144) **`alpha(float alpha)`**: 개별 처리
- [L149](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/Lightning.java#L149) **`update()`**: 시간·상태 갱신 / 참조 호출: Random.Float, Math.atan2, Math.sqrt

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 296. [`MagicMissile.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects` / 본문 719행 / 타입 8개 / 필드 40개 / 메서드 76개.

### 타입·상속 선언

- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L46) `class MagicMissile  extends Emitter`
- [L317](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L317) `class MagicParticle  extends PixelParticle`
- [L378](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L378) `class EarthParticle  extends PixelParticle.Shrinking`
- [L445](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L445) `class ShamanParticle  extends EarthParticle`
- [L511](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L511) `class WhiteParticle  extends PixelParticle`
- [L587](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L587) `class SlowParticle  extends PixelParticle`
- [L633](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L633) `class ForceParticle  extends PixelParticle.Shrinking`
- [L663](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L663) `class WardParticle  extends PixelParticle.Shrinking`

### 변수·상수 (단일 행 선언)

- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L48) `float SPEED` 초기식: `200f`
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L50) `Callback callback`
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L52) `PointF to`
- [L54](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L54) `float sx`
- [L55](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L55) `float sy`
- [L56](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L56) `float time`
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L59) `int MAGIC_MISSILE` 초기식: `0`
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L60) `int FROST` 초기식: `1`
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L61) `int FIRE` 초기식: `2`
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L62) `int CORROSION` 초기식: `3`
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L63) `int FOLIAGE` 초기식: `4`
- [L64](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L64) `int FORCE` 초기식: `5`
- [L65](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L65) `int BEACON` 초기식: `6`
- [L66](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L66) `int SHADOW` 초기식: `7`
- [L67](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L67) `int RAINBOW` 초기식: `8`
- [L68](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L68) `int EARTH` 초기식: `9`
- [L69](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L69) `int WARD` 초기식: `10`
- [L70](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L70) `int SHAMAN_RED` 초기식: `11`
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L71) `int SHAMAN_BLUE` 초기식: `12`
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L72) `int SHAMAN_PURPLE` 초기식: `13`
- [L73](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L73) `int SHAMAN_ELMO` 초기식: `14`
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L74) `int ELMO` 초기식: `15`
- [L75](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L75) `int POISON` 초기식: `16`
- [L76](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L76) `int LIGHT_MISSILE` 초기식: `17`
- [L78](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L78) `int MAGIC_MISS_CONE` 초기식: `100`
- [L79](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L79) `int FROST_CONE` 초기식: `101`
- [L80](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L80) `int FIRE_CONE` 초기식: `102`
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L81) `int CORROSION_CONE` 초기식: `103`
- [L82](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L82) `int FOLIAGE_CONE` 초기식: `104`
- [L83](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L83) `int FORCE_CONE` 초기식: `105`
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L84) `int SHADOW_CONE` 초기식: `107`
- [L85](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L85) `int RAINBOW_CONE` 초기식: `108`
- [L86](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L86) `int EARTH_CONE` 초기식: `109`
- [L87](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L87) `int WARD_CONE` 초기식: `110`
- [L88](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L88) `int PURPLE_CONE` 초기식: `111`
- [L89](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L89) `int SPARK_CONE` 초기식: `112`
- [L90](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L90) `int BLOOD_CONE` 초기식: `113`
- [L91](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L91) `int POISON_CONE` 초기식: `114`
- [L94](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L94) `int SPECK` 초기식: `1000`
- [L589](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L589) `Emitter emitter`

### 함수·메서드 역할과 내부 연결

- [L96](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L96) **`reset(int type, int from, int to, Callback callback)`**: 생성·초기화 / 참조 호출: reset, DungeonTilemap.raisedTileCenterToWorld
- [L103](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L103) **`reset(int type, Visual from, Visual to, Callback callback)`**: 생성·초기화 / 참조 호출: reset, from.center, to.center
- [L110](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L110) **`reset(int type, Visual from, int to, Callback callback)`**: 생성·초기화 / 참조 호출: reset, from.center, DungeonTilemap.raisedTileCenterToWorld
- [L117](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L117) **`reset(int type, PointF from, PointF to, Callback callback)`**: 생성·초기화 / 조건 분기·상태 선택 / 참조 호출: PointF.diff, PointF, normalize, scale, d.length, size, pour, Speck.factory, revive
- [L273](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L273) **`size(float size)`**: 개별 처리
- [L279](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L279) **`setSpeed(float newSpeed)`**: 상태 갱신 / 참조 호출: PointF.diff, PointF, normalize, scale, d.length
- [L288](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L288) **`boltFromChar(Group group, int type, Visual sprite, int to, Callback callback)`**: 개별 처리 / 조건 분기 / 참조 호출: group.recycle, Actor.findChar, missile.reset, sprite.center, sprite.destinationCenter
- [L299](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L299) **`isFrozen()`**: 조건 판정
- [L304](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L304) **`update()`**: 시간·상태 갱신 / 조건 분기 / 참조 호출: super.update, callback.call
- [L319](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L319) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L321](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L321) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L325](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L325) **`lightMode()`**: 개별 처리
- [L330](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L330) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetAttract, lightMode
- [L332](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L332) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetAttract
- [L336](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L336) **`lightMode()`**: 개별 처리
- [L341](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L341) **`MagicParticle()`**: 개별 처리 / 참조 호출: color, speed.set, Random.Float
- [L350](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L350) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive
- [L359](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L359) **`resetAttract(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.polar, Random.Float
- [L371](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L371) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, size
- [L380](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L380) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset
- [L382](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L382) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L387](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L387) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetBurst
- [L389](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L389) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetBurst
- [L394](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L394) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetAttract
- [L396](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L396) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetAttract
- [L401](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L401) **`EarthParticle()`**: 개별 처리 / 참조 호출: acc.set
- [L409](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L409) **`reset(float x, float y)`**: 생성·초기화 / 조건 분기 / 참조 호출: revive, Random.Int, color, ColorMath.random, speed.set, Random.Float
- [L427](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L427) **`resetBurst(float x, float y)`**: 생성·초기화 / 참조 호출: reset, speed.polar, Random.Float
- [L433](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L433) **`resetAttract(float x, float y)`**: 생성·초기화 / 참조 호출: reset, speed.polar, Random.Float, acc.set
- [L447](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L447) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, ColorMath.random
- [L449](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L449) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset, ColorMath.random
- [L455](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L455) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, ColorMath.random
- [L457](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L457) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset, ColorMath.random
- [L463](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L463) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, ColorMath.random
- [L465](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L465) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset, ColorMath.random
- [L471](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L471) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, ColorMath.random, lightMode
- [L473](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L473) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset, ColorMath.random
- [L478](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L478) **`lightMode()`**: 개별 처리
- [L486](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L486) **`ShamanParticle()`**: 개별 처리 / 참조 호출: acc.set
- [L493](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L493) **`reset(float x, float y, int endColor)`**: 생성·초기화 / 참조 호출: super.reset, size, ColorMath.random, speed.set, Random.Float
- [L505](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L505) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, color, ColorMath.interpolate
- [L513](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L513) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L515](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L515) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L519](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L519) **`lightMode()`**: 개별 처리
- [L524](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L524) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L526](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L526) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L530](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L530) **`lightMode()`**: 개별 처리
- [L535](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L535) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetWall, lightMode
- [L537](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L537) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetWall
- [L541](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L541) **`lightMode()`**: 개별 처리
- [L546](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L546) **`WhiteParticle()`**: 개별 처리
- [L554](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L554) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, hardlight
- [L564](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L564) **`reset(float x, float y, float r, float g, float b)`**: 생성·초기화 / 참조 호출: reset, hardlight
- [L569](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L569) **`resetWall(float x, float y)`**: 생성·초기화 / 참조 호출: reset, Math.round
- [L580](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L580) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, size
- [L591](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L591) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L593](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L593) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L597](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L597) **`lightMode()`**: 개별 처리
- [L602](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L602) **`SlowParticle()`**: 개별 처리 / 참조 호출: color, size
- [L611](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L611) **`reset(float x, float y, Emitter emitter)`**: 생성·초기화 / 참조 호출: revive, acc.set, speed.set, Random.Float
- [L625](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L625) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, acc.set
- [L635](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L635) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L637](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L637) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L642](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L642) **`lightMode()`**: 개별 처리
- [L647](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L647) **`reset(int index, float x, float y)`**: 생성·초기화 / 참조 호출: super.reset, ColorMath.interpolate, Random.Float, speed.polar
- [L656](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L656) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update
- [L665](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L665) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L667](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L667) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L671](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L671) **`lightMode()`**: 개별 처리
- [L676](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L676) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetUp, lightMode
- [L678](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L678) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetUp
- [L682](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L682) **`lightMode()`**: 개별 처리
- [L687](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L687) **`WardParticle()`**: 개별 처리 / 참조 호출: color
- [L695](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L695) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive
- [L705](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L705) **`resetUp(float x, float y)`**: 생성·초기화 / 참조 호출: reset, speed.set, Random.Float
- [L712](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/MagicMissile.java#L712) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 297. [`BlastParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BlastParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 66행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BlastParticle.java#L29) `class BlastParticle  extends PixelParticle.Shrinking`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BlastParticle.java#L31) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BlastParticle.java#L33) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BlastParticle.java#L37) **`lightMode()`**: 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BlastParticle.java#L42) **`BlastParticle()`**: 개별 처리 / 참조 호출: color, acc.set
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BlastParticle.java#L49) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, Random.Float, speed.polar
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BlastParticle.java#L62) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 298. [`BloodParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BloodParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 89행 / 타입 1개 / 필드 0개 / 메서드 9개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BloodParticle.java#L30) `class BloodParticle  extends PixelParticle.Shrinking`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BloodParticle.java#L32) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BloodParticle.java#L34) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BloodParticle.java#L39) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetBurst, lightMode
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BloodParticle.java#L41) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetBurst
- [L45](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BloodParticle.java#L45) **`lightMode()`**: 개별 처리
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BloodParticle.java#L50) **`BloodParticle()`**: 개별 처리 / 참조 호출: color, acc.set
- [L59](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BloodParticle.java#L59) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.set
- [L71](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BloodParticle.java#L71) **`resetBurst(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.polar, Random.Float
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/BloodParticle.java#L84) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 299. [`ChallengeParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ChallengeParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 69행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ChallengeParticle.java#L28) `class ChallengeParticle  extends PixelParticle.Shrinking`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ChallengeParticle.java#L30) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ChallengeParticle.java#L32) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ChallengeParticle.java#L36) **`lightMode()`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ChallengeParticle.java#L41) **`ChallengeParticle()`**: 개별 처리 / 참조 호출: color
- [L49](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ChallengeParticle.java#L49) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.set, Random.Float
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ChallengeParticle.java#L62) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 300. [`CorrosionParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/CorrosionParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 93행 / 타입 1개 / 필드 0개 / 메서드 10개.

### 타입·상속 선언

- [L29](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/CorrosionParticle.java#L29) `class CorrosionParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L31](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/CorrosionParticle.java#L31) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetMissile, lightMode
- [L33](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/CorrosionParticle.java#L33) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetMissile
- [L37](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/CorrosionParticle.java#L37) **`lightMode()`**: 개별 처리
- [L42](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/CorrosionParticle.java#L42) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetSplash, lightMode
- [L44](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/CorrosionParticle.java#L44) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetSplash
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/CorrosionParticle.java#L48) **`lightMode()`**: 개별 처리
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/CorrosionParticle.java#L53) **`CorrosionParticle()`**: 개별 처리 / 참조 호출: acc.set
- [L61](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/CorrosionParticle.java#L61) **`resetMissile(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.polar, Random.Float
- [L72](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/CorrosionParticle.java#L72) **`resetSplash(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.polar, Random.Float
- [L84](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/CorrosionParticle.java#L84) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, size, color, ColorMath.interpolate

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 301. [`EarthParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 99행 / 타입 1개 / 필드 0개 / 메서드 11개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java#L30) `class EarthParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java#L32) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java#L34) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L39](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java#L39) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetSmall
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java#L41) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetSmall
- [L46](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java#L46) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, resetFalling
- [L48](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java#L48) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, resetFalling
- [L53](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java#L53) **`EarthParticle()`**: 개별 처리 / 참조 호출: color, ColorMath.random, Random.Float
- [L60](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java#L60) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive
- [L74](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java#L74) **`resetSmall(float x, float y)`**: 생성·초기화 / 참조 호출: reset
- [L81](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java#L81) **`resetFalling(float x, float y)`**: 생성·초기화 / 참조 호출: reset, Random.Float
- [L93](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EarthParticle.java#L93) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, size

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 302. [`ElmoParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ElmoParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 68행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L28](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ElmoParticle.java#L28) `class ElmoParticle  extends PixelParticle.Shrinking`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ElmoParticle.java#L30) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ElmoParticle.java#L32) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L36](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ElmoParticle.java#L36) **`lightMode()`**: 개별 처리
- [L41](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ElmoParticle.java#L41) **`ElmoParticle()`**: 개별 처리 / 참조 호출: color, acc.set
- [L50](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ElmoParticle.java#L50) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive, speed.set
- [L63](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/ElmoParticle.java#L63) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 303. [`EnergyParticle.java`](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EnergyParticle.java)

패키지: `com.shatteredpixel.shatteredpixeldungeon.effects.particles` / 본문 69행 / 타입 1개 / 필드 0개 / 메서드 6개.

### 타입·상속 선언

- [L30](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EnergyParticle.java#L30) `class EnergyParticle  extends PixelParticle`

### 변수·상수 (단일 행 선언)

- 검출 없음

### 함수·메서드 역할과 내부 연결

- [L32](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EnergyParticle.java#L32) **`Factory()`**: 개별 처리 / 참조 호출: emit, emitter.recycle, reset, lightMode
- [L34](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EnergyParticle.java#L34) **`emit(Emitter emitter, int index, float x, float y)`**: 개별 처리 / 참조 호출: emitter.recycle, reset
- [L38](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EnergyParticle.java#L38) **`lightMode()`**: 개별 처리
- [L43](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EnergyParticle.java#L43) **`EnergyParticle()`**: 개별 처리 / 참조 호출: color, speed.polar, Random.Float
- [L52](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EnergyParticle.java#L52) **`reset(float x, float y)`**: 생성·초기화 / 참조 호출: revive
- [L62](https://github.com/ikkinamu/lemon-pixel-dungeon/blob/bd3a990254e4249458816f4879e93ab87275555b/core/src/main/java/com/shatteredpixel/shatteredpixeldungeon/effects/particles/EnergyParticle.java#L62) **`update()`**: 시간·상태 갱신 / 참조 호출: super.update, size, Random.Float

**해설 수준:** 이름에 따른 역할 분류와 본문에서 실제 나타난 호출명은 구분해야 한다. 모든 하위 구현·오버로드·스레드 처리까지 검증한 것이 아니다.

## 정적 분석 수치

{"files":16,"failed":0,"types":26,"fields":124,"methods":185}

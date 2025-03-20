# CSS3 변형과 애니메이션, CSS3 변환

Date: 2025년 3월 20일
페이지: p.401~449
완료: Yes
1일후 복습: No
7일후(주말) 복습: No
1달후 복습: No

# CSS3 변형과 애니메이션 요약본

## 1. CSS3 변형 속성(Transition Properties)

CSS3에서는 움직임을 구현하는 기능이 **변형 속성**과 **애니메이션 속성**으로 나뉩니다. 변형 속성은 특히 부드러운 애니메이션을 적용할 때 필요합니다.

### 1.1 변형 가능한 CSS 속성들

- 위치 속성: top, left, bottom, right
- 크기 속성: width, height
- 박스 속성: margin, padding
- 테두리 속성: border-width, border-radius, border-color
- 색상 속성: color, background-color
- 투명도 속성: opacity
- 변환 속성: transform

### 1.2 변형 속성 종류

| 속성 | 설명 | 예시 |
| --- | --- | --- |
| transition | 모든 transition 속성을 한번에 사용 | `transition: all 1s ease;` |
| transition-delay | 이벤트 발생 후 지연 시간 지정 | `transition-delay: 0.5s;` |
| transition-duration | 변형이 진행되는 시간 지정 | `transition-duration: 1s;` |
| transition-property | 어떤 속성을 변형할지 지정 | `transition-property: width, height;` |
| transition-timing-function | 수치 변형 함수를 지정 | `transition-timing-function: ease;` |

### 1.3 transition-timing-function 값

수치를 변형하는 함수를 지정할 때 사용하는 속성으로 다음 값들을 사용할 수 있습니다:

- ease: 느리게 시작해서 빨라졌다가 다시 느려짐
- linear: 일정한 속도로 변화
- ease-in: 느리게 시작해서 점점 빨라짐
- ease-out: 빠르게 시작해서 점점 느려짐
- ease-in-out: 느리게 시작해서 빨라졌다가 다시 느려짐
- cubic-bezier(n,n,n,n): 사용자 정의 베지어 곡선

## 2. 키 프레임과 애니메이션 속성

### 2.1 애니메이션 속성 종류

| 속성 | 설명 | 예시 |
| --- | --- | --- |
| animation | 모든 animation 속성을 한번에 적용 | `animation: move 2s infinite alternate;` |
| animation-delay | 애니메이션 시작 지연 시간 | `animation-delay: 1s;` |
| animation-direction | 애니메이션 진행 방향 설정 | `animation-direction: alternate;` |
| animation-duration | 애니메이션 재생 시간 | `animation-duration: 2s;` |
| animation-iteration-count | 애니메이션 반복 횟수 | `animation-iteration-count: 3;` |
| animation-name | 키프레임 이름 지정 | `animation-name: move;` |
| animation-play-state | 애니메이션 재생 상태 지정 | `animation-play-state: paused;` |
| animation-timing-function | 수치 변형 함수 지정 | `animation-timing-function: ease-in;` |

### 2.2 @keyframes 규칙

키프레임 규칙을 사용해 애니메이션을 정의합니다.

```css
@keyframes 이름 {
    0% { /* 시작 스타일 */ }
    50% { /* 중간 스타일 */ }
    100% { /* 끝 스타일 */ }
}

```

예제:

```css
@keyframes move {
    from { left: 0; }  /* 0%와 동일 */
    to { left: 300px; } /* 100%와 동일 */
}

```

### 2.3 animation-direction 값

| 값 | 설명 |
| --- | --- |
| normal | 계속 from에서 to로 이동 (기본값) |
| alternate | from→to로 이동 후 to→from으로 이동을 반복 |
| reverse | to에서 from으로 이동 |
| alternate-reverse | to→from으로 이동 후 from→to로 이동을 반복 |

### 2.4 animation-play-state 값

| 값 | 설명 |
| --- | --- |
| running | 애니메이션 재생 (기본값) |
| paused | 애니메이션 중지 |

## 3. CSS3 변환 (Transform)

### 3.1 2차원 변환 함수

| 함수 | 설명 | 예시 |
| --- | --- | --- |
| translate(x, y) | 특정 크기만큼 이동 | `transform: translate(100px, 50px);` |
| translateX(x) | X축으로 이동 | `transform: translateX(100px);` |
| translateY(y) | Y축으로 이동 | `transform: translateY(50px);` |
| scale(x, y) | 크기 확대/축소 | `transform: scale(2, 1.5);` |
| scaleX(x) | X축으로 확대/축소 | `transform: scaleX(2);` |
| scaleY(y) | Y축으로 확대/축소 | `transform: scaleY(1.5);` |
| skew(x-angle, y-angle) | 특정 각도만큼 기울임 | `transform: skew(30deg, 15deg);` |
| skewX(angle) | X축으로 기울임 | `transform: skewX(30deg);` |
| skewY(angle) | Y축으로 기울임 | `transform: skewY(15deg);` |
| rotate(angle) | 특정 각도만큼 회전 | `transform: rotate(45deg);` |

※ 중요: transform 속성에 함수를 공백으로 구분하여 여러 개 입력할 수 있으며, **적용 순서**에 따라 결과가 달라집니다.

### 3.2 transform-origin 속성

변환의 중심점을 설정하는 속성으로, 기본값은 요소의 중심(50% 50%)입니다.

```css
/* 키워드 값 사용 */
transform-origin: top left;

/* 퍼센트 값 사용 */
transform-origin: 25% 75%;

/* 픽셀 값 사용 */
transform-origin: 100px 50px;

```

### 3.3 3차원 변환 함수

| 함수 | 설명 | 예시 |
| --- | --- | --- |
| translate3d(x, y, z) | 3D 공간에서 이동 | `transform: translate3d(100px, 50px, 25px);` |
| translateZ(z) | Z축으로 이동 | `transform: translateZ(25px);` |
| scale3d(x, y, z) | 3D 공간에서 확대/축소 | `transform: scale3d(2, 1.5, 1);` |
| scaleZ(z) | Z축으로 확대/축소 | `transform: scaleZ(1.5);` |
| rotate3d(x, y, z, angle) | 3D 공간에서 회전 | `transform: rotate3d(1, 1, 1, 45deg);` |
| rotateX(angle) | X축을 중심으로 회전 | `transform: rotateX(45deg);` |
| rotateY(angle) | Y축을 중심으로 회전 | `transform: rotateY(45deg);` |
| rotateZ(angle) | Z축을 중심으로 회전 | `transform: rotateZ(45deg);` |

### 3.4 transform-style 속성

자식 요소들이 3D 공간에 배치될지 여부를 결정합니다.

| 값 | 설명 | 예시 |
| --- | --- | --- |
| flat | 자식 요소의 3D 속성을 무시 (기본값) | `transform-style: flat;` |
| preserve-3d | 자식 요소의 3D 속성을 유지 | `transform-style: preserve-3d;` |

### 3.5 backface-visibility 속성

3D 변환으로 회전된 요소의 뒷면 표시 여부를 결정합니다.

| 값 | 설명 | 예시 |
| --- | --- | --- |
| visible | 요소의 뒷면을 표시 (기본값) | `backface-visibility: visible;` |
| hidden | 요소의 뒷면을 숨김 | `backface-visibility: hidden;` |

### 3.6 perspective 속성

3D 변환 요소에 원근감을 부여합니다. 값이 작을수록 더 강한 원근감이 적용됩니다.

```css
/* 부모 요소에 적용 */
.container {
    perspective: 1000px;
}

/* 또는 transform 함수로 직접 적용 */
.element {
    transform: perspective(1000px) rotateY(45deg);
}

```

일반적으로 400~2000px 사이의 값을 사용합니다.

---

## 최종 요약

### 1. CSS3 변형(Transition)

- 요소의 상태 변화를 부드럽게 애니메이션화
- transition 속성으로 통합 사용 가능
- timing-function으로 변화 속도 곡선 조절
- 특정 속성만 변형시킬 수 있음

### 2. CSS3 애니메이션(Animation)

- @keyframes 규칙으로 복잡한 애니메이션 정의
- 다양한 속성(지속시간, 반복횟수, 방향 등) 조절 가능
- JavaScript 없이도 복잡한 동작 구현 가능
- 필수 속성: animation-name, animation-duration

### 3. CSS3 변환(Transform)

- 2D 변환: translate(), scale(), rotate(), skew() 함수로 요소 변형
- 3D 변환: translate3d(), rotate3d() 등으로 3차원 효과 구현
- transform-origin으로 변환 중심점 설정
- transform-style과 backface-visibility로 3D 효과 제어
- perspective로 원근감 부여

# CSS3 변형과 애니메이션 복습 퀴즈

## 문제 1

CSS3에서 애니메이션 재생 시간을 지정하는 속성은 무엇인가요?

1. animation-time
2. animation-duration
3. animation-speed
4. animation-length

**정답**: 2. animation-duration

**해설**: animation-duration 속성은 애니메이션이 한 사이클을 완료하는 데 걸리는 시간을 초(s) 또는 밀리초(ms) 단위로 지정합니다. 이 속성은 animation 속성을 사용할 때 필수적으로 지정해야 하는 속성 중 하나입니다.

## 문제 2

다음 중 CSS3의 변형 속성(transition)에 포함되지 않는 것은?

1. transition-delay
2. transition-duration
3. transition-direction
4. transition-timing-function

**정답**: 3. transition-direction

**해설**: transition-direction은 존재하지 않는 속성입니다. CSS3 변형 속성에는 transition-delay(지연 시간), transition-duration(지속 시간), transition-property(변형할 속성), transition-timing-function(수치 변형 함수)이 있으며, animation 속성에는 animation-direction이 있습니다.

## 문제 3

CSS3에서 요소를 회전시키는 transform 함수는?

1. translate()
2. skew()
3. rotate()
4. scale()

**정답**: 3. rotate()

**해설**: rotate() 함수는 요소를 특정 각도만큼 회전시키는 transform 함수입니다. 예를 들어 `transform: rotate(45deg);`는 요소를 시계 방향으로 45도 회전시킵니다. 반면 translate()는 이동, skew()는 기울임, scale()은 크기 변경을 담당합니다.

## 문제 4

CSS3 애니메이션에서 애니메이션을 무한 반복하도록 설정하는 값은?

1. continuous
2. repeat
3. loop
4. infinite

**정답**: 4. infinite

**해설**: animation-iteration-count 속성에 infinite 값을 지정하면 애니메이션이 무한히 반복됩니다. 예: `animation-iteration-count: infinite;`

## 문제 5

3D 공간에서 자식 요소의 3D 속성을 유지하기 위해 부모 요소에 설정해야 하는 속성과 값은?

1. transform: preserve-3d;
2. transform-style: 3d-space;
3. transform-style: preserve-3d;
4. perspective: preserve-3d;

**정답**: 3. transform-style: preserve-3d;

**해설**: 3D 공간에서 자식 요소의 3D 속성을 유지하기 위해서는 부모 요소에 `transform-style: preserve-3d;`를 설정해야 합니다. 이 속성이 없으면 자식 요소들은 평면(2D)에 투영되어 3D 효과가 제대로 표현되지 않습니다.

## 문제 6

@keyframes 규칙에서 애니메이션의 시작 상태를 나타내는 키워드는?

1. start
2. begin
3. from
4. initial

**정답**: 3. from

**해설**: @keyframes 규칙에서 애니메이션의 시작 상태는 `from` 키워드(또는 `0%`)로 나타냅니다. 끝 상태는 `to` 키워드(또는 `100%`)로 나타냅니다. 예: `@keyframes move { from { left: 0; } to { left: 300px; } }`

## 문제 7

CSS transition-timing-function 속성의 기본값은?

1. linear
2. ease
3. ease-in
4. ease-out

**정답**: 2. ease

**해설**: transition-timing-function 속성의 기본값은 ease로, 애니메이션이 느리게 시작해서 빨라졌다가 다시 느려지는 형태를 가집니다.

## 문제 8

3D 공간에서 원근감을 부여하는 CSS 속성은?

1. depth
2. perspective
3. view-distance
4. 3d-depth

**정답**: 2. perspective

**해설**: perspective 속성은 3D 공간에서 원근감(깊이)을 부여하는 속성으로, 일반적으로 400~2000px 사이의 값을 사용합니다. 값이 작을수록 더 강한 원근감이 적용됩니다.

## 문제 9

3D 변환에서 요소의 뒷면을 숨기는 속성과 값은?

1. hide-backface: true;
2. backface: hidden;
3. backface-visibility: hidden;
4. back-visibility: none;

**정답**: 3. backface-visibility: hidden;

**해설**: backface-visibility 속성에 hidden 값을 적용하면 3D 공간에서 회전된 요소의 뒷면이 보이지 않게 됩니다. 이 속성은 주로 카드 뒤집기 같은 효과를 구현할 때 사용됩니다.

## 문제 10

다음 중 애니메이션을 from→to로 이동 후 to→from으로 이동하는 방식으로 반복하게 하는 animation-direction 값은?

1. reverse
2. alternate
3. toggle
4. back-forth

**정답**: 2. alternate

**해설**: animation-direction 속성의 alternate 값은 애니메이션이 from→to로 이동한 후 다음 반복에서는 to→from으로 이동하는 방식으로 진행됩니다. 이렇게 하면 애니메이션이 부드럽게 왕복하는 효과를 만들 수 있습니다.

# CSS3 변형과 애니메이션 연습문제

## 연습문제 1: 버튼 호버 효과 구현하기

### 문제

다음 요구사항에 맞는 버튼 호버 효과를 구현하세요:

- 기본 상태: 배경색 #3498db, 글자색 흰색, 패딩 10px 20px
- 호버 상태: 배경색 #2980b9로 변경, 크기 1.1배 확대, 그림자 효과 추가
- 모든 효과는 0.3초 동안 부드럽게 변화해야 함
- 크기 변화의 기준점은 버튼의 중앙이어야 함

### 정답

```css
.button {
  background-color: #3498db;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: all 0.3s ease;
  transform-origin: center;
}

.button:hover {
  background-color: #2980b9;
  transform: scale(1.1);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
}

```

### 해설

- `transition: all 0.3s ease;`로 모든 속성 변화에 0.3초의 전환 효과를 적용
- `transform-origin: center;`로 변형의 중심점을 요소의 중앙으로 설정
- `:hover` 가상 클래스로 마우스 오버 시 스타일 변경
- `transform: scale(1.1);`로 호버 시 요소를 1.1배 확대
- `box-shadow`로 그림자 효과 추가

## 연습문제 2: 로딩 스피너 애니메이션 만들기

### 문제

무한 회전하는 로딩 스피너를 CSS3 애니메이션으로 구현하세요:

- 직경 50px의 원형
- 테두리는 5px 두께의 반투명한 회색(rgba(0, 0, 0, 0.1))
- 위쪽 테두리만 파란색(#3498db)
- 1초에 한 바퀴씩 무한히 회전
- 회전 애니메이션은 일정한 속도로 진행

### 정답

```css
.spinner {
  width: 50px;
  height: 50px;
  border: 5px solid rgba(0, 0, 0, 0.1);
  border-top: 5px solid #3498db;
  border-radius: 50%;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

```

### 해설

- `.spinner` 클래스로 원형 요소 스타일 정의
- `border-radius: 50%;`로 원형 모양 생성
- `border`로 모든 테두리를 반투명 회색으로 설정
- `border-top`으로 위쪽 테두리만 파란색으로 오버라이드
- `@keyframes spin`으로 회전 애니메이션 정의
- `animation: spin 1s linear infinite;`로 애니메이션 적용
    - `spin`: 사용할 키프레임 이름
    - `1s`: 한 바퀴 회전에 1초 소요
    - `linear`: 일정한 속도로 회전
    - `infinite`: 무한 반복

## 연습문제 3: 3D 카드 뒤집기 효과 구현하기

### 문제

마우스 호버 시 Y축을 기준으로 뒤집히는 3D 카드 효과를 구현하세요:

- 카드 크기: 너비 300px, 높이 200px
- 앞면: 파란색 배경
- 뒷면: 빨간색 배경
- 앞면과 뒷면 모두에 글자 중앙 정렬
- 호버 시 카드가 Y축을 기준으로 180도 회전
- 뒷면의 텍스트가 올바르게 보이도록 구현
- 회전 시간은 0.8초, 부드러운 가속/감속 효과 적용

### 정답

```css
.card-container {
  width: 300px;
  height: 200px;
  perspective: 1000px;
}

.card {
  width: 100%;
  height: 100%;
  position: relative;
  transform-style: preserve-3d;
  transition: transform 0.8s ease;
}

.card:hover {
  transform: rotateY(180deg);
}

.front, .back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  font-size: 24px;
}

.front {
  background-color: #3498db;
}

.back {
  background-color: #e74c3c;
  transform: rotateY(180deg);
}

```

### 해설

- `.card-container`에 `perspective: 1000px;`로 3D 공간 정의
- `.card`에 `transform-style: preserve-3d;`로 자식 요소의 3D 효과 유지
- `.front`와 `.back`에 `backface-visibility: hidden;`으로 뒷면 감춤
- `.back`에 `transform: rotateY(180deg);`로 초기 상태에서 뒤집어 놓음
- `:hover` 시 카드에 `transform: rotateY(180deg);`를 적용해 회전
- `transition: transform 0.8s ease;`로 부드러운 회전 효과 적용
- `display: flex; justify-content: center; align-items: center;`로 텍스트 중앙 정렬

## 연습문제 4: 순차적으로 나타나는 메뉴 아이템 구현하기

### 문제

페이지 로드 시 메뉴 아이템이 위에서 아래로 순차적으로 나타나는 효과를 구현하세요:

- 메뉴 아이템은 5개
- 각 아이템은 처음에 약간 위에 위치하고 투명한 상태
- 최종적으로 원래 위치로 이동하며 완전히 불투명해짐
- 각 아이템은 이전 아이템보다 0.2초 늦게 애니메이션 시작
- 각 아이템의 애니메이션 지속 시간은 0.5초
- 애니메이션 종료 후 최종 상태 유지

### 정답

```css
.menu-item {
  opacity: 0;
  transform: translateY(-20px);
  animation: fadeInDown 0.5s forwards;
}

.menu-item:nth-child(1) { animation-delay: 0.1s; }
.menu-item:nth-child(2) { animation-delay: 0.3s; }
.menu-item:nth-child(3) { animation-delay: 0.5s; }
.menu-item:nth-child(4) { animation-delay: 0.7s; }
.menu-item:nth-child(5) { animation-delay: 0.9s; }

@keyframes fadeInDown {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

```

### 해설

- 초기 상태에서 `.menu-item`은 `opacity: 0;`과 `transform: translateY(-20px);`로 투명하고 위로 이동
- `@keyframes fadeInDown`으로 최종 상태(불투명하고 원래 위치)만 정의
- `animation: fadeInDown 0.5s forwards;`로 애니메이션 적용
    - `forwards` 값으로 애니메이션 완료 후 최종 상태 유지
- `:nth-child()` 선택자로 각 아이템에 다른 `animation-delay` 적용
- 각 아이템은 이전 아이템보다 0.2초 늦게 시작(0.1s, 0.3s, 0.5s, 0.7s, 0.9s)

## 연습문제 5: 인터랙티브 진행 표시줄 구현하기

### 문제

마우스 호버 시 채워지는 진행 표시줄을 구현하세요:

- 진행 표시줄 크기: 너비 300px, 높이 10px
- 기본 상태: 회색 배경에 빈 진행 표시줄
- 호버 시: 왼쪽에서 오른쪽으로 파란색으로 채워짐
- 채워지는 시간: 2초
- 채워지는 속도: 처음에는 빠르게, 끝에는 느리게
- 마우스가 떠나면 원래 상태로 돌아감 (시간: 0.5초, 일정한 속도)

### 정답

```css
.progress-bar {
  width: 300px;
  height: 10px;
  background-color: #e0e0e0;
  border-radius: 5px;
  position: relative;
  overflow: hidden;
}

.progress-bar::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 100%;
  background-color: #3498db;
  transition: width 0.5s linear;
}

.progress-bar:hover::after {
  width: 100%;
  transition: width 2s ease-out;
}

```

### 해설

- `.progress-bar`는 회색 배경의 컨테이너
- `::after` 가상 요소를 사용해 진행 표시줄 구현
- 기본 상태에서 `::after`의 `width: 0;`로 진행 표시줄이 보이지 않음
- `overflow: hidden;`으로 진행 표시줄이 컨테이너를 벗어나지 않도록 설정
- 호버 시 `width: 100%;`로 진행 표시줄이 완전히 채워짐
- `transition: width 2s ease-out;`으로 호버 시 2초 동안 ease-out 타이밍으로 채워짐
    - ease-out: 처음에 빠르게, 끝에 느리게
- 마우스가 떠났을 때는 `transition: width 0.5s linear;`로 0.5초 동안 일정한 속도로 원래 상태로 돌아감
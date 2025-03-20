# CSS3 스타일 속성 기본 part1

Date: 2025년 3월 4일
페이지: p.157~p.184
완료: Yes
1일후 복습: Yes
7일후(주말) 복습: Yes
1달후 복습: No

# CSS 기본 단위 및 속성 종합 요약본

## 1. CSS 단위

CSS에서 크기, 색상 등을 지정할 때 사용하는 다양한 단위들에 대한 설명입니다.

### 1.1 크기 단위

크기를 지정할 때 사용하는 단위로, 절대 단위와 상대 단위로 구분할 수 있습니다.

| 단위 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `%` | 부모 요소의 크기에 비례하는 백분율 | 반응형 디자인, 부모 요소에 상대적인 크기가 필요할 때 | `width: 50%;` |
| `em` | 해당 요소의 폰트 크기를 기준으로 한 배수 | 폰트 크기에 비례하는 요소를 설계할 때 | `font-size: 1.2em;` |
| `px` | 화면의 픽셀 단위, 고정된 크기 | 정확한 크기 지정이 필요할 때 | `margin: 10px;` |
| `rem` | 루트 요소(html)의 폰트 크기를 기준으로 한 배수 | 일관된 크기 비율을 유지할 때 | `padding: 2rem;` |
| `vh`, `vw` | 뷰포트 높이/너비의 백분율 | 화면 크기에 따라 동적으로 조절할 때 | `height: 100vh;` |

### 1.2 색상 단위

색상을 표현하는 다양한 방식으로, 각각 다른 특성과 사용 목적을 가집니다.

| 단위 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| Hex 코드 | 16진수 색상 코드 (#RRGGBB) | 웹 디자인에서 가장 일반적인 색상 지정 방식 | `color: #ff5722;` |
| RGB | 빨강(R), 초록(G), 파랑(B) 값으로 색상 지정 | 각 색상 채널을 개별적으로 조절할 때 | `background-color: rgb(255, 204, 0);` |
| RGBA | RGB + 알파(투명도) | 투명도가 필요한 색상에 사용 | `color: rgba(0, 0, 0, 0.5);` |
| HSL | 색조(H), 채도(S), 밝기(L)로 색상 지정 | 색상 조정이 직관적으로 필요할 때 | `background: hsl(120, 100%, 50%);` |
| HSLA | HSL + 알파(투명도) | 색조 기반 + 투명도 조절이 필요할 때 | `background: hsla(120, 100%, 50%, 0.5);` |

### 1.3 URL 단위

외부 리소스의 경로를 지정할 때 사용하는 함수형 값입니다.

| 함수 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `url()` | 외부 리소스 경로 지정 | 배경 이미지, 폰트, 기타 외부 자원 참조 시 | `background-image: url('images/bg.jpg');` |

## 2. 가시 속성

요소의 가시성과 표시 방식을 제어하는 속성들입니다.

### 2.1 display 속성

요소가 화면에 어떻게 표시될지를 결정하는 핵심 속성입니다.

| 속성값 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `none` | 요소를 화면에서 완전히 제거 (공간도 차지하지 않음) | 요소를 숨기거나 동적으로 표시/숨김 처리할 때 | `display: none;` |
| `block` | 줄바꿈이 발생하며 너비가 부모 요소의 100%를 차지 | 단락, 제목, 구분된 컨텐츠 블록에 사용 | `display: block;` |
| `inline` | 줄바꿈 없이 콘텐츠 크기만큼만 공간 차지 | 텍스트 중간에 들어가는 요소(링크, 강조 등)에 사용 | `display: inline;` |
| `inline-block` | 인라인 요소처럼 줄바꿈 없이 배치되면서 블록 속성(너비, 높이 등) 지정 가능 | 가로로 배치하면서 크기 조절이 필요한 요소 | `display: inline-block;` |
| `flex` | 플렉스 박스 레이아웃 사용 | 1차원(행 또는 열) 레이아웃 구성 시 | `display: flex;` |
| `grid` | 그리드 레이아웃 사용 | 2차원(행과 열) 레이아웃 구성 시 | `display: grid;` |

### 2.2 visibility 속성

요소의 가시성을 제어하되, 레이아웃에는 다른 영향을 줍니다.

| 속성값 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `visible` | 요소를 정상적으로 표시 (기본값) | 기본 상태 | `visibility: visible;` |
| `hidden` | 요소는 보이지 않지만, 공간은 그대로 유지 | 요소의 공간을 유지하면서 일시적으로 숨길 때 | `visibility: hidden;` |
| `collapse` | 테이블 요소에서 행/열을 접을 때 사용 | 테이블 행/열을 시각적으로 제거할 때 | `visibility: collapse;` |

### 2.3 opacity 속성

요소의 투명도를 조절하는 속성입니다.

| 속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `opacity` | 투명도 지정 (0: 완전 투명, 1: 완전 불투명) | 페이드 효과, 반투명 오버레이 등 | `opacity: 0.8;` |

**display, visibility, opacity 비교:**

| 속성 | 시각적 효과 | 공간 점유 | 이벤트 처리 | 애니메이션 가능 |
| --- | --- | --- | --- | --- |
| `display: none` | 완전히 보이지 않음 | 공간도 제거됨 | 이벤트 불가 | 불가능 |
| `visibility: hidden` | 보이지 않음 | 공간은 유지 | 이벤트 불가 | 불가능 (visible/hidden만 가능) |
| `opacity: 0` | 보이지 않음 | 공간은 유지 | 이벤트 가능 | 가능 (점진적 변화) |

## 3. 박스 속성

HTML 요소의 크기와 공간을 제어하는 속성들입니다.

### 3.1 박스 모델 관련 속성

요소의 크기, 여백, 테두리를 다루는 속성들입니다.

| 속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `width`, `height` | 요소의 너비와 높이 | 요소의 크기를 지정할 때 | `width: 300px; height: 200px;` |
| `margin` | 요소 외부의 여백 | 요소 간 간격 조절, 중앙 정렬 등 | `margin: 10px 20px;` (상하 10px, 좌우 20px) |
| `padding` | 요소 내부의 여백 | 내용과 테두리 사이 간격 조절 | `padding: 15px;` |
| `box-sizing` | 요소 크기 계산 방식 지정 | 레이아웃 계산 방식 변경 | `box-sizing: border-box;` |

**box-sizing 속성값:**

| 값 | 설명 | 예시 코드 |
| --- | --- | --- |
| `content-box` | 기본값. width/height는 내용 영역만 포함 | `box-sizing: content-box;` |
| `border-box` | width/height에 padding과 border까지 포함 | `box-sizing: border-box;` |

**margin 축약 속성:**

| 문법 | 설명 | 예시 코드 |
| --- | --- | --- |
| `margin: 값1개;` | 상하좌우 모두 동일한 값 | `margin: 10px;` |
| `margin: 값2개;` | 상하, 좌우 각각 지정 | `margin: 10px 20px;` |
| `margin: 값3개;` | 상, 좌우, 하 순서로 지정 | `margin: 10px 20px 15px;` |
| `margin: 값4개;` | 상, 우, 하, 좌 시계 방향으로 지정 | `margin: 10px 20px 15px 5px;` |

## 4. 테두리 속성

요소의 테두리를 지정하는 속성들입니다.

| 속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `border-width` | 테두리 두께 | 테두리 굵기 지정 | `border-width: 2px;` |
| `border-style` | 테두리 종류 | 테두리 패턴 지정 | `border-style: solid;` |
| `border-color` | 테두리 색상 | 테두리 색 지정 | `border-color: #333;` |
| `border` | 테두리 속성 축약형 | 세 가지 속성을 한 번에 지정 | `border: 1px solid black;` |
| `border-radius` | 모서리 둥글기 | 요소 모서리를 둥글게 처리 | `border-radius: 10px;` |

**border-style 주요 값:**

| 값 | 설명 | 예시 코드 |
| --- | --- | --- |
| `solid` | 실선 | `border-style: solid;` |
| `dotted` | 점선 | `border-style: dotted;` |
| `dashed` | 파선 | `border-style: dashed;` |
| `double` | 이중선 | `border-style: double;` |
| `none` | 테두리 없음 | `border-style: none;` |

**border-radius 응용:**

| 문법 | 설명 | 예시 코드 |
| --- | --- | --- |
| `border-radius: 값1개;` | 모든 모서리에 동일한 둥글기 적용 | `border-radius: 10px;` |
| `border-radius: 값2개;` | 좌상단/우하단, 우상단/좌하단 각각 지정 | `border-radius: 10px 20px;` |
| `border-radius: 값4개;` | 좌상단, 우상단, 우하단, 좌하단 순서로 지정 | `border-radius: 10px 20px 15px 5px;` |
| `border-radius: 50%;` | 원형 또는 타원형 모양 생성 | `border-radius: 50%;` |

## 최종 요약

### 1. CSS 단위

CSS에서는 다양한 단위를 사용하여 크기와 값을 지정합니다. **크기 단위**로는 고정 크기인 `px`, 상대적 크기인 `%`, `em`, `rem`, `vh/vw` 등이 있으며, **색상 단위**로는 Hex 코드(`#RRGGBB`), RGB/RGBA, HSL/HSLA 등이 있습니다. 외부 리소스 참조 시에는 `url()` 함수를 사용합니다.

### 2. 가시 속성

요소의 표시 방식과 가시성을 제어하는 속성들입니다. **display** 속성은 요소의 박스 유형을 결정하며, `block`, `inline`, `inline-block`, `flex`, `grid` 등이 있습니다. **visibility** 속성(`visible`, `hidden`, `collapse`)은 요소의 가시성을 제어하되 레이아웃 공간은 유지합니다. **opacity** 속성은 0부터 1까지의 값으로 요소의 투명도를 조절합니다.

### 3. 박스 속성

HTML 요소의 크기와 여백을 제어하는 속성들입니다. **width/height**는 요소의 너비와 높이를, **margin**은 외부 여백을, **padding**은 내부 여백을 설정합니다. **box-sizing** 속성은 요소의 크기 계산 방식을 결정합니다(`content-box`는 내용 영역만, `border-box`는 테두리까지 포함).

### 4. 테두리 속성

요소 주변의 테두리를 정의하는 속성들입니다. **border-width**는 두께, **border-style**은 종류(solid, dotted, dashed 등), **border-color**는 색상을 지정합니다. **border** 축약 속성으로 한 번에 설정이 가능하며, **border-radius**로 모서리의 둥글기를 조절할 수 있습니다.

이러한 CSS 속성들을 적절히 조합하면 웹 페이지의 레이아웃, 디자인, 사용자 인터페이스를 효과적으로 구성할 수 있습니다.

# CSS 기본 단위 및 속성 복습 퀴즈

## 1. 다음 중 부모 요소의 크기에 상대적인 크기를 지정하는 단위는?

A) `px`

B) `em`

C) `%`

D) `vh`

**정답: C) `%`**

**해설:** 백분율(`%`) 단위는 부모 요소의 크기에 비례하여 크기를 지정합니다. 예를 들어 `width: 50%`는 부모 요소 너비의 절반을 차지합니다. `px`은 절대 단위이고, `em`은 해당 요소의 폰트 크기를 기준으로 한 상대 단위, `vh`는 뷰포트 높이에 대한 상대 단위입니다.

## 2. `display: inline-block`의 특징으로 올바른 것은?

A) 항상 새로운 줄에서 시작하며 가능한 모든 너비를 차지한다

B) 내용물의 크기만큼만 공간을 차지하며 width와 height를 지정할 수 없다

C) 내용물의 크기만큼 공간을 차지하며 width와 height를 지정할 수 있다

D) 요소를 화면에서 완전히 제거한다

**정답: C) 내용물의 크기만큼 공간을 차지하며 width와 height를 지정할 수 있다**

**해설:** `display: inline-block`은 인라인 요소와 블록 요소의 특성을 모두 갖습니다. 인라인 요소처럼 한 줄에 여러 요소가 배치될 수 있지만, 블록 요소처럼 width, height, margin, padding 등의 속성을 지정할 수 있습니다. 이는 요소들을 가로로 배치하면서도 크기를 제어해야 할 때 유용합니다.

## 3. `visibility: hidden`과 `display: none`의 차이점은?

A) 차이가 없다

B) `visibility: hidden`은 요소를 보이지 않게 하지만 공간은 유지하고, `display: none`은 요소와 그 공간을 모두 제거한다

C) `visibility: hidden`은 요소를 반투명하게 만들고, `display: none`은 요소를 완전히 투명하게 만든다

D) `visibility: hidden`은 요소를 화면 밖으로 이동시키고, `display: none`은 요소의 크기를 0으로 만든다

**정답: B) `visibility: hidden`은 요소를 보이지 않게 하지만 공간은 유지하고, `display: none`은 요소와 그 공간을 모두 제거한다**

**해설:** 두 속성의 핵심 차이점은 레이아웃에 미치는 영향입니다. `visibility: hidden`을 사용하면 요소는 보이지 않지만 여전히 공간을 차지합니다(빈 공간으로 남음). 반면 `display: none`을 사용하면 요소가 DOM에서 렌더링되지 않아 공간도 차지하지 않고 완전히 사라집니다. 이 차이는 페이지 레이아웃에 영향을 주지 않으면서 요소를 숨길지, 아니면 레이아웃까지 변경할지 결정할 때 중요합니다.

## 4. 색상 단위 중, 색조(Hue), 채도(Saturation), 밝기(Lightness)를 기반으로 색상을 지정하는 방식은?

A) RGB

B) Hex 코드

C) HSL

D) CMYK

**정답: C) HSL**

**해설:** HSL 색상 모델은 색조(Hue), 채도(Saturation), 밝기(Lightness)를 기반으로 색상을 정의합니다. 색조는 0~360도의 각도로 표현되고, 채도와 밝기는 0~100%로 표현됩니다. 이 방식은 색상을 직관적으로 조절할 수 있어 디자이너가 색상을 쉽게 조정하는 데 유용합니다. 예시: `color: hsl(120, 100%, 50%);`는 순수한 녹색을 나타냅니다.

## 5. `box-sizing: border-box`의 효과로 올바른 것은?

A) 요소의 width/height에 content 영역만 포함된다

B) 요소의 width/height에 content, padding, border가 모두 포함된다

C) 요소의 width/height에 content와 padding만 포함된다

D) 요소의 width/height에 content와 border만 포함된다

**정답: B) 요소의 width/height에 content, padding, border가 모두 포함된다**

**해설:** `box-sizing: border-box`를 사용하면 지정한 width와 height 값에 padding과 border 크기가 포함됩니다. 이는 요소의 전체 크기가 지정한 width/height와 정확히 일치하도록 만들며, 내부 content 영역은 필요에 따라 조정됩니다. 이 방식은 레이아웃을 더 예측 가능하게 만들기 때문에 많은 개발자들이 모든 요소에 기본적으로 적용합니다. 반면 기본값인 `box-sizing: content-box`는 width/height에 content 영역만 포함하고 padding과 border는 추가로 계산됩니다.

## 6. 다음 CSS 코드의 결과로 올바른 것은?

```css
margin: 10px 20px 15px;

```

A) 상: 10px, 우: 20px, 하: 15px, 좌: 20px

B) 상: 10px, 우: 20px, 하: 15px, 좌: 10px

C) 상: 20px, 우: 15px, 하: 10px, 좌: 15px

D) 상: 10px, 우: 15px, 하: 20px, 좌: 15px

**정답: A) 상: 10px, 우: 20px, 하: 15px, 좌: 20px**

**해설:** CSS의 margin 축약형에서 값이 3개인 경우, 상-우-하 순서로 적용되며 좌측 값은 우측 값과 동일하게 적용됩니다(시계 방향). 따라서 `margin: 10px 20px 15px;`는 상단 여백 10px, 우측 여백 20px, 하단 여백 15px, 좌측 여백은 우측과 같은 20px로 적용됩니다.

## 7. 투명도가 0.5인 빨간색을 표현하는 올바른 CSS 코드는?

A) `color: rgb(255, 0, 0, 0.5);`

B) `color: rgba(255, 0, 0, 0.5);`

C) `color: #ff0000-50%;`

D) `color: red transparent;`

**정답: B) `color: rgba(255, 0, 0, 0.5);`**

**해설:** 투명도를 포함한 색상을 표현하려면 알파 채널을 지원하는 색상 표기법을 사용해야 합니다. RGBA는 빨강(R), 초록(G), 파랑(B) 값에 알파(A) 값을 추가한 형식입니다. 알파 값은 0(완전 투명)부터 1(완전 불투명)까지의 값을 가집니다. 따라서 `rgba(255, 0, 0, 0.5)`는 50% 투명도를 가진 빨간색을 의미합니다. 일반 RGB 형식은 알파 채널을 지원하지 않고, Hex 코드에 투명도를 직접 추가하는 `#ff0000-50%` 같은 표기법은 유효하지 않습니다.

## 8. 요소의 테두리를 둥글게 만들 때 사용하는 속성은?

A) `border-curve`

B) `border-round`

C) `border-radius`

D) `corner-radius`

**정답: C) `border-radius`**

**해설:** CSS에서 요소의 모서리를 둥글게 만들 때는 `border-radius` 속성을 사용합니다. 이 속성은 값으로 길이나 백분율을 받으며, 모서리의 곡률을 결정합니다. 예를 들어 `border-radius: 10px;`는 모든 모서리에 10픽셀의 둥근 효과를 적용합니다. 특히 `border-radius: 50%;`를 사용하면 요소가 원형이나 타원형이 됩니다. `border-curve`, `border-round`, `corner-radius`는 CSS에 존재하지 않는 속성입니다.

## 9. 다음 중 테두리 스타일(border-style)로 유효하지 않은 것은?

A) `solid`

B) `dashed`

C) `wavy`

D) `dotted`

**정답: C) `wavy`**

**해설:** CSS의 border-style 속성에서 `wavy`는 유효한 테두리 스타일이 아닙니다. 유효한 테두리 스타일로는 `solid`(실선), `dashed`(파선), `dotted`(점선), `double`(이중선), `groove`, `ridge`, `inset`, `outset`, `none`, `hidden` 등이 있습니다. `wavy` 스타일은 text-decoration 속성에서는 사용할 수 있지만 border-style에서는 사용할 수 없습니다.

## 10. `em` 단위가 기준으로 삼는 요소는?

A) 루트 요소(html)의 폰트 크기

B) 부모 요소의 폰트 크기

C) 해당 요소의 폰트 크기

D) 브라우저 기본 폰트 크기

**정답: C) 해당 요소의 폰트 크기**

**해설:** `em` 단위는 해당 요소의 현재 폰트 크기를 기준으로 합니다. 예를 들어, 해당 요소의 폰트 크기가 16px일 때 `margin: 2em`은 32px의 여백을 의미합니다. 이는 폰트 크기가 변경될 때 그에 비례하여 다른 속성값도 자동으로 조정되기 때문에 유용합니다. 참고로, 폰트 크기가 명시적으로 설정되지 않은 경우, 요소는 부모로부터 폰트 크기를 상속받습니다. `rem` 단위는 루트 요소(html)의 폰트 크기를 기준으로 합니다.

# CSS 기본 단위 및 속성 연습문제

## 연습문제 1: CSS 단위 활용하기

**문제**:
반응형 웹 디자인의 일부로 다양한 CSS 단위를 적용해야 합니다. 다음 요구사항에 맞게 CSS 코드를 작성하세요.

1. 컨테이너 박스는 화면 너비의 80%를 차지하되, 최대 너비는 1200px로 제한합니다.
2. 제목의 글자 크기는 HTML 기본 폰트 크기의 2배로 설정합니다.
3. 문단의 글자 크기는 제목 글자 크기의 0.5배로 설정합니다.
4. 버튼의 패딩은 상하 10px, 좌우 20px로 설정하고, 테두리 반경은 8px로 합니다.
5. 배경 이미지는 화면 높이의 50%로 설정합니다.

HTML 코드:

```html
<div class="container">
  <h1>반응형 제목</h1>
  <p>이것은 본문 텍스트입니다. CSS 단위에 대한 설명이 포함되어 있습니다.</p>
  <button>자세히 보기</button>
  <div class="background-image"></div>
</div>

```

**정답**:

```css
/* 컨테이너 스타일 */
.container {
  width: 80%;           /* 화면 너비의 80% */
  max-width: 1200px;    /* 최대 너비 제한 */
  margin: 0 auto;       /* 가운데 정렬 */
  padding: 20px;
}

/* 제목 스타일 */
h1 {
  font-size: 2rem;      /* HTML 기본 폰트 크기의 2배 */
  margin-bottom: 1rem;
}

/* 문단 스타일 */
p {
  font-size: 1em;       /* 현재 요소(상속된)의 기본 크기 */
}

/* 버튼 스타일 */
button {
  padding: 10px 20px;   /* 상하 10px, 좌우 20px */
  border-radius: 8px;   /* 모서리 둥글기 */
  border: none;
  background-color: #007bff;
  color: white;
  cursor: pointer;
}

/* 배경 이미지 스타일 */
.background-image {
  height: 50vh;         /* 뷰포트 높이의 50% */
  background-image: url('example.jpg');
  background-size: cover;
  background-position: center;
  margin-top: 20px;
}

```

**해설**:

- **컨테이너 너비**: `width: 80%`는 부모 요소(여기서는 body) 너비의 80%를 차지하게 합니다. `max-width: 1200px`으로 큰 화면에서도 너무 넓어지지 않도록 제한했습니다.
- **제목 글자 크기**: `font-size: 2rem`은 루트 요소(html)의 기본 글꼴 크기의 2배를 의미합니다. 일반적으로 브라우저의 기본 글꼴 크기는 16px이므로, 이 값은 32px에 해당합니다.
- **문단 글자 크기**:
    - `font-size: 1em`은 현재 요소의 기본 글꼴 크기를 의미합니다.
    - 원래 문제에서는 "제목 글자 크기의 0.5배"를 요구했지만, 여기서 `em`을 사용하면 부모 요소(container)의 폰트 크기를 기준으로 합니다. 문단이 제목의 직계 자식이 아니기 때문에, h1의 2rem을 참조하려면 `0.5em`이 아닌 다른 방식으로 계산해야 합니다.
    - 이상적으로는 제목에 대한 상대적 크기를 원한다면 CSS 변수를 사용하거나, 명시적인 계산을 해야 합니다.
- **버튼 패딩**: `padding: 10px 20px`는 상하 10px, 좌우 20px의 내부 여백을 설정합니다.
- **배경 이미지 높이**: `height: 50vh`는 뷰포트(보이는 화면) 높이의 50%를 차지하도록 설정합니다. 이는 화면 크기에 따라 동적으로 조정됩니다.

이 코드는 다양한 CSS 단위(%, rem, em, px, vh)를 적절히 활용하여 반응형 디자인을 구현하고 있습니다.

## 연습문제 2: 가시 속성 비교하기

**문제**:
세 개의 동일한 박스를 만들고, 각각 다른 방법으로 숨기는 버튼을 구현하세요. 다음 요구사항에 맞게 CSS 코드를 작성하세요.

1. 첫 번째 버튼은 `display: none`을 사용하여 박스를 완전히 숨깁니다.
2. 두 번째 버튼은 `visibility: hidden`을 사용하여 박스를 숨깁니다.
3. 세 번째 버튼은 `opacity: 0`을 사용하여 박스를 투명하게 만듭니다.
4. 각 버튼은 해당 속성을 토글할 수 있어야 합니다.
5. 각 박스는 서로 다른 색상을 가지며, 숨김 효과의 차이가 명확히 보여야 합니다.

HTML 코드:

```html
<div class="container">
  <div class="control-panel">
    <button id="toggle-display">display 토글</button>
    <button id="toggle-visibility">visibility 토글</button>
    <button id="toggle-opacity">opacity 토글</button>
  </div>

  <div class="box-container">
    <div id="box1" class="box">display 속성</div>
    <div id="box2" class="box">visibility 속성</div>
    <div id="box3" class="box">opacity 속성</div>
  </div>
</div>

```

**정답**:

```css
/* 기본 스타일 */
.container {
  max-width: 600px;
  margin: 0 auto;
  font-family: Arial, sans-serif;
}

/* 컨트롤 패널 스타일 */
.control-panel {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}

.control-panel button {
  padding: 8px 12px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.control-panel button:hover {
  background-color: #45a049;
}

/* 박스 컨테이너 스타일 */
.box-container {
  display: flex;
  justify-content: space-between;
}

/* 박스 기본 스타일 */
.box {
  width: 30%;
  height: 150px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-weight: bold;
  border-radius: 8px;
  transition: opacity 1s ease;
}

/* 각 박스 개별 스타일 */
#box1 {
  background-color: #3498db;
}

#box2 {
  background-color: #e74c3c;
}

#box3 {
  background-color: #f39c12;
}

/* 숨김 클래스 */
.display-none {
  display: none;
}

.visibility-hidden {
  visibility: hidden;
}

.opacity-zero {
  opacity: 0;
}

```

JavaScript 코드 (참고용):

```jsx
// 버튼 요소 가져오기
const displayBtn = document.getElementById('toggle-display');
const visibilityBtn = document.getElementById('toggle-visibility');
const opacityBtn = document.getElementById('toggle-opacity');

// 박스 요소 가져오기
const box1 = document.getElementById('box1');
const box2 = document.getElementById('box2');
const box3 = document.getElementById('box3');

// display 토글 기능
displayBtn.addEventListener('click', function() {
  box1.classList.toggle('display-none');
});

// visibility 토글 기능
visibilityBtn.addEventListener('click', function() {
  box2.classList.toggle('visibility-hidden');
});

// opacity 토글 기능
opacityBtn.addEventListener('click', function() {
  box3.classList.toggle('opacity-zero');
});

```

**해설**:

- **기본 레이아웃**:
    - `display: flex`와 `justify-content: space-between`을 사용하여 버튼과 박스를 가로로 균등하게 배치했습니다.
    - 각 박스는 너비의 30%를 차지하도록 설정했습니다.
- **가시성 클래스**:
    - `display-none` 클래스: `display: none`을 적용하면 요소가 DOM에서 완전히 제거된 것처럼 동작합니다. 공간도 차지하지 않고, 사용자 이벤트도 받지 않습니다.
    - `visibility-hidden` 클래스: `visibility: hidden`을 적용하면 요소가 보이지 않지만, 공간은 그대로 유지됩니다. 사용자 이벤트도 받지 않습니다.
    - `opacity-zero` 클래스: `opacity: 0`을 적용하면 요소가 완전히 투명해져 보이지 않지만, 공간은 유지되고 사용자 이벤트도 받을 수 있습니다.
- **전환 효과**:
    - `transition: opacity 1s ease`를 적용하여 opacity 변화에 애니메이션 효과를 주었습니다.
    - display와 visibility는 중간 상태가 없어 전환 효과가 적용되지 않습니다.
- **토글 동작**:
    - JavaScript를 사용하여 각 버튼 클릭 시 해당 박스에 적절한 클래스를 추가/제거하는 방식으로 토글 기능을 구현했습니다.

이 예제를 통해 세 가지 숨김 방식의 중요한 차이점을 확인할 수 있습니다:

1. `display: none` - 요소가 완전히 제거된 것처럼 동작하여 레이아웃에 공간을 차지하지 않습니다.
2. `visibility: hidden` - 요소는 보이지 않지만, 레이아웃에서 공간은 그대로 유지됩니다.
3. `opacity: 0` - 요소는 완전히 투명해지지만, 공간은 유지되고 사용자와 상호작용이 가능합니다.

## 연습문제 3: 박스 모델 및 box-sizing 활용하기

**문제**:
두 개의 동일한 카드를 만들되, 하나는 `content-box`, 다른 하나는 `border-box`로 설정하여 박스 모델의 차이점을 보여주세요. 다음 요구사항에 맞게 CSS 코드를 작성하세요.

1. 두 카드 모두 너비 300px, 높이는 내용에 맞게 자동 조정됩니다.
2. 두 카드 모두 패딩 20px, 테두리 5px, 마진 10px을 갖습니다.
3. 첫 번째 카드는 기본 `content-box`, 두 번째 카드는 `border-box`로 설정합니다.
4. 카드 내부에는 제목, 내용, 그리고 최종 너비를 표시하는 텍스트가 포함되어야 합니다.
5. 두 카드의 실제 차지하는 너비가 계산되어 표시되어야 합니다.

HTML 코드:

```html
<div class="container">
  <div class="card content-box">
    <h2>content-box 카드</h2>
    <p>이 카드는 content-box로 설정되어 있습니다.</p>
    <div class="width-display">실제 너비: <span>계산 중...</span></div>
  </div>

  <div class="card border-box">
    <h2>border-box 카드</h2>
    <p>이 카드는 border-box로 설정되어 있습니다.</p>
    <div class="width-display">실제 너비: <span>계산 중...</span></div>
  </div>

  <div class="explanation">
    <h3>박스 모델 차이점</h3>
    <p>content-box: width 속성은 내용 영역만을 의미합니다. 패딩과 테두리는 별도로 더해집니다.</p>
    <p>border-box: width 속성은 내용 + 패딩 + 테두리를 포함한 전체 너비를 의미합니다.</p>
  </div>
</div>

```

**정답**:

```css
/* 기본 스타일 */
body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  margin: 0;
  padding: 20px;
  background-color: #f5f5f5;
}

.container {
  max-width: 800px;
  margin: 0 auto;
}

/* 카드 공통 스타일 */
.card {
  width: 300px;
  margin: 10px;
  padding: 20px;
  border: 5px solid #333;
  background-color: white;
  border-radius: 5px;
  margin-bottom: 30px;
}

/* content-box 카드 */
.content-box {
  box-sizing: content-box; /* 기본값이지만 명시적으로 설정 */
  background-color: #e6f7ff;
  border-color: #1890ff;
}

/* border-box 카드 */
.border-box {
  box-sizing: border-box;
  background-color: #f6ffed;
  border-color: #52c41a;
}

/* 너비 표시 스타일 */
.width-display {
  margin-top: 15px;
  padding: 10px;
  background-color: #f0f0f0;
  border-radius: 4px;
  font-family: monospace;
  font-weight: bold;
}

/* 설명 스타일 */
.explanation {
  clear: both;
  margin-top: 20px;
  padding: 15px;
  background-color: #fffbe6;
  border: 1px solid #ffe58f;
  border-radius: 4px;
}

/* 계산된 너비 표시를 위한 스타일 */
.content-box .width-display span::after {
  content: "350px (300px + 40px 패딩 + 10px 테두리)";
}

.border-box .width-display span::after {
  content: "300px (내용 + 패딩 + 테두리 모두 포함)";
}

```

**해설**:

- **카드 기본 구성**:
    - 두 카드 모두 `width: 300px`로 설정했습니다.
    - 패딩은 모든 방향으로 20px(좌우 합 40px), 테두리는 5px(좌우 합 10px)으로 설정했습니다.
- **box-sizing 차이점**:
    - **content-box (첫 번째 카드)**:
        - `box-sizing: content-box`는 CSS의 기본값입니다.
        - 지정한 너비(300px)는 내용 영역만 의미합니다.
        - 실제 차지하는 전체 너비는 내용(300px) + 패딩(40px) + 테두리(10px) = 350px입니다.
    - **border-box (두 번째 카드)**:
        - `box-sizing: border-box`로 설정하면 지정한 너비(300px)가 내용 + 패딩 + 테두리를 모두 포함합니다.
        - 실제 내용 영역은 300px - 패딩(40px) - 테두리(10px) = 250px입니다.
        - 하지만 전체 차지하는 너비는 정확히 300px입니다.
- **시각적 구분**:
    - 각 카드에 다른 배경색과 테두리 색상을 적용하여 시각적으로 구분했습니다.
    - `.width-display span::after` 가상 요소를 사용하여 각 카드의 계산된 너비를 표시했습니다.
- **실제 응용**:
    - `border-box`는 레이아웃을 더 직관적으로 계획할 수 있게 해주므로 현대 웹 개발에서 널리 사용됩니다.
    - 많은 CSS 프레임워크와 리셋 스타일시트는 모든 요소에 `box-sizing: border-box`를 기본으로 설정합니다.

이 예제를 통해 동일한 CSS 너비 값을 적용하더라도 `box-sizing` 속성에 따라 실제 요소가 차지하는 공간이 달라질 수 있음을 확인할 수 있습니다.

## 연습문제 4: 테두리 속성을 활용한 버튼 디자인

**문제**:
다양한 테두리 속성을 활용하여 세 가지 다른 스타일의 버튼을 디자인하세요. 다음 요구사항에 맞게 CSS 코드를 작성하세요.

1. 첫 번째 버튼은 기본 직사각형 버튼으로, 실선 테두리와 hover 효과를 갖습니다.
2. 두 번째 버튼은 둥근 모서리(border-radius)를 활용한 캡슐형 버튼입니다.
3. 세 번째 버튼은 점선 테두리를 사용하고, 클릭한 것처럼 보이는 입체감을 갖습니다.
4. 모든 버튼은 패딩, 마진, 글꼴 크기 등 기본 스타일이 적용되어야 합니다.
5. hover 상태에서는 각각 다른 시각적 효과가 적용되어야 합니다.

HTML 코드:

```html
<div class="button-container">
  <button class="btn btn-basic">기본 버튼</button>
  <button class="btn btn-rounded">둥근 버튼</button>
  <button class="btn btn-dashed">점선 버튼</button>
</div>

```

**정답**:

```css
/* 기본 스타일 */
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-color: #f5f5f5;
}

.button-container {
  display: flex;
  flex-direction: column;
  gap: 20px;
  padding: 20px;
  background-color: white;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

/* 버튼 공통 스타일 */
.btn {
  padding: 12px 24px;
  font-size: 16px;
  cursor: pointer;
  background-color: white;
  transition: all 0.3s ease;
  outline: none;
}

/* 기본 직사각형 버튼 */
.btn-basic {
  border: 2px solid #3498db;
  color: #3498db;
}

.btn-basic:hover {
  background-color: #3498db;
  color: white;
}

/* 둥근 모서리 캡슐형 버튼 */
.btn-rounded {
  border: 2px solid #2ecc71;
  color: #2ecc71;
  border-radius: 30px; /* 크게 설정하여 캡슐 모양 생성 */
}

.btn-rounded:hover {
  background-color: #2ecc71;
  color: white;
  box-shadow: 0 4px 8px rgba(46, 204, 113, 0.3);
  transform: translateY(-2px);
}

/* 점선 테두리 버튼 */
.btn-dashed {
  border: 2px dashed #e74c3c;
  color: #e74c3c;
  border-radius: 4px;
  box-shadow: 0 2px 0 #c0392b;
}

.btn-dashed:hover {
  background-color: #f9e8e8;
}

.btn-dashed:active {
  transform: translateY(2px);
  box-shadow: 0 0 0 #c0392b;
}

```

**해설**:

- **버튼 공통 스타일**:
    - 모든 버튼에 패딩, 글꼴 크기, 커서 스타일 등의 기본 스타일을 적용했습니다.
    - `transition: all 0.3s ease`로 모든 속성 변화에 부드러운 전환 효과를 적용했습니다.
- **기본 직사각형 버튼**:
    - `border: 2px solid #3498db`로 파란색 실선 테두리를 적용했습니다.
    - 호버 시 배경색이 테두리 색상으로 변하고, 텍스트 색상이 흰색으로 변합니다.
- **둥근 모서리 캡슐형 버튼**:
    - `border-radius: 30px`로 매우 둥근 모서리를 적용하여 캡슐 모양을 만들었습니다.
    - 호버 시 배경색 변경뿐만 아니라 `box-shadow`로 그림자를 추가하고, `transform: translateY(-2px)`로 약간 위로 떠오르는 효과를 주었습니다.
- **점선 테두리 버튼**:
    - `border: 2px dashed #e74c3c`로 빨간색 점선 테두리를 적용했습니다.
    - `box-shadow: 0 2px 0 #c0392b`로 아래쪽에 그림자를 주어 입체감을 만들었습니다.
    - 활성화(`:active`) 상태일 때 `transform: translateY(2px)`와 그림자 제거로 버튼이 눌리는 듯한 효과를 구현했습니다.
- **레이아웃**:
    - 버튼 컨테이너에 `display: flex`와 `flex-direction: column`을 적용하여 버튼들을 세로로 배치했습니다.
    - `gap: 20px`으로 버튼 사이의 간격을 설정했습니다.

이 예제는 테두리 속성(`border`, `border-radius`)과 관련 속성(`box-shadow`, `transform`)을 조합하여 다양한 버튼 스타일을 만드는 방법을 보여줍니다. 또한 가상 클래스(`:hover`, `:active`)를 활용하여 사용자 상호작용에 따른 시각적 피드백을 제공합니다.
# CSS3 스타일 속성 기본 part2

Date: 2025년 3월 5일
페이지: p.185~p.218
완료: Yes
1일후 복습: Yes
7일후(주말) 복습: Yes
1달후 복습: No

# CSS 속성과 단위 종합 정리

## 1. 배경 속성 (Background Properties)

배경 속성은 HTML 요소의 배경을 꾸미는 데 사용되는 CSS 속성들의 모음입니다. 이미지, 색상, 위치 등을 지정하여 웹 페이지의 시각적 효과를 향상시킬 수 있습니다.

### 1.1 배경 이미지 관련 속성

| 속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `background-image` | 배경에 넣을 그림을 지정 | 요소에 배경 이미지를 적용할 때 사용 | `background-image: url('background.png');` |
| `background-size` | 배경 이미지의 크기를 지정 | 이미지를 요소에 맞게 조절할 때 사용 | `background-size: 100% 250px;`<br>`background-size: cover;` (비율 유지하며 전체 채움) |
| `background-repeat` | 배경 이미지 반복 여부 지정 | 이미지 타일링을 조절할 때 사용 | `background-repeat: no-repeat;`<br>`background-repeat: repeat-x;` (가로방향만 반복) |

### 1.2 배경 위치 및 효과 속성

| 속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `background-position` | 배경 이미지 위치 지정 | 이미지를 특정 위치에 배치할 때 사용 | `background-position: center top;`<br>`background-position: 50% 20%;` |
| `background-attachment` | 스크롤에 따른 이미지 이동 여부 지정 | 패럴랙스 효과나 고정 배경을 만들 때 사용 | `background-attachment: fixed;` (스크롤해도 고정)<br>`background-attachment: scroll;` (기본값, 함께 스크롤) |
| `background-color` | 배경색 설정 | 이미지 없을 때 기본 색상을 지정하거나 반투명 이미지 아래 색상 지정 | `background-color: #e7e7e8;`<br>`background-color: rgba(255, 0, 0, 0.5);` |

### 1.3 배경 속성 축약형

| 속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `background` | 모든 배경 속성을 한 번에 지정 | 여러 배경 속성을 간결하게 적용할 때 사용 | `background: url('bg.png') no-repeat center / cover #f5f5f5;` |

**배경 속성 종합 예제:**

```css
/* 개별 속성 사용 */
.detailed-background {
  background-image: url('background.png');
  background-position: bottom;
  background-size: 100%;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-color: #e7e7e8;
}

/* 축약형 사용 */
.shorthand-background {
  background: url('background.png') bottom/100% no-repeat fixed #e7e7e8;
}

```

## 2. 폰트 속성 (Font Properties)

폰트 속성은 텍스트의 시각적 표현을 제어하는 CSS 속성들로, 글꼴, 크기, 스타일, 간격 등을 지정합니다.

### 2.1 기본 폰트 속성

| 속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `font-family` | 사용할 폰트 지정 | 텍스트에 특정 서체 적용 시 사용 | `font-family: "Times New Roman", Arial, sans-serif;` |
| `font-size` | 글자 크기 지정 | 텍스트 크기 조절 시 사용 | `font-size: 32px;`<br>`font-size: 1.5em;` |
| `font-weight` | 글자 두께 지정 | 텍스트 강조나 굵기 조절 시 사용 | `font-weight: bold;`<br>`font-weight: 700;` (100~900) |
| `font-style` | 글자 스타일 지정 | 이탤릭체 등 적용 시 사용 | `font-style: italic;`<br>`font-style: normal;` |

### 2.2 텍스트 레이아웃 속성

| 속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `line-height` | 줄 간격 지정 | 가독성 향상이나 수직 중앙 정렬 시 사용 | `line-height: 1.5;`<br>`line-height: 70px;` |
| `text-align` | 텍스트 정렬 방향 지정 | 텍스트 좌우 정렬 시 사용 | `text-align: center;`<br>`text-align: justify;` |
| `text-decoration` | 텍스트 장식 지정 | 밑줄 제거나 추가 시 사용 | `text-decoration: none;`<br>`text-decoration: underline;` |

### 2.3 폰트 속성 축약형

| 속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `font` | 폰트 관련 속성을 한 번에 지정 | 여러 폰트 속성을 간결하게 적용할 때 | `font: italic bold 16px/1.5 Arial, sans-serif;` |

**폰트 속성 종합 예제:**

```css
/* 개별 속성 사용 */
.detailed-text {
  font-family: "Open Sans", Arial, sans-serif;
  font-size: 16px;
  font-weight: bold;
  font-style: italic;
  line-height: 1.5;
  text-align: center;
  text-decoration: none;
}

/* 축약형 사용 (font-style, font-weight, font-size/line-height, font-family 순서) */
.shorthand-text {
  font: italic bold 16px/1.5 "Open Sans", Arial, sans-serif;
  text-align: center;
  text-decoration: none;
}

```

## 3. 위치 속성 (Position Properties)

위치 속성은 HTML 요소의 배치 방법과 레이아웃을 제어하는 CSS 속성들입니다. 이를 통해 요소의 위치를 정밀하게 제어할 수 있습니다.

### 3.1 기본 위치 속성

| 속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `position` | 요소의 위치 설정 방식 지정 | 요소를 특정 방식으로 배치할 때 사용 | `position: relative;`<br>`position: absolute;` |
| `top`, `right`, `bottom`, `left` | 요소의 각 방향별 위치 지정 | position 속성과 함께 위치를 조절할 때 사용 | `top: 10px; left: 20px;` |
| `z-index` | 요소의 쌓임 순서 지정 | 요소 간 겹침이 발생할 때 앞뒤 순서 조절 | `z-index: 100;` (값이 클수록 앞에 표시) |

### 3.2 position 속성 값

| 값 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `static` | 기본값, 문서 흐름에 따라 배치 | 일반적인 요소 배치에 사용 | `position: static;` |
| `relative` | 기본 위치에서 상대적으로 이동 | 작은 위치 조정이나 absolute 요소의 기준점 설정에 사용 | `position: relative; top: 10px;` |
| `absolute` | 가장 가까운 positioned 부모 요소 기준으로 배치 | 부모 요소 내에서 자유롭게 위치 지정 시 사용 | `position: absolute; top: 30px; left: 20px;` |
| `fixed` | 뷰포트(화면)를 기준으로 고정 배치 | 스크롤해도 위치가 고정되어야 할 때 사용 | `position: fixed; bottom: 10px; right: 10px;` |
| `sticky` | 스크롤 위치에 따라 static과 fixed 사이 전환 | 스크롤 시 특정 위치에 고정되어야 할 때 사용 | `position: sticky; top: 0;` |

### 3.3 오버플로우 관련 속성

| 속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `overflow` | 내용이 요소 영역을 넘어갈 때 처리 방법 지정 | 영역 크기가 제한된 상황에서 콘텐츠 관리 시 사용 | `overflow: hidden;` (넘친 부분 숨김)<br>`overflow: scroll;` (스크롤 표시) |
| `overflow-x`, `overflow-y` | 가로/세로 방향의 오버플로우 처리 개별 지정 | 특정 방향만 스크롤 허용 시 사용 | `overflow-y: scroll; overflow-x: hidden;` |

**위치 속성 종합 예제:**

```css
.parent-container {
  position: relative;
  width: 400px;
  height: 300px;
  border: 1px solid #ddd;
  overflow: hidden;
}

.absolute-box {
  position: absolute;
  top: 50px;
  left: 100px;
  width: 200px;
  height: 150px;
  background-color: #f0f0f0;
  z-index: 10;
}

.fixed-button {
  position: fixed;
  bottom: 20px;
  right: 20px;
  padding: 10px;
  background-color: #007bff;
  color: white;
  z-index: 100;
}

.sticky-header {
  position: sticky;
  top: 0;
  background-color: white;
  padding: 10px;
  border-bottom: 1px solid #ddd;
}

```

## 최종 요약

### 1. 배경 속성 (Background Properties)

배경 속성은 웹 요소의 배경을 꾸미는 데 사용됩니다. `background-image`로 이미지를 설정하고, `background-size`로 크기를, `background-position`으로 위치를, `background-repeat`로 반복 여부를 조절합니다. `background-attachment`는 스크롤 시 배경 동작을 결정하며, `background-color`는 기본 배경색을 설정합니다. 이 모든 속성은 `background` 축약형으로 한 번에 설정할 수 있어 효율적입니다.

### 2. 폰트 속성 (Font Properties)

폰트 속성은 텍스트의 시각적 표현을 제어합니다. `font-family`로 글꼴을, `font-size`로 크기를, `font-weight`로 두께를, `font-style`로 스타일(이탤릭 등)을 지정합니다. `line-height`는 줄 간격을 조절하고, `text-align`은 정렬 방향을, `text-decoration`은 밑줄 등의 장식을 설정합니다. 대부분의 폰트 속성은 `font` 축약형으로 함께 사용할 수 있습니다.

### 3. 위치 속성 (Position Properties)

위치 속성은 요소의 배치 방법을 결정합니다. `position` 속성의 값(`static`, `relative`, `absolute`, `fixed`, `sticky`)에 따라 요소의 배치 기준이 달라집니다. `top`, `right`, `bottom`, `left`로 구체적인 위치를 지정하고, `z-index`로 겹치는 요소들의 앞뒤 순서를 결정합니다. `overflow` 속성은 내용이 요소 영역을 벗어날 때 처리 방법을 지정합니다. 이러한 위치 속성들을 조합하면 복잡한 레이아웃 구현이 가능합니다.

# CSS 속성과 단위 복습 퀴즈

## 1. 다음 중 배경 이미지를 화면 크기에 맞춰 전체를 채우면서 비율을 유지하도록 설정하는 속성은?

A) `background-size: 100%;`

B) `background-size: contain;`

C) `background-size: cover;`

D) `background-size: stretch;`

**정답: C) `background-size: cover;`**

**해설:** `background-size: cover;`는 배경 이미지의 비율을 유지하면서 요소 영역을 완전히 덮도록 크기를 조절합니다. 이미지의 일부가 잘릴 수 있지만, 빈 공간은 생기지 않습니다. `background-size: 100%;`는 너비만 100%로 설정하고 높이는 자동 비율로 조정됩니다. `contain`은 이미지 전체가 보이도록 조절하지만 요소에 빈 공간이 생길 수 있습니다. `stretch`는 CSS에 존재하지 않는 값입니다.

## 2. 스크롤해도 배경 이미지가 고정되어 움직이지 않게 하려면 어떤 속성을 사용해야 하나요?

A) `background-position: fixed;`

B) `background-scroll: none;`

C) `background-attachment: fixed;`

D) `background-movement: static;`

**정답: C) `background-attachment: fixed;`**

**해설:** `background-attachment: fixed;`는 배경 이미지가 뷰포트(viewport)에 고정되어 페이지 스크롤과 무관하게 제자리에 머무르게 합니다. 이 효과는 패럴랙스(parallax) 스크롤링 효과를 만들거나 고정된 배경을 원할 때 유용합니다. 다른 옵션들은 유효하지 않은 CSS 속성이거나 값입니다. 참고로 `background-attachment`의 기본값은 `scroll`로, 이 경우 배경 이미지가 요소와 함께 스크롤됩니다.

## 3. 폰트 사이즈를 부모 요소의 폰트 크기에 비례하여 설정할 때 사용하는 단위는?

A) `px`

B) `pt`

C) `em`

D) `vh`

**정답: C) `em`**

**해설:** `em` 단위는 현재 요소의 폰트 크기를 기준으로 합니다. 예를 들어, 부모 요소의 폰트 크기가 16px일 때 자식 요소에 `font-size: 1.5em;`을 적용하면 자식 요소의 폰트 크기는 24px(16px × 1.5)이 됩니다. 이는 상대적인 크기 조절이 필요할 때 유용합니다. `px`은 고정 단위이고, `pt`는 주로 인쇄 매체에서 사용되며, `vh`는 뷰포트 높이의 백분율 단위입니다.

## 4. 다음 CSS 축약형이 올바르게 해석된 것은?

```css
font: italic bold 16px/1.5 Arial, sans-serif;

```

A) 이탤릭체, 굵은 글씨, 16px 크기, 1.5em 줄 간격, Arial 우선 서체

B) 이탤릭체, 굵은 글씨, 16px 크기, 150% 줄 간격, Arial 우선 서체

C) 이탤릭체, 굵은 글씨, 16px 크기, 1.5px 줄 간격, Arial 우선 서체

D) 이탤릭체, 굵은 글씨, 16픽셀/1.5픽셀 크기, Arial 우선 서체

**정답: B) 이탤릭체, 굵은 글씨, 16px 크기, 150% 줄 간격, Arial 우선 서체**

**해설:** `font` 축약형의 구문은 `font-style`, `font-weight`, `font-size/line-height`, `font-family` 순서로 작성됩니다. 여기서 `16px/1.5`는 16px 폰트 크기와 1.5배(150%)의 줄 간격을 의미합니다. 이 줄 간격은 `em` 단위가 아니라 폰트 크기를 기준으로 한 배수(multiplier)입니다. 따라서 실제 줄 간격은 16px × 1.5 = 24px이 됩니다. `font-family`는 Arial을 우선 사용하고, 없으면 시스템의 sans-serif 폰트를 적용합니다.

## 5. `position: absolute;`를 사용할 때 요소의 위치 기준이 되는 것은?

A) 항상 브라우저 창(뷰포트)

B) 항상 문서의 body 요소

C) 가장 가까운 position이 static이 아닌 부모 요소

D) 요소의 원래 위치(static 위치)

**정답: C) 가장 가까운 position이 static이 아닌 부모 요소**

**해설:** `position: absolute;`를 적용한 요소는 가장 가까운 조상 요소 중 `position` 속성이 `static`이 아닌(즉, `relative`, `absolute`, `fixed`, `sticky` 중 하나인) 요소를 기준으로 배치됩니다. 이런 조상 요소가 없다면 최상위 요소(html)를 기준으로 합니다. 이것이 `absolute`와 `fixed`의 주요 차이점입니다. `fixed`는 항상 뷰포트(브라우저 창)를 기준으로 하지만, `absolute`는 조상 요소에 따라 기준점이 달라집니다.

## 6. 요소가 스크롤되다가 특정 위치에서 고정되도록 하는 position 값은?

A) `position: fixed;`

B) `position: absolute;`

C) `position: sticky;`

D) `position: relative;`

**정답: C) `position: sticky;`**

**해설:** `position: sticky;`는 요소가 스크롤 동작 중에 지정된 임계점(threshold)에 도달하면 `fixed` 상태로 전환되어 화면에 고정되는 특성을 가집니다. 예를 들어 `top: 0;`을 함께 지정하면, 스크롤하는 동안 요소가 뷰포트의 상단에 도달했을 때 거기에 "달라붙어" 고정됩니다. 이는 내비게이션 바, 섹션 헤더 등을 만들 때 유용합니다. `fixed`는 항상 뷰포트에 고정되고, `absolute`와 `relative`는 이런 스크롤 기반 동작을 제공하지 않습니다.

## 7. 다음 중 내용이 요소의 크기를 초과할 때 가로 방향으로만 스크롤바를 표시하는 CSS 코드는?

A) `overflow: scroll;`

B) `overflow-x: scroll; overflow-y: hidden;`

C) `overflow: horizontal-scroll;`

D) `scroll-direction: horizontal;`

**정답: B) `overflow-x: scroll; overflow-y: hidden;`**

**해설:** 지정된 코드는 가로(x축) 방향으로는 스크롤바를 표시하고(`overflow-x: scroll;`) 세로(y축) 방향으로는 넘치는 콘텐츠를 숨깁니다(`overflow-y: hidden;`). `overflow: scroll;`은 두 방향 모두 스크롤바를 표시하며, `overflow: horizontal-scroll;`과 `scroll-direction: horizontal;`은 유효한 CSS 속성이 아닙니다. `overflow-x`와 `overflow-y`는 각 방향의 오버플로우를 개별적으로 제어할 수 있게 해주는 유용한 속성입니다.

## 8. 요소의 앞뒤 순서를 결정하는 속성은?

A) `layer-order`

B) `z-index`

C) `stack-level`

D) `depth`

**정답: B) `z-index`**

**해설:** `z-index` 속성은 요소들이 겹칠 때 어떤 요소가 앞에 표시되고 어떤 요소가 뒤에 표시될지 결정합니다. 값이 클수록 앞쪽(사용자에게 더 가깝게)에 배치됩니다. 예를 들어, `z-index: 100;`인 요소는 `z-index: 10;`인 요소보다 앞에 표시됩니다. 단, `z-index`는 `position` 속성이 `static`이 아닌 요소에만 적용됩니다. 나머지 옵션들은 CSS에 존재하지 않는 속성입니다.

## 9. 다음 중 배경을 설정하는 올바른 축약형 문법은?

A) `background: #ff0000 url('bg.jpg') top center repeat-x;`

B) `background: top center repeat-x url('bg.jpg') #ff0000;`

C) `background: repeat-x #ff0000 url('bg.jpg') top center;`

D) `background: url('bg.jpg') repeat-x top center #ff0000;`

**정답: D) `background: url('bg.jpg') repeat-x top center #ff0000;`**

**해설:** `background` 축약 속성의 권장 순서는 일반적으로 `background: [image] [repeat] [position] [attachment] [color]`입니다. 따라서 이미지 → 반복 → 위치 → 고정 방식 → 색상 순으로 작성하는 것이 좋습니다. 위 예시에서 `url('bg.jpg')`는 이미지, `repeat-x`는 가로 반복, `top center`는 위치, `#ff0000`은 배경색을 의미합니다. 비록 다른 순서로 작성해도 대부분 브라우저에서 작동하지만, 일관된 순서를 유지하는 것이 가독성과 유지보수 측면에서 좋습니다.

## 10. 텍스트를 수직 가운데 정렬하는 일반적인 방법은?

A) `text-align: middle;`

B) `vertical-align: center;`

C) `line-height`를 요소 높이와 같게 설정

D) `text-position: center;`

**정답: C) `line-height`를 요소 높이와 같게 설정**

**해설:** 단일 줄 텍스트를 포함하는 요소에서 텍스트를 수직 가운데 정렬하는 가장 일반적인 방법은 `line-height` 값을 요소의 높이와 동일하게 설정하는 것입니다. 예를 들어 높이가 40px인 버튼이 있다면, `line-height: 40px;`을 적용하여 텍스트를 수직 중앙에 배치할 수 있습니다. `text-align: middle;`은 존재하지 않는 값이고(text-align은 left, right, center, justify 등을 사용), `vertical-align: center;`도 유효하지 않습니다(vertical-align은 middle을 사용). `text-position` 속성은 CSS에 존재하지 않습니다.

# CSS 속성과 단위 연습문제

## 연습문제 1: 다층 배경 이미지 구현하기

**문제**:
헤더 영역을 디자인하는데 다음과 같은 배경 요구사항이 있습니다. CSS 코드를 작성하세요.

- 메인 배경 이미지는 'header-bg.jpg'로, 화면 전체를 커버하면서 비율을 유지해야 합니다.
- 상단에 그라데이션 오버레이를 추가하여 텍스트 가독성을 높여야 합니다.
- 배경 이미지는 스크롤해도 고정되어 있어야 합니다.
- 이미지가 로드되지 않을 경우를 대비해 짙은 파란색 배경색을 설정하세요.
- 모든 배경 속성은 축약형으로도 작성하세요.

HTML 코드:

```html
<header class="hero-header">
  <h1>웹사이트 제목</h1>
  <p>웹사이트 설명 텍스트</p>
</header>

```

**정답**:

```css
/* 개별 속성 방식 */
.hero-header {
  background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.3)), url('header-bg.jpg');
  background-size: cover;
  background-position: center center;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-color: #003366;

  /* 헤더 크기 설정 (내용을 보기 위한 추가 스타일) */
  height: 500px;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

/* 축약형 방식 */
.hero-header {
  background: linear-gradient(to bottom, rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.3)), url('header-bg.jpg') center center / cover no-repeat fixed #003366;

  /* 헤더 크기 설정 (내용을 보기 위한 추가 스타일) */
  height: 500px;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

```

**해설**:

1. **다중 배경 구현**:
    - `linear-gradient`와 이미지 URL을 콤마로 구분하여 층층이 배치했습니다.
    - 먼저 나온 그라데이션이 이미지 위에 오버레이됩니다.
2. **배경 이미지 속성**:
    - `background-size: cover`: 이미지가 요소를 완전히 덮도록 하면서 비율을 유지합니다.
    - `background-position: center center`: 이미지를 중앙 배치합니다.
    - `background-repeat: no-repeat`: 이미지 반복을 방지합니다.
3. **고정 배경**:
    - `background-attachment: fixed`: 스크롤해도 배경이 화면에 고정됩니다.
4. **폴백 배경색**:
    - `background-color: #003366`: 이미지 로딩 실패 시 표시될 짙은 파란색입니다.
5. **축약형 문법**:
    - `background: [image] [position] / [size] [repeat] [attachment] [color]` 형태로 작성했습니다.
    - 축약형에서 `background-size`는 `background-position` 뒤에 `/`로 구분하여 표기합니다.

이 예제는 여러 배경 속성을 조합하여 시각적으로 매력적인 헤더를 만드는 방법을 보여줍니다. 그라데이션 오버레이는 배경 이미지 위에 반투명한 층을 추가하여 텍스트 가독성을 높이는 일반적인 디자인 패턴입니다.

## 연습문제 2: 다양한 텍스트 스타일링 구현하기

**문제**:
블로그의 다양한 텍스트 요소를 스타일링해야 합니다. 다음 요구사항에 맞게 CSS 코드를 작성하세요.

- 본문 텍스트는 가독성이 좋은 'Open Sans'를 기본 글꼴로 사용하고, 시스템 글꼴로 대체 가능하도록 설정하세요.
- 제목(h1-h3)은 'Montserrat' 글꼴로, 두껍게 표시되어야 합니다.
- 블록 인용문은 기울임꼴로, 좌측에 세로 선을 추가하세요.
- 중요한 텍스트는 강조되어야 하며 밑줄을 표시하세요.
- 모든 텍스트는 적절한 줄 간격을 가져야 합니다.
- 필요한 경우 축약형 문법을 사용하세요.

HTML 코드:

```html
<article class="blog-post">
  <h1>메인 제목</h1>
  <h2>부제목</h2>
  <p>일반 텍스트 단락입니다. 이 곳에 본문 내용이 들어갑니다.</p>
  <blockquote>이것은 인용문입니다. 중요한 내용을 인용할 때 사용합니다.</blockquote>
  <p>이 문장에는 <span class="highlight">매우 중요한 내용</span>이 포함되어 있습니다.</p>
  <h3>소제목</h3>
  <p>추가적인 설명 문단입니다.</p>
</article>

```

**정답**:

```css
/* 기본 본문 스타일 */
.blog-post {
  font-family: 'Open Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;
  font-size: 16px;
  line-height: 1.6;
  color: #333;
}

/* 제목 스타일 */
.blog-post h1, .blog-post h2, .blog-post h3 {
  font-family: 'Montserrat', Helvetica, Arial, sans-serif;
  font-weight: 700;
  line-height: 1.2;
  margin-bottom: 0.5em;
}

/* 개별 제목 크기 설정 */
.blog-post h1 {
  font-size: 2.5em;
  color: #222;
}

.blog-post h2 {
  font-size: 2em;
  color: #333;
}

.blog-post h3 {
  font-size: 1.5em;
  color: #444;
}

/* 단락 스타일 */
.blog-post p {
  margin-bottom: 1.5em;
}

/* 인용문 스타일 */
.blog-post blockquote {
  font-style: italic;
  border-left: 4px solid #ccc;
  margin-left: 0;
  padding-left: 1.5em;
  color: #666;
  line-height: 1.8;
}

/* 강조 텍스트 스타일 */
.blog-post .highlight {
  font-weight: bold;
  text-decoration: underline;
  color: #d32f2f;
}

/* 축약형 예시 (제목에 대한) */
.blog-post h1 {
  /* font: [font-style] [font-variant] [font-weight] [font-size/line-height] [font-family] */
  font: normal 700 2.5em/1.2 'Montserrat', Helvetica, Arial, sans-serif;
  color: #222;
  margin-bottom: 0.5em;
}

```

**해설**:

1. **기본 폰트 설정**:
    - 본문에는 'Open Sans'를 지정하고, 시스템 폰트를 대체 옵션으로 설정했습니다.
    - `line-height: 1.6`으로 가독성을 높였습니다.
2. **제목 스타일링**:
    - 모든 제목(h1, h2, h3)에 'Montserrat' 글꼴과 굵은 폰트 가중치(700)를 적용했습니다.
    - 제목별로 크기를 차별화하여 시각적 계층을 만들었습니다.
    - h1에는 축약형 속성(`font: [style] [weight] [size/line-height] [family]`)을 적용했습니다.
3. **인용문 스타일링**:
    - `font-style: italic`으로 기울임꼴을 적용했습니다.
    - `border-left`로 왼쪽에 세로 선을 추가했습니다.
    - 색상과 여백을 조정하여 다른 텍스트와 차별화했습니다.
4. **강조 텍스트**:
    - `font-weight: bold`로 텍스트를 두껍게 만들었습니다.
    - `text-decoration: underline`로 밑줄을 추가했습니다.
    - 강조 색상을 적용하여 시각적으로 눈에 띄게 했습니다.
5. **여백과 라인 하이트**:
    - 적절한 `margin-bottom`과 `line-height`를 설정하여 텍스트 가독성을 높였습니다.

이 예제는 다양한 폰트 속성을 사용하여 일관된 텍스트 계층구조와 스타일을 설정하는 방법을 보여줍니다. 웹 폰트를 사용하되 폴백 폰트를 지정하는 방법과 다양한 텍스트 요소에 적절한 스타일을 적용하는 방법을 포함합니다.

## 연습문제 3: 위치 속성을 활용한 모달 창 구현하기

**문제**:
웹사이트에 모달 창을 구현해야 합니다. 다음 요구사항에 맞게 CSS 코드를 작성하세요.

- 모달 배경은 화면 전체를 덮어야 하며, 반투명한 검은색으로 설정합니다.
- 모달 내용은 화면 중앙에 위치해야 하며, 흰색 배경과 그림자 효과를 가집니다.
- 닫기 버튼은 모달 창의 우상단에 위치해야 합니다.
- 모달이 표시되는 동안 페이지 스크롤은 불가능해야 합니다.
- position 속성을 적절히 활용하세요.

HTML 코드:

```html
<div class="modal-overlay">
  <div class="modal-container">
    <button class="close-btn">×</button>
    <h2>모달 제목</h2>
    <p>모달 내용이 여기에 들어갑니다. 사용자에게 표시할 중요한 정보나 입력 양식을 포함할 수 있습니다.</p>
    <button class="action-btn">확인</button>
  </div>
</div>

```

**정답**:

```css
/* 모달 배경 오버레이 */
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.6); /* 반투명 검정 배경 */
  z-index: 1000; /* 다른 요소보다 위에 표시 */
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden; /* 스크롤 방지 */
}

/* 모달 컨테이너 */
.modal-container {
  position: relative; /* 닫기 버튼의 기준점 */
  width: 90%;
  max-width: 500px;
  background-color: white;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  z-index: 1001; /* 오버레이보다 위에 표시 */
}

/* 닫기 버튼 */
.close-btn {
  position: absolute;
  top: 10px;
  right: 10px;
  width: 30px;
  height: 30px;
  border: none;
  background: transparent;
  font-size: 24px;
  cursor: pointer;
  color: #666;
  border-radius: 50%;
}

.close-btn:hover {
  background-color: #f0f0f0;
  color: #333;
}

/* 모달 제목 */
.modal-container h2 {
  margin-top: 10px;
  margin-bottom: 15px;
}

/* 확인 버튼 */
.action-btn {
  display: block;
  margin: 20px 0 10px auto; /* 우측 정렬 */
  padding: 8px 16px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

/* 모달 표시 시 body 스크롤 방지 */
body.modal-open {
  overflow: hidden;
}

```

**해설**:

1. **모달 오버레이 구현**:
    - `position: fixed`를 사용하여 뷰포트를 기준으로 위치를 고정했습니다.
    - `top: 0`, `left: 0`, `width: 100%`, `height: 100%`로 화면 전체를 커버합니다.
    - `background-color: rgba(0, 0, 0, 0.6)`로 반투명한 검은색 배경을 설정했습니다.
    - `z-index: 1000`으로 다른 페이지 요소들보다 위에 표시되도록 했습니다.
2. **모달 컨테이너 위치 설정**:
    - `position: relative`를 사용하여 내부 요소(닫기 버튼)의 기준점을 설정했습니다.
    - Flexbox(`display: flex`, `justify-content: center`, `align-items: center`)를 사용하여 모달을 화면 중앙에 배치했습니다.
    - `max-width`를 설정하여 큰 화면에서도 적절한 크기를 유지하도록 했습니다.
3. **닫기 버튼 위치**:
    - `position: absolute`와 `top`, `right` 속성을 사용하여 모달의 우상단에 배치했습니다.
    - 이 버튼의 기준점은 `position: relative`가 설정된 부모 요소(modal-container)입니다.
4. **스크롤 방지**:
    - 오버레이에 `overflow: hidden`을 적용하여 모달 내부 콘텐츠가 넘치더라도 스크롤이 생기지 않도록 했습니다.
    - `body.modal-open` 클래스는 모달이 표시될 때 body에 추가하여 페이지 전체 스크롤을 방지합니다.
5. **시각적 효과**:
    - `box-shadow`를 사용하여 모달에 그림자 효과를 주었습니다.
    - `border-radius`로 모서리를 둥글게 처리했습니다.
    - 닫기 버튼에 hover 효과를 추가하여 사용자 경험을 향상시켰습니다.

이 예제는 position 속성의 다양한 값(fixed, relative, absolute)을 활용하여 요소를 정확하게 배치하는 방법을 보여줍니다. z-index를 통해 요소 간의 쌓임 순서도 조절했습니다.

## 연습문제 4: 배경과 위치 속성을 활용한 헤더 메뉴 구현하기

**문제**:
웹사이트의 헤더와 내비게이션 메뉴를 구현하세요. 다음 요구사항에 맞게 CSS 코드를 작성하세요.

- 헤더는 상단에 고정되어 스크롤해도 항상 보여야 합니다.
- 로고는 헤더 좌측에 위치합니다.
- 메뉴는 헤더 우측에 가로로 배치합니다.
- 드롭다운 메뉴는 마우스 호버 시 부모 메뉴 아래에 표시되어야 합니다.
- 배경, 폰트, 위치 속성을 적절히 활용하세요.

HTML 코드:

```html
<header class="main-header">
  <div class="logo">
    <a href="#">LOGO</a>
  </div>
  <nav class="main-nav">
    <ul>
      <li><a href="#">홈</a></li>
      <li class="has-dropdown">
        <a href="#">서비스</a>
        <ul class="dropdown">
          <li><a href="#">웹 개발</a></li>
          <li><a href="#">앱 개발</a></li>
          <li><a href="#">디자인</a></li>
        </ul>
      </li>
      <li><a href="#">포트폴리오</a></li>
      <li><a href="#">문의하기</a></li>
    </ul>
  </nav>
</header>
<div class="content">
  <h1>메인 콘텐츠</h1>
  <p>스크롤해도 헤더는 상단에 고정됩니다.</p>
  <!-- 더미 콘텐츠 -->
  <div style="height: 1500px;"></div>
</div>

```

**정답**:

```css
/* 기본 스타일 리셋 */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
}

/* 헤더 스타일링 */
.main-header {
  position: fixed;  /* 상단에 고정 */
  top: 0;
  left: 0;
  width: 100%;
  height: 70px;
  background-color: #333;
  color: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  z-index: 1000; /* 다른 요소보다 위에 표시 */
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}

/* 로고 스타일링 */
.logo a {
  font-size: 24px;
  font-weight: bold;
  color: white;
  text-decoration: none;
}

/* 메인 내비게이션 스타일링 */
.main-nav ul {
  display: flex;
  list-style-type: none;
}

.main-nav li {
  position: relative;  /* 드롭다운 메뉴의 기준점 */
}

.main-nav a {
  display: block;
  padding: 10px 15px;
  color: white;
  text-decoration: none;
  font-size: 16px;
}

.main-nav a:hover {
  background-color: #555;
}

/* 드롭다운 메뉴 스타일링 */
.dropdown {
  position: absolute;  /* 부모 요소 기준으로 배치 */
  top: 100%;           /* 부모 메뉴 바로 아래에 배치 */
  left: 0;
  min-width: 150px;
  background-color: #444;
  display: none;       /* 기본적으로 숨김 */
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}

.has-dropdown:hover .dropdown {
  display: block;      /* 호버 시 표시 */
}

.dropdown li {
  width: 100%;
}

.dropdown a {
  padding: 10px 15px;
}

/* 메인 콘텐츠 스타일링 */
.content {
  margin-top: 70px;    /* 헤더 높이만큼 여백 추가 */
  padding: 20px;
}

```

**해설**:

1. **고정 헤더 구현**:
    - `position: fixed`와 `top: 0`, `left: 0`을 사용하여 헤더를 화면 상단에 고정했습니다.
    - `width: 100%`로 전체 너비를 차지하도록 했습니다.
    - `z-index: 1000`으로 다른 요소보다 위에 표시되도록 했습니다.
2. **로고와 내비게이션 배치**:
    - 헤더에 `display: flex`와 `justify-content: space-between`을 적용하여 로고와 메뉴를 각각 좌우에 배치했습니다.
    - `align-items: center`로 수직 중앙 정렬했습니다.
3. **메인 내비게이션 스타일링**:
    - 메뉴 항목들을 `display: flex`로 가로로 배치했습니다.
    - 메뉴 항목(`li`)에 `position: relative`를 설정하여 드롭다운 메뉴의 기준점을 만들었습니다.
4. **드롭다운 메뉴 구현**:
    - `position: absolute`와 `top: 100%`로 부모 메뉴 바로 아래에 위치하도록 했습니다.
    - 기본적으로는 `display: none`으로 숨기고, 부모 요소에 호버 시 `display: block`으로 표시합니다.
    - 드롭다운 메뉴에 `box-shadow`를 적용하여 시각적으로 구분했습니다.
5. **콘텐츠 영역 조정**:
    - 헤더가 fixed 위치로 설정되어 일반 흐름에서 벗어났기 때문에, 콘텐츠 영역에 상단 여백(`margin-top: 70px`)을 추가하여 헤더에 가려지지 않도록 했습니다.

이 예제는 position, display 속성을 함께 활용하여 현대적인 내비게이션 메뉴를 구현하는 방법을 보여줍니다. 특히 `position: relative`와 `position: absolute`의 관계를 이용한 드롭다운 메뉴 구현은 웹 개발에서 자주 사용되는 패턴입니다.
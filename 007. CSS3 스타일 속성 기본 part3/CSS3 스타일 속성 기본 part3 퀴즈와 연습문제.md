# CSS3 스타일 속성 기본 part3 퀴즈와 연습문제

---

## 퀴즈

## 문제 1: Float 속성 사용 목적

**질문:**

CSS에서 `float` 속성의 주 용도는 무엇인가요?

**옵션:**

A. 요소들을 수직으로 정렬하기 위해

B. 요소들을 수평으로 띄워 배치하기 위해

C. 요소의 배경색을 설정하기 위해

D. 요소에 애니메이션 효과를 주기 위해

**정답:** B

**해설:**

`float` 속성은 요소를 문서의 일반적인 흐름에서 띄워내어 왼쪽 또는 오른쪽으로 배치합니다. 이를 통해 텍스트나 다른 요소들이 float된 요소 주위로 감싸지도록 할 수 있으며, 주로 페이지 레이아웃에서 영역 구분이나 사이드바 배치 등에 활용됩니다.

---

## 문제 2: Float로 인한 부모 요소 높이 문제 해결

**질문:**

float가 적용된 자식 요소들 때문에 부모 요소가 그 높이를 인식하지 못하는 문제를 해결하려면 어떻게 해야 할까요?

**옵션:**

A. 부모 요소에 `overflow: hidden;` 설정

B. 부모 요소에 `display: inline-block;` 지정

C. 부모 요소에 추가로 `float: left;` 적용

D. 부모 요소의 `width` 값을 100%로 변경

**정답:** A

**해설:**

float된 요소들은 문서의 일반적인 흐름에서 제외되기 때문에, 부모 요소는 그 내부의 float 요소들이 차지하는 높이를 계산하지 않습니다. 이 문제를 해결하기 위해 부모 요소에 `overflow: hidden;`을 설정하면 float된 자식 요소들을 감싸면서 부모의 높이를 올바르게 확장할 수 있습니다.

---

## 문제 3: Clear 속성의 역할

**질문:**

`clear: both;` 속성은 CSS 레이아웃에서 어떤 역할을 하나요?

**옵션:**

A. float된 요소들의 영향을 제거하고, 요소를 새로운 줄에 시작하게 함

B. 부모 요소 내 모든 float된 요소를 숨김 처리함

C. 요소의 주변 여백을 자동으로 조절함

D. 텍스트 그림자 효과를 초기화함

**정답:** A

**해설:**

`clear: both;`를 설정하면, 앞에서 float가 적용된 요소들(left 또는 right)이 미치는 영향을 없애고 해당 요소를 강제로 새로운 줄에서 시작하게 만듭니다. 이는 float가 끝난 후 레이아웃을 정상적으로 이어가기 위한 중요한 속성입니다.

---

## 문제 4: Shadow 속성 값 순서

**질문:**

아래 코드 `box-shadow: 10px 10px 10px black;`에서 값들이 지정된 올바른 순서는 무엇인가요?

**옵션:**

A. x 오프셋, 색상, y 오프셋, 블러 정도

B. x 오프셋, y 오프셋, 블러 정도, 색상

C. 색상, x 오프셋, 블러 정도, y 오프셋

D. y 오프셋, x 오프셋, 블러 정도, 색상

**정답:** B

**해설:**

Shadow 관련 속성에서는 값이 순서대로 `x 오프셋`, `y 오프셋`, `블러 정도`, 그리고 `색상`으로 지정됩니다. 예제에서는 오른쪽 10px, 아래로 10px, 그리고 10px의 흐림 효과를 주어 그림자를 생성하며, 색상은 black입니다.

---

## 문제 5: Gradient 방향 지정

**질문:**

CSS의 `linear-gradient` 함수에서 `to bottom`을 지정하면 어떤 효과가 나타날까요?

**옵션:**

A. 그라디언트가 아래에서 위로 변화함

B. 그라디언트가 좌에서 우로 변화함

C. 그라디언트가 우에서 좌로 변화함

D. 그라디언트가 위에서 아래로 변화함

**정답:** D

**해설:**

`to bottom`은 그라디언트의 방향을 위에서 아래로 지정합니다. 즉, 첫 번째 색상에서 시작하여 점차 아래쪽으로 진행하면서 두 번째(또는 그 이후) 색상으로 부드럽게 전환됩니다.

---

## 문제 6: 벤더 프리픽스의 목적

**질문:**

CSS에서 `-webkit-`, `-moz-`와 같은 벤더 프리픽스는 주로 어떤 목적으로 사용되나요?

**옵션:**

A. 특정 브라우저에서 실험적 기능이나 새롭게 도입된 CSS 속성을 지원하기 위해

B. CSS 파일의 용량을 줄이기 위해

C. 모든 브라우저에서 동일한 레이아웃을 보장하기 위해

D. CSS 선택자의 우선순위를 조정하기 위해

**정답:** A

**해설:**

벤더 프리픽스는 각 브라우저 제조사가 최신 CSS 기능이나 실험적인 기능을 먼저 지원할 때 사용합니다. 시간이 지나면서 브라우저들이 해당 기능을 표준으로 채택하면, 프리픽스 없이도 사용할 수 있게 됩니다.

---

## 연습문제

## 연습문제 1: Float를 이용한 기본 2단 레이아웃 만들기

**요구사항:**

- 전체 레이아웃 너비: **960px**
- 왼쪽 영역(사이드바): **200px**, 오른쪽 영역(본문): **760px**
- 각각의 영역에는 간단한 제목과 본문 내용을 추가
- 부모 요소에서 float된 자식 요소의 높이 문제가 발생하지 않도록, `overflow: hidden;` 속성을 적용

**작성 힌트:**

1. HTML에서 부모 컨테이너(`div#wrap`) 내부에 두 개의 자식 요소(`div#aside`, `div#section`)를 생성합니다.
2. `div#aside`는 `float: left;`로 고정하고, `div#section` 역시 `float: left;` 또는 `float: right;`로 배치합니다.
3. 부모 요소(`div#wrap`)에 `overflow: hidden;`을 주어 내부 float 요소의 높이를 올바르게 반영하도록 합니다.

**예시 코드 스켈레톤:**

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>2단 레이아웃 연습</title>
  <style>
    body {
      width: 960px;
      margin: 0 auto;
      font-family: Arial, sans-serif;
    }
    #wrap {
      overflow: hidden; /* Float 문제 해결 */
      border: 1px solid #ccc;
      padding: 10px;
    }
    #aside {
      width: 200px;
      float: left;
      background-color: #f0f0f0;
      padding: 10px;
      box-sizing: border-box;
    }
    #section {
      width: 750px; /* 전체 너비(960) - aside 너비(200) - margin/padding 조정 */
      float: left;
      margin-left: 10px;
      background-color: #e0e0e0;
      padding: 10px;
      box-sizing: border-box;
    }
  </style>
</head>
<body>
  <h1>Float 레이아웃 연습</h1>
  <div id="wrap">
    <div id="aside">
      <h2>사이드바</h2>
      <p>여기에 사이드바 내용을 입력하세요.</p>
    </div>
    <div id="section">
      <h2>본문 영역</h2>
      <p>여기는 주 콘텐츠가 들어가는 영역입니다.</p>
    </div>
  </div>
</body>
</html>

```

**해설:**

이 문제는 `float` 속성으로 기본적인 2단 레이아웃을 구성하면서, float 요소로 인해 부모가 높이를 계산하지 않는 문제를 `overflow: hidden;`으로 해결하는 방법을 직접 체험할 수 있습니다.

---

## 연습문제 2: Float Clear 사용하기

**요구사항:**

- HTML에 여러 float 요소가 나열된 후, 다음 요소가 float의 영향을 받지 않도록 `clear: both;`를 적용하는 연습을 하세요.
- 예시로, 두 개의 float 영역 아래에 “푸터” 영역을 추가하고, 이 영역이 새로운 줄에서 시작하도록 작성합니다.

**작성 힌트:**

1. 두 개의 float 요소(예: 좌측에 배치되는 `#box1`과 우측에 배치되는 `#box2`)를 작성합니다.
2. float 요소들 뒤에 `<div class="clear"></div>` 요소를 추가하여 float 효과를 정리합니다.
3. CSS에서 `.clear { clear: both; }`를 지정합니다.

**예시 코드 스켈레톤:**

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Float Clear 연습</title>
  <style>
    body {
      width: 960px;
      margin: 0 auto;
      font-family: Arial, sans-serif;
    }
    #box1 {
      width: 45%;
      float: left;
      background-color: #d1e7dd;
      padding: 15px;
      box-sizing: border-box;
    }
    #box2 {
      width: 45%;
      float: right;
      background-color: #f8d7da;
      padding: 15px;
      box-sizing: border-box;
    }
    .clear {
      clear: both;
    }
    #footer {
      background-color: #fff3cd;
      padding: 10px;
      margin-top: 15px;
      text-align: center;
    }
  </style>
</head>
<body>
  <h1>Float Clear 연습</h1>
  <div id="box1">
    <h2>왼쪽 박스</h2>
    <p>이 박스는 왼쪽에 float 처리되었습니다.</p>
  </div>
  <div id="box2">
    <h2>오른쪽 박스</h2>
    <p>이 박스는 오른쪽에 float 처리되었습니다.</p>
  </div>
  <div class="clear"></div>
  <div id="footer">
    <h2>푸터 영역</h2>
    <p>clear로 인해 float와 관계없이 새로운 줄에 배치됩니다.</p>
  </div>
</body>
</html>

```

**해설:**

이 연습문제는 float 요소 뒤에서 `clear: both;`를 사용하여 float의 영향을 제거하는 방법을 보여줍니다. 푸터가 예상대로 새로운 줄에서 시작하는지 확인해 보세요.

---

## 연습문제 3: 그림자 효과 (Shadow Properties) 적용하기

**요구사항:**

- 하나의 `<div>` 요소에 `box-shadow`와 `text-shadow`를 동시에 적용하는 코드를 작성하세요.
- 사용 속성 값:
    - `x offset`: 5px
    - `y offset`: 5px
    - `blur`: 5px
    - `색상`: `rgba(0, 0, 0, 0.5)` (또는 `gray`)

**작성 힌트:**

1. `<div>` 내부에 제목 텍스트가 들어가도록 합니다.
2. CSS에서 `box-shadow`와 `text-shadow`를 모두 지정합니다.

**예시 코드 스켈레톤:**

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>그림자 효과 연습</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
    }
    .shadow-box {
      border: 2px solid #333;
      padding: 20px;
      margin-bottom: 20px;
      box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.5);
    }
    .shadow-box h1 {
      text-shadow: 5px 5px 5px rgba(0, 0, 0, 0.5);
    }
  </style>
</head>
<body>
  <div class="shadow-box">
    <h1>그림자 효과 테스트</h1>
    <p>이 DIV 요소에는 box-shadow와 text-shadow가 동시에 적용됩니다.</p>
  </div>
</body>
</html>

```

**해설:**

Shadow 속성은 UI에 깊이와 입체감을 더해줍니다. 값의 순서는 항상 `x offset`, `y offset`, `blur` 순이며, 마지막에 색상을 지정합니다. 연습문제를 통해 다양한 값으로 실험해 보며 원하는 효과를 찾아보세요.

---

## 연습문제 4: CSS Gradient 배경 만들기

**요구사항:**

- 하나의 큰 `<div>` 요소에 CSS의 `linear-gradient`를 이용해 배경 그라데이션을 적용합니다.
- 그라데이션 방향은 **위에서 아래(즉, `to bottom`)**로 지정
- 3가지 색상을 사용하여 자연스러운 변화 효과를 주세요 (예: 빨강, 노랑, 파랑)
- 각 색상이 시작되는 위치를 퍼센트로 명시합니다.

**작성 힌트:**

1. CSS의 `background` 속성에 `linear-gradient`를 작성합니다.
2. 색상과 위치를 조정하여 깔끔한 그라데이션 효과를 만듭니다.

**예시 코드 스켈레톤:**

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gradient 배경 연습</title>
  <style>
    .gradient-box {
      width: 100%;
      height: 300px;
      background: linear-gradient(to bottom, red 0%, yellow 50%, blue 100%);
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 1.5em;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="gradient-box">
    그라데이션 배경 예제
  </div>
</body>
</html>

```

**해설:**

이 문제를 통해 CSS의 `linear-gradient`를 활용하여 한 요소의 배경에 매끄러운 색상 전환 효과를 주는 방법을 연습할 수 있습니다. 색상과 비율을 조절하며 원하는 분위기를 만들어 보세요.

---

## 연습문제 5: 벤더 프리픽스(Vendor Prefixes)와 Border Radius 적용하기

**요구사항:**

- `<div>` 요소에 모서리 둥글기 효과를 주는 `border-radius`를 적용합니다.
- 동시에 웹킷(-webkit-) 및 모질라(-moz-) 프리픽스를 포함하는 코드를 작성하세요.
- 모던 브라우저와 구형 브라우저에서도 동일하게 렌더링 되는지 확인합니다.

**작성 힌트:**

1. CSS 작성 시, `webkit-border-radius`, `moz-border-radius` 후 표준 `border-radius` 순서로 정의합니다.
2. 요소에 배경색과 경계선을 추가해 둥근 모서리가 잘 보이도록 합니다.

**예시 코드 스켈레톤:**

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>벤더 프리픽스 & Border Radius 연습</title>
  <style>
    .rounded-box {
      width: 300px;
      height: 200px;
      background-color: #aed581;
      border: 2px solid #555;
      /* 벤더 프리픽스 적용 */
      -webkit-border-radius: 15px;
      -moz-border-radius: 15px;
      border-radius: 15px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.2em;
      color: #333;
    }
  </style>
</head>
<body>
  <div class="rounded-box">
    둥근 모서리 박스
  </div>
</body>
</html>

```

**해설:**

벤더 프리픽스는 일부 구버전 브라우저에서 최신 CSS 기능을 지원하기 위해 사용됩니다. 모던 브라우저에서는 표준 속성만으로 충분하지만, 여러 프리픽스를 포함하면 더욱 폭넓은 호환성을 보장할 수 있습니다.

---

## 추가 도전 과제

- 위의 연습문제들을 조합하여, 하나의 웹 페이지 내에 **Float 레이아웃**, **Clear 처리**, **Shadow 효과**, **그라데이션 배경**, **벤더 프리픽스 처리된 둥근 모서리** 등을 모두 포함한 복합 레이아웃을 구성해 보세요.
- 새로운 CSS 속성(예: Flexbox 또는 Grid)과 비교하면서 각 방법의 장단점을 토의해보는 것도 좋은 연습이 될 것입니다.

---
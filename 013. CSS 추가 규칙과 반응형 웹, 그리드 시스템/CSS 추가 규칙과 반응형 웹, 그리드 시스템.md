# CSS 추가 규칙과 반응형 웹, 그리드 시스템

Date: 2025년 3월 21일
페이지: p.453~p.503
완료: Yes
1일후 복습: No
7일후(주말) 복습: No
1달후 복습: No

# CSS 추가 규칙과 반응형 웹 요약본

## 1. CSS 규칙(@-rule) 개요

### 1.1 규칙의 정의

CSS에서 `@`가 붙은 단어는 규칙(rule)이라 부릅니다. 이 규칙들은 반응형 웹 구현을 위해 특히 중요한 역할을 합니다.

### 1.2 주요 규칙 종류

- `@import`: 외부 CSS 파일 가져오기
- `@font-face`: 웹 폰트 정의
- `@media`: 미디어 쿼리로 반응형 구현
- `@keyframes`: 애니메이션 정의

## 2. @import 규칙

### 2.1 개념과 용도

CSS 파일 내에서 다른 CSS 파일을 불러오는 방법입니다. 코드 유지보수성을 높이고 HTML에서 `<link>` 태그 수를 줄일 수 있습니다.

| 속성 | 설명 | 예시 |
| --- | --- | --- |
| `@import url()` | 외부 CSS 파일 경로 지정 | `@import url('typography.css');` |
| `@import url() screen` | 미디어 쿼리와 결합 | `@import url('mobile.css') screen and (max-width: 768px);` |

### 2.2 사용 예시

```css
/* 기본 CSS 파일 */
@import url('reset.css');
@import url('typography.css');
@import url('mobile.css') screen and (max-width: 768px);

```

## 3. @font-face 규칙

### 3.1 용도와 특징

웹에서 사용자 지정 폰트를 제공하기 위한 규칙입니다. 웹 폰트 서비스가 지원하지 않는 폰트를 직접 제공할 때 사용합니다.

### 3.2 필수 속성

| 속성 | 설명 | 예시 |
| --- | --- | --- |
| `font-family` | 폰트 이름 지정 (필수) | `font-family: 'MyCustomFont';` |
| `src` | 폰트 파일 지정 (필수) | `src: url('fonts/custom.woff2');` |
| `font-weight` | 폰트 두께 지정 (선택) | `font-weight: 700;` |
| `font-style` | 폰트 스타일 지정 (선택) | `font-style: italic;` |

### 3.3 폰트 소스 지정 방식

- `local()`: 사용자 컴퓨터 내부 폰트 선택
- `url()`: 외부에서 폰트 파일 불러오기

### 3.4 사용 예시

```css
@font-face {
  font-family: 'OpenSansKorean';
  src: local('Open Sans'),
       url('fonts/OpenSansKorean.woff2') format('woff2'),
       url('fonts/OpenSansKorean.woff') format('woff');
  font-weight: normal;
  font-style: normal;
}

body {
  font-family: 'OpenSansKorean', sans-serif;
}

```

## 4. @media 규칙과 반응형 웹

### 4.1 @media 규칙 개념

다양한 장치와 화면 크기에 따라 스타일을 다르게 적용할 수 있게 해주는 규칙입니다.

### 4.2 반응형 웹 구현 방식

| 구현 방식 | 문법 | 예시 |
| --- | --- | --- |
| `<link>` 태그의 media 속성 | HTML에서 지정 | `<link rel="stylesheet" href="mobile.css" media="screen and (max-width: 768px)">` |
| `@media` 규칙 | CSS 내부에서 지정 | `@media screen and (max-width: 768px) { ... }` |
| `@import` 규칙 | CSS 파일 가져오기와 결합 | `@import url('mobile.css') screen and (max-width: 768px);` |

### 4.3 미디어 쿼리 속성

| 속성 | 설명 | 예시 |
| --- | --- | --- |
| `width` | 화면(뷰포트) 너비 | `@media (width: 768px) { ... }` |
| `height` | 화면(뷰포트) 높이 | `@media (height: 1024px) { ... }` |
| `device-width` | 장치 너비 | `@media (device-width: 390px) { ... }` |
| `device-height` | 장치 높이 | `@media (device-height: 844px) { ... }` |
| `orientation` | 장치 방향 | `@media (orientation: portrait) { ... }` |
| `device-aspect-ratio` | 화면 비율 | `@media (device-aspect-ratio: 16/9) { ... }` |
| `color` | 색상 비트 수 | `@media (color: 8) { ... }` |
| `resolution` | 장치 해상도 | `@media (resolution: 300dpi) { ... }` |

### 4.4 범위 지정

`min-`과 `max-` 접두사를 사용하여 범위를 지정할 수 있습니다.

```css
/* 최소 너비가 768px인 경우 */
@media (min-width: 768px) { ... }

/* 최대 너비가 480px인 경우 */
@media (max-width: 480px) { ... }

/* 너비가 480px에서 768px 사이인 경우 */
@media (min-width: 480px) and (max-width: 768px) { ... }

```

### 4.5 화면 방향 전환

`orientation` 속성으로 디바이스의 방향을 감지할 수 있습니다.

| 값 | 설명 | 예시 |
| --- | --- | --- |
| `portrait` | 세로 방향(높이>너비) | `@media (orientation: portrait) { ... }` |
| `landscape` | 가로 방향(너비>높이) | `@media (orientation: landscape) { ... }` |

## 5. 그리드 시스템

### 5.1 그리드 시스템 개념

미리 정의된 스타일시트로 격자 위에 요소를 배치할 수 있게 하는 시스템입니다. 일반적으로 12개의 열을 기준으로 합니다.

### 5.2 그리드 구성 요소

- **Column**: 내용이 위치하는 공간
- **Gutter(Gap)**: 열 사이의 여백

### 5.3 그리드 시스템 유형

| 유형 | 설명 |
| --- | --- |
| 정적 그리드 | 고정된 픽셀 단위로 너비 지정 |
| 동적 그리드 | 상대적 단위(%, em)로 너비 지정 |
| 반응형 그리드 | 미디어 쿼리와 결합하여 화면 크기에 따라 변화 |

## 6. CSS 그리드 레이아웃

### 6.1 CSS 그리드 개념

기존의 `float` 속성이나 `flexbox`보다 더 복잡한 2차원 레이아웃을 쉽게 만들 수 있는 CSS 레이아웃 시스템입니다.

### 6.2 그리드 컨테이너 설정

| 속성 | 설명 | 예시 |
| --- | --- | --- |
| `display: grid` | 그리드 컨테이너 지정 | `display: grid;` |
| `grid-template-columns` | 열(수직선) 크기 지정 | `grid-template-columns: 1fr 2fr;` |
| `grid-template-rows` | 행(수평선) 크기 지정 | `grid-template-rows: 100px auto;` |
| `grid-template` | 행과 열을 함께 지정 | `grid-template: 300px 300px / 1fr 2fr;` |
| `grid-gap` | 그리드 간격 지정 | `grid-gap: 10px;` |

### 6.3 그리드 유닛(fr)

비율을 나타내는 특별한 단위로, 가용 공간에 대한 비율을 지정합니다.

```css
.container {
  display: grid;
  /* 1:2:1 비율로 3개의 열 생성 */
  grid-template-columns: 1fr 2fr 1fr;
}

```

### 6.4 그리드 아이템 배치

| 속성 | 설명 | 예시 |
| --- | --- | --- |
| `grid-column-start` | 열 시작 위치 | `grid-column-start: 1;` |
| `grid-column-end` | 열 끝 위치 | `grid-column-end: 3;` |
| `grid-row-start` | 행 시작 위치 | `grid-row-start: 1;` |
| `grid-row-end` | 행 끝 위치 | `grid-row-end: 3;` |
| `grid-column` | 열 시작/끝 위치 단축 | `grid-column: 1 / 3;` |
| `grid-row` | 행 시작/끝 위치 단축 | `grid-row: 1 / 3;` |

### 6.5 문자열로 그리드 영역 지정

| 속성 | 설명 | 예시 |
| --- | --- | --- |
| `grid-template-areas` | 문자열로 레이아웃 정의 | `grid-template-areas: "header header" "sidebar content" "footer footer";` |
| `grid-area` | 요소가 차지할 영역 지정 | `grid-area: header;` |

### 6.6 그리드 레이아웃 예시

```css
.container {
  display: grid;
  grid-template-columns: 1fr 3fr;
  grid-template-rows: auto 1fr auto;
  grid-gap: 20px;
  grid-template-areas:
    "header header"
    "sidebar content"
    "footer footer";
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.content { grid-area: content; }
.footer { grid-area: footer; }

```

---

# 최종 요약

## CSS 규칙(@-rule)

- `@` 기호로 시작하는 CSS 규칙은 반응형 웹 구현에 중요
- 주요 규칙: `@import`, `@font-face`, `@media`

## @import 규칙

- CSS 파일 내에서 다른 CSS 파일 불러오기
- 문법: `@import url('파일경로.css');`
- 미디어 쿼리와 결합 가능: `@import url('mobile.css') screen and (max-width: 768px);`

## @font-face 규칙

- 웹 폰트 정의에 사용
- 필수 속성: `font-family`, `src`
- 선택 속성: `font-weight`, `font-style`
- `local()`과 `url()` 함수로 폰트 소스 지정

## @media 규칙과 반응형 웹

- 다양한 장치와 화면 크기에 맞게 스타일 적용
- 구현 방식: `<link>` 태그, `@media` 규칙, `@import` 규칙
- 주요 쿼리 속성: `width`, `height`, `orientation`, `device-width`
- `min-`/`max-` 접두사로 범위 지정

## 그리드 시스템

- 격자 기반 레이아웃 시스템, 보통 12열 기준
- 구성: Column(내용 공간), Gutter(여백)
- 유형: 정적, 동적, 반응형 그리드

## CSS 그리드 레이아웃

- 2차원 레이아웃 시스템, `display: grid`로 활성화
- 주요 속성: `grid-template-columns`, `grid-template-rows`, `grid-gap`
- `fr` 단위로 비율 지정
- 아이템 배치: `grid-column`, `grid-row`, `grid-area`
- 문자열 레이아웃: `grid-template-areas`로 시각적 구조 정의

# CSS 추가 규칙과 반응형 웹 - 복습 퀴즈

## 문제 1

CSS에서 `@import` 규칙의 주요 목적은 무엇인가요?

1. CSS 파일 내에서 자바스크립트를 실행하기 위함
2. 외부 CSS 파일을 현재 스타일시트로 가져오기 위함
3. 웹 폰트를 정의하기 위함
4. 미디어 쿼리를 선언하기 위함

**정답: 2**

**해설:** `@import` 규칙은 CSS 파일 내에서 다른 CSS 파일을 불러오는 방법입니다. 이를 통해 코드 유지보수성을 높이고 HTML에서 `<link>` 태그 수를 줄일 수 있습니다. 문법은 `@import url('파일경로.css');` 형태로 사용합니다.

## 문제 2

다음 중 `@font-face` 규칙에서 반드시 포함해야 하는 속성은 무엇인가요?

1. font-weight와 font-style
2. src와 unicode-range
3. font-family와 src
4. font-display와 font-stretch

**정답: 3**

**해설:** `@font-face` 규칙에서는 반드시 `font-family`(폰트 이름 지정)와 `src`(폰트 파일 위치 지정) 속성을 포함해야 합니다. `font-weight`나 `font-style` 같은 다른 속성들은 선택적으로 사용할 수 있습니다.

## 문제 3

반응형 웹을 구현하기 위한 방법으로 올바르지 않은 것은 무엇인가요?

1. `<link>` 태그에 media 속성 사용하기
2. CSS 파일 내 `@media` 규칙 사용하기
3. `@import` 규칙에 미디어 쿼리 추가하기
4. `@responsive` 규칙 사용하기

**정답: 4**

**해설:** CSS에는 `@responsive`라는 규칙이 존재하지 않습니다. 반응형 웹 구현을 위한 올바른 방법은 1) `<link>` 태그의 media 속성 사용, 2) CSS 내 `@media` 규칙 사용, 3) `@import` 규칙에 미디어 쿼리 추가하는 방법입니다.

## 문제 4

다음 중 미디어 쿼리에서 디바이스 방향을 감지하는 속성은 무엇인가요?

1. direction
2. rotation
3. position
4. orientation

**정답: 4**

**해설:** 미디어 쿼리에서 `orientation` 속성을 사용하여 디바이스의 방향을 감지할 수 있습니다. `orientation: portrait`은 세로 방향(높이>너비), `orientation: landscape`는 가로 방향(너비>높이)을 나타냅니다.

## 문제 5

CSS Grid 레이아웃에서 비율을 나타내는 특별한 단위는 무엇인가요?

1. %
2. fr
3. vw
4. em

**정답: 2**

**해설:** CSS Grid 레이아웃에서는 `fr`(fraction) 단위를 사용하여 가용 공간에 대한 비율을 지정합니다. 예를 들어 `grid-template-columns: 1fr 2fr 1fr`은 1:2:1 비율로 3개의 열을 생성합니다.

## 문제 6

CSS Grid 레이아웃에서 행과 열을 함께 지정하는 단축 속성은 무엇인가요?

1. grid-layout
2. grid-area
3. grid-template
4. grid-structure

**정답: 3**

**해설:** CSS Grid 레이아웃에서 `grid-template` 속성은 행(rows)과 열(columns)을 함께 지정하는 단축 속성입니다. 예: `grid-template: 300px 300px / 1fr 2fr;`는 높이가 300px인 두 개의 행과 1:2 비율의 두 개의 열을 생성합니다. 순서는 rows, columns 순입니다.

## 문제 7

다음 중 CSS Grid 컨테이너를 생성하는 올바른 속성은 무엇인가요?

1. display: grid-layout;
2. display: grid;
3. position: grid;
4. layout: grid;

**정답: 2**

**해설:** CSS Grid 레이아웃을 사용하려면 컨테이너 요소에 `display: grid;` 속성을 적용해야 합니다. 이것은 해당 요소의 직계 자식 요소들이 그리드 아이템으로 동작하도록 합니다.

## 문제 8

아래 코드에서 `.item1`은 그리드에서 몇 개의 열을 차지하나요?

```css
.grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
}
.item1 {
  grid-column: 1 / 3;
}

```

1. 1개
2. 2개
3. 3개
4. 4개

**정답: 2**

**해설:** `grid-column: 1 / 3;`은 첫 번째 그리드 라인에서 시작해 세 번째 그리드 라인에서 끝나는 것을 의미합니다. 그리드 라인은 0부터 시작하는 것이 아니라 1부터 시작하므로, 이 설정은 첫 번째와 두 번째 열을 차지하게 됩니다. 따라서 총 2개의 열을 차지합니다.

# CSS 추가 규칙과 반응형 웹 - 코딩 연습문제

## 연습문제 1: 웹 폰트 구현하기

### 문제

로컬에서 'Roboto' 폰트를 사용할 수 있지만, 사용자 컴퓨터에 없을 경우 웹 폰트로 제공하려고 합니다. 'Roboto' 폰트의 regular, bold 스타일을 모두 지원하는 @font-face 규칙을 작성하세요.

- 폰트 파일은 '/fonts' 폴더에 'roboto-regular.woff2', 'roboto-regular.woff', 'roboto-bold.woff2', 'roboto-bold.woff'로 있다고 가정합니다.
- 폰트를 body 요소에 적용하는 코드도 작성하세요.

### 정답

```css
/* 일반(regular) 폰트 스타일 정의 */
@font-face {
  font-family: 'Roboto';
  src: local('Roboto'),
       url('/fonts/roboto-regular.woff2') format('woff2'),
       url('/fonts/roboto-regular.woff') format('woff');
  font-weight: normal;
  font-style: normal;
}

/* 볼드(bold) 폰트 스타일 정의 */
@font-face {
  font-family: 'Roboto';
  src: local('Roboto Bold'),
       url('/fonts/roboto-bold.woff2') format('woff2'),
       url('/fonts/roboto-bold.woff') format('woff');
  font-weight: bold;
  font-style: normal;
}

/* body에 폰트 적용 */
body {
  font-family: 'Roboto', sans-serif;
}

```

### 해설

1. `@font-face` 규칙으로 두 가지 폰트 스타일을 정의했습니다:
    - 같은 'Roboto' 폰트 패밀리에 다른 `font-weight` 값을 지정해 브라우저가 적절한 스타일을 선택할 수 있게 합니다.
    - `font-family`로 폰트 이름을 지정합니다(필수 속성).
2. `src` 속성(필수)에서:
    - `local()` 함수로 사용자의 컴퓨터에 이미 설치된 폰트를 먼저 확인합니다.
    - `url()` 함수로 웹 폰트 파일 경로를 지정합니다.
    - `format()` 함수로 웹 폰트 형식을 지정해 브라우저 호환성을 높입니다.
    - WOFF2가 더 압축률이 높아 먼저 제공하고, 호환성을 위해 WOFF도 제공합니다.
3. `body`에 폰트를 적용하고, 폴백(fallback) 폰트로 sans-serif를 지정했습니다.

## 연습문제 2: 반응형 웹 헤더 구현하기

### 문제

다음 조건에 맞는 반응형 웹 헤더를 구현하세요:

- 화면 너비가 768px 이상일 때: 로고는 왼쪽, 메뉴는 오른쪽에 가로로 배열
- 화면 너비가 768px 미만일 때: 로고는 위쪽 중앙, 메뉴는 아래쪽에 세로로 배열
- 모바일 화면(480px 미만)에서는 메뉴 텍스트 크기를 14px로 줄임

HTML 구조는 다음과 같습니다:

```html
<header class="site-header">
  <div class="logo">Site Logo</div>
  <nav class="main-menu">
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>
</header>

```

### 정답

```css
/* 기본 스타일 */
.site-header {
  padding: 20px;
  background-color: #f5f5f5;
}

.logo {
  font-weight: bold;
  font-size: 24px;
}

.main-menu ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.main-menu li {
  margin: 10px 0;
}

.main-menu a {
  text-decoration: none;
  color: #333;
}

/* 모바일 스타일 (기본) */
.site-header {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.logo {
  margin-bottom: 20px;
  text-align: center;
}

/* 태블릿 & 모바일 (768px 미만) */
@media (max-width: 767px) {
  .main-menu ul {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

/* 작은 모바일 화면 (480px 미만) */
@media (max-width: 479px) {
  .main-menu a {
    font-size: 14px;
  }
}

/* 데스크톱 (768px 이상) */
@media (min-width: 768px) {
  .site-header {
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    margin-bottom: 0;
  }

  .main-menu ul {
    display: flex;
    flex-direction: row;
  }

  .main-menu li {
    margin: 0 0 0 20px;
  }
}

```

### 해설

1. **기본 스타일**: 모든 화면 크기에 적용되는 공통 스타일을 먼저 정의했습니다.
2. **모바일 우선 접근법**: 기본 스타일은 모바일용으로 설정하고, 미디어 쿼리를 통해 화면이 커질 때 변경사항을 적용했습니다.
    - 로고와 메뉴가 세로로 배치되도록 `flex-direction: column` 사용
    - 중앙 정렬을 위해 `align-items: center` 적용
3. **미디어 쿼리 사용**: 화면 크기별로 다른 스타일을 적용했습니다.
    - `@media (min-width: 768px)`: 768px 이상일 때 적용
    - `@media (max-width: 767px)`: 768px 미만일 때 적용
    - `@media (max-width: 479px)`: 480px 미만일 때 적용
4. **데스크톱 레이아웃**:
    - 로고와 메뉴를 가로 배치: `flex-direction: row`
    - 양쪽 정렬: `justify-content: space-between`
    - 메뉴 항목들을 가로 배치: `.main-menu ul`에 `flex-direction: row` 설정
5. **모바일 레이아웃**:
    - 480px 미만에서는 메뉴 폰트 크기를 14px로 줄임

## 연습문제 3: CSS Grid로 레이아웃 구성하기

### 문제

CSS Grid를 사용하여 다음 조건을 만족하는 레이아웃을 구현하세요:

- 헤더(header): 페이지 상단 전체 너비
- 사이드바(sidebar): 왼쪽에 배치, 너비는 가용 공간의 1/4
- 컨텐츠(content): 오른쪽에 배치, 너비는 가용 공간의 3/4
- 푸터(footer): 페이지 하단 전체 너비
- grid-template-areas를 사용하여 정의하세요

HTML 구조는 다음과 같습니다:

```html
<div class="container">
  <header class="header">Header</header>
  <aside class="sidebar">Sidebar</aside>
  <main class="content">Content</main>
  <footer class="footer">Footer</footer>
</div>

```

### 정답

```css
.container {
  display: grid;
  grid-template-columns: 1fr 3fr;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    "header header"
    "sidebar content"
    "footer footer";
  min-height: 100vh;
  gap: 20px;
}

.header {
  grid-area: header;
  background-color: #f0f0f0;
  padding: 20px;
}

.sidebar {
  grid-area: sidebar;
  background-color: #e0e0e0;
  padding: 20px;
}

.content {
  grid-area: content;
  background-color: #d0d0d0;
  padding: 20px;
}

.footer {
  grid-area: footer;
  background-color: #c0c0c0;
  padding: 20px;
}

/* 모바일 레이아웃 - 화면 너비 768px 미만 */
@media (max-width: 767px) {
  .container {
    grid-template-columns: 1fr;
    grid-template-areas:
      "header"
      "sidebar"
      "content"
      "footer";
  }
}

```

### 해설

1. **그리드 컨테이너 설정**:
    - `display: grid`로 그리드 레이아웃 활성화
    - `grid-template-columns: 1fr 3fr`로 1:3 비율의 두 열 생성
    - `grid-template-rows: auto 1fr auto`로 헤더와 푸터는 내용에 맞게, 컨텐츠 영역은 남은 공간 모두 차지
    - `min-height: 100vh`로 최소 화면 높이 설정
    - `gap: 20px`로 그리드 아이템 간 간격 설정
2. **그리드 영역 정의**:
    - `grid-template-areas`로 직관적인 2차원 레이아웃 정의
    - 각 줄은 하나의 행을 나타내고, 공백으로 구분된 영역 이름이 각 열을 나타냄
    - `"header header"`는 헤더가 첫 행의 두 열을 차지
    - `"sidebar content"`는 두 번째 행에서 사이드바와 콘텐츠 배치
    - `"footer footer"`는 푸터가 마지막 행의 두 열을 차지
3. **그리드 아이템 배치**:
    - 각 요소에 `grid-area` 속성으로 해당 영역 이름 지정
    - 이렇게 하면 HTML 순서와 무관하게 원하는 위치에 배치 가능
4. **반응형 레이아웃**:
    - 768px 미만 화면에서는 단일 열 레이아웃으로 변경
    - `grid-template-areas`를 재정의하여 모든 요소가 세로로 쌓이도록 함

이 구현은 미디어 쿼리와 그리드 레이아웃을 결합하여 반응형 웹 디자인을 효과적으로 보여줍니다.
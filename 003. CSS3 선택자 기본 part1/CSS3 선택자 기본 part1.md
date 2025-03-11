# CSS3 선택자 기본 part1

Date: 2025년 2월 28일
페이지: P.103~P.132
완료: Yes

## CSS 선택자 및 선택자 종류

CSS 선택자를 이용하면 특정 태그나 요소에 대해 스타일이나 기능을 적용할 수 있습니다. 일반적으로 HTML 문서의 `<head>` 부분에 `<style>` 태그를 이용해 작성합니다.

### 주요 선택자 종류

- **전체 선택자 ()**
    
    모든 태그를 한 번에 선택합니다.
    
- **태그 선택자**
    
    특정 태그를 선택합니다. 여러 태그를 선택하려면 쉼표로 구분합니다.
    
    예: `h1, h2, p`
    
- **아이디 선택자 (`#아이디`)**
    
    지정한 아이디 값을 가진 단 하나의 요소를 선택합니다. (아이디는 유일해야 합니다.)
    
    예: `#header`
    
- **클래스 선택자 (`.클래스`)**
    
    지정한 클래스를 가진 요소들을 선택합니다. 같은 클래스가 여러 요소에 적용될 수 있습니다.
    
    예: `.highlight` 또는 특정 태그에 한정할 때 `li.select`
    
- **속성 선택자**
    
    특정 속성과 그 값을 가진 요소를 선택합니다.
    
    예: `input[type="text"]`
    
    → 요소에 해당 속성이 있어야만 스타일이 적용됩니다.
    
- **후손 선택자 (Descendant Selector)**
    
    특정 부모 요소의 모든 후손(자식, 손자 등)을 선택합니다.
    
    예: `#header h1`는 id가 `header`인 요소 내부의 모든 `h1` 요소를 선택합니다.
    
    **주의:** `#header h1, h2`는 `h2`에 id 조건이 적용되지 않으므로, 올바른 작성은 `#header h1, #header h2`입니다.
    
- **자식 선택자 (Child Selector)**
    
    특정 부모의 **직접 자식**만 선택합니다.
    
    예: `#header > h1`는 id가 `header`인 요소의 바로 자식인 `h1` 요소만 선택합니다.
    
- **동위 선택자 (Sibling Selectors)**
    - **인접 형제 선택자 (`+`):** 바로 뒤에 위치한 형제 요소 한 개를 선택합니다.
    예: `h1 + h2` → `h1` 바로 뒤에 오는 `h2` 선택
    - **일반 형제 선택자 (`~`):** 뒤에 위치한 모든 형제 요소를 선택합니다.
    예: `h1 ~ h2` → `h1` 다음에 나오는 모든 `h2` 선택
- **반응(상태) 선택자 (Pseudo-classes)**
    
    특정 상태에 반응해 스타일을 적용합니다.
    
    - `:hover` → 마우스를 올렸을 때
    - `:active` → 클릭하는 순간

---

## 예제 코드

아래는 위에서 소개한 선택자들을 한 번에 확인할 수 있는 HTML 예제입니다.

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>CSS 선택자 예제</title>
  <style>
    /* 전체 선택자: 모든 태그에 기본 여백 제거 */
    * {
      margin: 0;
      padding: 0;
    }

    /* 태그 선택자: h1, h2, p에 파란색 텍스트 적용 */
    h1, h2, p {
      color: blue;
    }

    /* 아이디 선택자: id가 header인 요소에 배경색 적용 */
    #header {
      background-color: lightgray;
      padding: 10px;
    }

    /* 클래스 선택자: 클래스가 highlight인 요소에 굵은 빨간색 텍스트 */
    .highlight {
      color: red;
      font-weight: bold;
    }

    /* 특정 태그의 클래스 선택자: li 요소 중 class가 select인 경우 */
    li.select {
      color: green;
    }

    /* 속성 선택자: type이 "text"인 입력 필드에 테두리 적용 */
    input[type="text"] {
      border: 1px solid black;
      padding: 5px;
    }

    /* 후손 선택자: id가 header인 요소 내부의 모든 h1 선택 */
    #header h1 {
      font-size: 24px;
    }

    /* 자식 선택자: id가 header인 요소의 바로 자식 h1에 보더 적용 */
    #header > h1 {
      border-bottom: 2px solid blue;
    }

    /* 인접 동위 선택자 (+): h1 바로 뒤의 첫 h2에 스타일 적용 */
    h1 + h2 {
      margin-top: 10px;
      color: purple;
    }

    /* 일반 동위 선택자 (~): h1 뒤에 나오는 모든 h2에 이탤릭체 적용 */
    h1 ~ h2 {
      font-style: italic;
    }

    /* 반응 선택자: 마우스 오버될 때 a요소 밑줄 추가 */
    a:hover {
      text-decoration: underline;
    }

    /* 반응 선택자: a요소 클릭하면 텍스트 색상 변경 */
    a:active {
      color: orange;
    }
  </style>
</head>
<body>
  <!-- 아이디 선택자 예제를 위한 header 영역 -->
  <div id="header">
    <h1>사이트 헤더</h1>
    <h2>서브 헤더</h2>
  </div>

  <p>이 문장은 <span class="highlight">중요한</span> 정보를 포함합니다.</p>

  <ul>
    <li class="select">선택된 항목</li>
    <li>일반 항목</li>
  </ul>

  <form>
    <input type="text" placeholder="텍스트 입력">
    <input type="password" placeholder="비밀번호 입력">
  </form>

  <!-- 동위 선택자 예제 -->
  <h1>인접 및 일반 동위 선택자 예제</h1>
  <h2>바로 뒤에 오는 첫 h2 (h1 + h2 적용)</h2>
  <h2>이 h2는 h1과 일반 동위 선택자 적용(~)</h2>

  <!-- 반응 선택자 예제 -->
  <p>링크 예제: <a href="#">이곳에 마우스를 올리거나 클릭해 보세요.</a></p>
</body>
</html>

```

---

### 추가 설명

- **전체 선택자**를 사용하면 페이지 내의 모든 요소에 같은 속성을 적용할 수 있어 리셋(초기화) 스타일로 주로 사용됩니다.
- **아이디 선택자**는 한 문서 내에서 단 하나의 요소에만 적용되어야 하며, 고유한 식별자 역할을 합니다.
- **클래스 선택자**는 여러 요소에 공통 스타일을 적용할 때 사용되며, 클래스 이름은 여러 개를 공백으로 구분하여 부여할 수 있습니다.
- **후손 선택자**와 **자식 선택자**를 혼동하지 않도록 주의하세요. 후자는 모든 하위 요소에, 자식 선택자는 바로 아래(직접적인 자식) 요소에 적용됩니다.
- **동위 선택자**는 요소들의 순서에 따라 특정 위치에 있는 요소에 스타일을 적용할 수 있어 유용합니다.
- **반응 선택자**를 사용하면 사용자의 인터랙션에 따른 시각적 변화를 쉽게 줄 수 있습니다.

---

[CSS3 선택자 기본 part1 퀴즈와 연습문제](https://linen-artichoke-b37.notion.site/CSS3-part1-1b32ad07fb2080edb2c0d22c2b4ce97c?pvs=4)
# HTML5태그 기본 part2 퀴즈와연습문제

## 퀴즈

## HTML 학습 퀴즈

### 퀴즈 1: HTML 엔티티 코드

**문제:**  
다음 중 큰따옴표(`"`)를 HTML에 올바르게 표현하는 엔티티 코드는 무엇인가요?

- A. `&apos;`
- B. `&amp;`
- C. `&quot;`
- D. `&copy;`

> **정답:** C. `&quot;`  
>  
> **해설:** 큰따옴표는 `&quot;` 엔티티 코드를 사용하여 표현합니다.

### 퀴즈 2: 텍스트 강조 태그

**문제:**  
본문에서 **중요한** 내용을 강조하는 태그와, **단순히 스타일만** 적용하는 태그 중에서 의미론적으로 올바른 태그는 무엇일까요?

- A. `<b>`
- B. `<i>`
- C. `<em>`
- D. `<u>`

> **정답:** C. `<em>`  
>  
> **해설:** `<em>` 태그는 강조의 의미를 가지며, 화면 리더기에서 강조된 내용을 별도로 읽어줄 수 있습니다. `<b>`는 단순 볼드체 스타일만 적용됩니다.

### 퀴즈 3: 인용문 태그 구분

**문제:**  
짧은 인용문과 긴 인용문을 각각 적절하게 표현하기 위한 HTML 태그는 무엇일까요?

- A. 짧은 인용문: `<blockquote>`, 긴 인용문: `<q>`
- B. 짧은 인용문: `<q>`, 긴 인용문: `<blockquote>`
- C. 짧은 인용문: `<cite>`, 긴 인용문: `<address>`
- D. 짧은 인용문: `<dfn>`, 긴 인용문: `<abbr>`

> **정답:** B. 짧은 인용문: `<q>`, 긴 인용문: `<blockquote>`  
>  
> **해설:** `<q>`는 인라인 인용문을 위한 태그이고, `<blockquote>`는 긴 인용문의 경우 사용됩니다.

### 퀴즈 4: 폼 요소 구분

**문제:**  
사용자가 여러 줄의 텍스트를 입력할 수 있도록 하는 입력 요소는 무엇인가요?

- A. `<input type="text">`
- B. `<textarea>`
- C. `<select>`
- D. `<label>`

> **정답:** B. `<textarea>`  
>  
> **해설:** `<textarea>` 태그는 여러 줄의 텍스트를 입력받기 위해 사용됩니다.

### 퀴즈 5: 시멘틱 구조

**문제:**  
웹페이지의 내비게이션을 구성할 때 가장 적절한 태그는 무엇인가요?

- A. `<header>`
- B. `<nav>`
- C. `<article>`
- D. `<section>`

> **정답:** B. `<nav>`  
>  
> **해설:** `<nav>` 태그는 사이트의 주요 메뉴나 내비게이션 경로를 나타낼 때 사용되며, 시멘틱 마크업에 중요한 역할을 합니다.

## 연습문제

## 연습문제 1: HTML 엔티티 코드

**문제:**

HTML 문서에 다음 문자열을 올바르게 출력하려면, 적절한 HTML 엔티티 코드를 사용하여 코드를 작성하세요.

출력문:

```
A < B & C "D" 'E' ©

```

**예상 답안:**

```html
<p>A &lt; B &amp; C &quot;D&quot; &apos;E&apos; &copy;</p>

```

---

## 연습문제 2: 텍스트 관련 태그

**문제:**

다음 문장을 작성하여 각 부분을 지정된 태그로 강조해보세요.

문장:

```
HTML은 아주 중요한 언어입니다. 이 문장은 인용문 형태로 작성됩니다.

```

조건:

- "아주 중요한"은 `<strong>` 태그로 강조
- "인용문"은 `<q>` 태그로 작성
- 또한, 문장 전체는 `<p>` 태그 안에 작성

**예상 답안:**

```html
<p>
  HTML은 <strong>아주 중요한</strong> 언어입니다.
  이 문장은 <q>인용문</q> 형태로 작성됩니다.
</p>

```

---

## 연습문제 3: 콘텐츠 카테고리 이미지

**문제:**

콘텐츠 카테고리를 설명하는 이미지를 삽입하세요.

조건:

- 이미지 파일: `content.png`
- 대체 텍스트(alt): "콘텐츠 아이콘"
- 너비: 300, 높이: 200

**예상 답안:**

```html
<img src="content.png" alt="콘텐츠 아이콘" width="300" height="200">

```

---

## 연습문제 4: Video 태그 사용

**문제:**

다음 조건을 만족하는 비디오 태그를 작성하세요.

조건:

- 비디오 파일: `video.mp4`
- 포스터 이미지: `poster.jpg`
- 자동 재생(autoplay), 반복(loop), 컨트롤 표시(controls)
- 너비: 640, 높이: 360
- 브라우저가 지원하지 않을 경우 "비디오를 지원하지 않습니다." 메시지 출력

**예상 답안:**

```html
<video src="video.mp4" poster="poster.jpg" autoplay loop controls width="640" height="360">
  비디오를 지원하지 않습니다.
</video>

```

---

## 연습문제 5: 입력 양식 폼 만들기

**문제:**

사용자의 이름과 이메일을 입력받는 간단한 폼을 작성하세요.

조건:

- `<label>`과 `<input>` 태그를 사용하여 각각 “이름”과 “이메일” 항목을 만든다.
- `for`와 `id` 속성을 연결하여 접근성을 고려한다.
- 폼 제출 버튼을 포함한다.

**예상 답안:**

```html
<form action="/submit" method="post">
  <label for="name">이름:</label>
  <input type="text" id="name" name="name" placeholder="이름 입력"><br>
  <label for="email">이메일:</label>
  <input type="email" id="email" name="email" placeholder="이메일 입력"><br>
  <button type="submit">제출</button>
</form>

```

---

## 연습문제 6: 추가 입력 요소 활용하기

**문제:**

자기소개와 국가 선택을 위한 폼을 작성하세요.

조건:

- `<textarea>` 태그를 사용하여 자기소개를 입력 (cols: 30, rows: 5)
- `<select>` 태그 내에 두 개의 `<optgroup>` (예: "아시아", "유럽")를 사용하여 각각 두 개의 옵션(예: 한국, 일본 / 독일, 프랑스)을 제공

**예상 답안:**

```html
<form action="/submit" method="post">
  <fieldset>
    <legend>추가 정보 입력</legend>
    <label for="bio">자기소개:</label>
    <textarea id="bio" name="bio" cols="30" rows="5" placeholder="자기소개 입력"></textarea><br>
    <label for="country">국가 선택:</label>
    <select id="country" name="country">
      <optgroup label="아시아">
        <option value="kr">한국</option>
        <option value="jp">일본</option>
      </optgroup>
      <optgroup label="유럽">
        <option value="de">독일</option>
        <option value="fr">프랑스</option>
      </optgroup>
    </select>
  </fieldset>
</form>

```

---

## 연습문제 7: 공간 분할 태그 활용하기

**문제:**

`<div>`와 `<span>` 태그를 사용해서, 한 영역 내에 일반 텍스트와 강조된 텍스트를 작성하세요.

조건:

- 컨테이너 역할의 `<div>` 안에 "여기는 일반 텍스트이며, 여기에는 강조된 내용이 있습니다."를 작성
- 강조된 부분("강조된 내용")은 `<span>` 태그와 클래스 `highlight`를 사용

**예상 답안:**

```html
<div class="container">
  여기는 일반 텍스트이며, 여기에는 <span class="highlight">강조된 내용</span>이 있습니다.
</div>

```

---

## 연습문제 8: 시멘틱 구조 활용하기

**문제:**

웹페이지의 기본 레이아웃을 시멘틱 태그를 사용하여 구성하세요.

조건:

- `<header>`: 웹사이트 제목(예: "My Website") 포함
- `<nav>`: "홈", "소개", "연락처" 메뉴 (리스트로 구성)
- `<article>`: 주요 콘텐츠 영역 (예: "메인 콘텐츠" 텍스트 포함)
- `<aside>`: 보조 정보 영역 (사이드바 내용)
- `<footer>`: 바닥글 영역 (예: 저작권 정보)

**예상 답안:**

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>시멘틱 구조 예제</title>
</head>
<body>
  <header>
    <h1>My Website</h1>
    <nav>
      <ul>
        <li><a href="#">홈</a></li>
        <li><a href="#">소개</a></li>
        <li><a href="#">연락처</a></li>
      </ul>
    </nav>
  </header>
  <aside>
    <h2>사이드바</h2>
    <p>보조 정보가 여기에 표시됩니다.</p>
  </aside>
  <article>
    <h2>메인 콘텐츠</h2>
    <p>이곳에 주요 내용이 들어갑니다.</p>
  </article>
  <footer>
    <p>&copy; 2023 My Website. All rights reserved.</p>
  </footer>
</body>
</html>

```

---
# HTML5태그 기본 part2

Date: 2025년 2월 27일
페이지: P.71~P.100
완료: Yes
1일후 복습: Yes
7일후(주말) 복습: Yes
1달후 복습: No

# HTML 고급 요소 및 구조 요약본

## 1. HTML 엔티티 코드

HTML 엔티티 코드는 브라우저가 HTML 태그로 해석하지 않고 특수 문자로 표시해야 하는 문자들을 나타내는 방법입니다. 특수 기호, 예약 문자, 국제 문자 등을 웹 페이지에 안전하게 표시할 수 있게 해줍니다.

| 엔티티 코드 | 표시 문자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- | --- |
| `&nbsp;` | 공백 | 줄바꿈 없는 공백 | 여러 공백을 연속해서 표시할 때, 단어 사이에 강제 공백을 넣을 때 | `A&nbsp;&nbsp;B` → A  B |
| `&lt;` | < | 보다 작음 기호 | HTML 태그로 해석되지 않게 할 때 | `&lt;div&gt;` → \<div\> |
| `&gt;` | > | 보다 큼 기호 | HTML 태그로 해석되지 않게 할 때 | `&gt;` → > |
| `&amp;` | & | 앰퍼샌드 | 다른 엔티티 코드가 해석되지 않게 할 때 | `&amp;nbsp;` → |
| `&quot;` | " | 큰따옴표 | 속성값 내에서 큰따옴표를 표시할 때 | `<p title="&quot;인용&quot;">텍스트</p>` |
| `&apos;` | ' | 작은따옴표 | 속성값 내에서 작은따옴표를 표시할 때 | `<p title='&apos;인용&apos;'>텍스트</p>` |
| `&copy;` | © | 저작권 기호 | 저작권 정보 표시 시 | `&copy; 2023` → © 2023 |

## 2. 텍스트 서식 태그

HTML에서 다양한 텍스트 서식을 적용하는 태그들로, 시각적 효과뿐만 아니라 의미론적 구조도 제공합니다.

| 태그 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `<strong>` | 중요 텍스트 표시 (굵게) | 내용 중 특별히 중요한 부분 강조 시 | `<strong>중요 정보</strong>` |
| `<em>` | 강조 텍스트 (기울임) | 문장에서 강조하거나 억양이 필요한 부분 | `<em>강조된 부분</em>` |
| `<q>` | 짧은 인라인 인용문 | 텍스트 안에 직접 인용이 필요할 때 | `<q cite="출처 URL">인용문</q>` |
| `<blockquote>` | 블록 형식 인용문 | 문단 단위의 긴 인용이 필요할 때 | `<blockquote cite="출처 URL">긴 인용문...</blockquote>` |
| `<cite>` | 인용 출처 | 작품명, 논문, 웹사이트 등의 출처 표시 시 | `<cite>참고 자료 제목</cite>` |
| `<address>` | 연락처 정보 | 웹사이트 소유자, 기관, 작성자 정보 등 | `<address>서울시 강남구<br>이메일: example@mail.com</address>` |
| `<mark>` | 하이라이트 표시 | 검색어 강조, 주목해야 할 텍스트 표시 | `<mark>중요 키워드</mark>` |
| `<dfn>` | 용어 정의 | 문서에서 처음 소개되는 용어 정의 시 | `<dfn title="설명">용어</dfn>` |
| `<abbr>` | 약어 | 약어나 두문자어 사용 시 전체 의미 제공 | `<abbr title="HyperText Markup Language">HTML</abbr>` |
| `<sup>` | 윗첨자 | 수학식, 각주, 서수 등에 사용 | `x<sup>2</sup>` → x² |
| `<sub>` | 아랫첨자 | 화학식, 각주 등에 사용 | `H<sub>2</sub>O` → H₂O |
| `<kbd>` | 키보드 입력 | 사용자가 입력해야 하는 키보드 키 표시 | `<kbd>Ctrl</kbd> + <kbd>C</kbd>` |

## 3. 비디오 태그 및 속성

HTML5에서 도입된 `<video>` 태그는 외부 플러그인 없이 웹 페이지에 비디오를 삽입할 수 있게 해줍니다.

| 속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `src` | 비디오 파일 경로 | 재생할 비디오 파일 지정 시 | `<video src="video.mp4"></video>` |
| `poster` | 썸네일 이미지 | 비디오 로딩 중 또는 재생 전 표시할 이미지 | `<video poster="thumbnail.jpg"></video>` |
| `preload` | 사전 로딩 설정 | 페이지 로드 시 비디오 사전 로딩 여부 설정 (auto, metadata, none) | `<video preload="auto"></video>` |
| `autoplay` | 자동 재생 | 페이지 로드 시 비디오 자동 재생 (사용자 경험 고려 필요) | `<video autoplay></video>` |
| `loop` | 반복 재생 | 비디오 재생 완료 후 자동 반복 | `<video loop></video>` |
| `controls` | 컨트롤 표시 | 재생, 정지, 볼륨 등의 컨트롤 표시 | `<video controls></video>` |
| `width` / `height` | 크기 설정 | 비디오 플레이어 크기 설정 | `<video width="640" height="360"></video>` |

**전체 예시:**

```html
<video src="video.mp4" poster="thumbnail.jpg" controls width="640" height="360" preload="metadata">
  브라우저가 비디오 태그를 지원하지 않습니다.
</video>

```

## 4. 입력 양식 태그

웹 페이지에서 사용자 데이터를 수집하고 서버로 전송하기 위한 양식(Form) 관련 요소입니다.

### 4.1 기본 폼 구조

| 태그/속성 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `<form>` | 데이터 입력 양식 | 사용자로부터 데이터를 수집할 때 | `<form action="/submit" method="post">...</form>` |
| `action` | 데이터 전송 URL | 폼 데이터를 처리할 서버 스크립트 지정 | `<form action="/process.php">` |
| `method` | 전송 방식 | HTTP 메소드 지정(GET/POST) | `<form method="post">` |
| `<fieldset>` | 관련 요소 그룹화 | 관련 있는 입력 필드 묶기 | `<fieldset>...</fieldset>` |
| `<legend>` | 필드셋 제목 | 필드셋 그룹의 제목 지정 | `<fieldset><legend>개인정보</legend>...</fieldset>` |
| `<label>` | 입력 필드 레이블 | 입력 요소에 대한 설명 제공 (접근성 향상) | `<label for="username">이름:</label>` |

### 4.2 입력 필드 타입

| 입력 타입 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `text` | 일반 텍스트 입력 | 이름, 제목 등 짧은 텍스트 입력 시 | `<input type="text" name="username">` |
| `password` | 비밀번호 입력 | 비밀번호 입력 시 (문자가 *로 표시됨) | `<input type="password" name="pwd">` |
| `email` | 이메일 주소 입력 | 이메일 형식 검증이 필요한 경우 | `<input type="email" name="email">` |
| `number` | 숫자 입력 | 수량, 나이 등 숫자만 입력 시 | `<input type="number" min="0" max="100">` |
| `tel` | 전화번호 입력 | 전화번호 형식에 최적화된 입력 | `<input type="tel" name="phone">` |
| `checkbox` | 체크박스 | 여러 옵션 중 다중 선택 시 | `<input type="checkbox" name="hobby" value="reading">` |
| `radio` | 라디오 버튼 | 여러 옵션 중 단일 선택 시 | `<input type="radio" name="gender" value="male">` |
| `date` | 날짜 선택 | 연도, 월, 일 선택이 필요한 경우 | `<input type="date" name="birthday">` |
| `time` | 시간 선택 | 시간, 분 선택이 필요한 경우 | `<input type="time" name="meeting">` |
| `file` | 파일 업로드 | 파일 첨부가 필요한 경우 | `<input type="file" name="document">` |
| `color` | 색상 선택 | 색상 선택이 필요한 경우 | `<input type="color" name="theme">` |
| `range` | 범위 슬라이더 | 특정 범위 내 값 선택 시 | `<input type="range" min="0" max="10">` |
| `submit` | 제출 버튼 | 폼 데이터 전송 시 | `<input type="submit" value="제출하기">` |
| `reset` | 초기화 버튼 | 폼 입력 내용 초기화 시 | `<input type="reset" value="다시 작성">` |

### 4.3 추가 폼 요소

| 태그 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `<textarea>` | 다중 줄 텍스트 | 긴 텍스트, 댓글, 소개 등 입력 시 | `<textarea name="message" rows="5" cols="30"></textarea>` |
| `<select>` | 드롭다운 목록 | 여러 옵션 중 하나 선택 시 | `<select name="country">...</select>` |
| `<option>` | 선택 옵션 | select 요소 내 선택 항목 | `<option value="kr">한국</option>` |
| `<optgroup>` | 옵션 그룹 | 관련 옵션 묶기 | `<optgroup label="아시아"><option>...</option></optgroup>` |
| `<button>` | 버튼 요소 | 클릭 가능한 버튼 생성 | `<button type="submit">제출</button>` |

**전체 예시:**

```html
<form action="/submit" method="post">
  <fieldset>
    <legend>개인 정보</legend>
    <label for="name">이름:</label>
    <input type="text" id="name" name="name" required><br>

    <label for="email">이메일:</label>
    <input type="email" id="email" name="email"><br>

    <label for="birthdate">생년월일:</label>
    <input type="date" id="birthdate" name="birthdate"><br>

    <label>성별:</label>
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">남성</label>
    <input type="radio" id="female" name="gender" value="female">
    <label for="female">여성</label><br>

    <label for="country">국가:</label>
    <select id="country" name="country">
      <optgroup label="아시아">
        <option value="kr">한국</option>
        <option value="jp">일본</option>
      </optgroup>
      <optgroup label="유럽">
        <option value="fr">프랑스</option>
        <option value="de">독일</option>
      </optgroup>
    </select>
  </fieldset>

  <fieldset>
    <legend>추가 정보</legend>
    <label for="message">메시지:</label><br>
    <textarea id="message" name="message" rows="4" cols="40"></textarea>
  </fieldset>

  <button type="submit">제출하기</button>
  <button type="reset">초기화</button>
</form>

```

## 5. 공간 분할 및 시멘틱 구조

HTML 문서를 구조적으로 구성하기 위한 태그들로, 단순한 시각적 구분이 아닌 의미론적 구조를 제공합니다.

### 5.1 기본 분할 태그

| 태그 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `<div>` | 블록 레벨 컨테이너 | 요소들을 그룹화하여 스타일 적용 시 | `<div class="container">...</div>` |
| `<span>` | 인라인 컨테이너 | 텍스트의 일부분만 스타일 적용 시 | `<p>이것은 <span class="highlight">중요한</span> 내용입니다.</p>` |

### 5.2 시멘틱 구조 태그

| 태그 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `<header>` | 머리말 영역 | 페이지 상단, 섹션의 도입부 영역 | `<header><h1>웹사이트 제목</h1>...</header>` |
| `<nav>` | 내비게이션 영역 | 사이트 메뉴, 링크 모음 | `<nav><ul><li><a href="#">홈</a></li>...</ul></nav>` |
| `<main>` | 주요 콘텐츠 | 페이지의 핵심 콘텐츠 영역 | `<main><article>...</article></main>` |
| `<article>` | 독립적 콘텐츠 | 블로그 포스트, 뉴스 기사 등 | `<article><h2>제목</h2><p>내용...</p></article>` |
| `<section>` | 주제별 섹션 | 콘텐츠를 주제별로 그룹화 | `<section><h2>섹션 제목</h2>...</section>` |
| `<aside>` | 부가 정보 | 사이드바, 광고, 관련 링크 등 | `<aside><h3>관련 글</h3>...</aside>` |
| `<footer>` | 바닥글 영역 | 저작권 정보, 연락처, 사이트맵 등 | `<footer><p>&copy; 2023</p>...</footer>` |

**전체 예시:**

```html
<header>
  <h1>웹사이트 제목</h1>
  <nav>
    <ul>
      <li><a href="#">홈</a></li>
      <li><a href="#">소개</a></li>
      <li><a href="#">서비스</a></li>
      <li><a href="#">연락처</a></li>
    </ul>
  </nav>
</header>

<main>
  <article>
    <header>
      <h2>기사 제목</h2>
      <p>작성자: 홍길동 | 날짜: 2023-03-15</p>
    </header>
    <section>
      <h3>첫 번째 섹션</h3>
      <p>본문 내용...</p>
    </section>
    <section>
      <h3>두 번째 섹션</h3>
      <p>본문 내용...</p>
    </section>
    <footer>
      <p>태그: HTML, 시멘틱 웹, 웹 표준</p>
    </footer>
  </article>

  <aside>
    <h3>관련 기사</h3>
    <ul>
      <li><a href="#">관련 기사 1</a></li>
      <li><a href="#">관련 기사 2</a></li>
    </ul>
  </aside>
</main>

<footer>
  <p>&copy; 2023 웹사이트 이름. All rights reserved.</p>
  <address>
    연락처: <a href="mailto:info@example.com">info@example.com</a>
  </address>
</footer>

```

## 최종 요약

### 1. HTML 엔티티 코드

HTML에서 특수 문자를 표시하기 위한 코드로, `&nbsp;`(줄바꿈 없는 공백), `&lt;`(< 기호), `&gt;`(> 기호), `&amp;`(& 기호), `&quot;`(큰따옴표), `&apos;`(작은따옴표), `&copy;`(저작권 기호) 등이 있습니다. 이를 통해 HTML 태그로 해석되지 않고 문자 그대로 표시할 수 있습니다.

### 2. 텍스트 서식 태그

웹 페이지의 텍스트에 의미와 스타일을 부여하는 태그들로, `<strong>`(중요 강조), `<em>`(일반 강조), `<q>`(짧은 인용), `<blockquote>`(긴 인용), `<cite>`(출처 표시), `<address>`(연락처 정보), `<mark>`(하이라이트), `<dfn>`(용어 정의), `<abbr>`(약어), `<sub>`(아랫첨자), `<sup>`(윗첨자), `<kbd>`(키보드 입력) 등이 있습니다.

### 3. 비디오 태그 및 속성

`<video>` 태그를 통해 외부 플러그인 없이 웹 페이지에 비디오를 삽입할 수 있으며, `src`(비디오 파일 경로), `poster`(썸네일 이미지), `controls`(컨트롤 표시), `autoplay`(자동 재생), `loop`(반복 재생), `preload`(사전 로딩), `width`/`height`(크기 설정) 등의 속성으로 제어할 수 있습니다.

### 4. 입력 양식 태그

사용자로부터 정보를 수집하기 위한 `<form>` 요소와 다양한 입력 필드를 제공합니다. `<input type="text|password|email|number|checkbox|radio|file|date|...">`로 다양한 입력 유형을, `<textarea>`, `<select>`, `<option>` 등으로 추가 입력 요소를 만들 수 있으며, `<fieldset>`, `<legend>`, `<label>` 등으로 구조와 접근성을 향상시킬 수 있습니다.

### 5. 공간 분할 및 시멘틱 구조

의미 없는 `<div>`(블록 컨테이너), `<span>`(인라인 컨테이너)과 더불어 `<header>`(머리말), `<nav>`(내비게이션), `<main>`(주요 콘텐츠), `<article>`(독립 콘텐츠), `<section>`(주제별 섹션), `<aside>`(부가 정보), `<footer>`(바닥글) 등의 시멘틱 태그로 웹 페이지에 의미론적 구조를 제공합니다.

# HTML 고급 요소 및 구조 복습 퀴즈

## 1. HTML에서 "<div>" 태그를 그대로 텍스트로 표시하고 싶을 때 올바르게 사용해야 하는 엔티티 코드는?

A) `&div;`

B) `<div>`

C) `&lt;div&gt;`

D) `&#div;`

**정답: C) `&lt;div&gt;`**

**해설:** HTML에서 꺾쇠 괄호(`<`, `>`)는 태그의 시작과 끝을 나타내므로, 이를 텍스트로 표시하려면 엔티티 코드를 사용해야 합니다. `&lt;`는 less than 기호(`<`)를, `&gt;`는 greater than 기호(`>`)를 나타내는 엔티티 코드입니다. 따라서 `&lt;div&gt;`를 사용하면 브라우저는 이를 태그로 해석하지 않고 "\<div\>" 텍스트로 표시합니다.

## 2. 다음 중 텍스트의 의미론적 강조를 위해 사용해야 하는 태그는?

A) `<b>`

B) `<strong>`

C) `<i>`

D) `<mark>`

**정답: B) `<strong>`**

**해설:** `<strong>` 태그는 텍스트의 중요성을 의미론적으로 강조하기 위해 사용합니다. 단순히 시각적으로 굵게 표시하는 `<b>` 태그와는 달리 스크린 리더와 같은 보조 기술에서도 강조되어 읽히므로 접근성 측면에서도 더 좋습니다. `<i>` 태그는 시각적 이탤릭체를 위한 것이고, `<mark>` 태그는 하이라이트 효과를 주어 사용자의 주의를 끌기 위한 목적으로 사용됩니다.

## 3. HTML에서 비디오를 삽입할 때, 사용자에게 재생 컨트롤을 제공하려면 어떤 속성을 사용해야 하나요?

A) `playback`

B) `player`

C) `controls`

D) `autoplay`

**정답: C) `controls`**

**해설:** `<video>` 태그에 `controls` 속성을 추가하면 비디오 플레이어에 재생, 일시정지, 볼륨 조절, 탐색 등의 컨트롤이 표시됩니다. 이를 통해 사용자가 비디오 재생을 직접 제어할 수 있게 됩니다. `autoplay`는 페이지 로드 시 자동 재생을 설정하는 속성이고, `playback`과 `player`는 HTML 비디오 태그의 유효한 속성이 아닙니다.

## 4. 다음 중 이메일 주소 입력을 위해 가장 적합한 입력 필드 유형은?

A) `<input type="text">`

B) `<input type="mail">`

C) `<input type="email">`

D) `<input type="address">`

**정답: C) `<input type="email">`**

**해설:** HTML5에서 도입된 `<input type="email">`은 이메일 주소 입력에 특화된 필드 유형으로, 브라우저는 이메일 형식 검증을 자동으로 수행하고 모바일 키보드에서 '@' 기호와 같은 이메일 입력에 유용한 키를 표시합니다. `type="text"`는 일반 텍스트용이며 이메일 검증 기능이 없고, `type="mail"`과 `type="address"`는 HTML에 존재하지 않는 유형입니다.

## 5. 웹 페이지의 주요 내비게이션 메뉴를 마크업하는 데 가장 적합한 시멘틱 태그는?

A) `<menu>`

B) `<nav>`

C) `<links>`

D) `<navigation>`

**정답: B) `<nav>`**

**해설:** `<nav>` 태그는 웹 페이지 내에서 주요 내비게이션 링크의 집합을 나타내는 시멘틱 태그입니다. 이 태그를 사용하면 스크린 리더와 같은 보조 기기가 내비게이션 영역을 식별하고 건너뛸 수 있어 접근성이 향상됩니다. `<menu>` 태그는 명령 목록을 위한 것이며, `<links>`와 `<navigation>`은 HTML에 존재하지 않는 태그입니다.

## 6. 여러 옵션 중 하나만 선택해야 하는 폼 요소를 만들 때 가장 적합한 입력 타입은?

A) `<input type="checkbox">`

B) `<input type="select">`

C) `<input type="radio">`

D) `<input type="option">`

**정답: C) `<input type="radio">`**

**해설:** `<input type="radio">` 요소는 여러 옵션 중 하나만 선택해야 하는 경우에 사용됩니다. 같은 `name` 속성을 가진 라디오 버튼 그룹에서는 한 번에 하나의 옵션만 선택할 수 있습니다. `type="checkbox"`는 여러 항목을 동시에 선택할 수 있고, `type="select"`와 `type="option"`은 유효한 입력 타입이 아닙니다(`<select>`와 `<option>`은 별도의 태그로 존재).

## 7. HTML 문서에서 독립적으로 배포하거나 재사용할 수 있는 완결된 콘텐츠 블록을 마크업하기 위한 가장 적합한 시멘틱 태그는?

A) `<section>`

B) `<div>`

C) `<content>`

D) `<article>`

**정답: D) `<article>`**

**해설:** `<article>` 태그는 그 자체로 의미가 완전하고 독립적으로 배포하거나 재사용할 수 있는 콘텐츠 블록을 나타냅니다. 블로그 포스트, 신문 기사, 사용자 댓글, 제품 카드 등이 이에 해당합니다. `<section>` 태그는 관련 콘텐츠의 주제별 그룹화에 사용되고, `<div>`는 의미론적 가치 없이 순수하게 스타일링 목적으로 사용되며, `<content>`는 HTML에 존재하지 않는 태그입니다.

## 8. 다음 중 저작권 기호(©)를 HTML에 삽입하는 올바른 방법은?

A) `(c)`

B) `&copyright;`

C) `&copy;`

D) `&#169;`

**정답: C) `&copy;`** (참고: D도 정답이 될 수 있습니다)

**해설:** HTML에서 저작권 기호(©)를 삽입하는 가장 일반적인 방법은 `&copy;` 엔티티 코드를 사용하는 것입니다. 이 엔티티 코드는 모든 주요 브라우저에서 지원됩니다. `&#169;`도 동일한 결과를 보여주지만, `&copy;`가 더 가독성이 좋고 일반적으로 사용됩니다. `(c)`는 단순한 텍스트로 저작권 기호로 변환되지 않으며, `&copyright;`는 유효한 HTML 엔티티가 아닙니다.

## 9. 관련된 폼 요소들을 시각적으로나 의미론적으로 그룹화하는 데 사용되는 태그는?

A) `<group>`

B) `<fieldset>`

C) `<formgroup>`

D) `<section>`

**정답: B) `<fieldset>`**

**해설:** `<fieldset>` 태그는 HTML 폼에서 관련 있는 입력 요소들을 그룹화하는 데 사용됩니다. 이 태그는 일반적으로 `<legend>` 태그와 함께 사용되어 그룹의 제목이나 설명을 제공합니다. 이는 복잡한 폼에서 사용자가 쉽게 이해할 수 있도록 돕고, 스크린 리더와 같은 보조 기술에서도 구조를 명확히 전달합니다. `<group>`, `<formgroup>`은 HTML에 존재하지 않는 태그이며, `<section>`은 일반적인 콘텐츠 섹션을 위한 태그입니다.

## 10. 다음 중 비디오에 재생 전 표시할 썸네일 이미지를 지정하는 속성은?

A) `thumbnail`

B) `preview`

C) `poster`

D) `image`

**정답: C) `poster`**

**해설:** HTML `<video>` 태그의 `poster` 속성은 비디오가 로드되는 동안 또는 사용자가 재생 버튼을 누르기 전에 표시할 이미지를 지정합니다. 이는 사용자에게 비디오 내용에 대한 시각적 힌트를 제공하고 더 나은 사용자 경험을 만들어줍니다. 예: `<video src="video.mp4" poster="thumbnail.jpg" controls></video>`. `thumbnail`, `preview`, `image`는 HTML 비디오 태그의 유효한 속성이 아닙니다.

# HTML 고급 요소 및 구조 연습문제

## 연습문제 1: HTML 엔티티 코드 활용하기

**문제**:
다음 요구사항에 맞는 HTML 코드를 작성하세요.

1. "HTML에서 태그는 <angle brackets>로 둘러싸여 있습니다."라는 문장을 HTML 태그로 해석되지 않도록 표시하세요.
2. "COPYRIGHT © 2023"라는 텍스트를 저작권 기호를 엔티티 코드로 사용하여 표시하세요.
3. 연속된 세 개의 공백(" ")이 그대로 표시되도록 코드를 작성하세요.
4. "John's & David's Electronics" 문구에서 작은따옴표와 앰퍼샌드를 엔티티 코드로 표시하세요.

**정답**:

```html
<p>HTML에서 태그는 &lt;angle brackets&gt;로 둘러싸여 있습니다.</p>
<p>COPYRIGHT &copy; 2023</p>
<p>여기에&nbsp;&nbsp;&nbsp;공백이 있습니다.</p>
<p>John&apos;s &amp; David&apos;s Electronics</p>

```

**해설**:

1. HTML 태그로 해석되지 않도록 꺽쇠 괄호를 엔티티 코드로 변환하였습니다:
    - `<`는 `&lt;`(less than)으로 변환
    - `>`는 `&gt;`(greater than)으로 변환
2. 저작권 기호(©)는 `&copy;` 엔티티 코드를 사용하여 표시합니다.
3. 연속된 공백은 브라우저에서 하나의 공백으로 압축되므로, 줄바꿈 없는 공백 엔티티 코드 `&nbsp;`(non-breaking space)를 사용하여 세 개의 공백을 표시했습니다.
4. 특수 문자 처리:
    - 작은따옴표(')는 `&apos;` 엔티티 코드로 변환
    - 앰퍼샌드(&)는 `&amp;` 엔티티 코드로 변환 (이를 변환하지 않으면 다른 엔티티 코드의 시작으로 해석될 수 있음)

이러한 HTML 엔티티 코드를 사용하면 특수 문자를 웹 페이지에 안전하게 표시할 수 있으며, HTML 구문 해석 오류를 방지할 수 있습니다.

## 연습문제 2: 텍스트 서식 태그 활용하기

**문제**:
기술 블로그의 한 글을 다음 요구사항에 맞게 작성하세요.

1. "HTML 시맨틱 태그의 중요성"이라는 제목을 강조하세요.
2. "시맨틱 태그가 중요한 이유"라는 부제목을 만들고, 아래에 2개의 이유를 서술하세요.
3. 첫 번째 이유에서 "접근성"이라는 단어를 특별히 강조하세요.
4. Tim Berners-Lee의 다음 인용문을 인용 형식으로 추가하고 출처를 표시하세요: "The power of the Web is in its universality."
5. "HTML(HyperText Markup Language)"을 약어로 표시하고 마우스를 올렸을 때 전체 의미가 표시되도록 하세요.
6. 블로그 글 마지막에 작성자 연락처 정보를 추가하세요: "John Doe, [john@example.com](mailto:john@example.com)"

**정답**:

```html
<article>
  <h1><strong>HTML 시맨틱 태그의 중요성</strong></h1>

  <h2>시맨틱 태그가 중요한 이유</h2>
  <p>첫째, 시맨틱 태그는 웹 <mark>접근성</mark>을 향상시킵니다. 스크린 리더와 같은 보조 기술이 콘텐츠를 더 잘 이해하고 사용자에게 전달할 수 있습니다.</p>
  <p>둘째, 검색 엔진 최적화(SEO)에 도움이 됩니다. 검색 엔진은 시맨틱 태그를 통해 콘텐츠의 중요도와 의미를 더 잘 파악할 수 있습니다.</p>

  <blockquote cite="<https://www.w3.org/standards/webdesign/accessibility>">
    <p>"The power of the Web is in its universality."</p>
  </blockquote>
  <p><cite>- Tim Berners-Lee, W3C Director</cite></p>

  <p><abbr title="HyperText Markup Language">HTML</abbr>은 웹 페이지의 구조를 정의하는 마크업 언어입니다.</p>

  <footer>
    <address>
      작성자: John Doe<br>
      이메일: <a href="mailto:john@example.com">john@example.com</a>
    </address>
  </footer>
</article>

```

**해설**:

1. `<strong>` 태그를 사용하여 제목을 강조했습니다. 이는 중요성을 나타내는 의미론적 강조입니다.
2. `<h2>` 태그로 부제목을 만들고, 그 아래에 두 개의 단락(`<p>`)을 사용하여 이유를 서술했습니다.
3. `<mark>` 태그를 사용하여 "접근성"이라는 단어를 강조했습니다. 이는 형광펜으로 강조한 것과 같은 효과를 줍니다.
4. `<blockquote>` 태그를 사용하여 인용문을 표시하고, `cite` 속성으로 출처 URL을 제공했습니다. 또한 `<cite>` 태그를 사용하여 인용문의 출처(저자)를 별도로 표시했습니다.
5. `<abbr>` 태그와 `title` 속성을 사용하여 약어 "HTML"에 대한 전체 설명을 제공했습니다. 사용자가 마우스를 올리면 툴팁으로 전체 의미가 표시됩니다.
6. `<address>` 태그를 사용하여 연락처 정보를 표시했으며, 이메일 주소는 `<a href="mailto:...">` 형식으로 링크화했습니다.

이러한 텍스트 서식 태그들은 단순히 시각적 효과뿐만 아니라, 콘텐츠에 의미론적 구조를 부여하여 접근성과 SEO를 향상시킵니다.

## 연습문제 3: 비디오 태그 활용하기

**문제**:
회사 웹사이트의 제품 소개 페이지에 제품 시연 비디오를 다음 요구사항에 맞게 추가하세요.

1. 비디오 파일 "product-demo.mp4"를 재생하는 플레이어를 삽입하세요.
2. 비디오 로딩 전에 "product-thumbnail.jpg" 이미지를 썸네일로 표시하세요.
3. 사용자가 재생, 일시정지, 볼륨 조절 등의 컨트롤을 할 수 있도록 하세요.
4. 비디오 크기를 너비 800픽셀, 높이 450픽셀로 설정하세요.
5. 페이지 로딩 시 비디오 메타데이터만 미리 로드하도록 설정하세요.
6. 비디오 태그를 지원하지 않는 브라우저를 위한 대체 내용을 제공하세요.
7. 비디오 자동 재생은 하지 않도록 하세요.

**정답**:

```html
<div class="product-video">
  <h2>제품 시연 영상</h2>
  <video src="product-demo.mp4"
         poster="product-thumbnail.jpg"
         controls
         width="800"
         height="450"
         preload="metadata">
    죄송합니다. 귀하의 브라우저는 HTML5 비디오를 지원하지 않습니다.
    <a href="product-demo.mp4">비디오 파일 다운로드</a>
  </video>
  <p>위 영상에서 제품의 주요 기능을 확인하실 수 있습니다.</p>
</div>

```

**해설**:

1. `<video>` 태그를 사용하여 비디오 플레이어를 생성하고, `src` 속성으로 비디오 파일 경로를 지정했습니다.
2. `poster` 속성을 사용하여 비디오 로드 전이나 재생 전에 표시될 썸네일 이미지를 지정했습니다.
3. `controls` 속성을 추가하여 재생/일시정지, 볼륨, 진행 막대 등의 기본 컨트롤 UI를 표시했습니다.
4. `width`와 `height` 속성으로 비디오 플레이어 크기를 각각 800픽셀과 450픽셀로 설정했습니다.
5. `preload="metadata"` 속성을 사용하여 전체 비디오가 아닌 메타데이터(재생 시간, 해상도 등)만 미리 로드하도록 설정했습니다. 이는 페이지 로딩 속도와 대역폭을 절약하는 데 도움이 됩니다.
6. `<video>` 태그 사이에 대체 내용을 제공하여, 비디오 태그를 지원하지 않는 브라우저에서도 사용자가 비디오에 접근할 수 있는 방법(다운로드 링크)을 제시했습니다.
7. `autoplay` 속성을 사용하지 않음으로써 비디오 자동 재생을 비활성화했습니다. 자동 재생은 사용자 경험을 저해할 수 있고, 일부 브라우저에서는 제한될 수 있기 때문입니다.

이렇게 구성된 비디오 요소는 접근성과 사용자 경험을 모두 고려한 것으로, 다양한 환경과 브라우저에서 적절하게 작동합니다.

## 연습문제 4: 입력 양식 태그 활용하기

**문제**:
온라인 이벤트 등록 양식을 다음 요구사항에 맞게 작성하세요.

1. 양식이 제출되면 "register.php" 스크립트로 데이터를 POST 방식으로 전송하도록 설정하세요.
2. "개인 정보"와 "이벤트 선택" 섹션으로 구분하여 구조화하세요.
3. 개인 정보 섹션에 이름(필수), 이메일(필수), 전화번호, 생년월일 입력 필드를 추가하세요.
4. 이벤트 선택 섹션에 참여하고 싶은 이벤트를 선택할 수 있는 체크박스 목록(웹 세미나, 현장 워크숍, 네트워킹 이벤트)을 추가하세요.
5. 참석 예정 인원수를 선택할 수 있는 드롭다운 메뉴(1-5명)를 추가하세요.
6. 추가 요청사항을 입력할 수 있는 텍스트 영역을 추가하세요.
7. "등록하기"와 "초기화" 버튼을 추가하세요.

**정답**:

```html
<form action="register.php" method="post">
  <fieldset>
    <legend>개인 정보</legend>

    <div class="form-group">
      <label for="name">이름:</label>
      <input type="text" id="name" name="name" required>
    </div>

    <div class="form-group">
      <label for="email">이메일:</label>
      <input type="email" id="email" name="email" required>
    </div>

    <div class="form-group">
      <label for="phone">전화번호:</label>
      <input type="tel" id="phone" name="phone">
    </div>

    <div class="form-group">
      <label for="birthdate">생년월일:</label>
      <input type="date" id="birthdate" name="birthdate">
    </div>
  </fieldset>

  <fieldset>
    <legend>이벤트 선택</legend>

    <div class="form-group">
      <p>참여하고 싶은 이벤트를 선택하세요:</p>

      <input type="checkbox" id="webinar" name="events[]" value="webinar">
      <label for="webinar">웹 세미나</label><br>

      <input type="checkbox" id="workshop" name="events[]" value="workshop">
      <label for="workshop">현장 워크숍</label><br>

      <input type="checkbox" id="networking" name="events[]" value="networking">
      <label for="networking">네트워킹 이벤트</label>
    </div>

    <div class="form-group">
      <label for="attendees">참석 예정 인원수:</label>
      <select id="attendees" name="attendees">
        <option value="1">1명</option>
        <option value="2">2명</option>
        <option value="3">3명</option>
        <option value="4">4명</option>
        <option value="5">5명</option>
      </select>
    </div>

    <div class="form-group">
      <label for="requests">추가 요청사항:</label>
      <textarea id="requests" name="requests" rows="4" cols="50"></textarea>
    </div>
  </fieldset>

  <div class="form-actions">
    <button type="submit">등록하기</button>
    <button type="reset">초기화</button>
  </div>
</form>

```

**해설**:

1. `<form>` 태그에 `action="register.php"`와 `method="post"` 속성을 추가하여 양식 제출 시 데이터가 register.php로 POST 방식으로 전송되도록 설정했습니다.
2. `<fieldset>`과 `<legend>` 태그를 사용하여 양식을 "개인 정보"와 "이벤트 선택" 두 섹션으로 구조화했습니다. 이는 관련 입력 필드를 논리적으로 그룹화하는 데 도움이 됩니다.
3. 개인 정보 섹션에서:
    - `<input type="text">`로 이름 입력 필드 생성
    - `<input type="email">`로 이메일 입력 필드 생성
    - `<input type="tel">`로 전화번호 입력 필드 생성
    - `<input type="date">`로 생년월일 선택 필드 생성
    - 이름과 이메일 필드에는 `required` 속성을 추가하여 필수 입력 필드로 설정
4. 이벤트 선택 섹션에서 `<input type="checkbox">`를 사용하여 여러 이벤트를 선택할 수 있는 체크박스 목록을 만들었습니다. `name="events[]"`처럼 이름에 대괄호를 추가하여 서버 측에서 배열로 처리할 수 있게 했습니다.
5. `<select>` 태그와 내부의 `<option>` 태그를 사용하여 참석 예정 인원수를 선택하는 드롭다운 메뉴를 생성했습니다.
6. `<textarea>` 태그를 사용하여 여러 줄의 텍스트를 입력할 수 있는 추가 요청사항 필드를 생성했습니다. `rows`와 `cols` 속성으로 크기를 지정했습니다.
7. `<button>` 태그를 사용하여 양식 제출 및 초기화 버튼을 추가했습니다:
    - `type="submit"`은 양식을 제출하는 버튼
    - `type="reset"`은 양식의 모든 입력 값을 기본값으로 초기화하는 버튼

이 양식은 다양한 입력 필드 유형을 활용하고 구조적으로 정리되어, 사용자가 이벤트 등록 정보를 쉽게 입력할 수 있습니다. 또한 라벨을 적절히 사용하여 접근성도 향상되었습니다.

## 연습문제 5: 시맨틱 구조 태그 활용하기

**문제**:
다음 요구사항에 맞게 뉴스 웹사이트의 메인 페이지 구조를 HTML로 작성하세요.

1. 페이지 상단에 로고와 메인 메뉴(Home, News, Politics, Entertainment, Sports, Contact)를 포함하는 헤더를 추가하세요.
2. 메인 콘텐츠 영역에 "오늘의 주요 뉴스" 제목과 함께 두 개의 뉴스 기사를 추가하세요.
3. 각 뉴스 기사는 제목, 작성자, 날짜, 본문 첫 단락을 포함하고 "더 보기" 링크가 있어야 합니다.
4. 메인 콘텐츠 오른쪽에 "인기 기사"와 "구독하기" 섹션을 포함하는 사이드바를 추가하세요.
5. 페이지 하단에 저작권 정보, 개인정보 정책 링크, 사이트맵 링크를 포함하는 푸터를 추가하세요.
6. 모든 요소에 적절한 시맨틱 태그를 사용하세요.

**정답**:

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>뉴스 포털</title>
</head>
<body>
  <!-- 헤더 영역 -->
  <header>
    <div class="logo">
      <img src="logo.png" alt="뉴스 포털 로고">
    </div>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#news">News</a></li>
        <li><a href="#politics">Politics</a></li>
        <li><a href="#entertainment">Entertainment</a></li>
        <li><a href="#sports">Sports</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- 메인 콘텐츠 영역 -->
  <main>
    <section class="featured-news">
      <h1>오늘의 주요 뉴스</h1>

      <article>
        <header>
          <h2>첫 번째 뉴스 제목</h2>
          <p class="meta">
            작성자: <span class="author">홍길동</span> |
            날짜: <time datetime="2023-03-20">2023년 3월 20일</time>
          </p>
        </header>
        <p>첫 번째 뉴스 기사의 내용입니다. 이 기사는 최근 발생한 중요한 사건에 대해 다루고 있습니다.</p>
        <a href="article1.html">더 보기</a>
      </article>

      <article>
        <header>
          <h2>두 번째 뉴스 제목</h2>
          <p class="meta">
            작성자: <span class="author">김철수</span> |
            날짜: <time datetime="2023-03-20">2023년 3월 20일</time>
          </p>
        </header>
        <p>두 번째 뉴스 기사의 내용입니다. 이 기사는 최근 경제 동향에 대한 분석을 제공합니다.</p>
        <a href="article2.html">더 보기</a>
      </article>
    </section>

    <!-- 사이드바 영역 -->
    <aside>
      <section class="popular-articles">
        <h2>인기 기사</h2>
        <ul>
          <li><a href="#">인기 기사 제목 1</a></li>
          <li><a href="#">인기 기사 제목 2</a></li>
          <li><a href="#">인기 기사 제목 3</a></li>
        </ul>
      </section>

      <section class="subscription">
        <h2>구독하기</h2>
        <form>
          <label for="email">이메일 주소:</label>
          <input type="email" id="email" name="email" required>
          <button type="submit">구독</button>
        </form>
      </section>
    </aside>
  </main>

  <!-- 푸터 영역 -->
  <footer>
    <p>&copy; 2023 뉴스 포털. All rights reserved.</p>
    <nav>
      <ul>
        <li><a href="privacy.html">개인정보 정책</a></li>
        <li><a href="sitemap.html">사이트맵</a></li>
      </ul>
    </nav>
  </footer>
</body>
</html>

```

**해설**:

1. **헤더 영역**
    - `<header>` 태그를 사용하여 페이지 상단 영역을 정의했습니다.
    - 헤더 내부에 로고를 포함하고, `<nav>` 태그를 사용하여 메인 내비게이션 메뉴를 구성했습니다.
    - 메뉴 항목은 의미론적으로 목록에 해당하므로 `<ul>`, `<li>` 태그를 사용했습니다.
2. **메인 콘텐츠 영역**
    - `<main>` 태그를 사용하여 페이지의 주요 콘텐츠 영역을 정의했습니다.
    - 주요 뉴스 섹션은 `<section>` 태그로 그룹화하고, 각 뉴스 기사는 독립적인 콘텐츠이므로 `<article>` 태그를 사용했습니다.
    - 각 기사의 제목과 메타 정보는 `<header>` 태그로 묶고, 날짜는 `<time>` 태그와 `datetime` 속성을 사용하여 기계가 읽을 수 있는 형식으로 제공했습니다.
3. **사이드바 영역**
    - `<aside>` 태그를 사용하여 주요 콘텐츠와 관련은 있지만 분리된 부가 정보를 담는 사이드바를 정의했습니다.
    - 사이드바 내에서도 "인기 기사"와 "구독하기"라는 두 개의 구분된 섹션을 `<section>` 태그로 표시했습니다.
    - 구독 양식은 `<form>`, `<input>`, `<button>` 태그를 사용하여 구성했습니다.
4. **푸터 영역**
    - `<footer>` 태그를 사용하여 페이지 하단 영역을 정의했습니다.
    - 저작권 정보는 일반 텍스트와 `&copy;` 엔티티 코드를 사용했으며, 개인정보 정책과 사이트맵 링크는 다시 `<nav>` 태그를 사용하여 보조 내비게이션으로 구성했습니다.

이러한 시맨틱 태그 구조는 단순한 시각적 구분을 넘어 문서의 의미론적인 구조를 명확히 하여, 검색 엔진 최적화(SEO)와 접근성을 향상시킵니다. 또한 스크린 리더와 같은 보조 기술을 사용하는 사용자들이 웹 페이지를 더 잘 이해할 수 있도록 돕습니다.
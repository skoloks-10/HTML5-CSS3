# CSS3 선택자 기본 part1

Date: 2025년 2월 28일
페이지: P.103~P.132
완료: Yes
1일후 복습: Yes
7일후(주말) 복습: Yes
1달후 복습: No

# CSS 선택자 종합 요약본

## 1. CSS 선택자 개요

CSS 선택자(Selector)는 스타일을 적용할 HTML 요소를 지정하는 패턴입니다. 이를 통해 웹 페이지의 특정 요소나 요소 그룹을 선택하여 스타일을 적용할 수 있습니다. 선택자는 CSS의 기본이자 필수 요소로, 선택자의 종류와 사용법을 이해하면 효율적인 스타일링이 가능해집니다.

## 2. 기본 선택자

기본 선택자는 HTML 요소를 직접적으로 식별하는 가장 기본적인 선택자입니다.

### 2.1 전체 선택자

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `*` | 문서 내 모든 요소를 선택 | 전체 요소에 공통 스타일을 적용하거나, 스타일 초기화(CSS Reset)에 사용 | `* { margin: 0; padding: 0; }` |

### 2.2 태그 선택자

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `태그명` | 지정한 HTML 태그를 모두 선택 | 특정 태그에 공통 스타일을 적용할 때 사용 | `h1 { color: blue; }` |
| `태그명1, 태그명2` | 쉼표로 구분하여 여러 태그 선택 | 다수의 태그에 동일한 스타일을 적용할 때 사용 | `h1, h2, p { color: blue; }` |

### 2.3 아이디 선택자

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `#아이디명` | id 속성값이 일치하는 요소를 선택 | 페이지 내에서 유일한 요소에 스타일을 적용할 때 사용<br>(주의: HTML에서 id는 고유해야 함) | `#header { background-color: lightgray; }` |

### 2.4 클래스 선택자

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `.클래스명` | class 속성값이 일치하는 모든 요소 선택 | 동일한 스타일을 적용할 여러 요소를 그룹화할 때 사용 | `.highlight { color: red; }` |
| `태그명.클래스명` | 특정 태그 중에서 지정된 class를 가진 요소만 선택 | 특정 태그에 한정하여 클래스 스타일을 적용할 때 사용 | `li.select { color: green; }` |

### 2.5 속성 선택자

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `[속성]` | 지정된 속성을 가진 모든 요소 선택 | 특정 속성이 있는 요소만 스타일링할 때 사용 | `[disabled] { opacity: 0.5; }` |
| `[속성=값]` | 속성값이 정확히 일치하는 요소 선택 | 특정 속성의 값이 정확히 일치하는 요소에 스타일 적용 | `input[type="text"] { border: 1px solid black; }` |
| `[속성^=값]` | 속성값이 지정한 값으로 시작하는 요소 선택 | 특정 값으로 시작하는 속성을 가진 요소를 선택할 때 사용 | `[class^="btn-"] { padding: 5px 10px; }` |
| `[속성$=값]` | 속성값이 지정한 값으로 끝나는 요소 선택 | 특정 값으로 끝나는 속성을 가진 요소를 선택할 때 사용 | `[href$=".pdf"] { color: red; }` |
| `[속성*=값]` | 속성값이 지정한 값을 포함하는 요소 선택 | 특정 값을 포함하는 속성을 가진 요소를 선택할 때 사용 | `[class*="card"] { border-radius: 4px; }` |

## 3. 복합 선택자

복합 선택자는 두 개 이상의 선택자를 조합하여 더 구체적인 요소를 선택합니다.

### 3.1 후손 선택자

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `선택자1 선택자2` | 선택자1의 모든 하위(후손) 요소 중 선택자2에 해당하는 요소 선택 | 특정 요소 내부의 모든 하위 요소에 스타일을 적용할 때 사용 | `#header h1 { font-size: 24px; }` |

**주의사항**: `#header h1, h2`는 `#header` 내부의 `h1`과 모든 `h2`를 선택합니다. 만약 `#header` 내부의 `h1`과 `h2`만 선택하려면 `#header h1, #header h2`로 작성해야 합니다.

### 3.2 자식 선택자

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `선택자1 > 선택자2` | 선택자1의 직계 자식 중 선택자2에 해당하는 요소만 선택 | 특정 요소의 직접적인 자식에만 스타일을 적용할 때 사용 | `#header > h1 { border-bottom: 2px solid blue; }` |

### 3.3 동위 선택자

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `선택자1 + 선택자2` | 선택자1 바로 뒤에 위치한 선택자2 요소 한 개만 선택<br>(인접 형제 선택자) | 특정 요소 바로 뒤에 오는 형제 요소에 스타일을 적용할 때 사용 | `h1 + h2 { margin-top: 10px; }` |
| `선택자1 ~ 선택자2` | 선택자1 뒤에 위치한 모든 선택자2 요소 선택<br>(일반 형제 선택자) | 특정 요소 뒤에 오는 모든 형제 요소에 스타일을 적용할 때 사용 | `h1 ~ h2 { font-style: italic; }` |

## 4. 의사(가상) 클래스 선택자

의사 클래스는 요소의 특정 상태나 조건에 따라 스타일을 적용하는 선택자입니다.

### 4.1 상태 의사 클래스

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `:hover` | 마우스 포인터가 요소 위에 있을 때 선택 | 마우스 오버 효과를 적용할 때 사용 | `a:hover { text-decoration: underline; }` |
| `:active` | 요소가 활성화된 상태(클릭하는 순간)일 때 선택 | 클릭 효과를 적용할 때 사용 | `a:active { color: orange; }` |
| `:focus` | 요소가 포커스를 받았을 때 선택 | 입력 필드가 선택되었을 때 스타일을 적용할 때 사용 | `input:focus { border-color: blue; }` |
| `:visited` | 방문했던 링크 선택 | 방문한 링크에 다른 색상을 적용할 때 사용 | `a:visited { color: purple; }` |

### 4.2 구조적 의사 클래스

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `:first-child` | 부모 요소의 첫 번째 자식인 요소 선택 | 목록의 첫 번째 항목 등에 특별한 스타일을 적용할 때 사용 | `li:first-child { font-weight: bold; }` |
| `:last-child` | 부모 요소의 마지막 자식인 요소 선택 | 목록의 마지막 항목 등에 특별한 스타일을 적용할 때 사용 | `li:last-child { border-bottom: none; }` |
| `:nth-child(n)` | 부모 요소의 n번째 자식인 요소 선택 | 특정 순서의 요소에 스타일을 적용할 때 사용 | `tr:nth-child(odd) { background-color: #f2f2f2; }` |
| `:not(선택자)` | 지정한 선택자와 일치하지 않는 요소 선택 | 특정 요소를 제외한 모든 요소에 스타일을 적용할 때 사용 | `input:not([type="submit"]) { border: 1px solid gray; }` |

## 최종 요약

### 1. 기본 선택자

- **전체 선택자 ()**: 모든 HTML 요소를 선택하며, 초기화 스타일에 주로 사용합니다.
- **태그 선택자 (`태그명`)**: 특정 HTML 태그를 선택하며, 기본 스타일 정의에 사용합니다.
- **아이디 선택자 (`#아이디명`)**: 고유 ID를 가진 단일 요소를 선택하며, 페이지에서 유일해야 합니다.
- **클래스 선택자 (`.클래스명`)**: 동일 클래스를 가진 여러 요소를 선택하며, 재사용 가능한 스타일에 적합합니다.
- **속성 선택자 (`[속성=값]`)**: 특정 속성과 값을 가진 요소를 선택하며, 폼 요소 등 속성 기반 스타일링에 유용합니다.

### 2. 복합 선택자

- **후손 선택자 (`선택자1 선택자2`)**: 특정 요소 내의 모든 하위 요소를 선택합니다.
- **자식 선택자 (`선택자1 > 선택자2`)**: 특정 요소의 직접적인 자식만 선택합니다.
- **인접 형제 선택자 (`선택자1 + 선택자2`)**: 선택자1 바로 다음에 오는 선택자2 요소 하나를 선택합니다.
- **일반 형제 선택자 (`선택자1 ~ 선택자2`)**: 선택자1 다음에 오는 모든 선택자2 요소를 선택합니다.

### 3. 의사 클래스 선택자

- **상태 의사 클래스 (`:hover`, `:active` 등)**: 요소의 상태에 따라 선택하며, 상호작용 효과에 사용합니다.
- **구조적 의사 클래스 (`:first-child`, `:nth-child(n)` 등)**: 요소의 구조적 위치에 따라 선택하며, 패턴 스타일링에 유용합니다.

CSS 선택자를 효과적으로 조합하면 HTML 구조를 변경하지 않고도 원하는 요소에 정확하게 스타일을 적용할 수 있으며, 이는 유지보수성과 코드 효율성을 높이는 데 중요한 역할을 합니다.

# CSS 선택자 복습 퀴즈

## 1. 다음 중 페이지 내의 모든 요소에 동일한 스타일을 적용하는 선택자는?

A) `.all`

B) `body`

C) `*`

D) `#all`

**정답: C) `*`**

**해설:** 별표(`*`)는 전체 선택자로, HTML 문서 내의 모든 요소를 선택합니다. 주로 마진과 패딩을 초기화하는 등의 리셋 스타일에 사용됩니다. `.all`은 클래스 선택자, `#all`은 ID 선택자, `body`는 body 태그만 선택하는 태그 선택자입니다.

## 2. 아래 CSS 코드에서 `#header h1`은 어떤 요소를 선택하는가?

```css
#header h1 {
  font-size: 24px;
}

```

A) id가 header인 요소의 직계 자식인 h1 요소만

B) id가 header인 요소의 모든 자손 중 h1 요소

C) header 클래스를 가진 모든 h1 요소

D) 문서 내 모든 h1 요소와 header id를 가진 요소

**정답: B) id가 header인 요소의 모든 자손 중 h1 요소**

**해설:** 이것은 후손 선택자(descendant selector)로, 첫 번째 선택자(#header)에 의해 선택된 요소 내부의 모든 하위 요소(자식, 손자, 증손자 등) 중에서 두 번째 선택자(h1)와 일치하는 요소를 모두 선택합니다. 직계 자식만 선택하려면 자식 선택자(`#header > h1`)를 사용해야 합니다.

## 3. 다음 중 올바르게 클래스 선택자를 사용한 예는?

A) `p[highlight]`

B) `p.highlight`

C) `p#highlight`

D) `p:highlight`

**정답: B) `p.highlight`**

**해설:** `p.highlight`는 p 태그 중에서 "highlight" 클래스를 가진 요소만 선택합니다. `p[highlight]`는 highlight 속성을 가진 p 태그를 선택하는 속성 선택자, `p#highlight`는 highlight ID를 가진 p 태그를 선택하는 ID 선택자, `p:highlight`는 highlight라는 의사 클래스를 가진 p 태그를 선택하려는 것인데 유효한 의사 클래스가 아닙니다.

## 4. 다음 중 인접 형제 선택자(adjacent sibling selector)의 올바른 사용법은?

A) `div ~ p`

B) `div > p`

C) `div p`

D) `div + p`

**정답: D) `div + p`**

**해설:** 인접 형제 선택자는 `+` 기호를 사용하며, 첫 번째 요소 바로 다음에 위치한 형제 요소 한 개만 선택합니다. 따라서 `div + p`는 div 요소 바로 뒤에 오는 첫 번째 p 요소만 선택합니다. `div ~ p`는 일반 형제 선택자로 div 뒤의 모든 p 요소를, `div > p`는 자식 선택자로 div의 직계 자식 p 요소를, `div p`는 후손 선택자로 div 내부의 모든 p 요소를 선택합니다.

## 5. `li:nth-child(odd) { background-color: #f2f2f2; }` 코드의 효과는?

A) 모든 li 요소에 회색 배경 적용

B) li 요소 중 홀수 번째에 회색 배경 적용

C) li 요소 중 짝수 번째에 회색 배경 적용

D) 첫 번째와 마지막 li 요소에 회색 배경 적용

**정답: B) li 요소 중 홀수 번째에 회색 배경 적용**

**해설:** `:nth-child(odd)`는 부모 요소의 자식 요소 중 홀수 번째(1번, 3번, 5번...)에 위치한 요소를 선택합니다. 따라서 `li:nth-child(odd)`는 li 요소 중에서 부모 요소 내에서 홀수 번째에 위치한 요소에 회색 배경을 적용합니다. 짝수 번째를 선택하려면 `:nth-child(even)`을, 특정 패턴을 선택하려면 `:nth-child(an+b)` 형식을 사용합니다.

## 6. 마우스를 올렸을 때(hover)와 클릭하는 순간(active)에 다른 스타일을 적용하려면 어떤 선택자를 사용해야 하는가?

A) `a:select`, `a:click`

B) `a:on`, `a:press`

C) `a:hover`, `a:active`

D) `a:mouse`, `a:down`

**정답: C) `a:hover`, `a:active`**

**해설:** CSS에서 마우스를 올렸을 때 스타일을 변경하려면 `:hover` 의사 클래스를, 요소를 클릭하는 순간의 스타일을 지정하려면 `:active` 의사 클래스를 사용합니다. 이 두 선택자는 사용자 상호작용에 따른 시각적 피드백을 제공하는 데 매우 유용합니다. 다른 선택지에 있는 선택자들은 CSS에 존재하지 않는 잘못된 의사 클래스입니다.

## 7. `#header h1, h2`와 `#header h1, #header h2`의 차이점은?

A) 차이가 없다

B) 첫 번째는 id가 header인 요소 내의 h1과 모든 h2를 선택하고, 두 번째는 id가 header인 요소 내의 h1과 h2만 선택한다

C) 첫 번째는 id가 header인 요소 내의 h1만 선택하고, 두 번째는 id가 header인 요소 내의 h1과 h2를 모두 선택한다

D) 첫 번째는 id가 header인 요소와 h1, h2를 모두 선택하고, 두 번째는 id가 header인 요소 내의 h1과 h2만 선택한다

**정답: B) 첫 번째는 id가 header인 요소 내의 h1과 모든 h2를 선택하고, 두 번째는 id가 header인 요소 내의 h1과 h2만 선택한다**

**해설:** CSS 선택자에서 쉼표(,)는 여러 선택자를 그룹화하는 역할을 합니다. `#header h1, h2`는 "#header h1"과 "h2"라는 두 개의 독립적인 선택자로 해석되므로, id가 header인 요소 내의 모든 h1과 문서 내의 모든 h2를 선택합니다. 반면 `#header h1, #header h2`는 "#header h1"과 "#header h2"라는 두 선택자로, id가 header인 요소 내의 h1과 h2만 선택합니다.

## 8. 아래 HTML에서 `.select` 클래스를 가진 li 요소만 선택하는 올바른 CSS 선택자는?

```html
<ul>
  <li class="select">항목 1</li>
  <li>항목 2</li>
  <li class="select">항목 3</li>
</ul>

```

A) `ul select`

B) `li .select`

C) `ul > .select`

D) `li.select`

**정답: D) `li.select`**

**해설:** `li.select`는 li 태그 중에서 "select" 클래스를 가진 요소만 선택하는 선택자입니다. `ul select`는 ul 내의 select 태그를, `li .select`는 li 태그 내부의 select 클래스를 가진 요소를, `ul > .select`는 ul의 직계 자식 중 select 클래스를 가진 요소를 선택하지만, 예제 HTML에서는 li 요소 자체가 select 클래스를 가지고 있으므로 `li.select`가 올바른 선택자입니다.

## 9. 입력 필드 중에서 type이 "text"인 요소만 선택하는 선택자는?

A) `input.text`

B) `input:type("text")`

C) `input[type="text"]`

D) `input#text`

**정답: C) `input[type="text"]`**

**해설:** 속성 선택자는 대괄호(`[]`) 안에 속성과 값을 지정하여 사용합니다. `input[type="text"]`는 input 요소 중에서 type 속성의 값이 "text"인 요소만 선택합니다. `input.text`는 "text" 클래스를 가진 input 요소를, `input#text`는 "text" ID를 가진 input 요소를 선택하고, `input:type("text")`는 유효하지 않은 문법입니다.

## 10. 다음 중 자식 선택자(Child Selector)의 설명으로 올바른 것은?

A) 특정 요소의 모든 하위 요소를 선택한다

B) 특정 요소의 직접적인 자식만 선택한다

C) 특정 요소와 같은 부모를 가진 요소를 선택한다

D) 특정 요소 바로 다음에 오는 요소를 선택한다

**정답: B) 특정 요소의 직접적인 자식만 선택한다**

**해설:** 자식 선택자는 '>' 기호를 사용하여 표현하며, 첫 번째 선택자로 선택된 요소의 직접적인 자식(direct children)만 선택합니다. 예를 들어, `#header > h1`은 id가 header인 요소의 직계 자식 중 h1 요소만 선택합니다. 모든 하위 요소를 선택하는 것은 후손 선택자(공백으로 표시), 같은 부모를 가진 요소는 형제 선택자(~ 또는 +), 바로 다음에 오는 요소는 인접 형제 선택자(+)의 설명입니다.

# CSS 선택자 연습문제

## 연습문제 1: 기본 선택자 활용하기

**문제**:
다음 HTML 구조가 있을 때, 아래 요구사항을 충족하는 CSS 선택자를 작성하세요.

```html
<div class="container">
  <h1 id="main-title">웹사이트 제목</h1>
  <p class="intro">환영합니다!</p>

  <div class="content-box">
    <h2 class="section-title">첫 번째 섹션</h2>
    <p>일반 단락 텍스트입니다.</p>
    <p class="highlight">중요한 내용입니다!</p>
    <a href="<https://example.com>" target="_blank">링크</a>
  </div>

  <div class="sidebar">
    <h2 class="section-title">사이드바</h2>
    <ul>
      <li><a href="#home">홈</a></li>
      <li><a href="#about">소개</a></li>
      <li><a href="#contact" class="important">문의하기</a></li>
    </ul>
  </div>

  <input type="text" placeholder="검색" disabled>
  <input type="submit" value="검색">
</div>

```

요구사항:

1. 모든 제목(h1, h2)에 파란색 글자색 적용
2. ID가 "main-title"인 요소에만 밑줄 적용
3. "highlight" 클래스를 가진 모든 단락에 노란색 배경 적용
4. disabled 속성을 가진 모든 입력 필드에 회색 배경 적용
5. 새 창으로 열리는 링크(target="_blank")에 빨간색 글자색 적용

**정답**:

```css
/* 1. 모든 제목에 파란색 글자색 적용 */
h1, h2 {
  color: blue;
}

/* 2. ID가 "main-title"인 요소에만 밑줄 적용 */
#main-title {
  text-decoration: underline;
}

/* 3. "highlight" 클래스를 가진 모든 단락에 노란색 배경 적용 */
p.highlight {
  background-color: yellow;
}

/* 4. disabled 속성을 가진 모든 입력 필드에 회색 배경 적용 */
input[disabled] {
  background-color: gray;
}

/* 5. 새 창으로 열리는 링크에 빨간색 글자색 적용 */
a[target="_blank"] {
  color: red;
}

```

**해설**:

1. **태그 선택자(h1, h2)**: 쉼표를 사용하여 여러 태그를 그룹화하고 동일한 스타일을 적용했습니다. 이 선택자는 모든 h1과 h2 요소를 선택합니다.
2. **ID 선택자(#main-title)**: 해시(#) 기호를 사용하여 특정 ID를 가진 요소를 선택했습니다. ID는 페이지에서 고유해야 하므로, 이 선택자는 정확히 하나의 요소만 선택합니다.
3. **태그와 클래스 선택자 조합(p.highlight)**: p 요소 중에서 "highlight" 클래스를 가진 요소만 선택합니다. 이는 다른 태그(예: div)에 같은 클래스가 있어도 선택하지 않습니다.
4. **속성 선택자(input[disabled])**: disabled 속성이 있는 input 요소를 선택합니다. 이 선택자는 속성의 존재 여부만 확인합니다.
5. **속성 값 선택자(a[target="_blank"])**: target 속성의 값이 정확히 "_blank"인 a 요소를 선택합니다. 이 방식으로 새 창으로 열리는 링크만 스타일링할 수 있습니다.

## 연습문제 2: 복합 선택자 활용하기

**문제**:
다음 HTML 구조가 있을 때, 아래 요구사항을 충족하는 CSS 선택자를 작성하세요.

```html
<nav class="main-nav">
  <ul>
    <li><a href="#home">홈</a></li>
    <li><a href="#services">서비스</a></li>
    <li><a href="#about">소개</a></li>
    <li><a href="#contact">연락처</a></li>
  </ul>
</nav>

<section class="content">
  <article>
    <h2>첫 번째 글</h2>
    <p>첫 번째 문단입니다.</p>
    <p>두 번째 문단입니다.</p>
    <ul class="tags">
      <li>태그1</li>
      <li>태그2</li>
      <li>태그3</li>
    </ul>
  </article>

  <article>
    <h2>두 번째 글</h2>
    <p>첫 번째 문단입니다.</p>
    <p>두 번째 문단입니다.</p>
    <ul class="tags">
      <li>태그1</li>
      <li>태그2</li>
    </ul>
  </article>

  <aside>
    <h3>관련 글</h3>
    <ul>
      <li><a href="#">관련 글 1</a></li>
      <li><a href="#">관련 글 2</a></li>
    </ul>
  </aside>
</section>

```

요구사항:

1. "main-nav" 클래스 내의 모든 링크에만 흰색 글자색 적용
2. "content" 클래스 내에 있는 직계 자식 "article" 요소에만 테두리 적용
3. 모든 "article" 요소 내의 첫 번째 단락에만 굵은 글씨 적용
4. 헤더(h2) 바로 다음에 오는 단락에만 들여쓰기 적용
5. "tags" 클래스를 가진 목록 내의 모든 항목에 배경색 적용

**정답**:

```css
/* 1. "main-nav" 클래스 내의 모든 링크에만 흰색 글자색 적용 */
.main-nav a {
  color: white;
}

/* 2. "content" 클래스 내에 있는 직계 자식 "article" 요소에만 테두리 적용 */
.content > article {
  border: 1px solid #ccc;
}

/* 3. 모든 "article" 요소 내의 첫 번째 단락에만 굵은 글씨 적용 */
article p:first-of-type {
  font-weight: bold;
}

/* 4. 헤더(h2) 바로 다음에 오는 단락에만 들여쓰기 적용 */
h2 + p {
  text-indent: 20px;
}

/* 5. "tags" 클래스를 가진 목록 내의 모든 항목에 배경색 적용 */
.tags li {
  background-color: #f0f0f0;
}

```

**해설**:

1. **후손 선택자(.main-nav a)**: "main-nav" 클래스를 가진 요소 내부의 모든 a 요소를 선택합니다. 이는 깊이에 상관없이 모든 후손 요소를 대상으로 합니다.
2. **자식 선택자(.content > article)**: "content" 클래스를 가진 요소의 직계 자식 중 article 요소만 선택합니다. 이는 더 깊은 중첩 레벨에 있는 article은 선택하지 않습니다.
3. **의사 클래스 선택자(article p:first-of-type)**: 각 article 내에서 첫 번째로 등장하는 p 요소를 선택합니다. 이는 모든 article 내의 첫 단락에 스타일을 적용합니다.
4. **인접 형제 선택자(h2 + p)**: h2 요소 바로 다음에 오는 p 요소만 선택합니다. 이는 제목 바로 다음의 첫 단락에만 들여쓰기를 적용합니다.
5. **후손 선택자(.tags li)**: "tags" 클래스를 가진 요소 내부의 모든 li 요소를 선택합니다. 이는 태그 목록의 모든 항목에 배경색을 적용합니다.

## 연습문제 3: 의사 클래스 선택자 활용하기

**문제**:
다음 HTML 구조가 있을 때, 아래 요구사항을 충족하는 CSS 선택자를 작성하세요.

```html
<form class="signup-form">
  <div class="form-group">
    <label for="username">사용자 이름:</label>
    <input type="text" id="username" required>
  </div>

  <div class="form-group">
    <label for="email">이메일:</label>
    <input type="email" id="email" required>
  </div>

  <div class="form-group options">
    <label>관심사:</label>
    <div>
      <input type="checkbox" id="interest-tech" name="interests">
      <label for="interest-tech">기술</label>
    </div>
    <div>
      <input type="checkbox" id="interest-design" name="interests">
      <label for="interest-design">디자인</label>
    </div>
    <div>
      <input type="checkbox" id="interest-business" name="interests">
      <label for="interest-business">비즈니스</label>
    </div>
  </div>

  <div class="form-group">
    <button type="submit">가입하기</button>
    <button type="reset">초기화</button>
  </div>
</form>

<ul class="features-list">
  <li>첫 번째 기능</li>
  <li>두 번째 기능</li>
  <li>세 번째 기능</li>
  <li>네 번째 기능</li>
  <li>다섯 번째 기능</li>
</ul>

```

요구사항:

1. 사용자가 입력 필드에 포커스했을 때 파란색 테두리 적용
2. 체크박스가 체크되었을 때, 해당 체크박스 바로 다음에 오는 레이블에만 굵은 글씨 적용
3. 필수 입력 필드(required 속성이 있는)에 별표(*) 표시 추가
4. 기능 목록의 홀수 번째 항목에만 회색 배경 적용
5. 마지막 기능 항목에만 특별한 강조 스타일(굵은 글씨와 다른 색상) 적용

**정답**:

```css
/* 1. 사용자가 입력 필드에 포커스했을 때 파란색 테두리 적용 */
input:focus {
  border: 2px solid blue;
  outline: none; /* 기본 포커스 외곽선 제거 */
}

/* 2. 체크박스가 체크되었을 때, 해당 체크박스 바로 다음에 오는 레이블에만 굵은 글씨 적용 */
input[type="checkbox"]:checked + label {
  font-weight: bold;
}

/* 3. 필수 입력 필드(required 속성이 있는)에 별표(*) 표시 추가 */
input[required]::after {
  content: " *";
  color: red;
}

/* 또는 레이블에 별표 추가하기 (더 일반적인 접근법) */
label[for="username"]::after,
label[for="email"]::after {
  content: " *";
  color: red;
}

/* 4. 기능 목록의 홀수 번째 항목에만 회색 배경 적용 */
.features-list li:nth-child(odd) {
  background-color: #f0f0f0;
}

/* 5. 마지막 기능 항목에만 특별한 강조 스타일 적용 */
.features-list li:last-child {
  font-weight: bold;
  color: #ff6600;
}

```

**해설**:

1. **상태 의사 클래스(:focus)**: 사용자가 현재 상호작용하고 있는(포커스된) 입력 필드를 선택합니다. 추가로 outline: none을 적용하여 브라우저의 기본 포커스 외곽선을 제거했습니다.
2. **상태 의사 클래스와 인접 형제 선택자 조합(:checked + label)**: 체크된 체크박스 바로 다음에 오는 label 요소를 선택합니다. 이 조합은 사용자가 체크박스를 선택했을 때 레이블 스타일을 동적으로 변경하는 데 유용합니다.
3. **속성 선택자와 의사 요소 조합**:
    - `input[required]::after`는 required 속성이 있는 input 요소 뒤에 콘텐츠를 추가합니다. 그러나 실제로는 input 요소에 ::after 의사 요소를 사용할 수 없기 때문에 동작하지 않습니다.
    - 대안으로 레이블에 별표를 추가하는 방법을 제시했습니다. 이는 더 일반적이고 효과적인 접근법입니다.
4. **구조적 의사 클래스(:nth-child(odd))**: 부모 요소 내에서 홀수 번째 위치에 있는 자식 요소를 선택합니다. 이는 1번, 3번, 5번 항목을 선택합니다.
5. **구조적 의사 클래스(:last-child)**: 부모 요소의 마지막 자식을 선택합니다. 이는 목록의 마지막 항목에 특별한 스타일을 적용합니다.

## 연습문제 4: 속성 선택자 활용하기

**문제**:
다음 HTML 구조가 있을 때, 아래 요구사항을 충족하는 CSS 선택자를 작성하세요.

```html
<div class="resource-library">
  <h2>리소스 라이브러리</h2>

  <div class="resources">
    <a href="document.pdf" class="resource" data-type="document">
      회사 소개서 <span class="size">(2.5MB)</span>
    </a>

    <a href="presentation.pptx" class="resource" data-type="presentation">
      제품 발표자료 <span class="size">(4.8MB)</span>
    </a>

    <a href="spreadsheet.xlsx" class="resource" data-type="spreadsheet">
      분기별 보고서 <span class="size">(1.2MB)</span>
    </a>

    <a href="image.jpg" class="resource" data-type="image">
      제품 이미지 <span class="size">(3.7MB)</span>
    </a>

    <a href="video.mp4" class="resource" data-type="video">
      홍보 영상 <span class="size">(15.2MB)</span>
    </a>
  </div>

  <div class="external-links">
    <a href="<https://example.com/resources>" target="_blank">외부 리소스</a>
    <a href="mailto:info@example.com">이메일 문의</a>
    <a href="tel:+821012345678">전화 문의</a>
  </div>
</div>

```

요구사항:

1. PDF 파일 링크에만 빨간색 아이콘 추가
2. 프레젠테이션 파일(pptx)과 스프레드시트 파일(xlsx)에 공통 스타일 적용
3. "document" 데이터 타입을 가진 리소스에만 밑줄 적용
4. 메일 링크(mailto:로 시작하는)에만 특별한 아이콘 추가
5. 외부 링크(http 또는 https로 시작하는)에만 "새 창에서 열림" 텍스트 추가

**정답**:

```css
/* 1. PDF 파일 링크에만 빨간색 아이콘 추가 */
a[href$=".pdf"]::before {
  content: "📕 ";
  color: red;
}

/* 2. 프레젠테이션 파일(pptx)과 스프레드시트 파일(xlsx)에 공통 스타일 적용 */
a[href$=".pptx"],
a[href$=".xlsx"] {
  background-color: #f5f5f5;
  padding: 5px;
  border-radius: 3px;
}

/* 3. "document" 데이터 타입을 가진 리소스에만 밑줄 적용 */
a[data-type="document"] {
  text-decoration: underline;
}

/* 4. 메일 링크(mailto:로 시작하는)에만 특별한 아이콘 추가 */
a[href^="mailto:"]::before {
  content: "✉️ ";
}

/* 5. 외부 링크(http 또는 https로 시작하는)에만 "새 창에서 열림" 텍스트 추가 */
a[href^="http"]::after {
  content: " (새 창에서 열림)";
  font-size: 0.8em;
  color: #666;
}

```

**해설**:

1. **속성값 끝 부분 매칭 선택자([href$=".pdf"])와 의사 요소(::before)**: href 속성이 ".pdf"로 끝나는 링크를 선택하고, 그 앞에 빨간색 아이콘을 추가합니다. 의사 요소 ::before는 선택된 요소의 내용 앞에 콘텐츠를 삽입합니다.
2. **속성값 끝 부분 매칭 선택자와 그룹화**:
    - `a[href$=".pptx"], a[href$=".xlsx"]`는 href 속성이 ".pptx" 또는 ".xlsx"로 끝나는 링크를 모두 선택합니다.
    - 쉼표를 사용하여 여러 선택자를 그룹화하여 동일한 스타일을 적용합니다.
3. **속성 값 정확히 일치 선택자([data-type="document"])**: data-type 속성이 정확히 "document"인 요소를 선택합니다. 이는 커스텀 데이터 속성을 활용한 선택 방법을 보여줍니다.
4. **속성값 시작 부분 매칭 선택자([href^="mailto:"])**: href 속성이 "mailto:"로 시작하는 링크를 선택합니다. 이를 통해 이메일 링크만 특별하게 스타일링할 수 있습니다.
5. **속성값 시작 부분 매칭 선택자([href^="http"])**: href 속성이 "http"로 시작하는(http와 https 모두 포함) 링크를 선택합니다. 의사 요소 ::after를 사용하여 링크 내용 뒤에 추가 텍스트를 삽입합니다.

## 연습문제 5: 복합 선택자 종합 활용하기

**문제**:
다음 HTML 구조가 있을 때, 아래 요구사항을 충족하는 CSS 선택자를 작성하세요.

```html
<div class="blog">
  <article class="post featured">
    <header>
      <h2 class="post-title">주요 소식</h2>
      <p class="post-meta">작성자: 관리자 | 작성일: 2023-03-15</p>
    </header>
    <div class="post-content">
      <p>첫 번째 문단입니다.</p>
      <p>두 번째 문단입니다.</p>
      <blockquote>인용구입니다.</blockquote>
      <p>세 번째 문단입니다.</p>
    </div>
    <footer class="post-footer">
      <button class="btn like-btn">좋아요</button>
      <button class="btn share-btn">공유하기</button>
    </footer>
  </article>

  <article class="post">
    <header>
      <h2 class="post-title">일반 글</h2>
      <p class="post-meta">작성자: 사용자1 | 작성일: 2023-03-10</p>
    </header>
    <div class="post-content">
      <p>일반 글의 내용입니다.</p>
    </div>
    <footer class="post-footer">
      <button class="btn like-btn">좋아요</button>
      <button class="btn share-btn">공유하기</button>
    </footer>
  </article>

  <aside class="sidebar">
    <section class="widget">
      <h3>최근 글</h3>
      <ul>
        <li><a href="#">글 제목 1</a></li>
        <li><a href="#">글 제목 2</a></li>
        <li><a href="#">글 제목 3</a></li>
      </ul>
    </section>

    <section class="widget widget-tags">
      <h3>태그</h3>
      <div class="tag-cloud">
        <a href="#" class="tag">웹개발</a>
        <a href="#" class="tag">CSS</a>
        <a href="#" class="tag">JavaScript</a>
      </div>
    </section>
  </aside>
</div>

```

요구사항:

1. "featured" 클래스를 가진 게시물의 제목에만 특별한 스타일 적용
2. 모든 게시물의 인용구(blockquote) 앞뒤에 따옴표 추가
3. 게시물 내용(post-content) 안에 있는 모든 단락 중 첫 번째 단락에만 들여쓰기 제거
4. "widget-tags" 클래스를 가진 위젯 내부의 태그 링크에만 배경색 적용
5. 좋아요 버튼(like-btn)에만 호버 시 색상 변경 효과 적용

**정답**:

```css
/* 1. "featured" 클래스를 가진 게시물의 제목에만 특별한 스타일 적용 */
.post.featured .post-title {
  color: gold;
  font-size: 1.5em;
  border-bottom: 2px solid gold;
}

/* 2. 모든 게시물의 인용구(blockquote) 앞뒤에 따옴표 추가 */
.post-content blockquote::before {
  content: """;
  font-size: 2em;
  color: #ccc;
}

.post-content blockquote::after {
  content: """;
  font-size: 2em;
  color: #ccc;
}

/* 3. 게시물 내용 안에 있는 모든 단락 중 첫 번째 단락에만 들여쓰기 제거 */
.post-content p:first-of-type {
  text-indent: 0;
}

/* 4. "widget-tags" 클래스를 가진 위젯 내부의 태그 링크에만 배경색 적용 */
.widget.widget-tags .tag {
  background-color: #f0f0f0;
  padding: 3px 8px;
  border-radius: 3px;
  display: inline-block;
  margin: 2px;
}

/* 5. 좋아요 버튼에만 호버 시 색상 변경 효과 적용 */
.like-btn:hover {
  background-color: #ff6b6b;
  color: white;
}

```

**해설**:

1. **다중 클래스 선택자와 후손 선택자 조합(.post.featured .post-title)**:
    - `.post.featured`는 "post"와 "featured" 두 클래스를 모두 가진 요소를 선택합니다.
    - 그 뒤에 공백을 두고 `.post-title`을 추가하여 그 안에 있는 제목 요소를 선택합니다.
    - 이 복합 선택자는 일반 게시물이 아닌 특별 게시물의 제목만 선택합니다.
2. **후손 선택자와 의사 요소 조합(.post-content blockquote::before/::after)**:
    - `.post-content blockquote`는 게시물 내용 안에 있는 인용구를 선택합니다.
    - `::before`와 `::after` 의사 요소를 사용하여 인용구 앞뒤에 컨텐츠를 추가합니다.
    - 인용 부호를 큰 크기로 표시하고 회색으로 만들어 시각적으로 구분합니다.
3. **의사 클래스 선택자(.post-content p:first-of-type)**:
    - `:first-of-type`은 같은 유형의 형제 요소 중 첫 번째 요소를 선택합니다.
    - `.post-content p:first-of-type`는 게시물 내용 안에서 첫 번째 p 요소를 선택합니다.
    - 이렇게 선택된 첫 단락에만 들여쓰기를 제거합니다.
4. **다중 클래스 선택자와 후손 선택자 조합(.widget.widget-tags .tag)**:
    - `.widget.widget-tags`는 "widget"과 "widget-tags" 클래스를 모두 가진 요소를 선택합니다.
    - 그 뒤에 `.tag`를 추가하여 그 안에 있는 태그 링크만 선택합니다.
    - 이 선택자는 태그 위젯 내부의 태그에만 특별한 스타일을 적용합니다.
5. **상태 의사 클래스(.like-btn:hover)**:
    - `:hover` 의사 클래스는 마우스 포인터가 요소 위에 있을 때 적용됩니다.
    - `.like-btn:hover`는 좋아요 버튼에 마우스를 올렸을 때만 스타일을 적용합니다.
    - 이 선택자로 인해 사용자가 좋아요 버튼에 마우스를 올렸을 때 배경색이 빨간색으로 변하고 텍스트가 흰색으로 바뀌어 시각적 피드백을 제공합니다.

이 연습문제는 여러 종류의 CSS 선택자를 조합하여 복잡한 HTML 구조에서 특정 요소만 정확하게 선택하는 방법을 보여줍니다. 클래스 조합, 후손 선택자, 의사 클래스, 의사 요소 등 다양한 선택자 기술을 함께 사용함으로써 HTML 구조를 변경하지 않고도 세밀한 스타일링이 가능합니다. 이러한 선택자 조합은 대규모 웹사이트에서 스타일 충돌을 방지하고 코드의 유지보수성을 향상시키는 데 중요합니다.
# CSS3 선택자 기본 part2

Date: 2025년 3월 1일
페이지: P.133~P.152
완료: Yes
1일후 복습: Yes
7일후(주말) 복습: Yes
1달후 복습: No

# CSS 의사 클래스 및 선택자 종합 요약본

## 1. 의사 클래스와 의사 요소 개요

CSS 의사 클래스(Pseudo-classes)와 의사 요소(Pseudo-elements)는 HTML 문서의 특정 상태나 부분을 선택하기 위한 특수 선택자입니다. 이를 통해 마크업을 변경하지 않고도 다양한 상황이나 구조에 따라 요소에 스타일을 적용할 수 있습니다.

- **의사 클래스**는 콜론(`:`) 하나를 사용하여 표시하며, 요소의 특정 상태를 선택합니다.
- **의사 요소**는 콜론(`:`) 두 개(`::`)를 사용하여 표시하며, 요소의 특정 부분을 선택합니다.

## 2. 상태 선택자 (State Pseudo-classes)

상태 선택자는 요소의 현재 상태나 조건을 기반으로 선택합니다. 주로 폼 요소와 상호작용할 때 유용합니다.

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `:checked` | 체크된 상태의 입력 요소 선택 | 체크박스나 라디오 버튼이 선택되었을 때 시각적 피드백 제공 | `input:checked { background-color: lightblue; }` |
| `:focus` | 포커스를 받은 요소 선택 | 입력 필드가 활성화되었을 때 사용자에게 시각적 피드백 제공 | `input:focus { border-color: blue; box-shadow: 0 0 5px rgba(0,0,255,0.5); }` |
| `:enabled` | 활성화된 입력 요소 선택 | 사용 가능한 폼 요소에 기본 스타일 적용 | `input:enabled { background-color: #fff; }` |
| `:disabled` | 비활성화된 입력 요소 선택 | 사용할 수 없는 폼 요소를 시각적으로 표시 | `input:disabled { background-color: #ddd; cursor: not-allowed; }` |

## 3. 구조 선택자 (Structural Pseudo-classes)

구조 선택자는 문서 구조 내에서 요소의 위치에 따라 선택합니다. 특히 반복되는 요소 그룹에서 특정 위치의 요소에 스타일을 적용할 때 유용합니다.

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `:first-child` | 부모 내 첫 번째 자식 요소 선택 | 목록의 첫 번째 항목이나 표의 첫 행에 특별한 스타일 적용 | `li:first-child { font-weight: bold; }` |
| `:last-child` | 부모 내 마지막 자식 요소 선택 | 목록의 마지막 항목에 테두리 제거 등 | `li:last-child { border-bottom: none; }` |
| `:nth-child(n)` | 부모 내 n번째 자식 요소 선택 | 표의 짝수/홀수 행에 다른 배경색 적용 | `tr:nth-child(odd) { background-color: #f2f2f2; }` |
| `:nth-last-child(n)` | 부모 내 끝에서 n번째 자식 요소 선택 | 목록의 마지막에서 특정 위치에 있는 항목 강조 | `li:nth-last-child(2) { font-style: italic; }` |

### 3.1 nth-child 표현식

| 표현식 | 설명 | 예시 코드 |
| --- | --- | --- |
| `n` | 0부터 증가하는 모든 정수 (모든 요소 선택) | `p:nth-child(n) { color: blue; }` |
| `2n` 또는 `even` | 모든 짝수 위치 요소 | `tr:nth-child(even) { background-color: #f2f2f2; }` |
| `2n+1` 또는 `odd` | 모든 홀수 위치 요소 | `tr:nth-child(odd) { background-color: #e6e6e6; }` |
| `3n` | 3의 배수 위치 요소 | `li:nth-child(3n) { border-bottom: 2px solid #ddd; }` |
| `3n+1` | 1, 4, 7, ... 위치 요소 | `li:nth-child(3n+1) { font-weight: bold; }` |
| `n+5` | 5번째부터 모든 요소 | `li:nth-child(n+5) { color: gray; }` |
| `-n+5` | 처음부터 5번째까지의 요소 | `li:nth-child(-n+5) { font-weight: bold; }` |

## 4. 형태 구조 선택자 (Type-based Structural Pseudo-classes)

형태 구조 선택자는 같은 유형(태그)의 요소들 중에서 특정 위치에 있는 요소를 선택합니다. 여러 유형의 요소가 혼합된 구조에서 특히 유용합니다.

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `:first-of-type` | 같은 유형 중 첫 번째 요소 선택 | 다양한 요소가 섞인 컨테이너에서 첫 단락만 강조 | `p:first-of-type { font-size: 1.2em; }` |
| `:last-of-type` | 같은 유형 중 마지막 요소 선택 | 여러 헤더가 있는 섹션에서 마지막 헤더만 스타일 적용 | `h2:last-of-type { border-bottom: 1px solid #ddd; }` |
| `:nth-of-type(n)` | 같은 유형 중 n번째 요소 선택 | 블로그 포스트에서 두 번째 이미지만 확대 | `img:nth-of-type(2) { width: 100%; }` |
| `:nth-last-of-type(n)` | 같은 유형 중 끝에서 n번째 요소 선택 | 문서 끝부분에서 마지막에서 두 번째 단락을 강조 | `p:nth-last-of-type(2) { font-style: italic; }` |

## 5. 문자 선택자 (Textual Pseudo-elements)

문자 선택자는 요소 내의 특정 텍스트 부분을 선택합니다. 이들은 의사 요소로, 대부분 두 개의 콜론(`::`)으로 표기합니다.

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `::first-letter` | 요소의 첫 글자 선택 | 단락 시작 부분에 드롭캡 효과 적용 | `p::first-letter { font-size: 2em; float: left; margin-right: 5px; }` |
| `::first-line` | 요소의 첫 줄 선택 | 텍스트의 첫 줄을 강조하여 가독성 향상 | `p::first-line { font-weight: bold; }` |
| `::before` | 요소 내용 앞에 내용 삽입 | 목록 항목 앞에 아이콘 추가 | `li::before { content: "★ "; color: gold; }` |
| `::after` | 요소 내용 뒤에 내용 삽입 | 필수 입력 필드에 별표 표시 추가 | `label.required::after { content: " *"; color: red; }` |
| `::selection` | 사용자가 선택한 텍스트 부분 스타일링 | 선택한 텍스트에 특별한 배경색 적용 | `::selection { background-color: lightblue; color: navy; }` |

## 6. 링크 선택자 (Link Pseudo-classes)

링크 선택자는 하이퍼링크(`<a>` 태그)의 다양한 상태를 선택합니다.

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `:link` | 방문하지 않은 링크 선택 | 아직 클릭하지 않은 링크에 기본 스타일 지정 | `a:link { color: blue; }` |
| `:visited` | 이미 방문한 링크 선택 | 사용자가 이미 방문한 페이지 링크를 구분 | `a:visited { color: purple; }` |
| `:hover` | 마우스를 올린 링크 선택 | 마우스 오버 효과로 사용자 상호 작용 유도 | `a:hover { text-decoration: underline; color: #ff6600; }` |
| `:active` | 클릭 중인 링크 선택 | 링크를 클릭하는 순간에 시각적 피드백 제공 | `a:active { color: red; }` |

## 7. 부정 선택자 (Negation Pseudo-class)

부정 선택자는 특정 조건을 만족하지 않는 요소를 선택합니다.

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `:not(선택자)` | 지정한 선택자와 일치하지 않는 요소 선택 | 특정 클래스를 제외한 모든 요소에 스타일 적용 | `li:not(.active) { opacity: 0.6; }` |
| `:not(선택자1):not(선택자2)` | 복수의 조건을 모두 만족하지 않는 요소 선택 | 여러 조건을 제외한 요소에 스타일 적용 | `input:not([type="submit"]):not([type="reset"]) { border: 1px solid #ccc; }` |

## 8. 기타 유용한 의사 클래스

| 선택자 | 설명 | 사용 상황 | 예시 코드 |
| --- | --- | --- | --- |
| `:root` | 문서의 루트 요소(HTML) 선택 | 전역 CSS 변수 정의 등에 사용 | `:root { --main-color: #336699; }` |
| `:empty` | 자식 요소나 텍스트가 없는 요소 선택 | 콘텐츠가 없는 요소 숨기기 | `div:empty { display: none; }` |
| `:target` | 현재 URI의 조각 식별자(#)와 일치하는 요소 선택 | 페이지 내 앵커 대상 강조 | `section:target { background-color: #ffffd8; }` |
| `:lang(언어)` | 지정한 언어로 된 콘텐츠를 가진 요소 선택 | 다국어 콘텐츠에서 언어별 스타일 적용 | `:lang(ko) { font-family: 'Nanum Gothic', sans-serif; }` |

## 최종 요약

### 1. 상태 선택자

상태 선택자는 요소의 현재 상태를 기반으로 스타일을 적용합니다. `:checked`(체크된 요소), `:focus`(포커스된 요소), `:enabled`(활성화된 요소), `:disabled`(비활성화된 요소) 등이 있으며, 주로 폼 요소의 상호작용에 시각적 피드백을 제공하는 데 사용됩니다.

### 2. 구조 선택자

구조 선택자는 HTML 문서 구조에서 요소의 위치를 기준으로 선택합니다. `:first-child`(첫 번째 자식), `:last-child`(마지막 자식), `:nth-child(n)`(n번째 자식) 등의 선택자를 사용해 목록, 테이블 등에서 특정 위치의 요소에 스타일을 적용할 수 있습니다.

### 3. 형태 구조 선택자

형태 구조 선택자는 같은 유형(태그)의 요소 중에서 위치를 기준으로 선택합니다. `:first-of-type`(같은 유형 중 첫 번째), `:last-of-type`(같은 유형 중 마지막), `:nth-of-type(n)`(같은 유형 중 n번째) 등이 있으며, 여러 유형의 요소가 혼합된 구조에서 유용합니다.

### 4. 문자 선택자

문자 선택자(의사 요소)는 요소의 특정 부분을 선택합니다. `::first-letter`(첫 글자), `::first-line`(첫 줄), `::before`(내용 앞), `::after`(내용 뒤), `::selection`(선택된 텍스트)과 같은 선택자를 사용해 텍스트의 특정 부분을 스타일링하거나 추가 콘텐츠를 삽입할 수 있습니다.

### 5. 링크 선택자

링크 선택자는 하이퍼링크의 다양한 상태를 선택합니다. `:link`(방문하지 않은 링크), `:visited`(방문한 링크), `:hover`(마우스 오버 상태), `:active`(클릭 중인 상태)를 사용해 링크의 다양한 상호작용 상태에 스타일을 적용합니다.

### 6. 부정 선택자

`:not(선택자)` 부정 선택자는 지정한 조건을 만족하지 않는 요소를 선택합니다. 특정 요소를 제외하고 스타일을 적용할 때 유용하며, 복수의 `:not()` 선택자를 연결하여 여러 조건을 적용할 수 있습니다.

### 7. 기타 유용한 의사 클래스

`:root`(루트 요소), `:empty`(빈 요소), `:target`(URI 조각 대상), `:lang()`(특정 언어) 등의 선택자는 특수한 상황에서 유용하게 사용됩니다.

CSS 의사 클래스와 의사 요소는 HTML 마크업을 변경하지 않고도 다양한 상태와 구조에 따른 스타일링을 가능하게 하며, 이를 통해 더 동적이고 반응형 있는 웹 디자인을 구현할 수 있습니다.

# CSS 의사 클래스 및 선택자 복습 퀴즈

## 1. 다음 중 체크박스가 선택되었을 때 스타일을 적용하는 올바른 선택자는?

A) `input:active`

B) `input:selected`

C) `input:checked`

D) `input:marked`

**정답: C) `input:checked`**

**해설:** `:checked` 의사 클래스는 체크박스나 라디오 버튼 같은 입력 요소가 체크된 상태인 경우를 선택합니다. 이를 통해 사용자가 선택한 항목에 시각적 피드백을 제공할 수 있습니다. `:active`는 클릭하는 순간의 상태, `:selected`와 `:marked`는 CSS에 존재하지 않는 선택자입니다.

## 2. 다음 CSS 코드의 효과는 무엇인가요?

```css
li:nth-child(odd) {
    background-color: #f2f2f2;
}

```

A) 모든 li 요소에 회색 배경을 적용한다

B) li 요소 중 홀수 번째 항목에 회색 배경을 적용한다

C) li 요소 중 짝수 번째 항목에 회색 배경을 적용한다

D) li 요소 중 2개씩 건너뛰며 회색 배경을 적용한다

**정답: B) li 요소 중 홀수 번째 항목에 회색 배경을 적용한다**

**해설:** `:nth-child(odd)` 의사 클래스는 부모 요소의 모든 자식 요소 중에서 홀수 번째(1번, 3번, 5번...)에 위치한 요소를 선택합니다. 따라서 이 코드는 li 요소 중 홀수 번째 항목에 연한 회색(#f2f2f2) 배경색을 적용합니다. 이러한 스타일은 테이블이나 목록의 가독성을 높이기 위해 줄무늬(striped) 효과를 만들 때 자주 사용됩니다.

## 3. `p:first-of-type`과 `p:first-child`의 차이점은 무엇인가요?

A) 차이가 없다

B) `p:first-of-type`은 첫 번째 p 요소를, `p:first-child`는 부모의 첫 번째 자식이 p 요소일 때만 선택한다

C) `p:first-of-type`은 각 부모 내 첫 번째 p 요소를, `p:first-child`는 문서 내 첫 번째 p 요소만 선택한다

D) `p:first-of-type`은 부모의 첫 번째 자식을, `p:first-child`는 부모 내 첫 번째 p 요소를 선택한다

**정답: B) `p:first-of-type`은 첫 번째 p 요소를, `p:first-child`는 부모의 첫 번째 자식이 p 요소일 때만 선택한다**

**해설:** 두 선택자의 핵심 차이점은 다음과 같습니다:

- `p:first-child`: 부모 요소의 첫 번째 자식이 p 요소일 경우에만 선택합니다. 만약 p 요소 앞에 다른 요소가 있다면 아무것도 선택되지 않습니다.
- `p:first-of-type`: 부모 요소 내에서 p 태그 중에 첫 번째로 등장하는 요소를 선택합니다. p 요소 앞에 다른 요소가 있더라도, p 요소 중에서 첫 번째라면 선택됩니다.

예를 들어 `<div><h1>제목</h1><p>첫 단락</p><p>두번째 단락</p></div>`에서 `p:first-child`는 아무것도 선택하지 않지만, `p:first-of-type`은 "첫 단락"을 선택합니다.

## 4. 다음 CSS 코드의 효과는 무엇인가요?

```css
p::first-letter {
    font-size: 2em;
    color: red;
}

```

A) 모든 p 요소를 빨간색으로 표시한다

B) p 요소의 첫 번째 단어를 크게 표시한다

C) p 요소의 첫 글자만 크고 빨간색으로 표시한다

D) p 요소의 첫 번째 줄을 빨간색으로 표시한다

**정답: C) p 요소의 첫 글자만 크고 빨간색으로 표시한다**

**해설:** `::first-letter` 의사 요소는 요소의 첫 글자만을 선택합니다. 이 코드는 모든 p 요소의 첫 번째 글자의 크기를 주변 텍스트의 2배(`font-size: 2em`)로 키우고 빨간색(`color: red`)으로 표시합니다. 이는 인쇄 디자인에서 볼 수 있는 '드롭 캡(drop cap)' 효과를 웹 페이지에 적용하는 데 자주 사용됩니다. 첫 단어 전체에 적용하려면 `::first-line`이 아니라 JavaScript나 별도의 마크업이 필요합니다.

## 5. 비활성화된 입력 필드에 회색 배경을 적용하려면 어떤 선택자를 사용해야 하나요?

A) `input:inactive`

B) `input:disabled`

C) `input:off`

D) `input[disabled]`

**정답: B) `input:disabled` (참고: D도 정답이지만 B가 더 정확합니다)**

**해설:** 비활성화된 입력 필드를 선택하는 가장 적합한 방법은 `:disabled` 의사 클래스를 사용하는 것입니다. 이는 `disabled` 속성이 있는 모든 폼 요소를 선택합니다. `input[disabled]`도 기술적으로 동일한 요소를 선택하지만, `:disabled`는 의사 클래스로서 요소의 상태를 더 명확하게 표현하므로 시맨틱적으로 더 적절합니다. `:inactive`와 `:off`는 CSS에 존재하지 않는 선택자입니다.

## 6. 마지막 단락을 제외한 모든 단락에 여백을 적용하려면 어떤 선택자를 사용해야 하나요?

A) `p:not(p:last-child)`

B) `p:not(:last)`

C) `p:not(:last-child)`

D) `p:not(:last-of-type)`

**정답: C) `p:not(:last-child)`**

**해설:** 부정 선택자 `:not()`을 사용하면 특정 조건을 만족하지 않는 요소를 선택할 수 있습니다. `p:not(:last-child)`는 "부모의 마지막 자식이 아닌 모든 p 요소"를 선택합니다. 마지막 단락을 제외한 모든 단락에 여백을 적용하려면 이 선택자가 적합합니다. `p:not(:last-of-type)`도 비슷한 결과를 얻을 수 있지만, p 요소 뒤에 다른 요소가 있는 경우 다른 결과를 보일 수 있습니다. `:last`는 유효한 의사 클래스가 아닙니다.

## 7. 다음 중 요소의 내용 앞에 특수 기호를 추가하는 올바른 방법은?

A) `p:before { content: "※ "; }`

B) `p::before { content: "※ "; }`

C) `p:start { content: "※ "; }`

D) `p::start { content: "※ "; }`

**정답: B) `p::before { content: "※ "; }`**

**해설:** 요소의 내용 앞에 콘텐츠를 추가하려면 `::before` 의사 요소와 함께 `content` 속성을 사용해야 합니다. CSS3에서는 의사 요소에 이중 콜론(`::`)을 사용하는 것이 권장되지만, 하위 호환성을 위해 단일 콜론(`:`)도 여전히 작동합니다. 따라서 `p:before`도 작동하긴 하지만, 최신 표준은 `p::before`입니다. `:start`와 `::start`는 CSS에 존재하지 않는 선택자입니다.

## 8. 다음 중 사용자가 텍스트를 드래그해서 선택했을 때의 스타일을 변경하는 선택자는?

A) `::selected`

B) `::highlight`

C) `::selection`

D) `::choose`

**정답: C) `::selection`**

**해설:** `::selection` 의사 요소는 사용자가 드래그하여 선택한 텍스트 부분에 스타일을 적용합니다. 주로 선택된 텍스트의 배경색과 텍스트 색상을 변경하는 데 사용됩니다.

```css
::selection {
  background-color: lightblue;
  color: navy;
}

```

이렇게 하면 사용자가 페이지의 텍스트를 선택할 때 연한 파란색 배경에 짙은 파란색 텍스트로 표시됩니다. 나머지 선택지들은 CSS에 존재하지 않는 선택자입니다.

## 9. 목록에서 3의 배수 위치에 있는 항목에만 특별한 스타일을 적용하려면?

A) `li:every(3)`

B) `li:nth-child(3)`

C) `li:nth-child(3n)`

D) `li:multiple(3)`

**정답: C) `li:nth-child(3n)`**

**해설:** `:nth-child(3n)`은 3의 배수 위치(3, 6, 9, ...)에 있는 모든 자식 요소를 선택합니다. 여기서 `n`은 0부터 시작하는 정수입니다. 따라서 `li:nth-child(3n)`은 리스트에서 3번째, 6번째, 9번째 항목 등을 선택합니다. `:nth-child(3)`는 오직 3번째 위치의 요소만 선택하고, `:every(3)`와 `:multiple(3)`은 CSS에 존재하지 않는 선택자입니다.

## 10. 방문한 링크와 방문하지 않은 링크에 다른 스타일을 적용하려면 어떤 선택자를 사용해야 하나요?

A) `a:new` 및 `a:old`

B) `a:visited` 및 `a:unvisited`

C) `a:link` 및 `a:visited`

D) `a:fresh` 및 `a:used`

**정답: C) `a:link` 및 `a:visited`**

**해설:** 방문 상태에 따라 링크 스타일을 다르게 적용하려면:

- `:link` - 아직 방문하지 않은 링크에 적용
- `:visited` - 이미 방문한 링크에 적용

```css
a:link {
  color: blue;
}
a:visited {
  color: purple;
}

```

이 두 의사 클래스는 사용자의 브라우징 이력에 따라 링크 스타일을 자동으로 변경합니다. 참고로 개인정보 보호를 위해 `:visited` 선택자에 적용할 수 있는 CSS 속성은 제한되어 있습니다(주로 색상 관련 속성만 허용). 나머지 선택지들은 CSS에 존재하지 않는 선택자입니다.

# CSS 의사 클래스 및 선택자 연습문제

## 연습문제 1: 구조 선택자를 활용한 테이블 스타일링

**문제**:
아래 HTML 테이블에 구조 선택자(`:first-child`, `:last-child`, `:nth-child()` 등)를 사용하여 다음 요구사항을 만족하는 CSS 코드를 작성하세요:

1. 테이블의 첫 번째 행은 배경색을 다르게 하고 글자를 굵게 표시하세요.
2. 테이블의 짝수 행에는 밝은 회색 배경색을 적용하세요.
3. 테이블의 마지막 행은 테두리 하단에 굵은 선을 추가하세요.
4. 각 행의 첫 번째 열은 글자색을 진한 파란색으로 설정하세요.
5. 각 행의 마지막 열은 오른쪽 정렬하세요.

HTML 코드:

```html
<table class="data-table">
  <tr>
    <td>이름</td>
    <td>나이</td>
    <td>직업</td>
    <td>점수</td>
  </tr>
  <tr>
    <td>홍길동</td>
    <td>25</td>
    <td>개발자</td>
    <td>85</td>
  </tr>
  <tr>
    <td>김영희</td>
    <td>28</td>
    <td>디자이너</td>
    <td>92</td>
  </tr>
  <tr>
    <td>박철수</td>
    <td>32</td>
    <td>마케터</td>
    <td>78</td>
  </tr>
  <tr>
    <td>이지은</td>
    <td>22</td>
    <td>학생</td>
    <td>95</td>
  </tr>
</table>

```

**정답**:

```css
/* 기본 테이블 스타일 */
.data-table {
  width: 100%;
  border-collapse: collapse;
  font-family: Arial, sans-serif;
}

.data-table td {
  padding: 10px;
  border: 1px solid #ddd;
}

/* 1. 첫 번째 행 스타일 */
.data-table tr:first-child {
  background-color: #4CAF50;
  color: white;
  font-weight: bold;
}

/* 2. 짝수 행 스타일 */
.data-table tr:nth-child(even) {
  background-color: #f2f2f2;
}

/* 3. 마지막 행 스타일 */
.data-table tr:last-child {
  border-bottom: 3px solid #333;
}

/* 4. 각 행의 첫 번째 열 스타일 */
.data-table td:first-child {
  color: #003366;
}

/* 5. 각 행의 마지막 열 스타일 */
.data-table td:last-child {
  text-align: right;
}

```

**해설**:
이 문제는 구조 선택자를 활용하여 테이블의 특정 부분에 다양한 스타일을 적용하는 방법을 연습합니다.

1. **첫 번째 행 선택**: `tr:first-child` 선택자는 테이블의 첫 번째 행을 선택합니다. 여기에 배경색과 글자색, 굵은 글씨 스타일을 적용했습니다.
2. **짝수 행 선택**: `tr:nth-child(even)` 선택자는 2번, 4번, 6번... 등 짝수 위치의 행을 선택합니다. 이 행들에 밝은 회색 배경색을 적용했습니다.
3. **마지막 행 선택**: `tr:last-child` 선택자는 테이블의 마지막 행을 선택합니다. 이 행에 굵은 하단 테두리를 적용했습니다.
4. **각 행의 첫 번째 열 선택**: `td:first-child` 선택자는 각 행에서 첫 번째 셀을 선택합니다. 이 셀들에 진한 파란색 글자색을 적용했습니다.
5. **각 행의 마지막 열 선택**: `td:last-child` 선택자는 각 행에서 마지막 셀을 선택합니다. 이 셀들에 오른쪽 정렬을 적용했습니다.

이렇게 구조 선택자를 사용하면 HTML 구조를 변경하지 않고도 테이블의 특정 위치에 있는 요소들에 다양한 스타일을 효과적으로 적용할 수 있습니다.

## 연습문제 2: 폼 요소의 상태 선택자 활용하기

**문제**:
다음 HTML 폼에 상태 선택자(`:focus`, `:checked`, `:disabled` 등)를 사용하여 아래 요구사항을 만족하는 CSS 코드를 작성하세요:

1. 입력 필드에 포커스되면 밝은 파란색 테두리와 약한 그림자 효과를 추가하세요.
2. 체크된 체크박스 옆의 레이블 텍스트를 진한 녹색으로 변경하세요.
3. 선택된 라디오 버튼 옆의 레이블에 밑줄을 추가하세요.
4. 비활성화된 입력 필드에 회색 배경과 기울임꼴을 적용하세요.
5. 필수 입력 필드(required 속성이 있는)의 레이블 뒤에 빨간색 별표(*)를 추가하세요.

HTML 코드:

```html
<form class="signup-form">
  <div class="form-group">
    <label for="username">사용자 이름</label>
    <input type="text" id="username" required>
  </div>

  <div class="form-group">
    <label for="email">이메일</label>
    <input type="email" id="email" required>
  </div>

  <div class="form-group">
    <label for="bio">자기소개</label>
    <textarea id="bio"></textarea>
  </div>

  <div class="form-group">
    <label for="location">지역</label>
    <input type="text" id="location" disabled value="자동 설정됨">
  </div>

  <div class="form-group">
    <label>관심사:</label>
    <div class="checkbox-group">
      <input type="checkbox" id="interest-tech">
      <label for="interest-tech">기술</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="interest-design">
      <label for="interest-design">디자인</label>
    </div>
    <div class="checkbox-group">
      <input type="checkbox" id="interest-business">
      <label for="interest-business">비즈니스</label>
    </div>
  </div>

  <div class="form-group">
    <label>경험 수준:</label>
    <div class="radio-group">
      <input type="radio" name="experience" id="beginner">
      <label for="beginner">입문자</label>
    </div>
    <div class="radio-group">
      <input type="radio" name="experience" id="intermediate">
      <label for="intermediate">중급자</label>
    </div>
    <div class="radio-group">
      <input type="radio" name="experience" id="expert">
      <label for="expert">전문가</label>
    </div>
  </div>

  <button type="submit">가입하기</button>
</form>

```

**정답**:

```css
/* 기본 폼 스타일 */
.signup-form {
  max-width: 500px;
  margin: 0 auto;
  font-family: Arial, sans-serif;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input[type="text"],
input[type="email"],
textarea {
  width: 100%;
  padding: 8px;
  border: 1px solid #ddd;
  border-radius: 4px;
  box-sizing: border-box;
}

/* 1. 포커스된 입력 필드 스타일 */
input:focus,
textarea:focus {
  border-color: #4dabf7;
  box-shadow: 0 0 5px rgba(77, 171, 247, 0.5);
  outline: none;
}

/* 2. 체크된 체크박스 옆 레이블 스타일 */
input[type="checkbox"]:checked + label {
  color: #2e7d32;
  font-weight: bold;
}

/* 3. 선택된 라디오 버튼 옆 레이블 스타일 */
input[type="radio"]:checked + label {
  text-decoration: underline;
}

/* 4. 비활성화된 입력 필드 스타일 */
input:disabled {
  background-color: #f5f5f5;
  font-style: italic;
  cursor: not-allowed;
}

/* 5. 필수 입력 필드의 레이블에 별표 추가 */
input:required + label::after,
label + input:required::after {
  content: " *";
  color: #e53935;
}

/* 필수 필드 - 구조 수정 */
.form-group label:has(+ input:required)::after {
  content: " *";
  color: #e53935;
}

/* 체크박스와 라디오 버튼 그룹 스타일 */
.checkbox-group,
.radio-group {
  display: flex;
  align-items: center;
  margin: 5px 0;
}

.checkbox-group label,
.radio-group label {
  margin: 0 0 0 5px;
  display: inline;
}

button {
  padding: 10px 15px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

```

**해설**:
이 문제는 폼 요소의 다양한 상태에 따라 스타일을 적용하는 방법을 연습합니다.

1. **포커스된 입력 필드 선택**: `input:focus`, `textarea:focus` 선택자는 사용자가 클릭하거나 탭으로 선택한 입력 필드를 선택합니다. 이러한 필드에 파란색 테두리와 그림자 효과를 적용했으며, 기본 브라우저 아웃라인을 제거했습니다.
2. **체크된 체크박스 옆 레이블 선택**: `input[type="checkbox"]:checked + label` 선택자는 체크된 체크박스의 바로 다음에 오는 레이블을 선택합니다. 이 레이블에 녹색 텍스트와 굵은 글씨를 적용했습니다.
3. **선택된 라디오 버튼 옆 레이블 선택**: `input[type="radio"]:checked + label` 선택자는 선택된 라디오 버튼의 바로 다음에 오는 레이블을 선택합니다. 이 레이블에 밑줄을 추가했습니다.
4. **비활성화된 입력 필드 선택**: `input:disabled` 선택자는 disabled 속성이 있는 입력 필드를 선택합니다. 이러한 필드에 회색 배경과 기울임꼴을 적용했으며, 커서를 'not-allowed'로 변경했습니다.
5. **필수 입력 필드의 레이블 선택**: 여기서는 두 가지 방법을 제시했습니다.
    - `input:required + label::after`는 필수 입력 필드 다음에 오는 레이블의 끝에 별표를 추가합니다.
    - `.form-group label:has(+ input:required)::after`는 필수 입력 필드 이전에 오는 레이블의 끝에 별표를 추가합니다. (참고: `:has()` 선택자는 최신 브라우저에서만 지원됩니다)

이렇게 상태 선택자를 사용하면 폼 요소의 다양한 상태에 따라 직관적인 시각적 피드백을 제공할 수 있어, 사용자 경험을 크게 향상시킬 수 있습니다.

## 연습문제 3: 문자 선택자(의사 요소) 활용하기

**문제**:
아래 HTML 블로그 포스트에 문자 선택자(`::first-letter`, `::first-line`, `::before`, `::after` 등)를 사용하여 다음 요구사항을 만족하는 CSS 코드를 작성하세요:

1. 포스트 제목의 첫 글자는 크기를 크게 하고, 다른 색상으로 설정하세요.
2. 각 단락의 첫 줄은 굵게 표시하세요.
3. 인용문 앞뒤에 큰따옴표 기호를 추가하세요.
4. '중요' 클래스가 있는 텍스트 앞에 경고 아이콘(⚠️)을 추가하세요.
5. 링크에 마우스를 올리면 밑줄이 생기게 하고, 링크 뒤에 화살표(→) 기호를 추가하세요.

HTML 코드:

```html
<article class="blog-post">
  <h1 class="post-title">CSS 의사 요소의 마법</h1>

  <p class="post-meta">
    작성자: 홍길동 | 작성일: 2023년 3월 15일
  </p>

  <p>웹 디자인에서 CSS 의사 요소는 HTML 마크업을 변경하지 않고도 콘텐츠에
  스타일과 효과를 추가할 수 있는 강력한 도구입니다. 이 글에서는 의사 요소의
  다양한 활용법을 알아봅니다.</p>

  <blockquote class="quote">
    CSS 의사 요소는 디자인의 디테일을 살리는 데 필수적인 요소입니다.
  </blockquote>

  <p class="important">의사 요소를 남용하면 유지보수가 어려워질 수 있으니
  적절히 사용하는 것이 중요합니다.</p>

  <p>더 많은 CSS 팁과 트릭은 <a href="#">CSS 마스터 가이드</a>에서 확인할 수 있습니다.</p>
</article>

```

**정답**:

```css
/* 기본 블로그 스타일 */
.blog-post {
  max-width: 800px;
  margin: 0 auto;
  font-family: 'Georgia', serif;
  line-height: 1.6;
  color: #333;
}

.post-title {
  color: #2c3e50;
  margin-bottom: 5px;
}

.post-meta {
  color: #7f8c8d;
  font-size: 0.9em;
  margin-bottom: 20px;
}

/* 1. 제목 첫 글자 스타일링 */
.post-title::first-letter {
  font-size: 2em;
  color: #e74c3c;
  float: left;
  padding-right: 5px;
  line-height: 0.8;
}

/* 2. 단락 첫 줄 굵게 표시 */
.blog-post p::first-line {
  font-weight: bold;
}

/* 3. 인용문 앞뒤에 따옴표 기호 추가 */
.quote::before {
  content: '"';
  font-size: 2em;
  color: #7f8c8d;
  line-height: 0;
  position: relative;
  top: 0.5em;
}

.quote::after {
  content: '"';
  font-size: 2em;
  color: #7f8c8d;
  line-height: 0;
  position: relative;
  top: 0.5em;
}

/* 4. 중요 클래스에 경고 아이콘 추가 */
.important::before {
  content: '⚠️ ';
}

/* 5. 링크에 화살표 추가 및 호버 효과 */
a {
  color: #3498db;
  text-decoration: none;
  transition: all 0.3s ease;
}

a::after {
  content: ' →';
  opacity: 0;
  transition: opacity 0.3s ease;
}

a:hover {
  text-decoration: underline;
}

a:hover::after {
  opacity: 1;
}

/* 추가 스타일 */
blockquote {
  border-left: 4px solid #ecf0f1;
  padding-left: 15px;
  margin: 20px 0;
  font-style: italic;
}

```

**해설**:
이 문제는 CSS 의사 요소를 활용하여 HTML 마크업을 수정하지 않고도 추가적인 스타일과 콘텐츠를 적용하는 방법을 연습합니다.

1. **제목 첫 글자 선택**: `.post-title::first-letter` 선택자는 제목의 첫 번째 문자를 선택합니다. 이 문자에 더 큰 글꼴 크기와 다른 색상을 적용했으며, `float: left`를 사용하여 드롭캡(dropcap) 효과를 만들었습니다.
2. **단락 첫 줄 선택**: `.blog-post p::first-line` 선택자는 각 단락의 첫 번째 줄을 선택합니다. 이 줄에 굵은 글씨체를 적용했습니다. 화면 크기에 따라 첫 번째 줄로 간주되는 텍스트가 달라질 수 있습니다.
3. **인용문 앞뒤에 따옴표 추가**: `.quote::before`와 `.quote::after` 선택자를 사용하여 인용문 앞뒤에 큰따옴표 기호를 추가했습니다. `content` 속성을 사용하여 실제 텍스트를 삽입했으며, 위치 조정을 위해 `position`과 `top` 속성을 사용했습니다.
4. **중요 텍스트 앞에 경고 아이콘 추가**: `.important::before` 선택자를 사용하여 중요 클래스가 있는 텍스트 앞에 경고 아이콘(⚠️)을 추가했습니다.
5. **링크에 화살표 추가 및 호버 효과**:
    - `a::after`를 사용하여 모든 링크 뒤에 화살표를 추가했지만, 기본적으로는 투명하게 설정했습니다.
    - `a:hover`를 사용하여 마우스를 올렸을 때 밑줄이 생기도록 했습니다.
    - `a:hover::after`를 사용하여 마우스를 올렸을 때만 화살표가 보이도록 불투명도를 변경했습니다.

이처럼 의사 요소는 HTML 구조를 변경하지 않고도 시각적으로 풍부한 콘텐츠를 제공할 수 있게 해주는 강력한 도구입니다.
# CSS3 선택자 기본 part2

Date: 2025년 3월 1일
페이지: P.133~P.152
완료: Yes

# CSS 의사 클래스 및 선택자 종류

CSS에서는 특정 상태나 구조의 요소를 선택하기 위해 여러 가지 의사 클래스(pseudo-class)와 의사 요소(pseudo-element)를 사용합니다. 아래는 주요 분류와 각 항목에 대한 설명입니다.

---

## 1. 상태 선택자 (State Pseudo-classes)

- **`:checked`**
    - **설명:** 체크박스나 라디오 버튼 등에서 체크 상태인 input 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        input:checked {
          background-color: lightblue;
        }
        
        ```
        
- **`:focus`**
    - **설명:** 키보드나 마우스로 포커스(활성 상태)가 맞춰진 input 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        input:focus {
          border-color: blue;
        }
        
        ```
        
- **`:enabled`**
    - **설명:** 사용 가능한(활성화된) input 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        input:enabled {
          background-color: #fff;
        }
        
        ```
        
- **`:disabled`**
    - **설명:** 사용 불가능한(비활성화된) input 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        input:disabled {
          background-color: #ddd;
        }
        
        ```
        

---

## 2. 구조 선택자 (Structural Pseudo-classes)

- **`:first-child`**
    - **설명:** 부모 요소 내에서 첫 번째 자식 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        p:first-child {
          font-weight: bold;
        }
        
        ```
        
- **`:last-child`**
    - **설명:** 부모 요소 내에서 마지막 자식 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        p:last-child {
          color: red;
        }
        
        ```
        
- **`:nth-child(n)`**
    - **설명:** 부모 요소 내에서 앞에서부터 n번째 자식 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        li:nth-child(3) {
          background-color: yellow;
        }
        
        ```
        
- **`:nth-last-child(n)`**
    - **설명:** 부모 요소 내에서 뒤에서부터 n번째 자식 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        li:nth-last-child(1) {
          border: 2px solid black;
        }
        
        ```
        

---

## 3. 형태 구조 선택자 (Type-based Structural Pseudo-classes)

- **`:first-of-type`**
    - **설명:** 부모 요소 내에서 동일한 태그 유형 중 첫 번째로 등장하는 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        p:first-of-type {
          text-transform: uppercase;
        }
        
        ```
        
- **`:last-of-type`**
    - **설명:** 부모 요소 내에서 동일한 태그 유형 중 마지막으로 등장하는 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        p:last-of-type {
          font-style: italic;
        }
        
        ```
        
- **`:nth-of-type(n)`**
    - **설명:** 부모 요소 내에서 동일한 태그 유형 중 앞에서 n번째 등장하는 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        div:nth-of-type(2) {
          margin-top: 20px;
        }
        
        ```
        
- **`:nth-last-of-type(n)`**
    - **설명:** 부모 요소 내에서 동일한 태그 유형 중 뒤에서 n번째 등장하는 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        li:nth-last-of-type(2) {
          color: green;
        }
        
        ```
        

---

## 4. 문자 선택자 (Textual Pseudo-elements)

- **`:first-letter`**
    - **설명:** 요소 내에서 첫 번째 글자에 스타일을 적용합니다.
    - **사용 예시:**
        
        ```css
        p:first-letter {
          font-size: 2em;
          color: red;
        }
        
        ```
        
- **`:first-line`**
    - **설명:** 요소 내의 첫 번째 줄 전체에 스타일을 적용합니다.
    - **사용 예시:**
        
        ```css
        p:first-line {
          font-weight: bold;
        }
        
        ```
        
- **`:before`**
    - **설명:** 선택한 요소의 내용 앞에 가상의 콘텐츠를 삽입합니다.
    - **사용 예시:**
        
        ```css
        .note:before {
          content: "※ ";
          color: orange;
        }
        
        ```
        
- **`:after`**
    - **설명:** 선택한 요소의 내용 뒤에 가상의 콘텐츠를 삽입합니다.
    - **사용 예시:**
        
        ```css
        .note:after {
          content: " (참고)";
          color: gray;
        }
        
        ```
        
- **`:selection`**
    - **설명:** 사용자가 드래그로 선택한 텍스트 부분에 적용할 스타일을 지정합니다.
    - **사용 예시:**
        
        ```css
        ::selection {
          background-color: lightblue;
        }
        
        ```
        

---

## 5. 링크 선택자 (Link Pseudo-classes)

- **`:link`**
    - **설명:** 아직 방문하지 않은 링크(보통 `a` 태그의 `href` 속성이 있는 경우)에 적용됩니다.
    - **사용 예시:**
        
        ```css
        a:link {
          color: blue;
        }
        
        ```
        
- **`:visited`**
    - **설명:** 이미 방문한 링크에 적용됩니다.
    - **사용 예시:**
        
        ```css
        a:visited {
          color: purple;
        }
        
        ```
        

---

## 6. 부정 선택자 (Negation Pseudo-class)

- **`:not(선택자)`**
    - **설명:** 지정한 선택자와 일치하지 않는 모든 요소를 선택합니다.
    - **사용 예시:**
        
        ```css
        /* 클래스 active가 아닌 모든 li 요소 선택 */
        li:not(.active) {
          opacity: 0.6;
        }
        
        ```
        

---

[퀴즈와 연습문제](%E1%84%8F%E1%85%B1%E1%84%8C%E1%85%B3%E1%84%8B%E1%85%AA%20%E1%84%8B%E1%85%A7%E1%86%AB%E1%84%89%E1%85%B3%E1%86%B8%E1%84%86%E1%85%AE%E1%86%AB%E1%84%8C%E1%85%A6%201b32ad07fb2080639fddc7666ddbd4b3.md)
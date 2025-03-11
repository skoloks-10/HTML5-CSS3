# HTML5 태그 기본 part1

Date: 2025년 2월 26일
페이지: P.35~P.70
완료: Yes

## 1. 태그와 요소

- **태그**
    - HTML 문서는 시작 태그와 끝 태그로 구성됩니다.
    - 예:
        
        ```html
        <h1>시작태그</h1> <!-- 이 부분이 태그로 둘러싸인 콘텐츠 -->
        
        ```
        
- **요소**
    - 태그와 그 내부의 내용 전체를 의미하며, 일부 태그는 내부에 다른 태그를 삽입할 수 있습니다.

---

## 2. 속성

- 태그에 추가 정보를 제공하는 부분
- 예:
    
    ```html
    <h1 title="header">헤더 텍스트</h1>
    
    ```
    
    - 여기서 `title`은 속성이름, `"header"`는 속성값으로 표현됩니다.

---

## 3. 주석

- HTML 주석은 `<!--` 와 `->` 사이에 작성합니다.
- 예:
    
    ```html
    <!-- 이 부분은 주석입니다. -->
    
    ```
    
- **Emmet 단축키:**
    - 주석 추가 단축키: `ctrl + /`

---

## 4. 페이지 구조

- 기본 HTML 문서 구조 예시:
    
    ```html
    <!DOCTYPE html>
    <html lang="ko-KR">
      <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>문서 제목</title>
      </head>
      <body>
        <!-- 실제 콘텐츠가 들어갑니다. -->
      </body>
    </html>
    
    ```
    
    - **설명:**
        1. `<!DOCTYPE html>`: 현재 HTML 버전을 의미하며, 반드시 있어야 합니다.
        2. `<html lang="ko-KR">`: 문서의 언어 설정 (한국어).
        3. `<head>`: 스타일시트, 자바스크립트 등 바디에 필요한 정보를 기입합니다.
        4. `<title>`: 문서 제목
        5. `<body>`: 실제로 보이는 영역

---

## 5. 제목 태그

- 사용 태그: `<h1>` ~ `<h6>`
- **주의:**
    - 일반적으로 `<h1>`은 한 화면에 한 번만 사용합니다.
    - 숫자가 작을수록 더 중요한 제목을 나타냅니다.
    
    **예시:**
    
    ```html
    <h1>페이지 제목</h1>
    <h2>섹션 제목</h2>
    <h3>소제목</h3>
    ```
    

---

## 6. 본문 태그

- **단락 만들기:** `<p>`
- **줄바꿈:** `<br>`
- **수평줄:** `<hr>`
- **링크(앵커) 태그:** `<a>`
    - 링크 기능을 없애고 싶다면 `href="#"`를 사용

```html
<p>이것은 단락입니다.</p>
<br>
<hr>
<a href="https://example.com">Example Link</a>
```

---

## 7. 글자 태그

- **굵은 글자:** `<b>`
- **기울어진 글자:** `<i>`
- **작은 글자:** `<small>`
- **아래첨자:** `<sub>`
- **윗첨자:** `<sup>`
- **밑줄:** `<ins>`
- **취소선:** `<del>`

```html
<p>
  <b>굵은 글자</b><br>
  <i>기울어진 글자</i><br>
  <small>작은 글자</small><br>
  H<sub>2</sub>O, 10<sup>2</sup><br>
  <ins>밑줄</ins>과 <del>취소선</del>
</p>
```

---

## 8. 목록 태그

- **순서 없는 목록:** `<ul>`
- **순서 있는 목록:** `<ol>`
- **목록 항목:** `<li>`

```html
<!-- 순서 없는 목록 -->
<ul>
  <li>아이템 1</li>
  <li>아이템 2</li>
  <li>아이템 3</li>
</ul>

<!-- 순서 있는 목록 -->
<ol>
  <li>첫 번째</li>
  <li>두 번째</li>
  <li>세 번째</li>
</ol>
```

---

## 9. 정의 태그

- 정의 목록 구성:
    - `<dl>`: 정의 목록
    - `<dt>`: 정의 용어
    - `<dd>`: 정의 설명
    
    ```html
    <dl>
      <dt>HTML</dt>
      <dd>HyperText Markup Language의 약자입니다.</dd>
      <dt>CSS</dt>
      <dd>Cascading Style Sheets의 약자입니다.</dd>
    </dl>
    ```
    

---

## 10. 테이블 태그

- 기본 구조 및 속성 예시:
    
    ```html
    <table border="3">
      <tr>
        <th colspan="3">헤더</th>
      </tr>
      <tr>
        <td>내용1</td>
        <td>내용2</td>
        <td>내용3</td>
      </tr>
    </table>
    
    ```
    
    - **설명:**
        - `<tr>`: 행
        - `<th>`: 행의 제목 셀
        - `<td>`: 행의 내용 셀
        - `border`: 표 테두리 두께
        - `colspan`과 `rowspan`: 각각 셀의 가로, 세로 병합

---

## 11. 이미지 태그

- **예시:**
    
    ```html
    <img src="apple.png" alt="사과" width="300" height="150">
    
    ```
    
    - `src`: 이미지 경로
    - `alt`: 이미지가 없을 때 출력할 텍스트
    - 더미 이미지는 [dummyimage.com](https://dummyimage.com/) 등을 이용

---

## 12. 오디오 태그

- **예시:**
    
    ```html
    <audio controls>
        <source src="<https://www.w3schools.com/html/horse.mp3>" type="audio/mpeg" />
        Your browser does not support the audio element.
    </audio>
    
    ```
    
    - **속성:**
        - `src`: 음악 경로
        - `preload`: 재생 전에 미리 불러오기
        - `autoplay`: 자동 재생
        - `loop`: 반복 재생
        - `controls`: 재생 도구 출력
        - `type`: 파일 형식을 지정하여 트래픽 낭비 방지

---

## 13. Emmet 단축어

- **예시:**
    - `h1` → `<h1></h1>`
    - `h1+h2` → `<h1></h1><h2></h2>`
    - `h$*6` → `<h1></h1><h2></h2> ... <h6></h6>`
    - `h${hello}*6` → 각 제목 태그 안에 "hello" 텍스트 삽입
    - `div.one.two` → `<div class="one two"></div>`
    - `div#one.two.three` → `<div id="one" class="two three"></div>`
    
    ```html
    <!-- Emmet 단축어 예제 코드 -->
    
    <!-- 1. h1 -->
    <!-- Emmet 입력: h1 -->
    <h1></h1>
    
    <!-- 2. h1+h2 -->
    <!-- Emmet 입력: h1+h2 -->
    <h1></h1>
    <h2></h2>
    
    <!-- 3. h$*6 -->
    <!-- Emmet 입력: h$*6 -->
    <h1></h1>
    <h2></h2>
    <h3></h3>
    <h4></h4>
    <h5></h5>
    <h6></h6>
    
    <!-- 4. h${hello}*6 -->
    <!-- Emmet 입력: h${hello}*6 -->
    <h1>hello</h1>
    <h2>hello</h2>
    <h3>hello</h3>
    <h4>hello</h4>
    <h5>hello</h5>
    <h6>hello</h6>
    
    <!-- 5. div.one.two -->
    <!-- Emmet 입력: div.one.two -->
    <div class="one two"></div>
    
    <!-- 6. div#one.two.three -->
    <!-- Emmet 입력: div#one.two.three -->
    <div id="one" class="two three"></div>
    
    ```
    

---

## 14. 유용한 단축키

- **동시 편집:** `ctrl + alt + 방향키` 또는 `alt + 클릭`
- **설정:** `ctrl + ,`
- **터미널 열기:** `ctrl + \``
- **사이드바 토글:** `ctrl + b`
- **동시 편집(같은 단어 선택):** `ctrl + d`
- **주석 토글:** `ctrl + /`
- **내어쓰기:** `shift + tab`
- **커서 위치 조정:** `ctrl + ]` 또는 `ctrl +

---

[HTML5 태그 기본 part1 퀴즈와 연습문제](HTML5%20%E1%84%90%E1%85%A2%E1%84%80%E1%85%B3%20%E1%84%80%E1%85%B5%E1%84%87%E1%85%A9%E1%86%AB%20part1%20%E1%84%8F%E1%85%B1%E1%84%8C%E1%85%B3%E1%84%8B%E1%85%AA%20%E1%84%8B%E1%85%A7%E1%86%AB%E1%84%89%E1%85%B3%E1%86%B8%E1%84%86%E1%85%AE%E1%86%AB%E1%84%8C%E1%85%A6%201b32ad07fb2080e2a176e49896d82907.md)
# CSS3 스타일 속성 기본 part1

Date: 2025년 3월 4일
페이지: p.157~p.184
완료: Yes

# CSS 기본 단위 및 속성 정리

CSS에서는 다양한 단위와 속성을 사용하여 스타일을 지정합니다. 아래는 주요 항목들을 카테고리별로 정리한 내용입니다.

---

## 1. CSS3 단위

### 크기 단위

- **%**
    - **설명:** 백분율 단위로, 부모 요소의 크기에 비례하는 값을 지정
    - **예시:** `width: 50%;`
- **em**
    - **설명:** 요소의 폰트 크기를 기준으로 한 배수 단위
    - **예시:** `font-size: 1.2em;`
- **px**
    - **설명:** 픽셀 단위로, 고정된 크기를 지정
    - **예시:** `margin: 10px;`

### 색상 단위

- **Hex 코드**
    - **예시:** `#000000` (검정색)
- **RGB 색상**
    - **예시:** `rgb(255, 0, 0)` (빨강색)
- **HSLA 색상**
    - **예시:** `hsla(120, 100%, 50%, 0.5)`
        - *h*: 색조, *s*: 채도, *l*: 밝기, *a*: 투명도

### URL 단위

- **`url()`**
    - **설명:** 배경 이미지 등 외부 리소스 경로를 지정할 때 사용
    - **예시:**
        
        ```css
        background-image: url('a.jpg');
        
        ```
        

---

## 2. 가시 속성

### display 속성

- **`display: none;`**
    - **설명:** 요소를 화면에서 완전 제거 (렌더 트리에서 제외됨)
- **`display: block;`**
    - **설명:** 요소를 블록 레벨로 표시 (자체 줄바꿈 발생)
- **`display: inline;`**
    - **설명:** 요소를 인라인 레벨로 표시 (텍스트와 같은 줄에 배치됨)
- **`display: inline-block;`**
    - **설명:** 인라인 요소처럼 한 줄에 표시되면서도 블록 요소의 특성을 가짐 (너비, 높이 지정 가능)

> 비교:
> 
> - `display: none;`은 요소와 해당 공간을 모두 제거
> - `visibility: hidden;`은 요소는 보이지 않지만 공간은 유지

### visibility 속성

- **`visibility: visible;`**
    - **설명:** 요소를 보이게 함
- **`visibility: hidden;`**
    - **설명:** 요소를 보이지 않게 하지만, 요소 공간은 그대로 남김
- **`visibility: collapse;`**
    - **설명:** 주로 테이블 행이나 열을 제거할 때 사용, 요소를 완전히 없앤 효과를 준다

### opacity 속성

- **`opacity`**
    - **설명:** 요소의 투명도를 조절 (0: 완전 투명, 1: 완전 불투명)
    - **예시:** `opacity: 0.8;`

---

## 3. 박스 속성

### 박스 모델 관련 속성

- **`width`**, **`height`**
    - **설명:** 요소(예, 텍스트 박스)의 너비와 높이 지정
- **`margin`**
    - **설명:** 요소 외부 여백 설정
    - **예시:**
        
        ```css
        margin: 0 30px;  /* 위/아래: 0, 좌/우: 30px */
        
        ```
        
- **`padding`**
    - **설명:** 요소 내부 여백 설정
- **`box-sizing`**
    - **설명:** 요소의 크기를 계산하는 방식을 지정 ("content-box" 또는 "border-box")
    - **예시:**
        
        ```css
        box-sizing: border-box;
        
        ```
        

> 참고 이미지:
> 
> 
> ![images_sue6e2_post_b6d59cef-8f56-49a4-85e3-73e02888e046_box속성.png](images_sue6e2_post_b6d59cef-8f56-49a4-85e3-73e02888e046_box%EC%86%8D%EC%84%B1.png)
> 

---

## 4. 테두리 속성

- **`border-width`**
    - **설명:** 테두리 두께를 지정 (예: `1px`, `2px` 등)
- **`border-style`**
    - **설명:** 테두리의 종류 지정 (예: `solid`, `dotted`, `dashed` 등)
- **`border-color`**
    - **설명:** 테두리의 색상 지정
- **`border-radius`**
    - **설명:** 요소의 모서리를 둥글게 만드는 정도를 지정
    - **예시:**
        
        ```css
        .border-example {
          border: 3px dashed #ff5722;
          border-radius: 10px;
        }
        
        ```
        
        ---
        

---

---

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>CSS 기본 단위 및 속성 예제</title>
  <style>
    /* ==========================
       1. CSS3 단위
    ========================== */

    /* 크기 단위 예제 */
    .box {
      width: 50%;              /* 부모 너비의 50% */
      font-size: 1.5em;        /* 기본 폰트 사이즈의 1.5배 */
      padding: 20px;           /* 고정 20px 패딩 */
      border: 2px solid #333;  /* 2px 두께의 어두운 회색 테두리 */
      margin: 20px auto;       /* 상하 20px, 좌우 중앙 정렬 */
      box-sizing: border-box;  /* 패딩과 테두리를 포함한 해당 요소의 크기 계산 */
    }

    /* 색상 단위 예제 */
    .color-example {
      background-color: #ffcc00;               /* Hex 코드 사용 (노란색) */
      color: rgb(0, 100, 255);                   /* RGB 색상 (파란색 계열) */
      border: 5px solid hsla(120, 60%, 50%, 0.8); /* HSLA 사용 (약간 투명한 녹색) */
      padding: 10px;
      text-align: center;
      margin-bottom: 20px;
    }

    /* URL 단위 예제 */
    .bg-image {
      background-image: url('a.jpg');  /* 이미지 경로 지정 (a.jpg 파일 사용) */
      background-size: cover;
      height: 200px;
      width: 100%;
      margin-bottom: 20px;
    }

    /* ==========================
       2. 가시 속성 (display, visibility, opacity)
    ========================== */

    /* display 속성 예제 */
    .display-none {
      display: none;  /* 화면에서 제거: 요소와 공간이 사라짐 */
    }

    .display-block {
      display: block; /* 블록 요소로 표시 */
    }

    .display-inline {
      display: inline; /* 인라인 요소처럼 표시 */
    }

    .display-inline-block {
      display: inline-block; /* 인라인에 블록 특성: 크기 지정 가능 */
      padding: 5px;
      border: 1px solid #000;
    }

    /* visibility 속성 예제 */
    .visibility-hidden {
      visibility: hidden; /* 보이지 않지만 공간은 유지 */
    }

    .visibility-visible {
      visibility: visible; /* 기본값: 보임 */
    }

    /* opacity 속성 예제 */
    .opacity-example {
      opacity: 0.7; /* 70% 불투명, 30% 반투명 */
    }

    /* ==========================
       3. 박스 속성 (width, height, margin, padding, box-sizing)
    ========================== */

    .box-model {
      width: 300px;
      height: 150px;
      margin: 20px;
      padding: 15px;
      background-color: #e0f7fa; /* 밝은 청록색 배경 */
      /* box-sizing: content-box; 기본값; */
      box-sizing: border-box; /* 패딩과 border 포함 */
    }

    /* ==========================
       4. 테두리 속성 (border-width, border-style, border-color, border-radius)
    ========================== */

    .border-example {
      border-width: 3px;
      border-style: dashed;
      border-color: #ff5722; /* 주황/빨강 계열 */
      border-radius: 10px;
      padding: 10px;
      margin: 20px;
    }
  </style>
</head>
<body>
  <h1>CSS 기본 단위 및 속성 예제</h1>

  <!-- CSS3 단위 예제 -->
  <div class="box">
    이 박스의 너비는 부모의 50%, 폰트 크기는 1.5em, 패딩은 20px입니다.
  </div>

  <div class="color-example">
    배경색: #ffcc00, 글자색: rgb(0, 100, 255), 테두리: hsla(120, 60%, 50%, 0.8)
  </div>

  <div class="bg-image">
    <!-- background-image: url('a.jpg') 예제, 실제 파일 a.jpg가 존재하면 이미지가 배경에 반영됩니다. -->
  </div>

  <!-- 가시 속성 예제 -->
  <p class="display-inline-block">Display Inline-Block 예제</p>
  <p class="visibility-hidden">이 텍스트는 보이지 않지만 공간을 차지합니다.</p>
  <p class="opacity-example">이 텍스트는 70% 불투명합니다.</p>

  <!-- 박스 모델 예제 -->
  <div class="box-model">
    박스 모델 예제: 너비 300px, 높이 150px, margin 20px, padding 15px, box-sizing: border-box;
  </div>

  <!-- 테두리 속성 예제 -->
  <div class="border-example">
    테두리 예제: 3px dashed #ff5722, border-radius: 10px;
  </div>
</body>
</html>

```

---

### 예제코드 설명

1. **CSS3 단위:**
    - `.box` 클래스는 `%`, `em`, `px` 단위를 조합하여 부모 너비의 50%와 1.5em 폰트 크기를 적용합니다.
    - `.color-example`에서는 `#hex`, `rgb()`, `hsla()`를 사용해 배경, 글자, 테두리 색상을 지정합니다.
    - `.bg-image`에서는 `url()` 함수를 사용해 배경 이미지를 지정합니다.
2. **가시 속성:**
    - `.display-none`는 화면에서 완전히 제거되지만, 예제에서는 보이지 않는 클래스를 따로 만들었습니다.
    - `.visibility-hidden`은 요소는 공간을 유지하면서 보이지 않게 합니다.
    - `.opacity-example`는 요소의 투명도를 조절합니다.
3. **박스 속성:**
    - `.box-model` 클래스는 `width`, `height`, `margin`, `padding`, `box-sizing`을 사용하여 박스 모델을 조절합니다.
4. **테두리 속성:**
    - `.border-example`는 `border-width`, `border-style`, `border-color`, `border-radius`를 사용하여 테두리의 스타일과 곡률을 지정합니다.

[퀴즈와 연습문제](%E1%84%8F%E1%85%B1%E1%84%8C%E1%85%B3%E1%84%8B%E1%85%AA%20%E1%84%8B%E1%85%A7%E1%86%AB%E1%84%89%E1%85%B3%E1%86%B8%E1%84%86%E1%85%AE%E1%86%AB%E1%84%8C%E1%85%A6%201b32ad07fb2080c69c8ff389c3076eeb.md)
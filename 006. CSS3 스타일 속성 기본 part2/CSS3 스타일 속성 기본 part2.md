# CSS3 스타일 속성 기본 part2

Date: 2025년 3월 5일
페이지: p.185~p.218
완료: Yes

---

# CSS 속성과 단위 정리

## 1. 배경 속성 (Background Properties)

배경 속성은 요소의 배경 이미지, 색상, 위치 등을 지정하는 데 사용됩니다.

- **background-image**
    - **설명:** 배경에 넣을 그림을 지정합니다.
    - **사용 예시:**
        
        ```css
        background-image: url('background.png');
        
        ```
        
    - **추가 사항:** 여러 개의 배경 이미지를 겹쳐서 적용할 수 있습니다.
- **background-size**
    - **설명:** 배경 이미지의 너비와 높이를 지정합니다.
    - **사용 예시:**
        
        ```css
        background-size: 100% 250px;
        
        ```
        
- **background-repeat**
    - **설명:** 배경 이미지의 반복 여부를 지정합니다.
    - **사용 예시:**
        
        ```css
        background-repeat: no-repeat;
        
        ```
        
- **background-attachment**
    - **설명:** 배경 이미지가 스크롤에 따라 움직이는지 고정되는지 지정합니다.
    - **사용 예시:**
        
        ```css
        background-attachment: fixed;
        
        ```
        
    - **비교:**
        - `fixed`: 이미지가 고정되어 스크롤해도 움직이지 않음
        - `scroll`: 이미지와 함께 스크롤됨
- **background-position**
    - **설명:** 배경 이미지의 위치를 지정합니다.
    - **사용 예시:**
        
        ```css
        background-position: bottom;
        /* 또는, x와 y 좌표를 지정: */
        background-position: center top;
        
        ```
        
- **배경 속성 종합 예제:**
    
    ```css
    background-image: url('background.png');
    background-position: bottom;
    background-size: 100%;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-color: #e7e7e8;
    
    ```
    

---

## 2. 폰트 속성 (Font Properties)

폰트 속성은 텍스트의 크기, 서체, 스타일 및 정렬 등을 지정합니다.

- **font-size**
    - **설명:** 글자 크기를 지정합니다. (예: `32px`, `1.5em` 등)
    - **예시:**
        
        ```css
        .a { font-size: 32px; }
        
        ```
        
- **font-family**
    - **설명:** 사용할 폰트를 지정하며, 폰트가 없는 경우를 대비해 여러 폰트를 나열할 수 있습니다.
    - **예시:**
        
        ```css
        .font_roman {
          font-family: "Times New Roman", Arial, sans-serif, serif, "Mono Space";
        }
        
        ```
        
    - **참고:** 다국어의 경우 가장 기본이 되는 폰트가 마지막에 위치하는 것이 좋습니다.
- **font-style** & **font-weight**
    - **설명:** 폰트의 기울기(italic)와 두께(bold)를 조정합니다.
    - **예시:**
        
        ```css
        .example {
          font-style: italic;
          font-weight: bold;
        }
        
        ```
        
- **line-height**
    - **설명:** 글자 줄 간의 간격을 설정하며, 보통 텍스트의 높이와 동일한 값을 주어 수직 중앙 정렬 효과를 줍니다.
    - **예시:**
        
        ```css
        .text {
          line-height: 70px;
        }
        
        ```
        
- **text-align**
    - **설명:** 텍스트의 정렬을 지정합니다.
    - **예시:**
        
        ```css
        .align-right {
          text-align: right;
        }
        
        ```
        
- **text-decoration**
    - **설명:** 링크 등의 텍스트 장식을 지정하며, 밑줄 등 기본 스타일을 제거할 때 사용합니다.
    - **예시:**
        
        ```css
        a {
          text-decoration: none;
        }
        
        ```
        

---

## 3. 위치 속성 (Position Properties)

CSS 위치 속성은 요소의 배치 방식을 지정합니다. 절대 위치, 상대 위치, 고정 위치 등으로 구분됩니다.

- **position**
    - **설명:** 요소의 위치 설정 방식을 변경합니다.
    - **주요 값:**
        - `static`: 기본 값, 요소가 위에서 아래로 자연스럽게 배치됨
        - `relative`: 기본 위치에서 상대적으로 이동
        - `absolute`: 부모 요소를 기준으로 절대 위치 지정 (부모 요소에 `position: relative;`가 필요)
        - `fixed`: 브라우저 뷰포트를 기준으로 위치 지정
    - **예시:**
        
        ```css
        .example {
          position: absolute;
          left: 20px;
          top: 30px;
        }
        
        ```
        
- **z-index**
    - **설명:** 요소의 쌓임 순서를 지정합니다. 숫자가 클수록 앞으로 나타납니다.
    - **예시:**
        
        ```css
        .overlay {
          z-index: 10;
        }
        
        ```
        
- **overflow**
    - **설명:** 내부 요소가 부모 요소의 영역을 초과할 때 처리 방법을 지정합니다.
    - **주요 값:**
        - `hidden`: 초과된 부분을 숨김
        - `scroll`: 스크롤바를 추가하여 보이게 함
    - **예시:**
        
        ```css
        .container {
          overflow: hidden;
        }
        
        ```
        

> 위치 속성 관련 공식:
> 
> - `position: absolute;`를 사용할 때, 부모 요소에 `position: relative;` 및 적절한 `height`를 설정하여 자식 요소가 올바른 위치에 배치되도록 합니다.

### 위치 속성 예제 코드

```html
<!DOCTYPE html>
<html lang="ko-KR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>CSS3 Property Basic</title>
  <style>
    .box {
      width: 100px;
      height: 100px;
      position: absolute;
    }
    .red {
      background-color: red;
      left: 10px;
      top: 10px;
      z-index: 100;
    }
    .green {
      background-color: green;
      left: 50px;
      top: 50px;
      z-index: 10;
    }
    .blue {
      background-color: blue;
      left: 90px;
      top: 90px;
      z-index: 1;
    }

    body > div {
      width: 400px;
      height: 100px;
      border: 3px solid black;
      position: relative;
      overflow: scroll;
    }
  </style>
</head>
<body>
  <h1>Lorem, ipsum dolor sit amet</h1>
  <div>
    <div class="box red"></div>
    <div class="box green"></div>
    <div class="box blue"></div>
  </div>
  <h1>Lorem ipsum dolor sit, amet</h1>
</body>
</html>

```

---

---

[CSS3 스타일 속성 기본 part2 퀴즈와 연습문제](https://linen-artichoke-b37.notion.site/CSS3-part2-1ad2ad07fb2080de949ced1e04a2285c?pvs=4)
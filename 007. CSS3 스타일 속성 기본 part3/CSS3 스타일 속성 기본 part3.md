# CSS3 스타일 속성 기본 part3

Date: 2025년 3월 6일
페이지: p.219~p.243
완료: Yes

---

# CSS 레이아웃 및 스타일 속성 정리

## 1. Float 속성

- **설명:**
    - Float 속성은 웹 페이지 레이아웃을 구성할 때 많이 사용되며, 요소들을 수평으로 정리하는 데 유용합니다.
    - `float: left` 또는 `float: right`를 사용하여 요소가 좌측 또는 우측으로 띄워지며, 페이지 내 요소들의 순서대로 해당 방향으로 정렬됩니다.
    - 자손 요소에 float 속성을 적용할 경우, 부모 요소에 `overflow: hidden;`을 지정하면 float 요소의 높이가 부모에 반영됩니다. 이러한 방법은 One True Layout 방식을 채택한 예시입니다.
- **예제 코드 및 설명:**
    
    ```html
    <!DOCTYPE html>
    <html lang="ko-KR">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Float Style Property</title>
      <style>
        body {
          width: 960px;
          margin: 0 auto;
        }
        /* 부모 요소에 overflow를 hidden으로 지정해 float 영역을 감싸기 */
        #wrap {
          overflow: hidden;
        }
    
        #aside {
          width: 200px;
          float: left;
        }
        #section {
          width: 760px;
          float: left;
        }
      </style>
    </head>
    <body>
      <div id="header"><h1>Header</h1></div>
      <div id="navigation"><h1>Navigation</h1></div>
      <div id="wrap">
        <div id="aside">
          <h1>Aside</h1>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste sequi aspernatur temporibus illum labore harum dolores explicabo odit, voluptates, atque dicta ipsam tenetur reiciendis suscipit at nihil debitis quidem! Corporis.</p>
        </div>
        <div id="section">
          <h1>Section</h1>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ducimus vitae illum nulla in eligendi voluptas tenetur et? Ipsam eveniet possimus asperiores hic, ex, voluptas molestias commodi fugit cupiditate, facilis excepturi!</p>
        </div>
      </div>
      <div id="footer">
        <h1>Footer</h1>
      </div>
    </body>
    </html>
    
    ```
    

---

## 2. clear: both를 사용한 레이아웃

- **설명:**
    - Float을 이용한 레이아웃은 float를 적용한 요소 다음에 clear 속성을 추가하여 레이아웃을 끝맺음 처리할 수 있습니다.
    - 보통 float 적용 대상들의 뒤에만 clear: both;를 사용합니다.
- **예제 코드 및 설명:**
    
    ```html
    <!DOCTYPE html>
    <html lang="ko-KR">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Float Layout with Clear</title>
      <style>
        body {
          width: 960px;
          margin: 0 auto;
        }
    
        #aside {
          width: 260px;
          float: left;
        }
        #section {
          width: 700px;
          float: right;
        }
        .clear {
          clear: both;
        }
      </style>
    </head>
    <body>
      <div id="header"><h1>Header</h1></div>
      <div id="navigation"><h1>Navigation</h1></div>
      <div id="aside">
        <h1>Aside</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste sequi aspernatur temporibus illum labore harum dolores explicabo odit, voluptates, atque dicta ipsam tenetur reiciendis suscipit at nihil debitis quidem! Corporis.</p>
      </div>
      <div id="section">
        <h1>Section</h1>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ducimus vitae illum nulla in eligendi voluptas tenetur et? Ipsam eveniet possimus asperiores hic, ex, voluptas molestias commodi fugit cupiditate, facilis excepturi!</p>
      </div>
      <div class="clear"></div>
      <div id="footer">
        <h1>Footer</h1>
      </div>
    </body>
    </html>
    
    ```
    

---

## 3. 그림자 속성 (Shadow Properties)

- **설명:**
    - `text-shadow`는 텍스트에 그림자 효과를 주며,
    - `box-shadow`는 박스 요소에 그림자를 적용합니다.
    - 그림자 속성은 오른쪽, 아래로의 오프셋, 흐림 정도, 색상을 순서대로 지정합니다.
- **예제 코드 및 설명:**
    
    ```html
    <!DOCTYPE html>
    <html lang="ko-KR">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Shadow Properties Example</title>
      <style>
        div {
          border: 3px solid black;
          box-shadow: 10px 10px 10px black;
          text-shadow: 10px 10px 10px black;
        }
      </style>
    </head>
    <body>
      <div>
        <h1>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam modi non ut at dignissimos pariatur a dicta dolorem similique dolor, facilis ullam illo, tempore culpa nobis ipsam quia nostrum delectus?</h1>
      </div>
    </body>
    </html>
    
    ```
    
- **참고:**
    - 각 속성의 값은 오프셋 x, 오프셋 y, 블러 정도, 색상 순으로 지정됩니다.
    - 그림자 효과를 생성하기 위해 [CSS3 Generator](https://css3generator.com/)와 같은 툴을 사용하면 편리합니다.

---

## 4. 그레디언트 (Gradient)

- **설명:**
    - 그레디언트는 두 가지 이상의 색상을 혼합하여 배경을 채색하는 기능입니다.
    - CSS3에서는 linear-gradient 또는 radial-gradient를 사용합니다.
    - [ColorZilla Gradient Editor](https://www.colorzilla.com/ko/gradient-editor/)와 같은 툴을 사용하여 쉽게 생성할 수 있습니다.
- **예제 코드 및 설명:**
    
    ```html
    <!DOCTYPE html>
    <html lang="ko-KR">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>Gradient Background Example</title>
      <style>
        div {
          background: linear-gradient(to bottom,  #1e5799 0%, #2989d8 50%, #207cca 51%, #7db9e8 100%);
        }
      </style>
    </head>
    <body>
      <div>
        <h1>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam modi non ut at dignissimos pariatur a dicta dolorem similique dolor, facilis ullam illo, tempore culpa nobis ipsam quia nostrum delectus?</h1>
      </div>
    </body>
    </html>
    
    ```
    

---

## 5. 벤더 프리픽스 (Vendor Prefixes)

- **설명:**
    - 벤더 프리픽스는 -moz, -webkit 등과 같이 특정 브라우저 공급업체에서 CSS 실험적 기능을 사용할 때 붙이는 접두사입니다.
    - 예를 들면, `webkit-border-radius`는 WebKit 기반 브라우저에서 border-radius 속성이 정상적으로 작동하도록 도와줍니다.
    - 최신 브라우저에서는 점차 표준 속성만 사용되지만, 구형 브라우저 지원을 위해 때때로 필요합니다.
- **예제 코드 (간단 예):**
    
    ```css
    .rounded-box {
      -webkit-border-radius: 10px;
         -moz-border-radius: 10px;
              border-radius: 10px;
    }
    
    ```
    

---

[퀴즈와 연습문제](%E1%84%8F%E1%85%B1%E1%84%8C%E1%85%B3%E1%84%8B%E1%85%AA%20%E1%84%8B%E1%85%A7%E1%86%AB%E1%84%89%E1%85%B3%E1%86%B8%E1%84%86%E1%85%AE%E1%86%AB%E1%84%8C%E1%85%A6%201b32ad07fb2080eab32ad60543c1b5d8.md)
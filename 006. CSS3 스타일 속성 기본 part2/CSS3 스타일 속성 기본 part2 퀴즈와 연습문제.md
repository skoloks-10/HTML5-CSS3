# CSS3 스타일 속성 기본 part2 퀴즈와 연습문제

---

## 연습문제 1: 배경 속성 활용

**문제:**

다음 CSS 코드를 보고, 각 속성이 어떤 역할을 하는지 설명하시오.

```css
.background-demo {
  background-image: url('background.png');
  background-position: bottom;
  background-size: 100%;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-color: #e7e7e8;
}

```

**예상 정답:**

- **background-image:** `'background.png'` 파일을 요소의 배경 이미지로 지정
- **background-position:** 배경 이미지를 요소의 아래쪽(바닥)에 위치시킴
- **background-size:** 배경 이미지의 너비를 100%로, 높이는 자동으로 계산(또는 필요에 맞게 적용)
- **background-repeat:** 배경 이미지가 반복되지 않고 한 번만 표시됨
- **background-attachment:** 배경 이미지가 스크롤 시 고정되어 움직이지 않음
- **background-color:** 배경 이미지가 없거나 투명한 부분에 #e7e7e8 색상을 적용

**해설:**

이 코드는 요소의 배경에 이미지와 색상을 함께 지정합니다.

- 배경 이미지를 지정하고, 반복 없이 전체 너비에 맞게 표시합니다.
- background-attachment: fixed 속성으로 이미지가 스크롤 시에도 고정되어, 마치 창 배경처럼 동작합니다.
- 마지막으로 background-color는 이미지가 로드되지 않거나 투명할 때 대체 색상을 제공합니다.

---

## 연습문제 2: 폰트 속성 적용

**문제:**

다음 CSS 코드를 해석하고, 왜 폰트 패밀리를 여러 개 지정하는지 설명하시오.

```css
.font_roman {
  font-family: "Times New Roman", Arial, sans-serif, serif, "Mono Space";
  font-size: 32px;
}

```

**예상 정답:**

- **font-family:** 이 코드에서는 우선 "Times New Roman"을 사용하고, 해당 폰트가 없을 때 Arial, 그 다음 sans-serif, serif, "Mono Space" 순으로 폰트를 대체해서 사용하도록 지정되어 있습니다.
- **font-size:** 텍스트의 크기를 32픽셀로 설정합니다.

**해설:**

폰트 패밀리는 사용자의 시스템에 해당 폰트가 설치되어 있지 않을 경우 대비하여 여러 폰트를 순서대로 나열합니다.

- 가장 선호하는 폰트를 첫 번째에 두고, 그 이후 없을 때 사용할 대체 폰트들을 지정합니다.
- 이는 다국어 지원이나 시스템 환경 차이로 인한 폰트 렌더링 차이를 최소화하는 데 유용합니다.

---

## 연습문제 3: 위치 속성과 z-index

**문제:**

다음 코드를 참고하여, `position`과 `z-index`의 역할을 설명하고, 절대 위치(absolute)를 사용할 때 부모 요소에 어떤 설정이 필요한지 서술하시오.

```css
.box {
  width: 100px;
  height: 100px;
  position: absolute;
}
.red {
  background-color: red;
  left: 10px; top: 10px;
  z-index: 100;
}
.green {
  background-color: green;
  left: 50px; top: 50px;
  z-index: 10;
}
.blue {
  background-color: blue;
  left: 90px; top: 90px;
  z-index: 1;
}

```

**예상 정답:**

- **position: absolute;**
    - 요소를 문서 흐름에서 제거하고, 가장 가까운 위치 지정(parent) 요소(예를 들어 `position: relative`가 설정된 부모 요소)를 기준으로 위치를 절대 좌표로 지정합니다.
- **z-index:**
    - 같은 위치에 겹치는 요소들의 쌓임 순서를 결정하며, 숫자가 클수록 앞쪽에 표시됩니다.
- **부모 요소 설정:**
    - 자식 요소가 `position: absolute;`로 배치되려면, 부모 요소에 `position: relative;`(또는 absolute, fixed)를 설정하여 기준 위치를 제공해 주는 것이 좋습니다.

**해설:**

절대 위치를 사용하면 요소는 일반적인 문서 흐름에서 제외되어 다른 요소와 겹칠 수 있습니다.

- z-index를 사용하여 겹칠 때 어느 요소가 앞에 표시될지를 결정할 수 있으며,
- 부모 요소에 `position: relative;`를 지정하면 자식 요소의 절대 위치 기준점이 부모 요소가 됩니다.

---

## 연습문제 4: overflow 속성과 스크롤

**문제:**

다음 CSS 속성 중 `overflow: scroll;`이 설정된 경우 어떤 현상이 발생하며, `overflow: hidden;`과의 차이점을 설명하시오.

```css
.container {
  width: 400px;
  height: 100px;
  border: 3px solid black;
  position: relative;
  overflow: scroll;
}

```

**예상 정답:**

- `overflow: scroll;`은 컨텐츠가 부모 요소의 크기를 초과할 때, 무조건 스크롤바를 표시하여 사용자에게 초과 내용을 스크롤하여 볼 수 있게 합니다.
- `overflow: hidden;`은 초과되는 부분을 숨겨서 보이지 않도록 합니다.

**해설:**

`overflow` 속성은 컨텐츠가 지정된 영역을 벗어났을 때 처리 방식을 결정합니다.

- `scroll`은 초과분이 있더라도 스크롤바를 항상 표시하므로, 사용자가 스크롤하여 내용을 확인할 수 있습니다.
- 반면, `hidden`은 초과되는 부분을 잘라내어 보이지 않게 하지만, 스크롤은 제공하지 않습니다.

---

---

## 연습문제 1: 배경 속성 활용

**문제:**

`.hero` 클래스를 가진 요소에 다음 요구사항대로 배경 스타일을 적용하는 CSS 코드를 작성하시오.

- 배경 이미지: `hero.jpg`
- 배경 이미지는 반복 없이 한 번만 표시
- 배경은 전체 요소 너비에 맞추어 크기를 조절 (cover 사용)
- 배경 이미지는 스크롤 시 고정
- 배경 위치는 중앙 상단
- 배경 색상은 #cccccc (이미지 미로드 시 대체 색상)

**예상 정답:**

```css
.hero {
  background-image: url('hero.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
  background-position: center top;
  background-color: #cccccc;
}

```

**해설:**

이 코드는 배경에 여러 가지 속성을 한 번에 설정합니다.

- `background-image`로 `hero.jpg`를 지정하고,
- `background-repeat: no-repeat`로 이미지 반복을 막으며,
- `background-size: cover`를 통해 요소 전체를 덮도록 이미지를 조절합니다.
- `background-attachment: fixed`는 스크롤 시에도 배경이 고정되도록 하고,
- `background-position: center top`은 배경 이미지를 중앙 상단에 위치시킵니다.
- 마지막으로, `background-color`는 이미지가 없는 경우 대체 색상으로 사용됩니다.

---

## 연습문제 2: 폰트 속성 적용

**문제:**

`.headline` 클래스를 가진 요소의 텍스트에 대해 다음 스타일을 적용하는 CSS 코드를 작성하시오.

- 폰트 패밀리: "Arial", 대체 폰트로 sans-serif
- 글자 크기: 36px
- 글자 기울기: italic
- 줄 간격(line-height): 1.2
- 텍스트 정렬: central(즉, center)

**예상 정답:**

```css
.headline {
  font-family: Arial, sans-serif;
  font-size: 36px;
  font-style: italic;
  line-height: 1.2;
  text-align: center;
}

```

**해설:**

- `font-family`를 통해 먼저 Arial을 사용하고, Arial이 없을 때는 sans-serif 계열로 대체합니다.
- `font-size`와 `font-style`로 글자 크기와 기울기를,
- `line-height`는 글자의 행간을 설정하며,
- `text-align: center;`는 텍스트를 중앙으로 정렬합니다.

---

## 연습문제 3: 위치 속성 및 z-index

**문제:**

다음 HTML 구조를 기준으로, 컨테이너 내에 세 개의 박스(`.box1`, `.box2`, `.box3`)를 절대 위치로 위치시키고, 각 박스의 크기는 150×150px로 설정합니다.

- `.box1`: 좌표 (10px, 10px), 배경색 red, z-index 3
- `.box2`: 좌표 (30px, 30px), 배경색 green, z-index 2
- `.box3`: 좌표 (50px, 50px), 배경색 blue, z-index 1
또한, 부모 컨테이너는 크기가 400×400px, `position: relative;`로 지정합니다.
CSS 코드를 작성하시오.

**예상 정답:**

```css
.container {
  position: relative;
  width: 400px;
  height: 400px;
}
.box1, .box2, .box3 {
  position: absolute;
  width: 150px;
  height: 150px;
}
.box1 {
  background-color: red;
  left: 10px;
  top: 10px;
  z-index: 3;
}
.box2 {
  background-color: green;
  left: 30px;
  top: 30px;
  z-index: 2;
}
.box3 {
  background-color: blue;
  left: 50px;
  top: 50px;
  z-index: 1;
}

```

**해설:**

- 부모 컨테이너에 `position: relative;`를 적용하면, 자식 요소들이 부모를 기준으로 절대 위치를 설정할 수 있습니다.
- 각 박스는 `position: absolute;`로 지정되어 좌표(left, top) 값을 기준으로 배치되고, z-index 값에 따라 겹침 순서가 결정됩니다.

---

---

## 연습문제 4: overflow 속성

**문제:**

고정된 크기의 컨테이너(`.overflow-container`)가 있으며, 내부 내용이 이 영역을 벗어날 경우 초과된 내용을 숨기려면 어떤 CSS 코드를 적용해야 하는지 작성하시오.

- 컨테이너 크기: width 300px, height 200px

**예상 정답:**

```css
.overflow-container {
  width: 300px;
  height: 200px;
  overflow: hidden;
}

```

**해설:**

- `overflow: hidden;`을 사용하면 내부 콘텐츠가 컨테이너의 경계를 벗어났을 경우, 초과 부분이 잘려서 보이지 않게 됩니다.
- 반대로, `overflow: scroll;`이나 `auto;`를 사용하면 스크롤바를 통해 초과 콘텐츠를 볼 수 있게 됩니다.

---

---

## 연습문제 5: 종합 응용 – 배너 디자인

**문제:**

`.banner` 클래스를 가진 요소를 다음과 같이 스타일링하시오.

- 배경 이미지: `banner.jpg`
- 배경 이미지는 반복 없이 전체 너비(100%)에 맞춰, 높이는 자동 (`background-size: 100% auto;`)
- 배경 색상: #f5f5f5
- 배경 이미지는 고정(`background-attachment: fixed`)되고, 중앙 상단에 위치
- 텍스트는 중앙 정렬되며, 흰색이고, 크기는 48px
- 텍스트 위에 반투명한 검은색 오버레이를 적용하기 위해, `:before` 의사 요소를 사용하여 전체를 덮는 반투명(0.5) 검은색 레이어를 추가하시오.

**예상 정답:**

```css
.banner {
  position: relative;
  text-align: center;
  color: white;
  font-size: 48px;
  background-image: url('banner.jpg');
  background-repeat: no-repeat;
  background-size: 100% auto;
  background-attachment: fixed;
  background-position: center top;
  background-color: #f5f5f5;
}

.banner::before {
  content: "";
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background-color: rgba(0,0,0,0.5);
  z-index: 0;
}

.banner > * {
  position: relative;
  z-index: 1;
}

```

**해설:**

- `.banner` 클래스는 배경 이미지와 배경 색상을 지정하고, 텍스트 스타일을 적용합니다.
- `::before` 의사 요소를 사용하여 배너 전체에 걸쳐 반투명한 검은색 오버레이를 삽입합니다.
- 오버레이 아래에 있는 텍스트는 `z-index` 설정으로 보이도록 대비를 높입니다.
- 이와 같이 구성하면, 이미지와 텍스트가 잘 어우러진 효과적인 배너 디자인을 만들 수 있습니다.

---
# CSS3 변형과 애니메이션, CSS3 변환

Date: 2025년 3월 20일
페이지: p.401~449
완료: Yes
1일후 복습: No
7일후(주말) 복습: No
1달후 복습: No

CSS3 변형과 애니메이션

변형 속성 기본

CSS3에서 움직임을 구현할 수 있는 기능은 애니메이션 속성과 변형 속성으로 나뉜다.

부드러운 애니메이션을 적용할때 필요한 기능이 변형 속성이다.

CSS3의 변형 속성은 다음 스타일 속성과 함께 사용할 수 있다.

위치속성 top,left,bottom,right

크기 속성 width,height

박스 속성 margin, padding

테두리 속성 border-width, border-radius, border-color

색상 속성 color, background-color

투명도 속성 opacity

변환 속성 transform

변형 속성

CSS3는 다음과 같은 변형 속성을 제공한다.

transition 모든 transition 속성을 한번에 사용한다

transition-delay 이벤트 발생 후 몇초후에 재생할지 지정한다.

transition-duration 몇초동안 재생할지 지정한다.

transition-property 어떤 속성을 변형할지 지정한다.

transition-timing-function 수치 변형 함수를 지정한다.

transition-delay 속성

이벤트가 발생하고 몇초동안 기다린후 애니메이션이 작동할때 지정하는 속성.

transition-timing-function 속성

수치를 변형하는 함수를 지정할 때 사용하는 속성.

각각의 속성은 ease, linear, ease-in, ease-out, ease-in-out.

마음에 드는 형태가 없다면 cubic-bezier()함수를 사용

transition-property 속성

각각의 속성에 다른 형태의 애니메이션을 적용하고싶을때 사용.

지금까지의 모든 변형 속성은 transition 속성으로 한번에 입력할 수 있다.

키 프레임과 애니메이션 속성

CSS3는 다음의 애니메이션 속성을 지원한다.

animation 모든 애니메이션 속성을 한번에 적용한다.

animation-delay 이벤트 발생 후 몇 초 후에 재생할지 지정한다.

animation-direction 애니메이션 진행 방향을 설정한다.

animation-duration 애니메이션을 몇 초 동안 재생할지 지정한다.

animation-iteration-count 애니메이션 반복 횟수를 지정한다.

animation-name 애니메이션 이름을 지정한다.

animation-play-state 애니메이션 재생 ㅅ아태를 지정한다.

animation-timing-function 수치 변형 함수를 지정한다.

@keyframes 키프레임규칙이라 부르며 css3에서 애니메이션을 지정하는 형식이다.

@keyframes 이름 형태로 입력한다.

키프레임 안에는 퍼센트 단위로 애니메이션을 적용한다, 예외적으로 0%와 100%의 경우는 from과 to를 사용 가능하다.

animation-name 속성

키프레임을 생성한 이후에는 animation-name 속성을 사용해 태그를 키 프레임에 연결한다.

애니메이션 속성은 반드시 name과 duration 속성을 사용해야한다.

animation-iteration-count 속성

애니메이션을 특정 횟수만큼 반복하고 싶을때 사용한다.

숫자를 적용하며 적용한 숫자만큼 애니메이션을 반복한다.

무한번 반복하고싶으면 infinite 키워드를 적용한다.

animation-direction 속성

애니메이션을 반복하는 형태를 지정한다.

키워드는 다음과같다.

alternate  from에서 to로 이동후 to에서 from으로 이동을 반복

normal 계속 from에서 to로 이동

animation-play-state 속성

애니메이션을 중지하고 재생할때 사용하는 속성이다.

일반적으로 js를 사용해 조절한다.

anmation 속성은 통합해서 순서대로 사용할 수 있다, 사용하고싶지 않다면 none을 사용한다.

CSS3 변환

변환이란?

3차원을 구현하는 방법은 크게 2가지로 나뉜다

js를 사용한 webgl

css3를 사용한 3차원 변환

2차원 변환

transform 속성

transform 속성을 사용해 객체를 변환할 수 있다.

css3에서 가장 중요한 특징으로 꼽히고 있다.

2차원 변환 함수

css3는 변환 함수를 사용해 변활을 수행한다. 변환함수는 다음과 같다

translate(translateX, translateY) 특정 크기 만큼 이동한다.

translateX(translateX) X축으로 특정 크기만큼 이동한다.

translateY(translateY) Y축으로 특정 크기만큼 이동한다.

scale(scaleX, scaleY) 특정 크기 만큼 확대 및 축소한다.

scaleX(scaleX) X축으로 특정 크기만큼 확대 및 축소한다.

scaleY(scaleY) Y축으로 특정 크기만큼 확대 및 축소한다.

skew(angleX, angleY) 특정 각도만큼 기울인다.

angleX(angleX) X축으로 특정 각도 만큼 기울인다.

angleY(angleY) Y축으로 특정 각도 만큼 기울인다.

rotate(angleZ) 특정 각도만큼 회전한다.

transform 속성에 각각의 함수를 공백으로 구분해 입력한다.

변환 함수의 순서대로 변환이 이루어지기때문에 순서는 중요하다.

transform-origin 속성

변환 중심을 설정하는 속성이다. 태그 영역의 중심을 변환 중심으로 잡는다.

속성에는 2개의 크기 단위를 적용할 수 있으며 각각 변환 중심의 x좌표와 y좌표를 의미한다.

퍼센트 단위로 지정할 수도있고 키워드를 사용할 수도 있다.

3차원 변환

3차원 변환 함수

css3는 다음의 3차원 변환 함수를 제공한다

translate3d(translateX, translateY, translateZ) 특정 크기 만큼 이동한다.

translateX(translateX) X축으로 특정 크기만큼 이동한다.

translateY(translateY) Y축으로 특정 크기만큼 이동한다.

translateZ(translateZ) Z축으로 특정 크기 만큼 이동한다.

scale3d(scaleX, scaleY, scaleZ) 특정 크기 만큼 확대 및 축소한다.

scaleX(scaleX) X축으로 특정 크기만큼 확대 및 축소한다.

scaleY(scaleY) Y축으로 특정 크기만큼 확대 및 축소한다.

scaleZ(scaleZ) Z축으로 특정 크기만큼 확대 및 축소한다.

rotate3d(angleX, angleY,angleZ) 특정 각도만큼 회전한다.

rotateX(angleX) X축으로 특정 각도 만큼 회전한다.

rotateY(angleY) Y축으로 특정 각도 만큼 회전한다.

rotateZ(angleZ) Z축으로 특정 각도만큼 회전한다.

transform-style 속성

변환을 적용할 때 그 영향력이 자신에게만 적용할지 자손에게도 적용될지 정하는 속성

자손의 3차원 속성을 유지한채로 부모를 회전시키고 싶을때는 부모의 transform-style 속성에

preserve-3d 키워드를 적용.

transform-style에는 다음의 키워드를 사용한다.

flat 후손의 3차원 속성을 무시

preserve-3d 후손의 3차원 속성을 유지

backface-visibility 속성

3차원 공간에서 평면의 후면을 보이거나 보이지 않게 만드는 스타일이다.

키워드는 다음과 같다.

visible 후면을 보이게한다

hidden 후면을 보이지 않게 한다.

원근법

perspective는 원근법을 지정하는 속성이다, 얼마나 많은 3차원 픽셀을 놓을것인지 정의하는속성이다. 일반적으로 400~2000픽셀 사이를 입력한다.
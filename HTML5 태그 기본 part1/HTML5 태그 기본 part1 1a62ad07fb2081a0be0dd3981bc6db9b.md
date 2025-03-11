# HTML5 태그 기본 part1

Date: 2025년 2월 26일
페이지: P.35~P.70
완료: Yes
모르는것 존재: No

- 태그와  요소
    
    <h1>시작태그 </h1>끝태그
    
    일부태그는 태그 내부에 다른 태그를 삽입할 수 있다.
    
- 속성
    
    <h1 title=”heder”>title을 속성이름 header를 속성값으로 표현.
    
- 주석
    
    일반적인 슬래쉬 주석과 달리 <!— —>로 표기.
    
    emmet 명령어는 ctrl+/
    
- 페이지구조
    
    ```html
    <!DOCTYPE html>
    <html lang="ko-KR">
      <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title></title>
      </head>
      <body></body>
    </html>
    ```
    
    1줄 현재 버전을 의미, 반드시 있어야함.
    
    2줄 어느 언어로 만들어져있는지 표시
    
    <head> 바디에 필요한 스타일시트와 자바스크립트 기입
    
    <title> 제목
    
    <body> 실제로 보이는 영역
    
- 제목태그
    
    h1~h6 제목사용태그 숫자 순서대로 사용하며 h1은 한 화면에 한개
    
- 본문태그
    
    p  단락생성
    
    br 줄바꿈
    
    hr 수평줄
    
    a 앵커태크 링크역할
    
    링크기능을 없애고싶다면 href=”#”
    
- 글자태그
    
    b 굵은글자
    
    i 기울어진글자
    
    small 작은글자
    
    sub 아래첨자
    
    sup 윗첨자
    
    ins 밑줄
    
    del 취소선
    
- 목록태그
    
    ul 순서가 없는 목록 (점으로)
    
    ol 순서가 있는 목록 (숫자등)
    
    li 목록 요소
    
- 정의태그
    
    dl 정의목록
    
    dt 정의용어
    
    dd 정의설명
    
- 테이블태그
    
    <table></table>사용
    
    tr 행 
    
    th 행제목
    
    td 행내용
    
    border 표 테두리 두께
    
    <table border=”3”>의 형태
    
    <th colspan=”3”> 셀넓이
    
    <th rowspan=”3”> 셀 높이
    
- 이미지태그
    
    <img src=”apple.png” alt=”사과” width=”300” height=”150”>
    
    src 이미지경로
    
    alt 이미지가 없을때 출력
    
    dummyimage.com을 이용 더미이미지
    
- 오디오태그
    
    ```html
    <audio controls>
            <source src="https://www.w3schools.com/html/horse.mp3" type="audio/mpeg" />
            Your browser does not support the audio element.
        </audio>
    ```
    
    src 음악경로
    
    preload 재생하기전에 모두 불러오기
    
    autoplay 자동재생
    
    loop 반복재생
    
    controls 재생도구출력
    
    type 태그는 트래픽낭비 방지를 위함.
    
- emmet
    
    h1  <h1></h1>
    
    h1+h2 <h1>…</h2>
    
    h$*6 <h1><h2>…</h6>
    
    h${hello}*6 <h1>hello</h1>..hello</h6>
    
    div.one.two <div class=”one two”></div>
    
    div#one.two.three  <div id="one" class="two three"></div>
    
- 유용한 단축키
    
    동시편집 ctrl+alt+방향, alt+클릭
    
    설정 ctrl+,
    
    터미널 ctrl+`
    
    사이드바 ctrl+b
    
    동시편집 ctrl+d
    
    주석 ctrl+/
    
    내어쓰기 shift+tab
    
    커서가 뒤에있을땐 ctrl+] or [
    
    한줄삭제 shift+del
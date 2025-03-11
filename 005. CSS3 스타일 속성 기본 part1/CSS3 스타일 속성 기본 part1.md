# CSS3 스타일 속성 기본 part1

Date: 2025년 3월 4일
페이지: p.157~p.184
완료: Yes

1. CSS3 단위
    - 크기 단위
        
        `%` 백분율단위
        
        `em` 배수단위
        
        `px` 픽셀
        
    - 색상 단위
        
        `#000000` hex  코드 단위
        
        `rgb(n,n,n)` rgb 색상 단위
        
        `hsla(n,n,n,n)` hsla 색상 단위
        
    - URL 단위
        
        `url()` 
        
        `background-image:url('a.jpg')`
        
2. 가시 속성
    - display 속성
        
        `display:none;` 화면에서 보이지 않게 만듦
        
        `block` 태그를 block 형식 지정
        
        `inline` 태그를 inline 형식 지정
        
        `inline-block` 태그를 inline-block 형식 지정
        
    - visibility 속성
        
        `visibility:visible` 태그를 보이게
        
        `hidden` 태그를 보이지 않게
        
        `collapse` 테이블을 보이지 않게
        
    
    display의 none은 화면에서 제거
    
    visibility의 hidden은 화면에 보이지 않을뿐이라 공백발생
    
    - opacity 속성
        
        `opacity:` 투명도 조절
        
3. 박스 속성
    
    ![images_sue6e2_post_b6d59cef-8f56-49a4-85e3-73e02888e046_box속성.png](images_sue6e2_post_b6d59cef-8f56-49a4-85e3-73e02888e046_box%EC%86%8D%EC%84%B1.png)
    
    `width, height` 글자를 감싸는 영역의 크기
    
    `margin, padding` 마진과 패딩의 너비
    
    `margin: 0 30px;` 연달아 적용가능 (상하좌우)
    
    `box-sizing` 글자박스의 크기 범위 지정
    
4. 테두리 속성
    
    `border-width` 테두리의 너비를 지정
    
    `border-style` 테두리의 형태를 지정
    
    `border-color` 테두리의 색상
    
    `border-radius: 10px;` 테두리의 곡률
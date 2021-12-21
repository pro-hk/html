# 나만의 정리
---
## HTML
- 먼저 쓴 내용부터 적용됨
- 맨 마지막에 적용하고 싶으면 defer 추가
- 이미지 2개 등록 후 교차로 보이게(hover효과 등) 하면 위치 설정할 필요X
- logo는 보통 `<H1>`으로 설정
- inherit : 부모의 설정대로 따라감
### 폰트
#### 폰트 크기
 - rem : html 폰트 크기의 배수
 - em : 부모 폰트 크기의 배수
   
#### 구글 폰트 적용
 - 구글 폰트 사이트 접속 (https://fonts.google.com/)
 - 원하는 폰트 검색 및 선택
 - 우측에 link 복사해서 html head 상단에 붙여넣기
 - css에서 font-family 설정
```scss
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Lexend:wght@100;200;300;400;500;600;700;800;900&family=Noto+Sans+KR:wght@100;300;400;500;700;900&display=swap" rel="stylesheet" />
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet" />

body { font-family: "Lexend", "Noto Sans KR", sans-serif; }
```
   
### POSITION
- 자식의 부피만 갖음 → width와 height 설정시 원하는 부피가 생김
- z-index로 화면에 나타나게 조정 가능
#### ABSOLUTE
- 좌표를 지정할 수 있음
- 부모에 POSITION 적용해야 따라감 ( 미적용시 HTML 전체에 반영)
#### FIXED
- 부모와 상관없이 고정된 좌표를 지정
#### RELATIVE
- POSITION 선언만 하는 것 같음( 크게 영향이 없어 ABSOLUTE 쓴 부모에게 적용하는 것 같음)
   
### DISPLAY
#### FLEX
- 기본적으로 row(가로정렬), nowrap(줄바꿈X) 설정
- flex-direction : column / flex-wrap : wrap 변경 가능
- justify-content : 기준 축 방향 정렬 / align-items: 기준 반대축 방향 정렬
#### BLOCK
- inline → block 가능하게 함
- width와 height 설정시 부피가 생김
#### NONE
- 화면상에 나타나지 않음(부피 0)
---
##  scss
- 이름에 _ 설정시 css 저장안됨
### 1. mixin
#### 1. 설정
@mixin 설정할 이름($매개변수 : 지정값) { 설정할 내용; }
```scss
@mixin pseudo($display: block, $position: absolute) {
  content: "";
  display: $display;
  position: $position;
}
```
#### 2. 사용
1. 상단에 @import "mixins"; 선언
 - 이름에 있는 `_`는 생략
```scss
@import "mixins";
```
2. @include 설정한 이름(매개변수 값 입력);
- 미설정시 기본값 출력
```scss
@include pseudo();
```
---


자바스크립트 : run time -- 웹브라우저에 해석기가 있음

자바
JDK 설치
editor == 이클립스 / intelli j

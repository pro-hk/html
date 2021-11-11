# 나만의 정리
---
##  scss 설정
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

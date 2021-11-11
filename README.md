# HTML정리
---
## 1. mixin 설정   
@mixin 설정할 이름($매개변수 : 지정값) { 설정할 내용; }
```scss
@mixin pseudo($display: block, $position: absolute) {
  content: "";
  display: $display;
  position: $position;
}
```

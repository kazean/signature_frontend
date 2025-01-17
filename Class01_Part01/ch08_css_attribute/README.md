# Ch08. CSS 속성
- [1. 개요](#ch08-01-개요)
- [2. 너비 - width, height](#ch08-02-너비width-height)
- [3. css 단위](#ch08-03-css-단위)
- [4. 외부여백 - margin](#ch08-04-외부-여백margin)
- [5. 내부여백 - padding](#ch08-05-내부-여백padding)
- [6. 태두리 선(border)과 색상표현](#ch08-06-테두리-선border과-색상-표현)
- [7. 모서리 둥굴게 - border-radius](#ch08-07-모서리-둥굴게border-radius)
- [8. 크기계산 - box-sizing](#ch08-08-크기-계산box-sizing)
- [9. 넘침제어 - overflow](#ch08-09-넘침-제어overflow)
- [10. 출력특성 - display](#ch08-10-출력-특성display)
- [11. 투명도](#ch08-11-투명도)
- [12. 글꼴](#ch08-12-글꼴)
- [13. 문자](#ch08-13-문자)
- [14. 배경](#ch08-14-배경)
- [15. 배치(1)](#ch08-15-배치1)
- [16. 배치(2)](#ch08-16-배치2)
- [17. 배치(3)](#ch08-17-배치3)
- [18. 플랙스 정렬 Container - 1](#ch08-18-플랙스정렬-container1)
- [19. 플랙스 정렬 Container - 2](#ch08-19-플랙스정렬-container2)
- [20. 플랙스 정렬 - items](#ch08-20-플랙스정렬-items)
- [21. 전환](#ch08-21-전환)
- [22. 변환 - 1](#ch08-22-변환1)
- [23. 변환 - 2](#ch08-23-변환2)
- [24. Overwatch 캐릭터 선택예제- 1](#ch08-24-overwatch-캐릭터-선택예제1)
- [25. Overwatch 캐릭터 선택예제- 2](#ch08-25-overwatch-캐릭터-선택예제2)


---------------------------------------------------------------------
# ch08-01. 개요
- HTML 속성(Attributes), CSS 속성(Properties), JS 속성(Properties)
- 박스모델, 글꼴, 문자, 배경, 배치, 플렉스(정렬), 전환, 변환, 띄움, 애니메이션, 그리드, 다단, 필터
- 플렉스: 수평정렬, 띄움의 최신 기술
- 전환: 애니메이션(전, 후) 상태
- 변환: 회전, 이동, 크기 조절(요소의 변화 2D, 3D)
- 띄움: 요소를 공중으로 띄운다(그 주변으로 문자가 흐를 수 있는 구조)
- 다단: 하나의 페이지를 여러 개로 나누는 것
- 필터: 흐림(Blur)/흑백(Grayscale)/반전(Reverse) 처리 등


---------------------------------------------------------------------
# ch08-02. 너비(width, height)
- 박스 모델
- 요소의 가로/세로너비
> - `auto`: 기본값, 브라우저가 너비를 계산
> - 단위: `px`, em, vw 등 단위로 저장
- span
> - 대표적인 인라인 요소
> - 포함한 크기만큼 자동으로 줄어듬(auto)
- div
> - 대표적인 블럭 요소
> - w: 부모 요소의 크기만큼 자동으로 늘어남(auto)
> - h: 포함한 콘텐츠 크기만큼 자동으로 줄어듬
## max-width, max-height
- 요소가 커질 수 있는 최대 가로/세로 너비
> - none: 최대 너비 제한 없음(default)
> - auto, 단위
## min-width, max-height
> - 0: 최소 너비 제한 없음(default)
> - auto, 단위

## 실습(codepen)
```html
<div class="parent">
  <div class="child"></div>
</div>
```
```css
.parent {
  width: 300px;
  height: 200px;
  background-color: royalblue;
}
.child {
  min-width: 400px;
  height: 100px;
  background-color: orange; 
}
```
> 부모가 300px이지만 400px까지만 줄어듬


---------------------------------------------------------------------
# ch08-03. CSS 단위
- px: 픽셀(절대단위), 모니터크기(상대단위)
- %: 백분위
- em: 요소의 글꼴 크기, 1em(default = 10px)
- rem: 루트 요소(html)의 글꼴 크기
- vw: 뷰포트 가로 너비의 백분율
- vh: 뷰포트 세로 너비의 백뷴율

## 실습
```css
html {
/*   font-size: 16px; */
}
.parent {
  width: 300px;
  height: 200px;
  background-color: royalblue;
  font-size: 10px;
}
.child {
  width: 10em;
  height: 50%;
  background-color: orange; 
}
```


---------------------------------------------------------------------
# ch08-04. 외부 여백(margin)
- 요소 의 외부 여백(공간)을 지정하는 `단축 속성`
- 음수를 사용할 수 있다
> - 0: default
> - auto: 브라우저가 여백을 계산, 가운데 정렬의 활용
> - 단위
> - margin-top, right, bottom, left (`개별속성`)
> > - margin: 10px 20px; // top/bottom: 10px, left/right: 20px
> > - margin: 10px 20px 30px; //top, left/right, bottom
> > - marign: 10px 20px 30px 40px // top right, bottom, left(시계방향)

## 실습
```html
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```
```css
.container {
  
}
.container .item {
  width: 100px;
  height: 100px;
  background-color: orange;
  border: 4px solid red;
  margin: -20px 10px;
}
```


---------------------------------------------------------------------
# ch08-05. 내부 여백(padding)
- 요소의 내부 여백(공간)을 지정하는 `단축속성`
> - 0: default, 내부 여백 없음
> - 단위
> - %: 부모 요소의 가로 너비에 대한 비율로 지정
> - padding-top, right, bottom, left
> > - padding: 10px 20px 30px; // margin과 동일
> > - padding: 10px 20px 30px 40px;

---------------------------------------------------------------------
# ch08-06. 테두리 선(border)과 색상 표현
- 요소의 테두리 선을 지정하는 `단축속성`
- border: 선-두께(-width) 선-종류(-style) 선-색상(-color); // 요소 크기가 커짐
> - border: medium none black; // default
> - border-style: solid; (실선)
## border-width
요소 테두리 선의 두께
- medimum(d), thin, thick
- 단위 px, em, %
> - border-width: top, right, bottom, left // margin 과 같음
## border-style
요소 테두리 선의 종류
- `none(d), solid(실선), dashed(파선)`, 점선(dotted), 두 줄선(double), ...
> - border-style: top, right, ...
> - border-방향, border-방향-속성
# border-color
요소 테두리 선의 색상을 지정하는 단축 속성
- black(d), 색상, transparent(투명)
- border-color: top, ...
- 색상 표현
> - 색상이름(red, tomato), `Hex색상코드`(#000, #FFFFFF)
> - RGB: rgb(255, 255, 255) // 함수, RGBA: rgba(0, 0, 0, 0.5) rgba(0, 0, 0, 50%)

## 실습
```css
.container .item {
  width: 100px;
  height: 100px;
  background-color: orange;
    
}
.container .item:first-child {
  border: 10px dashed red;
}
```


---------------------------------------------------------------------
# ch08-07. 모서리 둥굴게(border-radius)
- 요소의 모서리를 둥글게 깎음
> - 0: 둥글게 없음, 단위
> - border-radius: 0 10px 0 0; // 왼쪽 상단부터 시계방향
> > px: 반지름


---------------------------------------------------------------------
# ch08-08. 크기 계산(box-sizing)
- 요소의 크기 계산 기준을 지정
> - content-box(d): 요소의 내용으로 크기 계산
> - border-box: 요소의 내용 + padding + border로 크기 계산

## 실습
```html
<div class="item">Hello</div>
<div class="item">Hello</div>
```
```css
.item {
  width: 100px;
  height: 100px;
  background-color: orange;
}
.item:first-child {
  border: 4px solid red;
  padding: 20px;
  box-sizing: border-box;
}
```


---------------------------------------------------------------------
# ch08-09. 넘침 제어(overflow)
- 요소의 크기 이상으로 내용이 넘쳤을 때, 보여짐을 제어하는 단축속성
> - visible: d, 넘친 내용을 그대로 보여줌
> - hidden(잘라냄), auto(넘친 경우에만 잘라내고 스크롤바 생성), scroll
> - overflow-x/y: 개별속성

## 실습
```html
<div class="parent">
  <div class="child"></div>
</div>
```
```css
.parent {
  width: 200px;
  height: 150px;
  background-color: royalblue;
  margin: 20px;
  padding: 20px;
  overflow: auto;
}
.child {
  width: 300px;
  height: 100px;
  background-color: orange
}
```
> scroll 시 세로도 스크롤이 생김 > auto


---------------------------------------------------------------------
# ch08-10. 출력 특성(display)
- 요소의 화면 출력 특성
> - block, inline, inline-block : 각 요소에 이미 지정되어 있는 값
> - flex(1차원 레이아웃), grid(2차원 행,열), none(화면에서 사라짐), 기타(table, table-row, table-cell, ...) : 따로 지정해서 사용하는 값


---------------------------------------------------------------------
# ch08-11. 투명도
- 요소 투명도
> - 1: d, 불투명
> - 0~1
> > - opacity: 0.4;

## 실습
```css
.parent {
  width: 100px;
  height: 100px;
  padding: 30px;
  background-color: royalblue;
  
}
.child {
  width: 200px;
  height: 100px;
  background-color: orange;
  opacity: .5;
}
```


---------------------------------------------------------------------
# ch08-12. 글꼴


---------------------------------------------------------------------
# ch08-13. 문자


---------------------------------------------------------------------
# ch08-14. 배경


---------------------------------------------------------------------
# ch08-15. 배치(1)


---------------------------------------------------------------------
# ch08-16. 배치(2)


---------------------------------------------------------------------
# ch08-17. 배치(3)


---------------------------------------------------------------------
# ch08-18. 플랙스(정렬) Container(1)


---------------------------------------------------------------------
# ch08-19. 플랙스(정렬) Container(2)


---------------------------------------------------------------------
# ch08-20. 플랙스(정렬) Items


---------------------------------------------------------------------
# ch08-21. 전환


---------------------------------------------------------------------
# ch08-22. 변환(1)


---------------------------------------------------------------------
# ch08-23. 변환(2)


---------------------------------------------------------------------
# ch08-24. Overwatch 캐릭터 선택(예제1)


---------------------------------------------------------------------
# ch08-25. Overwatch 캐릭터 선택(예제2)
# Ch06. HTML 핵심 정리
- [1. 핵심 요소 정리](#ch06-01-핵심-요소-정리)
- [2. 핵심 요소 출력 연습](#ch06-02-핵심-요소-출력-연습)
- [3. 주석](#ch06-03-주석)
- [4. 전역 속성](#ch06-04-전역-속성)


---------------------------------------------------------------------
# Ch06-01. 핵심 요소 정리
## 블록
- `div(Division)`
> 특별한 의미가 없는 구분을 위한 요소
- h1 ~ 6(Heading): 제목
- p(Paragraph): 문장, div로 해도 무관
- `ul(Unordered List) > li(List Item)`, ol

## 인라인
- img: 이미지
- a(Anchor): 링크
> target="_blank": 새탭
- `span`
> 특별한 의미가 없는 구분, 특수 처리 등을 사용할때 사용
- br(Break): 줄바꿈
- `label`
> - 라벨 가능 요소(input)의 제목

## `인라인 - 블록(inline-block)`
- Base는 inline을 가지고 있지만, Block 특징도 가지고 있는 요소
- `input`
> - 사용자가 데이터를 입력하는 요소
> - `<input type="text" value="HEROPY!" />`
> - Attribute: placeholder(힌트), disabled(비활성화, 화면엔 보이나 입력금지), checked, name(Group명)

## 테이블 요소(table-cell)
- table > tr > td
> 크게 보면 블럭요소


---------------------------------------------------------------------
# Ch06-02. 핵심 요소 출력 연습
## 실습 (codepen)
- h, img
- ul, li
- a, span, input, label
- table > tr > td
> colspan, td{ border: 1px solid red;}
>  > 요즘엔 더 나은 레이아웃이 있기에 사용을 잘하지 않는다


---------------------------------------------------------------------
# Ch06-03. 주석
- <!-- Commnet -->
> Cmd + /

## 실습
```html
<!-- 애국가-->
<p>
  동해물과 백두산이 마르고 닳도록
  하느님이 보우하사 우리나라 만세
</p>
```
```css
body {
/*   font-size: 50px; */
}
```


---------------------------------------------------------------------
# Ch06-04. 전역 속성
- `<태그 title="속성"></태그>`
> 요소의 정보나 설명을 지정, 마우스 올렸을때
- stlye
- class
> 요소를 지칭하는 `중복 가능한` 이름 > 선택자
- id
> 요소를 지칭하는 `고유한` 이름
- data-이름="데이터"
> 요소에 데이터를 지정, 특정 데이터를 잠시 저장하는 용도 후에 CSS, JS에서 사용

## 실습(codepen)
```html
<span id="abc">동해물</span>과 <span class="red">백두산</span>이 마르고 닳도록
하느님이 보우하사 <span class="red">우리나라</span> 만세
```
```css
body {
  font-size: 50px;
}
.red{
  color: red;
}
#abc{
  color: blue;
}
```
```html
<div data-fruit-name="apple">사과</div>
<div data-fruit-name="banana">바나나</div>
```
```js
const els = document.querySelectorAll('div')
els.forEach(el => {
  console.log(el.dataset.fruitName)
})
```
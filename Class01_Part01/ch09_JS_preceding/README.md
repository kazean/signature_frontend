# Ch09. JS 선행
- [1. 개요](#ch09-01-개요)
- [2. 데이터 종류](#ch09-02-데이터-죵류)
- [3. 변수, 예약어](#ch09-03-변수-예약어)
- [4. 함수](#ch09-04-함수)
- [5. 조건문](#ch09-05-조건문)
- [6. DOM API - 1](#ch09-06-dom-api1)
- [7. DOM API - 2](#ch09-07-dom-api2)
- [8. 메소드 체이닝](#ch09-08-메소드-체이닝)
- [9. 질의 응답](#ch09-09-질의-응답)


---------------------------------------------------------------------
# Ch09-01. 개요
## 표기법
- dash-case(kebab-case)
- snake_case
- camelCase
- ParcelCase

### dash-case(kebab-case)
- HTML, CSS에서 주로 사용
> the-quick-brwon-fox

### snake_case
- HTML, SS
> the_qucik_brown_fox

### camelCase
- `JS`
> theQuickBrwonFox

### ParcelCase
- `JS`: 생성자
> TheQuickBrwonFox
> > 첫 글자가 대문자

## Zero-based Numbering
- 0 기반 번호 매기기

## 주석(Comments)
```js
// 한 줄 메모
/* 힌 즐 메모 */
/**
 * 여러 줄
 * 메모1
 * 메모2
 */
```
> 단축키 Command/Ctrl + /

## 실습(test)
```js
console.log('HEROPY');

let fruits = ['Apple', 'Banana', 'Cherry'];

console.log(fruits[0]);
console.log(fruits[1]);
console.log(fruits[2]);

console.log(new Date('2021-01-30').getDay()); // 6, 토요일
console.log(new Date('2021-01-31').getDay()); // 0, 일요일
console.log(new Date('2021-02-01').getDay()); // 1, 월요일
```


---------------------------------------------------------------------
# Ch09-02. 데이터 죵류
- String, Number, Boolean, Undefined, Null, Object, Array

### String
```js
// String: 문자 데이터
// 따옴표를 사용합니다: "", '', ``
let hello = `Hello ${myName}?!`; 
```
> 보간법, '`', ```${<param>}```

### Undefined
- 값이 할당되지 않은 상태

### Null
- 어떤 값이 의도적으로 비어있음을 의미
> Undefined와 차이

### Object
```js
// Object: 객체 데이터
// 여러 데이터를 Key:Value 형태로 저장 { }
let user = {
  name: 'HEROPY',
  age: 85,
  isValid: true
};
console.log(user.name);
```
### Array
```js
// Array: 배열 데이터
let fruits = ['Apple', 'Banana', 'Cherry'];
console.log(fruits[0]);
```
### Number, Boolean, Null


---------------------------------------------------------------------
# Ch09-03. 변수, 예약어
## 변수
- 데이터를 저장하고 참조(사용)하는 데이터의 이름
> var(X), `let, const`
```js
let a = 2;
let b = 5;
console.log(a + b);

a = 12;
console.log(a);

const c = 12;
c = 999; // TypeError

```
> 변수 선언
> - let: 재사용, 재할당
> - const: 값의 재할당 불가

## 예약어
- 특별한 의미를 가지고 있어, 변수나 함수 이름으로 사용 불가능
```js
let this = 'Hello'; // SyntaxError
let if = 123; // SyntaxError
let break; // SyntaxError
```


---------------------------------------------------------------------
# Ch09-04. 함수
- 특정 동작(기능)을 수행하는 일부 코드의 집합, `function`
```js
// BASIC
function helloFunc() {
  // 실행코드
  console.log(1234);
}
helloFunc();


// RET
function returnFunc() {
  return 123;
}
let a = returnFunc();
console.log(a);

// PARAM
function sum(a, b) {
  return a + b;
}

// 익명 함수
let world = function () {
  console.log('World~');
}
world();

// 객체 데이터
const heropy = {
  name: 'HEROPY',
  age: 85,
  // 메소드
  getName: function () {
    return this.name;
  }
}
const hisName = heropy.getName();
```


---------------------------------------------------------------------
# Ch09-05. 조건문


---------------------------------------------------------------------
# Ch09-06. DOM API(1)
- Document Object Model, Application Programming Interface
> HTML(Document) > DIV, SPAN
```js
// HTML 요소(Element) 1개 검색/찾기
const boxEl = docuemnt.querySelector('<CSS Selector>');

// 요소에 적용할 수 있는 메소드
boxEl.addEventListener();
// 2 - 핸들러
boxEl.addEventListener('click', function () {
  console.log('Click~!')
});

// 요소의 클래스 정보 객체 활용!
boxEl.classList.add('active');
let isContains = boxEl.classList.contains('active');
console.log(isContains);
boxEl.classList.remove('active');
```
> document
> - `.querySelector()`
> - `.classList`.add/remove/contains()

## 실습
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  
</head>
<body>
  <div class="box">box</div>

  <script src="main.js"></script>
</body>
</html>
```
```html
<head>
  <script defer src="main.js"></script>
</head>
```
```js
let boxEl = document.querySelector('.box');
console.log(boxEl);
```


---------------------------------------------------------------------
# Ch09-07. DOM API(2)
```js
// HTML 요소 모두 검색/찾기
const boxEls = document.querySelectorAll('.box');

// 찾은 요소들 반복해서 함수 실행, 유사배열
boxEls.forEach(function (boxEl, index) {});

// Getter, Setter
const boxEl = document.querySelector('.box');
console.log(boxEl.textContent);
boxEl.textContent = 'HEROPY';
```
> - `docuemtn.querySelectorAll(<Selector>)`
> > - boxEls.forEact(function () { })
> - boxEl.textContent

## 실습
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <script defer src="main.js"></script>
</head>
<body>
  <div class="box">1</div>
  <div class="box">2</div>
  <div class="box">3</div>
  <div class="box">4</div>
</body>
</html>
```
```js
const boxEls = document.querySelectorAll('.box');

boxEls.forEach(function (boxEl, index) {
  boxEl.classList.add(`order-${index+1}`)
  console.log(index, boxEl);
});
```


---------------------------------------------------------------------
# Ch09-08. 메소드 체이닝(Method Chaining)
- 메소듸를 연결해서 붙여서 사용하는 것
```js
const a = 'Hello~';
const b = a.split('').reverse().join(''); // Method Chaining
```
> split/reverse/join: reverse/join은 배열, join은 split뒤에 못붙인다.


---------------------------------------------------------------------
# Ch09-09. 질의 응답
- The quick brown fox > camelCase 
- `let fruits = ['Apple', 'Banana', 'Cherry']` > Banana 출력
- '값이 의도적으로 비어있음'을 의미하는 데이터
- {} 위 데이터 종류는?
- Undefined
- const
- Arguments(인수) - Parameters(매개변수, 함수 인수)
- 익명 함수(Anonymous Function)
- defer
- document.querySelector().textContent
- `El.addEventListener('<event>', <handler>)`
- `El.classList.add('<class>')`
- Method Chaining
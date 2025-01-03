# Ch03. 무작정 시작하기
- [1. DOCTYPE](#ch03-01-doctypedto)
- [2. html, head, body](#ch03-02-html-head-body)
- [3. CSS, JS 연결하기](#ch03-03-cssjs-연결하기)
- [4. 정보를 의미하는 태그 살펴보기](#ch03-04-정보를-의미하는-태그-살펴보기)
- [5. 화면에 이미지 출력하기](#ch03-05-화면에-이미지-출력하기)
- [6. 상대 경로와 절대 경로](#ch03-06-상대-경로와-절대-경로)
- [7. 페이지를 나누고 연결(링크)하기)](#ch03-07-페이지를-나누고-연결링크하기)
- [8. 모든 파일 공백 크기 설정](#ch03-08-모든-파일-공백-크기-설정)
- [9. 개발자 도구 사용하기](#ch03-09-개발자-도구-사용하기)


---------------------------------------------------------------------
# Ch03-01. Doctype(DTO)
DOCTYPE(DTD, Document Type Definition)은 마크업 언어에서 문서 형식을 정의하며, 웹 브라우저가 `어떤 HTML 버전의 해석방식으로 페이지를 이해`하면 되는지를 알려주는 용도
- `<!DOCTYPE html>`
> - 문서(페이지)의 HTML 버전을 지정
> - HTML1 ~ 4, XHTML, HTML5(표준)
- `<!DOCTYPE html PUBLIC "">`: XHTML(너무 구버전) 
## 실습 (test)
- index.html
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    
  </head>
  <body>

  </body>
</html>
```


---------------------------------------------------------------------
# Ch03-02. HTML, HEAD, BODY
- HTML: 문서의 전체 범위
> `<html>`: 시작, `</html>`: 종료
- head: 문서의 정보를 나타내는 범위
> 웹 페이지의 제목, 설명, 사용할 파일 위치, 스타일(CSS)같은 웹페이지의 보이지 않는 정보
- body: 문서의 구조를 나타내는 범위
> 로고, 헤더, 푸터, 내비게이션 등과 같은 웹페이지의 보여지는 구조를 작성하는 범위


---------------------------------------------------------------------
# Ch03-03. CSS,JS 연결하기
- css 연결
> `<link rel="stylesheet" href="./main.css">`
- javascript 연결
> `<script src="./main.js"></script>`
## 실습
- index.html
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="stylesheet" href="./main.css">
  <script src="./main.js"></script>
</head>
<body>
  <div>Hello world!</div>
</body>
</html>
```
- main.css
```css
div {
  color: red;
  font-size: 100px;
}
```
- main.js
```js
console.log('HEROPY!');
```


---------------------------------------------------------------------
# Ch03-04. 정보를 의미하는 태그 살펴보기
- meta, title, link, script, style

- title: HTML 문서의 제목을 정의
- `link`: 외부 문서(대부분 CSS)을 가져와 연결할 때 사용
> - `rel="stylesheet/icon" href="./main.css"`
> - `rel="icon" href="../favicon.png"`
- style: 스타일을 HTML 문서 안에서 작성하는 경우에 사용
- `script`: JS파일 가져오거나 HTML 문서 안에서 작성하는 경우
> `src="./main.js"`
- `meta`: HTML 문서의 제작자, 내용, 키워드 같은, 여러 정보를 검색엔진이나 브라우저에게 제공
> - `name="author" content="HEROPY"`: name(종류), content(정보의 값)
> - `name="viewport" content="width=device-with, initial-scale=1.0"`
> - `charset="UTF-8"`


---------------------------------------------------------------------
# Ch03-05. 화면에 이미지 출력하기
## img tag
`<img src="<경로>" alt="<대체문자>">`

## 실습
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HEROPY~</title>
  <link rel="stylesheet" href="./css/main.css">
  <script src="./js/main.js"></script>
  <style>
    div {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <div>Hello world!</div>
  <img src="./images/logo.png" alt="HEROPY">
  <img src="https://heropy.blog/css/images/logo.png" alt="HEROPY">
</body>
</html>
```
> images, css, js 폴더 생성


---------------------------------------------------------------------
# Ch03-06. 상대 경로와 절대 경로
- 상대경로 vs 절대경로
```txt
./ (생략가능)     http (https)
../             / (//)
http://localhost:5500
```
> index.html, images, css

- ex)
> - index.html: /images/heropy.png 
> - main.css: ../images/heropy.png /images/heropy.png
> - remote: https://heropy.blog/css/image/logo.png
## 실습
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HEROPY~</title>
  <link rel="stylesheet" href="./css/main.css">
  <script src="./js/main.js"></script>
  <style>
    div {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <div></div>
</body>
</html>
```
```css
div {
  width: 500px;
  height: 500px;
  background: url("/images/logo.png")
}
```
> background: url("/images/logo.png")


---------------------------------------------------------------------
# Ch03-07. 페이지를 나누고 연결(링크)하기
## a Tag
- `href="<경로>"`
## 실습
- main.html
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HEROPY~</title>
  <link rel="stylesheet" href="./css/main.css">
  <script src="./js/main.js"></script>
  <style>
    div {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <a href="https://naver.com">NAVER</a>
  <a href="/about">About</a>
  <a href="/login">Login</a>
</body>
</html>
```
- about/index.html
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <a href="/">HOME</a>
  About!!
</body>
</html>
```
> login.html


---------------------------------------------------------------------
# Ch03-08. 모든 파일 공백 크기 설정
## Settings
- tab size: Editor: Tab Size
> - CMD + SHIFT + P : Indent Using Tabs


---------------------------------------------------------------------
# Ch03-09. 개발자 도구 사용하기
## Dev Tools
- Elements 
> - Styles
> > - CSS Selector(선택자): .class
> > - :hov > :hover
> - Computed: 직접 적용된 Style

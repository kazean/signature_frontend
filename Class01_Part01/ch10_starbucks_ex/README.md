# Ch10. 스타벅스 예제
- [1. 시작하기 - 프로젝트 시작, 스타일 초기화, 파비콘](#ch10-01-시작하기---프로젝트-시작-스타일-초기화-파비콘)
- [2. 시작하기 - 오픈그래프와 트위터 카드](#ch10-02-시작하기---오픈그래프와-트위터-카드)
- [3. 시작하기 Google Fonts](#ch10-03-시작하기-google-fonts)
- [4. 시작하기 Google Material Icons](#ch10-04-시작하기-google-material-icons)
- [5. 헤더와 드롭다운 메뉴 - 로고](#ch10-05-헤더와-드롭다운-메뉴---로고)
- [6. 헤더와 드롭다운 메뉴 - 서브](#ch10-06-헤더와-드롭다운-메뉴---서브)
- [7. 헤더와 드롭다운 메뉴 - 검색](#ch10-07-헤더와-드롭다운-메뉴---검색)
- [8. 헤더와 드롭다운 메뉴 - 메인 메뉴(1)](#ch10-08-헤더와-드롭다운-메뉴---메인-메뉴1)
- [9. 헤더와 드롭다운 메뉴 - 메인 메뉴(2)](#ch10-09-헤더와-드롭다운-메뉴---메인-메뉴2)
- [10. 헤더와 드롭다운 메뉴 - BEM](#ch10-10-헤더와-드롭다운-메뉴---bem)
- [11. 헤더와 드롭다운 메뉴 - 전역 배지(GSAP)(1)](#ch10-11-헤더와-드롭다운-메뉴---전역-배지gsap1)
- [12. 헤더와 드롭다운 메뉴 - 전역 배지(GSAP)(2)](#ch10-12-헤더와-드롭다운-메뉴---전역-배지gsap2)
- [13. 순차적 스타일 애니메이션 - 전역 버튼 스타일(1)](#ch10-13-순차적-스타일-애니메이션---전역-버튼-스타일1)
- [14. 순차적 스타일 애니메이션 - 전역 버튼 스타일(2)](#ch10-14-순차적-스타일-애니메이션---전역-버튼-스타일2)
- [15. 순차적 스타일 애니메이션 - 순차적으로 요소 보이기](#ch10-15-순차적-스타일-애니메이션---순차적으로-요소-보이기)
- [16. 요소 슬라이드 - 공지사항](#ch10-16-요소-슬라이드---공지사항)
- [17. Swiper.js - 라이브러리 버전 확인하기](#ch10-17-swiperjs---라이브러리-버전-확인하기\)
- [18. 요소 슬라이드 - 수직 슬라이드(Swiper)](#ch10-18-요소-슬라이드---수직-슬라이드swiper)
- [19. 요소 슬라이드 - 요소 가운데 배치](#ch10-19-요소-슬라이드---요소-가운데-배치)
- [20. 요소 슬라이드 - 프로모션 이미지 슬라이드(1)](#ch10-20-요소-슬라이드---프로모션-이미지-슬라이드1)
- [21. 요소 슬라이드 - 프로모션 이미지 슬라이드(2)](#ch10-21-요소-슬라이드---프로모션-이미지-슬라이드2)
- [22. 요소 슬라이드 - 슬라이드 영역 토글](#ch10-22-요소-슬라이드---슬라이드-영역-토글)
- [23. 유튜브 영상 배경 - 리워즈](#ch10-23-유튜브-영상-배경---리워즈)
- [24. 유튜브 영상 배경 - Youtube iframe API(1)](#ch10-24-유튜브-영상-배경---youtube-iframe-api1)
- [25. 유튜브 영상 배경 - Youtube iframe API(2)](#ch10-25-유튜브-영상-배경---youtube-iframe-api2)
- [26. 유튜브 영상 배경 - 반복 애니메이션](#ch10-26-유튜브-영상-배경---반복-애니메이션)
- [27. 고정 이미지 배경](#ch10-27-고정-이미지-배경)
- [28. 3D 애니메이션](#ch10-28-3d-애니메이션)
- [29. 스크롤 위치 계산 애니메이션(1)](#ch10-29-스크롤-위치-계산-애니메이션1)
- [30. 스크롤 위치 계산 애니메이션(2)](#ch10-30-스크롤-위치-계산-애니메이션2)
- [31. 다중 요소 슬라이드](#ch10-31-다중-요소-슬라이드)
- [32. 푸터](#ch10-32-푸터)
- [33. 페이지 상단으로 이동(ScrollTo)](#ch10-33-페이지-상단으로-이동scrollto)


---------------------------------------------------------------------
# Ch10-01. 시작하기 - 프로젝트 시작, 스타일 초기화, 파비콘
- [Github](https://github.com/ParkYoungWoong/starbucks-vanilla-app?tab=readme-ov-file)
- 프로젝트 만들기, 파비콘, reset.min.css

## 뷰포트(Viewport) 렌더링 방식 설정
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<link rel="icon" href="./favicon.png" />
```
- 대부분의 경우 루트 경로에 favicon.ico 파일을 위치하면 자동으로 로딩하기 때문에
- `<link />` 를 작성할 필요가 없습니다. favicon.png 파일을 사용하려면 다음과 같이 `<link />`를 작성하세요.
- `width=device-width`: 화면의 가로 너비를 각 디바이스(Device)의 가로 너비와 동일하게 적용
- `initial-scale=1.0`: 화면의 초기 화면 배율(확대 정도)을 설정
- user-scalable=no: 사용자가 디바이스 화면을 확대(yes)/축소(no)할 수 있는지 설정
- maximum-scale=1: 사용자가 화면을 확대할 수 있는 최댓값
- minimum-scale=1: 사용자가 화면을 축소할 수 있는 최솟값

## 실습(STARBUCKS)
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Starbucks Coffe Korea</title>
  <link rel="icon" href="./favicon.png" />
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reset-css@5.0.2/reset.min.css" />
  <link rel="stylesheet" href="./css/main.css" />
</head>
<body>
  Hello world!
</body>
</html>
```
```css
body {
  color: red;
}
```


---------------------------------------------------------------------
# Ch10-02. 시작하기 - 오픈그래프와 트위터 카드
## `오픈 그래프(The Open Graph protocol)`
`웹페이지가 소셜 미디어(페이스북 등)로 공유`될 때 우선적으로 활용되는 정보를 지정합니다.
> [더 많은 오픈 그래프 속성](https://ogp.me/)
```html
<meta property="og:type" content="website" />
<meta property="og:site_name" content="Starbucks" />
<meta property="og:title" content="Starbucks Coffee Korea" />
<meta property="og:description" content="스타벅스는 세계에서 가장 큰 다국적 커피 전문점으로, 64개국에서 총 23,187개의 매점을 운영하고 있습니다." />
<meta property="og:image" content="./images/starbucks_seo.jpg" />
<meta property="og:url" content="https://starbucks.co.kr" />
```
- `og:type`: 페이지의 유형(ex, website, video.movie)
- og:`site_name`: 속한 사이트의 이름
- og:`title`: 페이지의 이름(제목)
- og:`description`: 페이지의 간단한 설명
- og:`image`: 페이지의 대표 이미지 주소(URL)
- og:`url`: 페이지 주소(URL)

## 트위터 카드(Twitter Cards)
웹페이지가 소셜 미디어(트위터)로 공유될 때 우선적으로 활용되는 정보를 지정합니다.
```html
<meta property="twitter:card" content="summary" />
<meta property="twitter:site" content="Starbucks" />
<meta property="twitter:title" content="Starbucks Coffee Korea" />
<meta property="twitter:description" content="스타벅스는 세계에서 가장 큰 다국적 커피 전문점으로, 64개국에서 총 23,187개의 매점을 운영하고 있습니다." />
<meta property="twitter:image" content="./images/starbucks_seo.jpg" />
<meta property="twitter:url" content="https://starbucks.co.kr" />
```
- twitter:card: 페이지(카드)의 유형(E.g. summary, player)
- twitter:site: 속한 사이트의 이름
- twitter:title: 페이지의 이름(제목)
- twitter:description: 페이지의 간단한 설명
- twitter:image: 페이지의 대표 이미지 주소(URL)
- twitter:url: 페이지 주소(URL)

## 실습
```html
<head>
  <title>Starbucks Coffe Korea</title>
  
  <meta property="og:type" content="website" />
  <meta property="og:site_name" content="Starbucks" />
  <meta property="og:title" content="Starbucks Coffee Korea" />
  <meta property="og:description" content="스타벅스는 세계에서 가장 큰 다국적 커피 전문점으로, 64개국에서 총 23,187개의 매점을 운영하고 있습니다." />
  <meta property="og:image" content="./images/starbucks_seo.jpg" />
  <meta property="og:url" content="https://starbucks.co.kr" />

  <meta property="twitter:card" content="summary" />
  <meta property="twitter:site" content="Starbucks" />
  <meta property="twitter:title" content="Starbucks Coffee Korea" />
  <meta property="twitter:description" content="스타벅스는 세계에서 가장 큰 다국적 커피 전문점으로, 64개국에서 총 23,187개의 매점을 운영하고 있습니다." />
  <meta property="twitter:image" content="./images/starbucks_seo.jpg" />
  <meta property="twitter:url" content="https://starbucks.co.kr" />
</head>
```


---------------------------------------------------------------------
# Ch10-03. 시작하기 Google Fonts
[Google Fonts](https://fonts.google.com/)

## 사용법
- Nanum Gothic
```html
<link rel="preconnect" href="https://fonts.gstatic.com" />
<link href="https://fonts.googleapis.com/css2?family=Nanum+Gothic:wght@400;700&display=swap" rel="stylesheet" />
<link rel="stylesheet" href="./css/main.css" />
```
```css
font-family: "Nanum Gothic", serif;
```  


---------------------------------------------------------------------
# Ch10-04. 시작하기 Google Material Icons
[Google Material Icons](https://fonts.google.com/icons)

## 사용법: 이전 버전 Icons
```html
<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons" />
```
```html
<div class="material-icons">upload</div>
<div class="material-icons">
  search
</div>
```


---------------------------------------------------------------------
# Ch10-05. 헤더와 드롭다운 메뉴 - 로고
헤더 구성하기
## 헤더 - 로고
```html
<body>

  <!-- HEADER -->
  <header>
    <div class="inner">

      <a href="/" class="logo">
        <img src="./images/starbucks_logo.png" alt="STARBUCKS" />
      </a>

    </div>
  </header>

</body>
```
- header 태그 추가: 기능은 없지만, 의미적으로 구분

```css
/* COMMON */
body {
  color: #333;
  font-size: 16px;
  font-weight: 400;
  line-height: 1.4;
  font-family: "Nanum Gothic", serif;
}

img {
  display: block;
}


/* HEADER */
header {
  background-color: royalblue;
}
header .inner {
  width: 1100px;
  height: 120px;
  margin: 0 auto;
  background-color: orange;
  position: relative;
}
header .logo {
  height: 75px;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  margin: auto;
}
```
- `이미지 요소 가운데 정렬`
> - 부모 position: relative, 요소 position: absolute
> - 요소의 height 지정 > margin: auto, top/bottom의 거리 기준점
> > 가로 저열의 경우 left/right + margin: auto


---------------------------------------------------------------------
# Ch10-06. 헤더와 드롭다운 메뉴 - 서브



---------------------------------------------------------------------
# Ch10-07. 헤더와 드롭다운 메뉴 - 검색


---------------------------------------------------------------------
# Ch10-08. 헤더와 드롭다운 메뉴 - 메인 메뉴(1)


---------------------------------------------------------------------
# Ch10-09. 헤더와 드롭다운 메뉴 - 메인 메뉴(2)


---------------------------------------------------------------------
# Ch10-10. 헤더와 드롭다운 메뉴 - BEM


---------------------------------------------------------------------
# Ch10-11. 헤더와 드롭다운 메뉴 - 전역 배지(GSAP)(1)


---------------------------------------------------------------------
# Ch10-12. 헤더와 드롭다운 메뉴 - 전역 배지(GSAP)(2)


---------------------------------------------------------------------
# Ch10-13. 순차적 스타일 애니메이션 - 전역 버튼 스타일(1)


---------------------------------------------------------------------
# Ch10-14. 순차적 스타일 애니메이션 - 전역 버튼 스타일(2)


---------------------------------------------------------------------
# Ch10-15. 순차적 스타일 애니메이션 - 순차적으로 요소 보이기


---------------------------------------------------------------------
# Ch10-16. 요소 슬라이드 - 공지사항


---------------------------------------------------------------------
# Ch10-17. Swiper.js - 라이브러리 버전 확인하기


---------------------------------------------------------------------
# Ch10-18. 요소 슬라이드 - 수직 슬라이드(Swiper)


---------------------------------------------------------------------
# Ch10-19. 요소 슬라이드 - 요소 가운데 배치


---------------------------------------------------------------------
# Ch10-20. 요소 슬라이드 - 프로모션 이미지 슬라이드(1)


---------------------------------------------------------------------
# Ch10-21. 요소 슬라이드 - 프로모션 이미지 슬라이드(2)


---------------------------------------------------------------------
# Ch10-22. 요소 슬라이드 - 슬라이드 영역 토글


---------------------------------------------------------------------
# Ch10-23. 유튜브 영상 배경 - 리워즈


---------------------------------------------------------------------
# Ch10-24. 유튜브 영상 배경 - Youtube iframe API(1)


---------------------------------------------------------------------
# Ch10-25. 유튜브 영상 배경 - Youtube iframe API(2)


---------------------------------------------------------------------
# Ch10-26. 유튜브 영상 배경 - 반복 애니메이션


---------------------------------------------------------------------
# Ch10-27. 고정 이미지 배경


---------------------------------------------------------------------
# Ch10-28. 3D 애니메이션


---------------------------------------------------------------------
# Ch10-29. 스크롤 위치 계산 애니메이션(1)


---------------------------------------------------------------------
# Ch10-30. 스크롤 위치 계산 애니메이션(2)


---------------------------------------------------------------------
# Ch10-31. 다중 요소 슬라이드


---------------------------------------------------------------------
# Ch10-32. 푸터


---------------------------------------------------------------------
# Ch10-33. 페이지 상단으로 이동(ScrollTo)

# css header 영역

## 1. html 태그 작업

### 1.1. anchor 태그

- `<a href="보여줄 페이지 주소">글자</a>`
- `<a href="보여줄 페이지 주소">그림</a>`
- `<a href="보여줄 페이지 주소" target="_blank">네이버</a>`
  - 새 탭으로 보여주기 (`target="_blank"`)

### 1.2. img 태그

: 파일명.jpg, 파일명.png, 파일명.gif, 파일명.svg
: 팁 1. 1순위 png (고화질, 배경투명)
: 팁 2. 프론트엔드는 .WebP (Next.js 기본)
: 상식. .gif 는 여러장의 이미지를 일정한 시간으로 교체하면서 보여주는 파일.

- `<img src="경로/파일명.확장자" />`
- `<img src="경로/파일명.확장자" alt="이미지설명" />`
- alt="이미지설명" 이미지가 없을시 이미지대신 이미지 설명이 보여진다.

### 1.3. 목록 태그 (`ul, li`)

- 필수입니다.
- 판단하실 때 레이아웃이면 div, 내용이 동일한 형태면 ul, li

## 2. CSS 선택자

- 범위 안쪽에 있는 태그 찾기

```css
.header-logo-slide img {
  ....;
}
.header-logo-slide a {
  ....;
}
```

### 2.2. display 간단 이해

- 신규프로젝트는 적극적으로 `display: flex;` 를 활용
- 유지, 보수 프로젝트는 `display: inline, display: inline-block`을 조심하세요.

```text
//적극적으로 사용
display: block; 하나의 층

//사용하지마세요
display: inline; 은 width height margin padding 거의적용안됨

//아주가끔쓰는데 엔터키 공백이 들어감을 알고있어야함.
//inline은 엔터(공백)도 영역으로 인식 <div></div><div></div>이렇게 연결해서 사용
display: inline-block; 은 width height margin padding 줄수있음

//적극사용, 자주활용, 이모든걸 해결해준다.
display: flex;
기능: inline 으로 만든다 - inline-block로 만든다 - 엔터키공백을 없애준다

//자주활용, display를 안보이게 하는기능
//display: none 은 css로 초기 모양을 설정하는 부분에 오류발생 소지가 있다.
display: none;
```

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>레이아웃</title>
    <style>
      div,
      header,
      footer {
        border: 5px solid red;
      }

      main {
        display: none;
      }

      .community {
        display: flex;
      }
      .news {
        display: block;
        width: 25%;
        height: 400px;
      }
      .notice {
        display: block;
        width: 25%;
        height: 400px;
      }
      .banner {
        display: block;
        width: 25%;
        height: 400px;
      }
      .product {
        display: block;
        width: 25%;
        height: 400px;
      }
    </style>
  </head>
  <body>
    <!-- 전체 레이아웃 -->
    <div class="wrap">
      <!-- 상단 -->
      <header class="header">상단</header>
      <!-- 메인 -->
      <main class="main">
        <div class="slide">슬라이드</div>
        <div class="community">
          <div class="news">뉴스</div>
          <div class="notice">공지사항</div>
          <div class="banner">배너</div>
          <div class="product">제품소개</div>
        </div>
      </main>
      <!-- 하단 -->
      <footer class="footer">하단</footer>
    </div>
  </body>
</html>
```

### 2.3. flex 기초

- 관련사이트

  - https://codepen.io/enxaneta/pen/adLPwv
  - https://studiomeal.com/archives/197
  - https://flexboxfroggy.com/#ko

- container(상자) 용 flex

```css
.header-logo-link {
  display: flex;
  /* 세로 중앙 */
  align-items: center;
  /* 가로 왼쪽 정렬 */
  justify-content: flex-start;
  /* 가로 가운데 정렬 */
  justify-content: center;
  /* 가로 우측 정렬 */
  justify-content: flex-end;
  /* 가로 양쪽 균등 정렬 */
  justify-content: space-between;
  justify-content: space-around;
  /* 아이템과 아이템 사이의 여백 */
  gap: 30px;
}
```

- item용 flex

### 2.4. 글꼴

- 초기 디자인 및 css 작업은 글꼴에 대한 협의가 끝나고 진행한다. (1순위)
- [구글폰트](https://fonts.google.com/?query=inter) 검색 > [눈누](https://noonnu.cc/) 검색
- 존재하지 않는 경우 직접 폰트 생성진행

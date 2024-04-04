# CSS 기초

- html 은 화면에 보여줄 데이터(글자) 입니다.
- css 는 화면에 보여줄 데이터(html)를 보기 좋게 꾸며주는 역할을 합니다.

## 1. css 작성법 (4가지)

### 1.1. 인라인 방식 : html에 직접 적용

- <태그 style="이름 : 값">
- 가독성이 떨어진다.
- css 코드를 재활용 하는것이 불가능.

```html
<body style="background: green"></body>
```

### 1.2. &lt; style &gt; 태그 활용하기

- 가독성은 좋아요.
- css 코드 재활용은 어렵다.
- 선택자 { css 적용 } (선택자 : 선택의 대상)
- css Selector { css 적용 }

```html
<style>
  body {
    background: green;
  }
</style>
```

### 1.3. 외부파일로 css 분리하기

- 가독성 좋아요.
- css 코드 재활용 좋아요.
- 일반적으로 활용해요. (무조건 추천 !)
- css/common.css (확장자는 무조건 .css)

```html
<link rel="stylesheet" href="./css/common.css" />
```

### 1.4. css 에 css 파일 불러들여서 관리하기

- 대표적으로 글꼴을 @import 해서 사용

```css
@import url("https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@100..900&display=swap");
body {
  background: green;
}
```

- 참고사항
  : 프로그래밍 언어는 `;` 으로 문장의 끝을 표현한다.

## 2. css 초기화 하기

### 2.1. 선택을 하자. (코딩 컨벤션)

- https://necolas.github.io/normalize.css/8.0.1/normalize.css

- https://meyerweb.com/eric/tools/css/reset/reset.css

- 우리가 만든 common.css도 링크하자.

```css
@charset "utf-8";
* {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  /* 옵션 */
  /* outline-style: none; */
}
html {
  font-size: 16px;
}
body {
  color: #000000;
}
.wrap {
  width: 1170px;
}
```

: 꼭 기억하자.
`box-sizing: border-box;` (지정 영역(px) 더 넓어지는것을 방지)
: 필요시 기억하자
`outline-style: none;`

- 정말 중요한 것은 css 코드 배치 순서
  : html 적용 이후 class 적용
  : html 태그 > .class > #id 의 순서로 적용됨
  (html - class - id - !important;)
  : 만약 같은 종류라면 작성 순서 기준
  : 가장 우선시 한다면 `!important;`

## 3. css 로 전체 레이아웃에 적용해 보기

### 3.1. 멘토 및 실무자는 반드시 반응형을 봅니다.

- 화면(디바이스) 너비 관례상 기준
- 기본 화면(1280px 이상)을 먼저 작업한다.

```css
.warp {
  width: 95%
  max-width: 1280px;
  margin: 0 auto;
}
```

- 랜탑 화면(1024px)의 레이아웃을 작업한다.

```css
@media screen and (max-width: 1024px) {
}
```

- 타블렛 화면(960px)의 레이아웃을 작업한다.

```css
@media screen and (max-width: 960px) {
}
```

- 고해상도 모바일 화면(760px)의 레이아웃을 작업한다.

```css
@media screen and (max-width: 760px) {
}
```

- 중해상도 모바일 화면(480px)의 레이아웃을 작업한다.

```css
@media screen and (max-width: 480px) {
}
```

- 저해상도 모바일 화면(320px)의 레이아웃을 작업한다.

```css
@media screen and (max-width: 320px) {
}
```

: 완성된 예

```css
.wrap {
  width: 95%;
  max-width: 1280px;
  margin: 0 auto;
}
@media screen and (max-width: 1024px) {
}
@media screen and (max-width: 960px) {
}
@media screen and (max-width: 760px) {
}
@media screen and (max-width: 480px) {
}
@media screen and (max-width: 320px) {
}
```

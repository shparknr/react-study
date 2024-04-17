# css 최적화

# js Syntax 1장

1. Syntax (구문) : 약속된 문법

2. Interpreter (번역 ) : 갤럭시 AI/웹브라우저

3. 프로그래밍은 요구사항을 분석하고, (개인별로 작성 : 의사코드 )
   Syntax 를 이용해서
   적절한 자료구조 + 적절한 함수를 활용하고,
   흐름을 제어하여 요구사항을 만족 시킨다.

# js Syntax 코드 위치

1. inline 방식

```html
<div class="wrap" onclick="alert('안녕');"></div>
```

2. 태그 방식

```html
<script>
  alert("반가워");
</script>
```

3. 외부파일 방식

```html
<script src="./js/script.js">
  alert("반가워"); // 실행안됨, 외부파일에 의해 덮어 씌워짐
</script>
```

# Swiper Slide 적용해 보기

- Slide를 직접 코딩하지 마세요.
- 사용법을 배운다.
- [Swiper](https://swiperjs.com/), [Slick](https://kenwheeler.github.io/slick/), [BxSlider](https://bxslider.com/) 가 있어요.
- Swiper 많이 쓰는이유 1. react 지원 2. 터치 지원 3. 반응형 지원

## 1. Swiper 슬라이드 적용시 주의 사항

- (html 컨트롤 시 주의사항)
- html 로드 완료 및 이미지 로드 완료 후 실행 권장.

```js
window.addEventListener("load",funtion(){
    // 실제 슬라이드 코드 배치하자.
});
```

# js 2장

```txt
[javascript가 뭐지?]

publisher : 웹브라우저용 프로그래밍언어 (html,css다룸)
frontend : node.js (웹브라우저용 프로그램 아니고, pc용 프로그래밍언어) 서버 (dothome... db... htmml... css...)

ex) mp3 실행하려면? mp3 player
    .hwp 실행하려면? 한글
   자바스크립트 실행하려면 웹브라우저, pc


웹 브라우저 player 마다 다 다르다
IE , Chrome, Opera, Safari 모두 다 다르다 (Syntax ,문법)
: 메뉴 하나를 만들어도 다시 각각의 웹브라우저에 맞게 마이그레이션을 해야 했었다


[ES6]


[렌더링]

 SSR (Server Side Rendering)
: 완성품으로 만들어서 주는것
: 플렛폼에는 php, spring(WAS), Next.js 등이 있다.

 CSR (Client Side Rendering) 이 있어요.
: 접속한 웹브라우저에 조립(html,css,js)하여 주는것
: 플렛폼에는 React, Vue, Angula 등이 있다.

- 렌더링의 목표는 html, css, js로 문서 만들기


[AJax] : 아작스, 에이젝스
        : 데이터(json: javascipt object notation) 통신

- 비 동기 (Request 요청 - Response 회신)

- 동기

동기와 비동기 구분할줄 알아야한다.

ex)택배 배달 택배올때까지 기다림 동기
            딴짓하다가 택배받음 비동기



- XML HttpRequest (XHR 통신)
XML : html 태그라고생각
Http :  웹브라우저
Request : 요청
(F12- network - response)


- vanila JS / pure JS (fetch/async await)<=====> jQuery (ajax)
: XHR 통신할때 무었을 쓰나 (괄호안에것 쓴다)

- jQuery
: 웹브라우저마다 문법이 다다른데 코딩한번에 모든웹브라우저 호환을 맞춰준다.

- Node.js 하실수 있나요? = 서버(Express.js), DB(MongoDB, Mysql) 구축 가능합니까?

- SPA : Single Page Application (1장의 html)

- CBD : Component based Development
         (Component: 재사용가능한 모듈(코드묶음)))

// - ECMAScirpt (ES6이상의 자바스크립트)
: 클라이언트 사이드 API / Web API //

- 자바스크립트의 특징
1. 객체 지향 :  모든코드의 시작은 객체로 설계하여 전개한다.

ex)  기획자  : xls로 제공한다.

              - 인터파크 상품 (최상단에 배치되는 제품의 정보를 노출)

              - 상품의 기본정보
                : 할인율, 가격, 제목, 이미지 를 보여주면 되겠다
                : 제품상세 정보로 이동하는 경로를 제공

     디자이너  : UI 및 UX 배치

    BE 개발자  : 제품의 정보를 DB에 저장해둠 (일부만 Response)

    FE 개발자  :

      const Good = {
           ratio : 할인율,
           prics : 가격,
             itle : 제목,
             pic : 이미지주소,
             link : 제품주소,
         }

       const 객체명 = {
          속성명 : 속성값
            기능 : function ( ) { 기능 }
        }

? 여기서 프로퍼티와 메소드는뭔가?

? 컴포넌트는 객체인가? O

function go() {
}

div {
}
둘다 객체다.. (중괄호 열고닫는것은 객체..)

? 객체에는 정보와 기능이 있다.

2. 프로토타입 기반 :  프로토타입(유전자)를 상속받아 덧댄다.



- Babel이란?
: 현재 최신코드를 옛날 코드로 변환해 준다.
```

# Swiper Slide 적용해보기 2.

- 데모사이트의 core 메뉴를 통해서 참조한다.
- 기본 css와 js 파일은 CDN 으로 참조한다.

```html
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css"
/>
<script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
```

- 기본형 코드를 작성해서 원하는 영역에 배치한다.
- (`원하는 이름`과 `내용` 이외 변경금지.)
- 슬라이드 개수만큼 swiper-slide div를 만든다.

```html
<div class="swiper 원하는이름">
  <div class="swiper-wrapper">
    <div class="swiper-slide">내용</div>
    <div class="swiper-slide">내용</div>
    <div class="swiper-slide">내용</div>
  </div>
</div>
```

- css로 `원하는 이름` 을 찾아서 width, height를 100% 주자.
- css로 `원하는 이름` 에 절대로 display 등을 넣으면 안돼요.

# Swiper Slide 적용해 보기 3.

- 외부 데이터 연동(json)
- 데이터의 구조를 설계
- json이란 javaScript Object Notation 입니다.

```json
[
  { "키" : 값, "키":  값,       "키":  값 },
  { "id": 1, "pic": "b1.png", "url": "#" },
  { "id": 2, "pic": "b2.png", "url": "#" },
  { "id": 3, "pic": "b3.png", "url": "#" },
  { "id": 4, "pic": "b4.png", "url": "#" }
]
```

# Swiper Slide 적용해 보기 4.

- 비동기 호출하기 (vanila/pure js)
  - BE와 협업시 활용합니다.
- fetch를 활용가능
- asyn await 활용 가능

# js 3장

```txt
    DOM(Document Object Model)
   - html 을 읽고, 수정 등등의 조작을 하는
     함수 (DOM API)
     예 . document.querySelector(".wrap")

    클라이언트 사이드 API
    DOM, BOM, Canvas, XMLHttpRequest, fetch
    requestAnimationFrame, SVG, Web Storage,
    Web Component, Web Worker 등..

    Node.js   설치를 하면 자동으로
    npm 설치 됩니다. Node Package(js 소스) Manager
    https://www.npmjs.com/

    npm install 패키지명@버전
    node -v
    npm -v

    nvm (Node.js 의 버전을 자유롭게 변경하고, 설치)

    yarn install 패키지명@버전
```

# Swiper Slide 적용해 보기 5.

- 외부 js 파일을 이용한다.

```html
<script src="./js/파일명.js"></script>
```

```js
window.addEventListener("load", function () {
  //내용작성;
});
```

- swiper 에 보여줄 데이터를 외부 .json 파일로 연동한다.
  - 자료(데이터)를 만들어주는 동료가 BackEnd 입니다.
  - BE 와 협의가 필요하다. (협업의 기본)
  - 초기에는 가짜데이터(Dummy, Mockup) 을 가지고 작업

```json
[
  { "키명": "키값" }
  { "키명": "문자열" },
  { "키명": 숫자},
  { "키명": true},
  { "키명": []},
  { "키명": {} }
]
```

```json
[
  {
    "id": 1,
    "pic": "b1.png",
    "url": "#",
    "title": "AI 헬스케어의 <br/> 마일스톤을 찍다"
  },
  {
    "id": 2,
    "pic": "b2.png",
    "url": "#",
    "title": "카카오브레인의 <br/> 연구문화"
  },
  {
    "id": 3,
    "pic": "b3.png",
    "url": "#",
    "title": "PathFinder 2기의 <br/> 언어모델 활용기"
  },
  {
    "id": 4,
    "pic": "b4.png",
    "url": "#",
    "title": "칼로리의 꿈 <br/> 시리즈 ③"
  }
]
```

- json 데이터를 이용해서 자료를 추출한다.

  - 외부 주소를 통해서 자료를 불러들이기 위해 fetch를 알고 적용한다.
  - 더불어서 크롬 개발자 도구 (F12)의 NetWork 탭을 알아야 한다.
  - 옵션으로 Fetch/XHR을 선택할 수 있어야 한다.
  - request 와 response를 구별하여 파악할 수 있어야 한다.

```js
fetch("주소").then().then().catch();
```

```js
fetch("주소").then(function (결과)=>{접속결과}).then().catch();
```

```js
fetch("주소")
  .then((결과) => {
    const 접속결과 = 결과.json();
    return 접속결과;
  })
  .then(() => {})
  .catch(() => {});
```

```js
fetch("주소")
  .then((결과) => {
    const 접속결과 = 결과.json();
    return 접속결과;
  })
  .then(function (최종자료) {
    // 하고 싶은 일 마음대로....
    // 우리가 할 일을 진행한다.
  })
  .catch();
```

```js
fetch("주소")
  .then((결과) => {
    const 접속결과 = 결과.json();
    return 접속결과;
  })
  .then((최종자료) => {
    // 하고 싶은 일 마음대로....
    // 우리가 할 일을 진행한다.
  })
  .catch((오류) => {
    // 오류처리
  });
```

- 추출된 데이터로 html 을 생성한다.
  - 백틱(``)을 적극적으로 사용한다.

```js
let slideTags = "";

for (let i = 0; i < result.length; i++) {
  const data = result[i];
  // 템플릿 문법 필요 (html)
  const test = `<div class="swiper-slide">
          <a href="${data.url}" style="background:url('./images/${data.pic}') no-repeat center; background-size: cover;">
            <p class="slide-title">
              ${data.title}
            </p>
          </a>
        </div>`;
  slideTags = slideTags + test;
}
```

- html 을 배치한다.

```js
// 원하는 장소에 출력해 보자.
const whereTag = document.querySelector(".topslide .swiper-wrapper");
whereTag.innerHTML = slideTags;
```

- swiper 를 작동시킨다.
  - html 배치 완료 후 슬라이드 생성하자

```js
// DOM (html)을 다루려고 하는 목적인 경우
// 랜더링 이후 작동
window.addEventListener("load", function () {
  // 1. 외부에서 자료를 불러온다.
  const dataUrl = "./apis/topslide.json";

  fetch(dataUrl)
    .then((response) => {
      // Step 1. 자료 받아서 json 변경하기
      // 토큰을 js의 데이터로 변경하기
      const data = response.json();
      // 변환된 결과를 돌려주기
      return data;
    })
    .then((result) => {
      // Step 2. json 변경된 데이터 활용하기
      // 전체 글자 모음
      let slideTags = "";

      for (let i = 0; i < result.length; i++) {
        const data = result[i];
        // const data = {id: 1, pic: "png"}
        // 템플릿 문법 필요(html)
        const test = `<div class="swiper-slide">
          <a href="${data.url}" style="background:url('./images/${data.pic}') no-repeat center; background-size: cover;">
            <p class="slide-title">
              ${data.title}
            </p>
          </a>
        </div>`;
        slideTags = slideTags + test;
      }
      // 2. 자료를 이용해서 슬라이드에 배치할 html을 만든다.
      // 원하는 장소에 출력해 보자. DOM API 사용 document.querySelector();
      const whereTag = document.querySelector(".topslide .swiper-wrapper");
      whereTag.innerHTML = slideTags;
      // 3. html 완성후 swiper를 생성한다.
      // Swiper 기본코드를 넣어보자. *위치 중요
      var topSlide = new Swiper(".topslide", {});
    })
    .catch((error) => {});
});
```

# Swiper Slide 적용해 보기 6.

- [슬라이드 옵션](https://swiperjs.com/demos)
  - loop
  - autoplay
  - effect
  - speed
  - [pagenation](https://swiperjs.com/demos#pagination)
  - 페이지네이션 디자인 수정하기 참조

```css
.bannerslide .swiper-pagination {
  bottom: 30px !important;
}
.bannerslide .swiper-pagination-bullet {
  width: 4px !important;
  height: 4px !important;
  background: #ffffff !important;
  opacity: 0.7 !important;
  border-radius: 4px !important;
  transition: width 0.3s;
  margin: 0 2px !important;
}
.bannerslide .swiper-pagination-bullet-active {
  background: #ffffff !important;
  opacity: 1 !important;
  width: 20px !important;
}
```

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

# js 4장

- 호이스팅 (hositing) 은 변수, 함수를 선언하지 않았는데도 사용할수 있음.
- hositing이 일어나지 않도록 주의 (var는 안쓰는게 좋다.)
- var 변수명 = 변수값;
- let 변수명 = 변수값;
- const 변수명 = 변수값;

```txt
4장

어플리케이션은 데이터를 다루는 것이다.
프로그램은 데이터를 다루는것이다.
Create, Read, Update, Delete
데이터를 CRUD 하기위해 필요한것이 변수입니다.


변수 (Variable) :
하나의 값을 저장하기 위해 메모리공간 자체/ 메모리 공간 구분하기위해 이름을 붙인 것을 Syntax에서 변수 라고 합니다.

값의 위치를 가리키는 상징적인 이름(단어)이다.



컴퓨터에는 메모리(아파트)라고 하는 부품이 있어요.
메모리(아파트) 에는 각 층별로 정말 많은 Room이 있어요.








10

각 방에 이름표가 붙어있습니다 (메모리 주소 ex) 0x03000123340910238)
각 방에 이름표가 붙어있습니다 (메모리 주소 ex) 0x03000123340910238)

각 방에 이름표가 붙어있습니다 (메모리 주소 ex) 0x030001233409102382084810283) : 내가 아는 단어를 붙여서 (이름표(식별자)를 붙혀서) 보관할 수 있다.
   ->'나이'라는 이름표(식별자)를 붙여둔다 (메모리 주소에다가)
   -> 나이라고 이름표(식별자)를 붙여둔 메모리방에다가 10을 보관해줘

각 방에 이름표가 붙어있습니다 (메모리 주소 ex) 0x03000123340910238)
각 방에 이름표가 붙어있습니다 (메모리 주소 ex) 0x03000123340910238)
각 방에 이름표가 붙어있습니다 (메모리 주소 ex) 0x03000123340910238)
각 방에 이름표가 붙어있습니다 (메모리 주소 ex) 0x03000123340910238)




변수선언

ES5
var 나이;
==========
ES6 (ECMAScript)
let 나이2;
const 나이3;


호이스팅(hoisting) 은 변수를 선언하지 않았는데도 사용할수 있어요.
                           변수를 선언하지 않았는데도 에러없이 실행됨.


< ES5코드  >

var 나이;
console.log(나이)


호이스팅발생 (변수호이스팅, 함수호이스팅)
console.log(나이)
gogo();

var 나이;
function gogo(){}


---------------
<ES6(ECMAScript)코드>
호이스팅 발생하지만 에러 띄워준다.
let 나이;
const 나이;

var age;
이거보다는
var age = 0;
var age = "";
초기값 숫자=0, 문자=""이라도 지어놓는게 낫다.
```

# css의 opacity와 position의 이해.

- opacity 는 DOM의 내용까지도 투명도가 적용된다.

  - 반투명 (내용도 반투명) > opacity: 0~1;
  - 배경 반투명 내용은 그대로 사용하려면 > rgba (255,0,0,0.3)사용

- position
  - position 중에 absolute 로 픽셀 위치 설정의 경우 주의
  - absolute 사용 시 반드시 position 코드가 바깥 영역에도 있어야 합니다.
  - position 중에 fixed 는 웹브라우저를 기준으로 배치
  - fixed는 반드시 left, top, right, bottom 을 주자
  - fixed 는 보통 z-index를 준다.
  - fixed 는 높이에 반영이 안되므로 주의하자.(레이아웃 배치문제)

```css
대상 {
  position: relative;
}
대상 {
  position: absolute;
}
대상 {
  position: fixed;
}
```

- 주의하자

```css
.box-wrap {
  position: relative;
  margin: 0 auto;
  width: 600px;
  height: 300px;
  background: orange;
}
.box {
  position: absolute;
  right: 80px;
  bottom: 20px;

  width: 200px;
  height: 200px;
  background: red;
}
```

# js 윈도우 스크롤의 위치를 알아내기

```js
window.addEventLinstenr("scoll", function () {
  // 하고 싶은 일
});
```

```js
window.addEventLinstenr("scoll", function () {
  // 스크롤바의 위치
  const scY = window.scrollY;
});
```

# js 로 css 의 클래스 동적으로 활용하기

```js
// DOM 찾아서 변수로 레퍼런스 하기
const tags = document.querySelector(".클래스명");
// DOM 을 이용해서 선택한 곳에 적용된 css 클래스 목록 추가
tags.classList.add("클래스명");
// DOM 을 이용해서 선택한 곳에 적용된 css 클래스 목록 제거
tags.classList.remove("클래스명");
// DOM 을 이용해서 선택한 곳에 적용된 css 클래스 목록 추가 / 제거
tags.classList.toggle("클래스명");
// DOM 을 이용해서 선택한 곳에 적용된 css 클래스 목록 포함여부
tags.classList.contain("클래스명");
```

# js 의 함수란 ? 1번

- 동일한 코드가 2번 이상 반복되면 함수를 만들려고 노력하자.
- 반복은 되지 않더라도 하나의 기능이 너무 복잡하면 함수를 만들려고 노력하자.
- 복잡하지는 않는데 코드가 너무 길어지면 함수로 묶어주려고 노력하자.
- 실행의 결과가 그때, 그때 다른 경우에도 함수를 만들자.

```js
// 함수만들기(함수선언)
function 적절한동사() {
  // 하고 싶은 일 작성 ....
}
// 함수사용하기(함수호출)
적절한동사();
// 예 (함수 체이닝)
fetch().then().then().catch();
```

- 함수는 무조건 1개의 값을 리턴하도록 규정되어 있습니다.
- 리턴이라는 것은 함수 실행() 후 값을 돌려주는 것을 말합니다.

```js
function 함수명() {
  // 몰래 작성됨 return undefined;
}
함수명();
```

# js 5장

```txt
이 책을 읽기 위한 중요한 단어가 많이나와요

값 (value)
: 표현식이 평가(식을 해석해서 값을 생성하고 참조하는 것)된 결과를 말한다.

: 변수에 할당된 결과를 말한다.

…변수란? : 컴퓨터 공간에 이름을 붙여둔 방 한개

리터럴 (literal)

: 사람이 이해할 수 있는 문자 또는 약속된 기호를 사용해서 값을 생성하는 표기법

: 리터럴은 값을 평가해서 코드에 활용하기 위한 문법

function goog (){} / 사람이  function gogo (){} 이라고 적으면 컴퓨터는 리터럴과정을 통해 함수로 평가해서 보관

표현식 (expression)

조건 : 반드시 리터럴과정으로 거쳐서 값을 보관할 수 있어야함

: 리터럴 값으로 평가가 되면 OK!

5 , 숫자 리터럴 값으로 평가가되면 OK!

“안녕” 문자열 리터럴 값으로 평가가되면 OK!

문 (statement)

: 프로그램을 구성하는 기본단위 / 최소 실행단위

var foo = x = 100 (평가가 끝나면  100,  표현식 O)
```

# js 의 함수란 ? 2번

- 동일한 코드가 2번 이상 반복되면 함수를 만들려고 노력하자.
- 반복은 되지 않더라도 하나의 기능이 너무 복잡하면 함수를 만들려고 노력하자.
- 복잡하지는 않는데 코드가 너무 길어지면 함수로 묶어주려고 노력하자.
- 실행의 결과가 그때, 그때 다른 경우에도 함수를 만들자.

- 함수 정의문

```js
function 함수이름() {
  //할일
}
```

- 함수 실행/호출(call)문

```js
함수이름();
```

# js 의 함수의 매개변수란 ? 3번

- 초기 기능 즉, 함수를 정의하기 전에 기능상 자주 변하는 데이터를 고민한다.
- 기능은 스크롤시 특정 위치보다 커지면 css 추가하기
- 이전 코드는 좋지 않은 코드라고 생각이 든다.
- 함수는 스스로 지역 즉, Local 영역(Scope) 에서 `처리`되는것이 좋다고 봐요.
- `처리`라는 말은 변수를 찾는다 던가
- `처리`라는 말은 잘못된 값이 전달 되어서 오류가 나는것을 방지하는 것을 말합니다.

```js
// 홍길동에게 줄 함수
const a = 5;
const b = 0; // {지역변수}바깥 글로벌 변수에서 a,b 찾아보니깐 있다
function 나누기() {
  return a / b; // {지역변수 내에서 a,b 를 찾아보니없다}
}
나누기();
```

```js
// 함수에서 일반변수로 접근하는것은 좋지않다 . 매개변수로 접근하자
const a = 5;
const b = 0;
function 나누기(_num1, _num2) {
  if (_num2 === 0) {
    alret("나눗셈에서 0은 안됩니다.");
  }
  return _num1 / _num2;
}
나누기(a, b);
```

# js 6장

```txt
   데이터 타입 ( Data Type ) : 자료형
   타입 이라는 말이 자료의 형태
   JS의 리터럴로 처리될 수 있는 자료의 종류

   타입 스크립트 : 데이터 종류를 표현해 주는 방식

    '5'   , "55", `555`
    'a'   , "ab", `55555`

    "안녕
      반가워
    "
    `안녕 ${100}
      반가워
    `

    undefined 와  null 헷갈려요.
    const a = undefined; (모르겠다.)
    const b = null; (개발자가 직접 진짜 값이 비었다고 알려줌)

    Symbol 은 중복되지 않는다고 보장하는 값 타입
    Symbol()

    데이터 타입 ( Data Type ) : 자료형
    불변성(immutable) : 데이터 값이 변경될 수 없다.
    데이터는 immutable 해야 합니다.
    상태는   immutable 해야 합니다.
    state는  immutable 해야 합니다.

    1 = 1;


    가변성(mutable) : 데이터 값이 변경될 수 있다.


    원시데이터 6가지가 있는데 immutable 한 데이터 타입입니다.

    number   1
    string   'a'
    undefined undefined
    boolean    true, false
    null       null
    symbol     Symbol() 만들어진 값은 변경 불가

     복합형 데이터 객체
     객체는 원시데이터를 모아서 저장하고 관리하는 것.

    // 묶어라, Block
    const hong = {
        age: 20,
        marry : true
     }


     // 내가 c 라는 이름으로 저장할 거야
     // c 라는 공간은 글자를 보관할 거야
     // 그러니, 공간을 좀 마련해 줄래?

     // C 를 사용하는 프로그래머는
     char c = 'a'
     int num = 5;

     // js 를 사용하는 프로그래머는
     const c = 'a';
     const num = 5;

     // ts 를 사용하는 프로그래머는
     const c:string = 'a';
     const num:number = 5;


     // 오늘, 그리고 다음을 위해서 꼭 알아야 하는 단어

     1. 데이터 타입 : 자료(리터럴 값)의 종류

     2. js 에서는 값 리터럴에 따라 변수의 종류를 타입추론 한다.

     3. 타입을 추측해서 프로그래머에게 물어보지않고 타입을 변경한다. (암묵적 타입변경)

        let a = 1;
        a = "안녕";

        2번 3번은 원하지 않는 결과를 언젠가 실행됩니다.
        의도하지 않은 오류를 일으킨다.

        TypeScript

        let a:number = 1;
        a = "안녕"; // 오류 발생

  // 코딩 할 때 스스로 고민해 보자.

   1. 꼭 필요한 경우인지를 파악하고 변수를 만들자.
   2. 변수 유효범위는 좁게 (블록을 가능하면 쓰자)
   3. 전역변수는 가능하면 만들지 말자.
   4. 변수는 상수를 쓰세요.

      let a = 1; (X)

      const count = 1;

      {
        let count = 2;
      }
```

# 함수의 이해 7번

1. 함수를 만들어야겠다고 판단하는 케이스

- 동일한 코드가 2번 이상 반복되면 함수를 만들려고 노력하자.
- 반복은 되지 않더라도 하나의 기능이 너무 복잡하면 함수를 만들려고 노력하자.
- 복잡하지는 않는데 코드가 너무 길어지면 함수로 묶어주려고 노력하자.
- 실행의 결과가 그때, 그때 다른 경우에도 함수를 만들자.

2. 왜 화살표 함수를 만들지?

- 트렌드
- 코드가 해석하기 더 어려워집니다.

: 함수에서 화살표 함수로 바꾸기. (매개변수가 없는경우)

```js
function say() {
  console.log("안녕", this);
}
```

: step 1.

```js
say() => {
  console.log("안녕", this);
}
```

: step 2.

```js
const say = () => {
  console.log("안녕", this);
};
```

: 함수에서 화살표 함수로 바꾸기. (매개변수가 있는경우)

```js
function say(_who) {
  console.log("안녕", _who, this);
}
```

: step 1.

```js
const say = (_who) => {
  console.log("안녕", _who, this);
};
```

- this를 정확히 지정하기 위해서 활용한다.
  - 화살표 함수를 사용하면 일반적으로 큰 고민없이 사용하면 됩니다.
  - 하지만, 함수 안에 this 를 작성하시면 상황이 달라집니다.
  - 화살표 함수에서 this는 window를 가르킵니다.
  - 결론은 화살표 함수에서 this를 사용한다면 console.log(this) 확인 필수!!
  - 화살표 함수는 예전 일반 함수에서 window를 참조하지 못하는 문제를 해결함.

```js
// this 의 차이(어렵지만 이해해야 해요.)
const btWrap = document.querySelector(".bt-wrap");
// 일반 함수는 this 가 타이핑이 된 곳을 가르킨다.
btWrap.addEventListener("click", function () {
  console.log(this);
});
btWrap.addEventListener("click", () => {
  console.log(this);
});
```

# 배열의 이해

- [요소, 요소, 요소, 요소]
  - 요소로 담을 수 있는 자료형은 7가지 입니다.
- 배열의 속성(배열을 위한 특별한 변수)은 1개가 있습니다.
  : length 가 있어요. (요소의 개수) (배열명.length)
- 배열의 메소드(배열을 위한 특별한 함수)는 너무 많아요.
- 상당히 많은 메소드(배열을 위한 함수)가 있습니다.
- 배열.forEach((요소)=>{}), 배열.map((요소)=>{}), 배열.filter((요소)=>{}), 배열.find((요소)=>{})
- 배열의 요소를 하나씩 접근해서 활용하기

- `배열.forEach()`

```js
result.forEach((item) => {
  const tag = `<a href=${item.link} class="list-box">
        <div class="list-box-img br-20" style="background: url('./images/${item.imgpath}') no-repeat center; background-size: cover"></div>
        <div class="list-box-cate">
          <img src="./images/icon/${item.icon}" alt="${item.category}" />
          <span style="color:${item.txtcolor};">${item.category}</span>
        </div>
        <p class="list-box-title">${item.title}</p>
        <span class="list-box-day">${item.day}</span>
        </a>`;
  allTag = allTag + tag;
});
```

# 프로젝트 생성

## 1. 기본사항
- 깃허브에 먼저 소문자로 프로젝트명을 만든다.
- 깃허브에 설명은 반드시 작성한다.
- PC에 동일한 소문자로 폴더를 만든다.

### 1.1. 리엑트 및 퍼블리싱 프로젝트 생성
- VSCode 를 실행한다.
- PC에 만든 폴더를 드래그해서 등록한다.
- 명령어를 통하여 기본 파일럿 프로젝트를 생성한다.
    :`npx create-react-app ./` 를 실행한다.
    : Node.js 권장 설치버전 (https://nodejs.org/en/download)
    : Node.js 는 v20.12.0(LTS) 버전을 선택하자.
    : 설치는 기본폴더 그대로 설치하자. 손대면 오류발생 가능
    : 
    : npm 오류가 발생했다. (npm ERR! errno -4058)
    : `npm uninstall -g create-react-app` -g : 사용PC(global)
    : `npm install -g create-react-app`
    : 위처럼 오류 발생 시 위의 사항을 실행하고 난 후 
    : `npm create-react-app ./` 를 실행한다.

### 1.2. 테스트 해보기
- `npm run start` 실행해서 확인한다.
- 터미널에서 `ctrl + C` 로 미리보기를 종료한다.

## 2. 작업순서 기준
### 2.1. 웹서비스 개발 순서 (프론트)
- 퍼블리싱부터 진행
- 리액트 진행 (필요시)
- 타입스크립트 진행 (필요시)
- Next.js 진행 (필요시)

### 2.2. 퍼블리싱 해보기
- 생성된 폴더 최상위를 `Root` 라고 부른다.
- 코드상으로 `Root`는 `/` 로 표현한다.
- 퍼블리싱은 `/public` 폴더에 `www` 폴더 생성 후 진행
- 퍼블리싱 기본 폴더 생성 진행
: images 폴더 생성 (.png, .jpg, .gif, .svg)
: css 폴더 생성 (.css 파일들을 보관)
: js 폴더 생성 (.js 파일들을 보관)
: assets 폴더 생성 (문서, 동영상, 디자인원본(.psd : 포토샵데이터),피그마 관련, 담당자 연락처 등)
: index.html 파일 생성

### 2.3. index.html 기본구성
- `! 누르면서 tab 키를 선택` 하면  html 기본형이 제공된다. (스냅샷 기능)
- lang="en" 은 "ko" 로 수정한다.
- 최소한 title 은 변경한다.
- html 파일에서 마우스 오른쪽 `open width live server` 선택
```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>카카오 브레인 블로그</title>
</head>
<body>
    
</body>
</html>
```

### 2.4. html 문서 작업 순서
- 디자인 레이아웃 보기

- https://chromewebstore.google.com/detail/gofullpage-full-page-scre/fdpohaocaechififmbbbbbknoalclacl?pli=1 
 : chrome 추가, 원하는 홈페이지 캡처 후 download image (png) 
 : 디자인 파일은 /public/www/assets 폴더에 보관

- html 의 태그의 활용 이전에 꼭 체크 해 보자.
 : https://caniuse.com/ 의심가면 확인 해 보자.

- 디자인을 살펴보고 영역을 구분하는 작업 진행
 : 레이아웃을 위한 영역 (div 태그)
 : 내용별 배치 영역 (`태그가 내용을 설명하는 시멘틱 태그 활용 추천`)

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>카카오브레인 Blog</title>
</head>
<body>
    <!-- 전체 레이아웃 -->
    <div class="wrap">
        <!-- 상단 레이아웃 -->
        <div class="header"></div>
        <!-- 메인 레이아웃 -->
        <div class="main"></div>
        <!-- 하단 레이아웃 -->
        <div class="footer"></div>
    </div>
</body>
</html>
```

- 아래 추천
```html
 <!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>카카오브레인 Blog</title>
</head>
<body>
    <!-- 전체 레이아웃 -->
    <div class="wrap">
        <!-- 상단 레이아웃 -->
        <header class="header"></header>
        <!-- 메인 레이아웃 -->
        <main class="main"></main>
        <!-- 하단 레이아웃 -->
        <footer class="footer"></footer>
    </div>
</body>
</html>
```

- 참고사항
: camelCase (카멜케이스)
: PscalCase (파스칼케이스)
: snake_case (스네이크케이스)

- div 구조를 이용해서 뼈대를 잘만드는 것이 실력입니다.
: `<div class="wrap">내용</div>` 무조건 기본

``` html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>카카오브레인 Blog</title>
  </head>
  <body>
    <!-- 전체 레이아웃 -->
    <div class="wrap">
      <!-- 상단 레이아웃 -->
      <header class="header">
        <!-- 상단 로고 -->
        <div class="header-logo"></div>
        <!-- 상단 메뉴 -->
        <div class="header-navi"></div>
      </header>
      <!-- 메인 레이아웃 -->
      <main class="main">
        <!-- 메인 상단 -->
        <div class="main-top">
          <!-- 슬라이드 -->
          <div class="main-top-slide"></div>
          <!-- 타이틀 배너 -->
          <div class="main-top-banner"></div>
        </div>
        <!-- 메인 하단 -->
        <div class="main-bottom">
          <!-- 메인 리스트 영역 -->
          <div class="main-bottom-list">
            <!-- 새글 리스트 -->
            <div class="main-bottom-list-news"></div>
            <!-- 배너 -->
            <div class="main-bottom-list-banner"></div>
            <!-- 추천글 리스트 -->
            <div class="main-bottom-list-picks"></div>
          </div>
          <!-- 메인 카드 영역 -->
          <div class="main-bottom-cards">
            <!-- 카드 슬라이드 -->
            <div class="main-bottom-cards-slide"></div>
          </div>
        </div>
      </main>
      <!-- 하단 레이아웃 -->
      <footer class="footer">
        <!-- 하단 사이트 정보 및 사이트 맵 -->
        <div class="footer-top">
            <!-- 회사소개 -->
            <div class="footer-top-info"></div>
            <!-- 사이트맵 -->
            <div class="footer-top-sitemap"></div>
        </div>
        <!-- 하단 카피라이터 및 SNS 링크 -->
        <div class="footer-bottom"></div>
            <!-- 카피라이터 -->
            <div class="footer-bottom-copyright"></div>
            <!-- SNS 목록 -->
            <div class="footer-bottom-sns"></div>
      </footer>
    </div>
  </body>
</html>
```

## 3. Git 기초
### 3.1. 깃으로 관리할거에요.(초기화) (한번만)
- `git init`

### 3.2. 깃으로 관리하는 파일을 추가해주기 (매일 퇴근전, 필요시)
- `git add .`    
 `.` : 모든파일


### 3.3. 깃으로 작업 내역을 기록해 둔다. (메모 매일 퇴근전, 필요시)
- `git commit`

### 3.4. 깃을 깃허브로 업로드 한다. (힌반만)
- `git remote add 이름 http주소`
: `git remote add origin https://github.com/shparknr/blog-kakaobrain-shparknr.git`
- `git remote -v` : 주소 설정 잘됐는지 확인

### 3.5. 깃을 깃허브로 push 후 퇴근한다. (매일 퇴근전, 필요시)
- `git push -u origin main`
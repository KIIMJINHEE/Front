# [한 번에 끝내는 프론트엔드 개발 초격차 패키지 Online.]

# 강의 노트에 없는 내용



### 개요, VS code, 무작정 시작하기, 웹에서 시작하기

- 웹 앱(웹 애플리케이션) = 웹 사이트 = 웹 페이지 = 홈페이지
- Plugin
  - Beautify : 자동정렬
  - auto : 앞 태그 입력 시, 자동으로 뒤 태그 동일하게 만들어 줌
  - live server : 개발을 위해 임시로 '로컬 서버' 오픈 하는 것

- 비주얼 스튜디오 코드 내 유용한 단축키 (*맥os 기준)
  - 빠른 열기(파일 or 기호 탐색) : Cmd(Ctrl) + P
  - 모든 명령 표시(에디커의 모든 명령에 접근) : Cmd(Ctrl) + Shfit + P
  - 현재 라인의 코드를 위/아래로 이동 : Opt(Alt) + Up/Down
  - 현재 라인의 코드를 위/아래로 복사 : Opt(Alt) + Shift + Up/Down
  - 들여쓰기 : Tab
  - 내어쓰기 : Shift + Tab
  - 현재 탭의 좌측 탭으로 이동 : Cmd + Shfit + [
  - 현재 탭의 좌측 탭으로 이동 : Cmd + Shfit + ]
  - 편집기 분할 : Cmd + \
  - 사이드바 열고, 닫기 : Cmd + B

- HTML, HEAD, BODY

  ```html
  <!DOCTYPE html>
  <html lang="en"> //HTML문서의 전체 범위
      <head> //HTML문서의 '정보'를 나타내는 범위. 웹브라우저가 해석해야 할 웹 페이지의 제목, 설명, 사용할 파일 위치, 스타일(CSS)같은 보이지 않는 정보를 작성하는 범위
  
      </head>
      <body> //사용자 화면을 통해 보여지는 문서의 '구조'를 나타내는 범위, 로고, 헤더, 푸터, 내비게이션, 메뉴, 버튼, 이미지 같은 웹 페이지의 보여지는 구조를 작성하는 범위.
  
      </body>
  </html>
  ```

- <head></head> : 정보를 의미하는 태그 살펴보기

  ```html
  <!DOCTYPE html>
  <html lang="ko">
  
  <head>
    <!--head : '정보', meta, title, link, script, style 태그 사용-->
  
    <!--meta : title, link, script, style 태그로 나타낼 수 없는 모든 정보 표현시-->
    <!--charset : 문자 코딩 방식-->
    <meta charset="UTF-8">
    <meta name="author" content="KJH">
    <!--name : 정보의 종류, content : 정보의 값-->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
    <!--title : 브라우저 탭 이름-->
    <title>Jinny's webApplication</title>
  
    <!--link태그 : 외부 문서(대부분 css파일)를 가져와 연결.-->
    <!--rel : 가져올 문서와 관계, href : 가져올 문서의 경로-->
    <link rel="stylesheet" href="./main.css">
  
    <!--script : 1. 자바스크립트(JS)를 가져오는 경우-->
    <script src="./main.js"></script><!--'./' : 주변-->
    <!--script : 2. 자바스크립트(JS)를 HTML 문서 안에서 작성하는 경우-->
    <script>
      console.log('Hello world!')
    </script>
  
    <!--스타일(CSS)를 HTML 문서 안에서 작성하는 경우에 사용-->
    <style>
      div {
        text-decoration: underline;
      }
    </style>
  </head>
  
  <body>
    <!--구조-->
    <div>Hello, world! </div>
  </body>
  
  </html>
  ```

- 화면에 이미지 출력하기

  ```html
  <body>
    <!--구조-->
    <div>Hello world! </div>
    <img src="./images/logo.png" alt="이미지를 불러옺 못하는 경우, 보여지는 '대체 텍스트'">
    <img src="https://heropy.blog/css/images/logo.png" alt="대체 텍스트2">
  </body>
  ```

  

- 상대경로 vs 절대 경로  
  - 상대 경로
    - ./ : '나' 기준 주변에서 탐색 시작 (생략가능***)
      - ex) ./images/logo.png = images/logo.png
    - ../ : 한 번 밖으로 나간 후 탐색 시작
  - 절대 경로
    - http(https)
    - /(//) : 루트 (최상위 경로 = '프로젝트 전체' 의미)
- http://127.0.0.1:5500 = http://localhost:5500
  - 우리 컴퓨터 내부의 5500 주소에서 우리의 프로젝트를 개발서버로 오픈한 것
  - 준포트 번호가 달라지면, 프로젝트도 달라질 수 있음

- 페이지를 나누고 연결(링크)하기
  - href (Hypertext Reference) : 다른 페이지로 이동하는 참조가 되는 '경로'를 입력하는 속성.
    - Hypertext = link

```html
<body
  <!--구조-->
  <a href="https://naver.com">Naver</a>
</body>
```

- 웹에서 HTML/CSS/JS 개발 시작하기

  - https://codepen.io/pen/
    - HTML/CSS/JS Prepropessor = 전처리도구

- CSS 기본 스타일로 초기화 : 
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reset-css@5.0.1/reset.min.css">

- 에밋(Emmiy) : HTML, CSS 를 작성할 때 빠른 코딩을 위해 사용하는 플러그인이다.

  

## HTML 개요

- <태그>Hello world!</태그> : '요소(Elements)', '태그' 혼용
- Hello world! : 요소의 내용(Contents)
- 

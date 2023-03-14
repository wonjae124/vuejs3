
# 0.install

- `sudo apt install nodejs`
- `sudo apt install npm`
- vue vs code extension
- 크롬 veu.js devtools 확장 설치
- `npm install -g bootstrap@next` : 부트스트랩5 전역설치 
- `npm install vue@next` : npm을 통해 기본 vue 설치. 관련 라이브러리는 프로젝트 코드들과 함께 컴파일 후 코드 축소(minify)를 해 결과물의 사이즈를 줄인다
- `npm init vite hello-world-vite2` : npm/vite를 이용한 기본 프로젝트 생성


- Bootstrap이란
  - 부트스트랩은 빠르고 쉬운 웹 개발을 위한 프론트엔드 프레임워크입니다.
  - 부트스트랩에는 typography, forms, buttons, tables, navigation, modals, image carousels 및 기타 여러 가지를 위한 HTML 및 CSS 기반 디자인 템플릿과 선택적 JavaScript 플러그인이 포함되어 있습니다.
  - 부트스트랩은 반응형 디자인을 쉽게 만들 수 있는 기능을 제공합니다.
 - 선언적 렌더링
    - Vue.js의 핵심은 간단한 템플릿 구문을 사용하여 데이터를 선언적으로 DOM에 렌더링 할 수 있다. 
    - `<div>` 태그 안에 {{변수명}} 와 같은 구문을 선언해서 html DOM 에 데이터를 전달하는 방식
    - Declarative(선언적으로) 라는 표현은 구체적인 처리는 사용자가 신경쓸 필요 없게 해서 목적에만 집중할 수 있게 해준다는 의미였네
 - DOM(Document Object Model)
    - '문서 객체 모델' 로 XML이나 HTML 문서에 접근하기 위한 일종의 인터페이스를 말하며 문서 내의 모든 요소를 정의하고 요소에 접근하는 방법을 제공한다
    - Webpack은 자바스크립트 모듈 번들러(Bundler)로, 자바스크립트로 작성된 모듈을 번들링하여 하나 혹은 여러개의 번들로 만들어주는 도구입니다.
    - 이외에도 변도의 플러그인을 통해 CSS번들링, 트랜스파일, Lint, 코드 난독화, 빌드 및 배포 등의 기능을 사용할 수 있다는 장점이 있습니다.

- `npm run dev` : package.json 내 script 속성에 명시된 vite가 npx를 통해서 실행 된다. 이후, vite는 개발 서버를 실행시켜 localhost:3000으로 접근하게 만든다.
  - index.heml 안의 div 태그 : Vue 컴포넌트들을 포함할 수 있는 루트 엘리먼트
  - package.json : 프로젝트 정보와 의존 패키지가 들어있음
  - package-lock.json : 공동 프로젝트에서 의존성 패키지의 버전이 동일해질 수 있도록 해줌
  - localhost:5173
  <img src = https://github.com/wonjae124/vuejs3/blob/main/image/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-03-14%2016-20-51.png width=400>

- main.js
  - 애플리케이션이 생성시 루트 컴포넌트로부터 만들어진다.

- npm
  - node package manager : 프로젝트에 필요한 javascript 패키지 관리

- vite
  - 비트
  - vue를 이용해서 만든 애플리케이션을 .html로 변경하기 위한 build tool로 사용
  - node.js 기반 vue 개발을 위한 scaffolding 도구
  - 여러 프론트엔드 프레임워크 지원
  - Native Es module, Hot module replacement등을 제공
-vite Alias
  
  - `npm install path` 경로 생성시 도움을 주는 path library
  - 각 파일의 경로를 모두 적어줘야하는 불편 해소
  - `npx vite -v` vite 버젼 체크
# 1. Vue3 기초
- CDN을 통한 Hello world 구현
- index.html로 저장 후 크롬에서 실행시, Hello Vue 3 CDN이라는 글자가 브라우저에 뜬다.
- 
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Hello Vue 3 CDN</title>
    <script src="https://unpkg.com/vue@next"></script>

    <style>
      .app {
        font-size: 3em;
      }
    </style>
  </head>
  <body>
    <div class="app">{{msg_hello}}</div>
    <!--App객체 생성, 변수명 : msg_hello -->
    <script>
      const App = {
        data() {
          return {
            msg_hello: "Hello Vue 3 CDN",
          };
        },
      };

      Vue.createApp(App).mount(".app");
    </script>
  </body>
</html>
```

### 출처

- [Declarative rendering](https://velog.io/@art11010/Vue-%EC%84%A0%EC%96%B8%EC%A0%81-%EB%A0%8C%EB%8D%94%EB%A7%81)
<br><br><br>


# 0.Install

- `sudo apt install nodejs`
- `sudo apt install npm`
- vue vs code extension
- 크롬 veu.js devtools 확장 설치
- `npm install -g bootstrap@next` : 부트스트랩5 전역설치 


### Bootstrap이란
- 부트스트랩은 빠르고 쉬운 웹 개발을 위한 프론트엔드 프레임워크입니다.
- 부트스트랩에는 typography, forms, buttons, tables, navigation, modals, image carousels 및 기타 여러 가지를 위한 HTML 및 CSS 기반 디자인 템플릿과 선택적 JavaScript 플러그인이 포함되어 있습니다.
- 부트스트랩은 반응형 디자인을 쉽게 만들 수 있는 기능을 제공합니다.


# 1. Vue3 기초
- CDN을 통한 Hello world 구현
- index.html로 저장 후 크롬에서 실행시, Hello Vue 3 CDN이라는 글자가 브라우저에 뜬다.
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

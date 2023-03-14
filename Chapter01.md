
# 0.Vue3 핵심 문법

## a) Single File Component(SFC)
- Vue의 컴포넌트를 하나의 파일로 나타내는 것
- 하나의 파일은 하나의 컴포넌트를 나타내므로 관리가 쉽게 코드가 간결해진다.
  - template : 컴포넌트가 렌더링되어야 하는 HTML 코드 부분. 템플릿 문법을 이용해 반응형 컴포넌트를 만들 수 있다
  - script   : 템플릿의 반응성 변수 조작. Js나 Ts 등을 이용해 스크립트 코드를 작성한다.
    - script setup과 같이 이용하면 LOC(Line of code)의 양을 획기적으로 줄일 수 있다. 아직 RFC 상태
  - style    : 컴포넌트 혹은 전체 프로젝트에 사용할 css코드 삽입
    - scoped를 이용하면, css가 특정 컴포넌트에만 적용된다. scope 없으면 전체 프로젝트에 적용됨.
## b) 컴포지션 함수 Setup
- 컴포지션 API를 이용해 컴포턴트를 만든다.
- 객체를 반환하는 함수, 객체 내에는 화면을 담당하는 HTML에서 사용할 변수들이 들어있어야 함
    ```
      setup(){
        const data = 1
        return {data}
      }
    ```
  
- Vue 컴포넌트 생명주기
  - 컴포넌트를 생성하여 DOM 노드 트리에 마운트하고, 불필요한 엘리먼트를 제거하는 일련의 과정
  - Vue는 각 생명주기를 Hooking 할 수 있다.
    - options API의 옵션 함수 정의
      ```
      updated(){
        // Update Action
      }
      ```


### 출처

- []()
<br><br><br>

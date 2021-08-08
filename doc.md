## redux
### redux 사용의 장점

- 데이터가 집중화 되어있어 예측가능하다
- 데이터 흐름이 단방향이라 디버깅하기 쉽다.
- 리덕스와 연관된 좋은 생태계가 구축되어 있어 필요에 맞게 유연하게 구현 할 수 있다.
- 사용하는 부품들이 상호 의존성이 낮아 독립성이 높다
- store를 통하여 global state를 포함한 모든 state를 저장및 유지 할 수 있게되어 복잡한 어플리케이션일 수록 데이터의 흐름및 관리를 쉽게 도와준다.

![](https://camo.githubusercontent.com/5cdd3d479e7b612f7d3e62e298d3068657202f8cb4fdcc6123334642c99ac41e/68747470733a2f2f6d69726f2e6d656469756d2e636f6d2f6d61782f3234342f312a686e64683862577452392d6b565931516131423846772e706e67)

![](https://camo.githubusercontent.com/f70c93a196887b4157bfaa2986232dc034f77b8284e6c431981bce7915a20d5b/68747470733a2f2f6d69726f2e6d656469756d2e636f6d2f6d61782f3231392f312a5f4f6d764869697a4d61635735776f64394634734c412e706e67)

> 위와 같이 어플리케이션 복잡성이 높아질수록 state 관리가 어려워진다.

![](https://camo.githubusercontent.com/ecacb946e9b0eb5fcf39cc5b39296108e008e1ddc70f2a51536a558c2830c1ba/68747470733a2f2f6d69726f2e6d656469756d2e636f6d2f6d61782f3639312f312a4e4d462d474d5f554c6b4c6c55746b495767654773412e6a706567)

> redux를 통하여 글로벌하게 state를 관리하여 state 관리를 쉽게 도와준다


---

리덕스 개발

npm 설치시 예시

```js
// npm install --save redux // 명령어로 설치
import { createStore } from "redux";
import todoApp from "./reducers";

let store = createStore(todoApp); // store를 생성하고 reducer를 연결하여 어플리케이션에 연결함.
```

cdn 이용시 

```js
<script src="https://cdnjs.cloudflare.com/ajax/libs/redux/4.0.1/redux.js">
```
---

### store

- redux의 핵심. 정보가 저장되는 곳
- 무엇이 일어날지를 나타내는 action, 그리고 action에 따라 상태를 수정하는 reducer를 저장하는 어플리케이션에 있는 단 하나의 객체이다.

  ### state

  - store 안에 있다.
  - 직접 접근 금지

  ### reducer

  - store를 만들때 리듀서를 만들어줘야한다.
  - state를 입력받고 action을 참조해서 새로운 state를 가공한다.
  - action을 통해 어떠한 행동을 정의했다면 그 결과 어플리케이션의 상태가 어떻게 바뀌는지 특정하게되는 함수이다.
  - reducer 함수에서는 action의 type에 따라 변화된 state를 반환하게 된다.

### subscribe

- 구독.
- 랜더함수를 등록해서 state를 감지해서 랜더를 호출하도록한다.

### dispatch

- reducer를 호출해서 state를 바꾼다.
- 그후 subscribe를 호출해서 render를 통해 화면을 바꾼다.
- subscribe에 등록된 구독자를 다 호출해서 render가 다시 동작한다

---

### render

- state를 참조해서 ui를 만들다

### action

- dispatch에 들어가는 객체.
- store로 data를 보내는 방법. view에서 정의되어 있는 액션을 호출하면 action creators는 어플리케이션의 state를 변경해준다.
- 일반적으로 문자열 상수로 정의된다.



---


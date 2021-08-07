리덕스: 예측가능한 상태의 저장소

소프트웨어 개발의 가장큰 위험성

- 복잡성
  - 리덕스는 복잡성을 낮춰 예측가능성을 높혀준다.

---

state와 render 의 관계

## redux

### store

- redux의 핵심. 정보가 저장되는 곳

  ### state

  - store 안에 있다.
  - 직접 접근 금지

  ### reducer

  - store를 만들때 리듀서를 만들어줘야함
  - state를 입력받고 action을 참조해서 새로운 state를 가공한다.

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

---

리덕스 개발

npm 설치시

```bash
npm install --save redux
```

cdn 이용시

```bash

```

---

redux 사용의 장점

- 사용하는 부품들의 의존성을 낮춘다.
  - 독립성이 올라간다.
  -

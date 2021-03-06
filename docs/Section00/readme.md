# 평가

**코드가 계산(Evaluation) 되어 값을 만드는 것**

<br />

# 일급

- **값으로 다룰 수 있다.**
- **변수에 담을 수 있다.**
- **함수의 인자로 사용될 수 있다.**
- **함수의 결과로 사용될 수 있다.**

<br />

# 일급 함수

- **함수를 값으로 다룰 수 있다.**
- **조합성과 추상화의 도구**

<br />

# 고차 함수

- **함수를 값으로 다루는 함수**

<br />

# 함수를 인자로 받아서 실행하는 함수

- **apply1**

  ```js
  const apply1 = (f) => f(1);
  const add2 = (a) => a + 2;
  log(apply1(add2));
  log(apply1((a) => a - 1));
  ```

- **times**

  ```js
  const times = (f, n) => {
    let i = -1;
    while (++i < n) f(i);
  };

  times(log, 3);

  times((a) => log(a + 10), 3);
  ```

<br />

# 함수를 만들어 리턴하는 함수 (클로저를 만들어 리턴하는 함수)

- **addMaker**

  ```js
  const addMaker = (a) => (b) => a + b;
  const add10 = addMaker(10);
  log(add10(5));
  log(add10(10));
  ```

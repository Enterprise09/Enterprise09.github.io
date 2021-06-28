---
layout: post
title: "React 공부 일기장 (2)"
date: 2021-06-28 15:21:43 +0900
categories: Coding React
---

Hello!
> My Eighth Post

<br>

### 02. React 코딩 공부 일기장

> by Movie Web Service App coding with Normad Corder

오늘은 Javascript문법에서 함수의 호출시점을 살펴보려고 합니다.

예를 들어서 Button의 onClick props에는 js의 함수를 넣어줄 수 있는데

여기서 일반적으로 '함수명( )'으로 쓰게되죠?

하지만 Javascript(React.js)는 위와 같은 형식으로 쓰게 되면 즉시 호출이 된다고 합니다.

코드로 예를 들어봅시다.

```javascript
  state = {
    count: 0,
  };

  add = () => {
    this.setState({ count: this.state.count + 1 });
  };

  <button onClick={this.add()}>Add</button>
```

위와 같은 코드에서 add함수는 괄호가 붙어있는 형태로 기술되어 있기 때문에 

실행 즉시 실행이 된다고 합니다. 이와 반대의 코드를 봅시다.

---

```javascript
  state = {
    count: 0,
  };

  add = () => {
    this.setState({ count: this.state.count + 1 });
  };

  <button onClick={this.add}>Add</button>
```

위 코드에서 add함수는 button의 onClick시 실행될 함수로 지정되어 있습니다.

이 코드에서 add함수가 실행되는 시점은 실행시가 아닌 버튼의 클릭 시점에 실행되게 됩니다.

그게 바로 우리가 원하는 시점이라고 할 수 있겠죠 ?

---

오늘은 요렇게 함수의 형태에 따른 호출시점에 대해서 알아보았습니다.

잃어버리지 않기 위해서 기록하는 습관 ! 

---

[소스 보기\_Github](https://github.com/Enterprise09/movie_app.git){:target="\_blank"}

Good Bye ~

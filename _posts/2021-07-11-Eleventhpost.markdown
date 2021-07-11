---
layout: post
title: "React-Hooks 공부 일기장 (1)"
date: 2021-07-11 21:36:42 +0900
categories: Coding React React-Hooks
---

> My Eleventh Post

<br>

### 01. React-Hooks 코딩 공부 일기장

> by React Hooks Coding with Normad Corder

React 공부를 하다보니 React-Hooks이라는 것이 있더라구요.

그래서 그것도 찾아보니 강의가 있어서 여유롭게 들으면서 공부를 하고 있습니다.

여유롭게 듣다보니 배우는 내용을 정리해두면 좋을 것 같아서 React 공부일기장에 기록하게 되었습니다.

---

React-Hooks이라는 것은 본래 React의 컴포넌트들은 Class구조로 되어있는데

그것을 Function, 즉 함수형으로 구현하는 것입니다.

이렇게 하게되면 state등을 이용하여 프로그래밍 할 때 매우 편리하게 할 수 있습니다.

보통 Class구조의 컴포넌트에서는 state를 아래와 같이 사용합니다.

```javascript
state = {
  isLoading: true,
};

this.setState({ isLoading: false });
```

위와 같이 간단한 코드만을 사용한다면 크게 상관없겠지만 만약 state값이 길어지고,

그에따라 setState의 값이 매우 길어진다면 코드의 가독성이 떨어지게 됩니다.

이런 문제점을 해결하고자 컴포넌트들을 Function구조로 만들게 된 것 입니다.

---

그럼 이제 React-Hooks으로 같은 코드를 작성해보겠습니다.

```javascript
const [isLoading, setIsLoading] = useState(true);
```

코드가 정말많이 줄었습니다. . .

요렇게 하면 위와 같은 기능을 수행하는 코드를 한줄로 작성할 수 있습니다.

첫번째 isLoading값은 실질적으로 값을 저장하는 역할을 하고,

두번째 setIsLoading은 값을 지정하는 역할을 합니다.

여기서 useState를 이용하여 보다 쉽게 state값을 저장 및 변경가능합니다.

---

오늘은 왜 React-Hooks를 사용하는지 아주아주 간단하게 정리 하였습니다.

아직 배우는 입장이기 때문에 까먹지 않으려고 기록합니다.

다음에는 React-Hooks의 useRef()를 포스팅하도록 하겠습니다.

열공 ! ! !

안녕 ~ ~ !

---

[소스 보기\_Github](https://github.com/Enterprise09/nooks){:target="\_blank"}

Good Bye ~

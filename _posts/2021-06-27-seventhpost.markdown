---
layout: post
title: "React 공부 일기장"
date: 2021-06-27 00:58:33 +0900
categories: Coding React
---

Hello!

> My Seventh Post

<br>

### React 코딩 공부 일기장

> by Movie Web Service App coding with Normad Corder

새롭게 [노마드코더](https://nomadcoders.co/){:target="\_blank"} 에서 React 영화 웹서비스 앱 개발 강의를 들었습니다.

요즘 부쩍 React에 관심이 생기기 시작하면서 공부를 제대로 해보자는 마음으로

보통같으면 중 ~ 고급강의를 들었을 텐데 이번에는 초급강의부터 시작해보았습니다.

먼저 이런 무료강의를 제공해주신 니콜라스 선생님께 너무 감사드립니다 ~ ! !

---

```
    Map 함수란?

    Map함수는 배열의 각 원소들에 각각 정의된 함수를 실행한 후

    배열을 리턴해주는 배열을 다룰 때 아주아주 유용한 함수입니다.
```

이 함수를 이용하면 배열의 각 원소을 변경할 때 아주 간단하게 할 수 있습니다.

<br>

```javascript
foodILike.map((dish) => (
  <Food
    key={dish.id}
    name={dish.name}
    picture={dish.image}
    rating={dish.rating}
  />
));
```

위의 코드에서 foodILike는 배열입니다.

이렇게 코드를 작성을 하게 되면 dish가 foodILike에 있는 각 원소를 참조하고

그 참조한 값을 이용하여 Food 라는 Component에 보내줄 수 있게 됩니다.

굳이 배열관련된 반복문을 쓸 필요가 없이 간단하게 Component로 전송할 수 있는 것입니다.

---

```
    Prop-Types 란?

    Prop-Types는 흔히 말하는 값 체크를 위한 도구입니다.

    미리 들어와야하는 값을 지정하고 그 값이 아닌 기대하지 못한 값이 입력되면

    에러를 발생시켜 개발자가 확인할 수 있도록 유도합니다.
```

<br>

간단한 예제 소스를 기록하겠습니다.

```javascript
Food.propTypes = {
  name: PropTypes.string.isRequired,
  picture: PropTypes.string.isRequired,
  rating: PropTypes.number.isRequired,
};
```

Food는 위에서 설명한 것과 같이 Component이고, 이 Component에 들어오는 값들에게

조건을 걸어준다고 생각하면 되겠습니다.

만약 Java를 먼저 공부하신 분이라면 Java의 Validator클래스의 Validation메소드와

거의 유사한 역할을 한다고 생각하시면 되겠습니다.

---

```javascript
    사용시 유의점 ! ! !

    Food.propTypes 에서 맨앞의 'p'를 대문자로 쓰는 경우가 종종 있습니다.

    이럴 경우 React에는 이런 타입이 없다는 에러메시지가 발생되니 주의하시기 바랍니다.
```

---

[소스 보기\_Github](https://github.com/Enterprise09/movie_app.git){:target="\_blank"}

Good Bye ~

---
layout: post
title: "HTML과 CSS를 이용한 Github Clone Coding (1)"
date: 2021-07-03 12:34:22 +0900
categories: Coding CSS
---

Hello!

> My Ninth Post

<br>

### 01. Github Layout Clone Coding

> for HTML, CSS Study

언제 부터인지 웹을 만들 때 Bootstrab이나 관련된 테마들을 이용하여 Frontend를 제작하게 되었습니다.

아마도 디자인에 소질이 없다는 것을 깨달은 그 때 부터이겠죠? . . .

제가 처음 HTML과 CSS등 웹디자인에 관련된 언어를 배웠을 때가 1학년 때,

즉 2년쯤 전입니다. 그 때는 완전 간단하게 맛보기로만 배웠기 때문에 이번에 다시 공부해보려고 합니다.

---

오늘은 Github Layout Clone Coding의 첫번째 포스팅으로 CSS를 오랜만에 사용하면서 알게된 주의점을 포스팅하려고 합니다.

CSS에서 거의 가장 많이 쓰인다고 해도 과언이 아닌 width와 height속성들에는 사용시 중요한 주의점이 있습니다.

width, height에는 %, px, vh등 다양한 단위들이 있고, 단위를 생략하여 사용하기도 합니다.

```
첫번째로 %단위는 부모의 크기를 100%로 보고 자식들의 %에 따라서 넓이와 높이를 지정하는 단위입니다.

따라서 부모가 없는 영역은 width와 height를 %단위로 지정하여도 크기가 변하지 않습니다.
```

```
두번째로 단위를 생략하면 안먹히는 곳이 있기 때문에 가능하면 px단위를 이용하여

width와 height를 지정하는 것이 좋은 코드를 작성하는 방법입니다.
```

---

오늘은 CSS에서 주의할 점을 간단하게 기록해보았습니다.

프로젝트를 진행하다가 또 다른 에러나 주의점을 발견하면 이곳에 다시 포스팅하도록 하겠습니다.

안녕 ~ ~ !

---

[소스 보기\_Github](https://github.com/Enterprise09/Layout_Study.git){:target="\_blank"}

Good Bye ~

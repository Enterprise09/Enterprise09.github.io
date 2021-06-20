---
layout: post
title:  "Ruby & Jekyll Install Error at Labtab"
date:   2021-06-20 21:55:12 +0900
categories: jekyll update
---
Hello! 
> My Second post

---

> CATEGORY : ERROR

## Fixed Error

2021.06.20 (일요일)

오늘 내 노트북에 Ruby을 깔고 gem install를 통해서 

Jekyll 개발환경을 구축하려고 했다.

노트북 사양
> CPU : Ryzen9 5900hx

> RAM : 32GB _ Dual Channel

> GPU : 3070 Labtab

그 전날 데스크탑에 구축하는데 아주 쉽고 빠르게 진행을 했기 때문에 아주 쉬울 것으로 생각했는데...

웬걸... 하던데로 아래의 구문을 실행했는데 

```ruby
    cd 프로젝트경로
    jekyll new ./
    bundle install
    bundle exec jekyll server
```

이런한 에러가 뜨는 것이었다 . . .
```error
    Error: invalid byte sequence in UTF-8
```

분명 데스크탑에서는 아무 문제 없이 돌아갔던 것이어서 구글링을 하면서
```shell
    chcp 65001
```
등등의 많은 코드를 실행하고 레지스트리값까지 변경을 해보았지만 

현재로서는 해결되지 않고 있는 상황이다.

<br>

---

해결 일시
> 2021-06-21 00:33:16 

<br>

해결되었습니다 !

짐작대로 CPU가 Ryzen이고 Mainboard쪽에 문제가 있는 것이 아닌가 라고 생각했었는데 결국 그게 맞았네요 . . .

BIOS 업데이트를 다시 진행해보니 바로 정상으로 실행됩니다!

혹시 같은 문제를 겪으시는 분들은 꼭 BIOS 업데이트를 먼저 해보세요 ! ! ! 



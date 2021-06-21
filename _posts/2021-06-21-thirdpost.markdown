---
layout: post
title:  "setOnClickListener Error"
date:   2021-06-21 21:21:13 +0900
categories: Error Android
---
Hello! 
> My Third Post

오늘은 안드로이드 스튜디오를 이용하여 앱개발을 하던 중에 겪었던 에러 중에서 하나를 소개하려고 합니다.

안드로이드 스튜디오는 앱개발에 큰 도움이 되는 여러종류의 템플릿을 제공합니다.

그 중에서 Navigation Drawer Layout 템플릿을 사용하던 중 겪게된 에러입니다.

---

``` java
    Button btn;

    btn = (Button) findViewById(R.id.btn);
    btn.setOnClickListener(new View.setOnClickListener(){
        @Override
        public void onClick(View v) {
            Toast.makeText(
                getApplicationContext(), 
                "Toast", 
                Toast.LENGTH_SHORT).show();  
        }
        
    });
```
위와 같은 코드에서 에러가 발생했습니다.

코드에 대해서 설명을 간단하게 하면, 

ID가 btn 인 Button은 Drawer Layout에 존재하는 위젯입니다.

이 위젯의 아이디를 가져오는 코드가 아래의 코드 입니다.
```java
    Button btn;
    btn = (Button) findViewById(R.id.btn);
```

하지만 만약 저와 같이 Navigation Drawer Layout 템플릿을 사용하셨다면 . . .

위와 같은 코드로는 버튼 위젯을 가져올 수 없습니다. 

이유가 뭘까요?

그 이유는 Drawer Layout의 특징에 있습니다.

Drawer Layout은 특성상 가려져 있다가 사용자가 끌어서 보이고자 하면 그때서야 보여집니다.

따라서 위와 같은 코드로는 버튼이 실제 있는 공간을 찾아서 버튼 위젯을 가져올 수 없게 됩니다.

---

해결 방법

먼저 Drawer Layout 의 헤더를 찾아서 그 헤더속에 있는 버튼위젯을 찾아오면 됩니다.

아래와 같은 코드를 통해서 헤더를 가져올 수 있습니다.
```java
    NavigationView navigationView = findViewById(R.id.nav_view);
    btn = navigationView.getHeader(0).findViewById(R.id.btn);
    btn.setOnClickListener(new View.setOnClickListener(){
        @Override
        public void onClick(View v) {
            Toast.makeText(
                getApplicationContext(), 
                "Toast", 
                Toast.LENGTH_SHORT).show(); 
        }
    });
```

또 간단하게 코드 설명을 하면 여기서 navigationView는 말 그대로 Drawer Layout과 관련된

위젯을 가르키고 있는 인스턴스이고 여기에 nav_view라는 위젯을 연결해주었습니다.

다음으로 btn의 인스턴스를 연결하기 위해서 위에서 설명한 것과 같이 navigationView의 메소드인 

getHeader( )메소드를 이용하여 헤더값을 찾아온 후, 그 헤더에 속해있는 btn값을 가져오는 코드입니다.

이렇게 연결을 해주어야 btn의 인스턴스를 정상적으로 가져올 수 있습니다.

---

처음에 보여드렸던 코드와 같이 정상적으로 btn의 인스턴스를 가져오지 못할 경우 

바로 아래에 존재하는 setOnClickListener에서 오류가 발생하게 됩니다.

그 이유는 당연히 존재하지 않는 btn의 클릭 시 작동할 메소드를 지정할 수 없기 때문이겠죠?

쉽게 말해 존재하지 않는 버튼이기 때문의 버튼 위젯의 메소드인 

setOnClickListener를 사용할 수 없다고 할 수 있습니다.

<br>

혹시나 나중에라도 이런실수를 다시 하게 될까봐 여기에 포스팅으로 기록합니다.

제목은 정확한 오류메시지명으로 후에 수정하겠습니다.

Good Bye ~ 
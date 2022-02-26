# 웹과 Javascript

## WEB과 Javascript, HTML


WEB이 처음 등장했을 때, 사람들은 HTML(HyperText Markup Language)을 사용해서 정보를 주고받았습니다.

하지만 HTML은 정적입니다. 한 번 출력되면 그 모양이 바뀌지 않죠.

**사용자와 동적으로 상호작용하는 WEB을 만들기 위해서** Javascript가 등장했습니다.

이제 우리는 *HTML을 이용해 웹페이지를 만들고, Javascript를 이용해 사용자와 상호작용할 수 있도록 추가*할 겁니다.

즉, **정적인 정보인 HTML을 Javascript가 동적으로 만들어 주는 것**입니다.

 

## CSS

CSS란 디자인하는 언어입니다. 

* document.querySelector('body').style.backgroundColor='black'

* document.querySelector('body').style.backgroundColor='gray'

문서(document)에서 body라는 태그를 선택(Selector)합니다. 
 
그리고 난 후 style 속성값에서 backgroundColor를 'black'으로 설정한다는 뜻입니다.

이렇게 부여된 속성값은 아까 살펴봤듯이 body 태그의 style 속성으로 들어갑니다. 

이 style 속성은 CSS입니다.

## script 태그

Javascript는 HTML 위에서 동작하는 언어입니다. 

그렇다면 어떻게 서로 다른 두 언어를 하나로 합칠 수 있는 것일까요?

이 때 바로 Script 태그가 필요합니다
 

**HTML의 태그 중 하나인 script 태그 안에는 Javascript 코드를 쓸 수 있습니다.**

다음 예제 코드와 같이 쓸 수 있는 것이죠.

<body>
  <script>
    document.write('hello, world!');
  </script>
</body>

- Javascript

<body>
  <script>
    document.write('hello, world!',(1+1));
  </script>
</body>

- HTML

<body>
  hello, world! (1+1)
</body>

- HTML로 쓴 코드는 정적이기 때문에 문자 그대로 (1+1) 를 출력하지만, Javascript 코드는 동적으로 이를 계산 (2) 하여 출력

## Javascript와 사용자의 상호작용, 이벤트(Event)

- 웹 브라우저에서 일어나는 유용한 사건을 이벤트(Event)라고 합니다.

Javascript에서는 다음과 같은 코드를 통해서 alert 창을 만들 수 있습니다.

* alert('hi')

사용자가 어떤 버튼을 눌렀을 때 이 alert 창이 뜨도록 만들어봅시다. 

먼저 빈 화면에 버튼을 만들고, 이 버튼을 눌렀을 때 어떤 동작이 실행되도록 하는지 지정하는 속성인 onclick에 이 javascript 코드를 넣어봅시다. 

아래 코드처럼요.

* <input type="button" value="hi" onclick="alert('hi')">

**Onclick 이벤트**

- HTML 태그 안에서 onclick 속성은 javascript 코드를 가지게 됩니다. 

- 그리고 onclick이 포함된 태그가 클릭되었을 때 이 javascript 코드에 따라서 웹 브라우저가 동작됩니다. 

- 즉, 위의 코드에서 웹 브라우저는 alert('hi') 라는 코드를 기억하고 있다가, 사용자가 클릭하면 이를 실행해주는 것입니다.

**Onchange 이벤트**

- 예를 들면 다음과 같은 **입력창에서 사용자가 키보드를 이용해 무언가 입력하면, 그에 따라 내용이 바뀌는 사건을 의미하는 것**입니다. 

- 이 때, ***입력창에 입력한 후 바깥쪽을 클릭했을 때를 기준으로 그 전과 내용이 바뀌었는지 확인한다는 점***도 알아두세요.


**웹 브라우저에서 일어나는 사건을 이벤트라고 한다면, 이벤트에는 어떤 종류가 있을까요?**

    - https://www.w3schools.com/js/js_events.asp

이 외에도 총 10~20가지 정도의 이벤트가 존재합니다. 
이를 이용해서 사용자와 상호작용하는 웹 사이트를 만들 수 있게 됩니다.

이러한 다양한 이벤트들을 모두 외울 수는 없겠죠? 여러분이 코딩을 하다가 필요한 이벤트들은 구글링을 통해서 쉽게 찾아볼 수 있습니다. 

예를 들어서 키보드를 누르는 이벤트를 알아보고 싶다면, 구글에 "javascript keydown event"라고 검색하면 **onkeydown** 이라는 이벤트를 쉽게 찾을 수 있습니다.

버튼 위에 마우스를 올리면 경고창이 뜨도록

* <input type="button" value="click" onmouseover="alert('warning')">

## 콘솔 (Console)

- 콘솔(Console)을 이용하면 index.html 파일을 만들지 않고도 바로 Javascript 코드를 실행할 수 있습니다.



어떤 문자열(Hello, World!)의 길이를 알고 싶다고 해 봅시다. 


이 때 바로 이 콘솔 창에서 다음과 같이 치고 엔터를 누르면 문자열의 길이를 현재 페이지에서 바로 경고창으로 출력할 수 있습니다.



* alert('Hello, World!'.length)

즉, 콘솔을 통해서 입력된 코드는 *현재 페이지에서* 즉석으로 실행되는 것입니다.

**그렇다면 이런 콘솔을 어떻게 활용할 수 있을까요?**

예를 들어서 여러분이 페이스북에 댓글을 남기는 이벤트를 개최했다고 해 봅시다. 

이 때 아주 많은 참가자들 중 당첨자를 뽑아야 하는데, 여기서 콘솔을 사용할 수 있습니다. 

미리 짜 둔 Javascript코드를 콘솔 창에 적은 후 실행시키면 당첨자를 쉽게 뽑을 수 있겠죠.

정리하자면, **콘솔을 이용하면 웹사이트에서 간단한 문제를 간편하게 Javascript를 실행시켜서 해결할 수 있는 것**

## Javascript의 데이터 타입

- https://developer.mozilla.org/ko/docs/Web/JavaScript/Data_structures



**숫자(Number)**


예를 들어 1+1을 실행시키면 2가 출력될 겁니다. 

숫자 데이터 타입의 가장 중요한 점은 연산이 가능하다는 것입니다. 

즉, 1+1에서는 +라는 연산이 왼쪽에 있는 값과 오른쪽에 있는 값을 더해서 하나의 값을 만들어내게 됩니다. 그렇기 때문에 +를 이항 연산자라고 부릅니다. 

계산을 하기 때문에 산술 연산자라고 부르기도 합니다. 

여러분이 흔히 아는 사칙 연산 (+, -, *, /)는 모두 산술 연산자에 속합니다. 

즉, 사칙 연산을 이용해서 숫자 데이터 타입을 계산할 수 있는 것입니다.




**문자열(String)**

문자열은 따옴표로 시작해서 따옴표로 끝나게 됩니다. ( 작은 따옴표로 시작하면 작은 따옴표로 끝내고, 큰 따옴표로 시작하면 큰 따옴표로 끝내면 됩니다. )


문자열에서 흔히 사용하는 연산으로는 **length**가 있습니다. ( 문자열 뒤에 .을 붙이고 length를 입력하면 그 문자열의 길이를 알려주게 됩니다. )


그 외에도 문자를 처리하는 데 다양한 명령어를 사용할 수 있습니다. 

예를 들면 str.toUpperCase()를 사용하면 str 안에 들어 있는 모든 문자열의 문자들이 대문자로 바뀌게 됩니다. 

str.indexOf('hi')를 하면 str 안에 있는 hi 라는 문자열을 찾아서 그 부분이 앞에서부터 몇 번째 문자인지 알려주게 됩니다.

문자열을 처리하는 데에는 정말 다양한 명령어가 사용될 수 있습니다. 

이렇게 많은 명령어들을 다 외울 수는 없습니다. 
하지만 여러분들은 검색을 통해서 필요한 명령어를 쉽게 알아낼 수 있겠죠.

* "1"+"1"

>> 11

* 1+1

>> 2

## 변수와 대입연산자

- 재사용의 편리함, 유지보수의 용이성



## 웹 브라우저 제어

- 웹사이트의 색깔이 이렇게 바뀌기 위해서는 <body> 태그의 속성이 바뀌어야 한다는 사실입니다.

* <body>
* <body style="background-color: black; color: white;">

원래 웹페이지에서는 첫 줄과 같이 <body> 태그만 존재했습니다. 
    
하지만 원래의 <body> 태그에서 두 번째 줄과 같이 style을 지정해주면, 배경색은 검정색으로, 글자 색은 하얀색으로 바뀌게 됩니다. 
    
이 때 **style 속성에 들어있는 간단한 코드를 css**라고 부릅니다. 
 
css는 디자인을 위한 언어이고, HTML, Javascript와는 완전히 다른 언어입니다.

- 하지만 HTML은 한 번 표시되면 바뀌지 않는 정적인 언어입니다. 
- 즉 <body> 태그가 만들어지면, 저 style 속성 값을 바꿀 수 없다는 이야기입니다. 
- 지금부터 우리가 만들고자 하는 웹페이지는 Javascript를 이용해 이 문제를 해결할 겁니다.



body 태그의 style 속성을 바꾸어 배경 색은 파란색, 글자 색은 회색으로

* <body style="background-color: blue; color: gray;">

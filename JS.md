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

**Javascript는 HTML 위에서 동작하는 언어** 입니다. 

그렇다면 어떻게 서로 다른 두 언어를 하나로 합칠 수 있는 것일까요?

이 때 바로 **Script 태그**가 필요합니다
 

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

HTML로 쓴 코드는 정적이기 때문에 문자 그대로 (1+1) 를 출력하지만, Javascript 코드는 동적으로 이를 계산 (2) 하여 출력

## Javascript와 사용자의 상호작용, 이벤트(Event)

- 웹 브라우저에서 일어나는 유용한 사건을 이벤트(Event)라고 합니다.
- **이벤트를 다루는 속성을 Javascript로 작성** 합니다.


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

즉, 콘솔을 통해서 입력된 코드는 *현재 페이지에서* 바로 실행되는 것입니다.

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
- 변수를 선언할 때 사용하는 키워드 **var**


## 웹 브라우저 제어

- 웹사이트의 색깔이 이렇게 바뀌기 위해서는 <body> 태그의 속성이 바뀌어야 한다는 사실입니다.

* <body>
* <body style="background-color: black; color: white;">

원래 웹페이지에서는 첫 줄과 같이 <body> 태그만 존재했습니다. 
    
하지만 *원래의 <body> 태그에서 두 번째 줄과 같이 style을 지정해주면, 배경색은 검정색으로, 글자 색은 하얀색으로 바뀌게 됩니다.* 
    
이 때 **style 속성에 들어있는 간단한 코드를 css**라고 부릅니다. 
 
css는 디자인을 위한 언어이고, HTML, Javascript와는 완전히 다른 언어입니다.

- 하지만 HTML은 한 번 표시되면 바뀌지 않는 정적인 언어입니다. 
- 즉 *<body> 태그가 만들어지면, 저 style 속성 값을 바꿀 수 없다는 이야기*입니다. 
- 지금부터 우리가 만들고자 하는 **웹페이지는 Javascript를 이용해 이 문제를 해결**할 겁니다.



body 태그의 style 속성을 바꾸어 배경 색은 파란색, 글자 색은 회색으로

* <body style="background-color: blue; color: gray;">

## CSS의 기본 문법

- CSS를 이용하면 웹페이지에 있는 요소들의 디자인을 바꿀 수 있습니다.


이를 위해서는 *바꾸고 싶은 태그에 style 속성을 사용*하면 됩니다. 
이 style 속성 안에는 CSS가 들어가게 됩니다.


```python
<h1>Javascript<h1>
```


```python
<h1 style="color: blue">Javascript<h1>
```

## CSS기초 (style 태그)

- HTML에서 전체 문단이 아닌, 일부분에만 스타일을 적용하고 싶다면 어떻게 해야 할까요? 

- 같은 스타일을 여러군데에서 여러번 사용하고 싶다면 어떻게 하면 좋을까요? 

- **CSS class**를 이용해서 이 문제를 해결

### Span, Div


우리가 CSS를 이용해서 *문단의 특정 부분에만 스타일을 주어서 강조*를 하고 싶다고 해 봅시다. 이 때 이 부분을 감싸줄 수 있는 HTML 태그가 필요하겠죠.

이를 위해서 우리는 div와 span이라는 HTML 태그를 사용합니다. 

둘 모두 어떠한 특정한 기능이 있는 태그가 아니고, **CSS나 Javascript 코드를 삽입하기 위해서 존재하는 태그**입니다. 

**div 태그는 화면 전체를 사용하기 때문에 줄바꿈이 되고, span은 줄바꿈이 되지 않습니다.**


이제 이러한 div와 span 태그 안에 style 속성을 부여하면 이 태그로 감싸진 부분에만 디자인이 적용되게 됩니다.

하지만 이렇게 모든 부분을 div나 span 태그로 감싸려고 한다면 이를 쓰기도 힘들고, 수정하기는 더욱 힘들 것입니다. 

이를 위해서 CSS에는 **선택자** 라는 기능이 존재합니다.

### Class


```python
# <head> 태그 안에 <style>이라는 새로운 태그를 만들어 줍니다.
# <style> 태그 안에는 CSS 코드
# "js" class 생성

<head>
  <style>
    .js{
        font-weight: bold;
    }
  </style>
</head>
```


```python
# HTML 코드의 곳곳에 "js"class 적용시키면 됩니다. 
# 예를 들어 어떤 문장에서 Javascript라는 단어에만 이 class를 적용시켜서 볼드체로 만들고 싶다면 다음과 같이 쓰면 됩니다.

<span class="js">Javascript</span> is wonderful!

```

- style 태그 안에 있는 .js만 수정하면 js라는 class를 가진 모든 태그를 한 번에 바꿀 수 있습니다.

## CSS기초 (선택자)

- 하나의 class로 지정되어 있는 여러 부분 중 딱 한 부분에만 또 다른 스타일을 적용하고 싶다면 어떻게 하면 좋을까요?

선택자 class 외에도 id가 존재합니다. 

id는 class와는 달리 .대신 **#을 붙여야 한다**는 차이점이 있습니다. 



-  first라는 id 생성 

<style>
  #first {
    color: green;
  }
</style>

### Class와 Id의 차이점

그렇다면 만약 class와 id가 모두 지정되어 있는 태그에서는, 둘 중에 어떤 디자인을 따라가게 될까요? 이를 위해서 class와 id의 차이점을 알아봅시다.

class라는 단어는 그룹을 의미하고, id는 특정한 것을 식별한다는 의미입니다. 

class 선택자는 같은 스타일이 지정될 그룹을 의미하는 것이고, id는 특정한 태그에만 지정하고 싶은 스타일을 나타내는 것입니다. 

**그래서 class는 중복될 수 있지만, id는 한 페이지에서는 딱 한번만 쓰이게 되는 것**입니다.

즉, class 선택자가 id 선택자에 비해서 더 포괄적입니다. 

class 선택자를 이용하면 광범위한 효과를 줄 수 있고, id 선택자를 이용하면 예외적으로 디자인을 바꿀 수 있는 것이죠. 

그렇기 때문에 **class 위에 id를 얹어서 구현하는 것이 효율적**입니다.

### 선택자의 우선순위

마지막으로 id 선택자와 class 선택자 외에 스타일을 나타내는 한 가지 방법을 더 알아봅시다. 

만약 **앞에 .과 # 모두 지정하지 않으면 그것은 *태그 이름* 을 의미**합니다. 

즉 아래와 같은 코드를 사용하면 이 페이지에서 span이라는 이름의 태그는 모두 디자인이 바뀌는 것이죠.


```python
# .과 # 모두 지정하지 않고 
# style tag('span') 생성

<style>
  span {
    color: blue;
  }
</style>

```


```python
<span id="first" class="js">Javascript</span>
```

- id > class > 태그 순서로 우선순위

- span  : style tag
- hello : style class
- bye   : stlye id

<style>
  span {
    color: blue;
  }
  .hello {
    font-size: 12px;
    color: red;
  }
  #bye {
    font-size: 13px;
  }
</style>



```python
<span id="bye" class="hello">Javascript</span>
```

## querySelector ( )

- Javascript 코드를 통해서, 이벤트가 일어났을 때, 어떤 태그에 스타일이 지정될지 선택하는 작업 시 태그를 선택해야 합니다.
- https://developer.mozilla.org/ko/docs/Web/API/Document/querySelector

- Document.querySelector()는 제공한 선택자 또는 선택자 뭉치와 일치하는 문서 내 첫 번째 Element를 반환합니다. 
- 일치하는 요소가 없으면 null을 반환합니다.


```python
documnet.querySelector("body")
#documnet.querySelector(".js")
#documnet.querySelector("#first")
```

- 페이지 내에서 "body"라는 이름의 태그를 모두 선택하는 것이죠. 
- 만약 js라는 class를 가진 태그를 선택하고 싶다면 따옴표 사이에 ".js"를 쓰면 되고,
- first라는 id를 가진 태그를 선택하고 싶다면 "#first"라고 쓰면 됩니다. 




```python
# "body" 태그에 스타일을 적용 

documnet.querySelector("body").style.backgroundColor = 'black';
```

- body 태그를 모두 고른 뒤, 여기에 스타일을 적용하기 위해서 style이라고 써 주고, 

- 여러 스타일 중에서도 배경색을 지정하기 위해서 backgroundColor라고 써 준 것입니다.



```python
# 예를 들어서, 버튼을 클릭할 때 이러한 스타일 변화가 일어나도록 
<input type="button" value="night" onclick="documnet.querySelector('body').style.backgroundColor = 'black';">
```

## 프로그램, 프로그래밍, 프로그래머

프로그램에는 순서라는 의미가 있습니다. 

프로그래밍은 이러한 순서를 만드는 행위를 말하죠. 

프로그래머는 이러한 순서를 만드는 일을 하는 사람을 의미

컴퓨터를 사용할 때에는 다양한 기능을 순서대로 사용하게 됩니다. 그리고 보통은 이러한 기능이 반복적으로 이용합니다.

### HTML과 Javascript의 비교

HTML로 만든 웹페이지는 시간의 순서에 따라 실행되지 않고, 한 번 만들어지면 바뀌지 않습니다. 
때문에 HTML은 컴퓨터 프로그래밍 언어가 아닙니다.


반면에 Javascript는 사용자와 상호작용하고, 이를 위해서 시간에 따라 여러 기능이 실행되어야 하기 때문에 프로그래밍이라는 형태를 띄게 됩니다. 

따라서 Javascript는 컴퓨터 프로그래밍 언어라고 부를 수 있는 것입니다.

그리고 더 나아가서 시간에 따라 코드가 실행되는 것 외에도, 조건에 따라 다른 코드가 실행되도록 하거나, 같은 코드가 반복적으로 실행할 수 있는 방법도 고안하게 된 것입니다.


- Javascript 와 달리 HTML은 왜 프로그래밍 언어가 아닌지 스스로에게 설명해봅시다.

## 조건문, boolean


```python
if(true) {
    document.write('2')
  }
else {
    document.write('3')
```

## 조건문을 활용한 토글 만들기


```python
<input id="night_day" type="button" value="night">

```

- 현재 페이지에서 querySelector을 사용해서 id가 night_day인 태그를 찾기 위해서 id를 나타내는 #을 붙여줍니다. 
- 그리고 찾아낸 태그의 value를 알기 위해서 .value를 써 줍니다.


```python

if(document.querySelector('#night_day').value === 'night') {
  document.querySelector('body').style.backgroundColor = 'black';
  document.querySelector('body').style.color = 'white';
  document.querySelector('#night_day').value = 'day';
}
else {
  document.querySelector('body').style.backgroundColor = 'white';
  document.querySelector('body').style.color = 'black';
  document.querySelector('#night_day').value = 'night';
}
```

- 코드가 실행될 때마다 ('#night_day').value를 바꿔주는 코드도 추가하여 초기화 해야 합니다.

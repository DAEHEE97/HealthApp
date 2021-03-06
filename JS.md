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

\<body>

  \<script>
  
    document.write('hello, world!',(1+1));
    
  \</script>
  
\</body>

- HTML

\<body>

  hello, world! (1+1)
  
\</body>

HTML로 쓴 코드는 정적이기 때문에 문자 그대로 (1+1) 를 출력하지만, Javascript 코드는 동적으로 이를 계산 (2) 하여 출력

## Javascript와 사용자의 상호작용, 이벤트(Event)

- 웹 브라우저에서 일어나는 유용한 사건을 이벤트(Event)라고 합니다.
- **이벤트를 다루는 속성을 Javascript로 작성** 합니다.


Javascript에서는 다음과 같은 코드를 통해서 alert 창을 만들 수 있습니다.

* alert('hi')

사용자가 어떤 버튼을 눌렀을 때 이 alert 창이 뜨도록 만들어봅시다. 

먼저 빈 화면에 버튼을 만들고, 이 버튼을 눌렀을 때 어떤 동작이 실행되도록 하는지 지정하는 속성인 onclick에 이 javascript 코드를 넣어봅시다. 


* \<input type="button" value="hi" onclick="alert('hi')">

**Onclick 이벤트**

- HTML 태그 안에서 onclick 속성은 javascript 코드를 가지게 됩니다. 


- *onclick이 포함된 태그가 클릭되었을 때 이 javascript 코드에 따라서 웹 브라우저가 동작됩니다.* 


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

* \<input type="button" value="click" onmouseover="alert('warning')">

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
11

* 1+1  
2

## 변수와 대입연산자

- 재사용의 편리함, 유지보수의 용이성
- 변수를 선언할 때 사용하는 키워드 **var**


## 웹 브라우저 제어

- 웹사이트의 색깔이 이렇게 바뀌기 위해서는 <body> 태그의 속성이 바뀌어야 한다는 사실입니다.

* \<body>
* \<body style="background-color: black; color: white;">

원래 웹페이지에서는 첫 줄과 같이 \<body> 태그만 존재했습니다. 
    
하지만 *원래의 \<body> 태그에서 두 번째 줄과 같이 style을 지정해주면, 배경색은 검정색으로, 글자 색은 하얀색으로 바뀌게 됩니다.* 
    
이 때 **style 속성에 들어있는 간단한 코드를 css**라고 부릅니다. 
 
css는 디자인을 위한 언어이고, HTML, Javascript와는 완전히 다른 언어입니다.

- 하지만 HTML은 한 번 표시되면 바뀌지 않는 정적인 언어입니다. 

- 즉 *\<body> 태그가 만들어지면, 저 style 속성 값을 바꿀 수 없다는 이야기* 입니다. 



- **동적인 웹페이지를 위해 Javascript를 이용해 이 문제를 해결**할 겁니다.



ex) body 태그의 style 속성을 바꾸어 배경 색은 파란색, 글자 색은 회색으로


```python
<body style="background-color: blue; color: gray;">
```

## CSS의 기본 문법

- CSS를 이용하면 웹페이지에 있는 요소들의 디자인을 바꿀 수 있습니다.

이를 위해서는 *바꾸고 싶은 태그에 style 속성을 사용* 하면 됩니다. 

이 style 속성 안에는 CSS가 들어가게 됩니다.

```
<h1> Javascript <h1>

>

<h1 style="color: blue"> Javascript <h1>
```

## CSS기초 (style 태그)

- HTML에서 전체 문단이 아닌, 일부분에만 스타일을 적용하고 싶다면 어떻게 해야 할까요? 

- 같은 스타일을 여러군데에서 여러번 사용하고 싶다면 어떻게 하면 좋을까요? 

- **CSS class**를 이용해서 이 문제를 해결

### Span, Div

- 우리가 CSS를 이용해서 *문단의 특정 부분에만 스타일을 주어서 강조*를 하고 싶다고 해 봅시다. 

- 이 때 이 부분을 감싸줄 수 있는 HTML 태그가 필요하겠죠.

- div와 span이라는 HTML 태그를 사용합니다. 

- 둘 모두 어떠한 특정한 기능이 있는 태그가 아니고, **CSS나 Javascript 코드를 삽입하기 위해서 존재하는 태그**입니다. 



- **div 태그는 화면 전체를 사용하기 때문에 줄바꿈이 되고, span은 줄바꿈이 되지 않습니다.**


- **div와 span 태그 안에 style 속성을 부여하면 이 태그로 감싸진 부분에만 디자인이 적용되게 됩니다.**



하지만 이렇게 모든 부분을 div나 span 태그로 감싸려고 한다면 이를 쓰기도 힘들고, 수정하기는 더욱 힘들 것입니다. 

이를 위해서 CSS에는 **선택자** 라는 기능이 존재합니다.

### Class


```python
# <head> 태그 안에 <style>이라는 새로운 태그를 만들어 줍니다.
# <style> 태그 안에는 CSS 코드
# "js" class 생성
```

```
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
```

```
<span class="js"> Javascript </span> is wonderful!

```

- style 태그 안에 있는 .js만 수정하면 js라는 class를 가진 모든 태그를 한 번에 바꿀 수 있습니다.

## CSS기초 (선택자)

- 하나의 class로 지정되어 있는 여러 부분 중 딱 한 부분에만 또 다른 스타일을 적용하고 싶다면 어떻게 하면 좋을까요?

- 선택자 class 외에도 id가 존재합니다. 

- id는 class와는 달리 .대신 **#을 붙여야 한다**는 차이점이 있습니다. 



```python
# <style> 태그 안에는 CSS 코드
# "first" id 생성
```

```
<style>
  #first {
    color: green;
  }
</style>`
```

### Class와 Id의 차이점

class라는 단어는 그룹을 의미하고, id는 특정한 것을 식별한다는 의미입니다. 

class 선택자는 같은 스타일이 지정될 그룹을 의미하는 것이고, id는 특정한 태그에만 지정하고 싶은 스타일을 나타내는 것입니다. 





**class는 중복될 수 있지만, id는 한 페이지에서는 딱 한번만 쓰이게 되는 것**입니다.

즉, class 선택자가 id 선택자에 비해서 더 포괄적입니다. 

class 선택자를 이용하면 광범위한 효과를 줄 수 있고, id 선택자를 이용하면 예외적으로 디자인을 바꿀 수 있는 것이죠. 

따라서 **class 위에 id를 얹어서 구현하는 것이 효율적**입니다.

### style tag 

마지막으로 id 선택자와 class 선택자 외에 스타일을 나타내는 한 가지 방법을 더 알아봅시다. 

만약 **앞에 .과 # 모두 지정하지 않으면 그것은 *태그 이름* 을 의미**합니다. 

즉 아래와 같은 코드를 사용하면 이 페이지에서 span이라는 이름의 태그는 모두 디자인이 바뀌는 것이죠.

- .과 # 모두 지정하지 않고 
- style tag('span') 생성

~~~
<style>
  span {
    color: blue;
  }
</style>
~~~

```
<span> Javascript </span>
```


```
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
```


```
<span id="bye" class="hello">Javascript</span>
```

- span  : style tag
- hello : style class
- bye   : stlye id

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

컴퓨터를 사용할 때에는 다양한 기능을 순서대로 사용하게 됩니다. 

그리고 보통은 이러한 기능이 반복적으로 이용합니다.

### HTML과 Javascript의 비교

HTML로 만든 웹페이지는 시간의 순서에 따라 실행되지 않고, 한 번 만들어지면 바뀌지 않습니다. 
때문에 HTML은 컴퓨터 프로그래밍 언어가 아닙니다.


반면에 Javascript는 사용자와 상호작용하고, 이를 위해서 시간에 따라 여러 기능이 실행되어야 하기 때문에 프로그래밍이라는 형태를 띄게 됩니다. 

따라서 Javascript는 컴퓨터 프로그래밍 언어라고 부를 수 있는 것입니다.

그리고 더 나아가서 시간에 따라 코드가 실행되는 것 외에도, 조건에 따라 다른 코드가 실행되도록 하거나, 같은 코드가 반복적으로 실행할 수 있는 방법도 고안하게 된 것입니다.


- Javascript 와 달리 HTML은 왜 프로그래밍 언어가 아닌지 스스로에게 설명해봅시다.

# Javascript 제어

## 조건문, boolean

- ===

```
if(true) {
    document.write('2')
  }
else {
    document.write('3')`

```

## 조건문을 활용한 토글 만들기

- 버튼 생성

```
<input id="night_day" type="button" value="night">

```

- 현재 페이지에서 querySelector을 사용해서 id가 night_day인 태그를 찾기 위해서 id를 나타내는 #을 붙여줍니다. 
- 그리고 찾아낸 태그의 value를 알기 위해서 .value를 써 줍니다.
- 코드가 실행될 때마다 ('#night_day').value를 바꿔주는 코드도 추가하여 초기화 해야 합니다.


- 버튼생성 후 onclick 시 이벤트 발생

```

<input id="night_day" type="button" value="night" onclick = "

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

">
```

## 리팩토링(중복의 제거)

- 리팩토링을 통해 코드의 중복을 제거해 더 간결하고 가독성 높은 코드를 만들 수 있습니다.

### 리팩토링 - this 사용하기

- 자기 자신을 가리키기 위한 this

- input id 로 가져온 자기자신 태그를 가리키기 위한 this 
- document.querySelector('#night_day') > this 

```

<input id="night_day" type="button" value="night" onclick = "

    if(this.value === 'night') {
      document.querySelector('body').style.backgroundColor = 'black';
      document.querySelector('body').style.color = 'white';
      this.value = 'day';
    }
    else {
      document.querySelector('body').style.backgroundColor = 'white';
      document.querySelector('body').style.color = 'black';
      this.value = 'night';
    }

">
```

### 리팩토링 - 변수 사용 

- document.querySelector('body') > var 변수 선언 하여 중복 제거


```
<input id="night_day" type="button" value="night" onclick = "

    var target = document.querySelector('body');


    if(this.value === 'night') {
      target.style.backgroundColor = 'black';
      target.style.color = 'white';
      this.value = 'day';
    }
    else {
      target.style.backgroundColor = 'white';
      target.style.color = 'black';
      this.value = 'night';
    }

">
```

## 반복문




```python
# querySelectorAll 이 페이지의 모든 a 태그를 가져옵니다. 

var links = document.querySelectorAll('a');

# 반복문을 이용해서 각각의 a 태그들의 color을 blue로 바꿔주는 것입니다.

var i = 0;

while (i<links.length) {
  links[i].style.color = 'blue';
  i=i+1;
}
```


```python
document.write('<li>1</li>');

# 0,1,2 
# 3번 반복

var i = 0;
while (i < 3) {
  document.write('<li>2</li>');
  document.write('<li>3</li>');
  i = i + 1;
}

document.write('<li>4</li>');
```

## 배열 (Array)


```python
# firuts 배열 선언
var fruits = ["apple", "banana"];

# apple이 출력
document.write(fruits[0]);


```

### 배열의 길이 .length




```python
document.write(fruits.length);
```

### 배열에 값 추가하기 push


```python
fruits.push("coconut");
```

### 배열에 값 제거하기 splice


```python
fruits.splice("apple");
```


```python

var i = 0;

while (i < fruits.length) {
  document.write('<li>'+fruits[i]+'</li>');
  i = i + 1;
}
```

## 반복문과 배열의 활용


```python
# querySelectorAll 이 페이지에 있는 모든 a 태그를 배열(array) 형태로 alist에 저장
# 원래 사용하던 querySelector라는 함수는 하나의 태그만 가져옵니다.

var alist = document.querySelectorAll('a');

# 문서 안의 모든 a 태그의 색깔이 powderblue로 바뀌는 것

var i = 0;
while (i < alist.length) {
  alist[i].style.color = 'powderblue';
  i = i + 1;
}
```


```python
# 역순 출력 dcba

var coworkers = ['a', 'b', 'c', 'd'];
var i = coworkers.length - 1;

while(i >= 0) {
    document.write(coworkers[i]);
    i = i - 1;
}

```

# Javascript 함수

- 같은 코드가 반복될 때, 우리는 반복문 사용 뿐만 아니라 함수를 통해서도 코드를 간결하게 할 수 있습니다.

- \<head> 태그 안에 \<script> 태그를 만들어서 쓸 수 있습니다.
    
- function 함수명 (parameter/self)




```python
<head>

    <script>
        
      function nightdayhandler(self) {
          

      }
    </script>

<head>
```


```python
<input id='night_day' type='button' value='night' onclick='nightdayhandler(this);'>


```

## 매개변수 (Parameter) 와 인자 (Argument)

- 함수 입력에 해당하는 것을 매개변수 (Parameter)와 인자 (Argument)라고 부르고, 출력에 해당하는 것을 리턴(Return)이라고 부릅니다.


```python
function sum(left, right) # Parameter
{ 
  document.write(left + right);
}
```


```python
sum(2,3); # Argument
```


```python
function sum(left, right) {
  return left + right; # return
}
```

## 함수 호출

- *this* 는 그 코드가 포함되어 있는 태그를 가리키는데

- nightdayhandler 함수를 사용할 때 **this를 사용해서 태그를 전달**해주고, nightdayhandler 함수에서는 이를 매개변수로 받아서 사용
  



```python
<script>

  function nightdayhandler(self) {
      
        if(self.value === 'night') {  
            
  }
</script>
```


```python
# 함수 호출

<input id='night_day' type='button' value='night' onclick='nightdayhandler(this);'>
```

# Javascript 객체




## 객체 (object)

- 객체는 함수의 기반 위에서 존재하는 개념입니다. 

- 서로 연관된 함수와 변수가 아주 많아지면 이를 정리하기 위해서 사용하는 것이죠.




```python
function LinksSetColor(color){
  var alist = document.querySelectorAll('a');
  var i = 0;
  while(i < alist.length) {
    alist[i].style.color = color;
    i = i + 1;
  }
}
```


```python
setColor("powderblue");
```

배경과 글자의 색을 바꾸는 코드도 따로 함수 작성


```python
function BodySetColor(color){
  document.querySelector('body').style.color = color;
}
```


```python
function BodySetBackgroundColor(color){
  document.querySelector('body').style.backgroundColor = color;
}
```

다양한 함수들이 존재하는 상황에서 우리는 객체를 사용하면 됩니다. 

예를 들어 함수의 종류가 아주 많아지게 되면 이 함수들끼리 이름이 중복되지 않도록 만들게 하기 위해서 굉장히 복잡한 이름을 사용해야 하겠죠.

이 때 객체를 사용하면 이 함수들을 비슷한 것들끼리 그룹으로 만들어 묶어줄 수 있습니다. 

마치 여러분의 컴퓨터에서 폴더를 만들어서 정리하는 것과 비슷한 상황입니다. 이렇게 나뉜 함수들은 서로 다른 그룹끼리는 이름이 겹쳐도 괜찮습니다.




```python
document.querySelector('body');
```

- document가 바로 객체이고, querySelector가 document라는 객체에 속해 있는 함수라고 생각할 수 있는 것입니다. 
- 이렇게 객체에 속해 있는 함수들은 메소드(Method)라는 별도의 이름으로 부르게 됩니다.

## 객체 접근

- 우리는 이전에 배열에 대해서 배운 적이 있었습니다. 어떤 값들을 순서를 가지도록 저장하는 구조였습니다.

- 그렇다면 순서 없이 저장하는 구조도 있어야겠죠? 그것이 바로 객체입니다.

- **객체에는 순서가 없는 대신 각각에 이름이 붙어 있습니다. 이름을 이용해서 값들을 꺼내고 넣는 것**이죠.


```python
# 배열

var coworkers = []
```


```python
# 객체

var coworkers= {
  "programmer": "egoing",
  "designer": "leezche"
};
```

- 객체를 만들 때에는 배열과는 달리 중괄호를 사용합니다. 
- *각 요소들은 각각 이름과 값으로 이루어져 있죠.* 

- 예를 들면 egoing이라는 값에는 programmer이라는 이름표가 붙어있는 것입니다.

- 그렇다면 이 요소들을 꺼낼 때에는 어떻게 해야 할까요? 다음과 같이 써주면 됩니다.


```python
## 객체 인덱싱
```


```python
document.write(coworkers.programmer)
document.write(coworkers["programmer"])
```


```python
## 객체 요소 추가
```


```python
coworkers.bookkeeper = "duru";
coworkers["bookkeeper"] = "duru";
```

## 객체의 순회 ( iteration ) 

- 객체에 있는 모든 값들을 가져오는 방법
- for (var key in Object)


- 객체의 메소드 안에서 객체 자신을 가리키는 키워드 this


```python
# object {} 선언

var coworkers = {
  "programmer": "egoing",
  "designer": "leezche"
};

```


```python
# key 출력

for(var key in coworkers) {
  document.write(key+'<br>');
}
```


```python
# value 출력 object[key]

for(var key in coworkers) {
  document.write(coworkers[key]+'<br>');
}
```

## 객체의 메소드 (method)

- 객체에 새로운 함수, 즉 메소드를 추가할 수 있습니다.
- showAll()



```python
# coworkers 객체, showAll method 추가 
# coworkers에서만 사용할 수 있음

coworkers.showAll = function() {
  for (var key in coworkers) {
    document.write(key + ' : ' + coworkers[key] + '<br>');
  }
}
```

- cowerkers라는 변수 이름이 바뀌면 함수를 수정해야 하기 때문이죠. 

- 이 때 사용하는 것이 바로 this입니다. 

- **coworkers 대신에 이 메소드가 쓰인 객체를 가리키는 this를 사용** 해주면 됩니다. 




```python
coworkers.showAll = function() {
  for (var key in this) {
    document.write(key + ' : ' + this[key] + '<br>');
  }
}
```

## 객체의 프로퍼티 ( property )

- 객체에 해당하는 변수들 예를 들면 coworkers.programmer에서 programmer에 해당하는 것들입니다. 
- 이런 변수들은 프로퍼티(property)라고 부릅니다. (key)


## 객체 활용

- Body 객체

```
var Body = {
  setColor: function (color) {
    document.querySelector('body').style.color = color;
  },
  setBackgroundColor: function (color) {
    document.querySelector('body').style.backgroundColor = color;
  }
`
```

- Links 객체

```
var Links = {
  setColor: function (color) {
    var alist = document.querySelectorAll('a');
    var i = 0;
    while (i < alist.length) {
      alist[i].style.color = color;
      i = i + 1;
    }
  
```


- Body와 Links에 모두 setColor이라는 함수가 존재하게 됩니다. 
- 하지만 이 둘을 사용할 때에는 다음과 같이 다르게 사용하게 됩니다.

```
Body.setColor('black');
Links.setColor('powderblue')`
```

# Javascript 활용


##  파일을 이용해 코드 정리하기

복사 붙혀놓기로 수정하기 힘든 상황에서 파일로 쪼개는 것입니다.

새로운 js 파일을 만들어 봅시다. 

예를 들어서 colors.js라는 파일 이름으로 만들었다고 해 봅시다. 

그리고 그 파일에 모든 페이지에서 공통적으로 사용되는 Javascript 코드를 넣습니다.

그렇다면 원래 Javascript 코드가 있었던 \<script> 태그는 어떻게 바꾸면 될까요? 
다음과 같이 **src 속성에 이 파일 이름을 넣어서 바꾸면 됩니다.**

```
<script src='colors.js'>  </script>

```

## 파일 이용의 장점

이제 이 짧은 script 코드를 필요한 페이지에 붙여 넣으면 이 Javascript 코드를 한 번에 관리할 수 있는 것입니다. 

즉, 코드를 재사용할 수 있고, 동시에 코드를 수정할 수 있어서 유지보수가 편리해집니다. 

코드가 명확해지고 가독성이 좋아진다는 장점도 있습니다.

이렇게 파일을 분리하면 캐시의 입장에서도 장점을 가집니다. 

colors.js라는 파일을 한 번 다운로드해서 캐시에 저장해두면 다운로드 없이 사용할 수 있기 때문에 더 빨리 페이지를 표시할 수 있는 것입니다.

## 소프트웨어의 사회성

다른 사람들의 소프트웨어를 가져와서 사용할 수 있는 방법에 대해서 알아봅시다.


이렇게 다른 사람과 코드를 통해서 협력하는 모델에는 두 가지가 있습니다.


- 라이브러리는 프로그램에 필요한 부품이 되는 소프트웨어가 정리되어 있는 것입니다. 


- 프레임워크는 만들고자 하는 프로그램의 종류에 따라서 공통적인 부분을 미리 만들어놓는 것입니다. 


필요한 부분만 약간 수정해서 사용할 수 있는 것이죠. 


즉, 라이브러리는 우리가 필요한 부분을 가져와서 사용하는 것이라면, 프레임워크는 직접 프레임워크 안으로 들어가서 디테일을 수정해서 사용하는 것이라고 생각하시면 됩니다.



## jQuery 라이브러리

가장 유명한 Javascript 라이브러리 중 하나는 jQuery입니다. 

이 라이브러리를 사용하면 생산성을 높일 수 있습니다. 


인터넷에서 jQuery를 다운로드하는 방법도 있고, CDN이라는 방법을 사용해도 됩니다. 

- CDN을 사용하면 코드를 한 줄 추가하는 것만으로도 라이브러리를 가져와서 사용할 수 있습니다. 
- 예를 들어 jQuery의 구글 CDN은 다음과 같습니다. (jQuery 홈페이지에서 찾을 수 있습니다.)


- 이 한 줄을 \<head>에 추가하면 된다는 것이죠.


    
```
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>

```


    


jQuery를 사용하면 반복문을 사용하지 않고도 모든 태그를 한 번에 처리할 수 있습니다. 

```
$('a').css("color","powderblue");

```


예를 들어서 다음과 같이 사용할 수 있습니다.

반복문을 사용하지 않고 이 한 줄만으로 모든 a 태그의 색깔을 powderblue로 바꿀 수 있는 것입니다.


하지만 jQuery는 새로운 언어가 아닙니다. 

우리가 직접 함수를 만드는 대신 이러한 일을 하는 함수가 jQuery 안에 미리 만들어져 있는 것이죠.

이렇게 적절한 라이브러리를 잘 사용하면 효율적으로 코딩을 할 수 있게 됩니다.


## UI ( User Interface )와 API ( Application Programming Interface )


예를 들어서 어떤 페이지에 버튼이 하나 있고, 이 버튼을 누르면 경고창이 뜨게 만들었다고 해 봅시다. 
이 버튼을 사용하는 것은 웹페이지의 사용자죠. 

**사용자들이 시스템을 제어하기 위해서 조작하는 장치를 UI**라고 부릅니다.



이제 코드를 봅시다. 

이 경고창은 우리가 만든 것일까요? 

경고창의 텍스트나, 경고창이 뜨는 타이밍은 우리가 만든 것이지만, 우리는 경고창을 실제로 띄우기 위해서는 alert라는 함수를 사용했죠. 


alert라는 이 함수는 웹브라우저를 만든 사람들이 미리 만들어둔 것입니다. 

그리고 우리는 이 alert라는 함수를 호출해서 조작하는 것이죠. 

이렇게 **프로그래머들이 사용하는 조작 장치들을 API**라고 부릅니다. 

즉, alert는 API인 것이죠.



이러한 UI와 API라는 개념은 Javascript 뿐만 아니라 모든 프로그래밍 언어에 적용되는 개념입니다. 

우리는 **API를 응용하고 결합해서 새로운 프로그램을 만들 수 있는 것**입니다.

## 웹 개발과 관련된 검색

먼저 태그를 삭제하거나 자식 태그를 추가하고 싶은 경우에는 document라는 객체를 살펴보세요. 그래도 찾을 수 없다면 DOM 객체에 대해서도 살펴보세요.

만일 웹브라우저 자체를 제어해야 하는 경우, 예를 들면 웹페이지의 주소를 알아낸다거나, 창을 열거나 해야 하는 경우에는 windows 객체의 프로퍼티나 메소드를 찾아보세요.

웹페이지를 새로고침하지 않고도 정보를 변경하고 싶다면 ajax를 사용해보세요. 반대로 웹페이지가 새로고침되어도 현재 상태를 유지하도록 만들고 싶으면 cookie에 대해서 배워보세요.

인터넷이 끊겨도 동작하는 웹페이지를 위해서는 offline web application을 찾아보세요. 

화상 통신 웹 앱을 만들고 싶을 때에는 webRTC를 찾아보면 됩니다. 음성을 인식하거나 음성과 관련된 것을 처리하고 싶을 때에는 speech로 시작되는 API들을 살펴보세요.

3차원 그래픽을 이용하고 싶다면 webGL, 가상현실에 대해서 알아보고 싶다면 webVR에 대해서 찾아보시면 됩니다.

# Javascript 객체 기본

##  배열에서의 반복문

가장 기본적인 while 문을 사용해보겠습니다. 

i의 값은 0부터 memberArray의 길이보다 1작은 값까지 증가하기 때문에, 우리는 memberArray에 있는 값을 하나 하나 꺼내올 수 있게 됩니다. 

- __console.group__ 을 사용하면 결과값을 더 보기 좋게 정리할 수 있습니다. 

```
var memberArray = ['egoing','graphittie','leezche'];

console.group('array loop');

var i = 0;
while(i<memberArray.length){
    console.log(i, memberArray[i]);
    i = i + 1;
}

console.groupEnd('array loop');
```

## 객체에서의 반복문

- for-in 문
- for (현재 원소의 이름이 들어갈 변수) in (객체)
- name > key

- __console.group__ 을 사용하면 결과값을 더 보기 좋게 정리할 수 있습니다. 

```

console.group('object loop');


var memberObject = {
    manager: 'egoing',
    developer:'grphittie',
    designer: 'leezche'
}




for(var name in memberObject ){ 

    //객체에 있는 원소의 개수만큼 중괄호가 실행됩니다. 
    
    console.log(name);                       // property(key) 출력 
    console.log(name, memberObject[name]);   // property(key), value 출력


}


console.groupEnd('object loop');

```

##  내장 객체 math

- 표준 내장 객체
- https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects

자바스크립트는 미리 정의된 여러가지 기능을 제공합니다.

날짜와 관련된 기능, 수학과 관련된 기능 등 여러가지 기능들이 존재합니다. 

이러한 기능들을 잘 정돈하기 위해서 자바스크립트 개발자들은 객체를 이용하기로 했습니다.

예를 들어 Math라는 객체에는 수학과 관련된 여러 함수들이 그룹화되어 있습니다.






```python
console.log("Math.PI", Math.PI); // 파이 값을 출력합니다.
console.log("Math.random()", Math.random()); // 랜덤 값을 출력합니다.
console.log("Math.floor(3.9)", Math.floor(3.9)); // 값을 반올림합니다.
```

## 객체 생성


- 객체 안에 포함된 함수 'method'
- 객체를 사용하면 관련된 기능을 그룹화하여 편리하게 사용할 수 있습니다.


- {} MyMath 중괄호 객체 생성

```
var MyMath = {
    
    PI: Math.PI,
    
    random:function(){
        return Math.random();
    },
    
    floor:function(val){
        return Math.floor(val);
    }
    
}
```

```
var MyMath_PI = Math.PI;

function MyMath_random(){
    return Math.random();
}
function MyMath_floor(val){
    return Math.floor(val);
}
```

## this

- _어떤 메소드에서 그 메소드가 속해 있는 객체를 가리키는 특수 키워드_
- 객체 내부에서 사용 가능

```
var kim = {

    name: 'kim',
    first: 10,   //첫번째 게임 점수
    second: 20,  // 두번째 게임 점수 
    
    sum:function(f,s){ // 게임 접수 합계 함수
        return f+s;
    }
}

console.log( "kim.sum(kim.first, kim.second)", kim.sum(kim.first, kim.second));

```

```

var kim = {
    
    name: 'kim',
    first:  10,     //첫번째 게임 점수
    second: 20,     // 두번째 게임 점수 
    
    sum:function(){ // 게임 접수 합계 함수
        return this.first+this.second;
    }
}


console.log("kim.sum()",kim.sum());

```


## constructor의 필요성

- 객체 내부에 코드를 추가하다 보면 프로그래밍 상으로 문제는 없지만 **객체 내부의 내용이 바뀌면 같은 동작을 하는 모든 객체의 내용을 바꿔야한다는 단점**이 있습니다.

## 내장 객체 date

- **new 키워드**를 사용하여 새로운 Date 객체를 생성



- .getFullYear() method
- .getMonth() method

```
//2019년 4월 10일의 값을 가지는 Date 객체를 생성합니다.
var d1 = new Date('2019-4-10'); 


// 해당 객체의 년도를 출력합니다.
console.log('d1.getFullYear()',d1.getFullYear()); 


//0부터 카운트하여 해당 객체의 월을 출력합니다.
console.log('d1.getMonth()',d1.getMonth()); 

```

- 이처럼 date 객체를 만드는 공장(new)이 있다면 원하는 값을 가지는 객체를 양산해낼 수 있게 됩니다.

## 생성자 (constructor)


```

function Person(){
    this.name = 'kim';
    this.first = 10;
    this.second = 20;
    this.third = 30;
    this.sum = function(){ 
        return this.first+this.second+this.third;
    }
}

console.log('Person()', Person()); 

```

// result : Person() undefined

- 객체를 생성하는 생성자 **new** 키워드를 사용하여 객체 생성

```
console.log('new Person()', new Person());`
```

- new 키워드로 두개의 객체 생성후 객체내 함수 sum() method 호출

```
var kim = new Person();
var lee = new Person();

console.log("kim.sum()",kim.sum());
console.log("lee.sum()",lee.sum());
```



## 생성자 parameter

생성자 함수가 실행될 때 입력 값을 받도록

```

function Person(name,first,second,third){
    this.name = name;
    this.first = first;
    this.second = second;
    this.third = third;
    this.sum = function(){ 
        return this.first+this.second+this.third;
    }
}


var kim = new Person('kim',10,20,30);
var lee = new Person('lee',10,10,10);

```

## prototype의 필요성



생성자 함수에서는 새로운 객체가 생성될 때 마다, sum이라는 내부 메소드가 새롭게 생성되고 있습니다. 
그만큼 메모리 낭비가 발생해 성능이 떨어지게 됩니다.


sum 이라는 메소드의 내용을 수정하고 싶은 경우, 만들어진 객체만큼 수정 작업을 반복해야한다는 문제가 있습니다. 즉 생산성이 떨어지게 됩니다.



- 만약 Person 이라는 생성자를 이용해서 만든 모든 객체가 공통적으로 사용하는 함수를 만들 수 있다면 어떨까요?
- 공통적으로 사용하는 속성을 만들 수 있다면 어떨까요?




```python
https://developer.mozilla.org/ko/docs/Learn/JavaScript/Objects/Object_prototypes
```

prototype을 이용해 객체의 재사용성을 높일 수 있습니다.


```
function Person(name,first,second,third){
    this.name = name;
    this.first = first;
    this.second = second;
    this.third = third;
    
}

```


- Person 생성자에 prototype에 sum이라는 함수를 정의


```
Person.prototype.sum = function(){ 
    return this.first+this.second+this.third;
}


var kim = new Person('kim',10,20,30);
var lee = new Person('lee',10,10,10);
console.log("kim.sum()",kim.sum());
console.log("lee.sum()",lee.sum());


```


- 생성자 함수 안에 메소드를 정의하는 코드가 들어 있지 않기 때문에, __객체가 생성될 때마다 호출되지 않고 한번만 생성__ 하게 됩니다. 

- 여러개의 객체가 하나의 함수를 공유하므로써 성능을 높이고 메모리를 절약할 수 있습니다.


```
function Person(name,first,second,third){
    this.name = name;
    this.first = first;
    this.second = second;
    this.third = third;
    
}

Person.prototype.sum = function(){ 
    return 'prototype : ' + (this.first+this.second+this.third);
}
```



- 만약 하나의 객체에서만 sum이라는 함수를 다르게 동작시키고 싶다면 어떻게 해야할까요?
- kim이라는 객체에 sum 메소드를 추가


```

var kim = new Person('kim',10,20,30);

kim.sum = function(){
    return 'this : ' + (this.first+this.second+this.third);
}


var lee = new Person('lee',10,10,10);
console.log("kim.sum()",kim.sum());
console.log("lee.sum()",lee.sum());

```



- 자바스크립트는 객체에서 어떠한 메소드 또는 속성을 출력할때, 해당 객체가 그 메소드 또는 속성을 가지고 있는지를 확인합니다.

- 만약 가지고 있다면 객체 내의 메소드 또는 속성을 호출하고, 없다면 이 객체의 생성자의 prototype에 해당 메소드 또는 속성이 정의 되어 있는지를 확인합니다. 



###  생성자를 이용한 객체 생성

- 객체의 속성들 (변수들)은 생성자 함수 안에 넣는 것이 일반적입니다. 

- 객체의 메소드들은 생성자의 prototype에 추가하는 것이 일반적인 패턴입니다. 

```
function Person(name,first,second,third){
    this.name = name;
    this.first = first;
    this.second = second;
    this.third = third;
    
}

Person.prototype.sum = function(){ 
    return 'prototype : ' + (this.first+this.second+this.third);
}
```

## class


```python

```

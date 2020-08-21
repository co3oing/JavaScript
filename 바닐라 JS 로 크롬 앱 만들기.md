# 바닐라 JS로 크롬 앱 만들기

> https://nomadcoders.co/javascript-for-beginners/lobby  
>  코드 작성 : https://repl.it/

## THEORY

### variable

`dayOfWeek` : 변수는 소문자로 시작해서 띄어쓰기 필요시 다음 단어의 첫 글자를 대문자로 작성한다.

`let`

`const` : 변경할 수 없는 상수로 선언한다.

`var`
 
### Array

`dayOfWeek = [];`
 
 ### Object
 
 ```javascript
 const nicoInfo = {
  name : "Nico",
  age : 33,
  favFood : [
    {
      name : "Kimchi", // , 를 빼먹지 않게 조심하자.
      fatty : false
    },
    {
      name : "Cheese burger", // JavaScript에서 "" 와 '' 는 같다.
      fatty : true
    }
  ]
 }
 ```
 
 ## Practice
 
 ### Function
 
 ```javascript
 fuction sayHello() {
  console.log('Hello!');
 }
 
 sayHello();
 ```
 
Object 안에 Fuction을 만들 수 있다.

  ```javascript
 const calculator = {
  plus: fuction(a, b){
   return a + b;
  }
 }
 
 const plus = calculator.plus(5, 5);
 ```
 
 ### String
 
 ```javascript
 console.log("Hello " + name + " you are " + age + " years old");
 ```
 
 ### String Interpolation
 
 ```javascript
 console.log(`Hello ${name} you are ${age} years old`);
 ```

### JS DOM Functions

> DOM = Document Object Model

```javascript
const title = document.getElementById("title");
// querySelector 노드의 첫번째 자식을 반환
const title = document.querySelector("#title"); // ID
const title = document.querySelector(".title"); // Class
```

### Events

```javascript
function handleResize() {
 console.log("I have been resized");
}

// window.addEventListener("resize", handleResize()); 
// handleResize()일 경우함수를 바로 호출한다. 
// 하지만 우리는 "resize"일때만 함수를 호출하기를 원한다.
window.addEventListener("resize", handleResize);
```

```javascript
const title = document.querySelector("#title");

function handleClick() {
 title.style.color = "blue";
}

title.addEventListener("click", handleClick);
```

### DOM if else Function

```javascript
const title = document.querySelector("#title");

const BASE_COLOR = "rgb(52, 73, 94);
const OTHER_COLOR = "#7f8c8d";

function handleClick() {
 const currentColor = title.style.color;
 
 if (currentColor === BASE_COLOR) {
  title.style.color = OTHER_COLOR;
 } else {
  title.style.color = BASE_COLOR;
 }
}

function init() {
 title.stye.color = BASE_COLOR;
 title.addEventListener("click", handleClick); // mouseenter.. MDN을 활용하자
}

init();
```

### DOM if else Function 2

css, javascript를 적절하게 짜는것이 중요하다.

```css
body {
 background-color: #ecf0f1;
}

h1 {
 color: #34495e;
 transition: color 0.5s ease-in-out;
}

.clicked {
 color: #7f8c8d;
}
```

```javascript
const title = document.querySelector("#title");

const CLICKED_CLASS = "clicked";

function handleClick() {
 const currentColor = title.className;
 
 if (currentClass !== CLICKED_CLASS) {
  title.className = CLICKED_CLASS;
 } else {
  title.className = "";
 }
}

function init() {
 title.addEventListener("click", handleClick);
}

init();
```

### contains

```javascript
const hasClass = title.classList.contains(CLICKED_CLASS);

const CLICKED_CLASS = "clicked";

function handleClick() {
 if (!hasClass) {
  title.classList.add(CLICKED_CLASS);
 } else {
  title.classList.remove(CLICKED_CLASS);
 }
}

function init() {
 title.addEventListener("click", handleClick);
}

init();
```

### toggle

contains의 코드와 동일한 동작을 한다.

```javascript
const hasClass = title.classList.contains(CLICKED_CLASS);

const CLICKED_CLASS = "clicked";


function handleClick() {
 title.classList.toggle(CLICKED_CLASS);
}

function init() {
 title.addEventListener("click", handleClick);
}

init();
```

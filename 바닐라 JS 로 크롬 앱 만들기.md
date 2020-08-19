# 바닐라 JS 로 크롬 앱 만들기

> https://nomadcoders.co/javascript-for-beginners/lobby  
>  코드 작성 : https://repl.it/

## THEORY

### variable

> `dayOfWeek` : 변수는 소문자로 시작해서 띄어쓰기 필요시 다음 단어의 첫 글자를 대문자로 작성한다.

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
 fuction sayHello(){
  console.log('Hello!');
 }
 
 sayHello();
 ```
 
 > Object 안에 Fuction을 만들 수 있다.

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
const title = document.querySelector("#title"); // ID
const title = document.querySelector(".title"); // Class
```

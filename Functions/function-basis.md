## Function Declaration
- This is the most normal form of function and it is also known as function statement.
```javascript
function abc() {
    console.log("Himanshu Sharma")
}

abc();
```

## Function Expression
- When any function is stored in a variable it is known as function expression.
```javascript
const result = function () {
    console.log("Himanshu Sharma");
}
result();
```

## Anonymous Function
- A function with no name.
- The function part in the function expression is Anonymous Function as it does not have any name. 
- The function we make while making component in react is an anonymous function. 
- The callbacks are also anonymous function. 


- React component
```javascript
const Navbar = () => {

}
```
- Callback function
```javascript
setTimeout(() => {
    console.log("Himanshu Sharma")
}, 1000);
```

## First Class Functions
- In javascript, functions are treated as first class citizens.
- It means that functions can be assigned to variables, passed as arguments to other functions, and also can be returned as valued from other functions.

```javascript
function square(num) {
    return num * num;
}

function displaySquare(fn) {
    console.log("Square is " + fn(5));
}

displaySquare(square);
```

## IIFE
- It means Immediately Invoked Function Expression.
- It is wrapped inside the small barcket and arguments are passed just after it.
- We don't need to call it. It is immediately called.
```javascript
(function square(num){
    console.log(num * num);
})(5);
```

- Question 2 -> What is the output?

```javascript
(function (x) {
    return (function (y) {
        console.log(x);
    })(2);
})(1);  //1 because of closures.
``` 

## Function Scope
- Example 1 - Take the num1 and num2 from the global scope. Work same with let and const.
```javascript
var num1 = 20,
    num2 = 3,
    name = "Himanshu Sharma";
function multiply() {
    return num1 * num2; 
}
console.log(multiply())  //60
```

- Example 2 - Take the num1 and num2 from the local scope and name from the gloabal scope (Example 1).
```javascript
function getScore() {
    const num1 = 2,
        num2 = 3;

    function add() {
        return name + " scored " + (num1 + num2)
    }
    return add();
}
console.log(getScore()); //Himanshu Sharma scored 5
```

## Hoisting in Functions

- Functions are completely hoisted in javascript which means that they don't become undefined when called without initialization. 

```javascript
functionName1();
function functionName1 () {
    console.log("Himanshu Sharma")
}
```

- Question 2 -> What is the output?
```javascript
functionName();
console.log(x);
function functionName() {
    console.log("Himanshu Sharma")
}
var x = 5;  //Himanshu Sharma and undefined
```
- Question 2 -> What is the output?
```javascript
functionName1();
var x = 10;
function functionName1() {
    console.log(x);   
    var x = 5;
}    // undefined
```

## Params vs Arguments
- Params are passed the the function as parameter. 
- Arguments are passed at the time of calling 

```javascript
function rectangle(num) { //params
    console.log(num * num);
}
rectangle(5); //Arguments
```

## Rest Parameter and Spread Operator
- Rest parameter is used in function paramter.
- Used to collect multiple arguments in single Array.
- Spread Operator is used to split array or objects into individual elements.

- Question 3 -> What is the output?
```javascript
function add(... nums) {
    console.log(nums[0] + nums[1]);
}
```


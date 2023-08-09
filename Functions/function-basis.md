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

## Scope
**There is mainly three types of scope in javascript?**

Global Scope -> When any variables is declared globally.
- Ex ->
```javascript
var a = 5; //Here, var is gloablly declared.
```

Block Scope -> When any variable is declared inside any curly brackets.
- Ex ->
```javascript
{
    var a = 10; //Here, var a can be accessed only in the scope.
}
```
 Function Scope -> When any variable is declared inside any function.
- Ex ->
```javascript
function abc () {
    var a = 10;  //Here, var a can be accessed only inside this function. 
}
```

## Variable Shadowing

- When the variable is decleared in two scopes with the same name.
- Possible with Let and var also.

- Ex -> 
```javascript
const a = 15; 

function answer() {
    const a = 10;  //The value of a will be shadowed inside the function. 
    console.log(a)   // Output - 10
}
answer();

console.log(x);   //Outupt - 15
```

## Illegal Variable Shadowing

- While shadowing the variable it should not cross the boundary. i.e we can shadow var variable with let can const but can't do the opposite.
- When we try to shadow var varibale by let variable it is known as illegal shadowing. It gives  already defined error.

- We can shadow let variable with const varible and vice-versa. 
- Ex -> 

```javascript 
function answer() {
    var a = 10;
    var b = 12;

    if(true) {
        let a = 39;
        var b = 18;
        console.log(a);
        console.log(b);
    }
}
answer();
```

## Variable Declaration wihtout Initialization

```javascript
var a;   //Possible

let a;   //Possible

cont a;  //Not possible
```

## Variable Hoisting

- var, let and const all three variables are hosited in javascript. 
- When we try to access any var varible before initialization. It gives undefined output.
- const and const are hoisted in Temporal Dead Zone. 
- Temporal Dead zone is the time between hosting and value initialization.
- Ex -> 

```javascript
console.log(x);  //undefiend
var x = 10;

console.log(x);  //error and same with const
let x = 10; 
```

## Difference between var, let and const.

- var has global scope while let and const has block scope.
- var can be changed and redefiend.
- Ex -> 

```javascript
var a = 10;
var a = 13;
console.log(a)  //13. can be changed.

var a = 10;
    a = 13;
console.log(a)  //13. can be redefined.
```

- let can be redefined but it can't be changed.
- Ex ->

```javascript
let a = 10;
let a = 13;    // Not possible

var a = 10;
    a = 13;
console.log(a)  //13. can be redefined.
```

- const can neither be redefined or it can be changed.
- Ex ->

```javascript
let a = 10;
let a = 13;    // Not possible

var a = 10;
    a = 13;
console.log(a)  //Not possible
```

## Questions
**1) What is the output?**
```javascript
function  abc () {
    console.log(a);

    var a = 10;
}
abc();  //undefined
```


**2) What is the output?**
```javascript
function abc () {
    console.log(a, b, c);

    const c = 30;
    const b = 20;
    var a = 10;
}   
abc();  //error
```


**3) What is the output?**
```javascript

console.log(count);  //undefined
let count = 1;
var count2 = 2;  

```
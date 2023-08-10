## Arrow Function
- Introduced in ES6 version of javascript.
- Shorthand syntax of declaring a function.


- Example -> 
```javascript 
const add = (a, b) => a + b;
console.log(add(3, 5))
```

## Difference between Arrow function and Normal function

 **1) Declaration Syntax**

- Example -> 
```javascript 
//Normal Function
function add(a, b) {
    return a + b;
}
console.log(add(3, 5))

//Arrow Funtion
const add = (a, b) => {
  return  a + b
};
console.log(add(3, 5))
```

 **2) Implict Return Keyword**

- Example -> 
- In arrow function we can remove the return keyword. 
```javascript 
//Arrow Funtion one liner.
const add = (a, b) => a + b;
console.log(add(3, 5))
```

 **3) Argument keyword**
- We can't have argument keyword in arrow function. 

- Example -> 
```javascript 
//Normal Function
function fn() {
    console.log(arguments);
}
fn(1,3,2);

//Arrow Function
const fnArr = () => {
    console.log(arguments);
}
fnArr(1,3,2);
```

 **4) "this" keyword**
- this keyword inside the normal function points to the local object while this keyword inside the arrow function points to the global object.

- Example ->  What is the outupt?
```javascript 
let user = {
    userName: "Himanshu Sharma",
    rc1: () => {
        console.log("Subscribe to " + this.userName);
    },
    rc2() {
        console.log("Subscibe to " + this.userName);
    },
};
user.rc1(); //undefined because of arrow function.
user.rc2(); //Subscibe to Himanshu Sharma
```
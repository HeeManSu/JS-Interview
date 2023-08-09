## Rest Parameter and Spread Operator
- Rest parameter is used in function paramter.
- Used to collect multiple arguments in single Array.
- Spread Operator is used to split array or objects into individual elements.
- Spread operator also returns an array.

- Example ->
```javascript
function add(... nums) {   //Rest parameter
    console.log(nums[0] + nums[1]);
}
var arr = [5,6];
add(...arr);   //Spread Operator
```

## Questions
- Question 1 -> What is the output?
```javascript
function getItems1(fruitList, favouriteFruit, ...args) {
    return [...fruitList, ...args, favouriteFruit];
}
console.log(getItems1(["banana", "apple"], "pear", "mango", "papaya", "orange"));  
// (6) ['banana', 'apple', 'mango', 'papaya', 'orange', 'pear']
```

- Question 3 -> What is the output?
```javascript
const fn = (a, x, ...numbers, y) => {
    console.log(x, y, numbers);
};
fn(5, 6, 3, 7, 8, 9);

//The correct code is
const fn = (a, x, y , ...numbers) => {
    console.log(x, y, numbers);
};
fn(5, 6, 3, 7, 8, 9);  // 6 3 [7, 8, 9]
```


- Question 2 -> What is the output?
```javascript
 console.log([...'Himanshu']);
 // (8) ['H', 'i', 'm', 'a', 'n', 's', 'h', 'u']
```
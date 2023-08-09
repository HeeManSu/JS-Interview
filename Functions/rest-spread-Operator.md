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
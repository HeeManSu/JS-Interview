## Scope
**There is mainly three types of scope in javascript?**
- 1) Global Scope -> When any variables is declared globally.
- Ex ->
```javascript
var a = 5; //Here, var is gloablly declared.
```

- 2) Block Scope -> When any variable is declared inside any curly brackets.
- Ex ->
```javascript
{
    var a = 10; //Here, var a can be accessed only in the scope.
}
```
- 3) Function Scope -> When any variable is declared inside any function.
- Ex ->
```javascript
function abc () {
    var a = 10;  //Here, var a can be accessed only inside this function. 
}
```
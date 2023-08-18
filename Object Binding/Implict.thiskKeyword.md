## Implict Binding
- It means that the execution of this keyword gets automatically defined.


## What is this keyword?
- this keyword refers to the context or object from which the function is called.
- this keyword only points to its immediate parent object.

## this keyword in global context?
- this points to window obeject.

 **Ex ->** 
```javascript
this.b = 5; //here this points to window object.
```

## this keyword in normal function?
- this keyword inside the normal function targets its function parent object.

 **Ex 1 ->** 
```javascript
this.a = 5;
function getParams() {
    console.log(this.a)
}
getParams(); // 5
//this here target its parent obeject which is window object.
```

 **Ex 2 ->** 
```javascript
let user = {
    name: "Himanshu",
    age: 25,
    getDetails() {
        console.log(this.name);
    }
}
user.getDetails(); //Himanshu   this targets its parent object which is user.
```

 **Ex 3 ->** 
```javascript
let user1 = {
    name: "Himanshu",
    age: 25,
    childObj: {
        newName: "Himanshu Sharma",
        getUserDetails() {
         console.log(this.newName, "and", this.name);
        },
    },
};
user1.childObj.getUserDetails();
// Himanshu Sharma and undefined.
```


## this keyword in arrow function?
- this keyword in the arrow function points its parent function and it takes value from its parent function object.

 **Ex 1 ->** 
```javascript
this.a = 5;
const getParams = () => {
    console.log(this.a);
};
getParams();  //5
//Here, this points to its window object as it does not have any parent function. 
```


 **Ex 2 ->** 
```javascript
let user2 = {
    name: "Himanshu",
    age: 35,
    getDetails: () => {
         console.log(this.name);
    },
};
user2.getDetails(); //error
// because getDetails is a arrow function and it is pointing to window object.
```

 **Ex 3 ->** 
```javascript
let user3 = {
    name: "Himanshu",
    age: 35,
    getDetails() {
        const nestedArrow = () => console.log(this.name);
        nestedArrow();
    },
};
user3.getDetails(); //Himanshu
```
- because this in the arrow function is taking the values from its parent function and its parent function is taking the value of this from the object.

## this keyword inside class/constructor?
- this inside the class refers to the variables inside the constructor. 


 **Ex ->** 
```javascript
class user4 {
    constructor(n) {
        this.name = n;
    }
    getName() {
        console.log(this.name);
    }
}
const User = new user4("Himanshu Sharma");
User.getName(); // Himanshu Sharma
//this here is referring to the variables in the constructor.
```

## Questions?

 **Question 1-> What is the output and which of the firstName is logged and why** 
```javascript
const user5 = {
    firstName: "Himanshu",
    getName() {
        const firstName = "Himanshu Sharma Kumar";
        return this.firstName;
    },
}; 
console.log(user5.getName()); //Himanshu
```
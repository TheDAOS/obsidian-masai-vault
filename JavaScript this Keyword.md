In JavaScript, `this` keyword refers to the object that is currently calling the function

The **`this`** keyword refers to the context where a piece of code, such as a function's body, is supposed to run.

## this Inside Object Method
When `this` is used inside an object's method, `this` refers to the object it lies within. For example,

```js
const person = {
    name : 'Jack',
    age: 25,

    // this inside method
    // this refers to the object itself
    greet() {
        console.log(this);
        console.log(this.name);
    }
}

person.greet();
```

##### Output:
```js
{name: "Jack", age: 25, greet: ƒ}
Jack
```

## this inside Nested Object
```js
const person = {
	name: "Jack",
	age: 25,
	admin: {
		name: "Jane",
		greet() {
			console.log(this);
			console.log(this.name);
		},
	},
};

person.admin.greet();
```

##### Output:
```js
{ name: 'Jane', greet: [Function: greet] }
Jane
```

## this Inside Global Scope
When `this` is used alone, `this` refers to the global object (`window` object in browsers). For example,

```js
let a = this;
console.log(a);  // Window {}


this.name = 'Sarah';
console.log(window.name); // Sarah
Here, this.name is the same as window.name.
```

## this Inside Function
When `this` is used in a function, `this` refers to the global object (`window` object in browsers). For example,

```js
function greet() {

    // this inside function
    // this refers to the global object
    console.log(this);
}

greet(); // Window {}
```

- **Non-Strict Mode:** By default, `this` inside a function will point to the global object (similar to the global context).
- **Strict Mode:** If 'use strict' is declared, then `this` inside a function will be `undefined` unless the function is called as a method of an object, or its `this` value is set explicitly.
	```js
	function showThis() {
	  console.log(this);
	}
	showThis();  // In strict mode, outputs: undefined
	```
- This is because of “this substitution” , whenever value of `this` keyword is undefined or null `this` will be replaced with global object only if use Non-Strict Mode.

## The explicit binding of `this` using call/apply
When a function is called using the `call` or `apply` methods, then `this` refers to the value passed as the first argument of the `call` or `apply` function.

```js
function sayHello() {
	console.log("Hello! ", this);
}

var john = {
	name: "John Doe",
	age: 30
};

var james = {
	name: "James Bond",
	age: 30
};

sayHello.call(james);
sayHello.call(john);
```

## this inside Arrow functions
```js
const person = {
	age: 25,
	logContext: () => {
	    console.log(this);
	},
};

person.logContext();
```

### Behavior:
- When you call `person.logContext();`, the output will show the global `this` context (`window` in a browser environment) rather than the `person` object. This is because arrow functions inherit `this` from their surrounding (lexical) scope rather than binding `this` to the object they belong to.

## Arrow function inside normal function

```js
const person = {
	age: 25,
	name: "Alice",
	logDetails: function() {
		console.log("Outer function this:", this); // this refers to person
		
		const nestedArrowFunction = () => {
		    console.log("Nested arrow function this:", this); // this still refers to person
			console.log(`Name: ${this.name}, Age: ${this.age}`);
	    };
	    
	    nestedArrowFunction();
	}
};

person.logDetails();
```

### Explanation:
#### 1. Outer Function (`logDetails`):
- This is a regular function defined as a method of the `person` object.
- When `logDetails` is called, `this` refers to the `person` object because it's invoked as `person.logDetails()`.

#### 2. Nested Arrow Function (`nestedArrowFunction`):
- The `nestedArrowFunction` is an arrow function defined inside `logDetails`.
- **Arrow Function Behavior:** Arrow functions don't have their own `this`. Instead, they inherit `this` from the surrounding scope where they are defined.
- In this case, `nestedArrowFunction` inherits `this` from `logDetails`, where` `this refers to the `person` object.

#### Calling `logDetails()`:
- When you call `person.logDetails();`, the outer function logs `this`, which refers to `person`.
- The nested arrow function also logs `this`, and it still refers to the `person` object because it inherits `this` from the `logDetails` function.

## Output based Questions

### Question-1
```js
function sayGoodbye() {
  console.log("Good bye! ", this);
}

function sayHello() {
  console.log("Helloo! ", this);
  sayGoodbye();
}

sayHello();
```

### Question-2
```js
const person = {
	name: "John",
	
	sayHello: function () {
		console.log("Hello, my name is " + this.name);
	},
	
	sayDelayedHello: function () {
		setTimeout(function () {
		    console.log("Delayed Hello, my name is " + this.name);
		}, 1000);
	},
	
	sayArrowDelayedHello: function () {
		setTimeout(() => {
		    console.log("Arrow Delayed Hello, my name is " + this.name);
		}, 1000);
	},
};

person.sayHello(); // Output: Hello, my name is John
person.sayDelayedHello(); // Output: Delayed Hello, my name is undefined
person.sayArrowDelayedHello(); // Output: Arrow Delayed Hello, my name is John
```
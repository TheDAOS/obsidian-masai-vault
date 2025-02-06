Arrow functions and normal (traditional) functions in JavaScript differ in several ways, particularly in terms of **syntax**, `this` **binding**, and **usage scenarios**. Here's a detailed breakdown:
***

## 1. Syntax

### Arrow Function
- Shorter and more concise.
- No `function` keyword.
- If there's only one expression, you can omit `{}` and the `return` keyword.
	```js
	const add = (a, b) => a + b;
	
	console.log(add(5, 3)); // Output: 8
	```

### Normal Function
- Requires the `function` keyword.
- Typically uses `{}` to define the function body and `return` for the output.
	```js
	function add(a, b) {
	  return a + b;
	}
	
	console.log(add(5, 3)); // Output: 8
	```
***
## 2. `this` Binding

### Arrow Function
- Does **not** bind its own `this`.
- Inherits `this` from its surrounding (lexical) scope.
- Useful when you want to maintain the context of `this`.

##### Example:
```js
const user = {
  name: "Alice",
  greet: function () {
    const sayHello = () => `Hello, ${this.name}`;
    return sayHello();
  },
};

console.log(user.greet()); // Output: "Hello, Alice"
```

### Normal Function
- Binds its own `this` based on how the function is called (runtime context).
- `this` can vary depending on the caller.

##### Example:
```js
const user = {
  name: "Alice",
  greet: function () {
    function sayHello() {
      return `Hello, ${this.name}`;
    }
    return sayHello();
  },
};

console.log(user.greet()); // Output: "Hello, undefined" (in strict mode)
```
***

## 3. `arguments` Object

### Arrow Function
- Does **not** have its own `arguments` object.
- You must use rest parameters (`...args`) to access arguments.

##### Example:
```js
const arrowFunction = (...args) => args;

console.log(arrowFunction(1, 2, 3)); // Output: [1, 2, 3]
```

### Normal Function
- Has its own `arguments` object, which is an array-like object containing all passed arguments.

##### Example:
```js
function normalFunction() {
  return arguments;
}

console.log(normalFunction(1, 2, 3)); // Output: [1, 2, 3]
```
***
## 4. Constructor Functions

Let's break down the differences between `var`, `let`, and `const` in JavaScript in a way that is simple and easy for beginners to understand.

## 1. `var`:

The `var` keyword has been in JavaScript since the beginning. It was the only way to declare variables before `let` and `const` were introduced. However, `var` has some quirks that can be tricky for beginners, so let's explore its characteristics.

#### Characteristics of `var`:
- **Function Scope**: Variables declared with `var` are function-scoped. This means if you declare a variable inside a function, it is only accessible within that function, but if it's declared outside a function, it's available globally.
- **Hoisting**: When you use `var`, JavaScript hoists the variable to the top of its scope. This means you can use a variable before it's declared, but the value will be `undefined` until the line where the variable is initialized.

	```js
	console.log(myVar); // undefined
	var myVar = 10;
	console.log(myVar); // 10
	```
- **Re-declaration**: You can declare a variable with var more than once in the same scope without an error.
	```js
	var x = 5;
	var x = 10; // No error
	console.log(x); // 10
	```

## 2. `let`:

`let` was introduced in ES6 (2015) to address some of the issues with `var`.

#### Characteristics of `let`:
- **Block Scope**: `let` is block-scoped, which means it's only available inside the block {} where it'
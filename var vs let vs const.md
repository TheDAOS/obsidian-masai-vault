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
- **Block Scope**: `let` is **block-scoped**, which means it's only available inside the block `{}` where it's declared. This block could be an `if` statement, `for` loop, or any pair of curly braces.
	```js
	if (true) {
	    let y = 20;
	    console.log(y); // 20
	}
	console.log(y); // Error: y is not defined
	```

- **No Hoisting**: While technically `let` variables are hoisted, they are not initialized until the code reaches the line where the `let` is declared. This creates what we call a Temporal Dead Zone. If you try to use the variable before that, you'll get a `ReferenceError`.
	```js
	console.log(z); // ReferenceError: z is not defined
	let z = 30;
	```

- **Re-declaration**: You cannot re-declare the same variable in the same scope with `let`. This helps avoid errors caused by accidentally declaring the same variable more than once.
	```js
	let a = 10;
	let a = 20; // Error: Identifier 'a' has already been declared
	```

## 3. const:

`const` is short for "constant," meaning the value assigned to a `const` variable cannot be changed after it's set.

#### Characteristics of `const`:

Block Scope: Like let, const is block-scoped and only accessible within the block it's declared in.
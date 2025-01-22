Assignment operators in JavaScript are used to assign values to variables with varying modifications. These operators simplify writing code that involves arithmetic and assignment simultaneously.

1. **Assignment Operator** (`=`)
	- **Syntax**: `x = y`
	- **Equivalent to**: Direct assignment
	- **Description**: Sets the value of `x` to `y`.
	- **Example**:
		```js
		let x = 5;
		console.log(x);  // Outputs: 5
		```

2. **Addition Assignment Operator** (`+=`)
	- **Syntax**: `x += y`
	- **Equivalent to**: `x = x + y`
	- **Description**: Adds the value of `y` to `x` and assigns the result back to `x`.
	- **Example**:
		```js
		let x = 5;
		x += 3;
		console.log(x);  // Outputs: 8
		```

3. **Subtraction Assignment Operator** (`-=`)
	- **Syntax**: `x -= y`
	- **Equivalent to**: `x = x - y`
	- **Description**: Subtracts the value of `y` from `x` and assigns the result back to `x`.
	- **Example**:
		```js
		let x = 5;
		x -= 2;
		console.log(x);  // Outputs: 3
		```

4. **Multiplication Assignment Operator** (`*=`)
	- **Syntax**: `x *= y`
	- **Equivalent to**: `x = x * y`
	- **Description**: Multiplies `x` by `y` and assigns the result back to `x`.
	- **Example**:
		```js
		let x = 5;
		x *= 3;
		console.log(x);  // Outputs: 15
		```

5. **Division Assignment Operator** (`/=`)
	- **Syntax**: `x /= y`
	- **Equivalent to**: `x = x / y`
	- **Description**: Divides `x` by `y` and assigns the result back to `x`.
	- **Example**:
		```js
		let x = 10;
		x /= 2;
		console.log(x);  // Outputs: 5
		```

6. **Remainder Assignment Operator** (`%=`)
	- **Syntax**: `x %= y`
	- **Equivalent to**: `x = x % y`
	- **Description**: Divides `x` by `y`, calculates the remainder, and assigns it back to `x`.
	- **Example**:
		```js
		let x = 10;
		x %= 3;
		console.log(x);  // Outputs: 1
		```

7. **Exponentiation Assignment Operator** (`**=`)
	- **Syntax**: `x **= y`
	- **Equivalent to**: `x = x ** y`
	- **Description**: Raises x to the power of y and assigns the result back to x.
	- **Example**:
		```js
		let x = 2;
		x **= 3;
		console.log(x);  // Outputs: 8
		```

[[Assignment Operators Assignment]]

### Type Coercion
**Type coercion** refers to the automatic or manual conversion of values from one type to another. JavaScript is a loosely typed language, which means variables can hold different types of values, and type conversion can happen implicitly or explicitly.

### Implicit Type Coercion:
JavaScript automatically converts one data type to another when needed. This often occurs when combining different data types or comparing values.

Examples:
```js
console.log(5 + "5"); // Output: "55" (number is coerced to string)
console.log("5" - 2); // Output: 3 (string is coerced to number)
```

In the first case, JavaScript converts the number `5` to a string and concatenates it with `"5"`. In the second case, JavaScript converts `"5"` to a number and performs the subtraction.

### Explicit Type Coercion:
You can manually convert data types using functions like `Number()`, `String()`, or `Boolean()`.

Examples:
```js
var num = "123";
var convertedNum = Number(num); // Explicitly converting string to number
console.log(convertedNum); // Output: 123

var isTrue = Boolean(1); // Explicitly converting number to boolean
console.log(isTrue); // Output: true
```

### Common Type Coercion Pitfalls:
**Loose Equality (`==`)**: JavaScript uses type coercion when comparing values with `==`. This can lead to unexpected results because JavaScript converts both values to a common type before comparison.

Example:
```js
console.log(1 == "1"); // Output: true (because "1" is coerced to a number)
```

**Strict Equality (`===`)**: Strict equality prevents type coercion and compares values and types directly.

Example:
```js
console.log(1 === "1"); // Output: false (because they are of different types)
```

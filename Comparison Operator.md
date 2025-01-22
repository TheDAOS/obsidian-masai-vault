Comparison operators in JavaScript are used to compare two values, returning a boolean result (`true` or `false`). These operators are fundamental for controlling the flow of logic in scripts based on conditions. Let's delve into each common comparison operator with explanations and examples.

1. **Equal to (`==`)**:
	- **Syntax**: `x == y`
	- **Equivalent to**: Evaluating if `x` is equal to `y` after type conversion.
	- **Description**: Compares two values for equality, converting them to a common type if necessary. It returns `true` if the operands are equal after conversion.
	- **Example**:
		```js
		console.log(5==5);
		console.log("masai"=="masai");
		console.log(5=="5");
		console.log(ram == "ram");
		console.log(5=="ram");
		```

2. **Not Equal to (`!=`)**:
	- **Syntax**: `x != y`
	- **Equivalent to**: Evaluating if `x` is not equal to `y` after type conversion.
	- **Description**: Compares two values for inequality, converting them to a common type if necessary. It returns `true` if the operands are not equal after conversion.
	- **Example**:
		```js
		// Example demonstrating different comparisons using the != operator
		console.log(3 != '3');  // Outputs: false (since '3' is converted to numeric 3)
		console.log('hello' != 'hello');  // Outputs: false (exact match)
		console.log('10' != 10);  // Outputs: false (type conversion equality)
		console.log(0 != false);  // Outputs: false (0 is considered equivalent to false)
		console.log(1 != true);  // Outputs: false (1 is considered equivalent to true)
		console.log('JavaScript' != 'javascript');  // Outputs: true (case-sensitive comparison)
		console.log(2 != '3');  // Outputs: true (2 is not converted to '3')
		```

3. **Greater Than (`>`)**:
	- **Syntax**: `x > y`
	- **Equivalent to**: Checking if `x` is greater than `y`.
	- **Description**: Determines whether the first operand is greater than the second operand. Returns `true` if `x is greater than y`.
	- **Example**:
		```js
		// Example demonstrating different comparisons using the > operator
		console.log(4 > 3);  // Outputs: true
		console.log(5 > 5);  // Outputs: false
		console.log('b' > 'a');  // Outputs: true (based on lexicographical order)
		console.log('apple' > 'banana');  // Outputs: false (lexicographical comparison)
		console.log(10 > '2');  // Outputs: true (numeric comparison after conversion)
		```

4. **Less Than (`<`)**:
	- **Syntax**: `x < y`
	- **Equivalent to**: Checking if `x` is less than `y`.
	- **Description**: Determines whether the first operand is less than the second operand. Returns `true` if `x is less than y`.
	- **Example**:
		```js
		// Example demonstrating different comparisons using the < operator
		console.log(2 < 3);  // Outputs: true
		console.log(3 < 2);  // Outputs: false
		console.log('a' < 'b');  // Outputs: true (based on lexicographical order)
		console.log('banana' < 'apple');  // Outputs: false (lexicographical comparison)
		console.log('2' < 10);  // Outputs: true (numeric comparison after conversion)
		```

5. **Greater Than or Equal to (`>=`)**:
	- **Syntax**: `x >= y`
	- **Equivalent to**: Checking if `x` is greater than or equal to `y`.
	- **Description**: Determines whether the first operand is greater than or equal to the second operand. Returns `true` if `x is greater than or equal to y`.
	- **Example**:
		```js
		// Example demonstrating different comparisons using the >= operator
		console.log(4 >= 4);  // Outputs: true
		console.log(5 >= 4);  // Outputs: true
		console.log(3 >= 4);  // Outputs: false
		console.log('apple' >= 'apple');  // Outputs: true (exact match)
		console.log(10 >= '10');  // Outputs: true (numeric comparison after conversion)
		```

6. **Less Than or Equal to (`<=`)**:
	- **Syntax**: `x <= y`
	- **Equivalent to**: Checking if `x` is less than or equal to `y`.
	- **Description**: Determines whether the first operand is less than or equal to the second operand. Returns `true` if `x is less than or equal to y`.
	- **Example**:
		```js
		// Example demonstrating different comparisons using the <= operator
		console.log(3 <= 3);  // Outputs: true
		console.log(2 <= 3);  // Outputs: true
		console.log(4 <= 3);  // Outputs: false
		console.log('a' <= 'a');  // Outputs: true (exact match)
		console.log('2' <= 10);  // Outputs: true (numeric comparison after conversion)
		```

7. **Strictly Equal to (`===`)**:
	- **Syntax**: `x === y`
	- **Equivalent to**: Checking if `x` is exactly equal to `y` without type conversion.
	- **Description**: Compares two values for equality, without converting them to a common type. Returns `true` if both the value and the type of the two operands are equal.
	- **Example**:
		```js
		// Example demonstrating different comparisons using the === operator
		console.log(3 === '3');  // Outputs: false (no type conversion)
		console.log(4 === 4);  // Outputs: true
		console.log('hello' === 'hello');  // Outputs: true
		console.log(0 === false);  // Outputs: false (strict type checking)
		console.log(1 === true);  // Outputs: false (strict type checking)
		```

8. **Strictly Not Equal to (`!==`)**:
	- **Syntax**: `x !== y`
	- **Equivalent to**: Checking if `x` is not exactly equal to `y` without type conversion.
	- **Description**: Compares two values for inequality, without converting them to a common type. Returns `true` if either the value or the type of the two operands are not equal.
	- **Example**:
		```js
		// Example demonstrating different comparisons using the !== operator
		console.log(3 !== '3');  // Outputs: true (strict type checking)
		console.log(4 !== 4);  // Outputs: false
		console.log('hello' !== 'Hello');  // Outputs: true (case-sensitive and strict type checking)
		console.log(0 !== false);  // Outputs: true (strict type checking)
		console.log(1 !== true);  // Outputs: true (strict type checking)
		```

[[Comparison Operator Assignment]]

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

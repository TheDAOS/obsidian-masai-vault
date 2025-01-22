- Type conversion in JavaScript can be classified into two types: implicit and explicit. Understanding the differences and functionalities of each is crucial for managing data types effectively in your programming tasks.

***
## Implicit Conversion
- Implicit type conversion, also known as coercion, occurs automatically when the operator or function expects a particular data type but is given another. Examples often involve the `+` operator, which can perform both string concatenation and arithmetic addition.

### When a string is involved with the + operator, numbers are converted to strings.
```js
console.log('5' + 2);       // Outputs: "52"
console.log('Hello' + 23);  // Outputs: "Hello23"
console.log('5' + true);    // Outputs: "5true"
console.log('5' + null);    // Outputs: "5null"
```
- **Explanation**:
	1. `'5' + 2`:
		- **Output**: `"52"`
		- **Why**: The number `2` is converted to the string `"2"` and concatenated with `'5'`.
	2. `'Hello' + 23`:
		- **Output**: `"Hello23"`
		- **Why**: The number `23` is converted to the string `"23"` and concatenated with `'Hello'`.
	3. `'5' + true`:
		- **Output**: `"5true"`
		- **Why**: The boolean `true` is converted to the string `"true"` and concatenated with `'5'`.
	3. `'5' + null`:
		- **Output**: `"5null"`
		- **Why**: The `null` value is converted to the string `"null"` and concatenated with `'5'`.

### Non-string values are converted to numbers in operations other than addition
```js
console.log('10' - 5);      // Outputs: 5
console.log('100' * '2');   // Outputs: 200
console.log('100' / '10');  // Outputs: 10
console.log('10' * null);   // Outputs: 0
console.log('100' / true);  // Outputs: 100
```
- **Explanation**:
	1. `'10' - 5`:
		- **Output**: `5`
		- **Why**: The string `'10'` is converted to the number `10`. Subtracting `5` results in `5`.
	2. `'100' * '2'`:
		- **Output**: `200`
		- **Why**: Both strings `'100'` and `'2'` are converted to numbers, resulting in `100 * 2 = 200`.
	3. `'100' / '10'`:
		- **Output**: ``10``
		- **Why**: Both `'100'` and `'10'` are converted to numbers, and dividing `100` by `10` gives `10`.
	4. `'10' * null`:
		- **Output**: `0`
		- **Why**: The string `'10'` converts to the number `10`, and null is treated as `0` in numeric contexts, so `10 * 0 = 0`.
	5. `'100' / true`:
		- **Output**: `100`
		- **Why**: The string `'100'` converts to the number `100`. `true` is treated as `1` in numeric contexts, thus `100 / 1 = 100`.

***
## Explicit Conversion
- Explicit conversion, on the other hand, involves manually converting values from one type to another using JavaScript’s built-in functions, allowing more control over how data is treated.

### Converting to Number
- Converts strings, boolean, and other types to numbers.
```js
console.log(Number("123"));      // Outputs: 123
console.log(Number("123.45"));   // Outputs: 123.45
console.log(Number("123abc"));   // Outputs: NaN
console.log(Number(true));       // Outputs: 1
console.log(Number(false));      // Outputs: 0
console.log(Number(null));       // Outputs: 0
```
### Converting to String
- Converts numbers, boolean, `null`, and `undefined` to strings.
```js
console.log(String(123));        // Outputs: "123"
console.log(String(-0.45));      // Outputs: "-0.45"
console.log(String(true));       // Outputs: "true"
console.log(String(null));       // Outputs: "null"
console.log(String(undefined));  // Outputs: "undefined"
```
### Converting to Boolean
- Converts other types to boolean where `falsy` values (`0`, `"0"`, `""`, `null`, `undefined`, `NaN`) become `false` and all others become `true`.
```js
console.log(Boolean(0));         // Outputs: false
console.log(Boolean(1));         // Outputs: true
console.log(Boolean(""));        // Outputs: false
console.log(Boolean("hello"));   // Outputs: true
console.log(Boolean("false"));   // Outputs: true (interesting case)
console.log(Boolean([]));        // Outputs: true (empty array is true)
console.log(Boolean({}));        // Outputs: true (empty object is true)
console.log(Boolean(null));      // Outputs: false
```

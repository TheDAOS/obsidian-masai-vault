***
JavaScript provides several types of data to store information. These types fall into two categories:
## 1. Primitive Data Types:
- **String**: Textual data wrapped in single, double, or back ticks.
- **Number**: Numeric data, including integers and floating-point numbers.
- **Boolean**: Represents true or false values.
- **Undefined**: A variable declared but not yet assigned a value.
- **Null**: Represents the intentional absence of any value.
- **BigInt**: Represents whole numbers larger than `Number.MAX_SAFE_INTEGER`.
- **Symbol**: Used to create unique and immutable identifiers.

### Example:
```js
var city = "New York";  // String
var score = 99.9;       // Number
var isValid = false;    // Boolean
var bigNum = 9007199254740991n; // BigInt
```

## 2. Non-Primitive Data Types (Reference Types):
- **Object**: Collections of key-value pairs.
- **Array**: Ordered list of values.
- **Function**: Reusable blocks of code.

***
# JavaScript Data types
- JavaScript, a dynamically typed language, supports various data types that can handle different kinds of values. These types are broadly classified into primitive and non-primitive categories.

## Overview of JavaScript Data Types
- Primitive Data Types: These types represent a single simple value and include `String`, `Number`, `BigInt`, `Boolean`, `undefined`, `null`, and `Symbol`.
- Non-Primitive Data Types: These types can hold collections of values and currently include `Object`, `Array` and `function`

1. **String**:
	- Represents textual data enclosed in quotes.
	- Can use single quotes (' '), double quotes (" "), or back ticks (\` \`) for definition.
	- Example: 
		```js
		let fruit = 'apple';
		let country = "USA";
		let result = `pass`;
		```

2. **Number**:
	- Handles both integers and floating-point numbers.
	- Supports special numeric values like `Infinity`, `-Infinity`, and `NaN`.
	- Example:
		```js
		let integer_number = -3;
		let float_number = 3.15;
		```

3. **BigInt**:
	- Used for very large integers beyond the safe range of the regular `Number` type (`±(2^53 - 1)`).
	- Defined by appending `n` to the end of an integer.
	- Example:
		```js
		let largeNumber = 900719925124740999n;
		```

4. **Boolean**:
	- Represents logical entities and can be either `true` or `false`.
	- Commonly used in control flows and conditions.
	- Example:
		```js
		let isAvailable = true;
		```

5. **undefined**:
	- Assigned to variables that are declared but not initialized.
	- Indicates the absence of a value.
	- Example:
		```js
		let name;
		console.log(name);  // undefined
		```

6. **null**:
	- Explicitly denotes a null or "empty" value.
	- Often used to signify the intentional absence of any object value.
	- Example:
		```js
		let age = null;
		```

7. **Symbol**:
	- Introduced in ES 6 to create unique and immutable identifiers for objects.
	- Every symbol value is unique.
	- Example:
		```js
		let id1 = Symbol("id");
		let id2 = Symbol("id");
		console.log(id1 === id2);  // false
		```

8. **Object**:
	- Stores collections of data or more complex entities in key-value pairs.
	- Objects are mutable and can hold a mix of data types.
	- Example:
		```js
		let student = {
		    firstName: "John",
		    lastName: "Doe",
		    class: 10
		};
		```
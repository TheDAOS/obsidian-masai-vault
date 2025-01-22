- The `typeof` operator in JavaScript is a powerful tool used to determine the type of a given variable or expression. This operator is particularly useful when you need to process values differently based on their type or simply perform a quick type check.

### How `typeof` Works
- When you use the `typeof` operator with an operand, it returns a string that represents the type name of the operand. Here are some examples demonstrating how `typeof` is used and what it returns:
```js
// Using typeof with various data types
console.log(typeof undefined);   // Outputs: "undefined"
console.log(typeof 0);           // Outputs: "number"
console.log(typeof 10n);         // Outputs: "bigint"
console.log(typeof true);        // Outputs: "boolean"
console.log(typeof "foo");       // Outputs: "string"
console.log(typeof Symbol("id"));// Outputs: "symbol"

// Using typeof with built-in objects and functions
console.log(typeof Math);    // Outputs: "object"
console.log(typeof null);    // Outputs: "object" - historical JavaScript quirk
```
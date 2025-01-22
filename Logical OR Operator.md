+ The logical OR operator in JS is used to evaluate two expressions and returns `true` if at least one of the expressions is `true`. It only returns `false` if both expressions are `false`.

###### Syntax
- Using `or`: `expression1 or expression2`
- Using `||`: `expression1 || expression2`

###### Truth Table:
| Expression1 | Expression2 | Result |
| ----------- | ----------- | ------ |
| true        | true        | true   |
| true        | false       | true   |
| false       | true        | true   |
| false       | false       | false  |

### Basic Usage with Boolean Values
In its simplest form, the Logical OR evaluates boolean expressions:
```js
var a = true;
var b = true;

var c = a || b;
console.log(c);

a = true;
b = false;
console.log(a||b);

a = false;
b = true;
console.log(a||b);

a = false;
b = false;
console.log(a||b);
```
**Rule**: The OR operator returns `true` if at least one of the operands is `true`; it returns `false` only if all operands are `false`.

### Non-Boolean Operands
When operands are not boolean values, OR evaluates them for their "truthiness" or "falsiness". 

For example:
```js
console.log(1 || 0); // Outputs: 1 (1 is truthy, 0 is falsy)
console.log(null || "hello"); // Outputs: "hello" (null is falsy, "hello" is truthy)
```

- **Truthy values**: Most values are truthy except for a few "falsy" values.
- **Falsy values**: `false`, `0`, `""` (empty string), `null`, `undefined`, and `NaN`.

## OR `||` finds the first truthy value

Given multiple OR’ed values:
```js
result = value1 || value2 || value3;
```

The OR `||` operator does the following:
- Evaluates operands from left to right.
- For each operand, converts it to boolean. If the result is `true`, stops and returns the original value of that operand.
- If all operands have been evaluated (i.e. all were `false`), returns the last operand.

A value is returned in its original form, without the conversion.

In other words, a chain of OR `||` returns the first truthy value or the last one if no truthy value is found.

For instance:
```js
console.log( 1 || 0 ); // 1 (1 is truthy)
console.log( null || 1 ); // 1 (1 is the first truthy value)
console.log( null || 0 || 1 ); // 1 (the first truthy value)
console.log( undefined || null || 0 ); // 0 (all falsy, returns the last value)
```


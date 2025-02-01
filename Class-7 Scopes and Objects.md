[[var vs let vs const]]
[[Ternary Operators]]
[[JavaScript Objects]]
***[[Scope of Variables And Anonymous Functions]]***

## 1. `let` and `const` Declarations: Block Scoping Rules

`let` and `const` were introduced in **ES6** and differ from the traditional `var` in that they follow **block scoping**.

### Block Scoping
Variables declared with `let` or `const` are scoped to the block in which they are defined, which means they are only accessible inside the pair of `{}` where they were declared.

##### Example:
```js
if (true) {
  let a = 10;
  const b = 20;
  console.log(a);  // Output: 10
  console.log(b);  // Output: 20
}

console.log(a);  // Error: a is not defined
console.log(b);  // Error: b is not defined
```
In this example, both `a` and `b` are only accessible within the `if` block. Attempting to access them outside the block will result in an error.

### When to use `let` and `const`:
- Use `let` for variables that you intend to reassign later.
- Use `const` for variables that should remain constant after their initial assignment.

***
## 2. Differences Between `var`, `let`, and `const`

### `var`:
1. **Scope**: `var` is **function-scoped** or **globally-scoped** if declared outside a function. It **ignores block scope**.
2. **Hoisting**: Variables declared with `var` are hoisted to the top of their scope but initialized with `undefined`.
3. **Reassignment**: `var` variables can be reassigned.

##### Example of `var`:
```js
console.log(x);  // Output: undefined (due to hoisting)
var x = 5;
console.log(x);  // Output: 5

if (true) {
  var y = 10;
}
console.log(y);  // Output: 10 (no block scope for `var`)
```

### `let`:
1. **Scope**: `let` is **block-scoped**, meaning it only exists within the block `{}` where it was defined.
2. **Hoisting**: `let` is hoisted but is **not initialized**. It remains in the **Temporal Dead Zone** (TDZ) until its initialization.
3. **Reassignment**: `let` allows reassignment after declaration.

##### Example of `let`:
```js
console.log(z);  // Error: Cannot access 'z' before initialization
let z = 10;
console.log(z);  // Output: 10

if (true) {
  let a = 20;
}
console.log(a);  // Error: a is not defined (due to block scope)
```

### `const`:
1. **Scope**: Like `let`, `const` is **block-scoped**.
2. **Hoisting**: `const` is hoisted but remains in the **TDZ** until initialized.
3. **Reassignment**: `const` cannot be reassigned. However, if it refers to an object or array, the contents of the object or array can still be modified.

##### Example of `const`:
```js
const b = 30;
b = 40;  // Error: Assignment to constant variable

const obj = { key: "value" };
obj.key = "new value";  // This is allowed because the object itself isn't reassigned, just modified

console.log(obj);  // Output: { key: "new value" }
```
***
## 3. Temporal Dead Zone (TDZ)
The **Temporal Dead Zone (TDZ)** is the time between the start of the execution context and the point where a variable is declared. Variables declared with `let` and `const` exist in the TDZ until their declaration is encountered, which means they cannot be accessed before initialization.

##### Example of TDZ:
```js
console.log(x);  // Error: Cannot access 'x' before initialization
let x = 5;
```
The variable `x` is hoisted but remains in the TDZ until the `let` declaration is encountered. Therefore, accessing `x` before its declaration throws an error.

### Key Points:
- **TDZ** applies to both `let` and `const`.
- Variables in the TDZ cannot be accessed or initialized until the code execution reaches the variable declaration.
***
## 4. Block Scope: Variables Inside `{}`
Variables declared inside a block (with `let` or `const`) are only accessible within that block. This prevents unintended side effects caused by variables leaking out of the block.

##### Example:
```js
if (true) {
  let message = "Hello";
  const number = 123;
  console.log(message);  // Output: Hello
}

console.log(message);  // Error: message is not defined
console.log(number);  // Error: number is not defined
```
In this case, both `message` and `number` are limited to the block inside the `if` statement and cannot be accessed outside it.
***
## 5. Immutability with `const`: When and How to Use `const`
`const` creates a read-only reference to a value. However, it does not make the value itself immutable—just the variable binding. For primitive values like numbers or strings, the value itself is immutable. For objects and arrays, their properties or elements can be modified, but the reference itself cannot be reassigned.

##### Example of `const` with Objects:
```js
const car = { make: "Toyota", model: "Corolla" };
car.model = "Camry";  // Allowed: Modifying object properties

console.log(car);  // Output: { make: "Toyota", model: "Camry" }

car = { make: "Honda", model: "Civic" };  // Error: Assignment to constant variable
```
- **Use `const` for**: Variables that should never be reassigned, like configuration constants, fixed values, or objects whose reference should remain constant.
***

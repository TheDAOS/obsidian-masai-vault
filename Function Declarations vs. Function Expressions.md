## 1. Function Declaration

A **function declaration** defines a named function using the `function` keyword. Function declarations are hoisted, meaning they can be used before they are declared in the code.

##### Syntax:
```js
function functionName(parameters) {
  // Function body
  return value;
}
```

##### Example:
```js
function greet() {
  console.log("Hello, world!");
}

greet();  // Output: Hello, world!
```

- **Hoisting**: Function declarations are hoisted to the top of their scope, so they can be called before the declaration in the code.

### Example of Hoisting:
```js
greet();  // Output: Hello!
function greet() {
  console.log("Hello!");
}
```

## 2. Function Expression

A **function expression** defines a function and assigns it to a variable. Function expressions are not hoisted, meaning they cannot be called before they are defined in the code.

##### Syntax:
```js
const functionName = function(parameters) {
  // Function body
  return value;
};
```

##### Example:
```js
const greet = function() {
  console.log("Hello, world!");
};

greet();  // Output: Hello, world!
```

- **No Hoisting**: Function expressions are not hoisted, so they must be declared before they are invoked.

### Example (No Hoisting):
```js
greet();  // Error: Cannot access 'greet' before initialization
const greet = function() {
  console.log("Hello!");
};
```

## Differences Between Function Declarations and Expressions

| Aspect               | Function Declaration                                               | Function Expression                                               |
| -------------------- | ------------------------------------------------------------------ | ----------------------------------------------------------------- |
| **Hoisting**         | Hoisted to the top of their scope                                  | Not hoisted                                                       |
| **Naming**           | Must have a name                                                   | Can be anonymous or assigned to a variable                        |
| **Use case**         | Best for defining functions that will be used throughout your code | Best for defining functions conditionally or for use as callbacks |
| **Execution Timing** | Can be invoked anywhere within the scope                           | Must be defined before it can be invoked                          |

### When to Use Each
- **Function Declarations**: Use when you need to define utility functions that are used throughout your code or when hoisting is useful (e.g., reusable functions in a large program).
- **Function Expressions**: Use when you need a function that is declared conditionally or when you want to store functions in variables (e.g., for callbacks or event handlers).
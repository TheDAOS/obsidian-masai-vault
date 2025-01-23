[[Functions Unleashed in JavaScript]]

## Functions in JavaScript: Declarations, Expressions, Parameters, Arguments, and Return Statements

### Learning Objectives

By the end of this lesson, you will understand:
- The differences between function declarations and function expressions.
- How to pass data into functions using parameters and arguments.
- How to return data from functions using the `return` statement.
- The difference between local and global scope in JavaScript.
- How anonymous functions work and common use cases for them.
- Best practices for naming conventions and writing modular code.

### Introduction
Functions are fundamental building blocks in JavaScript that allow you to encapsulate code into reusable blocks. Understanding the different ways to define functions, how to pass data into them, and how to return data from them is crucial for writing modular and efficient code.

### Key Concepts and Definitions

#### Function Declarations vs. Function Expressions

#### 1. Function Declaration

A function declaration defines a named function using the function keyword. Function declarations are hoisted, meaning they can be used before they are declared in the code.

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

##### Example of Hoisting:
```js
greet();  // Output: Hello!
function greet() {
  console.log("Hello!");
}
```

#### 2. Function Expression
A **function expression** defines a function and assigns it to a variable. Function expressions are not hoisted, meaning they cannot be called before they are defined in the code.

##### Syntax:
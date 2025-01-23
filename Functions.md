
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

##### Example (No Hoisting):
```js
greet();  // Error: Cannot access 'greet' before initialization
const greet = function() {
  console.log("Hello!");
};
```

#### Differences Between Function Declarations and Expressions
| Aspect               | Function Declaration                                               | Function Expression                                               |
| -------------------- | ------------------------------------------------------------------ | ----------------------------------------------------------------- |
| **Hoisting**         | Hoisted to the top of their scope                                  | Not hoisted                                                       |
| **Naming**           | Must have a name                                                   | Can be anonymous or assigned to a variable                        |
| **Use case**         | Best for defining functions that will be used throughout your code | Best for defining functions conditionally or for use as callbacks |
| **Execution Timing** | Can be invoked anywhere within the scope                           | Must be defined before it can be invoked                          |

#### When to Use Each
- **Function Declarations**: Use when you need to define utility functions that are used throughout your code or when hoisting is useful (e.g., reusable functions in a large program).
- **Function Expressions**: Use when you need a function that is declared conditionally or when you want to store functions in variables (e.g., for callbacks or event handlers).
***

## Parameters and Arguments: Passing Data into Functions

### Parameters
Parameters are placeholders used in function definitions to represent the data that will be passed into the function.

##### Syntax:
```js
function functionName(parameter1, parameter2) {
  // Use parameter1 and parameter2
}
```

##### Example:
```js
function greet(name) {
  console.log("Hello, " + name);
}

greet("Alice");  // Output: Hello, Alice
```

In this example, `name` is a parameter, and the function uses it to greet the person whose name is passed as an argument.

### Arguments

Arguments are the actual values passed into the function when it is invoked. They are mapped to the corresponding parameters in the function.

##### Syntax:
```js
functionName(argument1, argument2);
```

##### Example:
```js
function add(a, b) {
  return a + b;
}

console.log(add(3, 4));  // Output: 7
```

In this example, `3` and `4` are arguments passed into the function, and they correspond to the parameters `a` and `b`.

### Multiple Parameters and Arguments

You can define a function with multiple parameters and pass multiple arguments to it.

```js
function multiply(x, y) {
  return x * y;
}

console.log(multiply(5, 10));  // Output: 50
```

### Default Parameters

You can provide default values for parameters in case no arguments are passed.

```js
function greet(name = "Guest") {
  console.log("Hello, " + name);
}

greet();           // Output: Hello, Guest
greet("John");     // Output: Hello, John
```

#### Rest Parameters (`...`)

Rest parameters allow you to handle an indefinite number of arguments as an array.

```js
function sum(...numbers) {
  let total = 0;
  for (let num of numbers) {
    total += num;
  }
  return total;
}

console.log(sum(1, 2, 3, 4, 5));  // Output: 15
```
***

## Return Statements: Outputting Data from Functions

The `return` statement is used to return a value from a function. When the `return` statement is encountered, the function execution stops, and the value is returned to the point where the function was called.

##### Syntax:

```js
function functionName(parameters) {
  return value;
}
```


#### Example 1: Returning a Value

```js
function add(a, b) {
  return a + b;
}

let result = add(2, 3);
console.log(result);  // Output: 5
```

In this example, `add(2, 3)` returns `5`, which is stored in the `result` variable.

#### Example 2: Returning Early

You can use the `return` statement to exit the function early.

```js
function checkAge(age) {
  if (age < 18) {
    return "Underage";
  }
  return "Adult";
}

console.log(checkAge(16));  // Output: Underage
console.log(checkAge(20));  // Output: Adult
```

In this example, the function returns `"Underage"` if the condition is met, exiting the function early and skipping the rest of the code.

#### Functions Without a Return Statement

If a function does not have a `return` statement, it implicitly returns `undefined`.

```js
function greet() {
  console.log("Hello!");
}

let result = greet();  // Output: Hello!
console.log(result);   // Output: undefined
```
***

## Step-by-Step Explanation

### Example 1: Function Declaration with Parameters and a Return Statement
```js
function square(number) {
  return number * number;
}

let result = square(5);
console.log(result);  // Output: 25
```

### Example 2: Function Expression with Default Parameters and Return
```js
const greet = function(name = "Guest") {
  return "Hello, " + name;
};

console.log(greet());         // Output: Hello, Guest
console.log(greet("Alice"));  // Output: Hello, Alice
```

### Example 3: Using Rest Parameters
```js
function findMax(...numbers) {
  return Math.max(...numbers);
}

console.log(findMax(1, 3, 5, 7, 9));  // Output: 9
```
***

## Practice Exercises

1. **Exercise 1**: Write a function declaration named `subtract` that takes two parameters and returns their difference.
2. **Exercise 2**: Write a function expression named `multiply` that takes two parameters and returns their product.
3. **Exercise 3**: Write a function named `greetUser` that takes a `name` parameter with a default value of `"Guest"` and returns a greeting message.
4. **Exercise 4**: Write a function named `sumAll` that uses rest parameters to return the sum of an arbitrary number of arguments.
***

## Summary

- **Function declarations** define named functions and are hoisted, allowing them to be used before they are declared.
- **Function expressions** assign a function to a variable and are not hoisted.
- **Parameters** are placeholders used in function definitions, while arguments are the actual values passed into the function during invocation.
- The `return` statement is used to return a value from a function and terminate its execution.

## Additional Resources
[MDN: # Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)

***

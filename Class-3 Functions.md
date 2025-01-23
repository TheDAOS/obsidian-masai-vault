
[[Functions]]

## Scope of Variables, Anonymous Functions, and Best Practices in JavaScript

### Introduction

In JavaScript, variables have a defined scope that determines where they can be accessed in your program. Additionally, understanding anonymous functions and how to follow best practices for naming and modularizing code will help you write more maintainable and readable code.

### Key Concepts and Definitions

#### Scope of Variables: Local vs. Global

In JavaScript, scope refers to the visibility or accessibility of variables and functions in different parts of your code. Variables can be classified into two main categories based on their scope: local scope and global scope.

#### Global Scope

- Variables declared outside of any function have global scope and can be accessed from anywhere in the program.
- They remain in memory throughout the execution of the program.

##### Example:
```js
let globalVar = "I'm global!";

function showGlobal() {
  console.log(globalVar);  // Can access globalVar from inside the function
}

showGlobal();  // Output: I'm global!
```

#### Local Scope

Variables declared inside a function or block (with let or const) are said to have local scope. They can only be accessed from within the function or block where they are defined.

They are created when the function is called and destroyed when the function finishes executing.

##### Example:
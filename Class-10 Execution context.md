## JavaScript Execution Context
The execution context in JavaScript is a fundamental concept that helps understand how JavaScript code is executed. It defines the environment in which JavaScript code is evaluated and executed. There are three types of execution contexts: Global Execution Context, Function Execution Context, and Eval Execution Context.

## 1. Global Execution Context
The Global Execution Context is the default context in which the JavaScript code runs. It is created when the JavaScript engine starts executing the script. This context includes:

- **Global Object**: In a browser, this is the `window` object. In Node.js, it is the `global` object.
- **`this` Binding**: In the global context, `this` refers to the global object.
- **Outer Environment**: In the global context, there is no outer environment.
- **Variable Object**: Contains all the variables and functions declared in the global scope.

##### Example:
```javascript
var globalVar = "I am global";

function globalFunction() {
    console.log("I am a global function");
}

console.log(globalVar); // Output: I am global
globalFunction(); // Output: I am a global function
```

## 2. Function Execution Context
A Function Execution Context is created whenever a function is invoked. Each function call creates a new execution context. This context includes:

- **Function Object**: The function being executed.
- **`this` Binding**: The value of `this` depends on how the function is called.
- **Outer Environment**: The lexical environment of the parent function or the global context if the function is not nested.
- **Variable Object**: Contains the arguments passed to the function and the variables and functions declared within the function.

##### Example:
```javascript
function exampleFunction(param) {
    var localVar = "I am local";
    console.log(param); // Output: I am a parameter
    console.log(localVar); // Output: I am local
}

exampleFunction("I am a parameter");
```

## 3. Eval Execution Context
The Eval Execution Context is created when the `eval` function is called. The `eval` function evaluates a string of JavaScript code and executes it in the current execution context. This context is similar to the function execution context but is less commonly used due to performance and security concerns.

##### Example:
```javascript
var x = 10;
eval("var x = 20; console.log(x);"); // Output: 20
console.log(x); // Output: 20
```

### Execution Context Stack
The JavaScript engine uses a stack data structure to manage execution contexts. When a function is called, a new execution context is pushed onto the stack. When the function returns, the execution context is popped off the stack. The stack ensures that the most recent execution context is always at the top.

##### Example:
```javascript
function firstFunction() {
    console.log("First function");
    secondFunction();
}

function secondFunction() {
    console.log("Second function");
}

firstFunction();
```

In this example, the execution context stack would look like this:
1. Global Execution Context
2. `firstFunction` Execution Context
3. `secondFunction` Execution Context

### Lexical Environment
The lexical environment is a component of the execution context that stores information about the identifiers (variables and functions) that are accessible in the current context. It consists of:

- **Environment Record**: Stores the actual bindings of variables and functions.
- **Outer Lexical Environment Reference**: A reference to the parent lexical environment.

##### Example:
```javascript
var globalVar = "I am global";

function outerFunction() {
    var outerVar = "I am outer";

    function innerFunction() {
        var innerVar = "I am inner";
        console.log(globalVar); // Accessible
        console.log(outerVar); // Accessible
        console.log(innerVar); // Accessible
    }

    innerFunction();
}

outerFunction();
```
In this example, the lexical environment of `innerFunction` includes references to `globalVar` and `outerVar` from the outer lexical environments.

## Conclusion
Understanding the execution context is crucial for grasping how JavaScript code is executed, especially when dealing with scope, closures, and asynchronous operations. By knowing how execution contexts are created, managed, and destroyed, developers can write more efficient and predictable JavaScript code.
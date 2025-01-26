## Anonymous Functions in JavaScript

Anonymous functions in JavaScript are functions that do not have a name. They are often used when you need a function for a short period, like for an event handler or as an argument to another function. These functions are also sometimes called "lambda functions" or "function expressions."

### Creating an Anonymous Function

Anonymous functions are defined using the `function` keyword, followed by parameters (if any) and the function body enclosed in curly braces `{}`. Here's the basic syntax:
```js
const variable = function(parameter) {
    // function body
};
```

### Example of an Anonymous Function

Here's a simple example where an anonymous function is used to add two numbers:
```js
const add = function(a, b) {
    return a + b;
};

console.log(add(1, 2)); // Outputs: 3
```

- **How It Works:**
	- The anonymous function takes two parameters, `a` and `b`.
	- It returns the sum of `a` and `b`.
	- This function is stored in a variable named `add`.
	- You can call this function using `add(1, 2)`, which will return `3`.


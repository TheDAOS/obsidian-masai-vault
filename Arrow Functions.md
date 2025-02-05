Arrow functions, introduced in ES6 (ECMAScript 2015), offer a more concise syntax for writing functions. They're particularly useful for simplifying short functions and maintaining lexical `this` context.

Let's first explore how a normal function looks and then convert it step-by-step into an **arrow function**.

## 1. Normal Function Declaration
Here’s how we typically declare a function in JavaScript:

```js
function greet(name) {
  return "Hello, " + name;
}

console.log(greet("John")); // Output: Hello, John
```
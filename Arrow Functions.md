Arrow functions, introduced in ES6 (ECMAScript 2015), offer a more concise syntax for writing functions. They're particularly useful for simplifying short functions and maintaining lexical `this` context.

Let's first explore how a normal function looks and then convert it step-by-step into an **arrow function**.

## Normal Function Declaration
Here’s how we typically declare a function in JavaScript:

```js
function greet(name) {
  return "Hello, " + name;
}

console.log(greet("John")); // Output: Hello, John
```

## Steps to Convert to Arrow Function:

### Step 1: Remove the `function` keyword
In an arrow function, you do not need to use the `function` keyword.

```js
const greet = (name) => {
  return "Hello, " + name;
}
```

### Step 2: Omit the parentheses if there is only one parameter
If the function takes only one argument, you can remove the parentheses around the parameter.

```js
const greet = name => {
  return "Hello, " + name;
}
```

### Arrow Function - Final Form:
```js
const greet = name => "Hello, " + name;
console.log(greet("John")); // Output: Hello, John
```

## Another Example for Practice:

### Normal Function:
```js
function add(a, b) {
  return a + b;
}

console.log(add(5, 3)); // Output: 8
```

### Step-by-Step Conversion:

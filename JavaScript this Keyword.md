In JavaScript, `this` keyword refers to the object that is currently calling the function

The **`this`** keyword refers to the context where a piece of code, such as a function's body, is supposed to run.

## this Inside Global Scope
When `this` is used alone, `this` refers to the global object (`window` object in browsers). For example,

```js
let a = this;
console.log(a);  // Window {}


this.name = 'Sarah';
console.log(window.name); // Sarah
Here, this.name is the same as window.name.
```


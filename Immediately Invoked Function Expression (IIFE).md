An **Immediately Invoked Function Expression (IIFE)** is an anonymous function that is executed immediately after it's defined. This is useful for creating a new scope and avoiding polluting the global scope.

##### Syntax:
```js
(function() {
  console.log("IIFE is running!");
})();
```

##### Example:
```js
(function() {
  let privateVar = "This is private!";
  console.log(privateVar);  // Output: This is private!
})();
```

In this example, the function is executed immediately, and `privateVar` is only accessible within that function, avoiding global scope pollution.

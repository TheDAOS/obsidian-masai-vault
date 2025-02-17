`...rest` allow a function work with a variable number of arguments by bundling them into an array

## Handling Multiple Arguments in JavaScript Functions

### Fixed Parameters and Their Limitations
When defining a function with a fixed number of parameters, like:
```js
function sum(num1, num2) {
    console.log(num1 + num2);
}
```
This function will only handle the exact number of arguments it is expecting. Any extra arguments passed will be ignored.

##### Example:
```js
sum(20, 30);           // Output: 50
sum(20, 30, 40);       // Output: 50 (extra argument ignored)
sum(20, 30, 40, 50);   // Output: 50 (extra arguments ignored)
```

#### Problem:
- **Limited Functionality:** This method is rigid and can’t handle a dynamic number of arguments.
- **Extra Arguments Ignored:** Any additional arguments passed to the function are ignored if not explicitly defined in the function signature.
***

### Using the `arguments` Object
To work around this limitation, JavaScript provides the built-in `arguments` object, which contains all the arguments passed to the function, regardless of the function signature. While the `arguments` object is array-like, it is not a true array (so it doesn't have access to array methods).

##### Example using `arguments`:
```js
function sum() {
    let sum = 0;
    for (let i = 0; i < arguments.length; i++) {
        sum += arguments[i];
    }
    console.log(sum);
}

sum(20, 30);           // Output: 50
sum(20, 30, 40);       // Output: 90
sum(20, 30, 40, 50);   // Output: 140
```

#### Explanation:

1. **No Parameters Defined:** The function doesn’t explicitly define any parameters but can still handle any number of arguments.
2. **Using `arguments`:** A `for...in` loop is used to iterate through the `arguments` object and sum the values passed to the function.

#### Drawbacks of Using `arguments`:
- The `arguments` object is not a true array, so methods like `.map()`, `.reduce()`, or `.filter()` are unavailable without converting it to an array.
- It is considered outdated in modern JavaScript (ES6+), and cleaner alternatives exist, such as the **rest operator**.


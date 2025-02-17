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

### Drawbacks of Using `arguments`:
- The `arguments` object is not a true array, so methods like `.map()`, `.reduce()`, or `.filter()` are unavailable without converting it to an array.
- It is considered outdated in modern JavaScript (ES6+), and cleaner alternatives exist, such as the **rest operator**.

## Handling Non-Numeric Arguments:

### Problem: What Happens When Non-Numeric Arguments Are Passed?
The function with the rest operator works perfectly when all the arguments passed are numbers. However, if any of the arguments are strings or non-numeric, the function will behave unexpectedly because JavaScript’s `+` operator performs concatenation when it encounters a string.

##### Example of Non-Numeric Argument:
```js
function sum(name, ...args) {
    let sum = 0;
    for (let i in args) {
        sum += args[i];
    }
    console.log(sum);
    console.log(name);
}

sum("Nick", 20, 30);            // Output: 50, "Nick"
sum("Nick", 20, 30, "40");      // Output: "5030", "Nick"
sum("Nick", 20, "30", 40, 50);  // Output: "20304050", "Nick"
```

#### Explanation:
- If one or more arguments passed after `name` are strings (e.g., `"40"`), JavaScript will concatenate the values instead of performing arithmetic addition.
	**Example:**
	```js
	sum("Nick", 20, 30, "40");  // Output: "5030", "Nick"
	```

- When a string is added to a number, the result is a concatenated string, which can lead to incorrect results when working with mixed data types.
***
### Fixing the Issue:
To fix this, you need to ensure that the function only sums numeric values and ignores or handles non-numeric values (like strings).

#### Updated Function:
```js
function sum(name, ...args) {
    let sum = 0;
    for (let i in args) {
        // Check if the value is a number before adding
        if (typeof args[i] === 'number') {
            sum += args[i];
        }
    }
    console.log(sum);
    console.log(name);
}

sum("Nick", 20, 30, "40");      // Output: 50, "Nick"
sum("Nick", 20, 30, 40, 50);    // Output: 140, "Nick"
sum("Nick", 20, "30", 40);      // Output: 60, "Nick"
```

#### Explanation:
1. **Type Checking:** Inside the loop, the function checks the type of each argument using `typeof args[i] === 'number'`.
2. **Sum Only Numbers:** Only if the argument is a number, it gets added to the sum.
3. **Handles Strings:** Non-numeric values, like strings, are ignored for the purpose of summing, so they don't affect the result.
***


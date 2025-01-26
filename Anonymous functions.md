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

### Benefits of Anonymous Functions

- **Flexibility**: They can be defined right where they are needed.
- **Conciseness**: Reduces the verbosity of syntax when a function is used only once or in a limited scope.
- **Encapsulation**: Keeps the functionality contained without cluttering the global namespace.
Anonymous functions are powerful tools in JavaScript that help make your code more modular and maintainable. They allow you to define functionality on-the-fly without needing to declare a named function, which is particularly useful for operations that don't need to be reused elsewhere in your code.


[[Anonymous functions Assignment]]
***
### Task 6: Count Vowels

**Description:**
Write an anonymous function to count the number of vowels in a given string. Store it in a variable named `countVowels`. Call the function with `"hello world"`, and print the result.

**Solution:**
```js
const countVowels = function(str) {
    let count = 0;
    const vowels = "aeiouAEIOU";
    for (let i = 0; i < str.length; i++) {
        if (vowels.includes(str[i])) {
            count++;
        }
    }
    return count;
};

console.log(countVowels("hello world")); // Output: 3
```


## Create a JavaScript Function
We can create a function in JavaScript using the `function` keyword:

```js
function greet() {
    console.log("Hello World!");
}
```

#### Create a JavaScript Function

- Here, we have created a simple function named `greet()` that prints `Hello World!` on the screen.

Our function contains the following parts:
- **Function Keyword** - The `function` keyword is used to create the function.
- **Function Name** - The name of the function is `greet`, followed by parentheses `()`.
- **Function Body** - The code that is executed when we call the function. In our case, it is `console.log("Hello World!")`;

## Call a Function
Previously, we declared a function named `greet()`:

```js
function greet() {
   console.log("Hello World!");
}
```

If we run the above code, we won't get any output. But why?

It's because creating a function doesn't mean we are executing the code inside it. In other words, the function is ready and available for us to execute whenever we choose.

And if we want to use the function, we need to call it.

##### Function Call
```js
greet();
```

As you can see, we call a function by writing the function name (greet) followed by parentheses `()`.

## Example 1: JavaScript Function Call
```js
// create a function
function greet() {
    console.log("Hello World!");
}

// call the function
greet();

console.log("Outside function");
```

##### Output
```js
Hello World!
Outside function
```

In the above example, we created a function named `greet()`. Here's how the control of the program flows:

#### Working of a Function in JavaScript

Here,
- When the `greet()` function is called, the program's control transfers to the function definition.
- All the code inside the function is executed (`Hello World!` is printed).
- The program control then jumps to the next statement after the function call (`Outside function` is printed).

### Student task:

#### Description:

Create a function named `showDateTime` that prints the current date and time using `console.log()`. Call the function to display the current date and time.

##### Solution:

```js
function showDateTime() {
    const now = new Date();
    console.log("Current Date and Time: " + now);
}

// Call the function
showDateTime();
```

Problem 5: Write a function to replace spaces in a given string with - .
```js
function replaceSpaces(str) {
    let result = '';
    for (let i = 0; i < str.length; i++) {
        if (str[i] === ' ') {
            result += '-'; // Replace space with '-'
        } else {
            result += str[i]; // Append the character as is
        }
    }
    return result;
}

// Example Usage:
console.log(replaceSpaces("hello world")); // Output: "hello-world"
console.log(replaceSpaces("this is a test")); // Output: "this-is-a-test"
console.log(replaceSpaces("no spaces here")); // Output: "no-spaces-here"
```


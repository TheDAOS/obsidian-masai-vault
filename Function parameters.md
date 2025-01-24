## JavaScript Function Arguments

Arguments are values you pass to the function when you call it.

```js
// function with a parameter called 'name'
function greet(name) {
    console.log(`Hello ${name}`);
}

// pass argument to the function
greet("John");

// Output: Hello John
```

In the above example, we passed `"John"` as an argument to the `greet()` function.

##### Pass Argument to the Function

Notice the name variable declared inside parentheses:

```js
function greet(name) {
    // code
}
```

Here, name is a function parameter, which acts as a placeholder to store the function argument.

In other words, the argument "John" is stored in the name parameter.

**Remember**: A function argument is the value we pass to the function, while a function parameter is a placeholder that stores the argument passed to the function.

**Pass Different Arguments to the Function**
We can pass different arguments in each call, making the function re-usable and dynamic.

```js
function greet(name) {
    console.log(`Hello ${name}`);
}

// pass "John" as argument
greet("John");

// pass "David" as argument
greet("David");
```

##### Output
```js
Hello John
Hello David
```
***

## Example 2: JavaScript Function to Add Two Numbers

We can also pass multiple arguments to a single function. For example,

```js
// function with two arguments
function addNumbers(num1, num2) {
    let sum = num1 + num2;
   console.log(`Sum: ${sum}`);
}

// call function by passing two arguments
addNumbers(5, 4);

// Output:
// Sum: 9
```

In the above example, we have created a function named `addNumbers()` with two parameters: `num1` and `num2`. Here,

- `num1` takes the value of the first argument, 5.
- `num2` takes the value of the second argument, 4.

The function then adds the values of `num1` and `num2` and the result is printed as output.

[[JavaScript Function Assignment]]

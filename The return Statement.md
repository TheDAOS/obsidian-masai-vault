We can return a value from a JavaScript function using the `return` statement.
```js
// function to find square of a number
function findSquare(num) {

    // return square
    return num * num;

}

// call the function and store the result
let square = findSquare(3);

console.log(`Square: ${square}`);
```

##### Output
```js
Square: 9
```

In the above example, we have created a function named `findSquare()`. The function accepts a number and returns the square of the number.

In our case, we passed 3 as an argument to the function. So, the function returns the square of 3, which is 9, to the function call.

We then stored this return value in the square variable and printed it.
***

## The return Statement Terminates the Function

Any code written in the function after the `return` statement is not executed. For example,

```js
function display() {

    console.log("This will be executed.");

    return "Returning from function.";

    console.log("This will not be executed.");
}

let message = display();
console.log(message);
```

##### Output:
```js
This will be executed.
Returning from function.
```

In this example, the `display()` function doesn't execute the second `console.log()` statement inside it.

This is because the function execution stops at the `return` statement. So, the following code is never reached:

```js
console.log("This will not be executed.");
```

This is what actually happens:
1. First, the function prints `This will be executed.` to the screen.
2. Then, it returns the string `Returning from function.` to the function call.
3. Finally, the function terminates its execution.
4. The return value is then stored in the  variable and printed. message

**Function Terminates After return**

#### Task 5: Return the Larger Number

##### Description:

Create a function `findLarger` that takes two numbers as arguments and returns the larger of the two. Call the function with `45` and `78`, then print the result.

##### Solution:
```js
function findLarger(num1, num2) {
    return num1 > num2 ? num1 : num2;
}

// Call the function and print the result
let larger = findLarger(45, 78);
console.log(`The larger number is: ${larger}`);
```


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
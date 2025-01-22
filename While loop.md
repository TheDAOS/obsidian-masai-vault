## Exploring the JavaScript while Loop
The `while` loop in JavaScript repeatedly executes a block of code as long as a given condition remains true.

### General Form of a while Loop
```js
while (condition) {
    command;
}
```
- Initially, JavaScript evaluates the specified condition. If it evaluates to true, the command within the loop is executed. After the command executes, JavaScript re-evaluates the condition; if it still holds true, the loop continues. The loop terminates when the condition evaluates to false. If the condition is false from the start, the loop does not execute at all.
- Since the condition is checked before each iteration, the `while` loop is known as a pre-test loop.

### Using a while Loop with a Single Command
A simple `while` loop without curly braces is syntactically correct in JavaScript if only one command is inside the loop:
```js
let count = 1;
while (count < 5)
    console.log(count++);
```

However, it is generally advisable to use curly braces for clarity and maintainability, even when the loop contains only one statement:
```js
let count = 1;
while (count < 5) {
    console.log(count);
    count++;
}
```

### Example of Using while Loop
In this example, a `while` loop is utilized to calculate the factorial of the number 5:
```js
let product = 1;
let counter = 1;

while (counter <= 5) {
    product *= counter;
    counter++;
}

console.log(product); // Outputs: 120
```

### Visualization of the Loop
Here’s how each iteration of the loop handles the steps:

1. **Initialization**: `product = 1`, `counter = 1`
2. **Iteration 1**: Check `counter <= 5 (1 <= 5)`, calculate `product *= 1` (product = 1), increment `counter` to 2.
3. **Iteration 2**: Check `counter <= 5 (2 <= 5)`, calculate `product *= 2` (product = 2), increment `counter` to 3.
4. **Iteration 3**: Check `counter <= 5 (3 <= 5)`, calculate `product *= 3` (product = 6), increment `counter` to 4.
5. **Iteration 4**: Check `counter <= 5 (4 <= 5)`, calculate `product *= 4` (product = 24), increment `counter` to 5.
6. **Iteration 5**: Check `counter <= 5 (5 <= 5)`, calculate `product *= 5` (product = 120), increment `counter` to 6.
7. **Termination**: Check `counter <= 5 (6 <= 5)` fails, exit the loop.

The output of the loop will be `120`, representing the factorial of 5.

### Example: Sum of All Odd Numbers from 1 to 99 Using a While Loop
This example calculates the sum of all odd numbers from 1 to 99 using a `while` loop instead of a `for` loop.

#### Code:
```js
let sumOddNumbers = 0;
let i = 1;  // Initialization

while (i < 100) {
    sumOddNumbers += i;
    i += 2;  // Update: Move to the next odd number
}

console.log("Sum of all odd numbers from 1 to 99:", sumOddNumbers);
```

#### Explanation:
- **Initialization**: Start with `i` at 1, which is the first odd number.
- **Condition**: The loop continues as long as `i` is less than 100.
- **Execution**: Add `i` to `sumOddNumbers` to accumulate the sum of odd numbers.
- **Update**: Increment `i` by 2 to ensure only odd numbers are considered, skipping even numbers.
##### Output:
```text
Sum of all odd numbers from 1 to 99: 2500
```

### Example: Calculating Factorial Using a While Loop
This example demonstrates calculating the factorial of a number using a `while` loop.

#### Code:
```js
let n = 5;
let factorial = 1;
let i = 1;  // Initialization

while (i <= n) {
    factorial *= i;  // Execute: Multiply factorial by i
    i++;             // Update: Increment i by 1
}

console.log(`Factorial of ${n} is ${factorial}`);
```

#### Explanation:
- **Initialization**: `i` starts at 1.
- **Condition**: The loop runs as long as `i` is less than or equal to `n`.
- **Execution**: Multiply `factorial` by `i` to calculate the factorial progressively.
- **Update**: Increment `i` by 1 after each iteration to move to the next integer.

##### Output:
```text
Factorial of 5 is 120
```


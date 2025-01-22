## Introduction to the JavaScript `break` Statement
The `break` statement in JavaScript is utilized to exit from the current loop or a `switch` statement. It is most often used with a conditional `if` statement that determines when the loop should be terminated early.

### Using the JavaScript `break` Statement in a `for` Loop
Here's an example of using the `break` statement in a `for` loop:

```js
for (let i = 0; i < 10; i++) {
    if (i === 5) {
        break;
    }
    console.log(i);
}
```

##### Output:
```js
0
1
2
3
4
```

#### Visualization:
- **Initialization**: `i = 0`
- **Iteration 1**: `i = 0`➜ Check `i < 10` (true) ➜ Check `i === 5` (false) ➜ Print `0` ➜ Increment `i` to `1`.
- **Iteration 2**: `i = 1` ➜ Check `i < 10` (true) ➜ Check `i === 5` (false) ➜ Print `1` ➜ Increment `i` to `2`.
- **Iteration 3**: `i = 2` ➜ Check `i < 10` (true) ➜ Check `i === 5` (false) ➜ Print `2` ➜ Increment `i` to `3`.
- **Iteration 4**: `i = 3` ➜ Check `i < 10` (true) ➜ Check `i === 5` (false) ➜ Print `3` ➜ Increment `i` to `4`.
- **Iteration 5**: `i = 4` ➜ Check `i < 10` (true) ➜ Check `i === 5` (false) ➜ Print `4` ➜ Increment `i` to `5`.
- **Iteration 6**: `i = 5` ➜ Check `i < 10` (true) ➜ Check `i === 5` (true) ➜ break executed, exit loop.
- **Loop Exit**: After `i = 5`, the loop terminates because of the `break` statement.

### Using the JavaScript `break` Statement in a `while` Loop
Here's how to use the `break` statement in a `while` loop:
```js
let k = 0;
while (k <= 10) {
    if (k === 5) {
        break;
    }
    console.log(k);
    k++;
}
```

##### Output:
```js
0
1
2
3
4
```

#### Visualization:
- **Initialization**: `k = 0`
- **Iteration 1**: `k = 0`➜ Check `k < 10` (true) ➜ Check `k === 5` (false) ➜ Print `0` ➜ Increment `k` to `1`.
- **Iteration 2**: `k = 1` ➜ Check `k < 10` (true) ➜ Check `k === 5` (false) ➜ Print `1` ➜ Increment `k` to `2`.
- **Iteration 3**: `k = 2` ➜ Check `k < 10` (true) ➜ Check `k === 5` (false) ➜ Print `2` ➜ Increment `k` to `3`.
- **Iteration 4**: `k = 3` ➜ Check `k < 10` (true) ➜ Check `k === 5` (false) ➜ Print `3` ➜ Increment `k` to `4`.
- **Iteration 5**: `k = 4` ➜ Check `k < 10` (true) ➜ Check `k === 5` (false) ➜ Print `4` ➜ Increment `k` to `5`.
- **Iteration 6**: `k = 5` ➜ Check `k < 10` (true) ➜ Check `k === 5` (true) ➜ break executed, exit loop.
- **Loop Exit**: After `k = 5`, the loop terminates because of the `break` statement.

## Introduction to the JavaScript `continue` Statement
The `continue` statement is used within looping structures (`for`, `while`, and `do...while` loops) to skip the current loop iteration and continue with the next iteration of the loop.

### Using the `continue` Statement in a `for` Loop
Here’s an example using the `continue` statement:
```js
for (let i = 1; i <= 4; i++) {
    if (i === 2) {
        continue; // Skips the current iteration when i is 2
    }
    console.log(i);
}
```

#### Visualization:
- **Initialization**: `i = 1`
- **Iteration 1**: `i = 1` ➜ Check `i <= 4` (true) ➜ Check `i === 2` (false) ➜ Print `1` ➜ Increment `i` to `2`.
- **Iteration 2**: `i = 2` ➜ Check `i <= 4` (true) ➜ Check `i === 2` (true) ➜ `continue` executed, skip printing, increment `i` to `3`.
- **Iteration 3**: `i = 3` ➜ Check `i <= 4` (true) ➜ Check `i === 2` (false) ➜ Print `3` ➜ Increment `i` to `4`.
- **Iteration 4**: `i = 4` ➜ Check `i <= 4` (true) ➜ Check `i === 2` (false) ➜ Print `4` ➜ Increment `i` to `5`.
- **Loop Exit**: After `i = 4`, the loop terminates as the next check `i <= 4` (5 <= 4) fails.

Every number except 2 is printed. The loop continues past 2 without interruption except for skipping the print statement during that iteration.

### Example with `continue` in a `while` Loop
Now, let's iterate over numbers from 1 to 10 but skip the number 5, continuing with the next iteration immediately.

##### JavaScript Code:
```js
let i = 1;
while (i <= 10) {
    if (i === 5) {
        i++;
        continue; // Skips the current iteration when i is 5
    }
    console.log(i);
    i++;
}
```

#### Visualization:
- **Iteration 1**: `i = 1` ➜ Checks if `i === 5` (false) ➜ Prints `1` ➜ Increments `i` to 2.
- **Iteration 2**: `i = 2` ➜ Checks if `i === 5` (false) ➜ Prints `2` ➜ Increments `i` to 3.
- **Iteration 3**: `i = 3` ➜ Checks if `i === 5` (false) ➜ Prints `3` ➜ Increments `i` to 4.
- **Iteration 4**: `i = 4` ➜ Checks if `i === 5` (false) ➜ Prints `4` ➜ Increments `i` to 5.
- **Iteration 5**: `i = 5` ➜ Increments `i` to 6 (to skip printing 5) ➜ Continues to the next iteration.
- **Iteration 6**: `i = 6` ➜ Checks if `i === 5` (false) ➜ Prints `6` ➜ Increments `i` to 7.
- **Iteration 7**: `i = 7` ➜ Prints `7` ➜ Increments `i` to 8.
- **Iteration 8**: `i = 8` ➜ Prints `8` ➜ Increments `i` to 9.
- **Iteration 9**: `i = 9` ➜ Prints `9` ➜ Increments `i` to 10.
- **Iteration 10**: `i = 10` ➜ Prints `10` ➜ Increments `i` to 11.

Every number except `5` is printed. The loop continues past `5` without interruption except for skipping the print statement during that iteration.

### Examples:
#### Example 1: Exit When a Perfect Square is Found
- **Scenario:** Use a `for` loop to find when a number squared exceeds 500 for the first time and exit the loop.

```js
for (let i = 1; i < 100; i++) {
    if (i * i > 500) {
        console.log(`The smallest number whose square is greater than 500 is ${i}`);
        break; // Exit the loop as soon as the condition is met
    }
}
```

##### Output:
```js
The smallest number whose square is greater than 500 is 23
```

#### Example 2: Prevent Infinite Loop
- **Scenario:** Use a `while` loop to increment a counter until it reaches a number divisible by 19, then exit.
```js
let counter = 1;
while (counter < 1000) {
    if (counter % 19 === 0) {
        console.log(`First number divisible by 19 below 1000 is ${counter}`);
        break; // Exit the loop when the first divisible number is found
    }
    counter++;
}
```

##### Output:
```js
First number divisible by 19 below 1000 is 19
```

#### Examples of `continue` Statement
#### Example 3: Skip Negative Values in Computation
- **Scenario:** Use a `for` loop to sum only positive integers from -10 to 10, skipping any negative values.

```js
let sum = 0;
for (let i = -10; i <= 10; i++) {
    if (i < 0) {
        continue; // Skip negative numbers
    }
    sum += i; // Only add non-negative numbers
}
console.log(`Sum of non-negative integers from -10 to 10 is ${sum}`);
```

##### Output:
```js
Sum of non-negative integers from -10 to 10 is 55
```

#### Example 4: Increment Only Odd Numbers
- **Scenario**: Increment through numbers, adding only odd numbers to the total until reaching 100, but skipping even numbers.

```js
let total = 0;
let num = 1;
while (num <= 100) {
    if (num % 2 === 0) {
        num++;
        continue; // Skip the addition for even numbers
    }
    total += num; // Add odd numbers only
    num++;
}
console.log(`Sum of odd numbers from 1 to 100 is ${total}`);
```

##### Output:
```js
Sum of odd numbers from 1 to 100 is 2500
```
***
[[Conditionals in loop - break & Continue Assignment]]

Combining `break` and `continue`
You can combine both `break` and `continue` in a single loop for more complex control.
```js
for (let i = 1; i <= 10; i++) {
  if (i % 2 === 0) {
    continue;  // Skip even numbers
  }
  if (i === 7) {
    break;  // Exit the loop when i is 7
  }
  console.log(i);
}
// Output: 1 3 5
```
Here, the loop skips all even numbers and stops completely when `i` is 7. The result is that only odd numbers less than 7 are printed.
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
- Initialization: i = 1
- Iteration 1: i = 1 ➜ Check i <= 4 (true) ➜ Check i === 2 (false) ➜ Print 1 ➜ Increment i to 2.
- Iteration 2: i = 2 ➜ Check i <= 4 (true) ➜ Check i === 2 (true) ➜ continue executed, skip printing, increment i to 3.
Iteration 3: i = 3 ➜ Check i <= 4 (true) ➜ Check i === 2 (false) ➜ Print 3 ➜ Increment i to 4.
Iteration 4: i = 4 ➜ Check i <= 4 (true) ➜ Check i === 2 (false) ➜ Print 4 ➜ Increment i to 5.
Loop Exit: After i = 4, the loop terminates as the next check i <= 4 (5 <= 4) fails.


Every number except 2 is printed. The loop continues past 2 without interruption except for skipping the print statement during that iteration.
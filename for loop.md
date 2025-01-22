## Exploring JavaScript's For Loop
The `for` loop in JavaScript is a fundamental control structure that allows you to execute a block of code repeatedly under controlled conditions.

#### Structure of the For Loop
```js
for (initialize; condition; update) {
    // Code to execute
}
```

#### Mechanics of the For Loop
1. **Initialization**: This step is executed only once when the loop starts. It typically involves setting up a loop control variable.
2. **Test Condition**: Evaluated at the start of each loop iteration. If the condition evaluates to true, the loop continues; if false, the loop exits.
3. **Update Expression**: This is executed at the end of each loop iteration, updating the loop control variable.

#### JavaScript For Loop Example
##### Code:
```js
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

##### How It Works:
1. **Initialization**: `let i = 1` - the loop starts with `i` initialized to `1`.
2. **Test Condition**: `i <= 5` - JavaScript checks if `i` is less than or equal to `5`.
3. **Body Execution**: `console.log(i);` - If the condition is true, JavaScript executes the loop body, printing the current value of `i` to the console.
4. **Update Expression**: `i++` - `i` is incremented by `1` after the loop body is executed.
5. **Repeat**: Steps 2-4 continue until the condition evaluates to false.
6. **Exit Loop**: The loop terminates when `i` is greater than `5`.

##### Output:
```js
1
2
3
4
5
```

##### Visualization
Each iteration of the loop handles these steps:
- **Iteration 1**: i = 1 ➜ Check (1 <= 5) → True ➜ Print 1 ➜ Increment i to 2.
- **Iteration 2**: i = 2 ➜ Check (2 <= 5) → True ➜ Print 2 ➜ Increment i to 3.
- **Iteration 3**: i = 3 ➜ Check (3 <= 5) → True ➜ Print 3 ➜ Increment i to 4.
- **Iteration 4**: i = 4 ➜ Check (4 <= 5) → True ➜ Print 4 ➜ Increment i to 5.
- **Iteration 5**: i = 5 ➜ Check (5 <= 5) → True ➜ Print 5 ➜ Increment i to 6.
- **Iteration 6**: i = 6 ➜ Check (6 <= 5) → False ➜ Exit loop.

##### Practical Example with For Loop
Suppose you want to calculate the sum of all even numbers from 2 to 20. Here's how you might implement this in JavaScript:
```js
let sumEvenNumbers = 0;

for (let i = 2; i <= 20; i += 2) {
    sumEvenNumbers += i;
}

console.log(sumEvenNumbers);
```

Output:
```js
110
```

**Explanation**
- **Initialization**: Set `i` starting at `2`.
- **Condition**: The loop runs while `i` is less than or equal to `20`.
- **Update**: Increment `i` by `2` in each iteration to focus exclusively on even numbers.
- **Execution**: Each iteration adds the next even number to `sumEvenNumbers`, resulting in fewer iterations than looping through all numbers.

#### Example : Sum of All Odd Numbers from 1 to 99

Suppose you want to calculate the sum of all odd numbers from 1 to 99. This can be efficiently done using a `for` loop.

##### Code
```js
let sumOddNumbers = 0;

for (let i = 1; i < 100; i += 2) {
    sumOddNumbers += i;
}

console.log("Sum of all odd numbers from 1 to 99:", sumOddNumbers);
```

##### Explanation:
- **Initialization**: Start `i` at `1`, the first odd number.
- **Condition**: Continue the loop as long as `i` is less than `100`.
- **Update**: Increment `i` by `2` to skip even numbers and only consider odd numbers.
- **Execution**: Add each odd number to `sumOddNumbers`.

##### Output:
```js
Sum of all odd numbers from 1 to 99: 2500
```

#### Example : Calculating Factorial Using For Loop
Calculating the factorial of a number is a classic example where a `for` loop can be used. Factorial of `n` (denoted as `n!`) is the product of all positive integers less than or equal to `n`.

##### Code:
```js
let n = 5;
let factorial = 1;

for (let i = 1; i <= n; i++) {
    factorial *= i;
}

console.log(`Factorial of ${n} is ${factorial}`);
```

##### Explanation:
- **Initialization**: `i` starts at `1`.
- **Condition**: Continues until `i` is less than or equal to `n`.
- **Update**: Increment `i` by `1` after each iteration.
- **Execution**: Multiply `factorial` by `i` to compute the factorial progressively.

##### Output:
```js
Factorial of 5 is 120
```

[[for loop Assignment]]
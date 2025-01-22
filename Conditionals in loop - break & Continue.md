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
- **Iteration 1**: i = 0 ➜ Check i < 10 (true) ➜ Check i === 5 (false) ➜ Print 0 ➜ Increment i to 1.
- Iteration 2: i = 1 ➜ Check i < 10 (true) ➜ Check i === 5 (false) ➜ Print 1 ➜ Increment i to 2.
- Iteration 3: i = 2 ➜ Check i < 10 (true) ➜ Check i === 5 (false) ➜ Print 2 ➜ Increment i to 3.
- Iteration 4: i = 3 ➜ Check i < 10 (true) ➜ Check i === 5 (false) ➜ Print 3 ➜ Increment i to 4.
- Iteration 5: i = 4 ➜ Check i < 10 (true) ➜ Check i === 5 (false) ➜ Print 4 ➜ Increment i to 5.
- Iteration 6: i = 5 ➜ Check i < 10 (true) ➜ Check i === 5 (true) ➜ break executed, exit loop.
- Loop Exit: After i = 5, the loop terminates because of the break statement.
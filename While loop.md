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

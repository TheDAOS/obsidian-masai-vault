## For Loop

The `for` loop is commonly used for iterating over each character in a string by using the string's length property to control the loop.
```js
let text = "Hello";
for (let i = 0; i < text.length; i++) {
    console.log(text[i]);  // Outputs each character of the string
}
```

##### Visualization of Iterations in For Loop:
- **Iteration 1**: i = 0 ➜ Check (0 < 5) → True ➜ Print "H" ➜ Increment i to 1.
- **Iteration 2**: i = 1 ➜ Check (1 < 5) → True ➜ Print "e" ➜ Increment i to 2.
- **Iteration 3**: i = 2 ➜ Check (2 < 5) → True ➜ Print "l" ➜ Increment i to 3.
- **Iteration 4**: i = 3 ➜ Check (3 < 5) → True ➜ Print "l" ➜ Increment i to 4.
- **Iteration 5**: i = 4 ➜ Check (4 < 5) → True ➜ Print "o" ➜ Increment i to 5.
- **Iteration 6**: i = 5 ➜ Check (5 < 5) → False ➜ Exit loop.

## While Loop

The `while` loop can also be used to iterate through a string by using an index variable and checking it against the string’s length.
```js
let text = "Hello";
let i = 0;
while (i < text.length) {
    console.log(text[i]);  // Outputs each character of the string
    i++;
}
```

##### Visualization of Iterations in While Loop:
- **Iteration 1**: i = 0 ➜ Check (0 < 5) → True ➜ Print "H" ➜ Increment i to 1.
- **Iteration 2**: i = 1 ➜ Check (1 < 5) → True ➜ Print "e" ➜ Increment i to 2.
- **Iteration 3**: i = 2 ➜ Check (2 < 5) → True ➜ Print "l" ➜ Increment i to 3.
- **Iteration 4**: i = 3 ➜ Check (3 < 5) → True ➜ Print "l" ➜ Increment i to 4.
- **Iteration 5**: i = 4 ➜ Check (4 < 5) → True ➜ Print "o" ➜ Increment i to 5.
- **Iteration 6**: i = 5 ➜ Check (5 < 5) → False ➜ Exit loop.

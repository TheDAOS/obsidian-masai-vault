## Introduction
Nested loops are loops within loops, and they are particularly useful for scenarios that involve repeated iterations, such as printing patterns. In pattern printing, the outer loop controls the rows, while the inner loop controls the columns. This combination allows you to create complex patterns, such as triangles, squares, and other shapes.

## Key Concepts and Definitions

### What is a Nested Loop?
A **nested loop** is when one loop (inner loop) is placed inside another loop (outer loop). The inner loop completes all of its iterations before the outer loop moves to its next iteration.

#### Syntax of a Nested Loop
```js
for (let i = 1; i <= rows; i++) {        // Outer loop controls the number of rows
  for (let j = 1; j <= columns; j++) {   // Inner loop controls the number of columns
    // Code to be executed
  }
}
```
- The outer loop runs a specified number of times (usually controlling rows).
- The inner loop runs for each iteration of the outer loop (usually controlling columns or items within each row).

#### Example of a Simple Nested Loop
```js
for (let i = 1; i <= 3; i++) {
  for (let j = 1; j <= 3; j++) {
    console.log(`i = ${i}, j = ${j}`);
  }
}
```

##### Output:
```js
i = 1, j = 1
i = 1, j = 2
i = 1, j = 3
i = 2, j = 1
i = 2, j = 2
i = 2, j = 3
i = 3, j = 1
i = 3, j = 2
i = 3, j = 3
```

## Step-by-Step Explanation: Printing Patterns with Nested Loops

### Example 1: Printing a Square Pattern of Stars (`*`)
This example prints a square pattern of stars where both the number of rows and columns are equal.

```js
for (let i = 1; i <= 5; i++) {         // Outer loop for rows
  let row = "";
  for (let j = 1; j <= 5; j++) {       // Inner loop for columns
    row += "* ";
  }
  console.log(row);                    // Print the row after the inner loop completes
}
```

##### Output:
```js
* * * * *
* * * * *
* * * * *
* * * * *
* * * * *
```

- The outer loop controls the number of rows (5 rows).
- The inner loop prints 5 stars (`*`) in each row.

### Example 2: Printing a Right-Angled Triangle Pattern
To print a right-angled triangle, the inner loop prints an increasing number of stars (`*`) in each row.

```js
for (let i = 1; i <= 5; i++) {         // Outer loop controls the number of rows
  let row = "";
  for (let j = 1; j <= i; j++) {       // Inner loop runs `i` times for each row
    row += "* ";
  }
  console.log(row);
}
```

##### Output:
```js
*
* *
* * *
* * * *
* * * * *
```

- The outer loop runs 5 times, each time representing a row.
- The inner loop prints an increasing number of stars in each row. On the first iteration, it prints 1 star, then 2 stars in the second row, and so on.

### Example 3: Inverted Right-Angled Triangle Pattern
You can modify the loop conditions to print an inverted triangle.
```js
for (let i = 5; i >= 1; i--) {         // Outer loop decreases the number of rows
  let row = "";
  for (let j = 1; j <= i; j++) {       // Inner loop prints fewer stars each time
    row += "* ";
  }
  console.log(row);
}
```
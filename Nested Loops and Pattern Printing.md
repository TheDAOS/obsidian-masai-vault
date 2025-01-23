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

##### Output:
```js
* * * * *
* * * *
* * *
* *
*
```

- The outer loop starts at 5 and decreases by 1 each time.
- The inner loop prints the corresponding number of stars based on the value of `i`.

### Example 4: Number Pyramid
This example prints a pyramid pattern with increasing numbers on each row.
```js
for (let i = 1; i <= 5; i++) {
  let row = "";
  for (let j = 1; j <= i; j++) {
    row += j + " ";                    // Append the number instead of a star
  }
  console.log(row);
}
```

### Output:
```js
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
```

- The outer loop controls the number of rows.
- The inner loop prints numbers from `1` to the current row number (`i`).

### Example 5: Inverted Number Pyramid
You can also create an inverted number pyramid by modifying the inner and outer loop conditions.

```js
for (let i = 5; i >= 1; i--) {         // Outer loop decreases the number of rows
  let row = "";
  for (let j = 1; j <= i; j++) {       // Inner loop prints numbers in each row
    row += j + " ";
  }
  console.log(row);
}
```

##### Output:
```js
1 2 3 4 5
1 2 3 4
1 2 3
1 2
1
```

- The outer loop starts from 5 and decreases to 1.
- The inner loop prints numbers from `1` to the current row number (`i`).

## Use Cases for Nested Loops in Pattern Printing

### 1. Creating Grid-Based Layouts
Nested loops are useful when creating grid-like structures, such as printing a square or rectangular pattern of characters, numbers, or symbols.

##### Example: 5 x 5 Number Grid
```
for (let i = 1; i <= 5; i++) {
  let row = "";
  for (let j = 1; j <= 5; j++) {
    row += j + " ";  // Print numbers 1 to 5 in each row
  }
  console.log(row);
}
```

### 2. Creating Triangular or Pyramid Shapes
You can use nested loops to print triangular or pyramid shapes. The outer loop controls the number of rows, and the inner loop controls the number of elements (stars or numbers) printed in each row.

### 3. Symmetrical Patterns
Nested loops are often used to create symmetrical patterns. By using different combinations of loops, conditions, and output formatting, you can generate various types of symmetrical patterns like diamonds or hourglass shapes.

## Practice Exercises

1. **Exercise 1**: Write a nested loop to print a right-angled triangle of numbers where the first row contains 1, the second row contains 2 3, and so on:
	```js
	1
	2 3
	4 5 6
	7 8 9 10
	```

2. **Exercise 2**: Write a nested loop to print the following pattern:
	```js
	* * * * *
	* * * * *
	* * * * *
	* * * * *
	* * * * *
	```

3. **Exercise 3**: Write a nested loop to print the following pyramid of stars:
	```js
	    *
	   * *
	  * * *
	 * * * *
	* * * * *
	```

4. **Exercise 4**: Write a nested loop to print the following diamond pattern of numbers:
	```js
	    1
	   1 2
	  1 2 3
	 1 2 3 4
	  1 2 3
	   1 2
	    1
	```

## Summary

- **Nested loops** consist of one loop inside another, allowing for complex repetition structures such as grids, triangles, and pyramids.
- In pattern printing, the outer loop typically controls the rows, and the inner loop controls the elements printed within each row.
- The combination of nested loops and string manipulation (such as concatenation) enables you to generate various types of patterns, such as triangles, squares, and pyramids.

## Additional Resources

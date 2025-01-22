## Notes on Nested for Loops in JavaScript
A **nested `for` loop** is when one `for` loop is placed inside another `for` loop. The inner loop completes all its iterations for every single iteration of the outer loop. This structure is often used for working with multidimensional data, patterns, or generating complex outputs like multiplication tables.
***
### Structure of Nested Loops
```js
for (let i = 0; i < outerLimit; i++) { // Outer loop
    for (let j = 0; j < innerLimit; j++) { // Inner loop
        // Code to execute for each combination of i and j
    }
}
```
***
### Key Points to Remember
1. Outer Loop:
	- Runs first and controls the number of iterations for the inner loop.
2. Inner Loop:
	- Executes completely for every iteration of the outer loop.
3. Execution Order:
	- For each iteration of the outer loop, the inner loop runs from start to finish.
4. Use Cases:
	- Generating multiplication tables.
	- Creating patterns like triangles or grids.
	- Working with 2D arrays or matrices.
***
#### Multiplication Table Example Using Nested Loops
Here’s an example to print multiplication tables for numbers 2 and 3:

```js
for (let num = 2; num <= 3; num++) { // Outer loop for table numbers
    console.log(`Multiplication Table for ${num}:`);
    for (let i = 1; i <= 10; i++) { // Inner loop for each multiplication
        console.log(`${num} x ${i} = ${num * i}`);
    }
    console.log(); // Add a blank line between tables
}
```
***
#### Explanation
1. **Outer Loop (`for (let num = 2; num <= 3; num++)`):**
	- Iterates through the numbers for which multiplication tables are generated (`2` and `3`).
	- Each iteration represents one multiplication table.
2. **Inner Loop (`for (let i = 1; i <= 10; i++)`):**
	- For each table number (`num`), the inner loop runs from `1` to `10`.
	- It calculates the product (`num * i`) and prints the result using template literals.
3. **Blank Line:**
	- A `console.log()` is added after the inner loop to separate tables visually.
***
#### Output
```text
Multiplication Table for 2:
2 x 1 = 2
2 x 2 = 4
2 x 3 = 6
2 x 4 = 8
2 x 5 = 10
2 x 6 = 12
2 x 7 = 14
2 x 8 = 16
2 x 9 = 18
2 x 10 = 20

Multiplication Table for 3:
3 x 1 = 3
3 x 2 = 6
3 x 3 = 9
3 x 4 = 12
3 x 5 = 15
3 x 6 = 18
3 x 7 = 21
3 x 8 = 24
3 x 9 = 27
3 x 10 = 30
```
***
#### Advantages of Nested Loops for Multiplication Tables
1. **Dynamic Range:**
	- You can easily adjust the outer loop to include more tables. For example:
		```js
		for (let num = 2; num <= 5; num++) { ... }
		
		```

2. **Clean Formatting:**
	- By using **template literals** (`${}`), the results are dynamically embedded in the string.

3. **Scalability:**
	- Works well for generating multiple tables with minimal changes to the code.
***
This example demonstrates how nested loops can efficiently generate and display multiplication tables, while template literals make the output clean and easy to read.

Here are some **pattern-related questions** with **solutions** using nested `for` loops in JavaScript:
***
[[Nested for loop Assignment]]

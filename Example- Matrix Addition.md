#### Code: Add Two 2x2 Matrices
```js
// Matrices to add
let matrixA = [
  [1, 2],
  [3, 4]
];
let matrixB = [
  [5, 6],
  [7, 8]
];

// Initialize the resulting matrix
let result = [];

// Loop through rows
for (let i = 0; i < matrixA.length; i++) {
  let row = [];
  // Loop through columns
  for (let j = 0; j < matrixA[i].length; j++) {
    // Add corresponding elements
    row.push(matrixA[i][j] + matrixB[i][j]);
  }
  // Add the row to the result matrix
  result.push(row);
}

// Print the resulting matrix
console.log(result);
```

#### Explanation:

##### Input Matrices:
```text
matrixA:            matrixB:
[1, 2]              [5, 6]
[3, 4]              [7, 8]
```

##### Resulting Matrix Dimensions:
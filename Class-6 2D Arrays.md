## JavaScript Multidimensional Array
In JavaScript, multidimensional arrays are arrays that contain other arrays as their elements.

### Example: Creating a Multidimensional Array
```js
// multidimensional array
const data = [[10, 20, 30], [40, 50, 60], [70, 80, 90]];

console.log(data);

// Output: [ [ 10, 20, 30 ], [ 40, 50, 60 ], [ 70, 80, 90 ] ]
```

Here, we created a multidimensional array named `data` with the following arrays as its elements: `[10, 20, 30]`, `[40, 50, 60]`, `[70, 80, 90]`.

## Use Existing Arrays as Elements
We can also create multidimensional arrays by nesting existing arrays within them.

##### Example:
```js
// declare three arrays
let group1 = [1, 2, 3];
let group2 = [4, 5, 6];
let group3 = [7, 8, 9];

// create multidimensional array using existing arrays
let groups = [group1, group2, group3];

// print the multidimensional array
console.log(groups);

// Output: [ [ 1, 2, 3 ], [ 4, 5, 6 ], [ 7, 8, 9 ] ]
```

Here, we first created three arrays: `group1`, `group2`, and `group3`.
We then nested these three arrays inside the `groups` array to create our multidimensional array.

## Access Elements of a Multidimensional Array
You can access elements of a multidimensional array using array indexes.

##### Example:
```js
let numbers = [
  [100, 200, 300],
  [400, 500, 600],
  [700, 800, 900]
];

// access the first inner array
console.log(numbers[0]); // [100, 200, 300]

// access the first item of the first inner array
console.log(numbers[0][0]); // 100

// access the second item of the third inner array
console.log(numbers[2][1]); // 800
```

##### Output:
```js
[100, 200, 300]
100
800
```

You can think of a multidimensional array (`numbers`) as a table with 3 rows and 3 columns:

|             | 1st Column | 2nd Column | 3rd Column |
| ----------- | ---------- | ---------- | ---------- |
| **1st Row** | 100        | 200        | 300        |
| **2nd Row** | 400        | 500        | 600        |
| **3rd Row** | 700        | 800        | 900        |

## Add Elements to a Multidimensional Array
You can use `index notation` or the `push()` method to add elements to a multidimensional array.

### 1. Using Index Notation
```js
let numbers = [[10, 20], [30, 40]];

// add 50 as the 3rd element of the 2nd inner array
numbers[1][2] = 50;

console.log(numbers);

// Output: [ [ 10, 20 ], [ 30, 40, 50 ] ]
```

### 2. Using the `push()` Method
The `push()` method inserts an element at the end of the array.

##### Example:
```js
let numbers = [[10, 20], [30, 40]];

// add element to the end of the outer array
numbers.push([50, 60]);

console.log(numbers);

// add 25 as the final element of the first inner array
numbers[0].push(25);

console.log(numbers);
```

##### Output:
```js
[ [ 10, 20 ], [ 30, 40 ], [ 50, 60 ] ]
[ [ 10, 20, 25 ], [ 30, 40 ], [ 50, 60 ] ]
```

### 3. Practical Exercises: Matrix Operations and Traversal Algorithms

#### Example 1: Printing All Elements of a 2D Array
```js
let matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

for (let i = 0; i < matrix.length; i++) {
  for (let j = 0; j < matrix[i].length; j++) {
    console.log(matrix[i][j]);
  }
}
// Output: 1 2 3 4 5 6 7 8 9
```

**Question**: Write a function to calculate the sum of all elements in a 2D array.

##### Solution:
```js
function sumAllElements(matrix) {
    let sum = 0;
    for (let i = 0; i < matrix.length; i++) {
        for (let j = 0; j < matrix[i].length; j++) {
            sum += matrix[i][j];
        }
    }
    return sum;
}

const matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];
console.log(sumAllElements(matrix)); // Expected: 45
```

##### Row Sum
- Write a function to calculate the sum of all elements in a specific row.
```js
const matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];
function sumRow(matrix, row) {
    // Your code here
}
console.log(sumRow(matrix, 1)); // Expected: 15
```

```js
const matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];

function sumRow(matrix, row) {
    // Check if the row index is within bounds
    if (row < 0 || row >= matrix.length) {
        return "Invalid row index";
    }

    // Initialize the sum
    let sum = 0;

    // Iterate through the elements in the specified row
    for (let i = 0; i < matrix[row].length; i++) {
        sum += matrix[row][i];
    }

    // Return the calculated sum
    return sum;
}

console.log(sumRow(matrix, 1)); // Expected: 15
console.log(sumRow(matrix, 0)); // Expected: 6
console.log(sumRow(matrix, 3)); // Expected: Invalid row index
```

### 4. Column Sum

**Question**: Write a function to calculate the sum of all elements in a specific column.

##### Solution:
```js
const matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];
function sumColumn(matrix, col) {
    if (col < 0 || col >= matrix[0].length) {
        return "Invalid column index";
    }
    let sum = 0;
    for (let i = 0; i < matrix.length; i++) {
        sum += matrix[i][col];
    }
    return sum;
}
console.log(sumColumn(matrix, 0)); // Expected: 12
console.log(sumColumn(matrix, 2)); // Expected: 18
console.log(sumColumn(matrix, 3)); // Expected: Invalid column index
```

### 5. Diagonal Sum

**Question**: Write a function to calculate the sum of the elements in the main diagonal (top-left to bottom-right).

##### Solution:
```js
const matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];
function diagonalSum(matrix) {
    let sum = 0;
    for (let i = 0; i < matrix.length; i++) {
        sum += matrix[i][i];
    }
    return sum;
}
console.log(diagonalSum(matrix)); // Expected: 15
```

**Question**: Write a function to calculate the sum of the elements in the diagonal (top-right to bottom-left).
```js
function antiDiagonalSum(matrix) {
    let sum = 0;
    const n = matrix.length; // Assuming it's a square matrix
    for (let i = 0; i < n; i++) {
        sum += matrix[i][n - 1 - i]; // Access the anti-diagonal element
    }
    return sum;
}

// Example matrix
const matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];

console.log(antiDiagonalSum(matrix)); // Expected: 15 (3 + 5 + 7)
```

### 6. Flatten a 2D Array
**Question**: Write a function to flatten a 2D array into a 1D array.

##### Solution:
```js
function flatten(matrix) {
    const result = [];
    for (let i = 0; i < matrix.length; i++) {
        for (let j = 0; j < matrix[i].length; j++) {
            result.push(matrix[i][j]);
        }
    }
    return result;
}
const matrix = [
    [1, 2],
    [3, 4],
    [5, 6]
];
console.log(flatten(matrix)); // Expected: [1, 2, 3, 4, 5, 6]
```

### 7. Find Maximum Element
**Question**: Write a function to find the maximum element in a 2D array.

##### Solution:
```js
function findMax(matrix) {
    let max = -Infinity;
    for (let i = 0; i < matrix.length; i++) {
        for (let j = 0; j < matrix[i].length; j++) {
            if (matrix[i][j] > max) {
                max = matrix[i][j];
            }
        }
    }
    return max;
}
const matrix = [
    [1, 9, 3],
    [4, 2, 6],
    [7, 8, 5]
];
console.log(findMax(matrix)); // Expected: 9
```

### 8. Replace Zeros with Ones
**Question**: Write a function to replace all zeros in a 2D array with ones.

##### Solution:
```js
function replaceZeros(matrix) {
    for (let i = 0; i < matrix.length; i++) {
        for (let j = 0; j < matrix[i].length; j++) {
            if (matrix[i][j] === 0) {
                matrix[i][j] = 1;
            }
        }
    }
    return matrix;
}
const matrix = [
    [0, 2, 3],
    [4, 0, 6],
    [7, 8, 0]
];
console.log(replaceZeros(matrix));
```

### 9. Count Occurrences of a Value

**Question**: Write a function to count the number of times a specific value appears in a 2D array.

##### Solution:
```js
function countOccurrences(matrix, value) {
    let count = 0;
    for (let i = 0; i < matrix.length; i++) {
        for (let j = 0; j < matrix[i].length; j++) {
            if (matrix[i][j] === value) {
                count++;
            }
        }
    }
    return count;
}

const matrix = [
    [1, 2, 3],
    [4, 2, 6],
    [7, 2, 9]
];
console.log(countOccurrences(matrix, 2)); // Expected: 3
console.log(countOccurrences(matrix, 5)); // Expected: 0
```

### 10. Boundary Sum

**Question**: Write a function to calculate the sum of all boundary elements in a square matrix.

##### Solution:
```js
javascript
Copy code
function boundarySum(matrix) {
    let sum = 0;
    const n = matrix.length;
    for (let i = 0; i < n; i++) {
        for (let j = 0; j < n; j++) {
            if (i === 0 || i === n - 1 || j === 0 || j === n - 1) {
                sum += matrix[i][j];
            }
        }
    }
    return sum;
}

const matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];
console.log(boundarySum(matrix)); // Expected: 40
```

### 11. Clear a Matrix

**Question**: Write a function to clear all elements in a 2D array (replace with zeros).

##### Solution:
```js
function clearMatrix(matrix) {
    for (let i = 0; i < matrix.length; i++) {
        for (let j = 0; j < matrix[i].length; j++) {
            matrix[i][j] = 0;
        }
    }
    return matrix;
}

const matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];
console.log(clearMatrix(matrix));
```

### 12. Addition
##### Code: Add Two 2x2 Matrice
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

[[Example- Matrix Addition]]

### 13. Rotate a Matrix by 90 Degrees
**Question**: Write a function to rotate a square matrix by 90 degrees clockwise.

##### Solution:
```js
function transpose(matrix) {
    const result = [];
    for (let i = 0; i < matrix[0].length; i++) {
        const row = [];
        for (let j = 0; j < matrix.length; j++) {
            row.push(matrix[j][i]);
        }
        result.push(row);
    }
    return result;
}
const matrix = [
    [1, 2, 3],
    [4, 5, 6]
];
console.log(transpose(matrix));
```

### 14. Transpose a Matrix
**Question**: Write a function to transpose a matrix (flip rows and columns).

##### Solution:
```js
function transpose(matrix) {
    const result = [];
    for (let i = 0; i < matrix[0].length; i++) {
        const row = [];
        for (let j = 0; j < matrix.length; j++) {
            row.push(matrix[j][i]);
        }
        result.push(row);
    }
    return result;
}
const matrix = [
    [1, 2, 3],
    [4, 5, 6]
];
console.log(transpose(matrix));
```

### Example 3: Matrix Multiplication (Basic)
Matrix multiplication involves taking the dot product of rows and columns.

##### Example:
```js
let matrixA = [
  [1, 2],
  [3, 4]
];
let matrixB = [
  [5, 6],
  [7, 8]
];

let resultMatrix = [
  [0, 0],
  [0, 0]
];

for (let i = 0; i < matrixA.length; i++) {
  for (let j = 0; j < matrixB[0].length; j++) {
    for (let k = 0; k < matrixB.length; k++) {
      resultMatrix[i][j] += matrixA[i][k] * matrixB[k][j];
    }
  }
}

console.log(resultMatrix);
// Output: [[19, 22], [43, 50]]
```
***

### U Traversal
```js
let mat = [
  [1, 2, 3, 4],
  [5, 6, 7, 8],
  [9, 10, 11, 12],
  [13, 14, 15, 16],
];

// Define ans array to store the result
let ans = [];

// Determine the number of rows and columns
let rows = mat.length; // no. of rows
let cols = mat[0].length; // no. of columns

// Initialize pointers
let topi = 0,
  left = 0,
  bottom = rows - 1,
  right = cols - 1;

// // Perform the U traversal
// // Traverse the first column (top to bottom)
// //00 10 20 30
for (let i = topi; i <= bottom; i++) {
  ans.push(mat[i][left]);
}


// Traverse the bottom row (left to right, if there is more than one row)
// 32 33 34
for (let i = left + 1; i <= right; i++) {
  ans.push(mat[bottom][i]);
}

// Traverse the last column (bottom to top, if there is more than one column)


for (let i = bottom - 1; i > topi; i--) {
  ans.push(mat[i][right]);
}

// Print the result
console.log(ans.join(" "));
```

### O traversal
```js
// Matrix initialization
let mat = [[1, 2, 3, 4],
           [5, 6, 7, 8],
           [9, 10, 11, 12],
           [13, 14, 15, 16]];

// Define ans array to store the result
let ans = [];

// Determine the number of rows and columns
let rows = mat.length; // no. of rows
let cols = mat[0].length; // no. of columns

// Initialize the pointers required for traversal
let top = 0, left = 0, bottom = rows - 1, right = cols - 1;

// Perform the O traversal
// Traverse the top row (left to right)
for (let i = left; i <= right; i++) {
  ans.push(mat[top][i]);
}

// Traverse the right column (top to bottom)
for (let i = top + 1; i <= bottom; i++) {
  ans.push(mat[i][right]);
}

// Traverse the bottom row (right to left, if there is more than one row)
  for (let i = right - 1; i >= left; i--) {
    ans.push(mat[bottom][i]);
  }

// Traverse the left column (bottom to top, if there is more than one column)
  for (let i = bottom - 1; i > top; i--) {
    ans.push(mat[i][left]);
  }


console.log(ans)
```

### Zigzag traversal
```js
// Matrix initialization
let mat = [[1, 2, 3, 4, 5],
           [6, 7, 8, 9, 1],
           [3, 2, 5, 4, 6],
           [7, 8, 9, 1, 2]];
           
           //1 2 3 4 5 1 9 8 7 6 3 2 5 4 6 2 1 9 8 7

// Define ans array to store the result
let ans = [];

// Determine the number of rows
let rows = mat.length;

// Perform zigzag row-wise traversal
for (let i = 0; i < rows; i++) {
  if (i % 2 === 0) {
    // Traverse left to right for even-indexed rows
    for (let j = 0; j < mat[i].length; j++) {
      ans.push(mat[i][j]);
    }
  } else {
    // Traverse right to left for odd-indexed rows
    for (let j = mat[i].length - 1; j >= 0; j--) {
      ans.push(mat[i][j]);
    }
  }
}

console.log(ans);
```

### Z traversal
```js
// Matrix initialization
let mat = [[1, 2, 3, 4],
           [5, 6, 7, 8],
           [9, 10, 11, 12],
           [13, 14, 15, 16]];


           //12 21 30
// Define ans array to store the result
let ans = [];

// Determine the number of rows and columns
let rows = mat.length; // no. of rows
let cols = mat[0].length; // no. of columns

// Initialize the pointers required for traversal
let topi = 0,
  left = 0,
  bottom = rows - 1,
  right = cols - 1;

// Traverse the topi row (left to right)
for (let i = left; i <= right; i++) {
  ans.push(mat[topi][i]);
}

// Traverse the diagonal (topi-right to bottom-left)
//
for (let i = 1; i < rows - 1; i++) {
  ans.push(mat[i][right - i]);
}

// Traverse the bottom row (left to right)
if (bottom > topi) { // Ensure there's more than one row
  for (let i = left; i <= right; i++) {
    ans.push(mat[bottom][i]);
  }
}

console.log(ans);
```

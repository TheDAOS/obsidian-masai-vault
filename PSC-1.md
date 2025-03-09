## U Traversal

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

## O traversal

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

## Zigzag traversal

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

## Z traversal

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
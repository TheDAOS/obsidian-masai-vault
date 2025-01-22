## Question 1: Right-Angled Triangle Pattern
Print a right-angled triangle pattern with `*`:

### Example for `n = 5`:
```text
*
**
***
****
*****
```

### Solution:
```js
let n = 5; // Number of rows

for (let i = 1; i <= n; i++) { // Outer loop for rows
    let row = "";
    for (let j = 1; j <= i; j++) { // Inner loop for columns
        row += "*";
    }
    console.log(row);
}
```
***

## Question 2: Inverted Triangle Pattern
Print an inverted triangle pattern with `*`:

### Example for `n = 5`:
```text
*****
****
***
**
*
```

### Solution:
```js
let n = 5; // Number of rows

for (let i = n; i >= 1; i--) { // Outer loop for rows
    let row = "";
    for (let j = 1; j <= i; j++) { // Inner loop for columns
        row += "*";
    }
    console.log(row);
}
```
***

## Question 3: Pyramid Pattern
Print a pyramid pattern:

### Example for `n = 5`:
```text
    *
   ***
  *****
 *******
*********
```

### Solution:
```js
let n = 5; // Number of rows

for (let i = 1; i <= n; i++) { // Outer loop for rows
    let row = "";
    // Add spaces
    for (let j = 1; j <= n - i; j++) {
        row += " ";
    }
    // Add stars
    for (let k = 1; k <= 2 * i - 1; k++) {
        row += "*";
    }
    console.log(row);
}
```
***

## Question 4: Diamond Pattern
Print a diamond pattern:

### Example for `n = 5`:
```js
    *
   ***
  *****
 *******
*********
 *******
  *****
   ***
    *
```

### Solution:
```js
let n = 5; // Number of rows for the top half

// Top half of the diamond
for (let i = 1; i <= n; i++) {
    let row = "";
    // Add spaces
    for (let j = 1; j <= n - i; j++) {
        row += " ";
    }
    // Add stars
    for (let k = 1; k <= 2 * i - 1; k++) {
        row += "*";
    }
    console.log(row);
}

// Bottom half of the diamond
for (let i = n - 1; i >= 1; i--) {
    let row = "";
    // Add spaces
    for (let j = 1; j <= n - i; j++) {
        row += " ";
    }
    // Add stars
    for (let k = 1; k <= 2 * i - 1; k++) {
        row += "*";
    }
    console.log(row);
}
```
***

## Question 5: Number Triangle
Print a right-angled triangle with numbers:

### Example for `n = 5`:
```text
1
12
123
1234
12345
```

### Solution:
```js
let n = 5; // Number of rows

for (let i = 1; i <= n; i++) { // Outer loop for rows
    let row = "";
    for (let j = 1; j <= i; j++) { // Inner loop for columns
        row += j;
    }
    console.log(row);
}
```
***

## Question 6: Inverted Number Triangle
Print an inverted right-angled triangle with numbers:

### Example for `n = 5`:
```text
12345
1234
123
12
1
```

### Solution:
```js
let n = 5; // Number of rows

for (let i = n; i >= 1; i--) { // Outer loop for rows
    let row = "";
    for (let j = 1; j <= i; j++) { // Inner loop for columns
        row += j;
    }
    console.log(row);
}
```
***

## Question 7: Floyd’s Triangle
Print Floyd’s triangle with numbers starting from 1:

### Example for `n = 5`:
```text
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
```

### Solution:
```js
let n = 5; // Number of rows
let num = 1;

for (let i = 1; i <= n; i++) { // Outer loop for rows
    let row = "";
    for (let j = 1; j <= i; j++) { // Inner loop for columns
        row += num + " ";
        num++;
    }
    console.log(row.trim());
}
```
***

## Question 8: Checkerboard Pattern
Print a checkerboard pattern of `*` and spaces:

### Example for `n = 5`:
```text
* * * * *
 * * * * *
* * * * *
 * * * * *
* * * * *
```

### Solution:
```js
let n = 5; // Size of the checkerboard

for (let i = 1; i <= n; i++) { // Outer loop for rows
    let row = "";
    for (let j = 1; j <= n; j++) { // Inner loop for columns
        if ((i + j) % 2 === 0) {
            row += "*";
        } else {
            row += " ";
        }
    }
    console.log(row);
}
```
***

## Question 9: Hollow Square Pattern
Print a hollow square pattern with `*`:

### Example for `n = 5`:
```text
*****
*   *
*   *
*   *
*****
```

### Solution:
```js
let n = 5; // Size of the square

for (let i = 1; i <= n; i++) { // Outer loop for rows
    let row = "";
    for (let j = 1; j <= n; j++) { // Inner loop for columns
        if (i === 1 || i === n || j === 1 || j === n) {
            row += "*";
        } else {
            row += " ";
        }
    }
    console.log(row);
}
```
***

## Question 10: Hollow Triangle Pattern
Print a hollow triangle pattern with `*`:

### Example for `n = 5`:
```text
    *
   * *
  *   *
 *     *
*********
```

### Solution:
```js
let n = 5; // Number of rows

for (let i = 1; i <= n; i++) {
    let row = "";
    for (let j = 1; j <= n - i; j++) {
        row += " ";
    }
    for (let k = 1; k <= 2 * i - 1; k++) {
        if (k === 1 || k === 2 * i - 1 || i === n) {
            row += "*";
        } else {
            row += " ";
        }
    }
    console.log(row);
}
```
***
These questions cover various patterns and their solutions using nested loops. Let me know if you need more patterns or additional explanations!

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

### Use Existing Arrays as Elements
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

### Access Elements of a Multidimensional Array
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


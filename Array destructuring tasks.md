Here’s a practical question-and-answer set on array destructuring:
***

### Question 1: Extract First Two Fruits
Given the array:
```js
const fruits = ["Apple", "Mango", "Pineapple", "Orange"];
```
Destructure it to extract the first two fruits into variables `fruit1` and `fruit2`.

##### Answer:
```js
const fruits = ["Apple", "Mango", "Pineapple", "Orange"];
const [fruit1, fruit2] = fruits;

console.log(fruit1); // Output: Apple
console.log(fruit2); // Output: Mango
```
***

### Question 2: Skip Elements
Given the array:
```js
const numbers = [10, 20, 30, 40, 50];
```
Destructure it to extract the first and third numbers into variables `first` and `third`.

##### Answer:
```js
const numbers = [10, 20, 30, 40, 50];
const [first, , third] = numbers;

console.log(first); // Output: 10
console.log(third); // Output: 30
```
***

### Question 3: Provide Default Values
Given the array:
```js
const colors = ["Red", "Green"];
```
Destructure it to extract three colors into variables `color1`, `color2`, and `color3`, setting a default value for `color3` as `"Blue"`.

##### Answer:
```js
const colors = ["Red", "Green"];
const [color1, color2, color3 = "Blue"] = colors;

console.log(color1); // Output: Red
console.log(color2); // Output: Green
console.log(color3); // Output: Blue
```
***

### Question 4: Swap Two Variables
Using array destructuring, swap the values of `x` and `y`.

##### Answer:
```js
let x = 5;
let y = 10;

// Swapping using destructuring
[x, y] = [y, x];

console.log(x); // Output: 10
console.log(y); // Output: 5
```
***

### Question 5: Nested Destructuring
Given the nested array:
```js
const nestedArray = [1, [2, 3], 4];
```
Destructure it to extract the value `1` into a, `2` into `b`, and `3` into `c`.

##### Answer:
```js
const nestedArray = [1, [2, 3], 4];
const [a, [b, c]] = nestedArray;

console.log(a); // Output: 1
console.log(b); // Output: 2
console.log(c); // Output: 3
```
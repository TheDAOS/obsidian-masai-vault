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

```
Destructure it to extract three colors into variables `color1`, `color2`, and color3, setting a default value for color3 as "Blue".
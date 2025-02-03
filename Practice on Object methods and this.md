
## Question 1: Adding Methods to an Object
Create an object named `calculator` with the following properties and methods:
1. `a` and `b` (properties to store two numbers).
2. `add` (a method that returns the sum of `a` and `b`).
3. `subtract` (a method that returns the difference of `a` and `b`).

```js
const calculator = {
  a: 10,
  b: 5,
  add: function () {
    // Your code here
  },
  subtract: function () {
    // Your code here
  },
};

console.log(calculator.add()); // Expected Output: 15
console.log(calculator.subtract()); // Expected Output: 5
```
***

## Question 2: `this` in Object Methods
What will be the output of the following code?

```js
const user = {
  firstName: "Arya",
  lastName: "Stark",
  getFullName: function () {
    return `${this.firstName} ${this.lastName}`;
  },
};

console.log(user.getFullName());
```

***

## Question 3: Compute the Area of a Rectangle

### Problem Statement:
Create an object `rectangle` with properties `length` and `width` and a method `getArea` that calculates and returns the area of the rectangle.

### Solution:
```js
const rectangle = {
  length: 5,
  width: 3,
  getArea: function () {
    return this.length * this.width;
  },
};

console.log(rectangle.getArea()); // Output: 15
```
***

## Question 4: Determine if a Number is Even or Odd

### Problem Statement:
Create an object `numberChecker` with a property `number` and a method `isEven` that returns `true` if the number is even and `false` if it is odd.
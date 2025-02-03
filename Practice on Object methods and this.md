
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

### Solution:
```js
const numberChecker = {
  number: 4,
  isEven: function () {
    return this.number % 2 === 0;
  },
};

console.log(numberChecker.isEven()); // Output: true
numberChecker.number = 7;
console.log(numberChecker.isEven()); // Output: false
```
***

## Question 5: Bank Account Object with Methods
Let’s consider a real-world example where a bank account object can perform operations like deposit and withdrawal using methods.

### Code Example:
```js
let bankAccount = {
  accountHolder: "Jane Doe",
  balance: 5000,
  deposit: function(amount) {
    this.balance += amount;
    console.log("Deposited: " + amount + ". New Balance: " + this.balance);
  },
  withdraw: function(amount) {
    if (amount > this.balance) {
      console.log("Insufficient funds.");
    } else {
      this.balance -= amount;
      console.log("Withdrew: " + amount + ". Remaining Balance: " + this.balance);
    }
  }
};

bankAccount.deposit(1000);  // Output: Deposited: 1000. New Balance: 6000
bankAccount.withdraw(3000);  // Output: Withdrew: 3000. Remaining Balance: 3000
bankAccount.withdraw(4000);  // Output: Insufficient funds.
```

##### Explanation:
- The `deposit` method adds money to the balance.
- The `withdraw` method subtracts money from the balance, but only if there are sufficient funds.

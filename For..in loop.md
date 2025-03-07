## Introduction to `for...in` Loop
The `for...in` loop is a special loop in JavaScript used to iterate over the **keys** (or properties) of an object. It allows you to traverse each key in an object one by one.

##### Syntax of `for...in` Loop:
```js
for (let key in object) {
  // Code to execute for each key
}
```
***
### Example 1: Basic Iteration
```javascript
let person = {
    firstName: "Arya",
    lastName: "Stark",
    age: 18,
    title: "Lady of Winterfell"
};

for (let key in person) {
    console.log(`${key}: ${person[key]}`);
}
```

##### Output:
```js
firstName: Arya
lastName: Stark
age: 18
title: Lady of Winterfell
```
***
### Example: Using `for...in` to Traverse an Object

```js
let person = {
  name: "John",
  age: 30,
  occupation: "Developer"
};

for (let key in person) {
  console.log(key + ": " + person[key]);
}

// Output:
// name: John
// age: 30
// occupation: Developer
```
***
### Filtering Keys

```js
let student = {
    name: "Samwell Tarly",
    age: 22,
    grade: "A",
    isGraduate: true
};

// Only log properties with string values
for (let key in student) {
    if (typeof student[key] === "string") {
        console.log(`${key}: ${student[key]}`);
    }
}
```

##### Output:
```js
name: Samwell Tarly
grade: A
```
***
### Counting Object Properties

```js
let house = {
    name: "Stark",
    region: "North",
    motto: "Winter is Coming"
};

let count = 0;
for (let key in house) {
    count++;
}
console.log(`Number of properties: ${count}`);
```

##### Output:
```js
Number of properties: 3
```
***
### Modify Object Values

```js
let prices = {
    bread: 2,
    milk: 1.5,
    cheese: 5
};

// Apply a 10% discount
for (let item in prices) {
    prices[item] = prices[item] * 0.9;
}

console.log(prices);
```

##### Output:
```js
{
  bread: 1.8,
  milk: 1.35,
  cheese: 4.5
}
```

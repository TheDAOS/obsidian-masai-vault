## Scenario: Managing a `course` Object

#### 1. Define a variable named `course` and assign an empty object to it.

```js
let course = {};
```

#### 2. Add a key `courseName` to the object with the value `"JavaScript Basics"`.

```js
course.courseName = "JavaScript Basics";
```

#### 3. Using `console.log`, log the value of the `courseName` key from the `course` object.

```js
console.log(course.courseName);
```

#### 4. Add another key `duration` to the object with the value `30`.

```js
course.duration = 30;
```

#### 5. Using `console.log`, log the value of the `duration` key from the `course` object.

```js
console.log(course.duration);
```

#### 6. Add another key `isOnline` with the value `true` to indicate if the course is online.

```js
course.isOnline = true;
```

#### 7. Using `console.log`, print the value of the `isOnline` key from the `course` object. 

```js
console.log(course.isOnline);
```

#### 8. Add a key `101` to the object with the value `"Introduction to Programming"`.

```js
course[101] = "Introduction to Programming";
```

#### 9. Using `console.log`, print the value of key `101` from the `course` object.

```js
console.log(course[101]);
```

#### 10. Check the total number of keys in the `course` object using the `Object.keys` method.

```js
let totalKeys = Object.keys(course).length;
console.log(totalKeys);
```

#### 11. Can you use reserved keywords like `class` or `function` as keys in an object? Why?

```js
"Yes, reserved keywords like `class` or `function` can be used as keys in an object because they are treated as strings."
```

#### 12. Remove the `isOnline` key from the `course` object and print the object before and after deleting the key.

```js
console.log(course);
delete course.isOnline;
console.log(course);
```

#### 13. Update the value of the `duration` key to `40` and print the updated object.

```js
course.duration = 40;
console.log(course);
```


This version uses a new context (course management) and provides a fresh take on the original set of questions.

Here is a completely re-imagined set of questions with **different scenarios**:

#### 1.
```js
let book = {
  title: 'JavaScript Basics',
  author: 'John Doe',
};
console.log(book.title);
```
##### Output:
**Explanation:** The `title` property is accessed using dot notation.
***
#### 2.
```js
let book = {
  title: 'JavaScript Basics',
  author: 'John Doe',
};
console.log(book['author']);
```
##### Output:
**Explanation:** The `author` property is accessed using bracket notation.
***
#### 3.
```js
let car = {
  brand: 'Tesla',
  model: 'Model S',
};

car.model = 'Model X';
console.log(car.model);
```
##### Output:
**Explanation:** The `model` property is updated to a new value.
***
#### 4.
```js
let pencil = {};
pencil.color = 'yellow';
console.log(pencil.color);
```
##### Output:
**Explanation:** The `color` property is dynamically added to the `pencil` object.
***
#### 5.
```js
let car = {
  brand: 'Tesla',
  model: 'Model S',
};

console.log(car['price']);
```
##### Output:
**Explanation:** Accessing a non-existent property returns `undefined`.
***
#### 6.
```js
let laptop = {
  details: function () {
    return 'This is a high-performance laptop.';
  },
  brand: 'Dell',
};
console.log(laptop.details());
```
##### Output:
**Explanation:** The `details` method is called, returning a string.
***
#### 7.
```js
let laptop = {
  brand: 'HP',
  description: function () {
    return `This laptop is made by ${this.brand}.`;
  },
};
console.log(laptop.description());
```
##### Output:
**Explanation:** The `description` method accesses the `brand` property using `this`.
***
#### 8.
```js
let smartphone = {
  callQuality: function () {
    return 'Call quality is excellent.';
  },
  brand: 'Samsung',
};
console.log(smartphone.callQuality());
```
##### Output:
**Explanation:** The `callQuality` method is called, returning a predefined string.
***
#### 9.
```js
let waterBottle = {
  capacity: '1 Litre',
  checkSize: function (requiredSize) {
    if (requiredSize > 1) {
      return 'This bottle is too small.';
    } else {
      return 'This bottle is sufficient.';
    }
  },
};
console.log(waterBottle.checkSize(2));
```
##### Output:
**Explanation:** The `checkSize` method evaluates the condition and returns the appropriate string.
***
#### 10.
```js
function reusableFunction() {
  return 'This function can be reused.';
}
let toolkit = {
  utility: reusableFunction,
};
console.log(toolkit.utility());
```
##### Output:
**Explanation:** The `utility` property is assigned a global function, which is then called.
***
#### 11.
```js
let person = {
  age: 30,
  address: {
    city: 'New York',
    country: 'USA',
  },
};
console.log(person.address.city);
```
##### Output:
**Explanation:** The nested `city` property is accessed using dot notation.
***
#### 12.
```js
let person = {
  age: 30,
  address: {
    city: 'New York',
    country: 'USA',
  },
};
person.address.zip = '10001';
console.log(person.address.zip);
```
##### Output:
**Explanation:** A new property `zip` is dynamically added to the `address` object.
***
#### 13.
```js
let person = {
  age: 30,
  address: {
    city: 'New York',
    country: 'USA',
  },
};
console.log(person);
delete person.age;
console.log(person);
```
##### Output:
**Explanation:** The `age` property is removed using the `delete` keyword.
***
#### 14.
```js
var organization = {
  teamA: {
    totalMembers: '12',
  },
  teamB: {
    totalMembers: '10',
  },
  teamC: {
    totalMembers: '8',
  },
};
console.log(organization.teamA.totalMembers);
```
##### Output:
**Explanation:** The nested `totalMembers` property is accessed using dot notation.
***
#### 15.
```js
var animal = {
  type: 'Cat',
};
console.log('type' in animal);
```
##### Output:
**Explanation:** The `in` operator checks for the existence of the `type` property in the `animal` object.
***

This set introduces **new objects, properties, and scenarios**, ensuring originality and relevance to object manipulation concepts in JavaScript.

***
Here’s an updated version of the exercise that does not use object methods:

#### Instructions
1. Create a variable named `warrior` using let and assign it an empty object.

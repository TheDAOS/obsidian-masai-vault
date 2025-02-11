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
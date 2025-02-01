## JavaScript Objects
JavaScript object is a variable that can store multiple data in **key-value** pairs.

##### Example
```js
// student object
const student = {
    firstName: "Jack",
    rollNo: 32
};
console.log(student);

// Output: { firstName: 'Jack', rollNo: 32 }
```

Here, `student` is an object that stores the first name and the roll number of students as key-value pairs.
***
## Create JavaScript Objects

##### The syntax of JavaScript object is:
```js
const objectName = {
    key1: value1,
    key2: value2,
    ...,
    keyN: valueN
};
```

Here,
- `objectName` - Name of the object.
- `key1: value1` - The first key-value pair.
- `key2: value2` - The second key-value pair.
- `keyN: valueN` - The `Nth` key-value pair.
Each key-value pair has a colon `:` between them and is separated by a comma `,`.
***
## Example 1: JavaScript Objects

```js
// create person object
const person = {
    name: "John",
    age: 20
};
console.log(person);

// Output: { name: "John", age: 20 }
```

In the above example, `name: "John"` and `age: 30` are key-value pairs.
**Note:** You can also create objects in a single line. For example,

```js
const person = { name: "John", age: 20 };
```

However, it's preferable to break down objects into multiple lines for better readability.
***
## JavaScript Object Properties

In JavaScript, the key-value pairs of an object are referred to as **properties**. For example,
```js
const person = {
    name: "John",
    age: 20,
};
```

Here, `name: "John"` and `age: 30` are the properties of the object person.
***
## Access Object Properties

You can access the **value** of a property by using its **key**.

**1. Using Dot Notation**
We can also include functions inside an object. For example,

```js
const person = {
    name: "Bob",
    age: 30,

    // use function as value
    greet: function () {
        console.log("Bob says Hi!");
    }

};

// call object method
person.greet();  // Bob says Hi!
```

Here, we have assigned a function as a value for the greet key.
These functions that are defined inside objects are called **methods**.
**Note:** Just like we use `()` to call a function, we must use `()` to call methods.

## JavaScript Method
A JavaScript method is a function defined within an object. For example,

```js
// dog object
const dog = {
    name: "Rocky",

    // bark method
    bark: function () {
        console.log("Woof!");
    }

};

// access method
dog.bark();
// Output: Woof!
```

In the above example, the dog object has two keys: name and bark.
Since the bark key holds a function, we refer to it as a **method**.
Notice that we accessed the `bark()` method using `dog.bark()`. Thus, the syntax to access an object method is:
```js
objectName.methodKey()
```

## Add Methods to an Object
You can add more methods to a JavaScript object even after we've defined it. For example,

```js
// student object
let student = {
    name: "John"
};

// add new method
student.greet = function () {
    console.log("Hello");
};
// access greet() method
student.greet();

// Output: Hello
```

In the above example, we created the student object with the property `name: "John"`.
Initially, student did not have any method. So, we used the dot notation to add a new method to the object:

```js
student.greet = function() {
    console.log("Hello");
};
```
***
# Inbuilt object methods

## 1. `Object.keys()`

- **Definition:** This method returns an array of a given object's own enumerable property names, iterated in the same order that a normal loop would.
- **Syntax:** `Object.keys(obj)`
- **Examples:**
	- **Example 1: Basic Usage**
		```js
		const car = { make: 'Toyota', model: 'Corolla', year: 2021 };
		const keys = Object.keys(car);
		console.log(keys);  // Output: ["make", "model", "year"]
		```

	- **Example 2: Filtering Properties**
		```js
		const scores = { Alice: 88, Bob: 77, Charlie: 93 };
		const passed = Object.keys(scores).filter(name => scores[name] > 80);
		console.log(passed);  // Output: ["Alice", "Charlie"]
		```

## 2. `Object.values()`

- **Definition:** This method returns an array of a given object's own enumerable property values, in the same order as provided by a `for...in` loop (the difference being that a `for...in` loop enumerates properties in the prototype chain as well).
- **Syntax:** `Object.values(obj)`
- **Examples:**
	- **Example 1: Basic Usage**
		```js
		const person = { name: 'Alice', age: 25 };
		const values = Object.values(person);
		console.log(values);  // Output: ["Alice", 25]
		```

	- **Example 2: Calculating Sum**
		```js
		const numbers = { a: 10, b: 20, c: 30 };
		const total = Object.values(numbers).reduce((sum, num) => sum + num, 0);
		console.log(total);  // Output: 60
		```

## 3. `Object.entries()`

- **Definition:** This method returns an array of a given object's own enumerable string-keyed property `[key, value]` pairs.
- **Syntax:** `Object.entries(obj)`
- **Examples:**
	- **Example 1: Iterating Entries**
		```js
		const book = { title: '1984', author: 'George Orwell', year: 1949 };
		Object.entries(book).forEach(([key, value]) => {
		  console.log(`${key}: ${value}`);
		});
		// Output:
		// title: 1984
		// author: George Orwell
		// year: 1949
		```

	- **Example 2: Conversion to Map**
		```js
		const settings = { darkMode: true, notifications: false, location: true };
		const settingsMap = new Map(Object.entries(settings));
		console.log(settingsMap);  // Output: Map(3) {"darkMode" => true, "notifications" => false, "location" => true}
		```

## Object.assign()
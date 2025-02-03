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

## 4. `Object.assign()`

- **Definition:** This method is used to copy all enumerable own properties from one or more source objects to a target object. It returns the modified target object.
- **Syntax:** `Object.assign(target, ...sources)`
- **Examples:**
	- **Example 1: Merging Objects**
		```js
		const target = { a: 1, b: 2 };
		const source = { b: 4, c: 5 };
		const returnedTarget = Object.assign(target, source);
		console.log(returnedTarget);  // Output: { a: 1, b: 4, c: 5 }
		```

	- **Example 2: Cloning an Object**
		```js
		const original = { name: 'Fido', breed: 'Labrador' };
		const clone = Object.assign({}, original);
		console.log(clone);  // Output: { name: 'Fido', breed: 'Labrador' }
		```

## 5. `Object.freeze()`

- **Immutability:** `Object.freeze()` makes an object completely immutable. This means you cannot add, delete, or modify any properties of the object. The object is effectively "frozen" in its current state.
- **Effect on properties:**
	- **Existing properties** cannot be changed or deleted.
	- **New properties** cannot be added.
	- **Writable properties** become non-writable.
	- **Configurable properties** become non-configurable.
- **Example:**
	```js
	const obj = {
	  name: "John",
	  age: 30
	};
	
	Object.freeze(obj);
	
	obj.name = "Jane"; // This will fail silently (or throw an error in strict mode)
	delete obj.age;    // This will fail silently (or throw an error in strict mode)
	obj.gender = "male"; // This will fail silently (or throw an error in strict mode)
	
	console.log(obj); // { name: "John", age: 30 }
	```

## 6. `Object.seal()`

- **Partial immutability:** `Object.seal()` allows you to modify existing properties of the object, but you cannot add or delete properties.
- **Effect on properties:**
	- **Existing properties** remain writable but become non-configurable.
	- **New properties** cannot be added.
	- **Existing properties** cannot be deleted.
- **Example:**
	```js
	const obj = {
	  name: "John",
	  age: 30
	};
	
	Object.seal(obj);
	
	obj.name = "Jane"; // This is allowed
	delete obj.age;    // This will fail silently (or throw an error in strict mode)
	obj.gender = "male"; // This will fail silently (or throw an error in strict mode)
	
	console.log(obj); // { name: "Jane", age: 30 }
	```


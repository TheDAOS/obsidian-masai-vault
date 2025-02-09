Here’s a set of 10 tasks on object destructuring, covering various use cases
***

### Task 1: Basic Object Destructuring
Given the object:
```js
const person = { name: "John", age: 30, city: "New York" };
```

1. Destructure it to extract `name`, `age`, and `city`.
2. Log each variable.
***

### Task 2: Renaming Variables
Given the object:
```js
const book = { title: "The Alchemist", author: "Paulo Coelho" };
```

1. Destructure it to extract `name`, `age`, and `city`.
2. Log each variable.
***

### Task 3: Default Values
Given the object:
```js
const product = { name: "Laptop", price: 800 };
```

1. Destructure it to extract `name`, `price`, and `stock`, assigning a default value of `100` to `stock`.
2. Log all variables.
***

### Task 4: Nested Object Destructuring
Given the object:
```js
const user = {
  id: 101,
  profile: { firstName: "Alice", lastName: "Smith" },
};
```

1. Destructure the object to extract `id`, `firstName`, and `lastName`.
2. Log the extracted values.
***

### Task 5: Destructuring with Rest Operator
Given the object:
```js
const car = { make: "Tesla", model: "Model S", year: 2023, color: "red" };
```

1. Destructure the object to extract `make` and `model`, and store the rest of the properties in a variable `others`.
2. Log `make`, `model`, and `others`.
***

### Task 6: Function Parameters with Destructuring
Create a function `displayUser` that takes an object parameter:
```js
const user = { name: "Bob", age: 25, profession: "Developer" };
```

1. Destructure the `name` and `profession` properties inside the function.
2. Log `"Bob is a Developer"`.
***

### Task 7: Destructuring in Loops
Given the array of objects:
```js
const students = [
  { id: 1, name: "Alice", grade: "A" },
  { id: 2, name: "Bob", grade: "B" },
  { id: 3, name: "Charlie", grade: "C" },
];
```

1. Use a `for...of` loop to destructure each object and log `Name: Alice, Grade: A`, and so on.
***

### Task 8: Renaming Nested Properties
Given the object:
```js
const employee = {
  id: 456,
  details: { fullName: "John Doe", position: "Manager" },
};
```

1. Destructure it to extract `id`, `details.fullName` as `name`, and `details.position` as `role`.
2. Log `id`, `name`, and `role`.
***

### Task 9: Combining Default Values with Renaming
Given the object:
```js
const gadget = { brand: "Apple", model: "iPhone 13" };
```

1. Destructure it to extract `brand` as `manufacturer`, `model`, and `warranty` with a default value of `1 year`.
2. Log `manufacturer`, `model`, and `warranty`.
***

### Task 10: Dynamic Property Destructuring
Given the object:
```js
const inventory = {
  product: "Tablet",
  quantity: 50,
  price: 300,
};
```

1. Create a function `getDetails` that takes the object and a key (e.g., `"price"`) as arguments.
2. Destructure the object to dynamically extract the value of the given key.
3. Log the result.
***
***
***

## Solutions:

### Task 1
```js
const person = { name: "John", age: 30, city: "New York" };
const { name, age, city } = person;

console.log(name); // Output: John
console.log(age);  // Output: 30
console.log(city); // Output: New York
```

### Task 2
```js
const book = { title: "The Alchemist", author: "Paulo Coelho" };
const { title: bookTitle, author: writer } = book;

console.log(bookTitle); // Output: The Alchemist
console.log(writer);    // Output: Paulo Coelho
```

### Task 3
```js
const product = { name: "Laptop", price: 800 };
const { name, price, stock = 100 } = product;

console.log(name);  // Output: Laptop
console.log(price); // Output: 800
console.log(stock); // Output: 100
```

### Task 4
```js
const user = {
  id: 101,
  profile: { firstName: "Alice", lastName: "Smith" },
};
const { id, profile: { firstName, lastName } } = user;

console.log(id);        // Output: 101
console.log(firstName); // Output: Alice
console.log(lastName);  // Output: Smith
```

### Task
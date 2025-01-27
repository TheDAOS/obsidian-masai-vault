## Using `for` Loop
In JavaScript, you can use a `for` loop to iterate over an array in a similar way to PHP:
```js
// Create an indexed array with four elements
const myArray = ['apple', 'banana', 'cherry', 'date'];

// Loop through the array and output each element
for (let i = 0; i < myArray.length; i++) {
  console.log(myArray[i] + ' ');
}

// Output:
// apple banana cherry date
```
- In this example, an indexed array named `myArray` is initialized with four elements: "apple", "banana", "cherry", and "date". These elements are accessed using numeric indexes, starting from 0. You can modify the value of an element in the array by referencing its index.
- The `for` loop is used to iterate over the array and display each element. The `.length` property of the array is used to determine the number of iterations needed.

##### Examples:
**Looping over an array of numbers**:
```js
const numbers = [10, 20, 30, 40, 50];
for (let number of numbers) {
  console.log(number + ' ');
}

// Output: 10 20 30 40 50
```

**Looping over an array of strings and numbers**:
```js
const mix = ['apple', 10, 'banana', 20, 'cherry', 30];
for (let i = 0; i < mix.length; i++) {
  console.log(mix[i] + ' ');
}

// Output: apple 10 banana 20 cherry 30
```

JavaScript also supports a more modern syntax for iterating over arrays:

#### Using `for...of` Loop
The `for...of` loop provides a simpler syntax for iterating over iterable objects such as arrays:
```js
const fruits = ["apple", "banana", "orange"];

for (let fruit of fruits) {
  console.log(fruit);
}

// Output:
// apple
// banana
// orange
```
**Note:** JavaScript's `forEach` method is another popular method for array iteration, offering a concise syntax for executing a function on each array element. However, the `for` loop and `for...of` loop provide more traditional and sometimes more flexible means for array iteration, especially when you need to break out of the loop or use an index within the loop body.

## Example 1: Summing All Elements in an Array

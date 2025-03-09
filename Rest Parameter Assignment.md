Here are the **questions and answers** on the **rest parameter** without using in-built methods or higher-order functions (HOFs):

### Question 1: Sum All Numbers
Write a function `sumAll` that accepts any number of arguments and returns their sum without using in-built methods.

##### Answer:
```js
function sumAll(...numbers) {
    let sum = 0;
    for (let i = 0; i < numbers.length; i++) {
        sum += numbers[i];
    }
    return sum;
}

console.log(sumAll(1, 2, 3, 4)); // Output: 10
console.log(sumAll(5, 10));      // Output: 15
```
***

### Question 2: Find Maximum
Create a function `findMax` that takes any number of arguments and returns the maximum value without using in-built methods.

##### Answer:
```js
function findMax(...numbers) {
    if (numbers.length === 0) return undefined; // Handle no arguments case
    let max = numbers[0];
    for (let i = 1; i < numbers.length; i++) {
        if (numbers[i] > max) {
            max = numbers[i];
        }
    }
    return max;
}

console.log(findMax(10, 20, 5, 30)); // Output: 30
console.log(findMax(1, -5, 3, 0));   // Output: 3
```
***

### Question 3: Filter Strings
Write a function `filterStrings` that accepts any number of arguments and returns an array containing only the string arguments.

##### Answer:
```js
function filterStrings(...args) {
    let strings = [];
    for (let i = 0; i < args.length; i++) {
        if (typeof args[i] === "string") {
            strings.push(args[i]);
        }
    }
    return strings;
}

console.log(filterStrings(1, "apple", true, "banana", 42)); // Output: ["apple", "banana"]
```
***

### Question 4: Join Words
Create a function `joinWords` that accepts a separator as the first argument and then any number of words. Return a single string where the words are joined by the separator without using in-built methods.

##### Answer:
```js
function joinWords(separator, ...words) {
    let result = "";
    for (let i = 0; i < words.length; i++) {
        result += words[i];
        if (i < words.length - 1) {
            result += separator;
        }
    }
    return result;
}

console.log(joinWords("-", "apple", "banana", "cherry")); // Output: "apple-banana-cherry"
console.log(joinWords(" ", "Hello", "World"));           // Output: "Hello World"
```
***

### Question 5: Exclude the First Two
Write a function `excludeFirstTwo` that accepts multiple arguments and returns an array of all arguments except the first two without using in-built methods.

##### Answer:
```js
function excludeFirstTwo(...args) {
    let result = [];
    for (let i = 2; i < args.length; i++) {
        result.push(args[i]);
    }
    return result;
}

console.log(excludeFirstTwo(1, 2, 3, 4, 5)); // Output: [3, 4, 5]
console.log(excludeFirstTwo(10, 20));        // Output: []
```
***

### Question 6: Multiply All Except First
Create a function `multiplyAllExceptFirst` that takes a number as the first argument and any number of additional arguments. Return the product of all arguments except the first.

##### Answer:
```js
function multiplyAllExceptFirst(first, ...rest) {
    let product = 1;
    for (let i = 0; i < rest.length; i++) {
        product *= rest[i];
    }
    return product;
}

console.log(multiplyAllExceptFirst(2, 3, 4, 5)); // Output: 60 (3 * 4 * 5)
console.log(multiplyAllExceptFirst(10));        // Output: 1 (no other numbers)
```
***

### **Question 7: Object Destructuring**

Write a function `extractDetails` that accepts an object with properties `name`, `age`, and any additional details. Use the rest parameter to collect additional properties into a new object.

### **Answer:**
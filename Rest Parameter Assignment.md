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


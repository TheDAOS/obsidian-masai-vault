The JavaScript spread operator `...` is used to expand or spread out elements of an iterable, such as an array, string, or object.

This makes it incredibly useful for tasks like combining arrays, passing elements to functions as separate arguments, or even copying arrays.

*Here's a quick example of the spread statement. You can read the rest of the tutorial for more.*

##### Example
```js
let numbers = [1, 2, 3];

// equivalent to
// console.log(numbers[0], numbers[1], numbers[2])
console.log(...numbers);

// Output: 1 2 3
```

Here, we used the spread operator `...` inside `console.log()` to expand the numbers array into individual elements.
***

## JavaScript Spread Operator Inside Arrays
We can also use the spread operator inside arrays to expand the elements of another array. For example,
```js
let fruits = ["Apple", "Banana", "Cherry"];

// add fruits array to moreFruits1
// without using the ... operator
let moreFruits1 = ["Dragonfruit", fruits, "Elderberry"];

// spread fruits array within moreFruits2 array
let moreFruits2 = ["Dragonfruit", ...fruits, "Elderberry"];
console.log(moreFruits1);
console.log(moreFruits2);
```

##### Output
```
[ 'Dragonfruit', [ 'Apple', 'Banana', 'Cherry' ], 'Elderberry' ]
[ 'Dragonfruit', 'Apple', 'Banana', 'Cherry', 'Elderberry' ]
```

Here, `...fruits` expands the fruits array inside the moreFruits2 array, which results in moreFruits2 consisting only of individual string elements and no inner arrays.

On the other hand, the moreFruits1 array consists of an inner array because we didn't expand the fruits array inside it.

**Note:** Since the spread operator was introduced in ES6, some browsers may not support its use. To learn more, visit JavaScript Spread Operator support.
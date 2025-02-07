Destructuring is a JavaScript technique to extract values from arrays and objects quickly. Traditionally, we use indices to get values from arrays and properties (keys) to get values from objects. With destructuring, it is possible to extract multiple values in one go, thereby removing the need to access properties or elements by individual keys or indices.

## `Array Destructuring`

Here's a code snippet that assigns array elements to different variables. Notice how extensive the code is because we're accessing the elements one by one.

```js
const numbers = [1, 2, 3];

const a = numbers[0];
const b = numbers[1];
const c = numbers[2];

console.log(a, b, c) //1 2 3
```


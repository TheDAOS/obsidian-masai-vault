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

Here's the same example using destructuring. The code becomes concise and clean.

```js
const numbers = [1, 2, 3];

// destructuring
const [a, b, c] = numbers;

console.log(a, b, c); //1 2 3
```

##### Here's how the destructuring statement works:
- We wrap the variables that we want to assign values to in a pair of brackets.
- We now have an array on the left and right sides of the destructuring statement.
- Each variable on the left gets assigned a value corresponding to its index from the right

*i.e.* `a` has an index of `0`, so a gets the value `numbers[0]` . Similarly, `b` is assigned `numbers[1]` and c is assigned `numbers[2]`

## `Object Destructuring`

We made use of array indices for array destructuring. Here, we'll use object property names. And instead of wrapping the variables in brackets, we wrap them in a pair of braces.

```js
const person = {
    name: 'Masai',
    language: 'JS',
};

const { name, language } = person;

console.log(name, language) 
```

The destructuring statement checks for the property on the left in the object specified on the right and then assigns the value.


## `Additional Features`

Now that we've covered the basic syntax es for array and object destructuring, we can move on to a few more 'features' that the syntax brings.


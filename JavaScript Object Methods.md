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


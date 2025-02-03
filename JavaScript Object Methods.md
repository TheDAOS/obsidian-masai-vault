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


We use `this` keyword in an object method to access a property of the same object. For example,

```js
// person object
const person = {
    name: "John",
    age: 30,

    // method
    introduce: function () {
        console.log(`My name is ${this.name} and I'm ${this.age} years old.`);

    }
};

// access the introduce() method
person.introduce();

// Output: My name is John and I'm 30 years old.
```

In the above example, we created the person object with two properties (name and age) and a method `introduce()`.

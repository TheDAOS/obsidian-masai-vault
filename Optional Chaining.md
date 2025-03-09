## What is Optional Chaining (`?.`)?
Optional chaining, introduced in ECMAScript 2020, is a feature that simplifies the process of accessing properties and methods of nested objects or arrays when intermediate properties may be `null` or `undefined`.

The optional chaining operator (`?.`) allows you to access properties or methods without the need for explicit `null` or `undefined` checks. If any intermediate property in the chain is `null` or `undefined`, the expression short-circuits, and the result is set to `undefined`.

In programming, "short-circuiting" refers to the behavior where the evaluation of an expression stops as soon as a `null` or `undefined` value is encountered along the chain of properties or methods being accessed. Instead of continuing to evaluate the expression, the result is immediately set to `undefined`, and any subsequent property or method access is skipped.

Now, let's dive into practical examples to see how optional chaining works in real-world scenarios.

## How to Access Nested Properties
In this example, we have a JavaScript object representing a user with nested address information.

```jsx
const user = {
  name: "John",
  address: {
    city: "New York",
    zipcode: "10001"
  }
};

```

### Traditional Approach
The traditional way to access the `city` property within the user's address involves multiple checks to ensure that the properties exist and are not `null` or `undefined`.

```jsx
let city;
if (user && user.address && user.address.city) {
  city = user.address.city;
} else {
  city = "Unknown";
}

console.log("Traditional Approach:", city); // Output: New York

```

This code checks if the user object exists, if it has an `address` property, and if the `address` property has a `city` property. If any of these conditions fail, the `city` variable is set to "Unknown".

### Optional Chaining Approach
With optional chaining, accessing the nested city property becomes much simpler:

```jsx
const city = user?.address?.city || "Unknown";

console.log("Optional Chaining Approach:", city); // Output: New York

```

The `?.` operator is used to access the `city` property of the user's address. If any intermediate property (`user` or `address`) is `null` or `undefined`, the expression short-circuits, and the result is immediately set to "Unknown".

## How to Call Nested Methods
In this example, we have a user object with a method `getAddress()` that returns the user's address.

```jsx
const user = {
  name: "Alice",
  getAddress() {
    return {
      city: "San Francisco",
      zipcode: "94105"
    };
  }
};

```

### Traditional Approach
The traditional way to call the `getAddress()` method and access the `city` property involves additional checks to ensure that the method exists and returns a non-null value.

```jsx
let city;
if (user && user.getAddress) {
  const address = user.getAddress();
  if (address) {
    city = address.city;
  }
}

console.log("Traditional Approach:", city); // Output: San Francisco

```

This code first checks if the user object exists and if it has a `getAddress` method. Then it calls the method and checks if the returned `address` object exists before accessing its `city` property.

### Optional Chaining Approach
With optional chaining, calling the nested method and accessing the `city` property can be done in a more concise manner:

```jsx
const city = user?.getAddress?.().city || "Unknown";

console.log("Optional Chaining Approach:", city); // Output: San Francisco

```

Here, the optional chaining operator is used to call the `getAddress()` method and access its `city` property. If `getAddress` method or any intermediate property in the chain is `null` or `undefined`, the expression short-circuits, and the result is immediately set to "Unknown".

## Dynamic Property Access
In this example, we have an array of users, where each user may or may not have a profile.

```jsx
const users = [
  { id: 1, profile: { name: "Alice" } },
  { id: 2 },
  { id: 3, profile: { name: "Bob" } }
];

```

### Traditional Approach
The traditional way to access the profile name dynamically involves multiple checks for each user object in the array.

```jsx
const names = users.map(user => {
  if (user && user.profile && user.profile.name) {
    return user.profile.name;
  } else {
    return "Unknown";
  }
});

console.log("Traditional Approach:", names); // Output: ["Alice", "Unknown", "Bob"]

```

This code uses `map()` to iterate over each user object in the array and checks if it has a profile with a `name` property. If the `name` property exists, it is returned – otherwise, "Unknown" is returned.

### Optional Chaining Approach
With optional chaining, dynamic property access becomes more straightforward:

```jsx
const names = users.map(user => user?.profile?.name || "Unknown");

console.log("Optional Chaining Approach:", names); // Output: ["Alice", "Unknown", "Bob"]

```

Here, the optional chaining operator is used to access the `name` property of each user's profile. If any intermediate property in the chain is `null` or `undefined`, the expression short-circuits, and "Unknown" is returned as the default value.

### Question 1: Accessing Nested Properties
Given the following object:

```js
javascript
Copy code
const person = {
    name: "Alice",
    address: {
        city: "New York",
        zip: "10001",
    },
};

```
Write a function `getZipCode` that returns the zip code if it exists, otherwise returns `"Zip code not found"` using optional chaining.

### Traditional method
```js
function getZipCode(person) {
    if (person && person.address && person.address.zip) {
        return person.address.zip;
    }
    return "Zip code not found";
}

const person = {
    name: "Alice",
    address: {
        city: "New York",
        zip: "10001",
    },
};

console.log(getZipCode(person)); // Output: "10001"
console.log(getZipCode({}));     // Output: "Zip code not found"
console.log(getZipCode(null));   // Output: "Zip code not found"
```

### Using optional chaining
```js
function getZipCode(person) {
    return person?.address?.zip || "Zip code not found";
}

console.log(getZipCode(person)); // Output: "10001"
console.log(getZipCode({}));     // Output: "Zip code not found"
```

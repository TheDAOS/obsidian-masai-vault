Here are a few additional code snippets with questions and their solutions for better understanding:
***
## Code Snippet 1: Block Scope for `var`, `let`, and `const`

```js
{
    var x = 5;
    let y = 10;
    const z = 15;
}
console.log(x); // What will this print?
console.log(y); // What will this print?
console.log(z); // What will this print?
```

### Solution:
- `x` is defined using `var` which does not have block scope. It will print `5`.
- `y` and `z` are defined using `let` and `const` which have block scope, so they are not accessible outside the block. It will throw a `ReferenceError` for both `y` and `z`.
***
## Code Snippet 2: Function Scope for `var`

```js
function testVarScope() {
    var num = 10;
    if (true) {
        var num = 20;
        console.log(num); // What will this print?
    }
    console.log(num); // What will this print?
}
testVarScope();
```

### Solution:
- The variable `num` inside the `if` block re-declares the same `num` in the function scope because `var` does not have block scope. Both console logs will print `20`.
***
## Code Snippet 3: Block Scope for `let`

```js
function testLetScope() {
    let num = 10;
    if (true) {
        let num = 20;
        console.log(num); // What will this print?
    }
    console.log(num); // What will this print?
}
testLetScope();
```

### Solution:
- The `num` declared inside the `if` block is a separate variable due to block scope of `let`. The first console log will print `20`, and the second will print `10`.
***
## Code Snippet 4: Variable Shadowing

```js
let globalVar = 100;
function shadowingExample() {
    let globalVar = 200; // Is this allowed? What will it print?
    console.log(globalVar);
}
shadowingExample();
console.log(globalVar);
```

### Solution:
- Yes, this is allowed. The `let globalVar` inside the function shadows the outer `globalVar`.
- Inside the function, it will print `200`.
- Outside the function, it will print `100`.
***
## Code Snippet 5: Hoisting with `var`

```js
function hoistingExample() {
    console.log(hoistedVar); // What will this print?
    var hoistedVar = 50;
    console.log(hoistedVar); // What will this print?
}
hoistingExample();
```

### Solution:
- The `hoistedVar` declaration is hoisted, but its value is not. The first log will print undefined, and the second will print `50`.
***
## Code Snippet 6: Hoisting with `let` and `const`

```js
function hoistingLetConst() {
    console.log(letVar); // What will this print?
    let letVar = 30;
    console.log(constVar); // What will this print?
    const constVar = 40;
}
hoistingLetConst();
```

### Solution:
- Both `let` and `const` variables are hoisted but are in a "temporal dead zone" until their declaration. Accessing them before declaration throws a `ReferenceError`.
***
## Code Snippet 7: Re-declaration with var, let, and const
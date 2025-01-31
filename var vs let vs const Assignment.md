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
## Code Snippet 7: Re-declaration with `var`, `let`, and `const`

```js
var num1 = 10;
var num1 = 20; // Is this allowed?
console.log(num1);

let num2 = 30;
let num2 = 40; // Is this allowed? What happens?

const num3 = 50;
const num3 = 60; // Is this allowed? What happens?
```

### Solution:
- Re-declaration with `var` is allowed. `num1` will be `20`.
- Re-declaration with `let` is not allowed. It will throw a `SyntaxError` for `num2`.
- Re-declaration with `const` is also not allowed. It will throw a `SyntaxError` for `num3`.
***
These code snippets, paired with their solutions, cover various concepts like scope, hoisting, shadowing, and re-declaration rules in JavaScript.

Here are the **questions** along with **solutions** for the above functional scope examples:
***
## Question 1

```js
function testScope() {
    var x = 5;
    if (true) {
        var x = 10;
        console.log(x); // What will this print?
    }
    console.log(x); // What will this print?
}
testScope();
```

### Solution:
1. Inside the `if` block, `var x` re-declares the same variable `x` due to function scope. It prints `10`.
2. Outside the `if` block, `x` retains the value `10` since `var` does not have block scope. It prints `10`.
***
## Question 2

```js
function testBlockScope() {
    let y = 15;
    if (true) {
        let y = 25;
        console.log(y); // What will this print?
    }
    console.log(y); // What will this print?
}
testBlockScope();
```

### Solution:
1. Inside the `if` block, `let y = 25` creates a new block-scoped variable. It prints `25`.
2. Outside the `if` block, the outer `y` is still `15`. It prints `15`.
***
## Question 3

```js
function constScope() {
    const z = 50;
    if (true) {
        const z = 100;
        console.log(z); // What will this print?
    }
    console.log(z); // What will this print?
}
constScope();
```

### Solution:
1. Inside the `if` block, `const z = 100` creates a new block-scoped constant. It prints `100`.
2. Outside the `if` block, the outer `const z` remains `50`. It prints `50`.
***
## Question 4

```js
function testMixedScope() {
    var a = 10;
    let b = 20;
    const c = 30;
    if (true) {
        var a = 40;
        let b = 50;
        const c = 60;
        console.log(a); // What will this print?
        console.log(b); // What will this print?
        console.log(c); // What will this print?
    }
    console.log(a); // What will this print?
    console.log(b); // What will this print?
    console.log(c); // What will this print?
}
testMixedScope();
```

### Solution:
1. Inside the `if` block:
	- `var a = 40` re-declares the function-scoped `a`. It prints `40`.
	- let b = 50 creates a new block-scoped b. It prints `50`.
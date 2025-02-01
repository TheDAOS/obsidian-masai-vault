[[var vs let vs const]]
[[Ternary Operators]]
[[JavaScript Objects]]
***[[Scope of Variables And Anonymous Functions]]***

## 1. `let` and `const` Declarations: Block Scoping Rules

`let` and `const` were introduced in **ES6** and differ from the traditional `var` in that they follow **block scoping**.

### Block Scoping
Variables declared with `let` or `const` are scoped to the block in which they are defined, which means they are only accessible inside the pair of `{}` where they were declared.

##### Example:
```js
if (true) {
  let a = 10;
  const b = 20;
  console.log(a);  // Output: 10
  console.log(b);  // Output: 20
}

console.log(a);  // Error: a is not defined
console.log(b);  // Error: b is not defined
```
In this example, both `a` and `b` are only accessible within the `if` block. Attempting to access them outside the block will result in an error.

### When to use `let` and `const`:
- Use `let` for variables that you intend to reassign later.
- Use `const` for variables that should remain constant after their initial assignment.

***

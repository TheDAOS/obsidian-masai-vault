## Local Variables:

Local variables are those declared within a function and cannot be accessed outside of that function. They are created when the function starts and disappear when the function ends.

##### Example Explained:

Here’s a function that shows how local variables work:
```js
function showMessage() {
  let message = "Hello, I'm JavaScript!"; // local variable

  console.log(message);
}

showMessage(); // Logs: Hello, I'm JavaScript!
```
- `message` is a local variable inside the `showMessage` function.
- You can see the message when `showMessage()` is called because the variable is accessible inside the function.
- If you try to access `message` outside the function, like this:

```js
console.log(message); // Error! The variable is local to the function
```
- You will get an error because `message` doesn’t exist outside the function.

## Outer Variables:

Outer variables are those declared outside any function and can be accessed and modified by functions.

##### Example with Outer Variables:
```js
let userName = 'John'; // This is an outer variable

function showMessage() {
  let message = 'Hello, ' + userName; // Uses outer variable
  console.log(message);
}

showMessage(); // Logs: Hello, John
```
- `userName` is an outer variable and can be accessed inside the `showMessage` function.

### Modifying Outer Variables:

A function can modify an outer variable, affecting its value globally:
```js
let userName = 'John';

function showMessage() {
  userName = "Bob"; // Changed the outer variable

  let message = 'Hello, ' + userName;
  console.log(message);
}

console.log(userName); // Before the function call, logs: John

showMessage(); // Changes userName to Bob and logs: Hello, Bob

console.log(userName); // After the function call, logs: Bob
```
- The function `showMessage()` modifies the global variable `userName`.

### Local Shadowing:

If a local variable in a function has the same name as an outer variable, it "shadows" the outer variable:
```js
let userName = 'John';

function showMessage() {
  let userName = "Bob"; // Local variable shadows the outer variable

  let message = 'Hello, ' + userName; // Uses local userName
  console.log(message);
}

showMessage(); // Logs: Hello, Bob

console.log(userName); // Still logs: John, because the outer variable was not changed
```
- Inside `showMessage()`, the local `userName` takes precedence over the outer `userName`.

## Global Variables:

Variables declared outside all functions are global. They can be accessed and modified by any function unless a local variable inside a function shadows them.

##### Best Practice:
- Minimize the use of global variables as they can lead to code that is harder to manage and debug.

[[Function scopes Assignment]]

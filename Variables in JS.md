
***
# Variables Rules
- Variable names are case sensitive, "a" & "A" is different.
- Only letters, digits, underscore(\_) and $ is allowed. (not even space)
- Only a letter, underscore(\_) or $ should be 1st character.
- Reserved words cannot be variable names.

# Variables
A **variables** is a container for storing data. In JavaScript, variable are declared using the keywords `var`, `let`, or `const`. Each has its own scope and behavior, but they all serve the same basic purpose of holding data.
For now we'll be using `var` only but going on we'll learn more about `let` & `const`

## Example:
```js
var name = "Alice";  // string type
var age = 30;        // number type
var isMember = true; // boolean type
```

We can easily grasps the concept of a "variable" if we imagine it as a "box" for data, with a uniquely-named sticker on it: 

For instance, the variable `message` can be imagined as a box labelled `"message"` with the value `"Hello!"` in it:    

We can put any value in the box.    
We can also change it as many times as we want:    

```js
let message; 
message = 'Hello!'; 
message = 'World!'; // value 
changedalert(message);
```
When the value is changed, the old data is removed from the variable:
We can also declare two variables and copy data from one into the other.
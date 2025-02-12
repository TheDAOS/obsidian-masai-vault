`...rest` allow a function work with a variable number of arguments by bundling them into an array

## Handling Multiple Arguments in JavaScript Functions

### Fixed Parameters and Their Limitations
When defining a function with a fixed number of parameters, like:
```js
function sum(num1, num2) {
    console.log(num1 + num2);
}
```
This function will only handle the exact number of arguments it is expecting. Any extra arguments passed will be ignored.

##### Example:
```js
sum(20, 30);           // Output: 50
sum(20, 30, 40);       // Output: 50 (extra argument ignored)
sum(20, 30, 40, 50);   // Output: 50 (extra arguments ignored)
```

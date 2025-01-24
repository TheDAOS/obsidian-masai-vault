## JavaScript Default Parameters

Starting from **JavaScript ES6**, we can provide default values for function parameters.

These default values are used when the function is called without passing the corresponding arguments.

*Here's a quick example of JavaScript default parameters. You can read the rest of the tutorial for more details.*

#### Example
```js
function greet(name = "Guest") {
    console.log(`Hello, ${name}!`);
}

greet();

// Output: Hello, Guest!
```
In this example, the `greet()` function has a default parameter name with the string value `Guest`. Since we have not passed any argument to the function, it uses the default value.
***

## Example: JavaScript Default Parameters
```js
function sum(x = 3, y = 5) {
    // return sum
    return x + y;
}
// pass arguments to x and y
var result = sum(5, 15);
console.log(`Sum of 5 and 15: ${result}`);

// pass argument to x but not to y
result = sum(7);
console.log(`Sum of 7 and default value (5): ${result}`);

// pass no arguments
// use default values for x and y
result = sum();
console.log(`Sum of default values (3 and 5): ${result}`);
```


##### Output
```js
Sum of 5 and 15: 20
Sum of 7 and default value (5): 12
Sum of default values (3 and 5): 8
```

In the above example, the default value of x is 3 and the default value of y is 5.

- `sum(5, 15)` - When both arguments are passed,  takes 5 and  takes 15.
	x
	y
- `sum(7)` - When 7 is passed,  takes 7 and  takes the default value 5.
	x
	y
- `sum()` - When no argument is passed,  and  take the default values 3 and 5, respectively.
	x
	y
***
[[Using Default parameters Assignment]]

#### Task: Calculate Final Bill

##### Description:

Create a function `generateBill` that takes three parameters:
- `basePrice`
- `tax` (default value `0.1`)
- `discount` (default value `0.05`)

Call the function with:
- No arguments.
- Only the `basePrice` argument.
- All three arguments.

##### Solution:
```js
function generateBill(basePrice, tax = 0.1, discount = 0.05) {
    const finalPrice = basePrice + (basePrice * tax) - (basePrice * discount);
    return finalPrice;
}

// Test the function
console.log(generateBill(100)); // Default tax (10%) and discount (5%) applied
console.log(generateBill(200, 0.15)); // Default discount (5%) applied
console.log(generateBill(300, 0.2, 0.1)); // All custom values
```
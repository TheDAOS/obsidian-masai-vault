## Overview of if Statement
The `if` statement in JavaScript is used to execute a block of code based on whether a specified condition is true.

#### Syntax
```js
if (condition) {
    // block of code to be executed if the condition is true
}
```

#### Key Points:
- It evaluates the condition inside the parentheses (`()`).
- If the condition evaluates to true, the code block inside the curly braces `{}` is executed.
- JavaScript performs type conversion when evaluating conditions.

#### Examples:
- **If with a Boolean Value:**
	```js
	console.log("Code Start");
	if (true) {
	    console.log("Inside Code");
	}
	console.log("Code End");
	```

- **If with an Expression:**
	```js
	if (5 > 3) {
	    console.log("Inside Code");
	}
	```

- **If with Variables:**
	```js
	var name1 = "rahul";
	var name2 = "rahul";
	var check = (name1 == name2);
	
	if (check) {
	    console.log("Both Names are same");
	}
	```

- **For a single statement, you don't need braces:**
```js
let age = 18;
if (age >= 18)
    console.log("You are eligible to vote."); 

// This outputs "You are eligible to vote."
```

### Using `if-else`
The `if...else` statement in JavaScript allows you to control the flow of execution based on conditions, executing different blocks of code depending on whether a condition is true or false.
- **Definition**: The `if...else` statement executes one block of code if a condition is truthy and another block if the condition is falsy.
- **Falsy Values**:
	- `false`
	- `0` and `"0"` (zero and negative zero)
	- `0n` (BigInt zero)
	- `""`, `''`, or (empty strings)
	- `null`
	- `undefined`
	- `NaN` (not a number)

#### Syntax
```js
if (condition) {
    // Code to execute if the condition is true
} else {
    // Code to execute if the condition is false
}
```

#### Comparing Two Numbers
```js
var a = 3;
var b = 20;

if (a > b) {
    console.log("a is greater");
} else {
    console.log("a is not greater");
}
```

#### Check Whether Two Names are Equal
```js
var name1 = "suraj";
var name2 = "suraj";

if (name1 == name2) {
    console.log("Names are Equal");
} else {
    console.log("Names are not equal");
}
```

#### Real-Life Scenario: Hotel Bill Discount
- **Scenario:** Determine if a hotel bill qualifies for a discount based on a minimum spend threshold.
- **Code**:
	```js
	var total_bill = 699;
	var discount_start_price = 500;
	
	if (total_bill >= discount_start_price) {
	    console.log("Discount Available");
	} else {
	    console.log("No discount");
	}
	```

#### You can execute alternative code with `else` for vote eligibility example:
```js
let age = 16;
if (age >= 18) {
    console.log("You are eligible to vote.");
} else {
    console.log("You are not eligible to vote yet.");
}
```

- Determines if a person is eligible to vote based on age, with a binary outcome.
- If the age is 18 or above, it prints a message of eligibility; otherwise, it informs them that they are not eligible yet.

### Using `if else if else`
- The `else-if` statement in JavaScript allows for more complex conditional structures, providing a way to test multiple conditions sequentially. This structure is particularly useful when decisions need to be made based on multiple criteria.
- **Functionality**: When an `if` condition fails, the `else-if` conditions are evaluated in order. If one of these conditions evaluates to true, its associated block of code executes.
- **Flow Control**: The execution does not enter any remaining `else-if` conditions or the `else` block once a true condition is found.
- **Usage Context**: Ideal for scenarios where multiple potential conditions could lead to different outcomes.

#### Syntax
```js
if (condition1) {
    // Code to execute if condition1 is true
} else if (condition2) {
    // Code to execute if condition1 is false and condition2 is true
} else {
    // Code to execute if all conditions are false
}
```

#### Real-life Example: Applying Discounts Based on Total Bill
**Problem Statement**: Depending on the amount of the total bill at a restaurant, different discounts apply. The goal is to apply the correct discount based on the bill amount.

##### Example: Discount Calculation
```js
var total_bill = 799;

if (total_bill > 1000) {
    console.log("20% discount");
} else if (total_bill > 500) {
    console.log("10% discount");
} else {
    console.log("No discount");
}
```

#### Manage multiple conditions with `else if` for vote eligibility:
```js
let age = 18;
if (age < 18) {
    console.log("You are not eligible to vote yet.");
} else if (age == 18) {
    console.log("Congratulations, you are just eligible to vote!");
} else {
    console.log("You are eligible to vote.");
}
```
- This handles multiple sequential conditions to provide specific messages for those exactly at the voting age, below, or above.
- Checks if the person is below 18, exactly 18, or older, and displays a corresponding message for each scenario.

[[Conditional Statements Assignment]]

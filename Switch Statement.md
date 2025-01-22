## Introduction to the JavaScript `switch` Statement
The `switch` statement is a control structure used in JavaScript for making decisions based on the value of a single variable or expression. It simplifies the process of handling multiple conditional branches by grouping cases that share the same code block.

### Practical Example: ATM Machine Interface
Consider an ATM machine that offers multiple transaction options such as Deposit, Withdraw, and Change Pin. Each option triggers a different block of code:
- **Deposit** → Executes code to deposit money.
- **Withdraw** → Executes code to withdraw money.
- **Change Pin** → Executes code to change the user's PIN.
- **Default** → Executes default action, like showing the main menu or an error message.

### ATM Interface Example Using `if...else`
Consider an ATM machine where users can choose operations like viewing balance, withdrawing money, depositing money, or changing their PIN. Here's how you might handle this with `if...else`:

```js
let option = 2; // User selects option 2 (Withdraw Money)

if (option === 1) {
    console.log("You selected: View Balance");
} else if (option === 2) {
    console.log("You selected: Withdraw Money");
} else if (option === 3) {
    console.log("You selected: Deposit Money");
} else if (option === 4) {
    console.log("You selected: Change PIN");
} else {
    console.log("Invalid option selected");
}
```

- This approach works well for a few conditions but can become cumbersome and less efficient as the number of options grows.

### Syntax and Usage of `switch`
The `switch` statement compares a value against multiple possible matches and executes the corresponding code block. It's a cleaner solution for multiple distinct cases. 
Here’s the syntax:
```js
switch (expression) {
    case value1:
        // code to execute when expression equals value1
        break;
    case value2:
        // code to execute when expression equals value2
        break;
    default:
        // code to execute if expression doesn't match any case
        break;
}
```

### ATM Interface Example Using `switch`
Refactoring the earlier `if...else` example to use a `switch` statement simplifies and clarifies the code:
```js
let option = 2; // User selects option 2 (Withdraw Money)

switch (option) {
    case 1:
        console.log("You selected: View Balance");
        break;
    case 2:
        console.log("You selected: Withdraw Money");
        break;
    case 3:
        console.log("You selected: Deposit Money");
        break;
    case 4:
        console.log("You selected: Change PIN");
        break;
    default:
        console.log("Invalid option selected");
}
```


### Example-2: Greeting Based on Time of Day

```js
let timeOfDay = "morning";

switch (timeOfDay) {
    case "morning":
        console.log("Have some coffee.");
        break;
    case "noon":
        console.log("How about some lemonade?");
        break;
    case "evening":
        console.log("Time for some tea.");
        break;
    default:
        console.log("Water is always a good choice.");
}
```

### Example-3 Combining cases

Problem 2 : Given any character, if it is a vowel print "Vowel"
```js
var char = "i";

if((char == "a") || (char=="e") || (char=="i") || (char=="o") || (char=="u") )
{
  console.log("is a vowel");
}
else{
  console.log("not a vowel");
}
```

This scenario showcases how to combine multiple cases in a `switch` statement that perform the same action for different conditions.
```js
// Switch Case
var char = "i";

switch(char)
{
	case "a":
	case "e":
	case "i":
	case "o":
	case "u":console.log("vowel");
	          break;
	default : console.log("Not a vowel");
}
```

[[Switch Statement Assignment]]

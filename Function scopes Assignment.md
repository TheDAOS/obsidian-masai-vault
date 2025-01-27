## Question 1: Understanding Scope with Local Variables

**Objective**: Demonstrate the scope of local variables in a JavaScript function.

##### Requirements:
- Define a function named `displayLocalTime` that creates a local variable to hold the current time using `new Date().toLocaleTimeString()`.
- Inside the function, log the time to the console.
- After calling the function, attempt to log the time variable outside the function to illustrate the scope limitation.

## Question 2: Modifying Outer Variables from Inside a Function

**Objective**: Explore how JavaScript functions can modify outer variables and observe the effects of such changes outside the function.

##### Requirements:
- Define an outer variable named `appStatus` with the value `"Idle"`.
- Create a function named `updateStatus` that changes the value of `appStatus` to `"Active"`.
- Log the value of `appStatus` before and after calling `updateStatus` to show how the function impacts the outer variable.


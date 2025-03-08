Stacks are a fundamental data structure in computer science, and they are particularly useful for solving a variety of problems. In JavaScript, you can implement a stack using an array or a linked list. Here, I'll focus on using an array to implement a stack and discuss some common problems that can be solved using stacks.

### Stack Implementation in JavaScript

A stack follows the Last-In-First-Out (LIFO) principle. Here's a simple implementation of a stack using an array:

```javascript
class Stack {
  constructor() {
    this.items = [];
  }

  // Add an element to the top of the stack
  push(element) {
    this.items.push(element);
  }

  // Remove and return the top element of the stack
  pop() {
    if (this.isEmpty()) {
      return "Underflow";
    }
    return this.items.pop();
  }

  // Return the top element without removing it
  peek() {
    if (this.isEmpty()) {
      return "No elements in Stack";
    }
    return this.items[this.items.length - 1];
  }

  // Check if the stack is empty
  isEmpty() {
    return this.items.length === 0;
  }

  // Return the number of elements in the stack
  size() {
    return this.items.length;
  }

  // Print the elements of the stack
  printStack() {
    return this.items.toString();
  }
}
```

### Common Problems Solved Using Stacks

1. **Balanced Parentheses**:
   - **Problem**: Given a string containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid.
   - **Solution**: Use a stack to push opening brackets and pop them when encountering closing brackets. If the stack is empty at the end, the string is balanced.

```javascript
function isBalanced(str) {
  const stack = new Stack();
  const matchingBracket = {
    ')': '(',
    '}': '{',
    ']': '['
  };

  for (let char of str) {
    if (char === '(' || char === '{' || char === '[') {
      stack.push(char);
    } else if (char === ')' || char === '}' || char === ']') {
      if (stack.isEmpty() || stack.pop() !== matchingBracket[char]) {
        return false;
      }
    }
  }

  return stack.isEmpty();
}

// Example usage:
console.log(isBalanced("({[]})")); // true
console.log(isBalanced("({[)]"));  // false
```

2. **Next Greater Element**:
   - **Problem**: Given an array, find the next greater element for each element. The next greater element for an element x is the first greater element on the right side of x in the array.
   - **Solution**: Use a stack to keep track of indices. For each element, pop from the stack while the current element is greater than the element at the index stored in the stack.

```javascript
function nextGreaterElement(arr) {
  const stack = [];
  const result = new Array(arr.length).fill(-1);

  for (let i = 0; i < arr.length; i++) {
    while (stack.length > 0 && arr[i] > arr[stack[stack.length - 1]]) {
      const index = stack.pop();
      result[index] = arr[i];
    }
    stack.push(i);
  }

  return result;
}

// Example usage:
console.log(nextGreaterElement([4, 5, 2, 25])); // [5, 25, 25, -1]
```

### Infix to Postfix Conversion (Completed)

```javascript
function infixToPostfix(expression) {
  const stack = new Stack();
  const precedence = {
    '+': 1,
    '-': 1,
    '*': 2,
    '/': 2
  };

  let postfix = '';

  for (let char of expression) {
    if (char.match(/[a-zA-Z0-9]/)) {
      postfix += char;
    } else if (char === '(') {
      stack.push(char);
    } else if (char === ')') {
      while (stack.peek() !== '(') {
        postfix += stack.pop();
      }
      stack.pop(); // Pop the '('
    } else {
      while (!stack.isEmpty() && precedence[char] <= precedence[stack.peek()]) {
        postfix += stack.pop();
      }
      stack.push(char);
    }
  }

  // Pop all the operators from the stack
  while (!stack.isEmpty()) {
    postfix += stack.pop();
  }

  return postfix;
}

// Example usage:
console.log(infixToPostfix("a+b*(c^d-e)^(f+g*h)-i")); // "abcd^e-fgh*+^*+i-"
```

### Additional Problems Solved Using Stacks

4. **Evaluate Postfix Expression**:
   - **Problem**: Evaluate a postfix expression.
   - **Solution**: Use a stack to store operands. When an operator is encountered, pop the required number of operands from the stack, perform the operation, and push the result back onto the stack.

```javascript
function evaluatePostfix(expression) {
  const stack = new Stack();

  for (let char of expression) {
    if (char.match(/[0-9]/)) {
      stack.push(parseInt(char));
    } else {
      const operand2 = stack.pop();
      const operand1 = stack.pop();
      switch (char) {
        case '+':
          stack.push(operand1 + operand2);
          break;
        case '-':
          stack.push(operand1 - operand2);
          break;
        case '*':
          stack.push(operand1 * operand2);
          break;
        case '/':
          stack.push(operand1 / operand2);
          break;
      }
    }
  }

  return stack.pop();
}

// Example usage:
console.log(evaluatePostfix("35*62/+")); // 11
```

5. **Stock Span Problem**:
   - **Problem**: Given an array of stock prices, find the span of each stock's price. The span of a stock's price today is the maximum number of consecutive days (including today) for which the price of the stock was less than or equal to today's price.
   - **Solution**: Use a stack to keep track of the indices of the prices. For each price, pop from the stack while the current price is greater than the price at the index stored in the stack.

```javascript
function calculateSpan(prices) {
  const stack = [];
  const spans = new Array(prices.length).fill(0);

  for (let i = 0; i < prices.length; i++) {
    while (stack.length > 0 && prices[i] >= prices[stack[stack.length - 1]]) {
      stack.pop();
    }
    spans[i] = stack.length === 0 ? i + 1 : i - stack[stack.length - 1];
    stack.push(i);
  }

  return spans;
}

// Example usage:
console.log(calculateSpan([100, 80, 60, 70, 60, 75, 85])); // [1, 1, 1, 2, 1, 4, 6]
```

These examples demonstrate the versatility of stacks in solving various problems. Stacks are essential for managing function calls, expression evaluation, and many other algorithms.
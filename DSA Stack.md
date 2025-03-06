A stack is a fundamental data structure in computer science that follows the Last In, First Out (LIFO) principle. This means that the last element added to the stack will be the first one to be removed. Stacks are widely used in various applications, including function call management, expression evaluation, and undo mechanisms in text editors.

Stacks are a versatile and essential data structure in computer science, providing a simple yet powerful way to manage data in a LIFO manner.
## Key Operations of a Stack

1. **Push**: Adds an element to the top of the stack.
2. **Pop**: Removes the top element from the stack.
3. **Peek/Top**: Retrieves the top element without removing it.
4. **IsEmpty**: Checks if the stack is empty.
5. **IsFull**: Checks if the stack is full (if the stack has a fixed size).

## Implementation of a Stack in JavaScript

```javascript
class Stack {
    constructor() {
        this.items = [];
    }

    // Check if the stack is empty
    isEmpty() {
        return this.items.length === 0;
    }

    // Add an element to the top of the stack
    push(element) {
        this.items.push(element);
    }

    // Remove and return the top element of the stack
    pop() {
        if (this.isEmpty()) {
            throw new Error("Pop from an empty stack");
        }
        return this.items.pop();
    }

    // Return the top element without removing it
    peek() {
        if (this.isEmpty()) {
            throw new Error("Peek from an empty stack");
        }
        return this.items[this.items.length - 1];
    }

    // Return the number of elements in the stack
    size() {
        return this.items.length;
    }

    // Print the elements of the stack
    printStack() {
        console.log(this.items.toString());
    }
}

// Example usage
const stack = new Stack();
stack.push(1);
stack.push(2);
stack.push(3);

console.log("Top element is:", stack.peek());  // Output: Top element is: 3
console.log("Stack size is:", stack.size());   // Output: Stack size is: 3

console.log("Popped element is:", stack.pop());  // Output: Popped element is: 3
console.log("Stack size is:", stack.size());   // Output: Stack size is: 2

stack.printStack();  // Output: 1,2
```

### Explanation

1. **Constructor**: Initializes an empty array to store the stack elements.
2. **isEmpty**: Checks if the stack is empty by verifying if the length of the array is zero.
3. **push**: Adds an element to the top of the stack using the `push` method of the array.
4. **pop**: Removes and returns the top element of the stack using the `pop` method of the array. Throws an error if the stack is empty.
5. **peek**: Returns the top element without removing it. Throws an error if the stack is empty.
6. **size**: Returns the number of elements in the stack.
7. **printStack**: Prints the elements of the stack in a readable format.

## Applications of Stacks

1. **Function Call Management**: The call stack in programming languages manages function calls and local variables.
2. **Expression Evaluation and Syntax Parsing**: Stacks are used in algorithms for evaluating expressions (e.g., postfix notation) and parsing syntax.
3. **Undo Mechanisms**: In text editors and other applications, stacks are used to implement undo functionality.
4. **Depth-First Search (DFS)**: Stacks are used to implement DFS in graph traversal algorithms.
5. **Backtracking Algorithms**: Stacks are used to keep track of the current state in backtracking algorithms.

## Time Complexity

- **Push**: O(1)
- **Pop**: O(1)
- **Peek**: O(1)
- **IsEmpty**: O(1)
- **IsFull**: O(1) (if the stack has a fixed size)

## Space Complexity

The space complexity of a stack depends on the number of elements it can hold. If the stack is implemented using a dynamic array (like a list in Python), the space complexity is O(n), where n is the number of elements in the stack.

## Implementation of a Stack in Python

Here is a simple implementation of a stack using a list in Python:

```python
class Stack:
    def __init__(self):
        self.items = []

    def is_empty(self):
        return len(self.items) == 0

    def push(self, item):
        self.items.append(item)

    def pop(self):
        if self.is_empty():
            raise IndexError("Pop from an empty stack")
        return self.items.pop()

    def peek(self):
        if self.is_empty():
            raise IndexError("Peek from an empty stack")
        return self.items[-1]

    def size(self):
        return len(self.items)

# Example usage
if __name__ == "__main__":
    stack = Stack()
    stack.push(1)
    stack.push(2)
    stack.push(3)

    print("Top element is:", stack.peek())  # Output: Top element is: 3
    print("Stack size is:", stack.size())   # Output: Stack size is: 3

    print("Popped element is:", stack.pop())  # Output: Popped element is: 3
    print("Stack size is:", stack.size())   # Output: Stack size is: 2
```
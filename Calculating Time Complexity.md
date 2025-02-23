Calculating the time complexity of a piece of code involves analyzing how the execution time of the code grows relative to the size of the input. Here’s a step-by-step guide to help you understand and calculate time complexity easily:

### 1. **Identify the Input Size**
   - Determine what the input size (usually denoted as \( n \)) is. This could be the number of elements in an array, the number of nodes in a tree, etc.

### 2. **Analyze the Code Structure**
   - Look at the loops, recursive calls, and any other structures that affect execution time.

### 3. **Count Basic Operations**
   - Focus on the most significant operations (like comparisons, assignments, etc.) within loops and recursive calls.
   - For each loop, determine how many times it runs in relation to \( n \).

### 4. **Nested Loops**
   - If you have nested loops, multiply their complexities. For example, if you have a loop that runs \( n \) times and inside it another loop that also runs \( n \) times, the total complexity is \( O(n^2) \).

### 5. **Recursive Functions**
   - For recursive functions, use the **recurrence relation** to express the time complexity. For example, a function that calls itself twice for each input size can be expressed as \( T(n) = 2T(n/2) + O(1) \). You can solve this using the **Master Theorem** or by expanding the recurrence.

### 6. **Consider the Worst Case**
   - Time complexity is often expressed in terms of the worst-case scenario. Analyze the code to find the maximum number of operations that could occur.

### 7. **Use Big O Notation**
   - Express the time complexity using Big O notation, which describes the upper bound of the time complexity. For example:
     - \( O(1) \) for constant time
     - \( O(\log n) \) for logarithmic time
     - \( O(n) \) for linear time
     - \( O(n \log n) \) for linearithmic time
     - \( O(n^2) \) for quadratic time, etc.

### 8. **Simplify**
   - When expressing the final time complexity, drop lower-order terms and constant factors. For example, if you find that the time complexity is \( 3n^2 + 2n + 1 \), you would simplify it to \( O(n^2) \).

### Example
Consider the following code snippet:

```python
def example_function(arr):
    n = len(arr)
    for i in range(n):          # Loop 1
        for j in range(n):      # Loop 2
            print(arr[i] + arr[j])  # Constant time operation
```

1. **Input Size**: \( n \) (length of `arr`)
2. **Outer Loop**: Runs \( n \) times.
3. **Inner Loop**: Runs \( n \) times for each iteration of the outer loop.
4. **Total Operations**: \( n \times n = n^2 \).
5. **Time Complexity**: \( O(n^2) \).

By following these steps, you can systematically analyze and calculate the time complexity of various algorithms and code snippets.
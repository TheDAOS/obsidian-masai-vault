
### Example 1: Simple Loop
```python
def simple_loop(n):
    for i in range(n):
        print(i)
```
- **Input Size**: \( n \)
- **Loop**: Runs ( n ) times.
- **Time Complexity**: \( O(n) \)

### Example 2: Nested Loops
```python
def nested_loops(n):
    for i in range(n):
        for j in range(n):
            print(i, j)
```
- **Input Size**: \( n \)
- **Outer Loop**: Runs \( n \) times.
- **Inner Loop**: Runs \( n \) times for each iteration of the outer loop.
- **Total Operations**: \( n \times n = n^2 \)
- **Time Complexity**: \( O(n^2) \)

### Example 3: Loop with Constant Time Operation
```python
def constant_time_loop(n):
    for i in range(n):
        print("Hello")  # Constant time operation
```
- **Input Size**: \( n \)
- **Loop**: Runs \( n \) times.
- **Time Complexity**: ( O(n) )

### Example 4: Logarithmic Time
```python
def binary_search(arr, target):
    low, high = 0, len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    return -1
```
- **Input Size**: \( n \) (length of `arr`)
- **Loop**: Each iteration halves the search space.
- **Time Complexity**: \( O(\log n) \)

### Example 5: Recursive Function
```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)
```
- **Input Size**: \( n \)
- **Recursive Calls**: Makes \( n \) calls until it reaches 0.
- **Time Complexity**: \( O(n) \)

### Example 6: Multiple Operations
```python
def multiple_operations(n):
    for i in range(n):          # O(n)
        print(i)
    for j in range(n):          # O(n)
        print(j)
```
- **Input Size**: \( n \)
- **Total Operations**: \( n + n = 2n \)
- **Time Complexity**: \( O(n) \) (drop constant factor)

### Example 7: Combination of Loops
```python
def combination(n):
    for i in range(n):          # O(n)
        for j in range(i):      # O(i)
            print(i, j)
```
- **Input Size**: ( n )
- **Inner Loop**: Runs ( 0 + 1 + 2 + ... + (n-1) ) times, which is ( frac{n(n-1)}{2} ).
- **Time Complexity**: ( O(n^2) )

### Summary
- **Linear**: ( O(n) )
- **Quadratic**: ( O(n^2) )
- **Logarithmic**: ( O(log n) )
- **Constant**: ( O(1) )

Selection sort is a simple and intuitive comparison-based sorting algorithm. It works by dividing the input list into two parts: a sorted sublist of items which is built up from left to right at the front (left) of the list, and a sublist of the remaining unsorted items. The algorithm proceeds by finding the smallest (or largest, depending on sorting order) element in the unsorted sublist, exchanging (swapping) it with the leftmost unsorted element (putting it in sorted order), and moving the sublist boundaries one element to the right.

Selection sort is not the most efficient sorting algorithm for large datasets due to its quadratic time complexity. However, it is simple to implement and can be useful for small datasets or when memory writes are costly.

Here is a step-by-step explanation of how selection sort works:

1. **Initialize**: Start with the entire list as the unsorted sublist.
2. **Find the Minimum**: Find the smallest element in the unsorted sublist.
3. **Swap**: Swap this smallest element with the first unsorted element.
4. **Move Boundary**: Move the boundary of the sorted sublist one element to the right.
5. **Repeat**: Repeat steps 2-4 for the remaining unsorted sublist until the entire list is sorted.

## Pseudo code

```plaintext
procedure selectionSort(A: list of sortable items)
    n := length(A)
    for i from 0 to n - 1 do
        // Find the minimum element in the remaining unsorted list
        minIndex := i
        for j from i + 1 to n - 1 do
            if A[j] < A[minIndex] then
                minIndex := j
        // Swap the found minimum element with the first element of the unsorted list
        swap(A[i] with A[minIndex])
```

## Example

Let's sort the list `[64, 25, 12, 22, 11]` using selection sort:

1. **Initial List**: `[64, 25, 12, 22, 11]`
   - Find the minimum element (11) and swap it with the first element (64).
   - Result: `[11, 25, 12, 22, 64]`

2. **List after first pass**: `[11, 25, 12, 22, 64]`
   - Find the minimum element in the remaining list (12) and swap it with the second element (25).
   - Result: `[11, 12, 25, 22, 64]`

3. **List after second pass**: `[11, 12, 25, 22, 64]`
   - Find the minimum element in the remaining list (22) and swap it with the third element (25).
   - Result: `[11, 12, 22, 25, 64]`

4. **List after third pass**: `[11, 12, 22, 25, 64]`
   - The remaining list has only one element, so it is already sorted.

## Time Complexity

- **Best Case**: O(n^2)
- **Average Case**: O(n^2)
- **Worst Case**: O(n^2)

### JavaScript implementation

```javascript
function selectionSort(arr) {
    const n = arr.length;
    for (let i = 0; i < n; i++) {
        // Find the minimum element in the remaining unsorted list
        let minIndex = i;
        for (let j = i + 1; j < n; j++) {
            if (arr[j] < arr[minIndex]) {
                minIndex = j;
            }
        }
        // Swap the found minimum element with the first element of the unsorted list
        [arr[i], arr[minIndex]] = [arr[minIndex], arr[i]];
    }
    return arr;
}

// Example usage
const arr = [64, 25, 12, 22, 11];
const sortedArr = selectionSort(arr);
console.log("Sorted array is:", sortedArr);
```

##### Output
```
Sorted array is: [11, 12, 22, 25, 64]
```

##### Explanation
1. **Function Definition**: The `selectionSort` function takes an array `arr` as input.
2. **Outer Loop**: The outer loop runs from the first element to the last element of the array.
3. **Inner Loop**: The inner loop finds the minimum element in the remaining unsorted portion of the array.
4. **Swap**: The minimum element found is swapped with the first element of the unsorted portion.
5. **Return**: The sorted array is returned.

### Python Code Implementation

```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n):
        # Find the minimum element in the remaining unsorted list
        min_index = i
        for j in range(i + 1, n):
            if arr[j] < arr[min_index]:
                min_index = j
        # Swap the found minimum element with the first element of the unsorted list
        arr[i], arr[min_index] = arr[min_index], arr[i]

# Example usage
arr = [64, 25, 12, 22, 11]
selection_sort(arr)
print("Sorted array is:", arr)
```

##### Output
```
Sorted array is: [11, 12, 22, 25, 64]
```
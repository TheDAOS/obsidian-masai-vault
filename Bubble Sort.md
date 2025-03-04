Bubble sort is a simple comparison-based sorting algorithm. It works by repeatedly stepping through the list to be sorted, comparing each pair of adjacent items and swapping them if they are in the wrong order. The pass through the list is repeated until the list is sorted.

Bubble sort is not the most efficient sorting algorithm for large datasets due to its O(n^2) time complexity, but it is simple to understand and implement.

Here's a step-by-step explanation of how bubble sort works:

1. **Start at the beginning of the list**: Compare the first two items.
2. **If the first item is greater than the second item, swap them**: This moves the larger item towards the end of the list.
3. **Move to the next pair of items**: Compare the second and third items, and swap them if necessary.
4. **Continue this process**: Move through the list, comparing and swapping adjacent items as needed.
5. **Repeat the entire process**: After one full pass through the list, the largest item will have "bubbled up" to the end. Repeat the process for the remaining items until the list is sorted.

### Example

Let's sort the list `[5, 3, 8, 4, 2]` using bubble sort:

1. **First pass**:
   - Compare 5 and 3: Swap to get `[3, 5, 8, 4, 2]`.
   - Compare 5 and 8: No swap needed.
   - Compare 8 and 4: Swap to get `[3, 5, 4, 8, 2]`.
   - Compare 8 and 2: Swap to get `[3, 5, 4, 2, 8]`.

2. **Second pass**:
   - Compare 3 and 5: No swap needed.
   - Compare 5 and 4: Swap to get `[3, 4, 5, 2, 8]`.
   - Compare 5 and 2: Swap to get `[3, 4, 2, 5, 8]`.
   - Compare 5 and 8: No swap needed.

3. **Third pass**:
   - Compare 3 and 4: No swap needed.
   - Compare 4 and 2: Swap to get `[3, 2, 4, 5, 8]`.
   - Compare 4 and 5: No swap needed.
   - Compare 5 and 8: No swap needed.

4. **Fourth pass**:
   - Compare 3 and 2: Swap to get `[2, 3, 4, 5, 8]`.
   - Compare 3 and 4: No swap needed.
   - Compare 4 and 5: No swap needed.
   - Compare 5 and 8: No swap needed.

At this point, the list is sorted, and no more swaps are needed.

### Pseudocode
```
procedure bubbleSort(A: list of sortable items)
    n := length(A)
    repeat
        swapped := false
        for i := 1 to n-1 inclusive do
            if A[i-1] > A[i] then
                swap(A[i-1], A[i])
                swapped := true
            end if
        end for
        n := n - 1
    until not swapped
end procedure
```

### JavaScript implementation

```javascript
function bubbleSort(arr) {
    let n = arr.length;
    for (let i = 0; i < n; i++) {
        // Track if any swaps were made in this pass
        let swapped = false;
        for (let j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                // Swap the elements
                let temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
                swapped = true;
            }
        }
        // If no swaps were made, the list is already sorted
        if (!swapped) {
            break;
        }
    }
    return arr;
}

// Example usage
let arr = [5, 3, 8, 4, 2];
let sortedArr = bubbleSort(arr);
console.log("Sorted array is:", sortedArr);
```

#### Explanation

1. **Outer Loop**: The outer loop runs `n` times, where `n` is the length of the array. This ensures that we make multiple passes through the array.
2. **Inner Loop**: The inner loop runs from the start of the array to `n - i - 1`. This is because after each pass, the largest element in the unsorted portion of the array is moved to its correct position, so we don't need to check it again.
3. **Swapping**: If the current element is greater than the next element, they are swapped.
4. **Optimization**: The `swapped` flag is used to optimize the algorithm. If no swaps are made in a pass, the array is already sorted, and we can break out of the loop early.

### Python Implementation

Here is a Python implementation of bubble sort:

```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        # Track if any swaps were made in this pass
        swapped = False
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                # Swap the elements
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swapped = True
        # If no swaps were made, the list is already sorted
        if not swapped:
            break
    return arr

# Example usage
arr = [5, 3, 8, 4, 2]
sorted_arr = bubble_sort(arr)
print("Sorted array is:", sorted_arr)
```
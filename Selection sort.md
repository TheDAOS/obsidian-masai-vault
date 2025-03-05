Selection sort is a simple and intuitive comparison-based sorting algorithm. It works by dividing the input list into two parts: a sorted sublist of items which is built up from left to right at the front (left) of the list, and a sublist of the remaining unsorted items. The algorithm proceeds by finding the smallest (or largest, depending on sorting order) element in the unsorted sublist, exchanging (swapping) it with the leftmost unsorted element (putting it in sorted order), and moving the sublist boundaries one element to the right.

Selection sort is not the most efficient sorting algorithm for large datasets due to its quadratic time complexity. However, it is simple to implement and can be useful for small datasets or when memory writes are costly.

Here is a step-by-step explanation of how selection sort works:

1. **Initialize**: Start with the entire list as the unsorted sublist.
2. **Find the Minimum**: Find the smallest element in the unsorted sublist.
3. **Swap**: Swap this smallest element with the first unsorted element.
4. **Move Boundary**: Move the boundary of the sorted sublist one element to the right.
5. **Repeat**: Repeat steps 2-4 for the remaining unsorted sublist until the entire list is sorted.

## Pseudocode

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

## Python Code Implementation

### Initial List
`[64, 25, 12, 22, 11]`

### Pass 1
- **Find the minimum element in the entire list**: The minimum element is `11`.
- **Swap it with the first element**: Swap `11` with `64`.
- **Resulting list**: `[11, 25, 12, 22, 64]`

### Pass 2
- **Find the minimum element in the sublist `[25, 12, 22, 64]`**: The minimum element is `12`.
- **Swap it with the second element**: Swap `12` with `25`.
- **Resulting list**: `[11, 12, 25, 22, 64]`

### Pass 3
- **Find the minimum element in the sublist `[25, 22, 64]`**: The minimum element is `22`.
- **Swap it with the third element**: Swap `22` with `25`.
- **Resulting list**: `[11, 12, 22, 25, 64]`

### Pass 4
- **Find the minimum element in the sublist `[25, 64]`**: The minimum element is `25`.
- **Swap it with the fourth element**: Swap `25` with `25` (no change needed).
- **Resulting list**: `[11, 12, 22, 25, 64]`

### Pass 5
- The list is already sorted, so no further swaps are needed.

### Final Sorted List
`[11, 12, 22, 25, 64]`

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

### Output
```
Sorted array is: [11, 12, 22, 25, 64]
```

This code will sort the list `[64, 25, 12, 22, 11]` using the selection sort algorithm and print the sorted list.
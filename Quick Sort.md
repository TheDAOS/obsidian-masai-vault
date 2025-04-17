
### Pusdo Code:

```
Algorithm quickSort(arr, low, high)
    // Check if low is less than high to continue sorting
    if low < high then
        // Partition the array and get pivot index
        pivotIndex := partition(arr, low, high)
		
        // Recur for left and right sub-arrays
        quickSort(arr, low, pivotIndex - 1)
        quickSort(arr, pivotIndex + 1, high)

Algorithm partition(arr, low, high)
    // Choose the pivot (can be any element, here choosing the last element)
    pivot := arr[high]
    i := low - 1  // Index of smaller element
	
    // Traverse the array
    for j := low to high - 1
        // If current element is smaller than or equal to pivot
        if arr[j] <= pivot then
            // Increment index of smaller element and swap
            i := i + 1
            swap arr[i] with arr[j]
	
    // Place the pivot element at its correct position
    swap arr[i + 1] with arr[high]
    return i + 1

// Function to swap two elements in an array
Algorithm swap(arr, i, j)
    temp := arr[i]
    arr[i] := arr[j]
    arr[j] := temp
```
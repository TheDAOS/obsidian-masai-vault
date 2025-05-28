## Pseudo code

```Pseudocode
merge(arr, l, m, r)
    n1 = m - l + 1
    n2 = r - m
	
    // Create temporary arrays
    Left[1...n1], Right[1...n2]
	
    // Copy data to temporary arrays Left[] and Right[]
    for i = 1 to n1
        Left[i] = arr[l + i - 1]
    for j = 1 to n2
        Right[j] = arr[m + j]
	
    // Merge the temporary arrays back into arr[l...r]
    i = 1 // Initial index of first subarray
    j = 1 // Initial index of second subarray
    k = l // Initial index of merged subarray
    while i <= n1 and j <= n2
        if Left[i] <= Right[j]
            arr[k] = Left[i]
            i = i + 1
        else
            arr[k] = Right[j]
            j = j + 1
        k = k + 1
	
    // Copy the remaining elements of Left[], if any
    while i <= n1
        arr[k] = Left[i]
        i = i + 1
        k = k + 1
	
    // Copy the remaining elements of Right[], if any
    while j <= n2
        arr[k] = Right[j]
        j = j + 1
        k = k + 1
```
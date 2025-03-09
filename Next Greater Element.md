The "Next Greater Element" for an element in the array is the first element to the right of it that is greater than the current element. If there is no such element, the next greater element is `-1`.

### Step 1: Understand the Problem
- **Input**: An array of integers.
- **Output**: An array where each element is the next greater element for the corresponding element in the input array.

### Step 2: Choose an Approach
We can use a stack to efficiently find the next greater element for each element in the array. This approach ensures that we only traverse the array once, making it O(n) in time complexity.

### Step 3: Implement the Solution
```javascript
function nextGreaterElement(nums) {
    const result = new Array(nums.length).fill(-1);
    const stack = [];

    for (let i = 0; i < nums.length; i++) {
        // Maintain a stack of indices
        while (stack.length > 0 && nums[i] > nums[stack[stack.length - 1]]) {
            const index = stack.pop();
            result[index] = nums[i];
        }
        stack.push(i);
    }

    return result;
}

// Example usage:
const nums = [1, 3, 2, 4];
const nextGreaterElements = nextGreaterElement(nums);
console.log(nextGreaterElements); // Output: [3, 4, 4, -1]
```

### Step 4: Explanation of the Code
1. **Initialization**:
   - `result`: An array initialized with `-1` values, which will store the next greater elements.
   - `stack`: An empty stack to keep track of indices.

2. **Iterate through the array**:
   - For each element in the array, check if the current element is greater than the element at the index stored at the top of the stack.
   - If it is, pop the index from the stack and update the `result` array at that index with the current element.
   - Push the current index onto the stack.

3. **Return the result**:
   - After processing all elements, the `result` array will contain the next greater elements for each element in the input array.

### Step 5: Test the Solution
Test the function with various inputs to ensure it works correctly.

```javascript
console.log(nextGreaterElement([1, 3, 2, 4])); // Output: [3, 4, 4, -1]
console.log(nextGreaterElement([4, 3, 2, 1])); // Output: [-1, -1, -1, -1]
console.log(nextGreaterElement([1, 2, 3, 4])); // Output: [2, 3, 4, -1]
console.log(nextGreaterElement([4, 1, 2]));    // Output: [-1, 2, -1]
```
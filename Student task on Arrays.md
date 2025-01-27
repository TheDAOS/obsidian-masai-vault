## Overall task on arrays
[[Array task]]
Here are the questions and solutions using only `for` loops, avoiding `for...of`:
***
## 1. Print Even Numbers

**Question:**
Create an array of numbers `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`. Write a function to loop through the array and print only the even numbers.

**Solution:**
```js
function printEvenNumbers(arr) {
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] % 2 === 0) {
            console.log(arr[i]);
        }
    }
}

let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
printEvenNumbers(numbers);
// Output: 2, 4, 6, 8, 10
```

***
## 2. Find the Largest Number

**Question:**
Create an array of numbers `[10, 25, 36, 45, 90, 56]`. Write a function to loop through the array and find the largest number.

**Solution:**
```js
function findLargest(arr) {
    let largest = arr[0];
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] > largest) {
            largest = arr[i];
        }
    }
    return largest;
}

let numbers = [10, 25, 36, 45, 90, 56];
console.log(findLargest(numbers));
// Output: 90
```

***
## 3. Reverse an Array

**Question:**
Write a function to reverse the array `[1, 2, 3, 4, 5]` using a loop, and print the reversed array.

**Solution:**
```js
function reverseArray(arr) {
    let reversed = [];
    for (let i = arr.length - 1; i >= 0; i--) {
        reversed.push(arr[i]);
    }
    return reversed;
}

let numbers = [1, 2, 3, 4, 5];
console.log(reverseArray(numbers));
// Output: [5, 4, 3, 2, 1]
```

***
## 4. Count Occurrences of an Element

**Question:**
Create an array `[1, 2, 3, 4, 3, 2, 1, 3]`. Write a function to count how many times the number `3` appears in the array.

**Solution:**
```js
function countOccurrences(arr, target) {
    let count = 0;
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] === target) {
            count++;
        }
    }
    return count;
}

let numbers = [1, 2, 3, 4, 3, 2, 1, 3];
console.log(`3 appears ${countOccurrences(numbers, 3)} times`);
// Output: 3 appears 3 times
```

***
#### 5. Sum All Elements

**Question:**
Write a function to calculate the sum of all elements in the array `[10, 20, 30, 40]` using a loop.

**Solution:**
```js
function sumArray(arr) {
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }
    return sum;
}

let numbers = [10, 20, 30, 40];
console.log(sumArray(numbers));
// Output: 100
```

***
## 6. Find the Index of an Element

**Question:**
Create an array `["apple", "banana", "cherry", "date"]`. Write a function to find and print the index of the element `"cherry"`.

**Solution:**
```js
function findIndex(arr, target) {
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] === target) {
            return i;
        }
    }
    return -1; // If not found
}

let fruits = ["apple", "banana", "cherry", "date"];
console.log(`Index of cherry: ${findIndex(fruits, "cherry")}`);
// Output: Index of cherry: 2
```

***

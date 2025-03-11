
JavaScript provides a variety of methods to manipulate and interact with arrays. Here are some of the most commonly used array methods:

1. **`push()`**
   - Adds one or more elements to the end of an array and returns the new length of the array.
   ```javascript
   let fruits = ['apple', 'banana'];
   fruits.push('orange');
   console.log(fruits); // ['apple', 'banana', 'orange']
   ```

2. **`pop()`**
   - Removes the last element from an array and returns that element.
   ```javascript
   let fruits = ['apple', 'banana', 'orange'];
   let lastFruit = fruits.pop();
   console.log(lastFruit); // 'orange'
   console.log(fruits); // ['apple', 'banana']
   ```

3. **`shift()`**
   - Removes the first element from an array and returns that element.
   ```javascript
   let fruits = ['apple', 'banana', 'orange'];
   let firstFruit = fruits.shift();
   console.log(firstFruit); // 'apple'
   console.log(fruits); // ['banana', 'orange']
   ```

4. **`unshift()`**
   - Adds one or more elements to the beginning of an array and returns the new length of the array.
   ```javascript
   let fruits = ['banana', 'orange'];
   fruits.unshift('apple');
   console.log(fruits); // ['apple', 'banana', 'orange']
   ```

5. **`map()`**
   - Creates a new array with the results of calling a provided function on every element in the calling array.
   ```javascript
   let numbers = [1, 2, 3, 4];
   let doubled = numbers.map(num => num * 2);
   console.log(doubled); // [2, 4, 6, 8]
   ```

6. **`filter()`**
   - Creates a new array with all elements that pass the test implemented by the provided function.
   ```javascript
   let numbers = [1, 2, 3, 4];
   let evens = numbers.filter(num => num % 2 === 0);
   console.log(evens); // [2, 4]
   ```

7. **`reduce()`**
   - Executes a reducer function (that you provide) on each element of the array, resulting in a single output value.
   ```javascript
   let numbers = [1, 2, 3, 4];
   let sum = numbers.reduce((acc, num) => acc + num, 0);
   console.log(sum); // 10
   ```

8. **`forEach()`**
   - Executes a provided function once for each array element.
   ```javascript
   let fruits = ['apple', 'banana', 'orange'];
   fruits.forEach(fruit => console.log(fruit));
   // 'apple'
   // 'banana'
   // 'orange'
   ```

9. **`find()`**
   - Returns the value of the first element in the array that satisfies the provided testing function.
   ```javascript
   let numbers = [1, 2, 3, 4];
   let found = numbers.find(num => num > 2);
   console.log(found); // 3
   ```

10. **`findIndex()`**
    - Returns the index of the first element in the array that satisfies the provided testing function.
    ```javascript
    let numbers = [1, 2, 3, 4];
    let index = numbers.findIndex(num => num > 2);
    console.log(index); // 2
    ```

11. **`includes()`**
    - Determines whether an array includes a certain value among its entries, returning `true` or `false` as appropriate.
    ```javascript
    let fruits = ['apple', 'banana', 'orange'];
    let hasBanana = fruits.includes('banana');
    console.log(hasBanana); // true
    ```

12. **`slice()`**
    - Returns a shallow copy of a portion of an array into a new array object selected from start to end (end not included) where start and end represent the index of items in that array. The original array will not be modified.
    ```javascript
    let fruits = ['apple', 'banana', 'orange', 'mango'];
    let citrus = fruits.slice(1, 3);
    console.log(citrus); // ['banana', 'orange']
    ```

13. **`splice()`**
    - Changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.
    ```javascript
    let fruits = ['apple', 'banana', 'orange', 'mango'];
    fruits.splice(1, 2, 'grape', 'kiwi');
    console.log(fruits); // ['apple', 'grape', 'kiwi', 'mango']
    ```

14. **`concat()`**
    - Merges two or more arrays. This method does not change the existing arrays, but instead returns a new array.
    ```javascript
    let array1 = [1, 2, 3];
    let array2 = [4, 5, 6];
    let mergedArray = array1.concat(array2);
    console.log(mergedArray); // [1, 2, 3, 4, 5, 6]
    ```

15. **`join()`**
    - Joins all elements of an array into a string and returns this string. You can specify a separator string to separate each element of the array.
    ```javascript
    let fruits = ['apple', 'banana', 'orange'];
    let fruitString = fruits.join(', ');
    console.log(fruitString); // 'apple, banana, orange'
    ```

16. **`reverse()`**
    - Reverses an array in place. The first array element becomes the last, and the last array element becomes the first.
    ```javascript
    let numbers = [1, 2, 3, 4];
    numbers.reverse();
    console.log(numbers); // [4, 3, 2, 1]
    ```

17. **`sort()`**
    - Sorts the elements of an array in place and returns the sorted array. The sort is not necessarily stable. The default sort order is according to string Unicode code points.
    ```javascript
    let numbers = [4, 2, 5, 1, 3];
    numbers.sort((a, b) => a - b);
    console.log(numbers); // [1, 2, 3, 4, 5]
    ```

18. **`every()`**
    - Tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.
    ```javascript
    let numbers = [1, 2, 3, 4];
    let allPositive = numbers.every(num => num > 0);
    console.log(allPositive); // true
    ```

19. **`some()`**
    - Tests whether at least one element in the array passes the test implemented by the provided function. It returns a Boolean value.
    ```javascript
    let numbers = [1, 2, 3, 4];
    let hasEven = numbers.some(num => num % 2 === 0);
    console.log(hasEven); // true
    ```

20. **`flat()`**
    - Creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.
    ```javascript
    let nestedArray = [1, [2, [3, 4], 5]];
    let flattenedArray = nestedArray.flat(2);
    console.log(flattenedArray); // [1, 2, 3, 4, 5]
    ```

21. **`flatMap()`**
    - First maps each element using a mapping function, then flattens the result into a new array. It is identical to a `map` followed by a `flat` of depth 1.
    ```javascript
    let numbers = [1, 2, 3, 4];
    let doubledAndFlattened = numbers.flatMap(num => [num * 2]);
    console.log(doubledAndFlattened); // [2, 4, 6, 8]
    ```
### Computing Frequency of Characters Using Objects
Another common use case is calculating the frequency of characters in a string using an object. Each character will be the key in the object, and the value will represent how many times that character appears in the string.

## Example 2: Character Frequency Calculation

##### Code Example:
```js
function getCharacterFrequency(str) {
  let frequency = {};

  for (let i = 0; i < str.length; i++) {
    let char = str[i];
    if (frequency[char] !== undefined) {
  // If the character already exists in the object, increment its count
  frequency[char] = frequency[char] + 1;
} else {
  // If the character does not exist, set its count to 1
  frequency[char] = 1;
}

  }

  return frequency;
}

console.log(getCharacterFrequency("abbccc"));
// Output: {a: 1, b: 2, c: 3}
```

```js
function getCharacterFrequency(str) {
  let frequency = {}; // Initialize an empty object

  for (let i = 0; i < str.length; i++) {
    let char = str[i]; // Get the current character

    // Check if the character already exists in the object
    if (frequency[char]) {
      frequency[char]++; // Increment the count if it exists
    } else {
      frequency[char] = 1; // Add it to the object with a count of 1
    }
  }

  return frequency; // Return the object with frequencies
}

console.log(getCharacterFrequency("abbccc"));
// Output: {a: 1, b: 2, c: 3}
```

##### Explanation:
- We loop through the string and check if the character already exists in the object.
- If it exists, we increment the frequency count; otherwise, we set it to `1` for new characters.
Here’s the code broken into multiple **small steps** for better understanding:
***

### Code with Small Steps:
```js
// Step 1: Define the input string
let str = "hello";

// Step 2: Create an empty object to store frequencies
let frequency = {};

// Step 3: Start a loop to process each character in the string
for (let i = 0; i < str.length; i++) {
  // Step 4: Get the current character from the string
  let char = str[i];

  // Step 5: Check if the character is already in the object
  if (frequency[char]) {
    // Step 6: If it exists, increment its count by 1
    frequency[char]++;
  } else {
    // Step 7: If it doesn't exist, add it to the object with an initial count of 1
    frequency[char] = 1;
  }
}

// Step 8: Output the final frequency object
console.log(frequency);
```

### What Happens at Each Step:

##### Input:
```js
"hello"
```

#### Step-by-Step Execution:

1. **Step 1:** Define the input string:
	```js
	let str = "hello";
	```

2. **Step 2:** Create an empty object to store the frequencies:
	```js
	let frequency = {};
	```

3. **Step 3:** Start the loop to process each character:
	```js
	for (let i = 0; i < str.length; i++) {
	```

4. **Step 4:** Get the current character:
	```js
	let char = str[i];
	```

5. **Step 5:** Check if the character exists in the frequency object:
```js
if (frequency[char]) {
```

1. **Step 6:** If it exists, increment the count:
	```js
	frequency[char]++;
	```

```js
function firstNonRepeatingCharacter(str) {
  let frequency = {}; // Object to store character frequency

  // Step 1: Count the frequency of each character
  for (let char of str) {
    if (frequency[char]) {
      frequency[char]++; // Increment the count if character already exists
    } else {
      frequency[char] = 1; // Initialize the count for new characters
    }
  }

  // Step 2: Find the first character with a frequency of 1
  for (let char of str) {
    if (frequency[char] === 1) {
      return char; // Return the first non-repeating character
    }
  }

  return null; // Return null if no non-repeating character is found
}

// Test the function
console.log(firstNonRepeatingCharacter("swiss")); // Output: "w"
console.log(firstNonRepeatingCharacter("aabbcc")); // Output: null
console.log(firstNonRepeatingCharacter("javascript")); // Output: "j"
```

## Explanation

### Step 1: Count Character Frequencies
- Use an object to count how many times each character appears in the string.
- Example:
	```js
	Input: "swiss"
	Frequency Object: { s: 3, w: 1, i: 1 }
	```

### Step 2: Check Frequency
- Loop through the string again, in the same order, to check the frequency of each character.
- The first character with a frequency of `1` is returned as the result.

### Step 3: Return `null` if None Found
- If no character has a frequency of `1`, return `null`.

***

## Output Walkthrough

### Input: `"swiss"`
1. **Frequency Object:**
	```js
	{ s: 3, w: 1, i: 1 }
	```

2. Loop through the string:
	- `'s'` → Frequency is `3`.
	- `'w'` → Frequency is `1`. **Return `'w'`**.

### Input: `"aabbcc"`
1. **Frequency Object:**
	```js
	{ a: 2, b: 2, c: 2 }
	```

2. Loop through the string:
	- All characters have a frequency greater than `1`. **Return `null`**.

### Input: `"javascript"`
1. **Frequency Object:**
	```js
	{ j: 1, a: 2, v: 1, s: 1, c: 1, r: 1, i: 1, p: 1, t: 1 }
	```

2. Loop through the string:
	- `'j'` → Frequency is `1`. **Return `'j'`**.

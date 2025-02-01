Once we have the character frequencies stored in an object, we can use the `for...in` loop to traverse through the object and output the frequencies.

```js
// Step 1: Input string
let str = "hello";

// Step 2: Create an empty object to store frequencies
let frequency = {};

// Step 3: Calculate frequencies
for (let i = 0; i < str.length; i++) {
  let char = str[i];
  if (frequency[char]) {
    frequency[char]++;
  } else {
    frequency[char] = 1;
  }
}

// Step 4: Traverse the frequency object
console.log("Character Frequencies:");
for (let char in frequency) {
  console.log(`Character '${char}': ${frequency[char]}`);
}
```

## Example: Traversing the Frequency Object

### Code Example:
```js
let frequency = getCharacterFrequency("abbccc");

for (let char in frequency) {
  console.log(char + " appears " + frequency[char] + " times.");
}

// Output:
// a appears 1 times.
// b appears 2 times.
// c appears 3 times.
```

##### Explanation:
- The `for...in` loop is used to traverse the `frequency` object.
- It prints each character along with the number of times it appears in the string.

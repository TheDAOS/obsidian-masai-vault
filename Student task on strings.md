Here are **10 questions** on strings along with their solutions, focusing on various string operations in JavaScript:
***
## 1. Find the Length of a String

##### Question:
Write a function that takes a string as input and returns its length.

##### Solution:
```js
function stringLength(str) {
    return str.length;
}

console.log(stringLength("Hello, World!")); // Output: 13
```
***
## 2. Convert a String to Uppercase

##### Question:
Write a function that converts a given string to uppercase.

##### Solution:
```js
function toUpperCase(str) {
    return str.toUpperCase();
}

console.log(toUpperCase("hello")); // Output: "HELLO"
```

***
## 3. Reverse a String

##### Question:
Write a function that takes a string and returns its reverse.

##### Solution:
```js
function reverseString(str) {
    let reversed = "";
    for (let i = str.length - 1; i >= 0; i--) {
        reversed += str[i];
    }
    return reversed;
}

console.log(reverseString("hello")); // Output: "olleh"
```
***
## 4. Count Vowels in a String

##### Question:
Write a function to count the number of vowels (`a, e, i, o, u`) in a string.

##### Solution:
```js
function countVowels(str) {
    let count = 0;
    let vowels = "aeiouAEIOU";
    for (let i = 0; i < str.length; i++) {
        if (vowels.includes(str[i])) {
            count++;
        }
    }
    return count;
}

console.log(countVowels("hello world")); // Output: 3
```
***

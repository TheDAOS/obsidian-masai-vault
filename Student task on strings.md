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
## 5. Check if a String is a Palindrome

##### Question:
Write a function that checks if a string is a palindrome (reads the same forward and backward).

##### Solution:
```js
function isPalindrome(str) {
    let reversed = "";
    for (let i = str.length - 1; i >= 0; i--) {
        reversed += str[i];
    }
    return str === reversed;
}

console.log(isPalindrome("madam")); // Output: true
console.log(isPalindrome("hello")); // Output: false
```
***
## 6. Find the First Non-Repeating Character

##### Question:
Write a function that returns the first non-repeating character in a string. If all characters repeat, return `null`.

##### Solution:
```js
function firstNonRepeatingChar(str) {
    for (let i = 0; i < str.length; i++) {
        if (str.indexOf(str[i]) === str.lastIndexOf(str[i])) {
            return str[i];
        }
    }
    return null;
}

console.log(firstNonRepeatingChar("swiss")); // Output: "w"
console.log(firstNonRepeatingChar("aabb"));  // Output: null
```
***
## 7. Count Occurrences of a Character

##### Question:
Write a function that counts how many times a specific character appears in a string.

##### Solution:
```js
function countCharacter(str, char) {
    let count = 0;
    for (let i = 0; i < str.length; i++) {
        if (str[i] === char) {
            count++;
        }
    }
    return count;
}

console.log(countCharacter("hello world", "o")); // Output: 2
```
***
## 8. Extract a Substring

##### Question:
Write a function that extracts a substring from a given string. The function should take the starting index and length of the substring as parameters.

##### Solution:
```js
function extractSubstring(str, start, length) {
    let result = "";
    for (let i = start; i < start + length && i < str.length; i++) {
        result += str[i];
    }
    return result;
}

console.log(extractSubstring("hello world", 0, 5)); // Output: "hello"
```
***
## 9. Replace All Occurrences of a Character

##### Question:
Write a function that replaces all occurrences of a specific character in a string with another character.

##### Solution:
```js
function replaceCharacter(str, oldChar, newChar) {
    let result = "";
    for (let i = 0; i < str.length; i++) {
        if (str[i] === oldChar) {
            result += newChar;
        } else {
            result += str[i];
        }
    }
    return result;
}

console.log(replaceCharacter("banana", "a", "o")); // Output: "bonono"
```
***
## 10. Check if a String Contains a Substring

##### Question:
Write a function that checks if a given substring is present in a string.

##### Solution:
```js
function containsSubstring(str, substring) {
    for (let i = 0; i <= str.length - substring.length; i++) {
        if (str.slice(i, i + substring.length) === substring) {
            return true;
        }
    }
    return false;
}

console.log(containsSubstring("hello world", "world")); // Output: true
console.log(containsSubstring("hello world", "earth")); // Output: false
```
***
These questions and solutions cover various string operations, from basic manipulations to problem-solving techniques, using loops and string methods. Let me know if you need more challenges or explanations!
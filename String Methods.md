JavaScript provides a variety of methods to manipulate and work with strings. Here are some of the most commonly used string methods:

### 1. `charAt(index)`
   - **Description**: Returns the character at the specified index.
   - **Example**:
	 ```javascript
	 let str = "Hello, World!";
	 console.log(str.charAt(0)); // Output: "H"
	 ```

### 2. `charCodeAt(index)`
   - **Description**: Returns the Unicode of the character at the specified index.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.charCodeAt(0)); // Output: 72
     ```

### 3. `concat(str1, str2, ..., strN)`
   - **Description**: Combines the text of two or more strings and returns a new string.
   - **Example**:
     ```javascript
     let str1 = "Hello";
     let str2 = "World";
     console.log(str1.concat(", ", str2)); // Output: "Hello, World"
     ```

### 4. `endsWith(searchString, [position])`
   - **Description**: Checks if a string ends with the specified characters.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.endsWith("World!")); // Output: true
     ```

### 5. `includes(searchString, [position])`
   - **Description**: Checks if a string contains the specified characters.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.includes("World")); // Output: true
     ```

### 6. `indexOf(searchString, [fromIndex])`
   - **Description**: Returns the index of the first occurrence of a specified value in a string.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.indexOf("World")); // Output: 7
     ```

### 7. `lastIndexOf(searchString, [fromIndex])`
   - **Description**: Returns the index of the last occurrence of a specified value in a string.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.lastIndexOf("o")); // Output: 8
     ```

### 8. `match(regexp)`
   - **Description**: Searches a string for a match against a regular expression.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.match(/World/)); // Output: ["World"]
     ```

### 9. `replace(searchValue, newValue)`
- **Description**: Searches a string for a specified value, or a regular expression, and returns a new string with the specified value(s) replaced.
- **Example**:
	```javascript
	let str = "Hello, World!";
	console.log(str.replace("World", "JavaScript")); // Output: "Hello, JavaScript!"
	```

### 10. `search(regexp)`
- **Description**: Searches a string for a specified value, or regular expression, and returns the position of the match.
- **Example**:
  ```javascript
  let str = "Hello, World!";
  console.log(str.search("World")); // Output: 7
  ```

### 11. `slice(start, end)`
- **Description**: Extracts a section of a string and returns it as a new string.
- **Example**:
  ```javascript
  let str = "Hello, World!";
  console.log(str.slice(0, 5)); // Output: "Hello"
  ```

### 12. `split(separator, limit)`
- **Description**: Splits a string into an array of substrings.
- **Example**:
  ```javascript
  let str = "Hello, World!";
  console.log(str.split(",")); // Output: ["Hello", " World!"]
  ```

### 13. `startsWith(searchString, [position])`
- **Description**: Checks if a string starts with the specified characters.
- **Example**:
	```javascript
	let str = "Hello, World!";
	console.log(str.startsWith("Hello")); // Output: true
	```

### 14. `substr(start, length)`
- **Description**: Returns a part of the string between the start index and a number of characters afterward.
- **Example**:
	```javascript
	  let str = "Hello, World!";
	  console.log(str.substr(0, 5));
	```

### 15. `substring(start, end)`
- **Description**: Returns a part of the string between the start and end indexes, or to the end of the string.
- **Example**:
	```javascript
	let str = "Hello, World!";
	console.log(str.substring(0, 5)); // Output: "Hello"
	```

### 16. `toLowerCase()`
   - **Description**: Converts a string to lowercase letters.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.toLowerCase()); // Output: "hello, world!"
     ```

### 17. `toUpperCase()`
   - **Description**: Converts a string to uppercase letters.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.toUpperCase()); // Output: "HELLO, WORLD!"
     ```

### 18. `trim()`
   - **Description**: Removes whitespace from both ends of a string.
   - **Example**:
     ```javascript
     let str = "   Hello, World!   ";
     console.log(str.trim()); // Output: "Hello, World!"
     ```

### 19. `trimStart()`
   - **Description**: Removes whitespace from the beginning of a string.
   - **Example**:
     ```javascript
     let str = "   Hello, World!";
     console.log(str.trimStart()); // Output: "Hello, World!"
     ```

### 20. `trimEnd()`
   - **Description**: Removes whitespace from the end of a string.
   - **Example**:
     ```javascript
     let str = "Hello, World!   ";
     console.log(str.trimEnd()); // Output: "Hello, World!"
     ```

### 21. `repeat(count)`
   - **Description**: Repeats a string a specified number of times.
   - **Example**:
     ```javascript
     let str = "Hello";
     console.log(str.repeat(3)); // Output: "HelloHelloHello"
     ```

### 22. `padStart(targetLength, padString)`
   - **Description**: Pads the current string with another string (repeated, if needed) so that the resulting string reaches a given length.
   - **Example**:
     ```javascript
     let str = "5";
     console.log(str.padStart(4, '0')); // Output: "0005"
     ```

### 23. `padEnd(targetLength, padString)`
   - **Description**: Pads the current string with another string (repeated, if needed) so that the resulting string reaches a given length.
   - **Example**:
     ```javascript
     let str = "5";
     console.log(str.padEnd(4, '0')); // Output: "5000"
     ```

### 24. `split(separator, limit)`
   - **Description**: Splits a string into an array of substrings.
   - **Example**:
     ```javascript
     let str = "a,b,c,d";
     console.log(str.split(",")); // Output: ["a", "b", "c", "d"]
     ```

### 25. `valueOf()`
   - **Description**: Returns the primitive value of a String object.
   - **Example**:
     ```javascript
     let str = new String("Hello, World!");
     console.log(str.valueOf()); // Output: "Hello, World!"
     ```

### 26. `localeCompare(compareString)`
   - **Description**: Compares two strings in the current locale.
   - **Example**:
     ```javascript
     let str1 = "Hello";
     let str2 = "World";
     console.log(str1.localeCompare(str2)); // Output: -1 (str1 is less than str2)
     ```

### 27. `normalize([form])`
   - **Description**: Returns the Unicode Normalization Form of a given string.
   - **Example**:
     ```javascript
     let str = "Café";
     console.log(str.normalize()); // Output: "Café"
     ```

### 28. `anchor(name)`
   - **Description**: Creates an HTML anchor element.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.anchor("link")); // Output: "<a name='link'>Hello, World!</a>"
     ```
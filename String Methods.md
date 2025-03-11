JavaScript provides a variety of methods to manipulate and work with strings. Here are some of the most commonly used string methods:

#### 1. **`charAt(index)`**
   - **Description**: Returns the character at the specified index.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.charAt(0)); // Output: "H"
     ```

#### 2. **`charCodeAt(index)`**
   - **Description**: Returns the Unicode of the character at the specified index.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.charCodeAt(0)); // Output: 72
     ```

#### 3. **`concat(str1, str2, ..., strN)`**
   - **Description**: Combines the text of two or more strings and returns a new string.
   - **Example**:
     ```javascript
     let str1 = "Hello";
     let str2 = "World";
     console.log(str1.concat(", ", str2)); // Output: "Hello, World"
     ```

#### 4. **`endsWith(searchString, [position])`**
   - **Description**: Checks if a string ends with the specified characters.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.endsWith("World!")); // Output: true
     ```

#### 5. **`includes(searchString, [position])`**
   - **Description**: Checks if a string contains the specified characters.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.includes("World")); // Output: true
     ```

#### 6. **`indexOf(searchString, [fromIndex])`**
   - **Description**: Returns the index of the first occurrence of a specified value in a string.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.indexOf("World")); // Output: 7
     ```

#### 7. **`lastIndexOf(searchString, [fromIndex])`**
   - **Description**: Returns the index of the last occurrence of a specified value in a string.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.lastIndexOf("o")); // Output: 8
     ```

#### 8. **`match(regexp)`**
   - **Description**: Searches a string for a match against a regular expression.
   - **Example**:
     ```javascript
     let str = "Hello, World!";
     console.log(str.match(/World/)); // Output: ["World"]
     ```

#### 9. **`replace(searchValue, newValue)`**
- **Description**: Searches a string for a specified value, or a regular expression, and returns a new string with the specified value(s) replaced.
- **Example**:
```javascript
let str = "Hello, World!";
console.log(str.replace("World", "JavaScript")); // Output: "Hello, JavaScript!"
```

#### 10. `search(regexp)`

- **Description**: Searches a string for a specified value, or regular expression, and returns the position of the match.
- **Example**:
  ```javascript
  let str = "Hello, World!";
  console.log(str.search("World")); // Output: 7
  ```

#### 11. **`slice(start, end)`**
    - **Description**: Extracts a section of a string and returns it as a new string.
    - **Example**:
      ```javascript
      let str = "Hello, World!";
      console.log(str.slice(0, 5)); // Output: "Hello"
      ```

#### 12. **`split(separator, limit)`**
    - **Description**: Splits a string into an array of substrings.
    - **Example**:
      ```javascript
      let str = "Hello, World!";
      console.log(str.split(",")); // Output: ["Hello", " World!"]
      ```

#### 13. **`startsWith(searchString, [position])`**
    - **Description**: Checks if a string starts with the specified characters.
    - **Example**:
      ```javascript
      let str = "Hello, World!";
      console.log(str.startsWith("Hello")); // Output: true
      ```

#### 14. **`substr(start, length)`**
    - **Description**: Returns a part of the string between the start index and a number of characters afterward.
    - **Example**:
      ```javascript
      let str = "Hello, World!";
      console.log(str.substr(0, 5));
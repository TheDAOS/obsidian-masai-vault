Pseudo-classes in CSS are used to define the special states of an element. They allow you to style elements based on their state or position in the document.

## Common Pseudo-classes

### 1. `:hover`
- Applies styles when the user hovers over an element.
```css
a:hover {
   color: red;
}
```

### 2. **:focus**
   - Applies styles when an element has focus (e.g., when a form field is selected).
   ```css
   input:focus {
       border: 2px solid blue;
   }
   ```

3. **:active**
   - Applies styles when an element is being activated (e.g., clicked).
   ```css
   button:active {
       background-color: green;
   }
   ```

4. **:first-child**
   - Applies styles to the first child of a parent element.
   ```css
   p:first-child {
       font-weight: bold;
   }
   ```

5. **:last-child**
   - Applies styles to the last child of a parent element.
   ```css
   p:last-child {
       font-style: italic;
   }
   ```

6. **:nth-child(n)**
   - Applies styles to the nth child of a parent element.
   ```css
   p:nth-child(2) {
       color: blue;
   }
   ```

7. **:nth-of-type(n)**
   - Applies styles to the nth element of a specific type.
   ```css
   p:nth-of-type(3) {
       color: green;
   }
   ```

8. **:not(selector)**
   - Applies styles to elements that do not match the specified selector.
   ```css
   p:not(.special) {
       color: gray;
   }
   ```

9. **:link**
   - Applies styles to unvisited links.
   ```css
   a:link {
       color: blue;
   }
   ```

10. **:visited**
    - Applies styles to visited links.
    ```css
    a:visited {
        color: purple;
    }
    ```

11. **:enabled**
    - Applies styles to enabled form elements.
    ```css
    input:enabled {
        background-color: white;
    }
    ```

12. **:disabled**
    - Applies styles to disabled form elements.
    ```css
    input:disabled {
        background-color: lightgray;
    }
    ```

13. **:checked**
    - Applies styles to checked form elements (e.g., checkboxes, radio buttons).
    ```css
    input:checked {
        background-color: yellow;
    }
    ```

14. **:root**
    - Applies styles to the root element of the document (usually `<html>`).
    ```css
    :root {
        --main-color: #06c;
    }
    ```

15. **:lang(language)**
    - Applies styles to elements with a specific language attribute.
    ```css
    p:lang(en) {
        font-family: Arial, sans-serif;
    }
    ```

These pseudo-classes help in creating dynamic and interactive web designs by allowing you to style elements based on their state and position.
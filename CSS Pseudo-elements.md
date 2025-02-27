Pseudo-elements in CSS are used to style specific parts of an element. They allow you to apply styles to content that is not explicitly present in the HTML.

## Common Pseudo-elements

1. **::before**
   - Inserts content before the content of an element.
   ```css
   p::before {
       content: "Note: ";
       color: red;
   }
   ```

2. **::after**
   - Inserts content after the content of an element.
   ```css
   p::after {
       content: " (end of note)";
       color: blue;
   }
   ```

3. **::first-line**
   - Applies styles to the first line of a block-level element.
   ```css
   p::first-line {
       font-weight: bold;
       color: green;
   }
   ```

4. **::first-letter**
   - Applies styles to the first letter of a block-level element.
   ```css
   p::first-letter {
       font-size: 2em;
       color: orange;
   }
   ```

5. **::selection**
   - Applies styles to the portion of an element that is selected by the user.
   ```css
   p::selection {
       background-color: yellow;
       color: black;
   }
   ```

6. **::placeholder**
   - Applies styles to the placeholder text in form elements.
   ```css
   input::placeholder {
       color: gray;
       font-style: italic;
   }
   ```

7. **::backdrop**
   - Applies styles to the backdrop of a full-screen element (e.g., a modal dialog).
   ```css
   ::backdrop {
       background-color: rgba(0, 0, 0, 0.5);
   }
   ```

8. **::marker**
   - Applies styles to the marker box of list items.
   ```css
   li::marker {
       color: red;
       font-size: 1.2em;
   }
   ```

9. **::file-selector-button**
   - Applies styles to the button of a file input element.
   ```css
   input[type="file"]::file-selector-button {
       background-color: blue;
       color: white;
   }
   ```

10. **::caret**
    - Applies styles to the caret (text insertion point) in editable elements.
    ```css
    input::caret {
        color: red;
        width: 2px;
    }
    ```

These pseudo-elements enhance the styling capabilities of CSS by allowing you to target and style specific parts of an element's content or behavior.
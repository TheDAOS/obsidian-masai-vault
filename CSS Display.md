In CSS (Cascading Style Sheets), the `display` property is used to define how an element is displayed on the web page. It determines the layout behavior of an element and affects how it interacts with other elements in the document. Here are some of the most common values for the `display` property:

1. **block**: The element is displayed as a block-level element. It starts on a new line and takes up the full width available. Examples include `<div>`, `<h1>`, `<p>`, etc.

   ```css
   .block {
       display: block;
   }
   ```

2. **inline**: The element is displayed as an inline element. It does not start on a new line and only takes up as much width as necessary. Examples include `<span>`, `<a>`, `<strong>`, etc.

   ```css
   .inline {
       display: inline;
   }
   ```

3. **inline-block**: The element is displayed as an inline-level block container. It allows you to set width and height while still flowing with other inline elements.

   ```css
   .inline-block {
       display: inline-block;
   }
   ```

4. **none**: The element is not displayed at all (it is removed from the document flow). This is often used to hide elements.

   ```css
   .hidden {
       display: none;
   }
   ```

5. **flex**: The element is displayed as a flex container, allowing for a flexible layout. This is useful for creating responsive designs.

   ```css
   .flex-container {
       display: flex;
   }
   ```

6. **grid**: The element is displayed as a grid container, enabling a grid-based layout system.

   ```css
   .grid-container {
       display: grid;
   }
   ```

7. **table**: The element is displayed as a table. This can be useful for creating table-like layouts without using the `<table>` element.

   ```css
   .table {
       display: table;
   }
   ```

8. **table-row**: The element is displayed as a table row.

   ```css
   .table-row {
       display: table-row;
   }
   ```

9. **table-cell**: The element is displayed as a table cell.

   ```css
   .table-cell {
       display: table-cell;
   }
   ```

### Summary
The `display` property is fundamental in CSS for controlling the layout of elements on a web page. By choosing the appropriate display value, you can create various layouts and control how elements interact with each other in the document flow.
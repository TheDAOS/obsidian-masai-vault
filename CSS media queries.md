CSS media queries are a powerful feature that allows you to apply different styles to your web pages based on various conditions, such as the width of the viewport, the type of device, and the orientation of the screen. This makes it possible to create responsive designs that adapt to different screen sizes and devices, ensuring a better user experience across a wide range of platforms.

### Basic Syntax

The basic syntax for a media query in CSS is as follows:

```css
@media (condition) {
  /* CSS rules */
}
```

### Common Conditions

1. **Width and Height**:
   - `min-width`: Applies styles when the viewport width is at least the specified value.
   - `max-width`: Applies styles when the viewport width is at most the specified value.
   - `min-height`: Applies styles when the viewport height is at least the specified value.
   - `max-height`: Applies styles when the viewport height is at most the specified value.

   ```css
   @media (min-width: 600px) {
     body {
       background-color: lightblue;
     }
   }

   @media (max-width: 480px) {
     body {
       background-color: lightcoral;
     }
   }
   ```

2. **Orientation**:
   - `orientation: portrait`: Applies styles when the device is in portrait mode.
   - `orientation: landscape`: Applies styles when the device is in landscape mode.

   ```css
   @media (orientation: portrait) {
     body {
       background-color: lightgreen;
     }
   }

   @media (orientation: landscape) {
     body {
       background-color: lightyellow;
     }
   }
   ```

3. **Device Type**:
   - `print`: Applies styles when the document is being printed.
   - `screen`: Applies styles when the document is being displayed on a screen.
   - `speech`: Applies styles when the document is being read aloud by a screen reader.

   ```css
   @media print {
     body {
       background-color: white;
       color: black;
     }
   }

   @media screen {
     body {
       background-color: lightgray;
       color: darkgray;
     }
   }
   ```

4. **Resolution**:
   - `min-resolution`: Applies styles when the resolution is at least the specified value.
   - `max-resolution`: Applies styles when the resolution is at most the specified value.

   ```css
   @media (min-resolution: 2dppx) {
     body {
       background-color: lightpink;
     }
   }
   ```

### Combining Conditions

You can combine multiple conditions using logical operators like `and`, `or`, and `not`.

```css
@media (min-width: 600px) and (orientation: landscape) {
  body {
    background-color: lightblue;
  }
}

@media (max-width: 480px) or (orientation: portrait) {
  body {
    background-color: lightcoral;
  }
}

@media not (min-width: 600px) {
  body {
    background-color: lightgreen;
  }
}
```

### Example

Here's a complete example that demonstrates how to use media queries to create a responsive design:

```css
/* Default styles */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

/* Styles for screens wider than 600px */
@media (min-width: 600px) {
  body {
    background-color: lightblue;
  }
  .container {
    width: 80%;
    margin: 0 auto;
  }
}

/* Styles for screens narrower than 600px */
@media (max-width: 599px) {
  body {
    background-color: lightcoral;
  }
  .container {
    width: 90%;
    margin: 0 auto;
  }
}

/* Styles for portrait orientation */
@media (orientation: portrait) {
  body {
    background-color: lightgreen;
  }
}

/* Styles for landscape orientation */
@media (orientation: landscape) {
  body {
    background-color: lightyellow;
  }
}
```
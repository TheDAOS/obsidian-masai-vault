CSS Specificity is a fundamental concept in Cascading Style Sheets (CSS) that determines which CSS rule is applied to an element when multiple rules could potentially apply. Understanding specificity is crucial for writing effective and maintainable CSS, as it helps you predict and control the application of styles.

### How Specificity Works

Specificity is calculated based on the types of selectors used in a CSS rule. The more specific a selector is, the higher its priority. Specificity is determined by the following hierarchy:

1. **Inline Styles**: Styles applied directly to an element using the `style` attribute.
2. **IDs**: Styles applied using an ID selector (e.g., `#id`).
3. **Classes, Attributes, and Pseudo-classes**: Styles applied using class selectors (e.g., `.class`), attribute selectors (e.g., `[type="text"]`), and pseudo-classes (e.g., `:hover`).
4. **Elements and Pseudo-elements**: Styles applied using element selectors (e.g., `div`) and pseudo-elements (e.g., `::before`).

### Calculating Specificity

Specificity is often represented as a four-part number: `(inline, id, class, element)`. Here’s how you can calculate it:

- **Inline Styles**: 1,0,0,0
- **IDs**: 0,1,0,0
- **Classes, Attributes, Pseudo-classes**: 0,0,1,0
- **Elements, Pseudo-elements**: 0,0,0,1

For example:
- `div p` has a specificity of 0,0,0,2.
- `.class p` has a specificity of 0,0,1,1.
- `#id p` has a specificity of 0,1,0,1.
- `div#id.class p` has a specificity of 0,1,1,2.

### Examples

1. **Inline Styles**:
   ```html
   <div style="color: red;">This text is red.</div>
   ```
   Inline styles have the highest specificity.

2. **ID Selector**:
   ```css
   #header {
     color: blue;
   }
   ```
   ID selectors have a higher specificity than class selectors.

3. **Class Selector**:
   ```css
   .button {
     color: green;
   }
   ```
   Class selectors have a lower specificity than ID selectors but higher than element selectors.

4. **Element Selector**:
   ```css
   p {
     color: purple;
   }
   ```
   Element selectors have the lowest specificity.

### Best Practices

- **Avoid Over-Specificity**: Overly specific selectors can make your CSS harder to maintain. Try to use class selectors where possible.
- **Use Classes for Styling**: Classes are more flexible and reusable than IDs.
- **Keep It Simple**: Simpler selectors are easier to read and maintain.
- **Use `!important` Sparingly**: The `!important` declaration can override specificity, but it should be used sparingly as it can make debugging difficult.
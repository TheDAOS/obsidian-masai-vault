The `prefers-color-scheme` media feature in CSS allows you to apply different styles based on the user's preferred color scheme, which can be either light or dark. This feature is particularly useful for creating responsive designs that adapt to the user's system settings, providing a better user experience.

Here's a basic example of how to use `prefers-color-scheme` in CSS:

```css
/* Default styles for light mode */
body {
    background-color: white;
    color: black;
}

/* Styles for dark mode */
@media (prefers-color-scheme: dark) {
    body {
        background-color: black;
        color: white;
    }
}
```

In this example:
- The default styles are applied for light mode.
- When the user's system is set to dark mode, the styles within the `@media (prefers-color-scheme: dark)` block are applied, changing the background color to black and the text color to white.

You can also use `prefers-color-scheme: no-preference` to target users who have not specified a preference:

```css
/* Styles for users with no preference */
@media (prefers-color-scheme: no-preference) {
    body {
        background-color: gray;
        color: black;
    }
}
```
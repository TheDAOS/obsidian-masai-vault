CSS combinators are used to combine selectors in a way that allows you to target elements based on their relationship to other elements in the document tree. There are several types of combinators in CSS, each serving a different purpose. Here's an overview of the main CSS combinators:

## 1. Descendant Combinator
The descendant combinator is represented by a space character. It selects elements that are descendants of a specified element.

```css
/* Selects all <p> elements that are descendants of a <div> element */
div p {
  color: blue;
}
```

## 2. Child Combinator
The child combinator is represented by the `>` symbol. It selects elements that are direct children of a specified element.

```css
/* Selects all <p> elements that are direct children of a <div> element */
div > p {
  color: green;
}
```

## 3. Adjacent Sibling Combinator
The adjacent sibling combinator is represented by the `+` symbol. It selects elements that are immediately preceded by a specified element.

```css
/* Selects all <p> elements that are immediately preceded by a <h1> element */
h1 + p {
  color: red;
}
```

## 4. General Sibling Combinator
The general sibling combinator is represented by the `~` symbol. It selects elements that are siblings of a specified element, regardless of how many elements come between them.

```css
/* Selects all <p> elements that are siblings of a <h1> element */
h1 ~ p {
  color: purple;
}
```

## 5. Column Combinator
The column combinator is represented by the `||` symbol. It is used in conjunction with the `::nth-column` pseudo-element to select elements in specific columns of a multi-column layout.

```css
/* Selects elements in the second column of a multi-column layout */
::nth-column(2) {
  background-color: yellow;
}
```

### Examples

##### Descendant Combinator
```html
<div>
  <p>This is a paragraph inside a div.</p>
  <span>
    <p>This is a paragraph inside a span inside a div.</p>
  </span>
</div>
```

```css
div p {
  color: blue;
}
```

##### Child Combinator
```html
<div>
  <p>This is a direct child paragraph.</p>
  <span>
    <p>This is not a direct child paragraph.</p>
  </span>
</div>
```

```css
div > p {
  color: green;
}
```

##### Adjacent Sibling Combinator
```html
<h1>Heading</h1>
<p>This is an adjacent sibling paragraph.</p>
<p>This is another paragraph.</p>
```

```css
h1 + p {
  color: red;
}
```

##### General Sibling Combinator
```html
<h1>Heading</h1>
<p>This is a sibling paragraph.</p>
<div>
  <p>This is a paragraph inside a div.</p>
</div>
<p>This is another sibling paragraph.</p>
```

```css
h1 ~ p {
  color: purple;
}
```
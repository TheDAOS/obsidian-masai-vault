The Document Object Model (DOM) is a programming interface for web documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects; this means that the document is structured in a way that allows for easy manipulation and interaction using JavaScript.

#### Key Concepts

1. **Document Object**: The `document` object is the entry point to the DOM. It represents the entire HTML document and provides methods and properties to access and manipulate the document's content.

2. **Nodes**: The DOM is composed of nodes, which are objects representing parts of the document. The most common types of nodes are:
   - **Element Nodes**: Represent HTML elements (e.g., `<div>`, `<p>`, `<a>`).
   - **Text Nodes**: Represent the text content within elements.
   - **Attribute Nodes**: Represent the attributes of elements (e.g., `id`, `class`, `href`).

3. **Traversing the DOM**: You can navigate through the DOM tree using various properties and methods, such as `parentNode`, `childNodes`, `firstChild`, `lastChild`, `nextSibling`, and `previousSibling`.

4. **Manipulating the DOM**: JavaScript provides a rich set of methods to create, modify, and delete nodes in the DOM. Common methods include `createElement`, `appendChild`, `removeChild`, `setAttribute`, and `getElementById`.

5. **Event Handling**: The DOM allows you to attach event listeners to elements, enabling interactive web applications. Common events include `click`, `mouseover`, `keydown`, and `submit`.

#### Basic Example

Here's a simple example to illustrate how to manipulate the DOM using JavaScript:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOM Manipulation Example</title>
</head>
<body>
    <h1 id="title">Hello, World!</h1>
    <button id="changeTextButton">Change Text</button>

    <script>
        // Select the button element
        const button = document.getElementById('changeTextButton');

        // Add an event listener to the button
        button.addEventListener('click', function() {
            // Select the h1 element
            const title = document.getElementById('title');

            // Change the text content of the h1 element
            title.textContent = 'Hello, JavaScript!';
        });
    </script>
</body>
</html>
```

In this example, clicking the button changes the text of the `<h1>` element from "Hello, World!" to "Hello, JavaScript!". This demonstrates how to select elements, add event listeners, and modify the content of the DOM.

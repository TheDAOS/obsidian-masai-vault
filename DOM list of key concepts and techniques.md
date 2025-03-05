
### Basic DOM Manipulation
1. [[DOM Selecting Elements]]
   - `document.getElementById()`
   - `document.getElementsByClassName()`
   - `document.getElementsByTagName()`
   - `document.querySelector()`
   - `document.querySelectorAll()`

2. [[DOM Creating and Adding Elements]]
   - `document.createElement()`
   - `element.appendChild()`
   - `element.insertBefore()`
   - `element.replaceChild()`
   - `element.removeChild()`

3. **Modifying Elements**
   - `element.innerHTML`
   - `element.textContent`
   - `element.setAttribute()`
   - `element.getAttribute()`
   - `element.style`

4. **Event Handling**
   - `element.addEventListener()`
   - `element.removeEventListener()`
   - Event types (e.g., `click`, `mouseover`, `keydown`)

### Advanced DOM Manipulation
1. **Traversing the DOM**
   - `element.parentNode`
   - `element.childNodes`
   - `element.firstChild`
   - `element.lastChild`
   - `element.nextSibling`
   - `element.previousSibling`
   - `element.children`

2. **Manipulating Attributes and Properties**
   - `element.classList`
   - `element.dataset`
   - `element.id`
   - `element.name`

3. **Form Handling**
   - `form.elements`
   - `element.value`
   - `element.checked`
   - `element.selectedIndex`

4. **Dynamic Content Loading**
   - `XMLHttpRequest`
   - `Fetch API`
   - `async` and `await`

### Best Practices and Performance
1. **Efficient DOM Manipulation**
   - Minimizing reflows and repaints
   - Using `documentFragment`
   - Batching DOM updates

2. **Error Handling**
    - `try...catch` blocks
    - `console.error()`
    - `window.onerror`

### Modern JavaScript Features
1. **Template Literals and Strings**
    - Using template literals for dynamic content

2. **Arrow Functions and ES6+ Features**
    - Using arrow functions for event handlers
    - Destructuring assignments

3. **Modules and Import/Export**
    - Using ES6 modules for better code organization

### Example Code Snippets

#### Selecting Elements
```javascript
// Selecting by ID
const elementById = document.getElementById('myId');

// Selecting by Class Name
const elementsByClass = document.getElementsByClassName('myClass');

// Selecting by Tag Name
const elementsByTag = document.getElementsByTagName('div');

// Selecting with querySelector
const elementByQuery = document.querySelector('.myClass');

// Selecting multiple elements with querySelectorAll
const elementsByQueryAll = document.querySelectorAll('.myClass');
```

#### Creating and Adding Elements
```javascript
// Creating a new element
const newDiv = document.createElement('div');
newDiv.textContent = 'Hello, World!';

// Adding the new element to the DOM
document.body.appendChild(newDiv);
```

#### Modifying Elements
```javascript
// Changing the inner HTML
elementById.innerHTML = '<strong>New Content</strong>';

// Changing the text content
elementById.textContent = 'New Text Content';

// Setting an attribute
elementById.setAttribute('data-custom', 'value');

// Getting an attribute
const customValue = elementById.getAttribute('data-custom');

// Changing the style
elementById.style.color = 'red';
```

#### Event Handling
```javascript
// Adding an event listener
elementById.addEventListener('click', function() {
    alert('Element clicked!');
});

// Removing an event listener
function handleClick() {
    alert('Element clicked!');
}
elementById.addEventListener('click', handleClick);
elementById.removeEventListener('click', handleClick);
```

#### Traversing the DOM
```javascript
// Getting the parent node
const parent = elementById.parentNode;

// Getting child nodes
const children = elementById.childNodes;

// Getting the first child
const firstChild = elementById.firstChild;

// Getting the last child
const lastChild = elementById.lastChild;

// Getting the next sibling
const nextSibling = elementById.nextSibling;

// Getting the previous sibling
const previousSibling = elementById.previousSibling;

// Getting all children
const allChildren = elementById.children;
```

#### Form Handling
```javascript
// Accessing form elements
const form = document.querySelector('form');
const input = form.elements['myInput'];

// Getting the value of an input

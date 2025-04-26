`useRef` is a hook in React that allows you to create a mutable object that persists for the lifetime of the component. Unlike state variables managed by `useState`, the value of a ref does not trigger a re-render when it changes. This makes `useRef` useful for scenarios where you need to store a value that should persist across renders without causing the component to re-render.

### Key Use Cases for `useRef`

1. **Accessing DOM Elements**: One of the most common uses of `useRef` is to directly access and manipulate DOM elements. This is particularly useful for focusing an input field, measuring the dimensions of an element, or interacting with third-party libraries that require direct DOM access.

2. **Storing Previous State**: You can use `useRef` to store the previous state value, which can be useful for comparing the current state with the previous state without causing a re-render.

3. **Storing Mutable Values**: If you need to store a value that changes over time but does not need to trigger a re-render, `useRef` is a good choice. For example, you might use it to keep track of a timer or an interval.

### Basic Syntax

```javascript
const myRef = useRef(initialValue);
```

- `myRef` is the ref object.
- `initialValue` is the initial value of the ref. This can be any value, including `null`.

### Example: Accessing a DOM Element

Here's an example of how to use `useRef` to focus an input field when a button is clicked:

```jsx
import React, { useRef } from 'react';

function FocusInput() {
	const inputRef = useRef(null);
	
	const focusInput = () => {
		inputRef.current.focus();
	};
	
	return (
		<div>
			<input ref={inputRef} type="text" />
			<button onClick={focusInput}>Focus the input</button>
		</div>
	);
}

export default FocusInput;
```

In this example, `inputRef` is a ref object that is attached to the input element. When the button is clicked, the `focusInput` function is called, which uses `inputRef.current` to access the input element and call its `focus` method.

### Example: Storing Previous State

Here's an example of how to use `useRef` to store the previous state value:

```jsx
import React, { useState, useRef, useEffect } from 'react';

function PreviousStateExample() {
	const [count, setCount] = useState(0);
	const prevCountRef = useRef();
	
	useEffect(() => {
		prevCountRef.current = count;
	}, [count]);
	
	return (
		<div>
			<p>Current Count: {count}</p>
			<p>Previous Count: {prevCountRef.current}</p>
			<button onClick={() => setCount(count + 1)}>Increment</button>
		</div>
	);
}

export default PreviousStateExample;
```

In this example, `prevCountRef` is used to store the previous value of `count`. The `useEffect` hook updates `prevCountRef.current` whenever `count` changes, allowing you to access the previous state value without causing a re-render.

### Conclusion

`useRef` is a versatile hook in React that provides a way to create mutable objects that persist across renders. It is particularly useful for accessing DOM elements, storing previous state values, and managing mutable values that do not need to trigger re-renders. By understanding and utilizing `useRef`, you can write more efficient and effective React components.
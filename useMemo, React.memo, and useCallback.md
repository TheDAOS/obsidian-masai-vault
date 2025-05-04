`useMemo`, `React.memo`, and `useCallback` are all tools in the React ecosystem designed to optimize performance by memoizing values, components, and functions, respectively. Each serves a specific purpose and is used in different contexts. Here's a comparison of these three hooks/optimizations:

### When to Use Each

- **`useMemo`**: Use when you have an expensive computation that you want to cache.
- **`React.memo`**: Use when you have a functional component that you want to prevent from re-rendering unless its props change.
- **`useCallback`**: Use when you have a callback function that you want to avoid recreating on every render, especially when passing it to memoized child components.

### Comparison Summary

| Feature      | `useMemo`                             | `React.memo`                      | `useCallback`                             |
| ------------ | ------------------------------------- | --------------------------------- | ----------------------------------------- |
| **Purpose**  | Memoizes computation results          | Memoizes component renders        | Memoizes callback functions               |
| **Syntax**   | `useMemo(() => computeValue, [deps])` | `React.memo(Component, areEqual)` | `useCallback(() => functionBody, [deps])` |
| **Use Case** | Expensive computations                | Preventing unnecessary re-renders | Stable callback references                |
| **Benefits** | Prevents recalculations               | Prevents re-renders               | Prevents recreations of callbacks         |
| **Caveats**  | Overuse, dependencies                 | Overuse, custom comparison        | Overuse, dependencies, stale closures     |

### `useMemo`

**Purpose**: Memoizes the result of a computation.

**Syntax**:
```javascript
const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);
```

**Use Case**:
- Use `useMemo` when you have an expensive computation that you want to avoid recalculating on every render.
- Ideal for memoizing derived values or results of complex calculations.

**Example**:
```javascript
const expensiveValue = useMemo(() => {
  let result = 0;
  for (let i = 0; i < 1e6; i++) {
    result += a + b;
  }
  return result;
}, [a, b]);
```

**Benefits**:
- Prevents unnecessary recalculations.
- Improves performance by caching the result of expensive computations.

**Caveats**:
- Overuse can lead to complex and hard-to-maintain code.
- Ensure dependencies are correctly specified to avoid stale data.

### `React.memo`

**Purpose**: Memoizes the rendering of a functional component.

**Syntax**:
```javascript
const MemoizedComponent = React.memo(Component, areEqual);
```

**Use Case**:
- Use `React.memo` when you have a functional component that you want to prevent from re-rendering unless its props change.
- Ideal for optimizing performance by avoiding unnecessary re-renders of child components.

**Example**:
```javascript
const MyComponent = React.memo(({ data }) => {
  console.log('MyComponent rendered');
  return <div>{data}</div>;
});
```

**Benefits**:
- Prevents unnecessary re-renders of components.
- Improves performance by memoizing the result of a component render.

**Caveats**:
- Overuse can lead to complex and hard-to-maintain code.
- Ensure the custom comparison function (if used) is correctly implemented.

### `useCallback`

**Purpose**: Memoizes a callback function.

**Syntax**:
```javascript
const memoizedCallback = useCallback(() => {
  // Function body
}, [dependency1, dependency2]);
```

**Use Case**:
- Use `useCallback` when you have a callback function that you want to avoid recreating on every render.
- Ideal for passing stable callback references to child components, especially when those components are memoized with `React.memo`.

**Example**:
```javascript
const handleClick = useCallback(() => {
  console.log('Button clicked');
  setCount(prevCount => prevCount + 1);
}, []);
```

**Benefits**:
- Prevents unnecessary recreations of callback functions.
- Improves performance by providing stable references to callbacks.

**Caveats**:
- Overuse can lead to complex and hard-to-maintain code.
- Ensure dependencies are correctly specified to avoid stale closures.
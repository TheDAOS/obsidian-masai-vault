### Step 1: Install Dependencies

You need to install the required packages first:

```bash
npm install redux react-redux
```

### Step 2: Define Action Types

```js
// src/redux/actionTypes.js
export const ADD_TODO = "ADD_TODO";
export const TOGGLE_TODO = "TOGGLE_TODO";
export const DELETE_TODO = "DELETE_TODO";
```

### Step 3: Create Action Creators

```js
// src/redux/actions.js
import { ADD_TODO, TOGGLE_TODO, DELETE_TODO } from "./actionTypes";

export const addTodo = (title) => ({
  type: ADD_TODO,
  payload: {
    title,
    id: Date.now(),
    status: false,
  },
});

export const toggleTodo = (id) => ({
  type: TOGGLE_TODO,
  payload: id,
});

export const deleteTodo = (id) => ({
  type: DELETE_TODO,
  payload: id,
});
```

### Step 4: Create the Reducer

```js
// src/redux/reducer.js
import { ADD_TODO, TOGGLE_TODO, DELETE_TODO } from "./actionTypes";

const initialState = {
  todos: [],
};

export const todoReducer = (state = initialState, action) => {
  switch (action.type) {
    case ADD_TODO:
      return {
        ...state,
        todos: [...state.todos, action.payload],
      };

    case TOGGLE_TODO:
      return {
        ...state,
        todos: state.todos.map((todo) =>
          todo.id === action.payload ? { ...todo, status: !todo.status } : todo
        ),
      };

    case DELETE_TODO:
      return {
        ...state,
        todos: state.todos.filter((todo) => todo.id !== action.payload),
      };

    default:
      return state;
  }
};
```

### Step 5: Create the Redux Store

```js
// src/redux/store.js
import { createStore } from "redux";
import { todoReducer } from "./reducer";

export const store = createStore(todoReducer);
```

### Step 6: Provide the Store to React

```js
// src/index.js
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";
import { Provider } from "react-redux";
import { store } from "./redux/store";

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(
  <Provider store={store}>
    <App />
  </Provider>
);
```

### Step 7: Build the React Components

#### `App.js`

```js
import React from "react";
import TodoInput from "./components/TodoInput";
import TodoList from "./components/TodoList";

const App = () => {
  return (
    <div>
      <h1>Todo List</h1>
      <TodoInput />
      <TodoList />
    </div>
  );
};

export default App;
```

#### `TodoInput.js`

```js
import React, { useState } from "react";
import { useDispatch } from "react-redux";
import { addTodo } from "../redux/actions";

const TodoInput = () => {
  const [title, setTitle] = useState("");
  const dispatch = useDispatch();

  const handleAdd = () => {
    if (title.trim()) {
      dispatch(addTodo(title));
      setTitle("");
    }
  };

  return (
    <div>
      <input
        type="text"
        placeholder="Enter todo"
        value={title}
        onChange={(e) => setTitle(e.target.value)}
      />
      <button onClick={handleAdd}>Add</button>
    </div>
  );
};

export default TodoInput;
```

#### `TodoList.js`

```js
import React from "react";
import { useSelector, useDispatch } from "react-redux";
import { toggleTodo, deleteTodo } from "../redux/actions";

const TodoList = () => {
  const todos = useSelector((state) => state.todos);
  const dispatch = useDispatch();

  return (
    <ul>
      {todos.map((todo) => (
        <li key={todo.id}>
          <span
            style={{ textDecoration: todo.status ? "line-through" : "none" }}
            onClick={() => dispatch(toggleTodo(todo.id))}
          >
            {todo.title}
          </span>
          <button onClick={() => dispatch(deleteTodo(todo.id))}>Delete</button>
        </li>
      ))}
    </ul>
  );
};

export default TodoList;
```

### Folder Structure

```
src/
├── components/
│   ├── TodoInput.js
│   └── TodoList.js
├── redux/
│   ├── actionTypes.js
│   ├── actions.js
│   ├── reducer.js
│   └── store.js
├── App.js
└── index.js
```
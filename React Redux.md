To set up a Vite project with React and legacy Redux for a simple counter application, follow these steps:

### Step 1: Create a Vite Project

1. **Install Vite** (if you haven't already):
   Make sure you have Node.js installed. Then, you can create a new Vite project using the following command:

   ```bash
   npm create vite@latest my-redux-counter -- --template react
   ```

   Replace `my-redux-counter` with your desired project name.

2. **Navigate to the project directory**:

   ```bash
   cd my-redux-counter
   ```

3. **Install dependencies**:

   ```bash
   npm install
   ```

### Step 2: Install Redux and React-Redux

```bash
npm install redux react-redux
```

### Step 3: Set Up Redux

1. **Create a Redux store**:

   Create a new folder called `store` in the `src` directory and create a file named `store.js`:

   ```javascript
   // src/store/store.js
   import { createStore } from 'redux';

   // Initial state
   const initialState = {
       count: 0,
   };

   // Reducer function
   const counterReducer = (state = initialState, action) => {
       switch (action.type) {
           case 'INCREMENT':
               return { ...state, count: state.count + 1 };
           case 'DECREMENT':
               return { ...state, count: state.count - 1 };
           default:
               return state;
       }
   };

   // Create store
   const store = createStore(counterReducer);

   export default store;
   ```

2. **Set up the Redux Provider**:

   Modify the `main.jsx` file to include the Redux Provider:

   ```jsx
   // src/main.jsx
   import React from 'react';
   import ReactDOM from 'react-dom/client';
   import { Provider } from 'react-redux';
   import App from './App';
   import store from './store/store';
   import './index.css';

   ReactDOM.createRoot(document.getElementById('root')).render(
       <Provider store={store}>
           <App />
       </Provider>
   );
   ```

### Step 4: Create the Counter Component

1. **Create a Counter component**:

   Create a new file named `Counter.jsx` in the `src` directory:

   ```jsx
   // src/Counter.jsx
   import React from 'react';
   import { useSelector, useDispatch } from 'react-redux';

   const Counter = () => {
       const count = useSelector((state) => state.count);
       const dispatch = useDispatch();

       return (
           <div>
               <h1>Counter: {count}</h1>
               <button onClick={() => dispatch({ type: 'INCREMENT' })}>Increment</button>
               <button onClick={() => dispatch({ type: 'DECREMENT' })}>Decrement</button>
           </div>
       );
   };

   export default Counter;
   ```

2. **Use the Counter component in App**:

   Modify the `App.jsx` file to include the `Counter` component:

   ```jsx
   // src/App.jsx
   import React from 'react';
   import Counter from './Counter';

   const App = () => {
       return (
           <div>
               <h1>My Redux Counter</h1>
               <Counter />
           </div>
       );
   };

   export default App;
   ```

### Step 5: Run the Application

```bash
npm run dev
```


[[Todo app example]]
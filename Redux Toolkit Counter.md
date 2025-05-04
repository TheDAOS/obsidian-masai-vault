
### 1. Install Redux Toolkit and React-Redux:
First, you need to install the necessary packages. You can do this using npm or yarn.

```bash
npm install @reduxjs/toolkit react-redux
```

### 2. Set up the Redux store and slice:
Create a file named `counterSlice.js` to define the slice.

```javascript
// counterSlice.js
import { createSlice } from '@reduxjs/toolkit';

const counterSlice = createSlice({
	name: 'counter',
	initialState: { value: 0 },
	reducers: {
		increment: (state) => {
			state.value += 1;
		},
		decrement: (state) => {
			state.value -= 1;
		},
		incrementByAmount: (state, action) => {
			state.value += action.payload;
		},
	},
});

export const { increment, decrement, incrementByAmount } = counterSlice.actions;
export default counterSlice.reducer;
```

### 3. Configure the store:
Create a file named `store.js` to configure the Redux store.

```javascript
// store.js
import { configureStore } from '@reduxjs/toolkit';
import counterReducer from './counterSlice';

const store = configureStore({
	reducer: {
		counter: counterReducer,
	},
});

export default store;
```

### 4. Create the React component:
Create a file named `Counter.js` to define the React component that will interact with the Redux store.

```jsx
// Counter.js
import React from 'react';
import { useSelector, useDispatch } from 'react-redux';
import { increment, decrement, incrementByAmount } from './counterSlice';

const Counter = () => {
	const count = useSelector((state) => state.counter.value);
	const dispatch = useDispatch();
	
	return (
		<div>
			<div>
				<button onClick={() => dispatch(decrement())}>-</button>
				<span>{count}</span>
				<button onClick={() => dispatch(increment())}>+</button>
			</div>
			<div>
				<button onClick={() => dispatch(incrementByAmount(2))}>Increment by 2</button>
			</div>
		</div>
	);
};

export default Counter;
```

### 5. Set up the React application:
Finally, set up your main application file (e.g., `App.js` or `index.js`) to provide the Redux store to your React application.

```jsx
// App.js
import React from 'react';
import { Provider } from 'react-redux';
import store from './store';
import Counter from './Counter';

const App = () => {
	return (
		<Provider store={store}>
			 <Counter />
		</Provider>
	);
};

export default App;
```

### 6. Run your application:
Make sure your development server is running. If you're using Create React App, you can start it with:

```bash
npm run dev
```


```
my-redux-app/
├── public/
│   ├── index.html
│   └── ...
├── src/
│   ├── components/
│   │   ├── Counter.js
│   │   └── ...
│   ├── features/
│   │   ├── counter/
│   │   │   ├── counterSlice.js
│   │   │   └── ...
│   │   └── ...
│   ├── reducers/
│   │   ├── index.js
│   │   └── ...
│   ├── store/
│   │   ├── index.js
│   │   └── ...
│   ├── App.js
│   ├── index.js
│   └── ...
├── package.json
├── README.md
└── ...
```
Setting up `react-router-dom` in a React application is a common task for managing navigation and routing. Below is a step-by-step guide to help you get started with `react-router-dom`.

### Step 1: Install `react-router-dom`

First, you need to install the `react-router-dom` package. You can do this using npm or yarn.

```bash
npm install react-router-dom
```

### Step 2: Set Up the Router

Create a new file, for example, `App.js`, and set up the router. You will use the `BrowserRouter` component to wrap your application and define your routes using the `Routes` and `Route` components.

```jsx
// App.js
import React from 'react';
import { BrowserRouter as Router, Routes, Route } from 'react-router-dom';
import Home from './Home';
import About from './About';
import Contact from './Contact';

function App() {
  return (
    <Router>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </Router>
  );
}

export default App;
```

### Step 3: Create Components for Each Route

Create separate components for each route. For example, create `Home.js`, `About.js`, and `Contact.js` files.

```jsx
// Home.js
import React from 'react';

function Home() {
  return <h1>Home Page</h1>;
}

export default Home;
```

```jsx
// About.js
import React from 'react';

function About() {
  return <h1>About Page</h1>;
}

export default About;
```

```jsx
// Contact.js
import React from 'react';

function Contact() {
  return <h1>Contact Page</h1>;
}

export default Contact;
```

### Step 4: Add Navigation Links

To navigate between the different routes, you can use the `Link` component from `react-router-dom`. Add a navigation bar to your `App.js` file.

```jsx
// App.js
import React from 'react';
import { BrowserRouter as Router, Routes, Route, Link } from 'react-router-dom';
import Home from './Home';
import About from './About';
import Contact from './Contact';

function App() {
	return (
	    <Router>
		    <nav>
		        <ul>
				    <li>
			            <Link to="/">Home</Link>
				    </li>
			        <li>
			            <Link to="/about">About</Link>
					</li>
			        <li>
			            <Link to="/contact">Contact</Link>
			        </li>
		        </ul>
		    </nav>
		    <Routes>
		        <Route path="/" element={<Home />} />
		        <Route path="/about" element={<About />} />
		        <Route path="/contact" element={<Contact />} />
		    </Routes>
	    </Router>
	);
}

export default App;
```

### Step 5: Run Your Application

Make sure your development server is running. If it's not, you can start it with:

```bash
npm start
```

### Additional Features

#### Nested Routes

You can also create nested routes by using the `Outlet` component.

```jsx
// App.js
import React from 'react';
import { BrowserRouter as Router, Routes, Route, Link, Outlet } from 'react-router-dom';
import Home from './Home';
import About from './About';
import Contact from './Contact';
import Dashboard from './Dashboard';
import Settings from './Settings';

function App() {
  return (
    <Router>
	    <nav>
	        <ul>
	            <li>
		            <Link to="/">Home</Link>
	            </li>
		        <li>
		            <Link to="/about">About</Link>
		        </li>
			    <li>
	                <Link to="/contact">Contact</Link>
		        </li>
	        </ul>
	    </nav>
	    <Routes>
	        <Route path="/" element={<Home />} />
	        <Route path="/about" element={<About />} />
	        <Route path="/contact" element={<Contact />} />
	        <Route path="/dashboard" element={<Dashboard />}>
		        <Route path="settings" element={<Settings />} />
	        </Route>
	    </Routes>
    </Router>
  );
}

function Dashboard() {
	return (
		<div>
		    <h1>Dashboard</h1>
		    <Outlet />
		</div>
	);
}

function Settings() {
	return <h2>Settings Page</h2>;
}

export default App;
```

#### Programmatic Navigation

You can also navigate programmatically using the `useNavigate` hook.

```jsx
// Home.js
import React from 'react';
import { useNavigate } from 'react-router-dom
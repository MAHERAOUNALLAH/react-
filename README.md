🚀 React Fundamentals for Beginners – My Learning Notes

Hey there! I’ve recently started learning React, and I decided to write this blog to share the key concepts I’ve discovered so far. If you’re also beginning your React journey, this post might help you get a clear understanding of the basics.

🔍 What is React?

React is a JavaScript library for building user interfaces. It helps you create dynamic, fast, and interactive web apps using a component-based architecture.

🧩 Core Concepts You Should Know

1)JSX – JavaScript + XML
JSX lets us write HTML-like syntax in JavaScript:

const element = <h1>Hello, world!</h1>;

It compiles to:

React.createElement('h1', null, 'Hello, world!');

2)Components – The Building Blocks
Components are reusable pieces of UI.

function Welcome() {
return <h1>Welcome to my site!</h1>;
}

Or:

const Welcome = () => <h1>Welcome!</h1>;

Usage: <Welcome />

3)Rendering the App
React apps usually start in index.js or index.jsx:

import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App';
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);

4)useState – Managing State

import { useState } from 'react';

function Counter() {
const [count, setCount] = useState(0);
return (
<div>
<p>Count: {count}</p>
<button onClick={() => setCount(count + 1)}>+1</button>
</div>
);
}

5)useEffect – Side Effects

import { useEffect } from 'react';

useEffect(() => {
console.log('Component mounted!');
}, []);

6)Props – Passing Data

function Greeting({ name }) {
return <h1>Hello, {name}</h1>;
}

Usage: <Greeting name="Maher" />

7)Events – Like onClick

<button onClick={() => alert('Clicked!')}>Click Me</button>

8)Lists and Keys

const items = ['Apple', 'Banana', 'Orange'];

function FruitList() {
return (
<ul>
{items.map((fruit, index) => (
<li key={index}>{fruit}</li>
))}
</ul>
);
}

Conditional Rendering

function Message({ isLoggedIn }) {
return (
<div>
{isLoggedIn ? <p>Welcome back!</p> : <p>Please log in.</p>}
</div>
);
}

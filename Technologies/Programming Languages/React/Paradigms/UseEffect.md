The `useEffect` hook in [[React]] is essential for handling **side effects** in functional components. Side effects are anything that interacts with the "outside world" outside of the normal rendering process, such as:

- **[[Data fetching]]** (API calls)
- **[[DOM Manipulation]]** (manually changing the title, focusing elements)
- **Setting up subscriptions or event listeners**
- **Timers** (``setTimeout``, ``setInterval``)

#### Basic Structure
The `useEffect` hook takes two arguments:

- **A function (the effect)**: This is where you put the side effect code
- **An optional array (the dependency array)**: This controls when the effect runs.

```Javascript
import React, { useState, useEffect } from 'react';

function ExampleComponent() {
  const [count, setCount] = useState(0);

  // 1. The basic effect structure
  useEffect(() => {
    // This code runs AFTER every completed render.
    console.log(`The component rendered. The count is ${count}`);

    // Standard side effect (e.g., updating the document title)
    document.title = `You clicked ${count} times`;

    // The function returns (optional) cleanup function (see Section 4)
  }); // No dependency array here

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

#### Run After Every Render
If you **omit** the dependency array, the effect will run after the **initial mount AND after every subsequent update/re-render** of the component.
```Javascript
useEffect(() => {
  // Runs after every render
  console.log('I run every time!');
});
```

#### Run Only Once
If you pass an **empty array** (`[]`), the effect will run **only once** after the initial render.
```Javascript
useEffect(() => {
  // Runs ONLY after the first render (componentDidMount equivalent)
  console.log('I only run once.');

  // This is the ideal place for initial API calls.
  fetchData();
}, []); // <--- Empty dependency array
```

#### Run When Specific Values Change
If you include **values inside the array**, the effect will re-run only when one of those specified values changes between renders
```Javascript
const [userId, setUserId] = useState(1);

useEffect(() => {
  console.log(`Fetching data for user ID: ${userId}`);
  
  // Example: Fetch data whenever userId changes
  fetch(`/api/users/${userId}`)
    .then(res => res.json())
    .then(data => console.log(data));

}, [userId]); // <--- Effect runs only when 'userId' changes
```
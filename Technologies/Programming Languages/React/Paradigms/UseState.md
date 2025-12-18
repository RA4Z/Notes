The `useState` hook in [[React]] is a fundamental tool for managing state in functional components. It allows you to add state variables to your components, enabling them to remember and respond to user interactions and other changes over time.

#### Importing and Initializing useState
To use the `useState` hook, you first need to import it from the [[React]] library:
```Javascript
import { useState } from 'react';
```

You can then initialize state in your components by calling `useState` with and initial state value.
```Javascript
function FavoriteColor() {
 const [color, setColor] = useState('red');
 return <h1>My favorite color is {color}!</h1>;
}
```
In this example, `color` is the current state, and `setColor` is the function used to update the state

#### Updating State
To update the state, you use the state updater function returned by `useState`. This function can be called with a new state value or a function that computes the new state based on the previous state.
```Javascript
function FavoriteColor() {
 const [color, setColor] = useState('red');
 return (
   <>
     <h1>My favorite color is {color}!</h1>
     <button type="button" onClick={() => setColor('blue')}>Blue</button>
   </>
 );
}
```
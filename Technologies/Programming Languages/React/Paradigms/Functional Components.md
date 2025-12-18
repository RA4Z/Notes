In [[React]], Functional Components are plain JavaScript functions that return JSX. They are lightweight, easy to read and don't require as boilerplate as Class Components.

```Javascript
import React, { useState } from "react";
const Counter = () => {
 const [count, setCount] = useState(0);
 return (
   <div>
     <h2>{count}</h2>
     <button onClick={() => setCount(count + 1)}>Add</button>
   </div>
 );
};
export default Counter;
```

Use Functional Components for most modern [[React]] development due to simplicity and hooks
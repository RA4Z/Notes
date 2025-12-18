The **Virtual DOM** is a lightweight, in-memory representation of the **Real [[DOM]]** that [[React]] uses to optimize UI updates. Instead of directly manipulating the browser's [[DOM]], which is slow, [[React]] updates this virtual copy first, then efficiently syncs only the necessary changes to the real [[DOM]].

#### Example
When you click **Add**, [[React]] updates the Virtual DOM, detects that only the `<h2>` text changed, and updates just that node in the real [[DOM]]
```Javascript
import React, { useState } from 'react';
function Counter() {
 const [count, setCount] = useState(0);
 return (
   <div>
     <h2>Count: {count}</h2>
     <button onClick={() => setCount(count + 1)}>Add</button>
   </div>
 );
}
export default Counter;
```
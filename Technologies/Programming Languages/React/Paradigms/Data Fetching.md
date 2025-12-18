Fetching data from a local [[JSON]] file in [[React]] is a common task, especially during development or when working with mock data.

- **1. Place the JSON File**: Save the ``data.json`` file in the `public` directory of the [[React]] project. Files in the `public` folder can be accessed directly via their relative path.

- **2. Fetch Data Using Fetch API**: Use the `fetch` method to retrieve the [[JSON]] data asynchronously
```Javascript
import React, { useState, useEffect } from 'react';
function App() {
 const [data, setData] = useState([]);
 const fetchData = () => {
   fetch('/data.json', {
     headers: {
       'Content-Type': 'application/json',
       Accept: 'application/json',
     },
   })
     .then((response) => response.json())
     .then((jsonData) => setData(jsonData))
     .catch((error) => console.error('Error fetching data:', error));
 };
 useEffect(() => {
   fetchData();
 }, []);
 return (
   <div>
     <h1>Fetched Data</h1>
     {data.length > 0 ? (
       data.map((item, index) => <p key={index}>{item.name}</p>)
     ) : (
       <p>Loading...</p>
     )}
   </div>
 );
}
export default App;
```
- **3. Key Points**:
	- **Path to JSON File**: Use `/data.json` or `./data.json` depending on its location in the `public` directory.
	- **State Management**: Use `useState` to store and render the fetched data.
	- **Error Handling**: Always include error handling to debug issues during development

- **4. Alternative:** Use Axios
For more robust HTTP requests, you can use Axios:
```Powershell
npm install axios
``` 

```Javascript
import axios from 'axios';
const fetchData = async () => {
 try {
   const response = await axios.get('/data.json');
   setData(response.data);
 } catch (error) {
   console.error('Error fetching data:', error);
 }
};
```

Refs provide a way to access [[DOM]] nodes or [[React]] elements created in the render method. They are commonly used to manage focus, text selection or media playback.
#### Example Focusing a Text Input
In this example, clicking the button will focus the input:
```Javascript
import { useRef } from 'react';
export default function Form() {
 const inputRef = useRef(null);
 function handleClick() {
   inputRef.current.focus();
 }
 return (
   <>
     <input ref={inputRef} />
     <button onClick={handleClick}>Focus the input</button>
   </>
 );
}
```

#### Example Scrolling to an Element
You can have more than a single ref in a component. In this example, there is a carousel of three images. Each button centers and image by calling the browser `scrollIntoView()` method on the corresponding [[DOM]] node:
```Javascript
import { useRef } from 'react';
export default function CatFriends() {
 const firstCatRef = useRef(null);
 const secondCatRef = useRef(null);
 const thirdCatRef = useRef(null);
 function handleScrollToFirstCat() {
   firstCatRef.current.scrollIntoView({ behavior: 'smooth', block: 'nearest', inline: 'center' });
 }
 function handleScrollToSecondCat() {
   secondCatRef.current.scrollIntoView({ behavior: 'smooth', block: 'nearest', inline: 'center' });
 }
 function handleScrollToThirdCat() {
   thirdCatRef.current.scrollIntoView({ behavior: 'smooth', block: 'nearest', inline: 'center' });
 }
 return (
   <>
     <nav>
       <button onClick={handleScrollToFirstCat}>Neo</button>
       <button onClick={handleScrollToSecondCat}>Millie</button>
       <button onClick={handleScrollToThirdCat}>Bella</button>
     </nav>
     <div>
       <ul>
         <li><img src="https://placecats.com/neo/300/200" alt="Neo" ref={firstCatRef} /></li>
         <li><img src="https://placecats.com/millie/200/200" alt="Millie" ref={secondCatRef} /></li>
         <li><img src="https://placecats.com/bella/199/200" alt="Bella" ref={thirdCatRef} /></li>
       </ul>
     </div>
   </>
 );
}
```
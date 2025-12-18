In [[React]], Class Components are ES6 classes that extend `React.Component`. They manage state using `this.state` and update it with `this.setState()`. They use life-cycle methods like `componentDidMount` and `componentWillUnmount` instead of hooks. They are verbose and require method binding for event handlers. Class Components have more [[Boilerplate]] code than Functional Components.

```Javascript
import React, { Component } from "react";
class Counter extends Component {
 constructor() {
   super();
   this.state = { count: 0 };
   this.increase = this.increase.bind(this);
 }
 increase() {
   this.setState({ count: this.state.count + 1 });
 }
 render() {
   return (
     <div>
       <h2>{this.state.count}</h2>
       <button onClick={this.increase}>Add</button>
     </div>
   );
 }
}
export default Counter;
```

Use Class Components in legacy projects or when working with libraries that require them
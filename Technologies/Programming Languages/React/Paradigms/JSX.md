JSX **([[JavaScript]] XML)** is a **syntax extension for [[JavaScript]]** used in [[React]] to describe what the UI should look like. It looks similar to HTML, but it's not HTML, it's syntactic sugar that gets **compiled into plain [[JavaScript]]** calls to `React.createElement()` 

#### What is JSX?
- JSX allows you to write UI components in a declarative way:
```JSX
const element = <h1>Hello, world!</h1>;
```

- This is **not valid [[JavaScript]]** by itself, browsers can't run it directly
- Tools like **[[Babel]]** transform JSX into [[JavaScript]] that [[React]] understands

#### How JSX is transformed
When you write:
```JSX
const element = <h1 className="title">Hello</h1>;
```

[[Babel]] compiles it into:
```JS
const element = React.createElement(
  'h1',                     // type of element
  { className: 'title' },    // props
  'Hello'                    // children
);
```

#### React.createElement() explained
`React.createElement(type, props, ...children):`
- **type**: HTML tag name ('div', 'h1') or a [[React]] component
- **props**: An object containing attributes and event handlers
- **children**: Any nested elements or text

Example with nesting:
```JSX
const element = (
  <div>
    <h1>Hello</h1>
    <p>World</p>
  </div>
);
```

[[Babel]] turns it into:
```JS
const element = React.createElement(
  'div',
  null,
  React.createElement('h1', null, 'Hello'),
  React.createElement('p', null, 'World')
);
```
**JSON ( JavaScript Object Notation)** is a **lightweight, text-based format** for storing and exchanging data. It is **human-readable**, easy to write, and widely used for communication between servers and clients in web applications.

#### Core Structure
- **Objects**: Unordered sets of _name/value_ pairs enclosed in `{}`
- **Arrays**: Ordered lists of values enclosed in `[]`

#### Example
Values can be **strings, numbers, booleans, null, objects, arrays**. Strings must be in **double quotes**.
```JSON
{
 "name": "Alice",
 "age": 28,
 "skills": ["Python", "JavaScript", "SQL"],
 "isEmployed": true
}
```

#### Key Features
- **Human-readable** and compact
- **Supports nesting** of objects and arrays
- **Cross-language compatibility** for data exchange
- **Standard format** for APIs, configuration files and NoSQL databases like MongoDB

#### Common Use Cases
- **Web APIs**: RESTful services return JSON responses
- **Configuration files**: Many tools store settings in `.json` files
- **Data storage**: Used in document-oriented databases
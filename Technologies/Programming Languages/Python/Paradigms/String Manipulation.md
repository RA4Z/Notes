[[🐍Python]] provides a rich set of tools for **string manipulation**, allowing developers to perform operations like **slicing**, **formatting**, **searching**, and **transforming** strings efficiently.

### Basic String Operations
```Python
text = "Hello, World!"
# Convert to uppercase
print(text.upper()) # Output: "HELLO, WORLD!"
# Replace a substring
print(text.replace("World", "Python")) # Output: "Hello, Python!"
# Check if string starts with a specific substring
print(text.startswith("Hello")) # Output: True
# Split string into a list
print(text.split(", ")) # Output: ['Hello', 'World!']
```

### Common String Methods
- **``strip()``:**  Removes leading and trailing whitespace
```Python
s = " Python "
print(s.strip()) # Output: "Python"
```

- **``find()``:**  Finds the first occurrence of a substring
```Python
print("hello".find("e")) # Output: 1
```

- **``join()``:**  Joins elements of an iterable with a string separator
```Python
words = ["Python", "is", "fun"]
print(" ".join(words)) # Output: "Python is fun"
```

- **``split()``:**  Splits a string into a list based on a delimiter
```Python
sentence = "Learn Python Programming"
print(sentence.split()) # Output: ['Learn', 'Python', 'Programming']
```

- **``replace()``:**  Replaces occurrences of a substring with another
```Python
print("apples".replace("a", "o")) # Output: "opples"
```

### Advanced Techniques
- **String Slicing:**
```Python
s = "abcdef"
print(s[1:4]) # Output: "bcd"
```

- **String Formatting:**
```Python
name = "Alice"
age = 25
print(f"My name is {name} and I am {age} years old.")
# Output: "My name is Alice and I am 25 years old."
```

- **String Inverting**:
```Python
text = "Python"
inverted_text = text[::-1]
print(inverted_text) # Output: nohtyP
```
### Considerations
- Strings are **immutable** in [[🐍Python]], all operations return a new string
- Use ``re`` module for complex pattern matching and replacements
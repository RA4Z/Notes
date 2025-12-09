In Python, the **JSON** [[Packages|package]] is a built-in module for encoding and decoding [[JSON]] data. It's part of the standard library, so you don't need to install anything, just `import json`.

#### Functions in JSON
```Python
import json
json.dumps(obj)          # Convert a Python object to a JSON string
json.dump(obj, file)     # Write a Python object as JSON to a file
json.loads(json_str)     # Parse a JSON string into a Python object
json.load(file)          # Parse JSON from a file into a Python object
```

#### Example Usage
```Python
import json

# Python dictionary
data = {
    "name": "Alice",
    "age": 30,
    "is_admin": True,
    "skills": ["Python", "Machine Learning"],
    "projects": None
}

# 1. Convert Python object to JSON string
json_str = json.dumps(data, indent=4)  # indent for pretty printing
print("JSON String:\n", json_str)

# 2. Save JSON to a file
with open("data.json", "w", encoding="utf-8") as f:
    json.dump(data, f, indent=4)

# 3. Read JSON from a string
parsed_data = json.loads(json_str)
print("\nParsed from string:", parsed_data)

# 4. Read JSON from a file
with open("data.json", "r", encoding="utf-8") as f:
    file_data = json.load(f)
print("\nParsed from file:", file_data)
```
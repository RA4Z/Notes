It refers to an object whose **state or contents can be changed after creation**

Changes happen without creating a new object, the identity remains the same, it's efficient for frequent updates, since no new object is created

### Examples
- **Lists**: You can add, remove or modify elements
- **Dictionaries:** You can change values, add or remove keys
- **Sets:** You can add or remove elements
```Python
# Mutable example: list
my_list = [1, 2, 3]
my_list.append(4) # Add element
my_list[0] = 99 # Modify element
print(my_list) # [99, 2, 3, 4]
# Mutable example: dictionary
person = {"name": "Alice", "age": 30}
person["age"] = 31 # Modify value
person["city"] = "NY" # Add new key-value
print(person) # {'name': 'Alice', 'age': 31, 'city': 'NY'}
```

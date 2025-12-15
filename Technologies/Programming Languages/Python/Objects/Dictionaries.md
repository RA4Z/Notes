In [[🐍Python]], dictionaries are used to store data values in **key:value** pairs. They are one of the four [[Built-in Collections|built-in]] data types in [[🐍Python]] used to store collections of data. Dictionaries are created using curly brackets, with keys and values separated by a colon. Dictionaries are natively capable of [[Comprehensions]]. Dictionaries are [[Mutable]]

#### Creating a Dictionary
Dictionaries can be created by placing all the key:value pairs inside curly brackets `{}` separated by commas
```Python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
```

#### Dictionary Characteristics
- Ordered: The items have a defined order, and that order will not change
- Changeable: We can change, add and remove items in a dictionary after it has been created
- No Duplicate Keys: Dictionaries **cannot** have items with the same key (if duplicate keys are present, the last assignment wins)

#### Dictionary Length
To determine how many items a dictionary has, use the `len()` function
```Python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(len(thisdict))
```

#### Dictionary Items - Data Types
The values in dictionary items can be of any data type, and a dictionary can contain different data types for its values (keys are generally strings or numbers)
```Python
dict1 = {
  "name": "abc",
  "age": 34,
  "is_male": True,
  "weight": 40
}
print(dict1)
```

#### The dict() Contructor
It is also possible to use the `dict()` constructor to create a new dictionary
```Python
thisdict = dict(brand="Ford", model="Mustang", year=1964)
print(thisdict)
```

#### Looping Techniques
When looping through dictionaries, the key and corresponding value can be retrieved at the same time using the `items()` method.
```Python
knights = {'gallahad': 'the pure', 'robin': 'the brave'}
for k, v in knights.items():
    print(k, v)

# Output: gallahad the pure
# Output: robin the brave
```
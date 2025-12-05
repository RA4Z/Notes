In [[🐍Python]], sets are used to store multiple items in a single variable. They are one of the four [[Built-in Collections|built-in]] data types in [[🐍Python]] used to store collections of data. Sets are created using curly brackets. Sets are **not** natively capable of **Comprehensions**. Sets are [[Mutable]].

#### Creating a set
Sets can be created by placing all the items inside curly brackets `{}` separated by commas
```Python
thisset = {"apple", "banana", "cherry"}
print(thisset)
```

#### Set Characteristics
- Unordered: The items do **not** have a defined order, and you cannot refer to items by index or key
- Changeable: We can add and remove items in a set after it has been created (but cannot change existing items)
- No Duplicates: Sets **cannot** have items with the same value

#### Set Length
To determine how many items a set has, use the `len()` function
```Python
thisset = {"apple", "banana", "cherry"}
print(len(thisset))
```

#### Set Items - Data Types
Set items can be of any data type, and a set can contain different data types
```Python
set1 = {"abc", 34, True, 40, "male"}
print(set1)
```

#### The set() Constructor
It is also possible to use the `set()` constructor to create a new set
```Python
thisset = set(("apple", "banana", "cherry"))
print(thisset)
```

#### 🚨🚨Set Special Tip🚨🚨
It is possible to create a Set using a created list
```Python
list_data = [1, 2, 3, 3]
set_data = set(list_data)
print(set_data) # Output: [1, 2, 3]
```
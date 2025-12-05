In [[🐍Python]], lists are used to store multiple items in a single variable. They are one of the four [[Built-in Collections|built-in]] data types in [[🐍Python]] used to store collections of data. Lists are created using square brackets. Lists are natively capable of [[Comprehensions]], Lists are [[Mutable]].

#### Creating a list
Lists can be created by placing all the items inside square brackets `[]` separated by commas
```Python
thislist = ["apple", "banana", "cherry"]
print(thislist)
```

#### List Characteristics
- Ordered: The items have a defined order, and that order will not change
- Changeable: We can change, add and remove items in a list after it has been created
- Allow Duplicates: Lists can gave items with the same value

#### List Length
To determine how many items a list has, use the `len()` function
```Python
thislist = ["apple", "banana", "cherry"]
print(len(thislist))
```

#### List Items - Data Types
List items can be of any data type, and a list can contain different data types
```Python
list1 = ["abc", 34, True, 40, "male"]
print(list1)
```

#### The list() Constructor
It is also possible to use the `list()` constructor to create a new list
```Python
thislist = list(("apple", "banana", "cherry"))
print(thislist)
```
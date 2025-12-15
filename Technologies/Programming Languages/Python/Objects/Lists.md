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

#### List extend()
To merge lists in [[🐍Python]] is used the `extend()` method
```Python
main_list = []

list_1 = [1, 2, 3]
list_2 = [4, 5, 6]

main_list.extend(list_1)
main_list.extend(list_2)

print(main_list)  # Output: [1, 2, 3, 4, 5, 6]
```

#### List Slicing
To slice lists in [[🐍Python]] it's possible to use the following command:
```Python
main_list = [1, 2, 3, 4, 5]  
test_list1 = test_list[:2] 
test_list2 = test_list[2:]  
print(test_list1) # Output: [1, 2]
print(test_list2) # Output: [3, 4, 5]
```
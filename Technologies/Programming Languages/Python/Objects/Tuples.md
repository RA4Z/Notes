In [[🐍Python]], tuples are used to store multiple items in a single variable. They are one of the four [[Built-in Collections|built-in]] data types in [[🐍Python]] used to store collections of data. Tuples are created using round brackets. Tuples are **not** natively capable of **Comprehensions**. Tuples are [[Immutable]].

#### Creating a Tuple
Tuples can be created by placing all the items inside round brackets `()` separated by commas
```Python
thistuple = ("apple", "banana", "cherry")
print(thistuple)
```

#### Tuple Characteristics
- Ordered: The items have a defined order, and that order will not change
- Unchangeable: We **cannot** change, add or remove items in a tuple after it has been created
- Allow Duplicates: Tuples can have items with the same value

#### Tuple Length
To determine how many items a tuple has, use the ``len()`` function
```Python
thistuple = ("apple", "banana", "cherry")
print(len(thistuple))
```

#### Tuple Items - Data Types
Tuple items can be of any data type, and a tuple can contain different data types
```Python
tuple1 = ("abc", 34, True, 40, "male")
print(tuple1)
```

#### The tuple() Constructor
It is also possible to use the `tuple()` constructor to create a new tuple
```Python
thistuple = tuple(("apple", "banana", "cherry"))
print(thistuple)
```

### 🚨🚨Tuple Comprehension Special Tip🚨🚨
It is possible to create a Tuple Comprehension using [[Generator|Generators]], using parentheses to create a Comprehension Python will generate a [[Generator]] Comprehension, but calling the `tuple()` constructor it's possible.
```Python
generator_expression = (x * 2 for x in range(5))
my_tuple_comprehension = tuple(generator_expression)
```

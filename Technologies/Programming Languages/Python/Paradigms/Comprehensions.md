[[🐍Python]] comprehensions are a more Pythonic alternative to traditional loops for many common data manipulation tasks.

### Types of Comprehensions
- **List Comprehensions:** Used to create new lists
```Python
# Basic syntax: [expression for item in iterable]
squares = [x * x for x in range(10)]
print(squares) # Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# With a conditional filter: [expression for item in iterable if condition]
even_numbers = [x for x in range(20) if x % 2 == 0]
print(even_numbers) # Output: [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]

# With if-else: [expression_if_true if condition else expression_if_false for item in iterable]
grades = [75, 88, 42, 91, 65]
status = ["Passed" if g >= 60 else "Failed" for g in grades]
print(status) # Output: ['Passed', 'Passed', 'Failed', 'Passed', 'Passed']
```

- **Dictionary Comprehensions:** Used to create new dictionaries
```Python
# Basic syntax: {key_expression: value_expression for item in iterable}
numbers = [1, 2, 3, 4]
square_dict = {num: num * num for num in numbers}
print(square_dict) # Output: {1: 1, 2: 4, 3: 9, 4: 16}

# With a conditional filter
word_lengths = {"apple": 5, "banana": 6, "grape": 5, "kiwi": 4}
long_words = {word: length for word, length in word_lengths.items() if length > 4}
print(long_words) # Output: {'apple': 5, 'banana': 6, 'grape': 5}
```

- **Set Comprehensions:** Used to create new sets
```Python
# Basic syntax: {expression for item in iterable}
numbers = [1, 2, 2, 3, 4, 4, 5]
unique_squares = {x * x for x in numbers}
print(unique_squares) # Output: {1, 4, 9, 16, 25} (order may vary)

# With a conditional filter
letters = ['a', 'b', 'c', 'a', 'd', 'e', 'c']
unique_vowels = {char for char in letters if char in 'aeiou'}
print(unique_vowels) # Output: {'a', 'e'} (order may vary)
```

- **Nested List Comprehensions**: Used to create matrices
```Python
transposed = []
for i in range(4):
    transposed.append([row[i] for row in matrix])

print(transposed) # Output: [[1, 5, 9], [2, 6, 10], [3, 7, 11], [4, 8, 12]]
```
### Advantages of Comprehensions
- **Conciseness:** They allow you to write compact and readable code, often replacing multiple lines of loop-based code with a single line
- **Efficiency:** Comprehensions are often more efficient than equivalent **for** loops in Python, as they are optimized at a lower level
- **Readability:** When used appropriately, comprehensions can make your code easier to understand by clearly expressing the intent of the data transformation
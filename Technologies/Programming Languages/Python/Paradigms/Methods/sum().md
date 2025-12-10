Sum all the elements in a Python [[Built-in Collections|Built-in Collection]].

#### Basic Example
```Python
numbers = [1, 2, 3, 4, 5]
result = sum(numbers)
```

#### Condition Example
```Python
def sum_list(data_list, condition=None):
    """
    Sums the elements of a list based on an optional condition.

    :param data_list: List of numbers (int or float)
    :param condition: Function that takes an element and returns True if it should be summed
    :return: Sum of the elements that meet the condition
    """
    # Input validation
    if not isinstance(data_list, list):
        raise TypeError("The parameter 'data_list' must be of type list.")
    if condition is not None and not callable(condition):
        raise TypeError("The parameter 'condition' must be a function or None.")

    # Filter and sum
    if condition:
        return sum(x for x in data_list if isinstance(x, (int, float)) and condition(x))
    else:
        return sum(x for x in data_list if isinstance(x, (int, float)))


# ===== Usage Examples =====

numbers = [10, 15, 20, 25, 30]

# 1️⃣ Sum all elements
print(sum_list(numbers))  # Output: 100

# 2️⃣ Sum only numbers greater than 20
print(sum_list(numbers, condition=lambda x: x > 20))  # Output: 55

# 3️⃣ Sum only even numbers
print(sum_list(numbers, condition=lambda x: x % 2 == 0))  # Output: 60

```
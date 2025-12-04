In [[🐍Python]], ``*args`` and ``***kwargs`` are special syntax used in function definitions to allow for a variable number of arguments. Providing flexibility when designing functions that need to handle varying number of inputs.

### Args (Non-Keyword Arguments)
The `*args` syntax is used to pass a variable number of **positional arguments** to a functions. These arguments are packed into a tuple
```Python
def sum_numbers(*args):
   return sum(args)
print(sum_numbers(1, 2, 3)) # Output: 6
print(sum_numbers(4, 5, 6, 7)) # Output: 22
```
- `*args` is just a convention, it's possible to use any name

### Kwargs (Keyword Arguments)
The `**kwargs` syntax is used to pass a variable number of **keyword arguments** to a function. These arguments are packed into a dictionary
```Python
def print_details(**kwargs):
   for key, value in kwargs.items():
       print(f"{key}: {value}")
print_details(name="Alice", age=30, city="New York")
# Output:
# name: Alice
# age: 30
# city: New York
```
- `**kwargs` is just a convention, it's possible to use any name

### Using Both Args and Kwargs
You can use both `*args` and `**kwargs` in the same function to handle a mix of positional and keyword arguments
```Python
def mixed_arguments(*args, **kwargs):
   print("Positional arguments:", args)
   print("Keyword arguments:", kwargs)
mixed_arguments(1, 2, 3, name="Alice", age=30)
# Output:
# Positional arguments: (1, 2, 3)
# Keyword arguments: {'name': 'Alice', 'age': 30}
```

### Ordering
When defining a function the order of arguments must be:
- 1. Regular arguments
- 2. `*args`
- 3. `**kwargs`
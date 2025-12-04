In programming, a **function that calls itself** is called a **recursive function**

Example in Python:
```Python
def fibonacci(n):
    if n <= 0:
        return 0  # Base case
    elif n == 1:
        return 1  # Base case
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)  # Recursive case

# Example usage
num = 6
print(f"Fibonacci({num}) =", fibonacci(num))
```

### Key Points About Recursive Functions
- **Must have a base case** to avoid infinite recursion
- Each recursive call is stored in the **call stack** until it returns
- Can be **direct** (calls itself) or **indirect** (calls another function that calls it back)
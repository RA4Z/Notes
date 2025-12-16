The following [[🐍Python]] code will:
- `try`: try to execute a code
- `except`: print an error
- `else`: execute if any error occur
- `finally`: execute always at the end, whether if an error occur or not 
```Python
def divide(x, y):
    try:
        result = x / y
    except ZeroDivisionError:
        print("division by zero!")
    else:
        print("result is", result)
    finally:
        print("executing finally clause")
```
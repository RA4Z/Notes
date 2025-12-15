The `break` statement in [[🐍Python]] breaks out of the innermost enclosing `for` or `while` loop:

```Python
for n in range(2, 10):
    for x in range(2, n):
        if n % x == 0:
            print(f"{n} equals {x} * {n//x}")
            break
```
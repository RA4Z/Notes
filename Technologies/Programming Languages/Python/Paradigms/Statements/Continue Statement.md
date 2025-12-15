The `continue` statement in [[🐍Python]] continues with the next iteration of the loop:

```Python
for num in range(2, 10):
    if num % 2 == 0:
        print(f"Found an even number {num}")
        continue
    print(f"Found an odd number {num}")
```
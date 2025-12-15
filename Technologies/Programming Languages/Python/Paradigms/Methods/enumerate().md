In [[🐍Python]], when looping through a sequence, the position index and corresponding value can be retrieved at the same time using the `enumerate()` function.

```Python
for i, v in enumerate(['tic', 'tac', 'toe']):
    print(i, v)
    
# Output: 0 tic
# Output: 1 tac
# Output: 2 toe
```
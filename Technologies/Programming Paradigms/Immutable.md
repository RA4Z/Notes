Refers to programming practices where **data structures or objects cannot be modified after creation**. It results in the creation of a new object with the updated state.

Once create, the **state** of an immutable object remains constant. For example in Python, ``int``, ``str`` and ``tuple`` are immutable

```Python
t = (1, 2, 3)
# t[0] = 4 # ❌ Raises TypeError
```

Immutability improves safety, but can increase **memory usage** due to object copying.
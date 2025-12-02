[[Dunder]] method. makes an [[Object]] callable; When you call an ``object()`` the compiler translates to `obj.__call__()`.

```Python
class Testing():
    def __call__(self):
        print("Object is callable")
        
test = Testing()
test()
```

Output:
```Terminal
Object is callable
```

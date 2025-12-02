[[Dunder]] method.

Called before an object is about to be destroyed.

```Python
class Test():
    def __del__(self,):
        print("this is about to be destroyed")

test = Test()
del test

```

Output:
```Terminal
this is about to be destroyed
```

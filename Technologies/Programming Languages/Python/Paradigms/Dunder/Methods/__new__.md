[[Dunder]] method. Creates the Python object instance

```Python
class Test:
    def __new__(cls, *args, **kwargs):
        print("I'm called to create the instance")
        return super().__new__(cls)

    def __init__(self, name):
        self.name = name
        print("I'm called later to initialize attributes")

test = Test("test_name")
```

Output:

```
I'm called to create the instance
I'm called later to initialize attributes
```


[[Dunder]] method. Used to initialize the attributes to a Python object after it's created by [[__new__|new]]

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

```Terminal
I'm called to create the instance
I'm called later to initialize attributes
```
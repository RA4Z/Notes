In [[🐍Python]], **special methods** are also called **magic methods** or **Dunder methods**. The convention is to use double leading and trailing underscores in the name at hand, so it looks like ```.__method__()```. 

There are different ways to call them:
```Python
print(repr(a))
print(a.__repr__())
```

Everything in [[🐍Python]] is an object, behind the scenes, a sum happens as follows:
```Python
var = a + b
var = a.__add__(b)
```

The fundamental Python data (`int`, `list`, `dict`, `str`, ` tuple` and `object`) are written in C. Every native Dunder method were written in C in the CPython implementation.

Always when you use an operator or built-in function with one of these native methods, the respective Dunder method is executed with C code.

### 🚨🚨Don't call Dunder directly🚨🚨
You should define Dunder methods in [[Class|classes]] but shouldn't call them directly, it's usually best to let it be used by [[🐍Python]] internal functions. You don't ever call `__len__`, you call `len()`, which then calls `__len__`.
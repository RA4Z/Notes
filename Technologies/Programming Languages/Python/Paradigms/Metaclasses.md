In [[🐍Python]], metaclasses define how [[Class|classes]] are created and behave.

While a [[Class]] is a blueprint for creating objects, a metaclass is a blueprint for creating [[Class|classes]].

By default [[🐍Python]] uses the built-in `type` as the metaclass for all classes

When writing:
```Python
class MyClass:
	pass
```

[[🐍Python]] internally does:
```Python
MyClass = type('MyClass', (), {})
```

- Classes are objects, and metaclasses create these class objects
- You can customize class creation by defining your own metaclass

Metaclass to rename all non-dunder attributes to uppercase:
```Python
# Custom metaclass
class UpperAttrMetaclass(type):
   def __new__(cls, name, bases, attrs):
       uppercase_attrs = {
           attr if attr.startswith("__") else attr.upper(): val
           for attr, val in attrs.items()
       }
       return super().__new__(cls, name, bases, uppercase_attrs)
# Using the metaclass
class Foo(metaclass=UpperAttrMetaclass):
   bar = 'bip'
print(hasattr(Foo, 'BAR')) # True
print(Foo.BAR) # bip
```
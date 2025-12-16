[[🐍Python]] supports multiple inheritance, that means a [[Technologies/Programming Paradigms/Class]] can inherit from more than one parent [[Technologies/Programming Paradigms/Class]] 

```Python
class Base1:
   def feature1(self):
       print("Feature from Base1")
class Base2:
   def feature2(self):
       print("Feature from Base2")
class Derived(Base1, Base2):
   pass
   
obj = Derived()
obj.feature1() # From Base1
obj.feature2() # From Base2
```

When multiple parents define the same method, [[🐍Python]] uses the [[C3 Linearization Algorithm]] to determine the order in which classes are searched.

When working with multiple inheritance it's recommended to use `mro()` to debug and understand method lookup order
In [[Python]], decorators are a tool that allows developers to modify the behavior of a function or class without changing it's code. This is achieved by taking a function as an argument into another function and then calling it inside a wrapper function

### Creating a Decorator
A decorator is a function that takes another function as an argument, adds some functionality, and returns a new function
```Python
def make_pretty(func):
   def inner():
       print("I got decorated")
       func()
   return inner
@make_pretty
def ordinary():
   print("I am ordinary")
ordinary()
```
Output:
```Terminal
I got decorated
I am ordinary
```

### Decorators with Parameters
Decorators can also work with functions that take parameters
```Python
def smart_divide(func):
   def inner(a, b):
       print("I am going to divide", a, "and", b)
       if b == 0:
           print("Whoops! cannot divide")
           return
       return func(a, b)
   return inner
@smart_divide
def divide(a, b):
   print(a / b)
divide(2, 5)
divide(2, 0)
```
Output:
```Terminal
I am going to divide 2 and 5
0.4
I am going to divide 2 and 0
Whoops! cannot divide
```

### Chaining Decorators
Multiple decorators can be applied to a single function by stacking them. The order matters.
```Python
def star(func):
   def inner(*args, **kwargs):
       print("*" * 15)
       func(*args, **kwargs)
       print("*" * 15)
   return inner
def percent(func):
   def inner(*args, **kwargs):
       print("%" * 15)
       func(*args, **kwargs)
       print("%" * 15)
   return inner
@star
@percent
def printer(msg):
   print(msg)
printer("Hello")
```
Output:
```Terminal
***************
%%%%%%%%%%%%%%%
Hello
%%%%%%%%%%%%%%%
***************
```

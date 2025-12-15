In [[🐍Python]], small anonymous functions can be created with the `lambda` keyword. This function returns the sum of its two arguments: `lambda a, b: a+b`. They are syntactically restricted to a single expression. Semantically, they are just syntactic sugar for a normal function definition. They can reference variables from the containing scope.
```Python
def make_incrementor(n):  
    return lambda x: x + n  
  
f = make_incrementor(42)  
print(f(4))     # Output: 46  
print(f(1))     # Output: 43
```

The above example uses a lambda expression to return a function. Another use is to pass a small function as an argument. With the following code, the intention is to sort the list based on the content of the second item of each tuple (the string).
```Python
pairs = [(1, 'one'), (2, 'two'), (3, 'three'), (4, 'four')]
pairs.sort(key=lambda pair: pair[1])
print(pairs) # Output: [(4, 'four'), (1, 'one'), (3, 'three'), (2, 'two')]
```
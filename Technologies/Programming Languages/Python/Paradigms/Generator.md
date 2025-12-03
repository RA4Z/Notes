Generators in [[Python]] are a special type of function that allow you to produce a sequence of values over time, instead of computing them all at once and storing them in memory They are created using the ``yield`` keyword, which pauses the function's execution and retains its state, resuming from where it left off when called again. Generators are a type of [[Iterators]].

Generators are useful for tasks like streaming data or processing large files, because they produce values on demand.

```Python
def count_up_to(n):
   i = 1
   while i <= n:
       yield i
       i += 1
# Using the generator
for number in count_up_to(5):
   print(number)
```

### Generator Expressions
Generator expressions provide a concise way to create generators, similar to list comprehensions, but using parentheses instead of square brackets. They are more memory-efficient as they do not store all values in memory.

```Python
squares = (x**2 for x in range(5))
for square in squares:
   print(square)
```

### Advantages
They simplify code, reduce memory usage and improve performance. They are useful for tasks like [[Lazy Loading|lazy]] evaluation, pipeline processing and handling large or infinite datasets
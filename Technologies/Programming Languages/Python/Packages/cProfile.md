Is a built-in Python [[Packages|module]] designed for profiling Python code, primarily at the function level. It works by instrumenting your code to record detailed statistics about function calls and execution times.

- When `cProfile` is used to profile a section of code, it wraps the functions within that code, allowing it to intercept function calls and returns
- The output shows which functions consume the most time, allowing you to focus optimization efforts on those areas
- `cProfile` is a built-in module in Python and is often used with tools like [[pstats]] for analysis or [[SnakeViz]] for visualization 


```Python
import cProfile

def my_slow_function():
    sum(range(10**6))

cProfile.run('my_slow_function()')
```

It's possible to read the output using [[pstats]] directly from the ``cProfile``, or saving the output in a `.prof` file and reading it later

We use [[pstats]] library to **read the data output** from `cProfile` and we use [[SnakeViz]] to see the data in an **interactive, browser-based graphical visualization**.
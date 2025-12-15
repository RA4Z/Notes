In a `for` or `while` loop in [[🐍Python]], the [[Break Statement]] may be paired with an `else` clause. If the loop finishes without executing the `break`, the else clause executes.

In a `for` loop, the `else` clause is executed after the loop finishes its final iteration, that is, if no break occurred

In a `while` loop, it's executed after the loop's condition becomes false

In either kind of loop, the `else` clause is **not** executed if the loop was terminated by a `break`, if `return` or `raise exception` it will also skip execution of the `else` clause.

```Python
for n in range(2, 10):
    for x in range(2, n):
        if n % x == 0:
            print(n, 'equals', x, '*', n//x)
            break
    else:
        # loop fell through without finding a factor
        print(n, 'is a prime number')
```
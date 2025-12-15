A `match` statement in [[🐍Python]] takes an expression and compares its value to successive patterns given as one or more case blocks. It's similar to switch statement. Only the first pattern that matches gets executed and it can also extract components from the value into variables

```Python
def http_error(status):
    match status:
        case 400:
            return "Bad request"
        case 404:
            return "Not found"
        case 418:
            return "I'm a teapot"
		case 401 | 403 | 404:
		    return "Not allowed"
        case _:
            return "Something's wrong with the internet"
```

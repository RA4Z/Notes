In [[GDScript]], Coroutines allow pausing and resuming functions, useful for animations or delays
```Javascript
func wait_and_print():
   yield(get_tree().create_timer(2.0), "timeout")
   print("2 seconds passed")
```

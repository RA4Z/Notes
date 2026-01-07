In [[GDScript]], the `play_backwards()` method plays the animation with key `name` in reverse

```Javascript
void play_backwards(
	name: StringName = &"", 
	custom_blend: float = -1
)
```

This method is a shorthand for [[play()]], with `custom_speed = -1.0` and `from_end = true`
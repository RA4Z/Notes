It is a [[Virtual Method]] that is called every visual frame. `delta` is the time elapsed since the last frame. Use this for things that need to look smooth, like moving a camera or updating a timer. The frequency depends on the user's FPS

```Javascript
func _process(delta):
	if Input.is_action_pressed("ui_right"):
		# MOVE RIGHT
```
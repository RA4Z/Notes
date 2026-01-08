[[Virtual Method]] that only triggers if no UI element or other script "consumed" the input first. This is usually where you put player movement or gameplay actions

```Javascript
func _unhandled_input(event):
	if event is InputEventKey:
		if event.pressed and event.keycode == KEY_ESCAPE:
			get_tree().quit()
```

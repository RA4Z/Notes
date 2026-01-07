In [[GDScript]], the `play()` method plays the animation with key `name`

```Javascript
void play(
	name: StringName = &"", 
	custom_blend: float = -1, 
	custom_speed: float = 1.0, 
	from_end: bool = false
)
```

The `from_end` option only affects when switching to a new animation track, or if the same track but at the start or end. It does not affect resuming playback that was paused in the middle of an animation. If `custom_speed` is negative and `from_end` is `true`, the animation will play backwards (which is equivalent calling [[play_backwards()]])

The [[AnimationPlayer]] keeps track of its current or last played animation with [[assigned_animation]] if the `play()` method is called withe that same animation `name`, or with no `name` parameter, the assigned animation will resume playing if it was paused.
In [[GDScript]], the `pause()` method pauses the currently playing animation. The [[current_animation_position]] will be kept and calling [[play()]] or [[play_backwards()]] without arguments or with the same animation name as [[assigned_animation]] will resume the animation.

```Javascript
void pause()
```
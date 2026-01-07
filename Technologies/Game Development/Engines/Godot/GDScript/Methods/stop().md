In [[GDScript]] the `stop()` method stops the currently playing animation. The animation position is reset to `0` and the `custom_speed` is reset to `1.0`. if ``keep_state`` is `true`, the animation state is not updated visually

```Javascript
void stop(keep_state: bool = false)
```
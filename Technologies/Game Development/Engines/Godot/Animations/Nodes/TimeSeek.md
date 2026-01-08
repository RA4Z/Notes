In [[AnimationTree]], this node allows you to seek to a time in the animation to its in input. Use this node to play an `Animation` starting from a certain playback position. Note that the seek request value is measured in seconds, so if you would like to play an animation from the beginning, set the value to `0.0`, or if you would like to play an animation from 3 seconds in, set the value to `3.0`.

![[TimeSeek.png]]

```Javascript
# Play child animation from the start.
animation_tree.set("parameters/TimeSeek/seek_request", 0.0)

# Alternative syntax (same result).
animation_tree["parameters/TimeSeek/seek_request"] = 0.0

# Play child animation from 12 second timestamp.
animation_tree.set("parameters/TimeSeek/seek_request", 12.0)

# Alternative syntax (same result).
animation_tree["parameters/TimeSeek/seek_request"] = 12.0
```
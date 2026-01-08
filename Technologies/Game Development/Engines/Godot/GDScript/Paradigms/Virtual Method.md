In [[GDScript]] we have the **Virtual Methods**, that have a similar purpose than the [[Dunder]] methods in Python, the difference is that they use only a single underscore `_`. They are special functionas called automatically by the engine at specific times;

We have different purposes for each type of Virtual Method

- Lifecycle Methods -> Handle the "birth" and "death" of an object
- The Frame Loops -> Run every single frame
- Input Handling -> Methods that catch mouse clicks, key presses and joypad movements

Handle one-off events in [[_input(event)]] or [[_unhandled_input(event)]]. For instance, pressing P to pause the game.

Handle continuous events in [[_process(delta)]] or [[_physics_process(delta)]]. For instance, accelerating as long as the shift key is pressed.
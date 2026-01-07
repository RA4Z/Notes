In [[GDScript]] we have the **Virtual Methods**, that have a similar purpose than the [[Dunder]] methods in Python, the difference is that they use only a single underscore `_`. They are special functionas called automatically by the engine at specific times;

We have different purposes for each type of Virtual Method

- Lifecycle Methods -> Handle the "birth" and "death" of an object
- The Frame Loops -> Run every single frame
- Input Handling -> Methods that catch mouse clicks, key presses and joypad movements

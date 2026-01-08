When working with 3D animations, a popular technique is for animators to use the root skeleton bone in [[AnimationTree]] to give motion to the rest of the skeleton. This allows animating characters in a way where steps actually match the floor below. It also allows precise interaction with objects during cinematics.

When playing back the animation in Godot, it is possible to select this bone as the _root motion track_. Doing so will cancel the bone transformation visually (the animation will stay in place).
![[animtree_rootmotiontrack.webp]]

```Javascript
# Get the motion delta
animation_tree.get_root_motion_position()
animation_tree.get_root_motion_rotation()
animation_tree.get_root_motion_scale()

# Get the actual blended value of the animation
animation_tree.get_root_motion_position_accumulator()
animation_tree.get_root_motion_rotation_accumulator()
animation_tree.get_root_motion_scale_accumulator()
```

This can be fed to functions such as [[move_and_slide()]] to control the character movement.

There is also a tool node, `RootMotionView`, you can place a scene that will act as a custom floor for your character and animations (this node is disabled by default during the game).
![[animtree15.gif]]


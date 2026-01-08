In [[Godot]], **AnimationTree** is a node designed to deal with advanced transitions.

**AnimationTree** does not contain its own animations. It uses animations contained in an [[AnimationPlayer]] node. You create, edit, or import your animations in an [[AnimationPlayer]] and then use an [[AnimationTree]] to control the playback.
![[AnimationTreeExample.png]]

A new scene was created for the player with a [[CharacterBody3D]] as root. Inside this scene, the original `.dae` (Collada) file was instantiated and an **AnimationTree** node was created

To use an **AnimationTree**, you have to set a root node.
A few types of root nodes are available:

- `AnimationNodeAnimation`: Selects an animation from the list and plays it. This is the simplest root node, and generally not used as a root
- [[AnimationNodeBlendTree]]: Contains multiple nodes as children in a graph. Many blend nodes are available, such as mix, blend2, blend3, one shot, etc
- `AnimationNodeBlendSpace1D`: Allows linear blending between two animation nodes. Control the blend position in a 1D blend space to mix between animations
- `AnimationNodeBlendSpace2D`: Allows linear blending between three animation nodes. Control the blend position in a 2D blend space to mix between animations
- [[AnimationNodeStateMachine]]: Contains multiple nodes as children in a graph. Each node is used as a state, with multiple functions used to alternate between states

### Controlling from Code
After building the tree and previewing it, the only question remaining is "How is all this controlled from code?".

Keep in mind that the animation nodes are just resources, so they are shared between all instances using them. Setting values in the nodes directly will affect all instances of the scene that uses this `AnimationTree`. This is generally undesirable, but does have some cool use cases, e.g. you can copy and paste parts of your animation tree, or reuse nodes with a complex layout (such as a StateMachine or blend space) in different animation trees.

The actual animation data is contained in the `AnimationTree` node and is accessed via properties. Check the "Parameters" section of the `AnimationTree` node to see all the parameters that can be modified in real-time:
![[animtree_parameters.webp]]

This is handy because it makes it possible to animate them from an [[AnimationPlayer]], or even the `AnimationTree` itself, allowing very complex animation logic.

To modify these values from code, you must obtain the property path. You can find them by hovering your mouse over any of the parameters:
![[animtree_propertypath.webp]]

Then you can set or read them:
```Python
animation_tree.set("parameters/eye_blend/blend_amount", 1.0)
# Alternate syntax (same result)
animation_tree["parameters/eye_blend/blend_amount"] = 1.0
```
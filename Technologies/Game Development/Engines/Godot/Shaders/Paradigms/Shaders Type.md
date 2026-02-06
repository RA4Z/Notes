Every [[Shading Language|Shader]] need to declare what it will affect, there are 4 main types:

- `spatial`: For 3D objects
- `canvas_item`: For 2D objects (Sprites, UI, Control Nodes)
- `particles`: For particles systems
- `sky`: For renderize sky backgrounds and 3D environments

```C
shader_type spatial; // Define that this shader is for 3D
```
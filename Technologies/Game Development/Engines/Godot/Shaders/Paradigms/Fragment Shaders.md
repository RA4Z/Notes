Fragment shaders in [[Shading Language|Godot]] are specialized programs that run on the GPU to determine the color of each pixel com a rendered object.

In Godot, a fragment shader is defined within the _fragment()_ function. This function is executed for every pixel of the object being rendered. Here's a simple example:
```C
shader_type canvas_item;
void fragment() {
   COLOR = vec4(1.0, 0.0, 0.0, 1.0); // Sets every pixel to red
}
```

The _COLOR_ variable is used to output the final color of the pixel. It is represented as a _vec4_ (RGBA), where each component ranges from 0.0 to 1.0.
Vertex lighting in [[Shading Language|Godo Shaders]] involves calculating lighting at the vertices of a mesh and interpolating the results across the surface.

#### Implementing Vertex Lighting in Godot
To create a vertex lighting shader in Godot, you need to define a [[Shaders Type|Spatial]] shader and calculate the lighting in the `vertex()` function.
```C
shader_type spatial;
void vertex() {
   // Calculate light intensity based on the vertex normal and light direction
   vec3 light_dir = normalize(vec3(0.5, 1.0, 0.5)); // Example light direction
   float intensity = max(dot(NORMAL, light_dir), 0.0);
   // Pass the calculated intensity to the fragment shader using COLOR
   COLOR.rgb = vec3(intensity);
}
void fragment() {
   // Use the interpolated vertex color for the fragment's final color
   ALBEDO = COLOR.rgb;
}
```

- **`NORMAL`**: Represents the vertex normal, which is used to calculate how light interacts with the surface
- **`dot(NORMAL, light_dir)`**: Computes the angle between the light direction and the surface normal to determine light intensity
- **`COLOR`**: Passes the calculated intensity from the vertex shader to the fragment shader for rendering

#### Advantages of Vertex Lighting
- **Performance**: Vertex lighting is faster as it calculates lighting only at vertices, making it ideal for low-end devices.
- **Simplicity**: Easier to implement and debug compared to fragment lighting.

#### Limitations
- **Accuracy**: Lighting is less precise, especially on low-polygon meshes, as the interpolation may not capture fine details.
- **Shadows**: Vertex lighting may not support real-time shadows or advanced lighting effects.

#### Use Cases
Vertex lighting is suitable for:
- Games targeting older hardware or mobile platforms.
- Stylized visuals where lighting precision is not critical.
- Scenarios where performance is prioritized over visual fidelity.
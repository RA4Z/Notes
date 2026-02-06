In [[Shading Language]], `vec3` holds three floating-point numbers: (x, y, z) or (r, g, b).

#### **Common Uses:**
- **3D Positions/Offsets:** Storing a point in 3D space.
- **Directions/Normals:** Indicating which way a surface is facing.
- **Opaque Colors:** RGB values (Red, Green, Blue) without transparency.

#### **Example:**
```C
vec3 my_color = vec3(1.0, 0.5, 0.0); // Orange
vec3 normal = vec3(0.0, 1.0, 0.0);   // Pointing UP
```

#### Summary
- If you are working with **3D light/surface color (ALBEDO)**, use **vec3**.
- If you are working with **2D transparency or UI (COLOR)**, use **vec4**.
- If you are doing **3D math/positions**, use **vec3**.
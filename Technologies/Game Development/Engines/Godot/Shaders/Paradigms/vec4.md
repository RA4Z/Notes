In [[Shading Language]], `vec4` holds four floating-point numbers: (x, y, z, w) or (r, g, b, a).

#### **Common Uses:**
- **Transparent Colors:** RGBA (Red, Green, Blue, Alpha/Transparency).
- **Homogeneous Coordinates:** Used in matrix math (the w component helps with translations and projections).
- **Quaternions:** Used for rotations.

#### **Example:**
```C
vec4 transparent_red = vec4(1.0, 0.0, 0.0, 0.5); // 50% Transparent Red
```

#### Summary
- If you are working with **3D light/surface color (ALBEDO)**, use **vec3**.
- If you are working with **2D transparency or UI (COLOR)**, use **vec4**.
- If you are doing **3D math/positions**, use **vec3**.
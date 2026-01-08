Structs are compound types which can be used for better abstraction of shader code. You can declare them at the global scope like:
```C
struct PointLight {
    vec3 position;
    vec3 color;
    float intensity;
};
```

After declaration, you can instantiate and initialize them like:
```C
void fragment()
{
    PointLight light;
    light.position = vec3(0.0);
    light.color = vec3(1.0, 0.0, 0.0);
    light.intensity = 0.5;
}
```

Or use struct constructor for same purpose:
```C
PointLight light = PointLight(vec3(0.0), vec3(1.0, 0.0, 0.0), 0.5);
```

Structs may contain other struct or array, you can also instance them as global constant:
```C
shader_type spatial;

...

struct Scene {
    PointLight lights[2];
};

const Scene scene = Scene(PointLight[2](PointLight(vec3(0.0, 0.0, 0.0), vec3(1.0, 0.0, 0.0), 1.0), PointLight(vec3(0.0, 0.0, 0.0), vec3(1.0, 0.0, 0.0), 1.0)));

void fragment()
{
    ALBEDO = scene.lights[0].color;
}
```

You can also pass them to functions:
```C
shader_type canvas_item;

...

Scene construct_scene(PointLight light1, PointLight light2) {
    return Scene({light1, light2});
}

void fragment()
{
    COLOR.rgb = construct_scene(PointLight(vec3(0.0, 0.0, 0.0), vec3(1.0, 0.0, 0.0), 1.0), PointLight(vec3(0.0, 0.0, 0.0), vec3(1.0, 0.0, 1.0), 1.0)).lights[0].color;
}
```
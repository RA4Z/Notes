It is possible to define functions in a [[Shading Language|Godot Shader]]. They use the following syntax:
```C
ret_type func_name(args) {
    return ret_type; // if returning a value
}

// a more specific example:

int sum2(int a, int b) {
    return a + b;
}
```

You can only use functions that have been defined above (higher in the editor) the function from which you are calling them. 

Function arguments can have special qualifiers:
- **in**: Means the argument is only for reading (default).
- **out**: Means the argument is only for writing.
- **inout**: Means the argument is fully passed via reference.
- **const**: Means the argument is a constant and cannot be changed, may be combined with **in** qualifier.

Example below:
```C
void sum2(int a, int b, inout int result) {
    result = a + b;
}
```

Function overloading is supported. You can define multiple functions with the same name, but different arguments. Note that [implicit casting](https://docs.godotengine.org/en/stable/tutorials/shaders/shader_reference/shading_language.html#casting) in overloaded function calls is not allowed, such as from `int` to `float` (`1` to `1.0`).
```C
vec3 get_color(int t) {
    return vec3(1, 0, 0); // Red color.
}
vec3 get_color(float t) {
    return vec3(0, 1, 0); // Green color.
}
void fragment() {
    vec3 red = get_color(1);
    vec3 green = get_color(1.0);
}
```

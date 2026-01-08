In [[Shading Language]], Local Arrays are declared in functions. They can use all of the allowed datatypes, except samplers. The array declaration follows a C-style syntax: `[const] + [precision] + typename + identifier + [array size]`.

```C
void fragment() {
    float arr[3];
}
```

They can be initialized at the beginning like:
```C
float float_arr[3] = float[3] (1.0, 0.5, 0.0); // first constructor

int int_arr[3] = int[] (2, 1, 0); // second constructor

vec2 vec2_arr[3] = { vec2(1.0, 1.0), vec2(0.5, 0.5), vec2(0.0, 0.0) }; // third constructor

bool bool_arr[] = { true, true, false }; // fourth constructor - size is defined automatically from the element count
```

To access an array element, use the indexing syntax:
```C
float arr[3];

arr[0] = 1.0; // setter

COLOR.r = arr[0]; // getter
```

Arrays also have a built-in function `.length()` (not to be confused with the built-in `length()` function). It doesn't accept any parameters and will return the array's size.
```C
float arr[] = { 0.0, 1.0, 0.5, -1.0 };
for (int i = 0; i < arr.length(); i++) {
    // ...
}
```
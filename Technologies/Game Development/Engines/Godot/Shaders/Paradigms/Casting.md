The [[Shading Language]] implicit casting between scalars and vectors of the same size but different type is not allowed.

```C
float a = 2; // invalid
float a = 2.0; // valid
float a = float(2); // valid
```

Default integer constants are signed, so casting is always needed to convert to unsigned:
```C
int a = 2; // valid
uint a = 2; // invalid
uint a = uint(2); // valid
```

_ctypes_ is a built-in Python [[Packages|library]] that allows you to call functions from shared libraries or DLLs

## Steps
- Write your C code and compile it into a shared library (_.so_ on Linux or _.dll_ on Windows)
```C
#include <stdio.h>
void say_hello() {
   printf("Hello from C!\n");
}
```

- Use _ctypes_ in Python to load and call the function
```Python
import ctypes
# Load the shared library
lib = ctypes.CDLL('./example.dll')
# Call the function
lib.say_hello()
```

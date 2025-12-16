Common utility scripts often need to process command line arguments. These arguments are stored in the `sys` [[Python Standard Library|module]]'s `argv` attribute as a list.
```Python
# File demo.py
import sys
print(sys.argv)  # Output: ['demo.py', 'one', 'two', 'three']
```


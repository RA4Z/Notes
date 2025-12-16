`os` is a [[Python Standard Library]] that provides dozens of functions for interacting with the operating system:
```Python
import os
os.getcwd()      # Return the current working directory

os.chdir('/server/accesslogs')   # Change current working directory
os.system('mkdir today')   # Run the command mkdir in the system shell
```

Be sure to use the `import os` style instead of `from os import *`. This will keep `os.open()` from shadowing the built-in `open()` function which operates much differently.

The build-int `dir()` and `help()` functions are useful as interactive aids for working with large modules like `os`:
```Python
import os

dir(os) # returns a list of all module functions
help(os) # returns an extensive manual page created from the module's docstrings
```

For daily file and directory management tasks, the `shutil` module provides a higher level interface that is easier to use:
```Python
import shutil

shutil.copyfile('data.db', 'archive.db')  # archive.db
shutil.move('/build/executables', 'installdir')  # installdir
```
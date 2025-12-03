Is a Python [[Packages|library]] that provides an interactive, browser-based graphical visualization of data from [[cProfile]]

To use SnakeViz, we need to execute our code with [[cProfile]], after that we need to read our profile instance using [[pstats]] and then exporting this result in an `.prof` file.
After that procedure, we can run a command line in the `Terminal` calling snakeviz to read that file.

```Python
import cProfile
import pstats

def minha_funcao():
    # Seu código aqui
    pass

with cProfile.Profile() as profile:
    minha_funcao()

stats = pstats.Stats(profile)
stats.dump_stats("profile.prof")
```

```Terminal
snakeviz profile.prof
```

After that, a webpage will open with the data extracted from the cProfile visible in graphics format
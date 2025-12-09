`tqdm` is a Python [[Packages|library]] that provides a fast and extensible progress bar for loops and [[Iterators|Iterables]]. It is particularly useful for tracking the progress of long-running tasks.

#### Installation
To use `tqdm`, you need to install it first. Use the following command:
```Terminal
pip install tqdm
```

#### Example
```Python
from tqdm import tqdm
from time import sleep
# Simple progress bar for a loop
for i in tqdm(range(100), desc="Processing"):
   sleep(0.1) # Simulate work
```
This will display a progress bar in the terminal, showing the percentage completed, elapsed time and estimated time remaining

#### Key Features
- 1. **Custom Descriptions**: Add a description to the progress bar using the `desc` parameter
- 2. **Integration with Libraries**: Works seamlessly with libraries like Pandas, Jupyter Notebooks and more
- 3. **Manual Updates**: Use `tqdm.update(n)` to manually control progress when iterating over unknowns-length data

#### Example: Custom Description
```Python
from tqdm import tqdm
from time import sleep
for i in tqdm(range(50), desc="Downloading Files"):
   sleep(0.05)
```

#### Example: Pandas Integration
```Python
import pandas as pd
from tqdm import tqdm
tqdm.pandas(desc="Processing Data")
df = pd.DataFrame({'A': range(100)})
df['B'] = df['A'].progress_apply(lambda x: x**2)
```

#### Considerations
- **Performance**: `tqdm` has minimal overhead (~60ns/iteration)
- **Compatibility**: Works on all platforms (Linux, Windows, Mac) and supports Jupyter Notebooks via `tqdm.notebook`
- **Customization**: You can tweak appearance using parameters like `bar_format`, `colour` and more
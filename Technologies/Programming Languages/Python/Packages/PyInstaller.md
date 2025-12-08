PyInstaller is a Python [[Packages|Package]] that packages Python scripts into standalone executables for Windows, macOS and Linux without requiring a Python installation on the target system

```PowerShell
pip install pyinstaller
```
### Customization
It's possible to customize the build using various options:
- **--name** Specify the name of the output file
- **--add-data** Include additional data files
- **--icon** Add an icon to the executable

### Examples of use
```PowerShell
{python_path} -m PyInstaller main.py --onefile
```

```PowerShell

PyInstaller --onefile --name=my_app --add-data="config.cfg:." --icon=my_icon.ico my_script.py
```
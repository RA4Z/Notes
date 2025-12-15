In [[🐍Python]], the built-in _[[open()|open()]]_ function lets you specify the **text encoding** used when reading or writing files. If you don't specify _encoding_, [[🐍Python]] chooses a **platform-dependent default** based on your system's locale settings.

#### Syntax
```Python
open(file, mode='r', buffering=-1, encoding=None, errors=None, newline=None)
```
- **encoding:** Name of the character encoding (e.g. "utf-8", "latin-1", "cp1252")
- **errors:** How to handle encoding/decoding errors ('strict', 'ignore', 'replace', etc.)

#### Default Encoding
- On **most modern systems** (Linux, macOS, Windows 10+ with UTF-8 locale), the default if **UTF-8**
- On older Windows setups, it may default to a **code page** like "cp1252" or "mbcs"
- You can check your default with:
```Python
import locale
print(locale.getpreferredencoding(False))
```

#### Handling Errors
```Python
# Ignore characters that can't be decoded
with open("data.txt", "r", encoding="utf-8", errors="ignore") as f:
    text = f.read()

# Replace problematic characters with �
with open("data.txt", "r", encoding="utf-8", errors="replace") as f:
    text = f.read()
```
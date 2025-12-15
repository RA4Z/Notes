In [[🐍Python]], the **with statement** is used to ensure **proper acquisition and release of resources** 

It automatically handles setup and cleanup, making code cleaner and safer than using manual `try...finally` 

```Python
# Without 'with'
file = open("example.txt", "r")
try:
   content = file.read()
   print(content)
finally:
   file.close()
# With 'with'
with open("example.txt", "r") as file:
   content = file.read()
   print(content) # File closes automatically here
```

The _with_ statement in Python **ensures proper acquisition and release of resources** and **simplifies exception handling**, making it a best practice for resource management

It's possible to open multiple context managers in a single `with` statement, separated by commas
```Python
# Example: Opening two files at once
try:
    with open("file1.txt", "r") as f1, open("file2.txt", "w") as f2:
        for line in f1:
            f2.write(line.upper())
except FileNotFoundError as e:
    print(f"Error: {e}")

```

#### Inserting items in files using comprehension
```Python
result = sap.CN47N(lote_de_ordens)  
with open(f'{os.getcwd()}/database/CN47N/{uuid.uuid4()}.txt') as f:  
    header_line = ';'.join(result['header'])  
    content_block = '\n'.join([';'.join(row) for row in result['content']])  
    f.write(f"{header_line}\n{content_block}\n")
```
In [[🐍Python]] is possible to list all files in a directory, iterate through them and interact with them using the `os` [[Packages|Package]], together with the [[With Statement]] and [[open()]] is possible to read the content of the files

```Python
folder = os.path.join(os.getcwd(), 'database')
directory = os.listdir(folder)
for item in directory:
	full_path = os.path.join(folder, item)
	if os.path.isfile(full_path):
		with open(full_path, 'r', encoding='utf-8') as file:
			rows = [row for row in file.readlines()]
```
In [[🐍Python]], using [[Generator|Generators]], it's possible to create chunk lists, to iter through lists not all at once, but based on a param size

```Python
def chunk_list(data: list, size: int) -> Generator:
	return (data[i:i + size] for i in range(0, len(data), size))

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
for chunk in chunk_list(numbers, 2):
	print(chunk)
```
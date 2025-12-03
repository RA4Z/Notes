In [[Python]], **iterators** are objects that let run through collections of data one element per time, following the iteration protocol

### Iterator implements:
- ``__iter__()``: Return the iterator
- ``__next__()``: Return the next element or raise ``StopIteration`` if there are no more items

### Basic Example
```Python
nums = [1, 2, 3]
iterator = iter(nums)   # Convert the list in an iterator

print(next(iterator))   # 1
print(next(iterator))   # 2
print(next(iterator))   # 3
print(next(iterator))   # ❌ StopIteration
```

### **For** Looping uses Iterator
Behind the scenes, the for loop makes use of an iterator
```Python
for num in [1, 2, 3]:
	print(num)

# Equals to:
iterator = iter([1, 2, 3])
while True:
	try:
		num = next(iterator)
		print(num)
	except StopIteration:
		break
```
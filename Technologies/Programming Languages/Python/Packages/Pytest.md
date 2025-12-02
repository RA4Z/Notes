It's a Python open-source [[Testing]] [[Packages|Package]], designed to simplify the process of writing and running software tests

```Terminal
pip install pytest
```

Pytest automatically discovers test files and functions based on naming conventions

- Test files should start with ``test_`` or end with ``_test.py``
- Test functions withing these files should start with ``test_``
- Tests are written as regular Python functions using the ``assert`` keyword for verification

```Python
# test_example.py
def add(a, b):
	return a + b

def test_add_function():
	assert add(1, 2) == 3
	assert add(-1, 1) == 0
	assert add(0, 0) == 0
```

- To run tests, navigate to the directory containing your test files and type ``pytest``
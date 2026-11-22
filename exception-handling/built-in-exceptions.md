# Built-in Exceptions

Python provides many built-in exception classes.

## Common exceptions

- `Exception`: base class for ordinary exceptions
- `ValueError`: invalid value for an operation
- `TypeError`: invalid operation for a type
- `ZeroDivisionError`: division by zero
- `IndexError`: sequence index outside the valid range
- `KeyError`: missing dictionary key
- `FileNotFoundError`: file or directory does not exist
- `PermissionError`: operation lacks permission
- `RuntimeError`: unexpected runtime condition

```python
values = [10, 20]

try:
    print(values[5])
except IndexError as error:
    print("Index is invalid:", error)
```

Catch specific exceptions before broad exceptions. Avoid a bare `except:` unless a cleanup or final action truly requires it.

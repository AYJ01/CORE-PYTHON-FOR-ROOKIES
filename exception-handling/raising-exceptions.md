# Raising Exceptions

Use `raise` to signal an error explicitly.

```python
def divide(a, b):
    if b == 0:
        raise ZeroDivisionError("b cannot be zero")
    return a / b
```

## Re-raise the current exception

```python
try:
    value = int("invalid")
except ValueError:
    print("Logging the original error")
    raise
```

## Exception chaining

```python
try:
    int("invalid")
except ValueError as error:
    raise RuntimeError("Could not initialize configuration") from error
```

Use `raise ... from ...` to preserve the original cause. Validate inputs at appropriate boundaries rather than relying on exceptions for routine control flow.

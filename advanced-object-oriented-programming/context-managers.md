# Context Managers

Context managers manage setup and cleanup using `with`.

## File context manager

```python
with open("data.txt", "w") as file:
    file.write("Hello")
```

## Custom class-based context manager

```python
class ManagedResource:
    def __enter__(self):
        print("Resource opened")
        return self

    def __exit__(self, exc_type, exc_value, traceback):
        print("Resource closed")

with ManagedResource() as resource:
    print("Using resource")
```

## Context manager decorator

```python
from contextlib import contextmanager

@contextmanager
def managed_resource():
    print("Open")
    try:
        yield "resource"
    finally:
        print("Close")

with managed_resource() as resource:
    print(resource)

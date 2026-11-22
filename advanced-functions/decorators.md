# Decorators

A decorator is a function that adds behavior to another function.

```python
def log_call(function):
    def wrapper(*args, **kwargs):
        print("Calling", function.__name__)
        result = function(*args, **kwargs)
        print("Finished", function.__name__)
        return result

    return wrapper

@log_call
def add(a, b):
    return a + b

print(add(10, 20))
```

## Timing decorator

```python
import time

def timer(function):
    def wrapper(*args, **kwargs):
        start = time.perf_counter()
        result = function(*args, **kwargs)
        elapsed = time.perf_counter() - start
        print(f"Elapsed: {elapsed:.6f} seconds")
        return result

    return wrapper
```

## Preserving metadata

```python
from functools import wraps

def decorator(function):
    @wraps(function)
    def wrapper(*args, **kwargs):
        return function(*args, **kwargs)

    return wrapper
```

`functools.wraps` preserves the decorated function's name and documentation.

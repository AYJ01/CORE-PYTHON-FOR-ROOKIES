# Processes

Processes have separate memory spaces and can take advantage of multiple CPU cores for CPU-bound work.

```python
from concurrent.futures import ProcessPoolExecutor


def square(value: int) -> int:
    return value * value


with ProcessPoolExecutor(max_workers=4) as executor:
    results = list(executor.map(square, range(10)))

print(results)
```

Protect process entry points with `if __name__ == "__main__":` when launching processes on platforms that use spawn.

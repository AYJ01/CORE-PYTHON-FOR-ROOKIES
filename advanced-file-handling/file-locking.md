# File Locking

File locking coordinates access across processes. Python's standard library does not provide a fully portable locking API.

On Unix-like systems, `fcntl` can be used:

```python
import fcntl

with open("shared.txt", "a+", encoding="utf-8") as file:
    fcntl.flock(file.fileno(), fcntl.LOCK_EX)
    file.write("A protected update\n")
    file.flush()
    fcntl.flock(file.fileno(), fcntl.LOCK_UN)
```

On Windows, third-party packages or platform-specific APIs are commonly needed.

Always hold locks for the minimum necessary duration and release them in `finally` or through a context manager.

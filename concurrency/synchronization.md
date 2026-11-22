# Synchronization

Shared state requires synchronization to prevent races and inconsistent updates.

```python
from threading import Lock

lock = Lock()
items: list[str] = []


def add_item(item: str) -> None:
    with lock:
        items.append(item)
```

Threading primitives include locks, `RLock`, semaphores, events, and queues. Async programs use async-safe primitives or design work so state is owned by a single task.

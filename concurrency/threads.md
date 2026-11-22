# Threads

Threads run within one Python process. They are useful for I/O-bound tasks, but the global interpreter lock can limit CPU-bound Python bytecode execution.

```python
from concurrent.futures import ThreadPoolExecutor


def download(url: str) -> str:
    return f"downloaded {url}"


urls = ["https://example.com/a", "https://example.com/b"]

with ThreadPoolExecutor(max_workers=4) as executor:
    results = list(executor.map(download, urls))

print(results)
```

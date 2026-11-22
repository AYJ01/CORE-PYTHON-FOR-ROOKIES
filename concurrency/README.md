# Concurrency

Concurrency allows multiple tasks to make progress during overlapping periods. It is useful for I/O-bound work, while parallelism is the main way to execute CPU-bound work on multiple cores.

## Navigation

- [Repository README](../README.md)
- [Concurrency](README.md)
- [Threads](threads.md)
- [Processes](processes.md)
- [AsyncIO](asyncio.md)
- [Synchronization](synchronization.md)
- [Practical questions](practical-questions.md)

## Example

```python
import asyncio


async def fetch(name: str) -> str:
    await asyncio.sleep(0.25)
    return f"completed {name}"


async def main() -> None:
    results = await asyncio.gather(fetch("first"), fetch("second"))
    print(results)


asyncio.run(main())
```

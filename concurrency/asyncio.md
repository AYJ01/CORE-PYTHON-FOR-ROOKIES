# AsyncIO

`asyncio` coordinates tasks that perform asynchronous I/O without creating a thread for every operation.

```python
import asyncio


async def work(name: str) -> str:
    await asyncio.sleep(1)
    return name


async def main() -> None:
    tasks = [asyncio.create_task(work("A")), asyncio.create_task(work("B"))]
    print(await asyncio.gather(*tasks))


asyncio.run(main())
```

Use `await` for coroutine operations and avoid blocking calls in the event-loop thread.

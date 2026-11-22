# Async Networking

Async networking lets one event loop manage many slow connections. Use `asyncio.StreamReader` and `StreamWriter` for line-oriented or framed protocols.

```python
import asyncio


async def handle_client(
    reader: asyncio.StreamReader,
    writer: asyncio.StreamWriter,
) -> None:
    try:
        while True:
            line = await reader.readline()
            if not line:
                break

            writer.write(b"echo: " + line)
            await writer.drain()
    finally:
        writer.close()
        await writer.wait_closed()


async def main() -> None:
    server = await asyncio.start_server(handle_client, "127.0.0.1", 9000)
    async with server:
        await server.serve_forever()


asyncio.run(main())
```

Never perform blocking DNS, file, or HTTP calls in the event-loop thread.

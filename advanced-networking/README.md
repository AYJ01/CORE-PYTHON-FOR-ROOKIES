# Advanced Networking

Advanced networking builds on basic sockets and HTTP by covering secure transport, protocol design, asynchronous I/O, multiplexing, and resilient network clients.

## Navigation

- [Repository README](../README.md)
- [Advanced networking](README.md)
- [TLS](tls.md)
- [Async networking](async-networking.md)
- [Protocol design](protocol-design.md)
- [Practical questions](practical-questions.md)

## Example

```python
import asyncio


async def fetch(reader: asyncio.StreamReader, writer: asyncio.StreamWriter) -> None:
    writer.write(b"PING\n")
    await writer.drain()

    data = await reader.readuntil(b"\n")
    print(data.decode().strip())

    writer.close()
    await writer.wait_closed()


async def main() -> None:
    reader, writer = await asyncio.open_connection("127.0.0.1", 9000)
    await fetch(reader, writer)


asyncio.run(main())
```

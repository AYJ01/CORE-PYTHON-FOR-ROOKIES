# Protocol Design

A network protocol specifies message boundaries, data formats, ordering, error handling, and versioning.

## Length-prefixed frame

```text
4-byte length | UTF-8 JSON payload
```

## Example parser

```python
import json
import struct


def encode_message(message: dict) -> bytes:
    payload = json.dumps(message, separators=(",", ":")).encode("utf-8")
    return struct.pack(">I", len(payload)) + payload


def decode_message(frame: bytes) -> dict:
    if len(frame) < 4:
        raise ValueError("Missing frame length")

    length = struct.unpack(">I", frame[:4])[0]
    payload = frame[4:]
    if len(payload) != length:
        raise ValueError("Incomplete frame")

    return json.loads(payload.decode("utf-8"))
```

Design for partial reads, oversized messages, malformed input, timeouts, cancellation, and backward-compatible version changes.

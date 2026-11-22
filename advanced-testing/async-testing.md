# Async Testing

Use an async test plugin such as pytest-asyncio to test coroutine-based code.

```python
import pytest


async def fetch_status():
    return "ready"


@pytest.mark.asyncio
async def test_fetch_status():
    assert await fetch_status() == "ready"
```

Install the plugin:

```bash
python -m pip install pytest-asyncio
```

Keep async fixtures and event-loop behavior explicit to avoid leaking tasks between tests.

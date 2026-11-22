# Mocking

Mocking replaces external dependencies so tests remain focused and predictable.

```python
from unittest.mock import Mock

service = Mock()
service.fetch.return_value = {"temperature": 22}

result = service.fetch()
assert result["temperature"] == 22
service.fetch.assert_called_once_with()
```

## Patching a function

```python
from unittest.mock import patch


def get_time_label():
    return "Current time"


with patch("module.get_time_label", return_value="Noon"):
    assert get_time_label() == "Noon"
```

Mock network calls, clocks, databases, and file systems only where they are difficult or undesirable to use directly.

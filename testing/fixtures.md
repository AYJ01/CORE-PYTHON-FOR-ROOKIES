# Test Fixtures

Fixtures prepare test data or resources before tests run.

```python
import pytest


@pytest.fixture
def scores():
    return [72, 85, 91]


def test_average(scores):
    average = sum(scores) / len(scores)
    assert average == 82.66666666666667
```

Fixtures can also create temporary files or database connections.

```python
import json


def test_write_json(tmp_path):
    path = tmp_path / "result.json"
    path.write_text(json.dumps({"ok": True}), encoding="utf-8")

    assert json.loads(path.read_text(encoding="utf-8"))["ok"] is True
```

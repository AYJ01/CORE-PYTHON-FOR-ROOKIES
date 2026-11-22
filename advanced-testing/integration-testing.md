# Integration Testing

Integration tests verify that multiple components work together.

```python
from tempfile import TemporaryDirectory
from pathlib import Path


def export_report(directory, rows):
    path = Path(directory) / "report.txt"
    path.write_text("\n".join(rows), encoding="utf-8")


def test_export_report():
    with TemporaryDirectory() as directory:
        export_report(directory, ["name,score", "Asha,95"])

        report = Path(directory) / "report.txt"
        assert report.read_text(encoding="utf-8") == "name,score\nAsha,95"
```

Integration tests may use temporary databases or containers, but should avoid flaky external network services unless those services are the system under test.

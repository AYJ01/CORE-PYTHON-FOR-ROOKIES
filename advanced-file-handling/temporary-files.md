# Temporary Files

Use temporary files and directories for data that should not persist permanently.

```python
import tempfile

with tempfile.NamedTemporaryFile(mode="w", encoding="utf-8", delete=True) as file:
    file.write("temporary data")
    file.seek(0)
    print(file.read())
```

## Temporary directory

```python
from pathlib import Path
import tempfile

with tempfile.TemporaryDirectory() as directory:
    path = Path(directory) / "result.txt"
    path.write_text("done", encoding="utf-8")
    print(path)
```

Temporary resources are cleaned up automatically when their context ends.

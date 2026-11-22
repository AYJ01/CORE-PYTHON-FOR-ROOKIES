# Advanced File Handling

Advanced file handling covers buffering, low-level I/O, temporary files, archives, compression, and efficient processing of large files.

## Navigation

- [Repository README](../README.md)
- [Advanced File Handling](README.md)
- [File modes and encoding](file-modes-and-encoding.md)
- [Large files](large-files.md)
- [Temporary files](temporary-files.md)
- [Archives](archives.md)
- [Compression](compression.md)
- [File locking](file-locking.md)
- [Practical questions](practical-questions.md)

## Example

```python
from pathlib import Path

for path in Path("data").rglob("*.txt"):
    print(path)
```

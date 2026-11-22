# Large Files

Do not load an entire large file into memory unless it is necessary.

## Process line by line

```python
from pathlib import Path

for line in Path("large.log").open("r", encoding="utf-8"):
    if "ERROR" in line:
        print(line.rstrip())
```

## Stream fixed-size blocks

```python
with open("large.bin", "rb") as file:
    while chunk := file.read(64 * 1024):
        process(chunk)
```

Define `process` appropriately for the data format.

## Memory-mapped files

```python
import mmap

with open("large.bin", "r+b") as file:
    with mmap.mmap(file.fileno(), 0) as mapped:
        print(mapped[:20])
```

Memory mapping can be useful for random access, but the file must support the requested mapping mode.

# Archives

## ZIP archives

```python
from pathlib import Path
from zipfile import ZipFile

with ZipFile("documents.zip", "w") as archive:
    for path in Path("documents").glob("*.txt"):
        archive.write(path, arcname=path.name)

with ZipFile("documents.zip", "r") as archive:
    print(archive.namelist())
    archive.extractall("output")
```

## TAR archives

```python
import tarfile

with tarfile.open("documents.tar.gz", "w:gz") as archive:
    archive.add("documents", arcname="documents")

with tarfile.open("documents.tar.gz", "r:gz") as archive:
    archive.extractall("output")
```

Validate archive contents and use a safe extraction directory when handling untrusted archives.

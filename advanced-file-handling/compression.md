# Compression

## gzip

```python
import gzip

with open("data.txt", "rb") as source:
    with gzip.open("data.txt.gz", "wb") as destination:
        destination.write(source.read())

with gzip.open("data.txt.gz", "rb") as source:
    print(source.read())
```

## Streaming compression

```python
import gzip

with open("large.txt", "rb") as source:
    with gzip.open("large.txt.gz", "wb") as destination:
        for chunk in iter(lambda: source.read(64 * 1024), b""):
            destination.write(chunk)
```

## bzip2

```python
import bz2

compressed = bz2.compress(b"Python file handling")
print(bz2.decompress(compressed))
```

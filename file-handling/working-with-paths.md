# Working with Paths

Use `pathlib.Path` for platform-independent path operations.

```python
from pathlib import Path

path = Path("data") / "scores.txt"
print(path)
print(path.exists())
```

## Reading and writing

```python
path = Path("message.txt")
path.write_text("Hello", encoding="utf-8")
text = path.read_text(encoding="utf-8")
print(text)
```

## Directory operations

```python
folder = Path("output")
folder.mkdir(exist_ok=True)

for item in folder.iterdir():
    print(item.name)
```

## Pattern matching

```python
for text_file in Path(".").glob("*.txt"):
    print(text_file)
```

## Useful properties

```python
path = Path("data/scores.txt")
print(path.name)
print(path.suffix)
print(path.parent)
```

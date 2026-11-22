# Opening and Closing Files

Use `open()` to open a file and `with` to ensure it closes automatically.

```python
file = open("example.txt", "r", encoding="utf-8")
print(file.read())
file.close()
```

Preferred approach:

```python
with open("example.txt", "r", encoding="utf-8") as file:
    contents = file.read()
```

## Common modes

- `r`: read; fails if the file does not exist.
- `w`: write; creates or truncates the file.
- `a`: append; creates the file if needed.
- `x`: exclusive creation; fails if the file exists.
- `r+`: read and write.
- `b`: binary mode.

```python
with open("log.txt", "a", encoding="utf-8") as file:
    file.write("New log entry\n")

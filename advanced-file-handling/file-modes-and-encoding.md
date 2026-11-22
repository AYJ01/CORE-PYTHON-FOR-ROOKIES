# File Modes and Encoding

Text files require a consistent encoding. UTF-8 is normally the safest choice.

```python
with open("unicode.txt", "w", encoding="utf-8", newline="") as file:
    file.write("Hello — नमस्ते — 你好\n")

with open("unicode.txt", "r", encoding="utf-8") as file:
    print(file.read())
```

## Encoding errors

```python
with open("data.txt", "r", encoding="utf-8", errors="replace") as file:
    text = file.read()
```

## Buffering

```python
with open("large.log", "w", encoding="utf-8", buffering=1) as file:
    file.write("Line 1\n")
```

Line-buffered text writes flush at newlines. Buffering may be disabled with `buffering=0` for binary files.

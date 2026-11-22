# Binary Files

Binary mode is used for non-text data such as images and archives.

```python
with open("image.png", "rb") as source:
    data = source.read()

with open("copy.png", "wb") as destination:
    destination.write(data)
```

## Appending bytes

```python
with open("numbers.bin", "ab") as file:
    file.write(bytes([10, 20, 30]))
```

Always use binary mode for raw bytes; do not pass a text encoding or decode binary data in the same operation.

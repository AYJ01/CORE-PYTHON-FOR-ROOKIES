# File Handling

File handling enables Python programs to read, create, update, and delete files.

## Navigation

- [Repository README](../README.md)
- [File Handling](README.md)
- [Opening and closing files](opening-and-closing.md)
- [Text files](text-files.md)
- [Binary files](binary-files.md)
- [Working with paths](working-with-paths.md)
- [CSV and JSON](csv-and-json.md)
- [Practical questions](practical-questions.md)

## Basic example

```python
with open("example.txt", "w", encoding="utf-8") as file:
    file.write("Hello, Python!")

with open("example.txt", "r", encoding="utf-8") as file:
    contents = file.read()
    print(contents)
```

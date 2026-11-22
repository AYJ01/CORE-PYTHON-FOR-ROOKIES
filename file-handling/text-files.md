# Text Files

## Reading an entire file

```python
with open("data.txt", "r", encoding="utf-8") as file:
    text = file.read()
```

## Reading line by line

```python
with open("data.txt", "r", encoding="utf-8") as file:
    for line in file:
        print(line.rstrip("\n"))
```

## Reading a list of lines

```python
with open("data.txt", "r", encoding="utf-8") as file:
    lines = file.readlines()
```

## Writing text

```python
lines = ["Python\n", "File handling\n"]

with open("data.txt", "w", encoding="utf-8") as file:
    file.writelines(lines)
```

## Appending text

```python
with open("data.txt", "a", encoding="utf-8") as file:
    file.write("A new line\n")

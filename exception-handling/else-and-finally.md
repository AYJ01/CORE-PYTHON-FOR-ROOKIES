# Else and Finally

## `else`

Code in `else` runs only when no exception occurs.

```python
try:
    number = int(input("Number: "))
except ValueError:
    print("Invalid integer")
else:
    print("The square is", number ** 2)
```

## `finally`

Code in `finally` runs whether an exception occurred or not.

```python
try:
    file = open("data.txt", "r", encoding="utf-8")
    print(file.read())
except FileNotFoundError:
    print("File not found")
finally:
    if "file" in locals():
        file.close()
```

Using a context manager is normally preferred for file cleanup:

```python
try:
    with open("data.txt", "r", encoding="utf-8") as file:
        print(file.read())
except FileNotFoundError:
    print("File not found")
```

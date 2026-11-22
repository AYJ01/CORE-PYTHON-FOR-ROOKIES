# For Loops

A `for` loop visits every item in an iterable.

```python
names = ["Asha", "Ben", "Chen"]

for name in names:
    print(name)
```

## Range

```python
for number in range(5):
    print(number)

for number in range(2, 11, 2):
    print(number)
```

## Strings

```python
for character in "Python":
    print(character)
```

## Tuples and sets

```python
for value in (10, 20, 30):
    print(value)

for value in {"red", "green", "blue"}:
    print(value)
```

## Dictionaries

```python
student = {"name": "Asha", "score": 92}

for key in student:
    print(key)

for value in student.values():
    print(value)

for key, value in student.items():
    print(key, value)
```

## Nested loops

```python
for row in range(1, 4):
    for column in range(1, 4):
        print(row, column)
```

## Enumerate

```python
names = ["Asha", "Ben", "Chen"]

for index, name in enumerate(names, start=1):
    print(index, name)
```

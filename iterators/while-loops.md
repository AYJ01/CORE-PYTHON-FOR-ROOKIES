# While Loops

A `while` loop repeats while its condition remains true.

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

## Counting backward

```python
count = 5

while count > 0:
    print(count)
    count -= 1
```

## User input loop

```python
answer = ""

while answer.lower() != "quit":
    answer = input("Enter a command (quit to stop): ")
```

## Sentinel value

```python
total = 0
value = int(input("Enter a number (0 to stop): "))

while value != 0:
    total += value
    value = int(input("Enter a number (0 to stop): "))

print(total)
```

## Avoid infinite loops

Every `while` loop with a potentially false condition must ensure that a variable or state eventually changes:

```python
attempt = 0

while attempt < 3:
    print("Attempt", attempt + 1)
    attempt += 1
```

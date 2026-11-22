# Loop Control Statements

## Break

`break` exits the loop immediately.

```python
for number in range(1, 11):
    if number == 5:
        break
    print(number)
```

## Continue

`continue` skips the rest of the current iteration.

```python
for number in range(1, 6):
    if number == 3:
        continue
    print(number)
```

## Pass

`pass` performs no operation and is useful as a placeholder.

```python
for number in range(3):
    pass
```

## Else with loops

The loop `else` block runs when a loop finishes normally and not because of `break`.

```python
for number in range(2, 10):
    if number % 7 == 0:
        print("Found", number)
        break
else:
    print("No multiple of seven found")
```

## Infinite loop with break

```python
while True:
    command = input("Enter command: ")
    if command.lower() == "quit":
        break
```

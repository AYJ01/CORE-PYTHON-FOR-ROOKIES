# List Methods

## Adding elements

```python
items = ["A", "B"]
items.append("C")
items.insert(1, "X")
items.extend(["D", "E"])
```

## Removing elements

```python
items = ["A", "B", "C", "B"]
items.remove("B")
last = items.pop()
```

## Sorting and searching

```python
numbers = [3, 1, 4, 2]
numbers.sort()
numbers.reverse()

print(numbers.count(2))
print(numbers.index(4))
numbers.clear()
```

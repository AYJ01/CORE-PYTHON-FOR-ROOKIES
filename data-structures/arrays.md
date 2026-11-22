# Arrays in Python

An array stores elements in numbered positions. Python's built-in `list` is dynamic and provides an array-like interface, while `array.array` and libraries such as NumPy provide space-efficient or fixed-type alternatives.

## Theory

Each element has an index, usually starting at `0`. Random access calculates the location of an element directly. Insertion and deletion in the middle may shift later elements.

## Basic operations

```python
numbers = [10, 20, 30, 40]

print(numbers[0])       # 10
print(numbers[-1])      # 40

numbers.append(50)
numbers.insert(2, 25)
removed = numbers.pop(1)

print(numbers)
print(removed)
```

## Complexity

| Operation | Average / typical |
|---|---:|
| Index access | O(1) |
| Append | amortized O(1) |
| Pop from end | O(1) |
| Insert or delete in middle | O(n) |
| Search | O(n) |

Python lists may occasionally resize, but appending is amortized O(1).

## Fixed-type arrays

```python
from array import array

values = array("i", [1, 2, 3, 4])
values.append(5)
print(values)
```

Use `array.array` when compact storage and a single primitive element type matter. Use a Python list for general-purpose code.

## Example: remove duplicates

```python
def unique(values):
    result = []
    seen = set()

    for value in values:
        if value not in seen:
            seen.add(value)
            result.append(value)

    return result

print(unique([4, 2, 4, 1, 2]))
```

## Exercises

1. Reverse an array in place.
2. Find a maximum and minimum using one pass.
3. Rotate elements by `k` positions.
4. Merge two sorted arrays.
5. Remove duplicates from a sorted array.

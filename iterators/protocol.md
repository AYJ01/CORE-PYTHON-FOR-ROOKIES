# The Iterator Protocol

Python's iterator protocol consists of two methods:

- `__iter__()` returns the iterator object.
- `__next__()` returns the next value or raises `StopIteration`.

## Example

```python
class CountingIterator:
    def __init__(self, maximum):
        self.maximum = maximum
        self.current = 1

    def __iter__(self):
        return self

    def __next__(self):
        if self.current > self.maximum:
            raise StopIteration

        value = self.current
        self.current += 1
        return value

numbers = CountingIterator(5)
print(list(numbers))
```

`StopIteration` tells Python that iteration has ended.

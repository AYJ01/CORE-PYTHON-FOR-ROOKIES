# Custom Iterators

## Number iterator

```python
class NumberIterator:
    def __init__(self, start, end):
        self.current = start
        self.end = end

    def __iter__(self):
        return self

    def __next__(self):
        if self.current > self.end:
            raise StopIteration

        value = self.current
        self.current += 1
        return value

for number in NumberIterator(3, 7):
    print(number)
```

## Countdown iterator

```python
class Countdown:
    def __init__(self, start):
        self.current = start

    def __iter__(self):
        return self

    def __next__(self):
        if self.current < 0:
            raise StopIteration

        value = self.current
        self.current -= 1
        return value

print(list(Countdown(3)))
```

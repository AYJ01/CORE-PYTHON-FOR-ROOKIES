# Common Iterator Patterns

## Enumerating values

```python
names = ["Asha", "Ben", "Chen"]

for index, name in enumerate(names, start=1):
    print(index, name)
```

## Combining iterables

```python
names = ["Asha", "Ben"]
scores = [92, 88]

for name, score in zip(names, scores):
    print(name, score)
```

## Reversing and sorting iterables

```python
print(list(reversed([1, 2, 3])))
print(sorted({3, 1, 2}))
```

## Filtering and transforming

```python
numbers = range(1, 11)
evens = filter(lambda number: number % 2 == 0, numbers)
squared = map(lambda number: number ** 2, evens)

print(list(squared))
```

## Consuming iterators

```python
value = iter([10, 20, 30])
print(sum(value))
print(list(value))
```

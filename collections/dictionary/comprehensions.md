# Dictionary Comprehensions

## Create from a sequence

```python
names = ["Asha", "Ben", "Chen"]
lengths = {name: len(name) for name in names}
print(lengths)
```

## Filter entries

```python
scores = {"Asha": 92, "Ben": 65, "Chen": 88}
passing = {name: score for name, score in scores.items() if score >= 70}
print(passing)
```

## Transform values

```python
prices = {"pen": 10, "book": 100, "bag": 500}
tax_included = {item: price * 1.18 for item, price in prices.items()}
```

# Getting Started with pytest

Pytest is a popular testing framework that can discover tests written as functions or classes.

```python
# calculator.py
def add(a, b):
    return a + b

# test_calculator.py
def test_add():
    assert add(2, 3) == 5


def test_add_negative_numbers():
    assert add(-2, -3) == -5
```

Install pytest:

```bash
python -m pip install pytest
```

Run all discovered tests:

```bash
python -m pytest
```

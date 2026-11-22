# Pytest Parametrization

Parametrized tests run the same test logic with multiple input sets.

```python
import pytest


def is_even(number):
    return number % 2 == 0


@pytest.mark.parametrize("number", [0, 2, 4, 100])
def test_even_numbers(number):
    assert is_even(number)


@pytest.mark.parametrize(
    ("number", "expected"),
    [(1, False), (2, True), (3, False)],
)
def test_is_even(number, expected):
    assert is_even(number) is expected
```

Parameter names can be combined with data structures or dataclasses for larger cases.

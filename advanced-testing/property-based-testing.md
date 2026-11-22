# Property-Based Testing

Property-based tests generate many examples and verify general invariants.

```python
# Requires hypothesis
from hypothesis import given, strategies as st


@given(st.lists(st.integers()))
def test_sorted_output_remains_the_same_length(values):
    result = sorted(values)
    assert len(result) == len(values)


@given(st.lists(st.integers()))
def test_sorted_output_is_sorted(values):
    result = sorted(values)
    assert all(a <= b for a, b in zip(result, result[1:]))
```

Install Hypothesis:

```bash
python -m pip install hypothesis
```

Hypothesis may shrink a failing example to a minimal reproduction.

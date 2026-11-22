# Testing

Testing verifies that Python code behaves as expected and helps prevent regressions.

## Navigation

- [Repository README](../README.md)
- [Testing](README.md)
- [Assertions](assertions.md)
- [Writing unittest tests](unittest.md)
- [Getting started with pytest](pytest.md)
- [Test fixtures](fixtures.md)
- [Mocking](mocking.md)
- [Test discovery](test-discovery.md)
- [Practical questions](practical-questions.md)

## Example

```python
# calculator.py
def add(a, b):
    return a + b

# test_calculator.py
def test_add():
    assert add(2, 3) == 5
```

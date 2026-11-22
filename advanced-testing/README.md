# Advanced Testing

Advanced testing covers isolating dependencies, parametrizing cases, measuring coverage, testing asynchronous code, and automating quality checks.

## Navigation

- [Repository README](../README.md)
- [Advanced Testing](README.md)
- [Pytest parametrization](parametrization.md)
- [Async testing](async-testing.md)
- [Coverage](coverage.md)
- [Test doubles](test-doubles.md)
- [Integration testing](integration-testing.md)
- [Property-based testing](property-based-testing.md)
- [Practical questions](practical-questions.md)

## Example

```python
import pytest


@pytest.mark.parametrize(
    ("left", "right", "expected"),
    [(1, 2, 3), (-1, 1, 0), (0, 0, 0)],
)
def test_add(left, right, expected):
    assert left + right == expected
```

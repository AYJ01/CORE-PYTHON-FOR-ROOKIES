# Testing Practical Questions

1. Add assertions to a small function.
2. Write a failing test and fix the code.
3. Write a test for positive numbers.
4. Write a test for negative numbers.
5. Test an empty collection.
6. Test invalid input.
7. Create a `unittest.TestCase`.
8. Install and run pytest.
9. Use pytest fixtures.
10. Test with `tmp_path`.
11. Mock an external service.
12. Verify that a mock was called.
13. Use `assert_called_once_with()`.
14. Run one test file only.
15. Filter tests with `-k`.
16. Run tests in verbose mode.
17. Organize tests in a `tests/` directory.
18. Separate test data from test logic.
19. Explain the arrange-act-assert pattern.
20. Build a test suite that produces no failing tests.

## Arrange-Act-Assert

```python
def test_multiply():
    # Arrange
    a = 6
    b = 7

    # Act
    result = a * b

    # Assert
    assert result == 42
```

## Mini-project

Write tests for a small calculator module covering addition, subtraction, multiplication, division, and division by zero. Include both normal cases and edge cases.

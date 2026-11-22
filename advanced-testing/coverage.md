# Coverage

Coverage reports show which lines execute during tests.

```bash
python -m pip install coverage pytest-cov
python -m pytest --cov=src --cov-report=term-missing
```

Aim for meaningful coverage of branches and behaviors, not only a high percentage. A 100% coverage report does not prove that every requirement or edge case is correct.

## Configuration example

```toml
[tool.coverage.run]
branch = true
source = ["src"]

[tool.coverage.report]
fail_under = 80
show_missing = true
```

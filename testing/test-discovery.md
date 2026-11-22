# Test Discovery

## pytest discovery

Pytest commonly discovers files named:

- `test_*.py`
- `*_test.py`

Use descriptive test names beginning with `test_`.

```bash
python -m pytest
python -m pytest tests/test_calculator.py
python -m pytest -k "add"
python -m pytest -v
```

## unittest discovery

Place test modules in discoverable Python packages or directories:

```text
project/
├── calculator.py
└── tests/
    └── test_calculator.py
```

Run:

```bash
python -m unittest discover -s tests
```

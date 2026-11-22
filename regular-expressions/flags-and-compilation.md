# Flags and Compilation

## Compile a pattern

```python
import re

word_pattern = re.compile(r"\bpython\b", re.IGNORECASE)
print(word_pattern.findall("Python, python, and py") )
```

## Common flags

- `re.I` or `re.IGNORECASE`: case-insensitive matching
- `re.M` or `re.MULTILINE`: `^` and `$` work per line
- `re.S` or `re.DOTALL`: `.` matches newline
- `re.X` or `re.VERBOSE`: allows whitespace and comments in a pattern

```python
pattern = re.compile(r"""
    ^             # beginning of a line
    [A-Z]         # first letter
    [a-z]*        # remaining letters
    $             # end of a line
""", re.X)
```

Compile patterns used repeatedly for readability and reuse.

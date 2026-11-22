# Basic Patterns

## Common character patterns

- `.`: any character except newline
- `\d`: digit
- `\w`: word character
- `\s`: whitespace
- `[A-Za-z]`: character range
- `[^0-9]`: any character except a digit

## Quantifiers

- `*`: zero or more
- `+`: one or more
- `?`: zero or one
- `{n}`: exactly `n`
- `{n,}`: at least `n`
- `{n,m}`: between `n` and `m`

```python
import re

print(re.findall(r"\d+", "Room 12, aisle 5"))
print(re.findall(r"[A-Za-z]+", "Python 3.12"))
```

Use raw strings to avoid unnecessary escaping:

```python
pattern = r"\b[A-Z][a-Za-z]*\b"
```

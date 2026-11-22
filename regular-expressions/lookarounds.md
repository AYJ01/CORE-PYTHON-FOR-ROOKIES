# Lookarounds

Lookarounds assert that a pattern appears without consuming it.

## Positive lookahead

```python
import re

print(re.findall(r"\w+(?=\s+world)", "hello world"))
```

## Negative lookahead

```python
print(re.findall(r"\b\w+(?!ing\b)", "coding running walk"))
```

## Positive lookbehind

```python
print(re.findall(r"(?<=\$)\d+", "Items: $25 and $40"))
```

## Negative lookbehind

```python
print(re.findall(r"(?<!\d)\b[A-Za-z]+\b", "A1 test 42 words"))
```

Lookbehind patterns should have a fixed width in Python's standard `re` module.

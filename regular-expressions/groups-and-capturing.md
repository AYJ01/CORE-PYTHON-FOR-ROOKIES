# Groups and Capturing

## Capturing groups

```python
import re

match = re.search(r"(\d{4})-(\d{2})-(\d{2})", "Date: 2026-11-22")

if match:
    print(match.group(0))
    print(match.group(1))
    print(match.group(2))
    print(match.groups())
```

## Named groups

```python
match = re.search(r"(?P<year>\d{4})-(?P<month>\d{2})", "2026-11")

if match:
    print(match.group("year"))
    print(match.groupdict())
```

## Non-capturing groups

```python
match = re.search(r"(?:com|org)", "example.com")
```

Use non-capturing groups when grouping is needed without creating a separate capture.

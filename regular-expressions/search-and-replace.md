# Search and Replace

## Search

```python
import re

match = re.search(r"python", "Learn Python", re.IGNORECASE)
print(match.group())
```

## Match at the beginning

```python
print(re.match(r"Hello", "Hello, world"))
```

## Find all matches

```python
print(re.findall(r"\b\w+\b", "one two three"))
```

## Replace

```python
text = "Call 123-456-7890"
masked = re.sub(r"\d", "*", text)
print(masked)
```

## Replace with a function

```python
text = "Python3 and Python12"
converted = re.sub(r"\d+", lambda match: f"[{match.group()}]", text)
print(converted)
```

## Split

```python
parts = re.split(r"[,;]+", "one, two;three")
print(parts)

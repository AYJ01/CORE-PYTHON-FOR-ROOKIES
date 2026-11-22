# Function Annotations

Annotations document the expected types and return values of a function.

```python
def add(a: int, b: int) -> int:
    return a + b
```

## Collection annotations

```python
def average(numbers: list[float]) -> float:
    return sum(numbers) / len(numbers)
```

## Optional values

```python
from typing import Optional

def find_name(name: str) -> Optional[str]:
    if name:
        return name
    return None
```

## Modern union syntax

```python
def to_text(value: int | float) -> str:
    return str(value)
```

Annotations do not enforce runtime types. Tools and editors can use them for validation and suggestions.

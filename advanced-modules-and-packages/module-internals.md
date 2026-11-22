# Module Internals

Each loaded module is cached in `sys.modules`.

```python
import math
import sys

print(math is sys.modules["math"])
print(math.__name__)
print(math.__file__)
```

## Module attributes

- `__name__`: module name
- `__package__`: containing package
- `__spec__`: import specification
- `__file__`: source or compiled file path
- `__cached__`: bytecode cache path
- `__loader__`: loader implementation

Modules execute once per process on the first normal import unless explicitly reloaded.

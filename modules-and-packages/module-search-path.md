# The Module Search Path

Python looks for imported modules in a search path available through `sys.path`.

```python
import sys

for directory in sys.path:
    print(directory)
```

Typical locations include:

- The current script or notebook directory
- Environment-specific `site-packages` directories
- Python installation directories
- Paths supplied through `PYTHONPATH`

Do not fix import errors only by changing `sys.path` unless that behavior is intentional. Prefer correct project structure and environment setup.

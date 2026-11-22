# Package Initialization

`__init__.py` runs when a package is imported.

```python
# my_package/__init__.py
from .core import calculate

__all__ = ["calculate"]
print("my_package imported")
```

Keep initialization lightweight. Avoid expensive I/O, network calls, and circular imports in package initializers.

## Re-exporting public APIs

```python
# my_package/__init__.py
from .models import User
from .services import create_user

__all__ = ["User", "create_user"]
```

This lets users write:

```python
from my_package import User, create_user
```

# Dynamic Imports

Use `importlib` to load modules whose names are determined at runtime.

```python
import importlib

module_name = "json"
module = importlib.import_module(module_name)
print(module.dumps({"loaded": True}))
```

## Reloading a module

```python
import importlib
import sample_plugin

sample_plugin = importlib.reload(sample_plugin)
```

Dynamic loading is useful for plugins and optional integrations. Treat module names as untrusted input carefully, and avoid dynamic imports for ordinary, known dependencies.

# Namespace Packages

Namespace packages can span multiple directories without requiring `__init__.py` in every directory.

```text
site_a/acme/tools.py
site_b/acme/clients.py
```

With both directories on `sys.path`, the `acme` namespace can combine their contents:

```python
from acme import tools, clients
```

Namespace packages are useful for plugin ecosystems or independently distributed components. Do not mix namespace-package style with a regular package of the same name unless the layout is intentionally compatible.

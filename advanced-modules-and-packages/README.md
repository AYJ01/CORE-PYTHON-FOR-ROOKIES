# Advanced Modules and Packages

Advanced packaging topics help structure larger Python applications and distribute reusable libraries.

## Navigation

- [Repository README](../README.md)
- [Advanced Modules and Packages](README.md)
- [Package initialization](package-initialization.md)
- [Namespace packages](namespace-packages.md)
- [Dynamic imports](dynamic-imports.md)
- [Module internals](module-internals.md)
- [Distribution and publishing](distribution-and-publishing.md)
- [Practical questions](practical-questions.md)

## Basic example

```python
import importlib

module = importlib.import_module("json")
print(module.dumps({"python": True}))
```

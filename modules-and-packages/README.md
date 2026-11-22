# Modules and Packages

Modules and packages organize Python code into reusable components.

## Navigation

- [Repository README](../README.md)
- [Modules and Packages](README.md)
- [Creating modules](creating-modules.md)
- [Import styles](import-styles.md)
- [Python packages](python-packages.md)
- [The module search path](module-search-path.md)
- [Virtual environments](virtual-environments.md)
- [Practical questions](practical-questions.md)

## Module example

```python
# math_tools.py
def square(number):
    return number * number

# main.py
from math_tools import square

print(square(5))
```

# Python Packages

A package is a directory containing modules, usually including `__init__.py`.

```text
shop/
├── __init__.py
├── products.py
└── customers.py
```

```python
# shop/__init__.py
from .products import list_products

# main.py
from shop.products import list_products
```

Use subpackages for larger projects:

```text
shop/
├── __init__.py
├── catalog/
│   ├── __init__.py
│   └── products.py
└── billing/
    ├── __init__.py
    └── invoices.py
```

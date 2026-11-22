# Import Styles

## Import a module

```python
import math

print(math.sqrt(16))
```

## Import a specific name

```python
from math import sqrt

print(sqrt(16))
```

## Import with an alias

```python
import numpy as np

print(np.array([1, 2, 3]))
```

## Import every public name

```python
from math import *
```

Wildcard imports are generally discouraged because they hide name origins and may overwrite existing names.

## Relative imports

```python
from .helpers import format_name
```

Relative imports are used inside packages.

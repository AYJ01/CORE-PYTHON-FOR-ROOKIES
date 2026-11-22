# Treaps

A treap combines a binary search tree key and a heap priority. Random priorities make the expected tree height logarithmic.

## Node

```python
import random


class TreapNode:
    def __init__(self, key, priority=None):
        self.key = key
        self.priority = priority if priority is not None else random.random()
        self.left = None
        self.right = None


def rotate_right(root):
    child = root.left
    root.left = child.right
    child.right = root
    return child


def rotate_left(root):
    child = root.right
    root.right = child.left
    child.left = root
    return child


def insert(root, key):
    if root is None:
        return TreapNode(key)

    if key < root.key:
        root.left = insert(root.left, key)
        if root.left.priority > root.priority:
            root = rotate_right(root)
    elif key > root.key:
        root.right = insert(root.right, key)
        if root.right.priority > root.priority:
            root = rotate_left(root)

    return root
```

## Theory

The treap has two invariants:

- Search-tree order by key.
- Heap order by priority.

A deterministic priority seed can make behavior reproducible. Random priorities usually avoid adversarial key patterns.

## Complexity

Expected O(log n) insertion, search, deletion, and split operations.

## Uses

- Ordered sets and maps
- Persistent data structures
- Randomized algorithms
- Competitive programming

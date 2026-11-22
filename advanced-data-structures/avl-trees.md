# AVL Trees

An AVL tree is a self-balancing binary search tree. Its invariant requires the height difference of the left and right subtrees of every node to be at most one.

## Invariant

For every node:

```text
-1 <= height(left) - height(right) <= 1
```

## Node and rotations

```python
class AVLNode:
    def __init__(self, key):
        self.key = key
        self.left = None
        self.right = None
        self.height = 1


def height(node):
    return node.height if node else 0


def balance(node):
    return height(node.left) - height(node.right) if node else 0


def right_rotate(y):
    x = y.left
    middle = x.right

    x.right = y
    y.left = middle

    y.height = 1 + max(height(y.left), height(y.right))
    x.height = 1 + max(height(x.left), height(x.right))
    return x


def left_rotate(x):
    y = x.right
    middle = y.left

    y.left = x
    x.right = middle

    x.height = 1 + max(height(x.left), height(x.right))
    y.height = 1 + max(height(y.left), height(y.right))
    return y
```

## Insertion

```python
def insert(node, key):
    if node is None:
        return AVLNode(key)

    if key < node.key:
        node.left = insert(node.left, key)
    elif key > node.key:
        node.right = insert(node.right, key)
    else:
        return node

    node.height = 1 + max(height(node.left), height(node.right))
    factor = balance(node)

    if factor > 1 and key < node.left.key:
        return right_rotate(node)

    if factor < -1 and key > node.right.key:
        return left_rotate(node)

    if factor > 1 and key > node.left.key:
        node.left = left_rotate(node.left)
        return right_rotate(node)

    if factor < -1 and key < node.right.key:
        node.right = right_rotate(node.right)
        return left_rotate(node)

    return node
```

## Complexity

| Operation | Time | Space |
|---|---:|---:|
| Search | O(log n) | O(h) |
| Insert | O(log n) | O(h) |
| Delete | O(log n) | O(h) |
| Traversal | O(n) | O(h) |

## Common errors

- Updating height after an incorrect rotation.
- Forgetting to rebalance after insertion or deletion.
- Comparing node values with stale child pointers.
- Using recursion without a call-depth strategy for extreme input sizes.

## Practice

1. Implement deletion.
2. Count nodes in a height range.
3. Verify the AVL invariant recursively.
4. Compare AVL insertion with an ordinary binary search tree.

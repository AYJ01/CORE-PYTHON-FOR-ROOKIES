# Trees and Binary Trees

A tree is a hierarchical structure made of nodes. Unlike a linear structure, a node may have child nodes.

## Terminology

- Root: the top node
- Parent: a node with one or more children
- Child: a node directly below a parent
- Leaf: a node with no children
- Subtree: a node and all its descendants
- Depth: distance from the root
- Height: longest path from the node to a leaf

## Binary tree node

```python
class Node:
    def __init__(self, value, left=None, right=None):
        self.value = value
        self.left = left
        self.right = right


root = Node("A",
    Node("B", Node("D"), Node("E")),
    Node("C", right=Node("F")))
```

## Traversals

```python
def preorder(node):
    if node is None:
        return
    print(node.value)
    preorder(node.left)
    preorder(node.right)


def inorder(node):
    if node is None:
        return
    inorder(node.left)
    print(node.value)
    inorder(node.right)


def postorder(node):
    if node is None:
        return
    postorder(node.left)
    postorder(node.right)
    print(node.value)
```

## Common traversals

- Preorder: node, left, right
- Inorder: left, node, right
- Postorder: left, right, node
- Level order: breadth-first by level

## Exercises

1. Count nodes recursively.
2. Calculate tree height.
3. Check whether two trees are identical.
4. Print a level-order traversal.
5. Check whether a binary tree is balanced.

# Linked Lists in Python

A linked list stores elements in nodes. Each node contains a value and a reference to the next node.

## Theory

Unlike arrays, linked-list nodes do not need to occupy a contiguous memory block. This makes insertion and removal efficient at a known node, but indexing and searching require traversal.

## Singly linked list

```python
class Node:
    def __init__(self, value):
        self.value = value
        self.next = None


class LinkedList:
    def __init__(self):
        self.head = None

    def prepend(self, value):
        node = Node(value)
        node.next = self.head
        self.head = node

    def append(self, value):
        node = Node(value)

        if self.head is None:
            self.head = node
            return

        current = self.head
        while current.next is not None:
            current = current.next
        current.next = node

    def iter_values(self):
        current = self.head
        while current is not None:
            yield current.value
            current = current.next


items = LinkedList()
items.append("A")
items.append("B")
items.prepend("start")

print(list(items.iter_values()))
```

## Complexity

| Operation | Time |
|---|---:|
| Prepend | O(1) |
| Append | O(n), or O(1) with tail reference |
| Search | O(n) |
| Insert after a known node | O(1) |
| Remove after a known node | O(1) |
| Index access | O(n) |

## Exercises

1. Implement `find(value)`.
2. Delete the first matching node.
3. Reverse the list iteratively.
4. Detect a cycle.
5. Find the middle node.

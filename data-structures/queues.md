# Queues in Python

A queue is a First-In, First-Out (FIFO) structure. The first item added is the first item removed.

## Implementation with deque

```python
from collections import deque

queue = deque()
queue.append("first")
queue.append("second")

print(queue.popleft())
print(queue.popleft())
```

Do not use `list.pop(0)` for repeated queue operations. Removing index zero shifts every remaining element and takes O(n) time.

## Queue class

```python
class Queue:
    def __init__(self):
        self._items = deque()

    def enqueue(self, value):
        self._items.append(value)

    def dequeue(self):
        if self.is_empty():
            raise IndexError("dequeue from empty queue")
        return self._items.popleft()

    def front(self):
        if self.is_empty():
            raise IndexError("empty queue")
        return self._items[0]

    def is_empty(self):
        return len(self._items) == 0
```

## Complexity

With `deque`, enqueue and dequeue are O(1).

## Uses

- Task scheduling
- Print queues
- Breadth-first search
- Message processing
- Customer-service lines

## Exercises

1. Implement a circular queue.
2. Implement a queue using two stacks.
3. Reverse the first `k` queue items.
4. Perform breadth-first search on a graph.

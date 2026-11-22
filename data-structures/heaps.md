# Heaps and Priority Queues

A heap is a complete binary tree that preserves an ordering property. Python's `heapq` module implements a min-heap.

## Min-heap example

```python
import heapq

items = [8, 3, 5, 1, 9]
heapq.heapify(items)

print(heapq.heappop(items))
heapq.heappush(items, 2)
print(items)
```

## Priority queue

```python
import heapq

tasks = []
heapq.heappush(tasks, (2, "write docs"))
heapq.heappush(tasks, (1, "fix bug"))

while tasks:
    priority, task = heapq.heappop(tasks)
    print(priority, task)
```

## Theory

In a min-heap, every parent is less than or equal to its children. The smallest item is always at index zero.

For a max-heap, invert priorities or store negatives.

## Complexity

| Operation | Time |
|---|---:|
| Find minimum | O(1) |
| Heapify | O(n) |
| Push | O(log n) |
| Pop | O(log n) |

## Uses

- Priority scheduling
- Finding the K largest or smallest items
- Merging sorted sequences
- Dijkstra's shortest-path algorithm
- Median maintenance

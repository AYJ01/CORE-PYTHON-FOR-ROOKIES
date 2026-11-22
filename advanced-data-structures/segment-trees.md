# Segment Trees

A segment tree stores aggregate values for array ranges and supports efficient range queries and point or range updates.

## Theory

Each node represents an interval. The root represents the complete array. Children represent halves of the parent interval.

## Example: sum and point update

```python
class SegmentTree:
    def __init__(self, values):
        self.n = len(values)
        self.tree = [0] * (4 * self.n)
        self.build(values, 1, 0, self.n - 1)

    def build(self, values, node, left, right):
        if left == right:
            self.tree[node] = values[left]
            return

        middle = (left + right) // 2
        self.build(values, 2 * node, left, middle)
        self.build(values, 2 * node + 1, middle + 1, right)
        self.tree[node] = self.tree[2 * node] + self.tree[2 * node + 1]

    def query(self, query_left, query_right):
        return self._query(1, 0, self.n - 1, query_left, query_right)

    def _query(self, node, left, right, query_left, query_right):
        if query_right < left or right < query_left:
            return 0
        if query_left <= left and right <= query_right:
            return self.tree[node]

        middle = (left + right) // 2
        return (self._query(2 * node, left, middle, query_left, query_right)
                + self._query(2 * node + 1, middle + 1, right, query_left, query_right))

    def update(self, index, value):
        self._update(1, 0, self.n - 1, index, value)

    def _update(self, node, left, right, index, value):
        if left == right:
            self.tree[node] = value
            return

        middle = (left + right) // 2
        if index <= middle:
            self._update(2 * node, left, middle, index, value)
        else:
            self._update(2 * node + 1, middle + 1, right, index, value)

        self.tree[node] = self.tree[2 * node] + self.tree[2 * node + 1]


values = [1, 3, 5, 7, 9]
tree = SegmentTree(values)
print(tree.query(1, 3))
tree.update(2, 10)
print(tree.query(1, 3))
```

## Complexity

- Build: O(n)
- Point update: O(log n)
- Range query: O(log n)
- Range update with lazy propagation: O(log n)

## Variants

- Sum, minimum, maximum, or GCD
- Range assignment
- Range addition
- Count in a range
- 2D range structures

## Exercises

1. Adapt the tree for range minimum queries.
2. Implement range addition with lazy propagation.
3. Count elements at least as large as `x` in a range.
4. Build a 2D segment tree.

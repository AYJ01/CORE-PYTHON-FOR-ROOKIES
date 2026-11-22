# Fenwick Trees

A Fenwick tree, or binary indexed tree (BIT), stores prefix information and supports efficient prefix sums and point updates.

## Theory

Each index stores a partial sum. Incrementing the index moves to the next responsible position.

## Implementation

```python
class FenwickTree:
    def __init__(self, values):
        self.tree = [0] * (len(values) + 1)
        for index, value in enumerate(values, start=1):
            self.add(index, value)

    def add(self, index, delta):
        while index < len(self.tree):
            self.tree[index] += delta
            index += index & -index

    def prefix_sum(self, index):
        total = 0
        while index > 0:
            total += self.tree[index]
            index -= index & -index
        return total

    def range_sum(self, left, right):
        return self.prefix_sum(right) - self.prefix_sum(left - 1)


fenwick = FenwickTree([1, 3, 5, 7])
print(fenwick.range_sum(2, 4))
fenwick.add(2, 4)
print(fenwick.range_sum(2, 4))
```

## Complexity

- Build: O(n)
- Point update: O(log n)
- Prefix/range sum: O(log n)

## Segment tree versus Fenwick tree

Use a segment tree for more flexible range operations. Use a Fenwick tree when the operation is a prefix aggregate that supports an inverse, such as sum.

## Exercises

1. Count smaller elements after the current element.
2. Implement range addition and point query.
3. Compress coordinates before building the tree.
4. Find the largest index with prefix sum at most `target`.

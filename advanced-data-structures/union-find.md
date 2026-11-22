# Disjoint-Set / Union-Find

Union-find tracks elements partitioned into disjoint sets. It is useful for connectivity, cycle detection, and grouped components.

## Implementation

```python
class UnionFind:
    def __init__(self, size):
        self.parent = list(range(size))
        self.rank = [0] * size
        self.count = size

    def find(self, item):
        if self.parent[item] != item:
            self.parent[item] = self.find(self.parent[item])
        return self.parent[item]

    def union(self, first, second):
        first_root = self.find(first)
        second_root = self.find(second)

        if first_root == second_root:
            return False

        if self.rank[first_root] < self.rank[second_root]:
            first_root, second_root = second_root, first_root

        self.parent[second_root] = first_root

        if self.rank[first_root] == self.rank[second_root]:
            self.rank[first_root] += 1

        self.count -= 1
        return True

    def connected(self, first, second):
        return self.find(first) == self.find(second)
```

## Optimizations

- **Union by rank:** attach the shorter tree under the taller tree.
- **Union by size:** attach the smaller component under the larger component.
- **Path compression:** shorten every node visited during `find`.

## Complexity

With both optimizations, operations are nearly constant: amortized O(α(n)), where `α` is the inverse Ackermann function.

## Uses

- Kruskal's minimum spanning tree
- Detecting cycles in a graph
- Connected components
- Dynamic connectivity
- Image-region grouping

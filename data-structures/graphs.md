# Graphs in Python

A graph consists of vertices (nodes) and edges (connections).

## Graph types

- Directed or undirected
- Weighted or unweighted
- Cyclic or acyclic
- Dense or sparse

## Adjacency list

```python
graph = {
    "A": ["B", "C"],
    "B": ["A", "D"],
    "C": ["A", "D"],
    "D": ["B", "C"],
}

print(graph["A"])
```

## Breadth-first search

```python
from collections import deque


def bfs(graph, start):
    visited = {start}
    queue = deque([start])

    while queue:
        node = queue.popleft()
        print(node)

        for neighbor in graph[node]:
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append(neighbor)
```

## Depth-first search

```python
def dfs(graph, start, visited=None):
    if visited is None:
        visited = set()

    visited.add(start)
    print(start)

    for neighbor in graph[start]:
        if neighbor not not in visited:
            dfs(graph, neighbor, visited)

    return visited
```

## Complexity

For `V` vertices and `E` edges:

- Depth-first or breadth-first search: O(V + E)
- Adjacency matrix storage: O(V²)
- Adjacency-list storage: O(V + E)

## Exercises

1. Detect a cycle in a directed graph.
2. Find the shortest path in an unweighted graph.
3. Find connected components.
4. Implement Dijkstra's algorithm.
5. Detect whether a graph is bipartite.

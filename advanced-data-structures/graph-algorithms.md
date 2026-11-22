# Graph Algorithms

Advanced graph structures and algorithms handle shortest paths, minimum spanning trees, strongly connected components, and network flow.

## Dijkstra's shortest-path algorithm

```python
import heapq


def dijkstra(graph, start):
    distances = {node: float("inf") for node in graph}
    distances[start] = 0
    queue = [(0, start)]

    while queue:
        distance, node = heapq.heappop(queue)

        if distance != distances[node]:
            continue

        for neighbor, weight in graph[node]:
            candidate = distance + weight
            if candidate < distances[neighbor]:
                distances[neighbor] = candidate
                heapq.heappush(queue, (candidate, neighbor))

    return distances
```

Dijkstra requires non-negative edge weights.

## Strongly connected components

Tarjan's or Kosaraju's algorithm partitions a directed graph into strongly connected components. Each SCC is a set of nodes where every node is reachable from every other node.

## Minimum spanning tree

- Kruskal: sort edges and merge components with union-find.
- Prim: grow a tree using a priority queue.

Both find a minimum-weight spanning tree for an undirected, weighted graph.

## Network flow

Representing a graph as a flow network enables maximum-flow problems. Common techniques include Edmonds-Karp and Dinic's algorithm.

## Complexity

| Algorithm | Common complexity |
|---|---:|
| Dijkstra with binary heap | O((V + E) log V) |
| Bellman-Ford | O(VE) |
| Prim with binary heap | O(E log V) |
| Kruskal | O(E log E) |
| Strongly connected components | O(V + E) |

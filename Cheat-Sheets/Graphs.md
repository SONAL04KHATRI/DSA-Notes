# Graphs Cheat Sheet

## Representations
- **Adjacency Matrix** → `O(V^2)` space complexity.
- **Adjacency List** → `O(V + E)` space complexity.

## BFS Algorithm
```python
from collections import deque

def bfs(graph, start):
    queue = deque([start])
    visited = set()
    
    while queue:
        node = queue.popleft()
        if node not in visited:
            print(node)
            visited.add(node)
            queue.extend(graph[node])

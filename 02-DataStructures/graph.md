# 🌐 Graph

A **graph** is a structure containing a set of objects (**nodes** or **vertices**) where there can be **edges** between them. Edges may be **directed** or **undirected**, and **weighted** or not.

---

## 📘 Common Use Cases

- Social networks (friendship, followers)
- Routing between cities or servers
- Task scheduling with dependencies
- Game state transitions

---

## 📚 Graph Representations

- **Adjacency List:** `{u: [v1, v2]}`
- **Adjacency Matrix:** `matrix[u][v] = 1`
- **Hashmap of Hashmaps:** `{u: {v: weight}}`

For algorithm interviews, adjacency lists or hashmaps are most common.

---

## ⏱️ Time Complexity

| Algorithm        | Time Complexity |
| ---------------- | --------------- |
| DFS / BFS        | O(V + E)        |
| Topological Sort | O(V + E)        |

> `V` = number of vertices, `E` = number of edges

---

## ⚙️ Graph Traversal Techniques

### 🔍 Depth-First Search (DFS) – Recursive (Matrix)

```python
def dfs(matrix):
    if not matrix:
        return []

    rows, cols = len(matrix), len(matrix[0])
    visited = set()
    directions = ((0, 1), (0, -1), (1, 0), (-1, 0))

    def traverse(i, j):
        if (i, j) in visited:
            return
        visited.add((i, j))
        for d in directions:
            ni, nj = i + d[0], j + d[1]
            if 0 <= ni < rows and 0 <= nj < cols:
                traverse(ni, nj)

    for i in range(rows):
        for j in range(cols):
            traverse(i, j)
```

### 📤 Breadth-First Search (BFS) – Queue (Matrix)

```python
from collections import deque

def bfs(matrix):
    if not matrix:
        return []

    rows, cols = len(matrix), len(matrix[0])
    visited = set()
    directions = ((0, 1), (0, -1), (1, 0), (-1, 0))

    def traverse(i, j):
        queue = deque([(i, j)])
        while queue:
            x, y = queue.popleft()
            if (x, y) not in visited:
                visited.add((x, y))
                for d in directions:
                    nx, ny = x + d[0], y + d[1]
                    if 0 <= nx < rows and 0 <= ny < cols:
                        queue.append((nx, ny))

    for i in range(rows):
        for j in range(cols):
            traverse(i, j)
```

---

## 📐 Topological Sort (Kahn's Algorithm)

```python
def graph_topo_sort(num_nodes, edges):
    from collections import deque
    nodes, order, queue = {}, [], deque()
    for node_id in range(num_nodes):
        nodes[node_id] = { 'in': 0, 'out': set() }
    for node_id, pre_id in edges:
        nodes[node_id]['in'] += 1
        nodes[pre_id]['out'].add(node_id)
    for node_id in nodes:
        if nodes[node_id]['in'] == 0:
            queue.append(node_id)
    while queue:
        node_id = queue.pop()
        for out_id in nodes[node_id]['out']:
            nodes[out_id]['in'] -= 1
            if nodes[out_id]['in'] == 0:
                queue.append(out_id)
        order.append(node_id)
    return order if len(order) == num_nodes else None

# Example usage:
print(graph_topo_sort(4, [[0, 1], [0, 2], [2, 1], [3, 0]]))
```

---

## ⚠️ Corner Cases

- Empty graph
- One or two nodes
- Cycles or disconnected components
- Matrix boundaries (out-of-bounds)
- Revisiting visited nodes (track `visited`)

---

## 🎯 Tips

- Use `deque` in Python for O(1) pop from left (BFS).
- DFS uses recursion or stack; BFS uses queue.
- Check for cycles when needed.
- Graph may be **directed**, **undirected**, **weighted**, or **cyclic**.
- Some graphs may be represented as **2D grids**.

---

## 🧠 Summary

| Traversal | Uses                              | Structure              |
| --------- | --------------------------------- | ---------------------- |
| DFS       | Recursion/path-finding            | Stack                  |
| BFS       | Shortest path in unweighted graph | Queue                  |
| TopoSort  | Task/course scheduling            | Queue + indegree count |

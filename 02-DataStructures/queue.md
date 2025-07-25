# 🧠 Queue

A **queue** is a linear data structure that follows the **FIFO** (First In, First Out) principle.  
Elements are **enqueued** at the back and **dequeued** from the front.

---

## 🧾 Why Queues?

- Useful for managing order of processing tasks or events.
- Commonly used in **Breadth-First Search (BFS)**.
- Can be implemented with arrays, linked lists, or deque structures.

---

## ⏱️ Time Complexity (All O(1))

| Operation | Time |
| --------- | ---- |
| Enqueue   | O(1) |
| Dequeue   | O(1) |
| Front     | O(1) |
| Back      | O(1) |
| isEmpty   | O(1) |

> ⚠️ Note: If you use arrays/lists for queues, be cautious of O(n) cost for `pop(0)` in some languages.

---

## 🧪 Corner Cases

- Empty queue
- Queue with 1 item
- Queue with 2 items

---

## ⚙️ Key Techniques

### 🔁 BFS with Queue (Level Order Traversal)

```python
from collections import deque

queue = deque()
queue.append(root)  # enqueue

while queue:
    node = queue.popleft()  # dequeue
    # process node
    if node.left:
        queue.append(node.left)
    if node.right:
        queue.append(node.right)
```

---

## 💬 Tips for Interviews

- Prefer `deque` over list for efficient O(1) enqueue and dequeue in Python.
- In JS or languages without queue, clarify with the interviewer your implementation assumptions.
- Queue is ideal for problems that require processing in the order of arrival.

---

## 📌 Classic Applications

- Level order traversal in trees
- Topological sort (Kahn’s Algorithm)
- Dijkstra's algorithm (if priority queue not required)
- Simulation systems (printer queue, process scheduling)

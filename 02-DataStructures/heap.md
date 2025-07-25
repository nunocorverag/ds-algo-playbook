# 🐘 Heap

A **heap** is a complete binary tree used for **priority queue** operations.  
In interviews, it’s mainly used to get the **top K** smallest/largest elements efficiently.

---

## 🔢 Types

- **Min Heap**: smallest element at root
- **Max Heap**: largest element at root  
  👉 Python’s `heapq` is a **Min Heap** by default. Use negatives (`-val`) to simulate a Max Heap.

---

## ⏱️ Time Complexity

| Operation | Time     |
| --------- | -------- |
| Insert    | O(log n) |
| Remove    | O(log n) |
| Peek      | O(1)     |
| Heapify   | O(n)     |

---

## ⚙️ Key Techniques

### 📌 Top K Elements

```python
import heapq

def topK(nums, k):
    heap = []
    for n in nums:
        heapq.heappush(heap, n)
        if len(heap) > k:
            heapq.heappop(heap)
    return heap
```

👉 For **top K largest**, use **Min Heap** of size K  
👉 For **top K smallest**, invert values for Max Heap behavior

---

## 💡 When to Use

- "Top K" problems (e.g., frequent elements, largest/smallest K)
- Need to access/remove **min/max** efficiently
- Simulate a **priority queue**

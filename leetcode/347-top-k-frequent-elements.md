# 🧩 Problem: Top K Frequent Elements

## 📜 Description

> Given an integer array `nums` and an integer `k`, return the `k` most frequent elements. You may return the answer in **any order**.

## 💡 Idea

- Count the frequency of each number using a hashmap.
- Use either a **heap** (to get top k frequent quickly) or a **bucket sort** (to get linear time).
- These approaches are efficient in time and space for interview settings.

## 🔍 Strategy

- **Heap Approach**:
  - Use a max heap to keep track of the top k frequent elements.
  - Simulate max heap by inserting negative frequency.
  - Time: O(n log k), Space: O(n)
- **Bucket Sort Approach**:
  - Create a list of buckets where index = frequency.
  - Collect from highest to lowest frequency until k elements.
  - Time: O(n), Space: O(n)

## 🧠 Pseudocode (Heap)

1. Count frequencies with a hashmap.
2. Push (-freq, num) into the heap.
3. Pop k times to get k most frequent.

## ⏱️ Complexity

| Metric | Heap       | Bucket Sort |
| ------ | ---------- | ----------- |
| Time   | O(n log k) | O(n)        |
| Space  | O(n)       | O(n)        |

## 🧪 Edge Cases

- Fewer than k unique elements.
- All elements the same.
- Negative or zero values.

---

## 💻 Code (Heap)

```python
from collections import defaultdict
import heapq

class Solution:
    def topKFrequent(self, nums, k):
        counter = defaultdict(int)
        for n in nums:
            counter[n] += 1

        heap = []
        for key, val in counter.items():
            heapq.heappush(heap, (-val, key))

        res = []
        for _ in range(k):
            res.append(heapq.heappop(heap)[1])

        return res
```

## 💻 Code (Bucket Sort)

```python
from collections import defaultdict

class Solution:
    def topKFrequent(self, nums, k):
        counter = defaultdict(int)
        for n in nums:
            counter[n] += 1

        freq = [[] for _ in range(len(nums) + 1)]
        for num, count in counter.items():
            freq[count].append(num)

        res = []
        for i in range(len(freq) - 1, -1, -1):
            for num in freq[i]:
                res.append(num)
                if len(res) == k:
                    return res
```

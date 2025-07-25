# 🧠 Hash Table

A **hash table** (or **hash map**) is a data structure that maps **keys to values** using a **hash function** to compute an index.  
It enables fast access, insertion, and deletion — usually in **O(1)** average time.

---

## 🧾 Why Hash Tables?

- Avoid linear search by storing values using hash codes.
- Ideal when fast lookup or membership checking is required.
- Great for frequency counts, lookups, and grouping elements.

---

## ⏱️ Time Complexity (Average Case)

| Operation | Time | Notes                        |
| --------- | ---- | ---------------------------- |
| Search    | O(1) | Hash to find location        |
| Insert    | O(1) | Unless resizing is triggered |
| Remove    | O(1) |                              |

> ⚠️ Hash collisions and bad hash functions can degrade performance.

---

## ⚙️ Key Techniques

### 🔑 Key Lookup

```python
map = {}
map["apple"] = 3
value = map.get("apple", 0)
```

### 🔢 Frequency Count

```python
from collections import defaultdict
freq = defaultdict(int)
for num in nums:
    freq[num] += 1
```

### 🧮 Grouping Elements

```python
from collections import defaultdict
groups = defaultdict(list)
for word in words:
    key = ''.join(sorted(word))  # or use tuple of frequencies
    groups[key].append(word)
```

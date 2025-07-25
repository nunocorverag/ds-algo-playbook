# 🧠 Dynamic Programming

Dynamic Programming (DP) is used to solve **optimization problems** by breaking them down into **overlapping subproblems** and storing the results of subproblems to avoid recomputation.

---

## ⏱️ Time Complexity Pattern

| Pattern                | Time Complexity                |
| ---------------------- | ------------------------------ |
| Top-down (Memoization) | Often O(n) or O(n^2)           |
| Bottom-up (Tabulation) | Often O(n) or O(n^2)           |
| Optimized space        | Can be reduced to O(1) or O(k) |

---

## 🧩 Key Techniques

### ✅ Identify Subproblems

Break the problem into smaller overlapping pieces.

### 📦 Memoization (Top-down)

Recursive + cache

```python
from functools import lru_cache

@lru_cache(None)
def dp(i):
    # base case
    # recursive case
    return ...
```

### 📋 Tabulation (Bottom-up)

Build a table iteratively.

```python
dp = [0] * (n + 1)
for i in range(1, n + 1):
    dp[i] = ...
```

### 💡 Space Optimization

Use only what's necessary (e.g., two rows instead of full matrix).

---

## ⚠️ Common Pitfalls

- Not identifying overlapping subproblems.
- Missing base cases.
- Recomputing states due to lack of caching.
- Confusing top-down vs bottom-up flow.

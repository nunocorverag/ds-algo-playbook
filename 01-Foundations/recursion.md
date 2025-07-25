# 🔁 Recursion

Recursion is a method of solving problems where the solution depends on solving smaller subproblems of the same type.

---

## 🧱 Key Concepts

- A **recursive function** must have:
  1. A **base case** to stop recursion.
  2. A **recursive call** that breaks the problem down.

```python
# Fibonacci Example
def fib(n):
    if n <= 1:
        return n
    return fib(n - 1) + fib(n - 2)
```

- Recursion is used in problems like:
  - Tree Traversals
  - Backtracking (permutations, combinations)
  - Divide and Conquer (merge sort, binary search)
  - DFS on graphs or grids

---

## ⚠️ What to Watch Out For

- Always define a base case to prevent infinite recursion.
- Recursive calls use the **call stack**, so deep recursion may cause stack overflow.
- Avoid duplicate work with **memoization**.
- Know if your language supports **tail-call optimization (TCO)**.

---

## 🧪 Edge Cases

- `n = 0`, `n = 1` — make sure base cases handle these.
- Watch out for:
  - Overlapping subproblems
  - Duplicate work
  - Large inputs without memoization

---

## ⚙️ Technique: Memoization

Memoization stores results of previous calls to avoid redundant computations.

```python
# Memoized Fibonacci
memo = {}
def fib(n):
    if n in memo:
        return memo[n]
    if n <= 1:
        return n
    memo[n] = fib(n-1) + fib(n-2)
    return memo[n]
```

- Improves naive recursion from **O(2^n)** to **O(n)**
- Common in DP problems (top-down approach)

---

## ✅ Common Recursive Patterns

- **Combinations/Subsets**
- **Generate Parentheses**
- **Permutations**
- **Backtracking**
- **DFS/Binary Tree/Graph Traversal**

---

## 💡 Tips

- If each call only reduces by 1 (e.g. `f(n-1)`), you may need **1 base case**.
- If each call splits (e.g. `f(n-1) + f(n-2)`), you need **2 or more base cases**.
- Use recursion for **tree problems**, **exploration problems**, or when **generating all possibilities**.

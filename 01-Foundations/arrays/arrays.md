# 📦 Arrays

Arrays are fixed or dynamic containers of contiguous memory. They're the foundation of many interview questions and often appear combined with other topics (strings, DP, etc.).

---

## ✅ Advantages

- Fast access: O(1) by index.
- Compact memory layout.

## ⚠️ Disadvantages

- Insertion/removal (middle): O(n) due to shifting.
- Fixed-size (in some languages): resizing costs O(n).

---

## ⏱️ Time Complexity

| Operation     | Time     |
| ------------- | -------- |
| Access        | O(1)     |
| Search        | O(n)     |
| Binary Search | O(log n) |
| Insert/Remove | O(n)     |
| Insert at End | O(1)\*   |

\* Amortized in dynamic arrays (Python, JS, etc.)

---

## 🎯 Key Concepts

- **Subarray**: contiguous slice – `[3, 6, 1]`
- **Subsequence**: ordered but not necessarily contiguous – `[3, 1, 5]`

---

## ⚙️ Techniques

- **Sliding Window**: Fixed or variable-size window across the array.
- **Two Pointers**: Useful for merging, comparing, or traversing from both ends.
- **Reverse Traversal**: Traverse from the end if problem logic depends on “future” elements.
- **Precomputation**: Prefix sums/products for range queries.
- **In-place Hashing**: Use array indices to track presence (when elements are 1..n).

---

## ❗ Common Pitfalls

- Index out of bounds
- Duplicate elements
- Off-by-one errors
- Costly slicing/copying (`O(n)`) — avoid unless needed

---

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

### 🪟 Sliding Window

Process subarrays or substrings efficiently. Move two pointers in tandem to create a window and adjust it based on constraints.

- Fixed-size (e.g., maximum sum in subarray of size `k`)
- Variable-size (e.g., longest substring with unique characters)

### 🎯 Two Pointers

Useful for problems involving sorted arrays, merging, or bidirectional traversal.

- Move pointers inward or separately on different arrays
- Reduce nested loops to linear time

### 🔁 Right-to-Left Traversal

Scan from the end when future values impact the result (e.g., suffix max, monotonic stacks).

### 🧮 Precomputation

Use prefix sums, suffix products, or hash maps to optimize repeated queries or range-based operations.

### 🔢 Index as Hash Key (In-Place Hashing)

Modify the array itself to store state (e.g., negate at index `val - 1`) when values are in a known range (like `1..n`).

### 🔁 Multiple Passes Over the Array

Cleanly separate logic into multiple O(n) passes when a single pass becomes too complex.

### 🔃 Sorting the Array

Enables binary search, two-pointers, and greedy techniques. Beware of altering element order when it matters.

---

## ❗ Common Pitfalls

- Index out of bounds
- Duplicate elements
- Off-by-one errors
- Costly slicing/copying (`O(n)`) — avoid unless needed

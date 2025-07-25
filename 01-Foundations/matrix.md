# 🧠 Matrix Cheatsheet for Coding Interviews

A **matrix** is a 2D array. Matrix problems often relate to **dynamic programming** or **grid traversal**.

---

## 🧾 Why Matrices?

- Represent 2D spatial relationships or game states (e.g., Sudoku, Tic-Tac-Toe).
- Often used in DP problems with tabulation.
- May represent graphs where each cell has neighbors (top, bottom, left, right).

---

## ⚠️ Corner Cases

- Empty matrix (e.g., `matrix = []` or `matrix[0] = []`)
- 1×1 matrix
- Matrix with only one row or one column

---

## ⚙️ Common Techniques

### 📐 Creating a Matrix of Size N × M

```python
# Creates a zero-initialized matrix of same size as `matrix`
zero_matrix = [[0 for _ in range(len(matrix[0]))] for _ in range(len(matrix))]
```

### 🧭 Copying a Matrix

```python
copied_matrix = [row[:] for row in matrix]
```

### 🔁 Transposing a Matrix

```python
transposed = list(zip(*matrix))
```

Useful in games like Tic-Tac-Toe or Connect 4 to reuse horizontal checking logic for vertical checks.

---

## 🧪 Interview Tips

- Matrix traversal can be row-wise, column-wise, or both.
- Think of boundary checks: avoid `IndexError` on edges/corners.
- Know how to identify neighbors (4-way or 8-way adjacency).
- Consider visited state (especially for DFS/BFS).

---

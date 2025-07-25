# 🥞 Stack

A **stack** is a linear data structure that follows the **LIFO** (Last-In, First-Out) principle.

Elements are **pushed** onto the top of the stack and **popped** from the top — like a stack of plates.

---

## 📌 Why Use Stacks?

- Ideal for reversing operations.
- Useful for parsing expressions and validating syntax.
- Supports recursion and backtracking (e.g. Depth-First Search).

---

## ⏱️ Time Complexity

| Operation | Time |
| --------- | ---- |
| Top/Peek  | O(1) |
| Push      | O(1) |
| Pop       | O(1) |
| isEmpty   | O(1) |
| Search    | O(n) |

> ⚠️ Watch out for edge cases like popping from an empty stack.

---

## 🔍 Techniques

- **DFS** (recursive or iterative) often uses a stack.
- **Expression Evaluation** (e.g. parentheses matching, RPN).
- **Undo/Redo Operations** use two stacks.
- **Backtracking problems** (like maze solving, permutations).

---

## 🧪 Corner Cases

- Empty stack
- One or two elements
- Popping more times than pushed

# 🧠 Linked List

A **linked list** is a linear data structure where each element (node) points to the next, allowing **sequential traversal** without requiring contiguous memory.

---

## 🔍 Why Linked Lists?

✅ Efficient **insertion and deletion** at known positions — `O(1)`  
❌ Slower **access/search** — `O(n)` due to sequential traversal

---

## 🔗 Types of Linked Lists

- **Singly Linked List**: Each node points to the next.
- **Doubly Linked List**: Each node points to the next and previous.
- **Circular Linked List**: Last node points to the head (optional: prev of head to tail in doubly circular).

---

## ⏱️ Time Complexity

| Operation | Time | Note                       |
| --------- | ---- | -------------------------- |
| Access    | O(n) | Need to traverse from head |
| Search    | O(n) |                            |
| Insert    | O(1) | If position is known       |
| Delete    | O(1) | If position is known       |

---

## 🛠️ Common Routines

- Count nodes
- Reverse in-place
- Find middle (two-pointer)
- Merge two lists

---

## 📐 Corner Cases

- Empty list (`head = None`)
- One or two nodes only
- Cycles (clarify with interviewer)

---

## ⚙️ Key Techniques

### 1. Dummy Nodes (Sentinels)

- Add dummy at head/tail to simplify edge handling
- Helps avoid null checks and simplifies logic

### 2. Two Pointers

- **Find kth from last**: Move one pointer `k` steps ahead
- **Detect cycle**: Fast/slow pointer (Floyd’s algorithm)
- **Find middle**: Fast/slow pointer, slow is at middle when fast reaches end

### 3. Using Space (Avoid if Asked In-Place)

- Constructing a new list is simple but memory-heavy
- Most interviews prefer in-place modifications

---

## 🧹 Elegant Operations

- **Truncate**: Set `.next = None` at cutoff
- **Swap values**: Swap `.val` only (not `.next`)
- **Combine lists**: Link tail of one to head of another

---

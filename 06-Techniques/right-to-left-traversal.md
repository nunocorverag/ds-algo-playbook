# 🔁 Right-to-Left Traversal

Traversing an array or string from **right to left** can simplify problems where future values affect current logic.  
It's especially useful when:

- The output depends on elements to the **right**
- You're calculating suffix properties (like suffix max/min)
- Forward traversal leads to complex state management

---

## 🧠 When to Use

- When the problem asks for "next greater" or "next smaller" to the right
- When suffix data (e.g. product, sum, max) is required
- When simulating lookahead behavior

---

## ⏱️ Complexity

| Operation | Time | Space                           |
| --------- | ---- | ------------------------------- |
| Traversal | O(n) | O(1) or O(n) depending on usage |

---

## 🧪 Example Problems

- Daily Temperatures (next warmer day)
- Number of Visible People in a Queue
- Trapping Rain Water (right max tracking)
- Stock Span Problem (reverse processing)

---

## 📌 Tips

- Use reverse loops: `for (int i = n - 1; i >= 0; i--)`
- Combine with auxiliary arrays if needed (`rightMax[i]`, etc.)
- Works great with stacks or suffix arrays

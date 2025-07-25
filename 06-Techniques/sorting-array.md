# 🔃 Sorting the Array

Sorting can significantly simplify a problem or unlock more efficient solutions.  
A sorted array often enables **binary search**, **greedy decisions**, and **two-pointer techniques**.

---

## 🧠 When to Use

- You're allowed to reorder the elements
- Problem involves order, range, or proximity
- There's a need to reduce nested loops to linear time
- Binary search is a viable optimization

---

## ⏱️ Complexity

| Operation     | Time       |
| ------------- | ---------- |
| Sorting (std) | O(n log n) |
| Binary Search | O(log n)   |

---

## 📌 Tips

- Check if the array is already sorted
- For custom conditions, use a custom comparator
- Use stable sorting if order matters
- Sorting breaks original indexing — track indices if needed

---

## ⚠️ Caveats

- Don't sort if the **relative order** must be preserved
- Consider time/space limits — avoid sorting if `O(n log n)` is too slow

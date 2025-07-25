# 🔢 Index as Hash Key (In-Place Hashing)

When dealing with arrays containing values from a known range (like 1 to N), you can often use the array itself to store state — **without extra space**.

This is a powerful trick for achieving **O(1) space complexity**.

---

## 🧠 When to Use

- You’re given a range-limited array (e.g., values from 1 to N)
- You're asked to find duplicates, missing numbers, or frequencies
- Problem constraints specify O(1) space

---

## 🧰 Common Techniques

- **Negate the value at index (val - 1)** to mark presence
- **Swap values to correct index** (index sorting)
- **Mark out-of-range values with a sentinel (e.g., -1 or 0)**

---

## ⏱️ Complexity

| Operation     | Time | Space |
| ------------- | ---- | ----- |
| Scan & Modify | O(n) | O(1)  |

---

## 🧪 Example Problems

- First Missing Positive
- Find All Duplicates in an Array
- Cyclic Sort Variants
- Set Mismatch
- Find Numbers Disappeared in an Array

---

## 📌 Tips

- Always check value ranges before using index as a key
- Make sure not to overwrite needed values before using them
- Restore the original array if needed at the end

---

## ⚠️ Caveats

- May not work if values are not in the 1 to N range
- Only safe if modifications to input are allowed
- Be careful with 0-based vs 1-based indexing

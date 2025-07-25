# 🔁 Multiple Passes Over the Array

Sometimes solving a problem efficiently doesn't require doing everything in one pass.  
Doing **two or three simple linear passes** can often be cleaner and just as optimal as a complex one-pass solution.

---

## 🧠 When to Use

- You need prefix and suffix information
- First pass gathers data, second pass computes result
- A single pass is messy, hard to debug, or requires future knowledge

---

## 🧰 Typical Scenarios

- One pass to build state, another to consume it
- Left-to-right for one metric, right-to-left for another
- Passes for accumulating data (like min/max, frequencies)

---

## ⏱️ Complexity

| Operation        | Time | Space        |
| ---------------- | ---- | ------------ |
| Two/Three Passes | O(n) | O(1) or O(n) |

Remember: multiple passes are still linear — O(n) — as long as each pass is linear.

---

## 🧪 Example Problems

- Maximum Subarray (Kadane’s Algorithm)
- Trapping Rain Water
- Daily Temperatures (using monotonic stack)
- Longest Subarray with Limit

---

## 📌 Tips

- Use multiple passes when one-pass logic becomes too complex
- Precompute and store prefix/suffix values to avoid recalculating
- Use monotonic stacks for next greater/smaller problems in separate passes

---

## ⚠️ Caveats

- Make sure each pass is truly linear
- Be clear about what each pass is doing — separation of concerns helps

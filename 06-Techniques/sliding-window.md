# 🪟 Sliding Window Technique

The sliding window technique helps efficiently process **subarrays** or **substrings**. It allows reducing the time complexity from O(n²) to O(n) in many cases.

---

## 🧠 When to Use

Use when:

- You're asked to find subarrays/substrings with a fixed or variable condition
- The problem involves **contiguous elements**
- You're told to optimize to **O(n)** or **O(n log n)**

---

## 🧰 Types of Sliding Window

### 1. Fixed Size

Used when the window size `k` is given.

**Steps**:

1. Compute sum/logic for the first window.
2. Slide the window by removing the first element and adding the next.
3. Update result as needed.

### 2. Variable Size

Used when the window size isn't fixed — often to satisfy a condition (e.g., sum ≤ target).

**Steps**:

1. Expand right pointer until the condition breaks.
2. Shrink from the left until it satisfies again.
3. Track min/max window or result.

---

## ⏱️ Time & Space

| Approach             | Time      | Space |
| -------------------- | --------- | ----- |
| Naive (nested loops) | O(n \* k) | O(1)  |
| Sliding Window       | O(n)      | O(1)  |

---

## 🧪 Example Problem

**Maximum sum of subarray of size k**  
`Input: [1, 4, 2, 10, 23, 3, 1, 0, 20], k = 4`  
`Output: 39` → subarray `[4, 2, 10, 23]`

---

## 📌 Tips

- Use sliding window instead of recalculating from scratch
- Track values with prefix sums or counters when needed
- Works for strings too!

---

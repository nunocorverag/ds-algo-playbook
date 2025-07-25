# 📊 Sorting & Searching

Sorting involves rearranging elements in a sequence (e.g., ascending or descending).  
Searching is about locating a value efficiently — often using binary search on sorted input.

---

## 🔍 Why Sorting & Searching?

- Sorting helps apply techniques like binary search or identify patterns in data.
- Binary search reduces search time from **O(n)** to **O(log n)** on sorted arrays.

---

## ⏱️ Time Complexity

| Algorithm      | Time       | Space    |
| -------------- | ---------- | -------- |
| Bubble Sort    | O(n²)      | O(1)     |
| Insertion Sort | O(n²)      | O(1)     |
| Selection Sort | O(n²)      | O(1)     |
| Quicksort      | O(n log n) | O(log n) |
| Mergesort      | O(n log n) | O(n)     |
| Heapsort       | O(n log n) | O(1)     |
| Counting Sort  | O(n + k)   | O(k)     |
| Radix Sort     | O(nk)      | O(n + k) |

| Search Algorithm | Time     |
| ---------------- | -------- |
| Binary Search    | O(log n) |

> In interviews, sorting is typically done using built-in sort functions (e.g., `sort()`).

---

## ⚙️ Techniques

### ✅ Sorted Inputs

If the input is sorted, consider using **binary search** for faster lookup or decision problems.

### 🔢 Counting Sort (Non-comparison sort)

Used when elements fall within a known **limited range** (e.g., 0 to 1000).  
Example: **H-Index**, where counting frequencies helps speed up the solution.

---

## ⚠️ Corner Cases to Watch

- Empty array
- One or two elements
- All elements identical
- Already sorted or reversed

---

## 🧪 Essential Questions

- Binary Search
- Search in Rotated Sorted Array

---

## 🧠 Recommended Practice

- Kth Smallest Element in a Sorted Matrix
- Search a 2D Matrix
- Kth Largest Element in an Array
- Find Minimum in Rotated Sorted Array
- Median of Two Sorted Arrays

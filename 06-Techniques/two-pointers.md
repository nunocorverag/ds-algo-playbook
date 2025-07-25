# 🎯 Two Pointers Technique

The Two Pointers technique is a simple yet powerful strategy used to solve array and string problems in linear time, especially when working with **sorted arrays** or **bidirectional logic**.

---

## 🧠 When to Use

- Finding pairs/triplets with a target sum
- Processing data from both ends
- Comparing two arrays or substrings
- Optimizing nested loop solutions to linear time

---

## 🧰 Strategy

1. Initialize two pointers: `left = 0`, `right = n - 1`
2. Loop while `left < right`:
   - If `arr[left] + arr[right] == target`, return result
   - If sum < target → move `left++`
   - If sum > target → move `right--`

---

## 🧪 Example: Two Sum in Sorted Array

```cpp
bool twoSum(vector<int> &arr, int target) {
    int left = 0, right = arr.size() - 1;
    while (left < right) {
        int sum = arr[left] + arr[right];
        if (sum == target) return true;
        else if (sum < target) left++;
        else right--;
    }
    return false;
}
```

---

## ⏱️ Complexity

| Approach     | Time  | Space |
| ------------ | ----- | ----- |
| Naive        | O(n²) | O(1)  |
| Two Pointers | O(n)  | O(1)  |

---

## ✅ Key Benefits

- Efficient for sorted input
- No extra memory required
- Easy to extend to 3Sum, 4Sum, merging arrays, etc.

---

## 📌 Common Problems

- Two Sum (Sorted)
- 3Sum / 4Sum
- Container With Most Water
- Trapping Rain Water
- Valid Palindrome
- Merge Sorted Arrays

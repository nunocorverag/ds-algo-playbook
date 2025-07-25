# 🧩 Problem: Two Sum

## 📜 Description

> Given an array of integers `nums` and an integer `target`, return the indices of the two numbers such that they add up to `target`.

You may assume that each input would have exactly one solution, and you may not use the same element twice.  
You can return the answer in any order.

## 💡 Idea

- Use a hash map to track previously seen numbers and their indices.
- For each number, check if `target - num` has already been seen.
- If yes, we found the solution in O(1) time for this element.
- Brute force would involve nested loops with O(n²) time.

## 🔍 Strategy

- **Data Structure**: Hash Map (`dict`)
- **Pattern**: Hash Table lookup
- Iterate over array and store each number's index as you go.

## 🧠 Pseudocode (optional)

```
Create empty hash map
For each index and value in nums:
    If (target - value) in hash map:
        return current index and hash map's value
    Else:
        store current value and index in hash map
```

## ⏱️ Complexity

| Metric | Complexity |
| ------ | ---------- |
| Time   | O(n)       |
| Space  | O(n)       |

## 🧪 Edge Cases

- Negative numbers (e.g. [-1, 2, 4], target = 3)
- Duplicates in array
- One solution only (as per problem statement)

## 💻 Code (Python)

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        pair_idx = {}

        for i, num in enumerate(nums):
            if target - num in pair_idx:
                return [i, pair_idx[target - num]]
            pair_idx[num] = i
```

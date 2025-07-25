# 🧩 Problem: Contains Duplicate

## 📜 Description

> Given an integer array `nums`, return `true` if any value appears at least twice in the array, and return `false` if every element is distinct.

## 💡 Idea

- Use a set to track seen numbers.
- If a number appears again while iterating, return `True`.
- The set ensures O(1) lookup time.
- Brute force would compare each element with the rest, giving O(n²) time.

## 🔍 Strategy

- **Data Structure**: Set
- **Pattern**: Membership checking
- Loop through each number and check if it's already in the set.

## 🧠 Pseudocode (optional)

```
Create empty set
For each number in array:
    If number in set:
        return True
    Add number to set
Return False
```

## ⏱️ Complexity

| Metric | Complexity |
| ------ | ---------- |
| Time   | O(n)       |
| Space  | O(n)       |

## 🧪 Edge Cases

- Empty array
- All distinct values
- Duplicates at beginning or end

## 💻 Code (Python)

```python
class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:
        num_set = set()

        for n in nums:
            if n in num_set:
                return True
            num_set.add(n)

        return False
```

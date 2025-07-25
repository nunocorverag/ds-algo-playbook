# 🧩 Problem: Valid Anagram

## 📜 Description

> Given two strings `s` and `t`, return `true` if `t` is an anagram of `s`, and `false` otherwise.

## 💡 Idea

- Count the frequency of each character in `s`, then subtract the count using characters in `t`.
- If all character counts return to zero, then `t` is a valid anagram of `s`.

## 🔍 Strategy

- **Data structures**: Dictionary for character counts.
- **Algorithmic pattern**: Hash map frequency counting.
- **Breakdown**:
  - Traverse `s` and count frequency of each character.
  - Traverse `t` and decrement those frequencies.
  - If at any point a character is not found or frequency goes below zero, return False.

## 🧠 Pseudocode (optional)

- If lengths differ, return False.
- For each character in `s`, add to a counter.
- For each character in `t`, decrement from counter.
- If any value goes below zero or character not found, return False.
- If loop completes, return True.

## ⏱️ Complexity

| Metric | Complexity                             |
| ------ | -------------------------------------- |
| Time   | O(n)                                   |
| Space  | O(1) (since alphabet size is constant) |

## 🧪 Edge Cases

- Empty strings → should return True.
- Different lengths → should return False.
- Same characters but different counts → False.
- Unicode/mixed case? Depends on constraints.

## 💻 Code (Python)

```python
class Solution:
    def isAnagram(self, s: str, t: str) -> bool:
        if len(s) != len(t):
            return False

        counter = {}

        for char in s:
            counter[char] = counter.get(char, 0) + 1

        for char in t:
            if char not in counter or counter[char] == 0:
                return False
            counter[char] -= 1

        return True
```

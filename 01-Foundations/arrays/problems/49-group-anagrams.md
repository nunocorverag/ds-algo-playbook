    # 🧩 Problem: Group Anagrams

## 📜 Description

> Given an array of strings `strs`, group the anagrams together. You can return the answer in any order.

## 💡 Idea

- Anagrams have the same characters with the same frequencies.
- We can group them by creating a unique key per string that reflects its character distribution.
- Two common ways:
  1. Sort each string and use the sorted string as key.
  2. Count character frequency (26-length array) and use that as key (more efficient for long strings).

## 🔍 Strategy

- **Data Structures**: Dictionary (hash map), list for frequency counts.
- **Patterns**: Hashing, frequency map, grouping by signature.
- **Breakdown**:
  - For each word, compute its signature (sorted string or frequency tuple).
  - Use the signature as a key to group words into a hash map.

## 🧠 Pseudocode (optional)

- Initialize a dictionary `ans`.
- For each string:
  - Either sort it or create a frequency count list and convert to tuple.
  - Use this as the key and append the word to `ans[key]`.
- Return `ans.values()`.

## ⏱️ Complexity

| Metric | Complexity                 |
| ------ | -------------------------- |
| Time   | O(m _ n) or O(m _ n log n) |
| Space  | O(m \* n)                  |

> where `m` is the number of strings, and `n` is the average length of a string.

## 🧪 Edge Cases

- Empty input list → should return `[]`.
- Single word → returns list with one group.
- Strings with different lengths.
- Very long strings → prefer counting method for performance.

## 💻 Code (Python)

```python
from collections import defaultdict
from typing import List

class Solution:
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
        ans = defaultdict(list)

        for s in strs:
            # Option 1: sorted string as key
            key = "".join(sorted(s))
            ans[key].append(s)

        return list(ans.values())
```

### Alternate Solution (using character count key)

```python
from collections import defaultdict
from typing import List

class Solution:
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
        ans = defaultdict(list)

        for s in strs:
            count = [0] * 26
            for c in s:
                count[ord(c) - ord('a')] += 1
            ans[tuple(count)].append(s)

        return list(ans.values())
```

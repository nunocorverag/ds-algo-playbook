# 🧵 Strings

A **string** is a sequence of characters. Many array techniques apply here as well, but some unique patterns and structures are key to mastering string problems.

---

## 📦 Common Structures & Algorithms

- **Trie / Prefix Tree**
- **Suffix Tree**
- **Rabin-Karp** (substring search using rolling hash)
- **KMP Algorithm** (efficient substring search)

---

## ⏱️ Time Complexity

| Operation                  | Time      |
| -------------------------- | --------- |
| Access                     | O(1)      |
| Search                     | O(n)      |
| Insert / Remove            | O(n)      |
| Find Substring (naive)     | O(n \* m) |
| Concatenation (n + m)      | O(n + m)  |
| Slice or Split             | O(m)      |
| Strip (whitespace removal) | O(n)      |

---

## ⚠️ Interview Tips

- Ask about **input charset** and **case sensitivity**
- Check for **unicode**, **punctuation**, and **whitespace**

---

## 🧪 Corner Cases

- Empty strings
- One or two character strings
- Repeated or all unique characters

---

## 🎯 Techniques

### 🔢 Counting Characters

- Use a hash map or frequency array (e.g. `collections.Counter`)
- Space complexity is **O(1)** for lowercase Latin characters (26 letters)

### 🧮 Bitmask for Unique Characters

Use a 26-bit mask to track presence:

```python
mask = 0
for c in word:
    mask |= (1 << (ord(c) - ord('a')))
```

To check if two words share characters:

```python
if mask_a & mask_b > 0:
    # They share at least one character
```

---

### 🔁 Anagram Detection

- **Sort + Compare** → O(n log n) time
- **Frequency Counter** → O(n) time, O(1) space
- **Prime Multiplication (hash)** → O(n) time, O(1) space

---

### 🔂 Palindrome Tricks

- **Reverse + Compare**
- **Two Pointers**: inward from both ends
- **Expand Around Center**: for **Longest Palindromic Substring**
  - Even/odd centers require 2 passes per index

# 🌲 Trie

## 📘 Introduction

A **Trie** (or prefix tree) is a specialized tree structure that stores strings efficiently, especially for prefix-based queries. Common use cases include autocomplete, dictionary validation, and prefix matching.

---

## ⏱️ Time Complexity

Let `m` be the length of the string.

| Operation | Time |
| --------- | ---- |
| Search    | O(m) |
| Insert    | O(m) |
| Remove    | O(m) |

---

## ⚠️ Corner Cases

- Searching in an empty trie
- Inserting empty strings

---

## ⚙️ Techniques

- Preprocess a list of `n` words into a trie to allow word search in **O(k)** time instead of **O(n)**, where `k` is the length of the search word.
- Useful for problems involving dictionaries, autocomplete, or prefix groupings.

---

## 🔧 Sample Operations

```python
class TrieNode:
    def __init__(self):
        self.children = {}
        self.is_end = False

class Trie:
    def __init__(self):
        self.root = TrieNode()

    def insert(self, word):
        node = self.root
        for ch in word:
            if ch not in node.children:
                node.children[ch] = TrieNode()
            node = node.children[ch]
        node.is_end = True

    def search(self, word):
        node = self.root
        for ch in word:
            if ch not in node.children:
                return False
            node = node.children[ch]
        return node.is_end

    def startsWith(self, prefix):
        node = self.root
        for ch in prefix:
            if ch not in node.children:
                return False
            node = node.children[ch]
        return True
```

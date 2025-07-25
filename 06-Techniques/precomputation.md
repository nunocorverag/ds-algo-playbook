# 🧮 Precomputation

Precomputation allows solving problems faster by calculating reusable data ahead of time.  
This often includes **prefix sums**, **suffix products**, or **hash maps** for counting or indexing.

---

## 🧠 When to Use

- Subarray sum or product queries
- Repeated queries over similar data
- Optimizing nested loops by caching results
- Need to access accumulated results in constant time

---

## 🧰 Common Precomputations

- **Prefix Sum** → cumulative sums up to each index
- **Suffix Product** → cumulative product from the end
- **Frequency Hash Maps** → count elements in advance
- **Factorials/Primes Arrays** → used in combinatorics and number theory

---

## ⏱️ Complexity

| Operation      | Time | Space |
| -------------- | ---- | ----- |
| Precomputation | O(n) | O(n)  |
| Query Access   | O(1) | O(1)  |

---

## 🧪 Example Problems

- Product of Array Except Self
- Minimum Size Subarray Sum
- Range Sum Query
- Prefix Sum + Hash Map: Subarray Sum Equals K
- Leetcode prefix-sum tag problems

---

## 📌 Tips

- Use `prefix[i] = prefix[i-1] + arr[i]` to build sums
- For modular arithmetic, precompute factorials and inverses
- Be cautious with overflow (especially in products)

---

## ⚠️ Caveats

- Avoid unnecessary memory use if array is large
- Some queries may not benefit unless repeated

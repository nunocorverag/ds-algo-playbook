# 🧠 Binary Cheatsheet

Binary and bit manipulation questions are less common but still appear in interviews — especially for systems or embedded roles.

---

## 🧾 Key Concepts

- Convert between decimal and binary in your language
- Understand bitwise operators: `&`, `|`, `^`, `~`, `<<`, `>>`
- Be aware of overflow/underflow, especially with signed numbers

---

## 🧪 Bitwise Techniques

| Task                       | Code                     |
| -------------------------- | ------------------------ | ----------- |
| Test if k-th bit is set    | `num & (1 << k) != 0`    |
| Set k-th bit               | `num                     | = (1 << k)` |
| Turn off k-th bit          | `num &= ~(1 << k)`       |
| Toggle k-th bit            | `num ^= (1 << k)`        |
| Multiply by 2^k            | `num << k`               |
| Divide by 2^k              | `num >> k`               |
| Is power of 2              | `(num & (num - 1)) == 0` |
| Swap two numbers (bitwise) | `a ^= b; b ^= a; a ^= b` |

---

## 🧱 Practice

- Be ready for problems that involve:
  - Counting bits (`bin(n).count("1")`)
  - Bitmasks (especially in subsets/DP)
  - Power of 2 checks

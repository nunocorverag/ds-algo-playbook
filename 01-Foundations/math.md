# ➕ Math

Math is a foundational aspect of Computer Science and is sometimes tested in coding interviews. You usually won't need advanced math, but understanding some basics can help in implementing operations and reasoning about edge cases.

---

## 🚨 Things to Watch For

- Division or modulo by **0**
- Overflow/underflow (especially in C++/Java)
- Negative numbers and float precision issues

---

## ⚠️ Corner Cases

- Division by 0
- Multiplication by 1
- Negative numbers
- Floating-point rounding errors

---

## 📐 Common Formulas

| Use Case                    | Formula / Expression   |
| --------------------------- | ---------------------- |
| Even check                  | `num % 2 == 0`         |
| Sum 1 to N                  | `(n * (n + 1)) // 2`   |
| Geometric sum (powers of 2) | `2^(n+1) - 1`          |
| Permutations of N           | `N! / (N - K)!`        |
| Combinations of N           | `N! / (K! * (N - K)!)` |

---

## ⚙️ Techniques

### 🔁 Multiples

Use modulo:

```python
if x % k == 0:
    # x is a multiple of k
```

### 🧮 Comparing Floats Safely

```python
abs(x - y) <= 1e-6
```

### ⚡ Fast Operators

Use:

- **Exponentiation by squaring** (O(log n))
- **Binary search** for inverse operations like `sqrt(x)`

Examples:

```python
def pow(x, n):
    if n == 0: return 1
    half = pow(x, n // 2)
    return half * half if n % 2 == 0 else half * half * x
```

---

## 🧠 Essential Practice Questions

- `Pow(x, n)`
- `Sqrt(x)`

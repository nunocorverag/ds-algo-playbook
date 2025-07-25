# 📏 Interval

Interval problems involve **arrays of [start, end] pairs**, often requiring sorting and merging logic.

---

## 📘 Common Use Cases

- Merging calendar meetings
- Finding overlaps between intervals
- Inserting a new range into a schedule
- Covering ranges with minimum number of intervals

---

## 🔍 Things to Clarify in Interviews

- Are `[1, 2]` and `[2, 3]` considered overlapping?
- Can intervals have `a >= b`? (e.g. `[3, 3]`)

---

## ⚠️ Corner Cases

- No intervals
- Duplicate or equal intervals
- Contained intervals (e.g., `[1,10]` and `[2,3]`)
- Touching endpoints
- Already sorted input

---

## ⚙️ Core Techniques

### 🔢 Sort by Start Time

```python
intervals.sort(key=lambda x: x[0])
```

### 🔁 Check Overlap

```python
def is_overlap(a, b):
    return a[0] < b[1] and b[0] < a[1]
```

### 🔗 Merge Two Intervals

```python
def merge_intervals(a, b):
    return [min(a[0], b[0]), max(a[1], b[1])]
```

---

## 🧠 Summary Table

| Step          | Purpose                               |
| ------------- | ------------------------------------- |
| Sort          | Brings overlapping intervals together |
| Check Overlap | Identify if two ranges intersect      |
| Merge         | Consolidate into one range            |

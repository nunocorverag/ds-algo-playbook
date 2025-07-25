# 📐 Geometry

Geometry questions in interviews usually involve **2D space**, and focus on shape relations, distances, and overlap. These problems rarely require advanced math — you're often expected to apply **basic geometry + data structures**.

---

## 🧠 Key Concepts

- Work with 2D points, lines, rectangles, circles
- Be careful with **zero values**
- Avoid unnecessary floating point operations when possible

---

## 📌 Techniques

### 1. Distance Between Two Points

Use squared distance to avoid `sqrt`:

```python
dx, dy = x1 - x2, y1 - y2
distance_squared = dx * dx + dy * dy
```

### 2. Overlapping Circles

Two circles overlap if:

```python
dist_squared < (r1 + r2) ** 2
```

Where `dist_squared` is the squared distance between centers.

### 3. Overlapping Rectangles

```python
def is_overlapping(rect_a, rect_b):
    return (
        rect_a.left < rect_b.right and
        rect_a.right > rect_b.left and
        rect_a.top > rect_b.bottom and
        rect_a.bottom < rect_b.top
    )
```

> Make sure rectangles are well-defined (e.g. top > bottom).

---

## 🧪 Sample Questions

- Count how many rectangles intersect on a plane
- Find the `k` closest points to the origin
- Detect overlapping rectangles
- Triangulate a polygon

---

## 🧯 Corner Cases

- Points/rectangles with zero area
- Overlapping but not intersecting (e.g. touching at edge)

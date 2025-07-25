# 🌳 Tree

## 🧾 Introduction

A **tree** is a hierarchical structure composed of nodes. Each node has a parent (except the root) and zero or more children. Trees are **connected**, **acyclic**, and are commonly traversed recursively.

### Common Applications:

- File systems
- Expression parsing
- DOM trees
- Trie structures

## 📚 Common Tree Types

- **Binary Tree**: Each node has at most two children.
- **Binary Search Tree (BST)**: Left < Root < Right
- **Balanced Tree**: Left and right subtree heights differ by at most one.
- **Complete Tree**: All levels filled except possibly the last, filled from left to right.
- **N-ary Tree**: Node may have more than two children.
- **Trie**: Tree used to store prefixes of strings.

## 📘 Terminology

| Term       | Meaning                                       |
| ---------- | --------------------------------------------- |
| Root       | Node with no parent                           |
| Leaf       | Node with no children                         |
| Depth      | Edges from node to root                       |
| Height     | Edges from node to furthest leaf              |
| Subtree    | A tree formed from a node and its descendants |
| Ancestor   | A node’s parent or parent’s ancestor          |
| Descendant | A node’s child or child’s descendant          |

## 🔁 Tree Traversals

- **In-order** (Left → Root → Right)
- **Pre-order** (Root → Left → Right)
- **Post-order** (Left → Right → Root)
- **Level-order** (Breadth-First using Queue)

> 🔹 In-order traversal of BST gives sorted order.

## ⏱️ Time Complexity (for Balanced BST)

| Operation | Time     |
| --------- | -------- |
| Access    | O(log n) |
| Search    | O(log n) |
| Insert    | O(log n) |
| Delete    | O(log n) |

> Worst-case time is O(n) if tree is skewed.

## 🧠 Core Techniques

### ✅ Use Recursion

- Base case is usually when node is `null`
- Useful for divide-and-conquer logic
- Combine subtrees to compute result

### 🔄 Iterative Traversal

Use a **stack** for DFS-like traversal or a **queue** for BFS.

### 🧮 Common Operations

- Validate BST
- Insert/Delete/Search node
- Height of tree
- Count nodes
- Get min/max value

## ⚠️ Corner Cases

- Empty tree
- Single node
- Skewed tree (linked list)
- Duplicate values (clarify with interviewer)

## 📌 Interview Tip

Be able to write all DFS traversals **recursively and iteratively**. Interviewers may ask for both.

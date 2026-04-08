# HW1: Binary Search Trees (BST)

This project involves the complete, from-scratch implementation of a **Binary Search Tree (BST)** in C++, along with theoretical analysis of tree structures and sorting algorithms. 

*Note: The use of the C++ Standard Template Library (STL) or any external data structure libraries was strictly prohibited for this assignment. All tree structures and operations were implemented manually using raw pointers.*

## Implementation Details

The core of the assignment is the `BinarySearchTree` class, built using a custom `TreeNode` struct. The implementation includes the following fundamental operations:

* **`insert(int x)`**: Inserts a new node while maintaining the BST properties.
* **`retrieve(int x)`**: Iteratively searches the tree for a specific key.
* **`deleteKey(int x)`**: Removes a node while preserving the BST structure. It correctly handles all three deletion scenarios:
    * Case 0: Deleting a leaf node.
    * Case 1: Deleting a node with a single child.
    * Case 2: Deleting a node with two children (implemented using the **inorder successor**).
* **`height()`**: Calculates the maximum depth of the tree using a private recursive helper function.

## Theoretical Components (See `Report.pdf`)

In addition to the C++ implementation, this assignment covers the following theoretical concepts:
* Mathematical analysis of Full Binary Trees (calculating leaf and internal node counts based on height).
* Pseudocode implementation and step-by-step trace of the `SearchBST` algorithm.
* Big-O time complexity analysis of the `TreeSort` algorithm under both worst-case (unbalanced) and average-case (roughly balanced) scenarios.
* Algorithms for serializing (saving via preorder traversal) and deserializing (restoring) binary search trees.

---
*Disclaimer: This repository is intended to serve as a personal portfolio. Copying these solutions for academic submissions is a violation of the Bilkent University Honor Code.*

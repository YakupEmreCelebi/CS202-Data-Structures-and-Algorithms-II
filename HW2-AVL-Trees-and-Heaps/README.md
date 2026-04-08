# HW2: Priority Task Scheduler & Sequence Quality Monitor

This repository contains two completely scratch-built C++ implementations focusing on advanced data structures: **Heaps** and **AVL Trees**. The use of C++ STL was strictly prohibited, requiring manual memory management and pointer manipulation.

## Part 1: Aging Task Scheduler (Heaps)
Simulates a multi-processor task scheduling system using custom Min-Heap and Max-Heap structures.

* **Algorithm:** Implements an "aging" priority queue where a task's priority increases the longer it waits.
* **Data Structures:** * `TaskMaxHeap`: Manages the waiting queue based on dynamic Effective Priority.
    * `ProcessorMinHeap`: Tracks processor availability to efficiently assign tasks.
* **Complexity:** Achieves $O(N \log N)$ execution time by cleverly calculating effective priorities mathematically without iterating through the entire queue at each time step.

## Part 2: Sequencing Quality Monitor (AVL Tree)
A high-performance genomic sequence analyzer using a sliding window approach over massive datasets.

* **Algorithm:** Calculates the "Local Impact Sum" (sum of the $P$ lowest quality scores) within a sliding window of size $W$, and maintains a "Global Quality Metric".
* **Data Structure:** A fully self-balancing **AVL Tree** implemented from scratch.
* **Augmented Nodes:** To achieve the required $O(N \log W)$ complexity, every tree node is augmented with `subtree_size`, `subtree_sum`, and `value_count`. This eliminates the need to traverse $P$ nodes, allowing sum calculations in logarithmic time.

## Compilation
A `Makefile` is provided to compile both executables:
```bash
make all
# Generates ./scheduler and ./monitor binaries

---
*Disclaimer: This repository is intended to serve as a personal portfolio. Copying these solutions for academic submissions is a violation of the Bilkent University Honor Code.*

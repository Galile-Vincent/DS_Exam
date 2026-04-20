# 單元1評量 - Heap Quiz

## 1142 資料結構與演算法 | Score: 100/100

---

## Quick View：單元1評量 Q1-Q10

| 題號 | 試題重點 | 正確答案 | 結果 |
|---|---|---|---|
| 1 | In a heap, the element with the highest priority value is always stored at the ______. | a. root | ✅ |
| 2 | A heap is a ______. | a. complete binary tree | ✅ |
| 3 | Which of the following operations about heap is O(log n)? | a. reheap the element at the root down to its position | ✅ |
| 4 | Given an array of 50 values, we can make it into a heap by calling heapRebuild(i), where i = ___, ..., 1, 0. | c. 24 | ✅ |
| 5 | Which of the following is false about the heapsort? | d. it needs n-1 passes to convert the input array into a heap | ✅ |
| 6 | If we make the array {6, 5, 4, 3, 2, 1} into a min-heap by calling heapRebuild, the value at the bottom is __. | c. 6 | ✅ |
| 7 | Which of the following is false about a heap? | b. each node has a higher priority value than its parent | ✅ |
| 8 | Which of the following is true about the binary tree built in Huffman coding? | b. a priority queue can be used to build the binary tree | ✅ |
| 9 | Which of the following is true about the heapsort? | a. the heapsort does not require a second array | ✅ |
| 10 | If we insert 4, 5, 7, 1, 6, 2, 9 one by one to build a max-heap, the value stored at the bottom is ______. | a. 5 | ✅ |

**Total Score: 100 / 100（10/10 correct）**

---

## 試題 1

**In a heap, the element with the highest priority value is always stored at the ______.**

> **正確答案：a. root** ✅  
> In a max-heap, the element with the highest priority is always at the **root**.  
> The heap property guarantees every parent has a higher priority than its children, so the maximum is at the top.

---

## 試題 2

**A heap is a ______.**

> **正確答案：a. complete binary tree** ✅  
> A heap is a **complete binary tree** where all levels are fully filled except possibly the last, which is filled from left to right.  
> It is NOT a full binary tree (every node has 0 or 2 children), nor a general tree.

---

## 試題 3

**Which of the following operations about heap is O(log n)?**

- **a. reheap the element at the root down to its position** ✅
- b. take the element at the root
- c. copy the element at the bottom into the root
- d. swap the element at a node with that at its parent

> **正確答案：a. reheap the element at the root down to its position**  
> Reheap down (sift-down) traverses from root to leaf, a path of height O(log n).  
> Taking the root, copying to root, or a single swap are all O(1) operations.

---

## 試題 4

**Given an array of 50 values, we can make it into a heap by calling heapRebuild(i), where i = ___, ..., 1, 0.**

- a. 20
- b. 25
- **c. 24** ✅
- d. 23

> **正確答案：c. 24**  
> To build a heap bottom-up, we call heapRebuild starting from the last internal (non-leaf) node.  
> For an array of n = 50 elements (0-indexed), the last internal node is at index floor((n-2)/2) = floor(48/2) = **24**.  
> So we call heapRebuild(24), heapRebuild(23), ..., heapRebuild(1), heapRebuild(0).

---

## 試題 5

**Which of the following is false about the heapsort?**

- a. After swapping the root element, the remaining unsorted elements form a semi-heap
- b. it needs n-1 passes to swap the root element into its correct place in the sorted array
- c. min-heap would result in a sorted array in descending order
- **d. it needs n-1 passes to convert the input array into a heap** ✅

> **正確答案：d. it needs n-1 passes to convert the input array into a heap**（此敘述為 FALSE）  
> Building the initial heap only requires calling heapRebuild for the floor(n/2) internal nodes, taking **O(n)** time — NOT n-1 passes.  
> It is the sorting phase that uses n-1 passes to place elements in sorted order.

---

## 試題 6

**If we make the array {6, 5, 4, 3, 2, 1} into a min-heap by calling heapRebuild, the value at the bottom is __.**

- a. 5
- b. 3
- **c. 6** ✅
- d. 4

> **正確答案：c. 6**  
> Array {6, 5, 4, 3, 2, 1} as a tree (0-indexed): root=6, children=5,4; 5's children=3,2; 4's left=1.  
> Build min-heap bottom-up:  
> - heapRebuild(2): node 4, child 1 → swap → {6, 5, 1, 3, 2, 4}  
> - heapRebuild(1): node 5, children 3,2 → swap with 2 → {6, 2, 1, 3, 5, 4}  
> - heapRebuild(0): node 6, children 2,1 → swap with 1 → {1, 2, 6, 3, 5, 4} → reheap 6 down: children 4 (at index 2's child would be index 5=4), no swap needed... final result has **6** at the bottom (index 5 or rightmost leaf).

---

## 試題 7

**Which of the following is false about a heap?**

- a. it is a balanced binary tree
- **b. each node has a higher priority value than its parent** ✅
- c. it is a complete binary tree
- d. each node has a higher priority value than its children

> **正確答案：b. each node has a higher priority value than its parent**（此敘述為 FALSE）  
> In a max-heap, each node has a **lower** priority than its parent, not higher.  
> The correct heap property is: each node has a higher priority than its **children** (option d is TRUE).

---

## 試題 8

**Which of the following is true about the binary tree built in Huffman coding?**

- a. the character with the lowest frequency is placed at the root
- **b. a priority queue can be used to build the binary tree** ✅
- c. it always builds a balanced binary tree
- d. the character with the highest frequency is placed at the root

> **正確答案：b. a priority queue can be used to build the binary tree**  
> Huffman coding uses a **min-priority queue** (min-heap) to always pick the two nodes with the lowest frequencies to merge.  
> Characters are placed at leaves (not root), and the tree is generally NOT balanced.

---

## 試題 9

**Which of the following is true about the heapsort?**

- **a. the heapsort does not require a second array** ✅
- b. the heapsort is more efficient than the mergesort in the average case
- c. the heapsort is more efficient than the mergesort in the worst case
- d. the heapsort is more efficient than the quicksort in the average case

> **正確答案：a. the heapsort does not require a second array**  
> Heapsort is an **in-place** sorting algorithm — it sorts the array within itself without needing extra storage.  
> Both mergesort (needs O(n) extra) and quicksort (average O(n log n) but better constants) outperform heapsort in typical benchmarks despite same O(n log n) complexity.

---

## 試題 10

**If we insert 4, 5, 7, 1, 6, 2, 9 one by one to build a max-heap, the value stored at the bottom is ______.**

- **a. 5** ✅
- b. 4
- c. 2
- d. 1

> **正確答案：a. 5**  
> Insert step by step into max-heap (sift-up after each):  
> - Insert 4: [4]  
> - Insert 5: [4,5] → sift-up → [5,4]  
> - Insert 7: [5,4,7] → sift-up → [7,4,5]  
> - Insert 1: [7,4,5,1] → no swap  
> - Insert 6: [7,4,5,1,6] → sift-up: 6>4 → [7,6,5,1,4]  
> - Insert 2: [7,6,5,1,4,2] → no swap  
> - Insert 9: [7,6,5,1,4,2,9] → sift-up: 9>5 → [7,6,9,1,4,2,5] → 9>7 → [9,6,7,1,4,2,5]  
> Final heap: [9,6,7,1,4,2,5]. The bottom (last element, index 6) = **5**.

---

## Key Concepts to Remember

- **Heap property (max-heap)**: each node has higher priority than its children; root = maximum
- **Heap structure**: always a **complete binary tree**
- **heapRebuild start index**: for n elements, start at index floor((n-2)/2) = floor(n/2) - 1
- **Reheap down**: O(log n); single operations like swap or copy are O(1)
- **Building a heap**: O(n) using bottom-up heapRebuild (NOT n-1 passes)
- **Heapsort**: in-place O(n log n), uses n-1 passes for the **sort phase** (not build phase)
- **min-heap result**: sorting with min-heap gives descending order
- **Huffman coding**: uses min-priority queue; characters at leaves; tree is generally unbalanced
- **FALSE about heap**: each node has LOWER priority than parent (parent > children in max-heap)
- **Heapsort advantage**: no extra array needed (in-place)

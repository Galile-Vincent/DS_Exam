# 單元1評量 - Heap & Priority Queue Quiz

## 1142 資料結構與演算法 | Score: 100/100 (Merged)

---

## Quick View：單元1評量 Q1-Q20

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
| 11 | If the ____ algorithm is used as a priority queue, the pqDelete operation is O(1), while the pqInsert operation is O(n). | b. insertion sort | ✅ |
| 12 | Which of the following is true about the differences between heaps and binary search trees? | a. BSTs can be viewed as being sorted but heaps are not | ✅ |
| 13 | If we insert 7, 9, 4, 6, 8, 3 one by one to build a max-heap, its pre-order traversal sequence will be ______. | a. 9, 8, 6, 7, 4, 3 | ✅ |
| 14 | The first item to be removed from a priority queue is the item _____. | b. with the highest priority value | ✅ |
| 15 | Which of the following is false about the priority queue implemented by a binary search tree? | a. the root has the highest priority value | ✅ |
| 16 | If we insert 7, 9, 4, 6, 8, 3 one by one to build a max-heap, its post-order traversal sequence will be ______. | Correct: 6, 7, 8, 3, 4, 9 | ✅ |
| 17 | If we make the array {7, 3, 4, 6, 8, 9} into a max-heap by calling heapRebuild, the value at the bottom is __. | Correct: 4 | ✅ |
| 18 | Given an array of 25 values, we can make it into a heap by calling heapRebuild(i), where i = ___, ..., 1, 0. | Correct: 11 | ✅ |
| 19 | If the ____ algorithm is used as a priority queue, the pqInsert operation is O(1), while the pqDelete operation is O(n). | a. selection sort | ✅ |
| 20 | If we insert 4, 5, 7, 1, 6, 9, 2 one by one to build a min-heap, the value stored at the bottom is ______. | d. 7 | ✅ |

---

## 試題 11

**If the ____ algorithm is used as a priority queue, the pqDelete operation is O(1), while the pqInsert operation is O(n).**

- a. selection sort
- **b. insertion sort** ✅
- c. heap sort
- d. bubble sort

> **正確答案：b. insertion sort**  
> Using insertion sort (keeping a sorted list), finding the highest priority item (at front/back) is **O(1)**.  
> However, inserting a new item into its sorted position takes **O(n)** time.

---

## 試題 12

**Which of the following is true about the differences between heaps and binary search trees?**

- **a. binary search trees can be viewed as being sorted but heaps are not** ✅
- b. binary search trees are always balanced binary trees but heaps are always complete binary trees
- c. binary search trees can be used as priority queues but heaps are not
- d. binary search trees are always complete binary trees but heaps are always balanced binary trees

> **正確答案：a. binary search trees can be viewed as being sorted but heaps are not**  
> In-order traversal of a BST visits nodes in sorted order.  
> A heap only maintains a partial order (parent vs children), not a full global sort.

---

## 試題 13

**If we insert 7, 9, 4, 6, 8, 3 one by one to build a max-heap, its pre-order traversal sequence will be ______.**

- **a. 9, 8, 6, 7, 4, 3** ✅
- b. 3, 4, 7, 8, 6, 9
- c. 3, 6, 9, 8, 4, 7
- d. 7, 8, 4, 9, 6, 3

> **正確答案：a. 9, 8, 6, 7, 4, 3**  
> Step by step insertion into max-heap:  
> [7] -> [9,7] -> [9,7,4] -> [9,7,4,6] -> [9,8,4,6,7] -> [9,8,4,6,7,3] (after sifting up 8 over 7).  
> Pre-order (Root-Left-Right): 9, 8, 6, 7, 4, 3.

---

## 試題 14

**The first item to be removed from a priority queue is the item _____.**

- a. with the highest value
- **b. with the highest priority value** ✅
- c. at the front of the priority queue
- d. at the end of the priority queue

> **正確答案：b. with the highest priority value**  
> By definition, a priority queue removes the item with the highest **priority**, regardless of arrival time.

---

## 試題 15

**Which of the following is false about the priority queue implemented by a binary search tree?**

- **a. the root has the highest priority value** ✅
- b. the worst case occurs when the binary search tree is skewed
- c. pqInsert and pqDelete are both O(n) in the worst case
- d. pqInsert and pqDelete are both O(log n) in the average case

> **正確答案：a. the root has the highest priority value**（此敘述為 FALSE）  
> In a BST, the node with the highest value (priority) is the **rightmost node**, not necessarily the root.

---

## 試題 16

**If we insert 7, 9, 4, 6, 8, 3 one by one to build a max-heap, its post-order traversal sequence will be ______.**

- **a. 6, 7, 8, 3, 4, 9** ✅
- b. 9, 8, 6, 7, 4, 3
- c. 3, 6, 9, 8, 4, 7
- d. 3, 4, 7, 8, 6, 9

> **正確答案：a. 6, 7, 8, 3, 4, 9**  
> Heap structure: Root=9, LeftChild=8, RightChild=4. 8's Children=6,7. 4's Child=3.  
> Post-order (Left-Right-Root): [6, 7, 8], [3, 4], 9.  
> Result: **6, 7, 8, 3, 4, 9**.

---

## 試題 17

**If we make the array {7, 3, 4, 6, 8, 9} into a max-heap by calling heapRebuild, the value at the bottom is __.**

- **a. 4** ✅
- b. 6
- c. 3
- d. 7

> **正確答案：a. 4**  
> Array {7, 3, 4, 6, 8, 9} build bottom-up:  
> - heapRebuild(2): node 4, child 9 → {7, 3, 9, 6, 8, 4}  
> - heapRebuild(1): node 3, children 6,8 → {7, 8, 9, 6, 3, 4}  
> - heapRebuild(0): node 7, children 8,9 → {9, 8, 7, 6, 3, 4}  
> Index 5 (bottom) is **4**.

---

## 試題 18

**Given an array of 25 values, we can make it into a heap by calling heapRebuild(i), where i = ___, ..., 1, 0.**

- **a. 11** ✅
- b. 25
- c. 12
- d. 10

> **正確答案：a. 11**  
> For n=25: floor((25-2)/2) = **11**.

---

## 試題 19

**If the ____ algorithm is used as a priority queue, the pqInsert operation is O(1), while the pqDelete operation is O(n).**

- **a. selection sort** ✅
- b. mergesort
- c. quicksort
- d. insertion sort

> **正確答案：a. selection sort**  
> Selection sort logic: insertion just appends (**O(1)**); deletion requires scanning for max (**O(n)**).

---

## 試題 20

**If we insert 4, 5, 7, 1, 6, 9, 2 one by one to build a min-heap, the value stored at the bottom is ______.**

- a. 4
- b. 5
- c. 6
- **d. 7** ✅

> **正確答案：d. 7**  
> Insert steps: [4] -> [4,5] -> [4,5,7] -> [1,4,7,5] -> [1,4,7,5,6] -> [1,4,2,5,6,9] -> [1,4,2,5,6,9,7].  
> Index 6 (bottom) is **7**.
Merge additional questions into exam1.md---

## 試題 1
[... root explanation ...]
## 試題 2
[... complete binary tree explanation ...]
## 試題 3
[... O(log n) explanation ...]
## 試題 4
[... 24 explanation ...]
## 試題 5
[... building heap FALSE explanation ...]
## 試題 6
[... 6 at bottom explanation ...]
## 試題 7
[... node > parent FALSE explanation ...]
## 試題 8
[... Huffman priority queue explanation ...]
## 試題 9
[... no second array explanation ...]
## 試題 10
[... 5 at bottom explanation ...]

## Key Concepts to Remember (Updated)

- **Selection sort priority queue**: O(1) insert, O(n) delete
- **Insertion sort priority queue**: O(n) insert, O(1) delete
- **BST as priority queue**: Rightmost node is max (not root). O(log n) avg, O(n) worst.
- **Traversal sequences**: Trace heap insertion carefully for pre/post-order.
- **Heap vs BST**: BST is globally sorted; Heap is partially ordered.
- **Bottom-up build**: heapRebuild starts at floor(n/2)-1.
- **Heapsort**: In-place, O(n log n). Initial build is O(n). Sorting phase is n-1 passes.
- **Huffman Coding**: Uses min-priority queue (min-heap). Characters at leaves. Tree is generally unbalanced.
- **FALSE about heap**: each node has LOWER priority than parent (parent > children in max-heap).
- **Heapsort advantage**: no extra array needed (in-place).

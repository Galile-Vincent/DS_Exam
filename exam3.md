# 單元3評量 - 2-3 Tree & 2-3-4 Tree Quiz
## 1142 資料結構與演算法 | Score: 90/100

---

# Quick View：單元3評量 Q1-Q30

| 題號 | 試題重點 | 正確答案 | 結果 |
|---|---|---|---|
| 1 | A 2-3 tree of height 5 has at most ______ nodes. | a. 121 | ✅ |
| 2 | A node that contains two keys and three children is called a ______. | d. 3-node | ✅ |
| 3 | Each node in a 2-3-4 tree contains ______ keys. | c. one, two or three | ✅ |
| 4 | Which of the following is TRUE about 2-3-4 tree? | a. each node has at most 4 children | ✅ |
| 5 | Which is NOT a step for inserting a new key into a 2-3 tree? | c. merge two leaves into one node if necessary | ✅ |
| 6 | If a node in a 2-3-4 tree has three children, it must contain ______ keys. | d. two | ✅ |
| 7 | Search of an item on a 2-3-4 tree is ______. | d. O(log n) | ✅ |
| 8 | Deletion of an item from a 2-3 tree is ______. | a. O(log n) | ✅ |
| 9 | The height of a 2-3-4 tree that contains 300 items is at least ______. | c. 5 | ❌ |
| 10 | The height of a 2-3 tree that contains 1023 items is at most ______. | b. 10 | ✅ |
| 11 | The height of a binary search tree that contains 1023 items is at least ______. | c. 10 | ✅ |
| 12 | Insertion of an item into a 2-3 tree is ______. | c. O(log n) | ✅ |
| 13 | Which is FALSE about linear implementations of ADT table? | b. Unsorted array-based implementation is O(n) on insertion | ❌ |
| 14 | _______ may occur during insertion of a new key into a 2-3 tree. | c. Splitting nodes | ✅ |
| 15 | A node that contains one key and two children is called a ______. | a. 2-node | ✅ |
| 16 | ______ implementation is O(log n) on retrieval of an item. | c. Sorted array-based | ✅ |
| 17 | Insert 1, 2, 3, 8, 6, 4, 7 into a 2-3-4 tree: total nodes? | a. 4 | ✅ |
| 18 | A 4-node contains at most ______ keys. | d. three | ✅ |
| 19 | Insertion of an item into a 2-3-4 tree is ______. | c. O(log n) | ✅ |
| 20 | Which is FALSE about 2-3-4 trees? | b. Insertion requires more steps than 2-3 tree | ✅ |
| 21 | Insert 4, 5, 7, 1, 6, 9, 3 into a 2-3 tree: root key? | b. 5 | ✅ |
| 22 | In a 2-3-4 tree, when a node is split, its parent cannot be a _____. | a. 4-node | ✅ |
| 23 | ______ is NOT a balanced search tree. | c. Heap | ✅ |
| 24 | In a 2-3 tree, what happens first if the key is deleted from an internal node? | b. swap it with the in-order successor | ✅ |
| 25 | Binary search tree implementation is O(n) on ______. | a. traversal of all items | ✅ |
| 26 | Which is FALSE about balanced search trees? | c. 2-3 tree is a binary tree | ✅ |
| 27 | When the root of a 2-3 tree has no item after deleting a key, we _______. | b. remove the root | ✅ |
| 28 | ______ is a tree in which all leaves are at the same level. | b. 2-3 tree | ✅ |
| 29 | The balance of a _______ is sensitive to insertion order. | d. binary search tree | ✅ |
| 30 | A 2-3 tree of height 5 has at least ______ nodes. | c. 31 | ✅ |

**Total Score: 90 / 100（18/20 correct）**

---

## 試題 1
**A 2-3 tree of height 5 has at most ______ nodes.**

> **正確答案：a. 121** ✅  
> Maximum nodes occur when every node is a 3-node.  
> Total = 3^0 + 3^1 + 3^2 + 3^3 + 3^4 = 1 + 3 + 9 + 27 + 81 = **121**.

---

## 試題 2
**A node that contains two keys and three children is called a ______.**

> **正確答案：d. 3-node** ✅  
> Node names are based on the number of children.  
> A node with 2 keys and 3 children is a **3-node**.  
> Rule: k children -> k - 1 keys.

---

## 試題 3
**Each node in a 2-3-4 tree contains ______ keys.**

> **正確答案：c. one, two or three** ✅  
> 2-node has 1 key, 3-node has 2 keys, and 4-node has 3 keys.  
> Therefore, each node contains **1, 2, or 3** keys.

---

## 試題 4
**Which of the following is TRUE about 2-3-4 tree?**

> **正確答案：a. each node has at most 4 children** ✅  
> In a 2-3-4 tree, a node can have 2, 3, or 4 children.  
> The maximum is **4 children**, so it is not a binary tree.

---

## 試題 5
**Which of the following is NOT a step for inserting a new key into a 2-3 tree?**

> **正確答案：c. merge two leaves into one node if necessary** ✅  
> Insertion steps are: locate leaf -> insert -> **split** if overflow occurs.  
> Merging happens during **deletion**, not insertion.

---

## 試題 6
**If a node in a 2-3-4 tree has three children, it must contain ______ keys.**

> **正確答案：d. two** ✅  
> 3 children means the node is a 3-node.  
> Rule: k children -> k - 1 keys, so 3 children -> **2 keys**.

---

## 試題 7
**Search of an item on a 2-3-4 tree is ______.**

> **正確答案：d. O(log n)** ✅  
> A 2-3-4 tree is always balanced.  
> Search travels from root to leaf, so the time complexity is **O(log n)**.

---

## 試題 8
**Deletion of an item from a 2-3 tree is ______.**

> **正確答案：a. O(log n)** ✅  
> Deletion follows a path whose length is the tree height.  
> Since a 2-3 tree is balanced, deletion is **O(log n)** even with redistribution or merging.

---

## 試題 9
**The height of a 2-3-4 tree that contains 300 items is at least ______.**

> **我的答案：a. 4** ❌  
> **正確答案：c. 5**
>
> Minimum height occurs when every node is a 4-node.  
> Max items at height h = (4^h - 1) / 3.  
> h = 4: (4^4 - 1) / 3 = 85 < 300  
> h = 5: (4^5 - 1) / 3 = 341 >= 300  
> Therefore, the minimum height is **5**.

---

## 試題 10
**The height of a 2-3 tree that contains 1023 items is at most ______.**

> **正確答案：b. 10** ✅  
> Maximum height occurs when every node is a 2-node.  
> Max items at height h = 2^h - 1.  
> 2^10 - 1 = 1023, so the maximum height is **10**.

---

## 試題 11
**The height of a binary search tree that contains 1023 items is at least ______.**

> **正確答案：c. 10** ✅  
> Minimum height occurs in a perfectly balanced BST.  
> 2^h - 1 >= 1023, so h >= 10.  
> Since 1023 = 2^10 - 1, the minimum height is **10**.

---

## 試題 12
**Insertion of an item into a 2-3 tree is ______.**

> **正確答案：c. O(log n)** ✅  
> Locating the leaf takes O(log n).  
> Splits may move upward, but at most along the tree height.  
> Total time complexity is **O(log n)**.

---

## 試題 13
**Which of the following is FALSE about linear implementations of ADT table?**

> **我的答案：a.** ❌  
> **正確答案：b. Unsorted array-based implementation is O(n) on insertion**
>
> Unsorted array-based insertion can append to the end, so it is **O(1)**.  
> Therefore, saying it is O(n) is **FALSE**.  
> Sorted array-based insertion is O(n) because elements may need to shift.

---

## 試題 14
**_______ may occur during the insertion of a new key into a 2-3 tree.**

> **正確答案：c. Splitting nodes** ✅  
> When insertion causes overflow, the node is **split** and the middle key is promoted.  
> Merging and redistribution are related to deletion.

---

## 試題 15
**A node that contains one key and two children is called a ______.**

> **正確答案：a. 2-node** ✅  
> A node is named by its number of children.  
> A 2-node has 1 key and **2 children**.

---

## 試題 16
**______ implementation is O(log n) on retrieval of an item.**

> **正確答案：c. Sorted array-based** ✅  
> A sorted array supports binary search, so retrieval is **O(log n)**.  
> Pointer-based lists do not support direct random access, and unsorted structures require linear search.

---

## 試題 17
**If we insert 1, 2, 3, 8, 6, 4, 7 one by one to build a 2-3-4 tree, there are ______ nodes in total.**

> **正確答案：a. 4** ✅  
> Insert 1, 2, 3 -> root becomes [1,2,3].  
> Insert 8 -> split [1,2,3], promote 2, giving root [2] with children [1] and [3,8].  
> Insert 6 -> right child becomes [3,6,8].  
> Insert 4 -> split [3,4,6,8], promote 6, giving root [2,6] and children [1], [3,4], [8].  
> Insert 7 -> child [8] becomes [7,8].  
> Total nodes = **4**.

---

## 試題 18
**A 4-node contains at most ______ keys.**

> **正確答案：d. three** ✅  
> A 4-node has 4 children and exactly **3 keys**.  
> Rule: k-node -> k - 1 keys.

---

## 試題 19
**Insertion of an item into a 2-3-4 tree is ______.**

> **正確答案：c. O(log n)** ✅  
> 2-3-4 tree insertion uses top-down splitting.  
> The algorithm makes one root-to-leaf pass, so insertion is **O(log n)**.

---

## 試題 20
**Which of the following is FALSE about 2-3-4 trees?**

> **正確答案：b. Insertion on a 2-3-4 tree requires more steps than that on a 2-3 tree** ✅  
> This statement is **FALSE**.  
> 2-3-4 tree insertion usually needs fewer steps because it splits 4-nodes on the way down.  
> 2-3 tree insertion may split bottom-up and travel back toward the root.

---

## 試題 21
**If we insert 4, 5, 7, 1, 6, 9, 3 one by one to build a 2-3 tree, the key on the root is ______.**

- a. 3
- b. **5** ✅
- c. 6
- d. 4

> **正確答案：5**  
> 插入並分裂節點後，中間值 **5** 會被提升到 root。

---

## 試題 22
**In a 2-3-4 tree, when a node is split, its parent cannot possibly be a ____.**

- a. **4-node** ✅
- b. 2-node
- c. 3-node
- d. all the above

> **正確答案：4-node**  
> 在 2-3-4 tree 中，split 前會先確保 parent 不是 4-node，所以 parent 不可能是 4-node。

---

## 試題 23
**______ is NOT a balanced search tree.**

- a. 2-3 tree
- b. AVL tree
- c. **Heap** ✅
- d. 2-3-4 tree

> **正確答案：Heap**  
> Heap 是完全二元樹，但不是搜尋樹，因為它不符合 BST 的搜尋順序性質。

---

## 試題 24
**In a 2-3 tree, we first _______ if the key is deleted from an internal node.**

- a. merge two nodes
- b. **swap it with the in-order successor** ✅
- c. redistribute keys
- d. remove the root

> **正確答案：swap it with the in-order successor**  
> 刪除 internal node 的 key 時，先與 in-order successor 交換，再刪除葉節點上的值。

---

## 試題 25
**Binary search tree implementation is O(n) on ______.**

- a. **traversal of all items** ✅
- b. insertion of an item
- c. deletion of an item
- d. retrieval of an item

> **正確答案：traversal of all items**  
> Traversal 必須訪問所有 n 個節點，因此時間複雜度固定為 **O(n)**。

---

## 試題 26
**Which of the following is FALSE about balanced search trees?**

- a. 2-3 tree is always balanced
- b. 2-3 tree is never taller than a minimum-height binary search tree
- c. **2-3 tree is a binary tree** ✅
- d. 2-3-4 tree requires more storage than a binary search tree

> **正確答案：2-3 tree is a binary tree**（此敘述為 FALSE）  
> 2-3 tree 的節點可以有 2 或 3 個子節點，不是 binary tree。

---

## 試題 27
**When the root of a 2-3 tree has no item after deleting a key, we _______.**

- a. merge two nodes
- b. **remove the root** ✅
- c. redistribute keys
- d. swap it with the in-order successor

> **正確答案：remove the root**  
> 若 root 刪除後為空，代表樹的高度縮減，直接移除 root，樹高 -1。

---

## 試題 28
**______ is a tree in which all leaves are at the same level.**

- a. AVL tree
- b. **2-3 tree** ✅
- c. Binary search tree
- d. Heap

> **正確答案：2-3 tree**  
> 2-3 tree 保證所有葉節點都在同一層，因此是 perfectly balanced。

---

## 試題 29
**The balance of a _______ is sensitive to the order in which items are inserted into it.**

- a. 2-3 tree
- b. min heap
- c. 2-3-4 tree
- d. **binary search tree** ✅

> **正確答案：binary search tree**  
> BST 的形狀與高度會受到插入順序影響；最差情況可能退化成線性鏈。

---

## 試題 30
**A 2-3 tree of height 5 has at least ______ nodes.**

- a. 120
- b. 32
- c. **31** ✅
- d. 121

> **正確答案：31**  
> 最少節點時，所有節點都是 2-node。  
> 各層節點數：1 + 2 + 4 + 8 + 16 = **31**。

---

# Key Concepts to Remember

- **Node naming**: k-node = k children, k - 1 keys
- **2-3 tree insertion**: bottom-up split on overflow
- **2-3-4 tree insertion**: top-down split, usually more efficient
- **Merge**: happens during deletion underflow
- **Split**: happens during insertion overflow
- **Sorted array**: supports O(log n) retrieval through binary search
- **Height formula**: max-height 2-3 tree with n items uses 2^h - 1

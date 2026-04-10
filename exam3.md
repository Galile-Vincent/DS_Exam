# 單元3評量 - 2-3 Tree & 2-3-4 Tree Quiz
## 1142資料結構與演算法 | Score: 90/100

---

## Q1. A 2-3 tree of height 5 has at most ______ nodes.

**Correct Answer: a. 121** ✅

**Explanation:** In a 2-3 tree, maximum nodes occur when every node is a 3-node (3 children). Total = 3^0 + 3^1 + 3^2 + 3^3 + 3^4 = 1 + 3 + 9 + 27 + 81 = **121**.

---

## Q2. A node that contains two keys and three children is called a ______.

**Correct Answer: d. 3-node** ✅

**Explanation:** Node names are based on number of children. A node with 2 keys and 3 children = **3-node**. Rule: k children → k-1 keys.

---

## Q3. Each node in a 2-3-4 tree contains ______ keys.

**Correct Answer: c. one, two or three** ✅

**Explanation:**
- 2-node: 1 key, 2 children
- 3-node: 2 keys, 3 children
- 4-node: 3 keys, 4 children

So each node contains **1, 2, or 3** keys.

---

## Q4. Which of the following is TRUE about 2-3-4 tree?

**Correct Answer: a. each node has at most 4 children** ✅

**Explanation:** By definition, 2-3-4 tree nodes can have 2, 3, or 4 children. Max = **4 children** (a 4-node). It is NOT a binary tree.

---

## Q5. Which of the following is NOT a step for inserting a new key into a 2-3 tree?

**Correct Answer: c. merge two leaves into one node if necessary** ✅

**Explanation:** Insertion steps: locate leaf → insert → **split** if overflow. Merging only happens during **deletion** (underflow). Merging is NOT an insertion step.

---

## Q6. If a node in a 2-3-4 tree has three children, it must contain ______ keys.

**Correct Answer: d. two** ✅

**Explanation:** 3 children → 3-node → **2 keys**. Formula: k children = k-1 keys.

---

## Q7. Search of an item on a 2-3-4 tree is ______.

**Correct Answer: d. O(log n)** ✅

**Explanation:** 2-3-4 tree is always balanced. Height = O(log n). Search traverses root to leaf = **O(log n)**.

---

## Q8. Deletion of an item from a 2-3 tree is ______.

**Correct Answer: a. O(log n)** ✅

**Explanation:** Deletion traverses the tree (O(log n)) and may redistribute/merge nodes upward. At most O(log n) operations → total **O(log n)**.

---

## Q9. The height of a 2-3-4 tree that contains 300 items is at least ______.

**My Answer: a. 4** ❌ | **Correct Answer: c. 5**

**Explanation:** Minimum height = when every node is a 4-node. Max items at height h (1-indexed) = (4^h - 1)/3.
- h=4: (4^4-1)/3 = 85 < 300 ✗
- h=5: (4^5-1)/3 = 341 >= 300 ✓

So minimum height = **5** (when height is counted starting from 1).

---

## Q10. The height of a 2-3 tree that contains 1023 items is at most ______.

**Correct Answer: b. 10** ✅

**Explanation:** Maximum height = when every node is a 2-node. Max items at height h = 2^h - 1. So 2^h - 1 >= 1023 → h >= 10. Max height = **10**.

---

## Q11. The height of a binary search tree that contains 1023 items is at least ______.

**Correct Answer: c. 10** ✅

**Explanation:** Minimum height BST = perfectly balanced. 2^h - 1 >= 1023 → h >= 10. Min height = **10** (since 1023 = 2^10 - 1, perfect binary tree).

---

## Q12. Insertion of an item into a 2-3 tree is ______.

**Correct Answer: c. O(log n)** ✅

**Explanation:** Locate leaf O(log n) + at most O(log n) node splits upward = **O(log n)** total.

---

## Q13. Which of the following is FALSE about linear implementations of ADT table?

**My Answer: a.** ❌ | **Correct Answer: b. Unsorted array-based implementation is O(n) on insertion**

**Explanation:**
- a. Unsorted pointer-based deletion: O(n) to find → TRUE
- **b. Unsorted array-based insertion: O(1) (append to end) — so saying O(n) is FALSE** ✓
- c. Sorted pointer-based deletion: O(n) to find → TRUE
- d. Sorted array-based insertion: O(n) to shift → TRUE

---

## Q14. _______ may occur during the insertion of a new key into a 2-3 tree.

**Correct Answer: c. Splitting nodes** ✅

**Explanation:** When a node overflows during insertion, it is **split** (middle key promoted to parent). Merging occurs during deletion. Redistribution is for deletion too.

---

## Q15. A node that contains one key and two children is called a ______.

**Correct Answer: a. 2-node** ✅

**Explanation:** Named by number of children:
- 2-node: 1 key, **2** children
- 3-node: 2 keys, 3 children
- 4-node: 3 keys, 4 children

---

## Q16. ______ implementation is O(log n) on retrieval of an item.

**Correct Answer: c. Sorted array-based** ✅

**Explanation:** Only **sorted array** supports binary search → O(log n). Linked list (pointer-based) cannot do binary search (no random access). Unsorted → O(n) linear search.

---

## Q17. If we insert 1, 2, 3, 8, 6, 4, 7 one by one to build a 2-3-4 tree, there are ______ nodes in total.

**Correct Answer: a. 4** ✅

**Explanation (step-by-step):**
1. Insert 1: [1] — 1 node
2. Insert 2: [1,2] — 1 node
3. Insert 3: [1,2,3] — 1 node (full 4-node)
4. Insert 8: split [1,2,3], promote 2 → root=[2], left=[1], right=[3,8] — 3 nodes
5. Insert 6: → right becomes [3,6,8] — 3 nodes
6. Insert 4: [3,4,6,8] overflow → split, promote 6 → root=[2,6], children=[1],[3,4],[8] — 4 nodes
7. Insert 7: 7 goes into [8] → [7,8] — **4 nodes** total

---

## Q18. A 4-node contains at most ______ keys.

**Correct Answer: d. three** ✅

**Explanation:** A 4-node has 4 children and exactly **3 keys**. Formula: k-node has k-1 keys.

---

## Q19. Insertion of an item into a 2-3-4 tree is ______.

**Correct Answer: c. O(log n)** ✅

**Explanation:** 2-3-4 tree uses **top-down insertion**: split 4-nodes on the way down, insert at leaf. Single pass = **O(log n)**. More efficient than 2-3 tree (no bottom-up backtracking needed).

---

## Q20. Which of the following is FALSE about 2-3-4 trees?

**Correct Answer: b. Insertion on a 2-3-4 tree requires more steps than that on a 2-3 tree** ✅

**Explanation:** This is **FALSE**. 2-3-4 tree insertion is actually **faster** than 2-3 tree insertion because:
- 2-3-4: Top-down splits, single pass, no backtracking
- 2-3: Bottom-up splits, may need to travel back up to root

---

## Summary Table

| Q  | Question (Short)                              | Correct Answer                       | Result |
|----|-----------------------------------------------|--------------------------------------|--------|
| 1  | Max nodes in 2-3 tree, height 5               | a. 121                               | ✅     |
| 2  | Node with 2 keys & 3 children                 | d. 3-node                            | ✅     |
| 3  | Keys per node in 2-3-4 tree                   | c. one, two or three                 | ✅     |
| 4  | TRUE about 2-3-4 tree                         | a. at most 4 children per node       | ✅     |
| 5  | NOT a step for 2-3 tree insertion             | c. merge two leaves                  | ✅     |
| 6  | Keys in node with 3 children (2-3-4)          | d. two                               | ✅     |
| 7  | Search complexity on 2-3-4 tree               | d. O(log n)                          | ✅     |
| 8  | Deletion complexity in 2-3 tree               | a. O(log n)                          | ✅     |
| 9  | Min height of 2-3-4 tree with 300 items       | c. 5                                 | ❌     |
| 10 | Max height of 2-3 tree with 1023 items        | b. 10                                | ✅     |
| 11 | Min height of BST with 1023 items             | c. 10                                | ✅     |
| 12 | Insertion complexity in 2-3 tree              | c. O(log n)                          | ✅     |
| 13 | FALSE about linear ADT table implementations  | b. Unsorted array O(n) on insert     | ❌     |
| 14 | What occurs during 2-3 tree insertion         | c. Splitting nodes                   | ✅     |
| 15 | Node with 1 key & 2 children                  | a. 2-node                            | ✅     |
| 16 | O(log n) retrieval implementation             | c. Sorted array-based                | ✅     |
| 17 | Nodes in 2-3-4 tree (insert 1,2,3,8,6,4,7)   | a. 4                                 | ✅     |
| 18 | Max keys in a 4-node                          | d. three                             | ✅     |
| 19 | Insertion complexity in 2-3-4 tree            | c. O(log n)                          | ✅     |
| 20 | FALSE about 2-3-4 trees                       | b. Insertion requires more steps     | ✅     |

**Total Score: 90 / 100 (18/20 correct)**

### Key Concepts to Remember:
- **Node naming**: k-node = k children, k-1 keys
- **2-3 tree insertion**: bottom-up split on overflow
- **2-3-4 tree insertion**: top-down split (more efficient)
- **Merge**: only happens during DELETION (underflow)
- **Split**: only happens during INSERTION (overflow)
- **Sorted array**: only structure with O(log n) retrieval via binary search
- Height formula: 2-3 tree with n items → max height = log2(n+1)

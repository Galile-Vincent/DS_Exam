# Exam All

## Exam1

1. Q: In a heap, the element with the highest priority value is always stored at the ______.
   A: a. root

2. Q: A heap is a ______.
   A: a. complete binary tree

3. Q: Which of the following operations about heap is O(log n)?
   A: a. reheap the element at the root down to its position

4. Q: Given an array of 50 values, we can make it into a heap by calling heapRebuild(i), where i = ___, ..., 1, 0.
   A: c. 24

5. Q: Which of the following is false about the heapsort?
   A: d. it needs n-1 passes to convert the input array into a heap

6. Q: If we make the array {6, 5, 4, 3, 2, 1} into a min-heap by calling heapRebuild, the value at the bottom is __.
   A: c. 6

7. Q: Which of the following is false about a heap?
   A: b. each node has a higher priority value than its parent

8. Q: Which of the following is true about the binary tree built in Huffman coding?
   A: b. a priority queue can be used to build the binary tree

9. Q: Which of the following is true about the heapsort?
   A: a. the heapsort does not require a second array

10. Q: If we insert 4, 5, 7, 1, 6, 2, 9 one by one to build a max-heap, the value stored at the bottom is ______.
   A: a. 5

11. Q: If the ____ algorithm is used as a priority queue, the pqDelete operation is O(1), while the pqInsert operation is O(n).
   A: b. insertion sort

12. Q: Which of the following is true about the differences between heaps and binary search trees?
   A: a. BSTs can be viewed as being sorted but heaps are not

13. Q: If we insert 7, 9, 4, 6, 8, 3 one by one to build a max-heap, its pre-order traversal sequence will be ______.
   A: a. 9, 8, 6, 7, 4, 3

14. Q: The first item to be removed from a priority queue is the item _____.
   A: b. with the highest priority value

15. Q: Which of the following is false about the priority queue implemented by a binary search tree?
   A: a. the root has the highest priority value

16. Q: If we insert 7, 9, 4, 6, 8, 3 one by one to build a max-heap, its post-order traversal sequence will be ______.
   A: Correct: 6, 7, 8, 3, 4, 9

17. Q: If we make the array {7, 3, 4, 6, 8, 9} into a max-heap by calling heapRebuild, the value at the bottom is __.
   A: Correct: 4

18. Q: Given an array of 25 values, we can make it into a heap by calling heapRebuild(i), where i = ___, ..., 1, 0.
   A: Correct: 11

19. Q: If the ____ algorithm is used as a priority queue, the pqInsert operation is O(1), while the pqDelete operation is O(n).
   A: a. selection sort

20. Q: If we insert 4, 5, 7, 1, 6, 9, 2 one by one to build a min-heap, the value stored at the bottom is ______.
   A: d. 7

## Exam2

1. Q: If we insert 1, 2, 3, 8, 6, 4, 7 one by one to build a DEAP, the item on the leftmost node is ______.
   A: b. 6

2. Q: In an array-based implementation of a DEAP, items[____] is on the min-heap.
   A: d. 150

3. Q: Which of the following is NOT a correct step for deleting the minimum from a min-max heap?
   A: c. re-heap down the item from its smaller child if it is larger than its smaller child

4. Q: The root of a DEAP (double-ended heap) always keeps ______.
   A: a. nothing

5. Q: The merge operation of binomial heap is ______.
   A: a. O(log n)

6. Q: If we insert 4, 5, 7, 1, 6, 9, 2 one by one to build a DEAP, the item on the leftmost node is ______.
   A: a. 5

7. Q: If we insert 4, 5, 7, 1, 6, 9, 2 one by one to build a min-max heap, the item on the leftmost node is ______.
   A: b. 4

8. Q: In an array-based implementation of a DEAP, items[____] is on the max-heap.
   A: b. 240

9. Q: The ______ operation is NOT supported by binomial heap.
   A: b. search

10. Q: If we insert 7, 9, 4, 6, 8, 3 one by one to build a min-max heap, its in-order traversal sequence is ______.
   A: d. 6, 9, 8, 3, 4, 7

11. Q: The ______ operation is supported by Fibonacci heap, instead of binomial heap.
   A: b. decrease

12. Q: Which of the following is NOT needed for the insertion procedure of min-max heap?
   A: c. swap with its smaller child

13. Q: If we insert 7, 9, 4, 6, 8, 3 one by one to build a DEAP, the item at the bottom is ______.
   A: a. 6

14. Q: In an array-based implementation of a min-max heap, the grandchildren of items[50] are _______.
   A: c. item[203], item[204], item[205], item[206]

15. Q: If we insert 4, 5, 7, 1, 6, 9, 2 one by one to build a binomial heap, the roots on the linked list are ______.
   A: c. 1, 2, 6

16. Q: A binomial tree of order k is merged by two binomial trees of order ______.
   A: b. k - 1

17. Q: In an array-based implementation of a min-max heap, the grandchildren of items[i] are _______.
   A: b. item[i*4 + j], j = 3, 4, 5, 6

18. Q: ______ are easy to be merged together.
   A: b. Fibonacci heaps

19. Q: ______ is a double-ended priority queue.
   A: a. Min-max heap

20. Q: Which of the following is FALSE about min-max heap?
   A: d. below the root, a min-heap is its left subtree and a max-heap is its right subtree

## Exam3

1. Q: A 2-3 tree of height 5 has at most ______ nodes.
   A: a. 121

2. Q: A node that contains two keys and three children is called a ______.
   A: d. 3-node

3. Q: Each node in a 2-3-4 tree contains ______ keys.
   A: c. one, two or three

4. Q: Which of the following is TRUE about 2-3-4 tree?
   A: a. each node has at most 4 children

5. Q: Which is NOT a step for inserting a new key into a 2-3 tree?
   A: c. merge two leaves into one node if necessary

6. Q: If a node in a 2-3-4 tree has three children, it must contain ______ keys.
   A: d. two

7. Q: Search of an item on a 2-3-4 tree is ______.
   A: d. O(log n)

8. Q: Deletion of an item from a 2-3 tree is ______.
   A: a. O(log n)

9. Q: The height of a 2-3-4 tree that contains 300 items is at least ______.
   A: c. 5

10. Q: The height of a 2-3 tree that contains 1023 items is at most ______.
   A: b. 10

11. Q: The height of a binary search tree that contains 1023 items is at least ______.
   A: c. 10

12. Q: Insertion of an item into a 2-3 tree is ______.
   A: c. O(log n)

13. Q: Which is FALSE about linear implementations of ADT table?
   A: b. Unsorted array-based implementation is O(n) on insertion

14. Q: _______ may occur during insertion of a new key into a 2-3 tree.
   A: c. Splitting nodes

15. Q: A node that contains one key and two children is called a ______.
   A: a. 2-node

16. Q: ______ implementation is O(log n) on retrieval of an item.
   A: c. Sorted array-based

17. Q: Insert 1, 2, 3, 8, 6, 4, 7 into a 2-3-4 tree: total nodes?
   A: a. 4

18. Q: A 4-node contains at most ______ keys.
   A: d. three

19. Q: Insertion of an item into a 2-3-4 tree is ______.
   A: c. O(log n)

20. Q: Which is FALSE about 2-3-4 trees?
   A: b. Insertion requires more steps than 2-3 tree

21. Q: Insert 4, 5, 7, 1, 6, 9, 3 into a 2-3 tree: root key?
   A: b. 5

22. Q: In a 2-3-4 tree, when a node is split, its parent cannot be a _____.
   A: a. 4-node

23. Q: ______ is NOT a balanced search tree.
   A: c. Heap

24. Q: In a 2-3 tree, what happens first if the key is deleted from an internal node?
   A: b. swap it with the in-order successor

25. Q: Binary search tree implementation is O(n) on ______.
   A: a. traversal of all items

26. Q: Which is FALSE about balanced search trees?
   A: c. 2-3 tree is a binary tree

27. Q: When the root of a 2-3 tree has no item after deleting a key, we _______.
   A: b. remove the root

28. Q: ______ is a tree in which all leaves are at the same level.
   A: b. 2-3 tree

29. Q: The balance of a _______ is sensitive to insertion order.
   A: d. binary search tree

30. Q: A 2-3 tree of height 5 has at least ______ nodes.
   A: c. 31

## Exam4

1. Q: If we insert 3, 5, 6, 7, 9, 8 one by one to build a red-black tree...
   A: b. 5

2. Q: On a red-black tree, if a node has only one child...
   A: b. the node, its child

3. Q: ______ is a balanced binary search tree.
   A: b. Red-black tree

4. Q: If we insert 1, 2, 3, …, 32 one by one to build a red-black tree...
   A: b. 5

5. Q: Which of the following is TRUE about a red-black tree?
   A: a. every external path cannot have two consecutive red pointers

6. Q: On a red-black tree, if a leaf is pointed to by a red pointer...
   A: a. if it has a sibling, the sibling must be pointed to by a red pointer

7. Q: If we insert 1, 4, 5, 7, 6, 9, 3 one by one to build an AVL tree...
   A: d. 6

8. Q: ______ is NOT a balanced search tree.
   A: d. Min-max heap

9. Q: If we insert 1, 2, 3, …, 32 one by one to build an AVL tree...
   A: c. 6

10. Q: In an AVL tree, each ______.
   A: c. internal node is a 2-node

11. Q: In AVL trees, if the balance factor of a node is -2, we check...
   A: b. its right child

12. Q: In AVL trees, if the balance factor of a node is +2, we check...
   A: a. its left child

13. Q: If we insert 1, 4, 5, 7, 6, 9, 3 one by one to build a red-black tree...
   A: d. 3

14. Q: After adding a new node X into an AVL tree, we must check...
   A: c. X's ancestors

15. Q: If we insert 1, 2, 3, …, 9 one by one to build a red-black tree...
   A: c. 4

16. Q: If we insert 1, 2, 3, 8, 6, 4, 7 one by one to build a red-black tree...
   A: d. 2

17. Q: In AVL trees, balance factor -2 and right child -1 or 0...
   A: a. -1 or 0

18. Q: The balance of a ______ is sensitive to the order of insertion.
   A: d. red-black tree

19. Q: In the red-black representation of a 2-3-4 tree, every 2-node has...
   A: a. 0

20. Q: In the red-black representation of a 2-3-4 tree, every 4-node has...
   A: a. 2

## Exam5

1. Q: The load factor of a hash table is defined as ______.
   A: a. the current number of table items / the table size

2. Q: With quadratic probing on a hash table of 10 locations, if there are totally 4 items in consecutive locations, the average length of the probe sequence for any unsuccessful search is equal to ______.
   A: a. 1.7

3. Q: A ______ occurs when a hash function maps two or more distinct search keys into the same location.
   A: b. collision

4. Q: ______ is a collision-resolution scheme that accommodates more than one item in the same location.
   A: c. Separate chaining

5. Q: Which of the following is FALSE about double hashing?
   A: c. The second hash function returns the second location

6. Q: 令雜湊表hash table大小為11，若每個位置只存放一筆資料，一旦存入達到5筆資料，發生碰撞collision的機率就會超過60%。
   A: b. Agree

7. Q: 某些碰撞解法可以互補，並不互相衝突。以下組合哪些是可行的？
   A: b. 雙重雜湊double hash + bucket, c. 分開鏈結separate chaining + bucket

8. Q: Which of the following is NOT a problem of linear probing?
   A: d. The probe sequence may not visit every location in the hash table

9. Q: Given a hash table of 365 locations, the probability of a collision is higher than 50% if at least ______ items are assigned.
   A: b. 23

10. Q: With linear probing on a hash table of 100 locations, if there are totally 19 items in consecutive locations, the average length of the probe sequence for any unsuccessful search is equal to ______.
   A: d. 2.9

11. Q: 運用雙重雜湊double hash作為雜湊表的碰撞解法collision resolution，搜尋存在值的比較次數number of comparisons等於其探索次數number of probes。
   A: a. Disagree

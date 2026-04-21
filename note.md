# 1142 資料結構與演算法期中考複習筆記 (單元 1-5)

## 演算法時間複雜度比較表

| 資料結構 / 演算法 | 搜尋 (Search) | 插入 (Insert) | 刪除 (Delete) | 合併 (Merge) | 特色 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Binary Search Tree** | $O(n)$ | $O(n)$ | $O(n)$ | $O(n)$ | 視插入順序而定，可能退化成鏈狀 |
| **Max/Min Heap** | $O(n)$ | $O(\log n)$ | $O(\log n)$ | $O(n)$ | 完全二元樹 (Complete BT)，優先佇列實作 |
| **Min-Max Heap** | $O(n)$ | $O(\log n)$ | $O(\log n)$ | $O(n)$ | 雙向優先佇列 (DEPQ)，層級交替 Min/Max |
| **DEAP** | $O(n)$ | $O(\log n)$ | $O(\log n)$ | $O(n)$ | 雙向優先佇列，Root 為空，左 Min 右 Max |
| **Binomial Heap** | $O(n)$ | $O(\log n)$ | $O(\log n)$ | $O(\log n)$ | 由 Binomial Trees 組成，合併效率高 |
| **Fibonacci Heap** | $O(n)$ | $O(1)^*$ | $O(\log n)^*$ | $O(1)^*$ | $*$均攤時間 (Amortized)，適合大量合併/降低鍵值 |
| **2-3 Tree** | $O(\log n)$ | $O(\log n)$ | $O(\log n)$ | - | 絕對平衡，所有葉子在同一層，由下而上生長 |
| **2-3-4 Tree** | $O(\log n)$ | $O(\log n)$ | $O(\log n)$ | - | 搜尋更穩定，由上而下分裂 (Top-down) |
| **AVL Tree** | $O(\log n)$ | $O(\log n)$ | $O(\log n)$ | - | 嚴格平衡，平衡係數 (BF) 限制為 -1, 0, 1 |
| **Red-Black Tree** | $O(\log n)$ | $O(\log n)$ | $O(\log n)$ | - | 2-3-4 樹的二元表示，無連續紅指標，適合頻繁插入刪除 |
| **Hash Table** | $O(1)_{avg}$ | $O(1)_{avg}$ | $O(1)_{avg}$ | - | 取決於負載因子 (Load Factor) 與碰撞處理方式 |

---

## 單元 1：優先佇列與堆積 (Priority Queue & Heap)

### 1. 基本概念
- **Priority Queue (PQ)**: 非先進先出，而是由權重 (Priority) 決定誰先離開。
- **Heap**: 是一種 **完全二元樹 (Complete Binary Tree)**。
  - **Max-Heap**: 每個節點的值 $\ge$ 子節點。
  - **Min-Heap**: 每個節點的值 $\le$ 子節點。
  - **Array 實作**: 節點 $i$ 的左子節點為 $2i$，右子節點為 $2i+1$，父節點為 $\lfloor i/2 \rfloor$ (1-indexed)。

### 2. 堆積運算
- **Insert (Sift-up)**: 加在最後一個位置，往上跟父節點比較並交換。
- **Delete (Sift-down)**: 將最後一個節點移到根節點，往下跟較大/較小的子節點交換。
- **Build Heap**: 呼叫 `heapRebuild`，從 index $\lfloor n/2 \rfloor$ 到 0 進行 sift-down。時間複雜度為 $O(n)$。

### 3. Heap Sort
1. 先將陣列轉成 Heap ($O(n)$)。
2. 重複把根節點 (最大/最小) 與最後一個元素交換，縮小範圍並重新調整根節點。
3. 總時間複雜度 $O(n \log n)$。

---

## 單元 2：堆積變形 (Advanced Heaps)

### 1. Double-Ended Priority Queue (DEPQ)
- **Min-Max Heap**:
  - Root 為 Min，第 1 層為 Max，第 2 層為 Min，依此類推。
  - 插入時判斷所在層級，再跟父節點比較決定往上或往下調整。
- **DEAP (Double-Ended Heap)**:
  - **Root 為空**。
  - 左子樹為 Min-Heap，右子樹為 Max-Heap。
  - 對應關係：左子樹位置 $i$ 對應右子樹 $i + 	ext{offset}$，確保 $Min[i] \le Max[i']$。

### 2. Mergeable Heaps
- **Binomial Heap**:
  - 由一組二項式樹 ($B_k$) 組成。
  - 合併兩個 $B_{k-1}$ 變成 $B_k$。
  - 合併過程類似二進位加法，最多 $\log n$ 棵樹。
- **Fibonacci Heap**:
  - 延遲合併 (Lazy merging)，插入只需 $O(1)$。
  - `Decrease Key` 操作在特定條件下僅需 $O(1)$。

---

## 單元 3：2-3 樹與 2-3-4 樹

### 1. 2-3 Tree
- **2-node**: 1 個 Key, 2 個子節點。
- **3-node**: 2 個 Keys, 3 個子節點。
- **特色**: 絕對平衡 (All leaves at the same level)。
- **插入**:
  - 找到葉子後插入。
  - 若變成 3 個 Keys (overflow)，中間值提升至父節點，節點分裂 (Split)。
- **刪除**:
  - 與 In-order Successor 交換。
  - 若造成空節點 (underflow)，嘗試跟兄弟借 (Redistribute) 或合併 (Merge)。

### 2. 2-3-4 Tree
- 允許 **4-node** (3 個 Keys, 4 個子節點)。
- **Top-down Split**: 搜尋路徑上遇到 4-node 就先分裂，避免刪除時的回溯，更有效率。

---

## 單元 4：平衡二元搜尋樹 (AVL & Red-Black Tree)

### 1. AVL Tree
- 限制：任何節點的左右子樹高度差 (Balance Factor, BF) 為 $-1, 0, 1$。
- **旋轉 (Rotation)**:
  - **LL / RR**: 單一旋轉。
  - **LR / RL**: 複式旋轉。
  - **例子**: 插入造成左子樹太重且其左子樹偏重 (LL)，則對問題點進行右旋。

### 2. Red-Black Tree
- 性質：
  1. 節點非紅即黑。
  2. Root 必為黑。
  3. 紅節點不可連續 (紅父必黑子)。
  4. 從任一節點到葉子的路徑中，黑色節點數量相同 (Black-Height)。
- **與 2-3-4 樹關係**:
  - 一個黑色節點帶著紅色的子節點，就代表一個 2-3-4 的寬節點。

---

## 單元 5：雜湊 (Hashing)

### 1. 雜湊函數與碰撞
- **Load Factor ($\lambda$)**: $n / 	ext{table\_size}$。
- **Collision**: 不同 Key 算出相同 Hash Value。

### 2. 碰撞處理 (Collision Resolution)
- **Open Addressing (開放定址法)**:
  - **Linear Probing**: 順序找下一個。缺點：Primary Clustering (群聚現象)。
  - **Quadratic Probing**: 找 $i^2, -i^2$。缺點：Secondary Clustering，且不一定能找遍全表。
  - **Double Hashing**: 第二個雜湊函數決定 **步長 (Step size)**。
- **Separate Chaining (分開鏈結法)**:
  - 每個 Slot 接一個 Linked List。適合 $\lambda > 1$ 的情況。

### 3. 例子
- **Linear Probing 刪除**: 不能直接清空，否則會斷開搜尋路徑。需設標記 (Deleted) 或重排。
- **Birthday Problem**: 在 365 大小的表，只需 23 筆資料，碰撞機率就大於 50%。

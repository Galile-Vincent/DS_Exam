# 單元5評量 - Hash Table Quiz

## 1142 資料結構與演算法 | Score: 100/100

---

## Quick View：單元5評量 Q1-Q10

| 題號 | 試題重點 | 正確答案 | 結果 |
|---|---|---|---|
| 1 | The load factor of a hash table is defined as ______. | a. the current number of table items / the table size | ✅ |
| 2 | With quadratic probing on a hash table of 10 locations, if there are totally 4 items in consecutive locations, the average length of the probe sequence for any unsuccessful search is equal to ______. | a. 1.7 | ✅ |
| 3 | A ______ occurs when a hash function maps two or more distinct search keys into the same location. | b. collision | ✅ |
| 4 | ______ is a collision-resolution scheme that accommodates more than one item in the same location. | c. Separate chaining | ✅ |
| 5 | Which of the following is FALSE about double hashing? | c. The second hash function returns the second location | ✅ |
| 6 | 令雜湊表hash table大小為11，若每個位置只存放一筆資料，一旦存入達到5筆資料，發生碰撞collision的機率就會超過60%。 | b. Agree | ✅ |
| 7 | 某些碰撞解法可以互補，並不互相衝突。以下組合哪些是可行的？ | b. 雙重雜湊double hash + bucket, c. 分開鏈結separate chaining + bucket | ✅ |
| 8 | Which of the following is NOT a problem of linear probing? | d. The probe sequence may not visit every location in the hash table | ✅ |
| 9 | Given a hash table of 365 locations, the probability of a collision is higher than 50% if at least ______ items are assigned. | b. 23 | ✅ |
| 10 | With linear probing on a hash table of 100 locations, if there are totally 19 items in consecutive locations, the average length of the probe sequence for any unsuccessful search is equal to ______. | d. 2.9 | ✅ |
運用雙重雜湊double hash作為雜湊表的碰撞解法collision resolution，搜尋存在值的比較次數number of comparisons等於其探索次數number of probes。 Answer: Disgree

**Total Score: 100 / 100（10/10 correct）**

---

## 試題 1

**The load factor of a hash table is defined as ______.**

> **正確答案：a. the current number of table items / the table size** ✅  
> Load factor = (number of items currently in the table) / (table size).  
> It measures how full the hash table is. A higher load factor increases the probability of collision.

---

## 試題 2

**With quadratic probing on a hash table of 10 locations, if there are totally 4 items in consecutive locations, the average length of the probe sequence for any unsuccessful search is equal to ______.**

> **正確答案：a. 1.7** ✅  
> For quadratic probing, the average unsuccessful probe length is approximately 1 / (1 - load factor).  
> Load factor = 4/10 = 0.4, so 1 / (1 - 0.4) = 1 / 0.6 ≈ 1.67 ≈ **1.7**.

---

## 試題 3

**A ______ occurs when a hash function maps two or more distinct search keys into the same location.**

> **正確答案：b. collision** ✅  
> A **collision** happens when two different keys hash to the same index.  
> Collision resolution strategies include linear probing, quadratic probing, double hashing, and separate chaining.

---

## 試題 4

**______ is a collision-resolution scheme that accommodates more than one item in the same location.**

- a. Quadratic probing
- b. Double hashing
- **c. Separate chaining** ✅
- d. Linear probing

> **正確答案：c. Separate chaining**  
> Separate chaining stores multiple items at the same index using a linked list (or other data structure).  
> Open addressing schemes (linear probing, quadratic probing, double hashing) find another empty slot instead.

---

## 試題 5

**Which of the following is FALSE about double hashing?**

- a. The first hash function returns the first location
- b. It uses two hash functions to reduce clustering problems
- **c. The second hash function returns the second location** ✅
- d. It creates key dependent probe sequences

> **正確答案：c. The second hash function returns the second location**（此敘述為 FALSE）  
> The second hash function in double hashing returns the **step size** (probe increment), NOT the second location.  
> The probe sequence is: h1(k), h1(k) + h2(k), h1(k) + 2*h2(k), ...

---

## 試題 6

**令雜湊表hash table大小為11，若每個位置只存放一筆資料，一旦存入達到5筆資料，發生碰撞collision的機率就會超過60%。**

- a. Disagree
- **b. Agree** ✅

> **正確答案：b. Agree**  
> P(no collision with 5 items in table of 11) = 11/11 * 10/11 * 9/11 * 8/11 * 7/11  
> = 10 * 9 * 8 * 7 / 11^4 = 5040 / 14641 ≈ 0.344  
> P(collision) = 1 - 0.344 = 0.656 > 60%, so **Agree**.

---

## 試題 7

**某些碰撞解法可以互補，並不互相衝突。例如，以下組合哪些是可行的？**

- a. 線性探索linear probing + 雙重雜湊double hash
- **b. 雙重雜湊double hash + bucket** ✅
- **c. 分開鏈結separate chaining + bucket** ✅
- d. 平方探索quadratic probing + 分開鏈結separate chaining

> **正確答案：b & c**  
> - **Double hash + bucket**: Double hashing determines the slot, bucket stores multiple items at that slot — complementary.  
> - **Separate chaining + bucket**: Separate chaining uses linked structures; each chain node can be a bucket — complementary.  
> - Linear probing and double hashing are both open addressing — they conflict.  
> - Quadratic probing and separate chaining are fundamentally different approaches — they conflict.

---

## 試題 8

**Which of the following is NOT a problem of linear probing?**

- a. Items tend to cluster together and large clusters tend to get even larger
- b. Empty locations after deletions would incorrectly stop a probe sequence
- c. Large clusters cause long probing sequences
- **d. The probe sequence may not visit every location in the hash table** ✅

> **正確答案：d. The probe sequence may not visit every location in the hash table**  
> This is NOT a problem of linear probing — linear probing **does** visit every location (step size is 1, so it cycles through all slots).  
> This is actually a potential problem with **quadratic probing**, where the probe sequence may not cover all slots.

---

## 試題 9

**Given a hash table of 365 locations, the probability of a collision is higher than 50% if at least ______ items are assigned.**

- a. 20
- **b. 23** ✅
- c. 22
- d. 21

> **正確答案：b. 23**  
> This is the classic "Birthday Problem" with 365 days.  
> P(no collision with n items) = 365/365 * 364/365 * 363/365 * ... * (365-n+1)/365  
> At n = 22: P(no collision) ≈ 0.524 → P(collision) ≈ 47.6% < 50%  
> At n = 23: P(no collision) ≈ 0.493 → P(collision) ≈ 50.7% > 50%  
> Therefore, at least **23** items are needed.

---

## 試題 10

**With linear probing on a hash table of 100 locations, if there are totally 19 items in consecutive locations, the average length of the probe sequence for any unsuccessful search is equal to ______.**

- a. 50.5
- b. 11.05
- c. 2.1
- **d. 2.9** ✅

> **正確答案：d. 2.9**  
> For a cluster of size s, the average unsuccessful probe length = (s + 1) / 2 * (2 - (s+1)/n) + 1 is complex.  
> Using the approximation for linear probing: Unsuccessful avg = (1 + 1/(1-λ)^2) / 2 where λ = load factor.  
> However, for a cluster of 19 consecutive items, the direct calculation gives:  
> The 19 occupied consecutive slots each have probe lengths of 1, 2, ..., 19, 20 for the cells from last occupied + 1 back through the cluster.  
> Weighted average = (1 + 2 + ... + 20) / 100 + contributions from empty slots ≈ **2.9**.

---

## Key Concepts to Remember

- **Load factor (λ)**: λ = number of items / table size; higher λ → more collisions
- **Collision**: occurs when two keys hash to the same location
- **Linear probing**: step size = 1; visits all slots but causes **primary clustering**
- **Quadratic probing**: step size = i²; reduces clustering but may not visit all slots
- **Double hashing**: step size determined by second hash function; key-dependent, reduces clustering
- **Separate chaining**: multiple items at same index via linked list; no need to find new slot
- **Bucket hashing**: each slot holds multiple items
- **Birthday problem**: with 365 slots, need only 23 items for >50% collision probability
- **False statement about double hashing**: second hash function returns step size, NOT second location
- **NOT a problem of linear probing**: failing to visit all locations (that's quadratic probing's issue)

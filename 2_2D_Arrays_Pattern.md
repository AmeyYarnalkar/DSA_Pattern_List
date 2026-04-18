# 2D Arrays (Matrix) 

##  1. Spiral Traversal (Layer Shrinking)

###  Pattern

Traverse matrix in layers using 4 boundaries.

###  Variables

```
top, bottom, left, right
```

###  Flow

* left → right (top row)
* top → bottom (right column)
* right → left (bottom row)
* bottom → top (left column)

###  Update

```
top++, bottom--, left++, right--
```

###  Pitfalls

* Missing boundary checks → duplicates
* Incorrect loop order

###  Problems

* Spiral Matrix (LC 54)
* Spiral Matrix II (LC 59)
* Spiral Matrix III (LC 885)

---

##  2. Matrix Rotation (In-place)

###  Pattern

Transform instead of simulating rotation.

###  Steps

1. Transpose
2. Reverse each row

###  Key Relation

```
matrix[i][j] ↔ matrix[j][i]
```

###  Pitfalls

* Using extra space
* Wrong order of operations

###  Problems

* Rotate Image (LC 48)
* Set Matrix Zeroes (LC 73)
* Game of Life (LC 289)

---

##  3. Diagonal Traversal

###  Pattern

Use index relationships.

###  Conditions

```
Main diagonal: i == j
Anti-diagonal: i + j == n - 1
```

###  Approach

* Fix starting point
* Move diagonally

###  Pitfalls

* Direction switching errors
* Index out of bounds

###  Problems

* Diagonal Traverse (LC 498)
* Sort Matrix Diagonally (LC 1329)
* Toeplitz Matrix (LC 766)

---

##  4. Search in Sorted Matrix

###  Pattern

Eliminate row/column at each step.

###  Start Point

Top-right corner

###  Logic

* target < current → move left
* target > current → move down

### ⏱ Complexity

```
O(n + m)
```

###  Pitfalls

* Applying binary search incorrectly

###  Problems

* Search 2D Matrix II (LC 240)
* Search 2D Matrix (LC 74)
* Kth Smallest in Sorted Matrix (LC 378)

---

##  5. Grid DFS / BFS

###  Pattern

Treat matrix as graph.

###  Directions

```
up, down, left, right
```

###  Use Cases

* Connected components
* Shortest path
* Flood fill

###  Pitfalls

* Not marking visited
* Infinite loops

###  Problems

* Number of Islands (LC 200)
* Rotting Oranges (LC 994)
* Shortest Path in Binary Matrix (LC 1091)

---

##  6. 2D Prefix Sum

###  Pattern

Precompute for fast queries.

###  Formula

```
sum = A - B - C + D
```

###  Use Case

* Submatrix sum queries

###  Pitfalls

* Index mismanagement
* Boundary errors

###  Problems

* Range Sum Query 2D (LC 304)
* Matrix Block Sum (LC 1314)
* Max Sum Rectangle ≤ K (LC 363)

---

##  7. Boundary Traversal

###  Pattern

Traverse only outer edges.

###  Flow

* Top row
* Right column
* Bottom row (reverse)
* Left column (reverse)

###  Pitfalls

* Corner duplication

###  Problems

* Boundary Traversal (GFG)
* Spiral Matrix (LC 54)
* Matrix Layer Rotation (HackerRank)

---

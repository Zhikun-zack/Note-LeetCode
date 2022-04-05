---
description: https://www.youtube.com/watch?v=eLlZEYzZVyQ  https://zxi.mytechroad.com/blog/
---

# DP

* [x] [LC 63 Unique Paths II](by-number/50-100.md#63.-unique-paths-ii)
* [x] [303 Range Sum Query - Immutable](by-number/300-350.md#303-range-sum-query-immutable-easy)
* [x] [576 Out of Boundary Paths](by-number/550-600.md#576.-out-of-boundary-paths)
* [x] [688 Knight Probability in Chessboard](by-number/650-700.md#688.-knight-probability-in-chessboard)
* [x] [**746**](by-number/700-750.md#746-min-cost-climbing-stairs) **Min Cost Climbing Stairs**
* [ ] [**790 Domino and Tromino Tiling**](by-number/750-800.md#790-domino-and-tromino-tiling)
* [ ] [**1137**](by-number/1100-1150.md#1137-n-th-tribonacci-number) **Nth Tribonacci number**
* [x] [1218 Longest Arithmetic Subsequence of Given Difference](by-number/1200-1250.md#1218-longest-arithmetic-subsequence-of-given-difference-medium)
* [x] [#1027-longest-arithmetic-subsequence-m](by-number/1000-1050.md#1027-longest-arithmetic-subsequence-m "mention")

| Number                                                                                     | Similiar Probs                                                                                                                                   | Description        |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------ |
| [303 Range Sum Query - Immutable](by-number/300-350.md#303-range-sum-query-immutable-easy) | [1218 Longest Arithmetic Subsequence of Given Difference](by-number/1200-1250.md#1218-longest-arithmetic-subsequence-of-given-difference-medium) | ++++++++++++++++++ |
|                                                                                            |                                                                                                                                                  |                    |
|                                                                                            |                                                                                                                                                  |                    |
|                                                                                            |                                                                                                                                                  |                    |
|                                                                                            |                                                                                                                                                  |                    |
|                                                                                            |                                                                                                                                                  |                    |
|                                                                                            |                                                                                                                                                  |                    |
|                                                                                            |                                                                                                                                                  |                    |
|                                                                                            |                                                                                                                                                  |                    |

## Type: 1

### Description

* Input: O(n)
* dp\[i]: optimized solution for ith problem
* dp\[i] dependents on its sub problems
* T Com O(N)
* S Com O(N) -> O(1)

### Problems

1. [**LC 746**](by-number/700-750.md#746-min-cost-climbing-stairs) **Min Cost Climbing Stairs**
   * dp\[i] = min cost to climb to i stairs
   * dp\[i] = min(dp\[i-1] + cost\[i-1] , dp\[i-2] + cost\[i-2])
2. **\*\*\*\***[**LC 1137**](by-number/1100-1150.md#1137-n-th-tribonacci-number) **Nth Tribonacci number**
   * dp\[i] = ith Tribonacci number
   * dp\[i] = dp\[i-1]+dp\[i-2]+dp\[i-3]
   * Can using dp1 dp2 dp3 and res four vars to represent dp list
3. [**LC 790 Domino and Tromino Tiling**](by-number/750-800.md#790-domino-and-tromino-tiling)
4.

## Type 2

### Description

* Input is O(nm)
* DP is O(nm) can be optimized to O(n) or O(1)(Using the input array to store values)
* T O(N^2) S O(n^2)，O(N) or O(1)

### Problems

[LC 304](by-number/300-350.md#304-range-sum-query-2d-immutable)

[LC 1277](by-number/1200-1250.md#1277-count-square-submatrices-with-all-ones-m)

####

####

## Type: 2.2

### Description:

* Input: O(mn)
* dp\[ k ]\[ i ]\[ j ] = solution of position (i, j) after k steps
* dp\[ k ]\[ i ]\[ j ] = sum(dp\[k-1] \[i']\[j']) sum of values of all prev position
* T Com: O(kmn)
* S Com: O(kmn) -> O(nm)

### Problems

LC 62

[LC 63 Unique Paths II](by-number/50-100.md#63.-unique-paths-ii)

[LC 576 Out of Boundary Paths](by-number/550-600.md#576.-out-of-boundary-paths)

[LC 688 Knight Probability in Chessboard](by-number/650-700.md#688.-knight-probability-in-chessboard)

### Template

```
// Some code
dp = [k][m][n]
for k in k:
    for i in m:
        for j in n:
            dp[k][i][j] = f(dp[k-1][i'][j'])
return 
```

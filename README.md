---
description: https://www.youtube.com/watch?v=eLlZEYzZVyQ
---

# DP

## Type: 1.1

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
2. #### ****[**LC 1137**](by-number/1100-1150.md#1137-n-th-tribonacci-number) **Nth Tribonacci number**
   * dp\[i] = ith Tribonacci number
   * dp\[i] = dp\[i-1]+dp\[i-2]+dp\[i-3]
   * Can using dp1 dp2 dp3 and res four vars to represent dp list
3. ####
4. ####





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

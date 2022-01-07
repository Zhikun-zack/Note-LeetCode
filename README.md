---
description: https://www.youtube.com/watch?v=eLlZEYzZVyQ
---

# DP

## Type: 2.2

### Description:

* Input: O(mn)
* dp\[ k ]\[ i ]\[ j ] = solution of position (i, j) after k steps
* dp\[ k ]\[ i ]\[ j ] = sum(dp\[k-1] \[i']\[j']) sum of values of all prev position
* T Com: O(kmn)
* S Com: O(kmn) -> O(nm)

### Problems

LC 576

[LC 688](by-number/650-700.md#688.-knight-probability-in-chessboard)

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












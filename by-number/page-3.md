# 350-400

* [x] 366 Find Leaves of Binary Tree
*
* [x] 368 Largest Divisible Subset
*
* [x] 378 Kth Smallest Element in a Sorted Matrix
* [x] 395 Longest Substring with At Least K Repeating Characters

## 366 Find Leaves of Binary Tree M

### D



Given the `root` of a binary tree, collect a tree's nodes as if you were doing this:

* Collect all the leaf nodes.
* Remove all the leaf nodes.
* Repeat until the tree is empty.

&#x20;

**Example 1:**

![](https://assets.leetcode.com/uploads/2021/03/16/remleaves-tree.jpg)

```
Input: root = [1,2,3,4,5]
Output: [[4,5,3],[2],[1]]
Explanation:
[[3,5,4],[2],[1]] and [[3,4,5],[2],[1]] are also considered correct answers since per each level it does not matter the order on which elements are returned.
```

**Example 2:**

```
Input: root = [1]
Output: [[1]]
```

&#x20;

**Constraints:**

* The number of nodes in the tree is in the range `[1, 100]`.
* `-100 <= Node.val <= 100`

### S

height(root)=1+max(height(root.left), height(root.right))

```
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def findLeaves(self, root: Optional[TreeNode]) -> List[List[int]]:
        res = collections.defaultdict(list)
        
        def dfs(node,layer):
            if not node:
                return layer
            l = dfs(node.left, layer)
            r = dfs(node.right, layer)
            layer = max(l, r)
            res[layer].append(node.val)

            return layer+1
        dfs(root, 0)
        return res.values()
```

## 368. Largest Divisible Subset

### Description

Given a set of **distinct** positive integers `nums`, return the largest subset `answer` such that every pair `(answer[i], answer[j])` of elements in this subset satisfies:

* `answer[i] % answer[j] == 0`, or
* `answer[j] % answer[i] == 0`

If there are multiple solutions, return any of them.

**Example 1:**

```
Input: nums = [1,2,3]
Output: [1,2]
Explanation: [1,3] is also accepted.
```

**Example 2:**

```
Input: nums = [1,2,4,8]
Output: [1,2,4,8]
```

### Solutions:

```
## https://leetcode-cn.com/problems/largest-divisible-subset/solution/gong-shui-san-xie-noxiang-xin-ke-xue-xi-0a3jc/
class Solution:
    def largestDivisibleSubset(self, nums: List[int]) -> List[int]:
        nums.sort()
        n = len(nums)
        
        # f is the length of subset at that position
        # g is the value of that position
        f, g = [0] * n, [0] * n
        for i in range(n):
            # 至少包含自身一个数，因此起始长度为 1，由自身转移而来
            length, prev = 1, i
            for j in range(i):
                if nums[i] % nums[j] == 0:
                    # 如果能接在更长的序列后面，则更新「最大长度」&「从何转移而来」
                    if f[j] + 1 > length:
                        length = f[j] + 1
                        prev = j
            # 记录「最终长度」&「从何转移而来」
            f[i] = length
            g[i] = prev

        # 遍历所有的 f[i]，取得「最大长度」和「对应下标」
        max_len = idx = -1
        for i in range(n):
            if f[i] > max_len:
                idx = i
                max_len = f[i]
        
        # 使用 g[] 数组回溯出具体方案
        ans = []
        while len(ans) < max_len:
            ans.append(nums[idx])
            idx = g[idx]
        ans.reverse()
        return ans
```

## 378 Largest Divisible Subset

### D



Given an `n x n` `matrix` where each of the rows and columns is sorted in ascending order, return _the_ `kth` _smallest element in the matrix_.

Note that it is the `kth` smallest element **in the sorted order**, not the `kth` **distinct** element.

You must find a solution with a memory complexity better than `O(n2)`.

&#x20;

**Example 1:**

```
Input: matrix = [[1,5,9],[10,11,13],[12,13,15]], k = 8
Output: 13
Explanation: The elements in the matrix are [1,5,9,10,11,12,13,13,15], and the 8th smallest number is 13
```

**Example 2:**

```
Input: matrix = [[-5]], k = 1
Output: -5
```

&#x20;

**Constraints:**

* `n == matrix.length == matrix[i].length`
* `1 <= n <= 300`
* `-109 <= matrix[i][j] <= 109`
* All the rows and columns of `matrix` are **guaranteed** to be sorted in **non-decreasing order**.
* `1 <= k <= n2`

&#x20;

**Follow up:**

* Could you solve the problem with a constant memory (i.e., `O(1)` memory complexity)?
* Could you solve the problem in `O(n)` time complexity? The solution may be too advanced for an interview but you may find reading [this paper](http://www.cse.yorku.ca/\~andy/pubs/X+Y.pdf) fun.

### S

[https://leetcode-cn.com/problems/kth-smallest-element-in-a-sorted-matrix/solution/ci-ti-er-fen-cha-zhao-guo-cheng-de-dong-tu-yan-shi/](https://leetcode-cn.com/problems/kth-smallest-element-in-a-sorted-matrix/solution/ci-ti-er-fen-cha-zhao-guo-cheng-de-dong-tu-yan-shi/)

```

class Solution:
    def kthSmallest(self, matrix: List[List[int]], k: int) -> int:
        n = len(matrix)
        def check(mid):
            """遍历获取较小元素部分元素总数，并与k值比较"""
            i, j = n-1, 0
            num = 0
            while i >= 0 and j < n:
                if matrix[i][j] <= mid:
                    # 当前元素小于mid，则此函数及上方函数均小于mid
                    num += i + 1
                    # 向右移动
                    j += 1
                else:
                    # 当前元素大于mid，则向上移动，直到找到比mid小的值，或者出矩阵
                    i -= 1
            return num >= k
        left, right = matrix[0][0], matrix[-1][-1]
        while left < right:
            mid = (left + right) >> 1
            if check(mid):
                # 满足 num >= k，范围太大，移动right至mid， 范围收缩
                right = mid
            else:
                left = mid + 1
        return left

```

## 395 Longest Substring with At Least K Repeating Characters M

### D



Given a string `s` and an integer `k`, return _the length of the longest substring of_ `s` _such that the frequency of each character in this substring is greater than or equal to_ `k`.

&#x20;

**Example 1:**

```
Input: s = "aaabb", k = 3
Output: 3
Explanation: The longest substring is "aaa", as 'a' is repeated 3 times.
```

**Example 2:**

```
Input: s = "ababbc", k = 2
Output: 5
Explanation: The longest substring is "ababb", as 'a' is repeated 2 times and 'b' is repeated 3 times.
```

&#x20;

**Constraints:**

* `1 <= s.length <= 104`
* `s` consists of only lowercase English letters.
* `1 <= k <= 105`

### S

* Cannot be solved by normal sliding windows, moving l and r will not visit all possible situations
* Have to fix the number of distinct char in the substring
* Get the largest len of valid substring which contains only i distinct chars
* Two ways below: only difference are the range of fixed number
  * first is the len of distinct numbers in string s
  * second is 26

```
class Solution:
    def longestSubstring(self, s: str, k: int) -> int:
        res = 0
        
        num_of_distinct = collections.defaultdict(int);
        for j in s:
            num_of_distinct[j] += 1
        
        # Get the largest len of valid substring which only contains i chars
        for i in range(1, len(num_of_distinct) + 1):
            l, r = 0, 0 
            # Should init dict as dict of int
            hashmap = collections.defaultdict(int)
            sum_ = 0 # Number of distinct characters in substring
            valid = 0 # Number of char which freq larger equal to k
            
            # move r
            while r < len(s):
                hashmap[s[r]] += 1
                # if hashmap add a new char
                if hashmap[s[r]] == 1:
                    sum_ += 1
                # If freq of value in hashmap larger than k
                if hashmap[s[r]] == k:
                    valid += 1
                
                # Move l until number of char in hashmap less than i
                while sum_ > i:
                    hashmap[s[l]] -= 1
                    if hashmap[s[l]] == 0:
                        sum_ -= 1
                    if hashmap[s[l]] == k-1:
                        valid -= 1
                    l += 1
                # If frequency of all chars in substring larger than k
                if sum_ == i == valid:
                    res = max(res, r-l+1)
                r += 1
        return res
```

```
class Solution:
    def longestSubstring(self, s: str, k: int) -> int:
        res = 0
        
        for i in range(1, 27):
            l, r = 0, 0 
            hashmap = collections.defaultdict(int)
            sum_ = 0 # Number of distinct characters in substring
            valid = 0 # Number of char which freq larger equal to k
            
            while r < len(s):
                hashmap[s[r]] += 1
                if hashmap[s[r]] == 1:
                    sum_ += 1
                if hashmap[s[r]] == k:
                    valid += 1
                    
                while sum_ > i:
                    hashmap[s[l]] -= 1
                    if hashmap[s[l]] == 0:
                        sum_ -= 1
                    if hashmap[s[l]] == k-1:
                        valid -= 1
                    l += 1
                if sum_ == i == valid:
                    res = max(res, r-l+1)
                r += 1
        return res
```

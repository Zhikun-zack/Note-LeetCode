# Tree

### Traversal

### In Order Traversal&#x20;

#### Problem

* [LC 94](by-number/50-100.md#94-binary-tree-inorder-traversal)

#### Solution

1. Iteration

Using one line to do iteration

```
//
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def inorderTraversal(self, root: Optional[TreeNode]) -> List[int]:
        return self.inorderTraversal(root.left) + [root.val] + self.inorderTraversal(root.right) if root else []
```



### BFS

Problem

* [LC 103 ](by-number/100-150.md#103-binary-tree-zigzag-level-order-traversal)

Solution

### DFS

Problem

*   Recursively

    [#427-construct-quad-tree-m](by-number/400-450.md#427-construct-quad-tree-m "mention")

    [#366-find-leaves-of-binary-tree-m](by-number/page-3.md#366-find-leaves-of-binary-tree-m "mention")



### Binary Search Tree

#### Problem

* [LC 230 ](by-number/200-250.md#230-kth-smallest-element-in-a-bst)
* [LC 701](by-number/700-750.md#701-insert-into-a-binary-search-tree)



###


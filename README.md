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



### Binary Search Tree

### Problem

* [LC 230 ](by-number/200-250.md#230-kth-smallest-element-in-a-bst)
* [LC 701](by-number/700-750.md#701-insert-into-a-binary-search-tree)


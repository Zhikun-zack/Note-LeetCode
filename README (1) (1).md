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
* [#662-maximum-width-of-binary-tree-m](by-number/650-700.md#662-maximum-width-of-binary-tree-m "mention")

Solution

### DFS

Problem

*   Recursively

    [#427-construct-quad-tree-m](by-number/400-450.md#427-construct-quad-tree-m "mention")

    [#366-find-leaves-of-binary-tree-m](by-number/page-3.md#366-find-leaves-of-binary-tree-m "mention")

    [#979-distribute-coins-in-binary-tree-m](by-number/950-1000.md#979-distribute-coins-in-binary-tree-m "mention")



### Binary Search Tree

#### Problem

* [LC 230 ](by-number/200-250.md#230-kth-smallest-element-in-a-bst)
* [LC 701](by-number/700-750.md#701-insert-into-a-binary-search-tree)
* Traversal&#x20;
  * [#1008-construct-binary-search-tree-from-preorder-traversal-m](by-number/1000-1050.md#1008-construct-binary-search-tree-from-preorder-traversal-m "mention")
* Build a BST
  * [#96-unique-binary-search-trees](by-number/50-100.md#96-unique-binary-search-trees "mention")



### Prefix Tree (Trie)

* [#208-implement-trie-prefix-tree-m](by-number/200-250.md#208-implement-trie-prefix-tree-m "mention")



### Binary Tree

* [#101-symmetric-tree-e](by-number/100-150.md#101-symmetric-tree-e "mention")

###


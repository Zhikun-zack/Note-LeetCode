# Tree

### Traversal

In pre post order traversal are all DFS

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



### Post-Order-traversal

* [#333-largest-bst-subtree-m](by-number/300-350.md#333-largest-bst-subtree-m "mention")
* [#145-binary-tree-postorder-traversal](by-number/100-150.md#145-binary-tree-postorder-traversal "mention")
* [#106-construct-binary-tree-from-inorder-and-postorder-traversal-m](by-number/100-150.md#106-construct-binary-tree-from-inorder-and-postorder-traversal-m "mention")

### Pre-Order-traversal

* [#144-binary-tree-preorder-traversal-e](by-number/100-150.md#144-binary-tree-preorder-traversal-e "mention")
* [#105-construct-binary-tree-from-preorder-and-inorder-traversal-m](by-number/100-150.md#105-construct-binary-tree-from-preorder-and-inorder-traversal-m "mention")
*

### BFS

Problem

* [LC 103 ](by-number/100-150.md#103-binary-tree-zigzag-level-order-traversal)
* [#662-maximum-width-of-binary-tree-m](by-number/650-700.md#662-maximum-width-of-binary-tree-m "mention")
* [#116-populating-next-right-pointers-in-each-node-m](by-number/100-150.md#116-populating-next-right-pointers-in-each-node-m "mention")
* [#117-populating-next-right-pointers-in-each-node-ii-m](by-number/100-150.md#117-populating-next-right-pointers-in-each-node-ii-m "mention")
* [#107-binary-tree-level-order-traversal-ii-m](by-number/100-150.md#107-binary-tree-level-order-traversal-ii-m "mention")

Solution

### DFS

Problem

*   Recursively

    [#427-construct-quad-tree-m](by-number/400-450.md#427-construct-quad-tree-m "mention")

    [#366-find-leaves-of-binary-tree-m](by-number/page-3.md#366-find-leaves-of-binary-tree-m "mention")

    [#979-distribute-coins-in-binary-tree-m](by-number/950-1000.md#979-distribute-coins-in-binary-tree-m "mention")

    [#337-house-robber-iii-m](by-number/300-350.md#337-house-robber-iii-m "mention")

    [#129-sum-root-to-leaf-numbers-m](by-number/100-150.md#129-sum-root-to-leaf-numbers-m "mention")

    Not DFS but like DFS recursive

    * [#226-invert-binary-tree-e](by-number/200-250.md#226-invert-binary-tree-e "mention")
*   DFS + helper structure

    [#652-find-duplicate-subtrees-m](by-number/650-700.md#652-find-duplicate-subtrees-m "mention")
*   DFS, but not just record node's value

    [#987-vertical-order-traversal-of-a-binary-tree-h](by-number/950-1000.md#987-vertical-order-traversal-of-a-binary-tree-h "mention")
*   DFS, return some values in each dfs function

    [#1110-delete-nodes-and-return-forest-m](by-number/1100-1150.md#1110-delete-nodes-and-return-forest-m "mention")
*   DFS with more parameters

    [#1026-maximum-difference-between-node-and-ancestor-m](by-number/1000-1050.md#1026-maximum-difference-between-node-and-ancestor-m "mention")

    [#1245-tree-diameter-m](by-number/1200-1250.md#1245-tree-diameter-m "mention")



### Binary Search Tree

#### Problem

* [LC 230 ](by-number/200-250.md#230-kth-smallest-element-in-a-bst)
* [LC 701](by-number/700-750.md#701-insert-into-a-binary-search-tree)
* Traversal&#x20;
  * [#1008-construct-binary-search-tree-from-preorder-traversal-m](by-number/1000-1050.md#1008-construct-binary-search-tree-from-preorder-traversal-m "mention")
  *   BFS inorder traversal

      [#99-recover-binary-search-tree-m](by-number/50-100.md#99-recover-binary-search-tree-m "mention")&#x20;

      *   Find the successor and predecessor

          [#450-delete-node-in-a-bst-m](by-number/400-450.md#450-delete-node-in-a-bst-m "mention")

          [#510-inorder-successor-in-bst-ii-m](by-number/500-550.md#510-inorder-successor-in-bst-ii-m "mention")
* Recursion
  * 109&#x20;
* Build a BST
  * [#96-unique-binary-search-trees](by-number/50-100.md#96-unique-binary-search-trees "mention")



### Prefix Tree (Trie)

* [#208-implement-trie-prefix-tree-m](by-number/200-250.md#208-implement-trie-prefix-tree-m "mention")



### Binary Tree

* [#101-symmetric-tree-e](by-number/100-150.md#101-symmetric-tree-e "mention")
* Recursion
  * 894&#x20;

## Priority Queue

* [#703-kth-largest-element-in-a-stream-e](by-number/700-750.md#703-kth-largest-element-in-a-stream-e "mention")

## Trie

* [#1166-design-file-system-m](by-number/1150-1200.md#1166-design-file-system-m "mention")

## Serialization And Deserialization

* [#428-serialize-and-deserialize-n-ary-tree-h](by-number/400-450.md#428-serialize-and-deserialize-n-ary-tree-h "mention")
* [#889-construct-binary-tree-from-preorder-and-postorder-traversal-m](by-number/850-900.md#889-construct-binary-tree-from-preorder-and-postorder-traversal-m "mention")
* [#95-unique-binary-search-trees-ii-m](by-number/50-100.md#95-unique-binary-search-trees-ii-m "mention")
* [#108-convert-sorted-array-to-binary-search-tree-e](by-number/100-150.md#108-convert-sorted-array-to-binary-search-tree-e "mention")

## LCA

* [#235-lowest-common-ancestor-of-a-binary-search-tree-e](by-number/200-250.md#235-lowest-common-ancestor-of-a-binary-search-tree-e "mention")
* [#1123-lowest-common-ancestor-of-deepest-leaves-m](by-number/1100-1150.md#1123-lowest-common-ancestor-of-deepest-leaves-m "mention")
  * [#865-smallest-subtree-with-all-the-deepest-nodes-m](by-number/850-900.md#865-smallest-subtree-with-all-the-deepest-nodes-m "mention")
* [#1676-lowest-common-ancestor-of-a-binary-tree-iv](by-number/1650-1700.md#1676-lowest-common-ancestor-of-a-binary-tree-iv "mention")

## Tree Path

* [#257-binary-tree-paths-e](by-number/250-300.md#257-binary-tree-paths-e "mention")
* [#687-longest-univalue-path-m](by-number/650-700.md#687-longest-univalue-path-m "mention")
* Using recursion, each recursion function return some values:
  * [#1372-longest-zigzag-path-in-a-binary-tree](by-number/1350-1400.md#1372-longest-zigzag-path-in-a-binary-tree "mention")
  * [#124-binary-tree-maximum-path-sum-h](by-number/100-150.md#124-binary-tree-maximum-path-sum-h "mention")
  * [#549-binary-tree-longest-consecutive-sequence-ii-m](by-number/500-550.md#549-binary-tree-longest-consecutive-sequence-ii-m "mention")
  * [#1120-maximum-average-subtree-m](by-number/1100-1150.md#1120-maximum-average-subtree-m "mention")

## Others

* Recursion (top down or bottom up)
  * [#110-balanced-binary-tree-e](by-number/100-150.md#110-balanced-binary-tree-e "mention")
  * [#617-merge-two-binary-trees](by-number/600-650.md#617-merge-two-binary-trees "mention")


# Binary Search Tree Height

**Difficulty:** Medium  
**Topic:** Trees

Compute the height of a binary tree given its root.

## Approach
Recursively compute max depth of left and right subtrees.

## Complexity
O(n) time, O(h) space

## Solution
```python
def solve(root):
    def height(node):
        if not node:
            return -1
        return 1+max(height(node.left),height(node.right))
    return height(root)
```

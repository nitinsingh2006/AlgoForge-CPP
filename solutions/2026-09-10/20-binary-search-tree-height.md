# Binary Search Tree Height

**Difficulty:** Medium  
**Topic:** Trees

Compute height of a binary tree given its root.

## Approach
Recursive depth-first traversal.

## Complexity
O(n) time, O(h) space

## Solution
```python
def solve(root):
    if not root:
        return -1
    return 1+max(solve(root.left),solve(root.right))
```

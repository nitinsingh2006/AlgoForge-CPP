# Find Duplicate in Array

**Difficulty:** Easy  
**Topic:** Hashing

Given n+1 integers 1..n, find the duplicate number.

## Approach
Apply Floyd's Tortoise and Hare cycle detection.

## Complexity
O(n) time, O(1) space

## Solution
```python
def find_duplicate(nums): slow=nums[0]; fast=nums[nums[0]];\n    while slow!=fast:\n        slow=nums[slow]; fast=nums[nums[fast]]\n    slow=0;\n    while slow!=fast:\n        slow=nums[slow]; fast=nums[fast]\n    return slow
```

# Find Duplicate

**Difficulty:** Easy  
**Topic:** Hashing

In an array of n+1 integers 1..n, find the duplicate number.

## Approach
Use Floyd's cycle detection on the value graph.

## Complexity
O(n) time, O(1) space

## Solution
```python
def find_duplicate(nums):\n    slow=fast=nums[0]\n    while True:\n        slow=nums[slow]\n        fast=nums[nums[fast]]\n        if slow==fast:\n            break\n    slow=nums[0]\n    while slow!=fast:\n        slow=nums[slow]\n        fast=nums[fast]\n    return slow
```

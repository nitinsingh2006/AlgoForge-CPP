# Find Duplicate in Array

**Difficulty:** Medium  
**Topic:** Arrays

Given an array of n+1 integers where each integer is between 1 and n inclusive, find the duplicate number. The array contains exactly one duplicate, which may appear multiple times.

## Approach
Use Floyd's cycle detection algorithm.

## Complexity
O(n) time, O(1) space.

## Solution
```python
def findDuplicate(nums):
    slow = nums[0]
    fast = nums[nums[0]]
    while slow != fast:
        slow = nums[slow]
        fast = nums[nums[fast]]
    slow = 0
    while slow != fast:
        slow = nums[slow]
        fast = nums[fast]
    return slow
```

# Find Duplicate Number

**Difficulty:** Medium  
**Topic:** Arrays

In an array of n+1 integers where each integer is between 1 and n, find the duplicate number.

## Approach
Use Floyd's Tortoise and Hare cycle detection.

## Complexity
O(n) time, O(1) space

## Solution
```python
def find_duplicate(nums):
    slow=fast=nums[0]
    while True:
        slow=nums[slow]
        fast=nums[nums[fast]]
        if slow==fast:
            break
    slow=nums[0]
    while slow!=fast:
        slow=nums[slow]
        fast=nums[fast]
    return slow
```

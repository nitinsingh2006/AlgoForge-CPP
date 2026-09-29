# Find Duplicate

**Difficulty:** Easy  
**Topic:** Hashing

In an array of n+1 integers where each integer is between 1 and n, find the duplicate number.

## Approach
Apply Floyd's Tortoise and Hare cycle detection to locate the duplicate.

## Complexity
O(n) time, O(1) space

## Solution
```python
def find_duplicate(nums):
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

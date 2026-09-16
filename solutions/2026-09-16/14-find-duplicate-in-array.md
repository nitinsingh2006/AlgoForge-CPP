# Find Duplicate in Array

**Difficulty:** Medium  
**Topic:** Arrays

Given an array of n+1 integers where each integer is between 1 and n inclusive, find the duplicate number.

## Approach
Use Floyd's Tortoise and Hare cycle detection.

## Complexity
O(n) time, O(1) space

## Solution
```python
def find_duplicate(nums):
    tortoise=nums[0]
    hare=nums[nums[0]]
    while tortoise!=hare:
        tortoise=nums[tortoise]
        hare=nums[nums[hare]]
    tortoise=0
    while tortoise!=hare:
        tortoise=nums[tortoise]
        hare=nums[hare]
    return hare
```

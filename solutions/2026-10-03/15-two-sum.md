# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target sum, return indices of two numbers that add up to the target.

## Approach
Use a hash map to store each number's index while iterating.

## Complexity
O(n) time, O(n) space

## Solution
```python
def two_sum(nums, target):
    d = {}
    for i, num in enumerate(nums):
        if target - num in d:
            return [d[target - num], i]
        d[num] = i
    return []
```

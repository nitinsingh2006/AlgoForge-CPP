# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target, return indices of two numbers that add up to the target.

## Approach
Use a hash map to store numbers and their indices while iterating.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums, target):
    seen = {}
    for i, num in enumerate(nums):
        complement = target - num
        if complement in seen:
            return [seen[complement], i]
        seen[num] = i
    return []
```

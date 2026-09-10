# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target, return indices of two numbers that add up to the target.

## Approach
Use a hash map to store numbers and their indices.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums, target):\n    lookup = {}\n    for i, num in enumerate(nums):\n        if target - num in lookup:\n            return [lookup[target - num], i]\n        lookup[num] = i\n    return []
```

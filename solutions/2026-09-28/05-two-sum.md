# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target sum, return indices of two numbers that add up to the target.

## Approach
Use a hash map to store numbers and their indices while iterating.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve_two_sum(nums, target):\n    seen = {}\n    for i, num in enumerate(nums):\n        diff = target - num\n        if diff in seen:\n            return [seen[diff], i]\n        seen[num] = i\n    return []
```

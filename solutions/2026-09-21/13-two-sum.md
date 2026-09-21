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
def solve(nums,target):\n    d={}\n    for i,num in enumerate(nums):\n        if target-num in d:\n            return [d[target-num],i]\n        d[num]=i\n    return []
```

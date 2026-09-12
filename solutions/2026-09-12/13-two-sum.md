# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target, return indices of two numbers that sum to target.

## Approach
Use a hash map to store seen numbers and their indices.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums,target):\n    seen={}\n    for i,n in enumerate(nums):\n        if target-n in seen:\n            return [seen[target-n],i]\n        seen[n]=i\n    return []
```

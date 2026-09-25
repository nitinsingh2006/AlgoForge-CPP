# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target sum, return indices of two numbers that add up to the target.

## Approach
Use a hash map to store numbers and indices while iterating.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums,target):d={};[d.update({n:i}) or None for i,n in enumerate(nums) if target-n in d and d.update({target-n:i})]
```

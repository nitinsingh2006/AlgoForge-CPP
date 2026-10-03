# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target sum, return indices of two numbers that add up to the target. Each input has exactly one solution, and you cannot reuse the same element. Return indices in any order.

## Approach
Use a hash map.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums,target):seen={};for i,x in enumerate(nums):if target-x in seen:return[seen[target-x],i];seen[x]=i;return []
```

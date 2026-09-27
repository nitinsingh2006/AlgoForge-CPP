# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target sum, return indices of two numbers that add up to target.

## Approach
Use a hash map to store complements.

## Complexity
O(n) time, O(n) space

## Solution
```python
def two_sum(nums, target):
    d={}
    for i,num in enumerate(nums):
        comp=target-num
        if comp in d:
            return [d[comp],i]
        d[num]=i
    return []
```

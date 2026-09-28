# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target, return indices of two numbers that sum to the target.

## Approach
Use a hash map to store seen numbers.

## Complexity
O(n) time, O(n) space

## Solution
```python
def two_sum(nums,target):
    seen={}
    for i,n in enumerate(nums):
        if target-n in seen:
            return [seen[target-n],i]
        seen[n]=i
    return []
```

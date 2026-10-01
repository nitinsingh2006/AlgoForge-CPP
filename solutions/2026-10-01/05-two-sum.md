# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target, return indices of two numbers that add up to target.

## Approach
Use a hash map to store seen numbers.

## Complexity
O(n) time, O(n) space

## Solution
```python
def two_sum(nums,target):
    seen={}
    for i,num in enumerate(nums):
        diff=target-num
        if diff in seen:
            return [seen[diff],i]
        seen[num]=i
    return []
```

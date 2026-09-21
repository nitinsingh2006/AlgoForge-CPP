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
def solve(nums,target):
    h={}
    for i,n in enumerate(nums):
        if target-n in h:
            return [h[target-n],i]
        h[n]=i
    return None
```

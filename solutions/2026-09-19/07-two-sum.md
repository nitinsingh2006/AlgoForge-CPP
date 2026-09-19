# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target, return indices of two numbers that add up to target. Each input has exactly one solution, and you cannot reuse an element.

## Approach
Use a hash map to store numbers and their indices while iterating.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums, target):
    d={}
    for i,n in enumerate(nums):
        if target-n in d:
            return [d[target-n], i]
        d[n]=i
    return []
```

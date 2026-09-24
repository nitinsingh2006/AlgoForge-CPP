# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers nums and an integer target, return the indices of the two numbers that add up to target. Assume exactly one solution exists and you cannot use the same element twice.

## Approach
Use a hash map to store numbers and their indices while iterating.

## Complexity
O(n) time, O(n) space

## Solution
```python
def two_sum(nums,target):
    d={}
    for i,num in enumerate(nums):
        comp=target-num
        if comp in d:
            return [d[comp],i]
        d[num]=i
    return []
```

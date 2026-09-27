# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target sum, return indices of two numbers that add up to the target. Each input has exactly one solution, and you cannot reuse the same element.

## Approach
Iterate through the array, storing each number's complement in a hash map. When a number's complement is found, return the indices.

## Complexity
O(n) time, O(n) space

## Solution
```python
def two_sum(nums,target):
    seen={}
    for i,n in enumerate(nums):
        if n in seen:
            return [seen[n],i]
        seen[target-n]=i
```

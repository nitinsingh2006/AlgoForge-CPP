# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target, return indices of two numbers that sum to the target.

## Approach
Iterate through the array, storing each number and its index in a hash map. For each element, check if the complement exists in the map. If so, return the pair of indices.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums,target):
    seen={}
    for i,n in enumerate(nums):
        comp=target-n
        if comp in seen:
            return [seen[comp],i]
        seen[n]=i
    return []
```

# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target value, return the indices of two numbers that sum to the target. Indices are zero‑based and each input has exactly one solution.

## Approach
Use a hash map to store seen numbers.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums,target):d={};
for i,n in enumerate(nums):
 if target-n in d:
  return [d[target-n],i]
 d[n]=i
return []
```

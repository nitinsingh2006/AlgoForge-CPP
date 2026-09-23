# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find two indices in an array such that the numbers at those indices add up to a given target. Return the indices as a list. Assume exactly one solution exists and you cannot use the same element twice.

## Approach
Use a hash map to store numbers and their indices while iterating.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums, target):\n    d={}\n    for i,n in enumerate(nums):\n        if target-n in d:\n            return [d[target-n], i]\n        d[n]=i\n    return []
```

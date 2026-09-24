# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find two indices of numbers that add up to target.

## Approach
Use a hash map to store complements.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums,target):\n    d={}\n    for i,n in enumerate(nums):\n        if n in d:\n            return [d[n],i]\n        d[target-n]=i\n    return []
```

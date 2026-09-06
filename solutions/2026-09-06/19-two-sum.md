# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find two indices in an array that sum to a target value.

## Approach
Use a hash map to store numbers and their indices.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums,target): d={};\n    for i,n in enumerate(nums):\n        if target-n in d:\n            return [d[target-n],i]\n        d[n]=i\n    return []
```

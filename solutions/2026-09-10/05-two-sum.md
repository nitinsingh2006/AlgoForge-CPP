# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find two indices in an array that sum to a target. Return indices or empty list.

## Approach
Use a hash map.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums, target):
    d={}
    for i, num in enumerate(nums):
        if target-num in d:
            return [d[target-num], i]
        d[num]=i
    return []
```

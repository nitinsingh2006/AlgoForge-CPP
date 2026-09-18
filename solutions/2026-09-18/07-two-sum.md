# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find two indices in an array such that the numbers add up to a target sum. Return the indices as a list. If no solution, return empty list.

## Approach
Use a hash map.

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

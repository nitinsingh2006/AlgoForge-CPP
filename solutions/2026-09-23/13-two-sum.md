# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find two indices in an array whose values sum to a target. Return the indices.

## Approach
Use a hash map to store seen numbers and their indices.

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

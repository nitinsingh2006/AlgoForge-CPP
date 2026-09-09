# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers, find two indices whose values sum to a target. Return indices in any order.

## Approach
Use a hash map to store seen numbers and their indices.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums,target):
    seen={}
    for i,num in enumerate(nums):
        if target-num in seen:
            return [seen[target-num],i]
        seen[num]=i
    return []
```

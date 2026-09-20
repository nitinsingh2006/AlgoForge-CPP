# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find two indices in an integer array such that the numbers at those indices add up to a given target. Return the indices as a list. If no solution exists, return an empty list.

## Approach
Use a hash map to store numbers and their indices while iterating.

## Complexity
O(n) time, O(n) space

## Solution
```python
def two_sum(nums, target):
    lookup={}
    for i, num in enumerate(nums):
        complement=target-num
        if complement in lookup:
            return [lookup[complement], i]
        lookup[num]=i
    return []
```

# Unique Pair Sum Count

**Difficulty:** Easy  
**Topic:** Arrays

Given an integer array and a target, count distinct unordered pairs that sum to target.

## Approach
Use a set to track seen numbers and another set for pairs.

## Complexity
O(n) time, O(n) space

## Solution
```python
def count_pairs(nums,target):
    seen=set();pairs=set()
    for x in nums:
        y=target-x
        if y in seen:
            pairs.add(tuple(sorted((x,y))))
        seen.add(x)
    return len(pairs)
```

# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find two indices in an array that sum to a target.

## Approach
Use a hash map to store seen numbers.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums, target):
    hashmap = {}
    for i, num in enumerate(nums):
        if target - num in hashmap:
            return [hashmap[target - num], i]
        hashmap[num] = i
    return []
```

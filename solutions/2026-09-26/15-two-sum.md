# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find two indices in an integer array such that their values sum to a given target. Return the indices as a list. If no solution exists, return an empty list.

## Approach
Use a hash map to store numbers and their indices while iterating. For each number, check if the complement (target - number) exists in the map. If found, return the pair of indices.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums, target):\n    lookup={}\n    for i, num in enumerate(nums):\n        if target-num in lookup:\n            return [lookup[target-num], i]\n        lookup[num]=i\n    return []
```

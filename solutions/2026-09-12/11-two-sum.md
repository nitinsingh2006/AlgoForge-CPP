# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target value, return indices of two numbers that add up to target. Each input has exactly one solution, and you cannot reuse an element.

## Approach
Iterate through array, store each number's index in a hash map. For each element, check if target minus element exists in map. If so, return indices.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums, target):\n    lookup = {}\n    for i, num in enumerate(nums):\n        if target - num in lookup:\n            return [lookup[target - num], i]\n        lookup[num] = i\n    return []
```

# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target sum, return indices of two numbers that add up to the target. Each input has exactly one solution, and you cannot use the same element twice.

## Approach
Iterate through the array, storing each number and its index in a hash map. For each number, check if the complement (target - number) exists in the map.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums, target):\n    lookup = {}\n    for i, num in enumerate(nums):\n        comp = target - num\n        if comp in lookup:\n            return [lookup[comp], i]\n        lookup[num] = i\n    return []
```

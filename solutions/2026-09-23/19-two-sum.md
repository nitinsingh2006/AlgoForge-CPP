# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find two indices in an array that add up to a target sum.

## Approach
Use a hash map to store seen numbers and their indices.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums, target):\n    seen = {}\n    for i, num in enumerate(nums):\n        comp = target - num\n        if comp in seen:\n            return [seen[comp], i]\n        seen[num] = i\n    return []
```

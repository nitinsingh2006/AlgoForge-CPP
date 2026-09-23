# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Given an integer array, find the contiguous subarray with the largest sum and return that sum.

## Approach
Kadane's algorithm tracks current and global maximum while iterating.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):\n    max_ending=max_so_far=nums[0]\n    for n in nums[1:]:\n        max_ending=max(n,max_ending+n)\n        max_so_far=max(max_so_far,max_ending)\n    return max_so_far
```

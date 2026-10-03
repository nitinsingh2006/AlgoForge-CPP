# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Find the contiguous subarray within an array that has the largest sum.

## Approach
Kadane's algorithm keeps track of current and global maximum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):\n    max_ending=max_so_far=nums[0]\n    for n in nums[1:]:\n        max_ending=max(n,max_ending+n)\n        max_so_far=max(max_so_far,max_ending)\n    return max_so_far
```

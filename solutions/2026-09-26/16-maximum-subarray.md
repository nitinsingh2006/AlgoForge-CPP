# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an integer array, find the contiguous subarray with the largest sum and return that sum.

## Approach
Apply Kadane's algorithm: iterate through the array, maintaining the maximum sum ending at the current position and the overall maximum. Update these values in O(1) space.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):\n    max_ending_here = max_so_far = nums[0]\n    for x in nums[1:]:\n        max_ending_here = max(x, max_ending_here + x)\n        max_so_far = max(max_so_far, max_ending_here)\n    return max_so_far
```

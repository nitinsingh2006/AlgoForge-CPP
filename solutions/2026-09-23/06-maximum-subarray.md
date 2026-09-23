# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an integer array, find the contiguous subarray with the largest sum and return that sum. Use Kadane's algorithm to achieve linear time.

## Approach
Iterate through the array, keeping track of the maximum sum ending at the current position and the overall best sum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    max_ending=best=nums[0]\n    for x in nums[1:]:\n        max_ending=max(x, max_ending+x)\n        best=max(best, max_ending)\n    return best
```

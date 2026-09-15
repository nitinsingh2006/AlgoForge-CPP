# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, find the contiguous subarray with the largest sum.

## Approach
Kadane's algorithm maintains current and maximum sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def maxSubArray(nums):\n    max_so_far=nums[0]\n    max_ending_here=nums[0]\n    for num in nums[1:]:\n        max_ending_here=max(num,max_ending_here+num)\n        max_so_far=max(max_so_far,max_ending_here)\n    return max_so_far
```

# Maximum Subarray Sum

**Difficulty:** Easy  
**Topic:** DP

Given an integer array nums, find the contiguous subarray with the largest sum and return that sum.

## Approach
Apply Kadane's algorithm to track current and maximum sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums): max_ending=0; max_so_far=float('-inf'); for x in nums: max_ending=max(x,max_ending+x); max_so_far=max(max_so_far,max_ending); return max_so_far
```

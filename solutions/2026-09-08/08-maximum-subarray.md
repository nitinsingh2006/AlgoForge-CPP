# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, find the contiguous subarray with the largest sum and return that sum. The subarray must contain at least one element.

## Approach
Kadane's algorithm.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):max_ending=nums[0];max_so_far=nums[0];
for n in nums[1:]:
 max_ending=max(n,max_ending+n)
 max_so_far=max(max_so_far,max_ending)
return max_so_far
```

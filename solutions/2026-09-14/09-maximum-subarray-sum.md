# Maximum Subarray Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers, find the maximum sum of a contiguous subarray.

## Approach
Kadane's algorithm.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):max_ending=max_so_far=nums[0];for x in nums[1:]:max_ending=max(x,max_ending+x);max_so_far=max(max_so_far,max_ending);return max_so_far
```

# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an integer array, find the contiguous subarray with the largest sum and return that sum.

## Approach
Use Kadane's algorithm to track current and maximum sums while iterating.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):max_so_far=curr=nums[0];for x in nums[1:]:curr=max(x,curr+x);max_so_far=max(max_so_far,curr);return max_so_far
```

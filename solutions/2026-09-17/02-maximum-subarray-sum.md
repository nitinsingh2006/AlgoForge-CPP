# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an integer array nums, find the contiguous subarray with the largest sum and return that sum.

## Approach
Use Kadane's algorithm: iterate, keep current sum and max sum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def maxSubArray(nums): max_so_far=curr=nums[0]; for num in nums[1:]: curr=max(num,curr+num); max_so_far=max(max_so_far,curr); return max_so_far
```

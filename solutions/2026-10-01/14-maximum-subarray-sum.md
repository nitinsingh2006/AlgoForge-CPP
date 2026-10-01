# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, find the contiguous subarray with the largest sum.

## Approach
Use Kadane's algorithm to track current and max sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def maxSubArray(nums):
    max_so_far=nums[0]
    curr=nums[0]
    for num in nums[1:]:
        curr=max(num,curr+num)
        max_so_far=max(max_so_far,curr)
    return max_so_far
```

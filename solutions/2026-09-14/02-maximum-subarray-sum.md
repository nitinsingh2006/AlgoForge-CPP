# Maximum Subarray Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an integer array, find the maximum sum of a contiguous subarray.

## Approach
Kadane's algorithm maintains current and global max.

## Complexity
O(n) time, O(1) space

## Solution
```python
def maxSubArray(nums):
    max_ending=max_global=nums[0]
    for num in nums[1:]:
        max_ending=max(num,max_ending+num)
        max_global=max(max_global,max_ending)
    return max_global
```

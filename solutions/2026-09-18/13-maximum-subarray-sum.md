# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array nums, return the maximum sum of any contiguous subarray.

## Approach
Iterate once, keep current sum and max sum; reset current sum to 0 if negative.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    max_sum=cur=nums[0]\n    for x in nums[1:]:\n        cur=max(x,cur+x)\n        max_sum=max(max_sum,cur)\n    return max_sum
```

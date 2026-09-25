# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, return the largest sum of any contiguous subarray.

## Approach
Iterate, keep current sum and max sum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    cur=max_sum=nums[0]\n    for num in nums[1:]:\n        cur=max(num,cur+num)\n        max_sum=max(max_sum,cur)\n    return max_sum
```

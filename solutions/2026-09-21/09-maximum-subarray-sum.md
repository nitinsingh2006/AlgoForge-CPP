# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, return the sum of the contiguous subarray with the largest sum.

## Approach
Iterate once, keeping current and maximum sums (Kadane).

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    cur=max_sum=nums[0]\n    for x in nums[1:]:\n        cur=max(x,cur+x)\n        max_sum=max(max_sum,cur)\n    return max_sum
```

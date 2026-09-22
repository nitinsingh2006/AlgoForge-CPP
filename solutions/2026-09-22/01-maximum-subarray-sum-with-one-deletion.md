# Maximum Subarray Sum with One Deletion

**Difficulty:** Medium  
**Topic:** Arrays,DP

Given an integer array, you may delete at most one element. Return the maximum sum of any contiguous subarray after the deletion. If no deletion improves the sum, return the maximum subarray sum without deletion.

## Approach
Use two DP arrays: keep track of max sum ending at i without deletion and with one deletion. Update iteratively, taking max of current element, previous sum plus current, or previous sum without deletion. Track global maximum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray_sum_with_one_deletion(nums):\n    n=len(nums)\n    if n==0: return 0\n    dp0=nums[0]\n    dp1=0\n    best=dp0\n    for i in range(1,n):\n        dp1=max(dp0, dp1+nums[i])\n        dp0=max(dp0+nums[i], nums[i])\n        best=max(best, dp0, dp1)\n    return best
```

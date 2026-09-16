# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, find the maximum sum of any contiguous subarray.

## Approach
Iterate once, keeping current and best sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums): cur=best=nums[0]; for x in nums[1:]: cur=max(x,cur+x); best=max(best,cur); return best
```
